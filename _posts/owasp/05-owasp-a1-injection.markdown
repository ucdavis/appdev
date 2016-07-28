---
layout: article
title: "A1. Injection"
description: "Injection Attacks"
date: 2016-07-25
category: "owasp"
image:
breadcrumb: Owasp
---

# A1. Injection
#### 25 July 2016

While finding injection attacks may present challenges, once an attacker discovers security holes the injections require little effort. Injection attacks offer a high ROI (often in the form of data). 

### Injection Flaws
We have an injection flaw anytime an attacker can access a data source; SQL injection offers the most popular route, but other forms exist as well: XPath, LDAP, Command, File, and NoSQL.

### Attacks
In a typical attack, the threat agent passes SQL through a search input to dump a database.
```
// returns Category ID 2228 (perhaps books)
http://e-commerce.com/items/subcat.php?cat_id=2228

// attacker tests options... 
//   such as an "always true" value:
http://e-commerce.com/items/subcat.php?cat_id=2228' OR `1`=`1`
//   tries a UNION:
http://e-commerce.com/items/subcat.php?cat_id=2228' UNION SELECT username, password FROM users
//   or even attempts to drop a table:
http://e-commerce.com/items/subcat.php?cat_id=2228' AND DROP TABLE users
```

Advanced SQL injection may involve executing OS-level commands, like `EXEC` on MSSQL... 
```
EXEC master.dbo.xp_cmdshell `DIR`
```
...or I/O commands on MySQL:
```
UNION SELECT LOAD_FILE('/etc/passwd');
UNION SELECT 'File Content' INTO OUTFILE '/tmp/file'; 
```

Attackers with greater understanding may utilize hexadecimal injection and slow complex queries to hide from an IDS.

### Case Study: ABC Manufacturing
ABC Manufacturing has critical R&D information, primarily blueprints and architectural designs for their product lines. ABC Manufacturing has multiple locations with robust and mature IT support.

#### Goals
1. Get access to critical R&D info, externally _or_ internally
2. Use any and all methods available
3. Simulate real-world attacks

#### The Incursion
Researcher notices an ASP.Net HR application connecting to an MSSQL Server. Initial attacks utilize SQL injection which succeeds; database runs as root. MSSQL keeps the execute feature off by default, but once the attacker has root access, s/he can enable execution and dump a list of running executables on the machine. The attacker knows Microsoft uses Kerberos tokens with a lifespan of 8 hours, and it just so happens that the domain administrator has tokens on the system. After hijacking the domain admin's tokens, the attacker creates users on the domain with admin rights, granting access to _all_ accessible files, including the critical R&D info.

One single attack vector (in this case, SQL injection) results in the attacker getting access to everything, including trade secrets.

### Alternate Approaches
**XPath Injection** utilizes XML queries instead of SQL.
**LDAP Injection** rarely occurs; MS Active Directory and OpenLDAP fare well against these attacks.
**Command Injection**: if you can pass a parameter to a command, and the command does not validate the input, you can pipe the command to another executable (stay away from OS-level commands in web applications. 
**File Injection**: on a form that allows uploads, attackers may successfully upload an executable shell and gain access to the filesystem.
**NoSQL Injection** occurs in document databases; attackers may retrieve all documents with a single query. NoSQL databases have little security documentation and ship with insecure defaults.
