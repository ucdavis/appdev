---
layout: event
title:  "NoSQL and Elasticsearch, Updates on Open Source Policy"
description: "Christopher Thielen delivers an overview of the NoSQL landscape and dives into the specifics of the very useful Elasticsearch database. Shawn DeArmond presents updates on the Open Source guidelines."
author: "Christopher Thielen"
date:   2017-10-10
event-time: 11:00AM - 12:00PM
event-location: "2005 Plant Sciences"
tags: "nosql, elasticsearch, open source policy"
category: "events"
---

NoSQL Overview + Elasticsearch Quick Dive
-
Christopher Thielen presented an overview of the NoSQL database field and delivered a quick dive into Elasticsearch with examples.

The following examples (based on CURL but feel free to adapt them) will work from any computer until at least Friday, October 13, 2017. Please play around!

*Any title with the word 'Homer'*
{% highlight bash %}
# Copy-and-paste version
# curl -X POST https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search -H 'cache-control: no-cache' -H 'postman-token: 7f72d86e-e48d-1aad-f67a-1212ef99f035' -d '{"query": {"match": {"title": "Homer"}}}'

# Easy-to-read version
curl -X POST \
  https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 7f72d86e-e48d-1aad-f67a-1212ef99f035' \
  -d '{
	"query": {
		"match": {
			"title": "Homer"
		}
	}
}'
{% endhighlight %}

*Any title with the word 'Homer' and an IMDB rating not greater than 7*
{% highlight bash %}
# Copy-and-paste version
# curl -X POST https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search -H 'cache-control: no-cache' -H 'postman-token: 12ae77e0-3ffa-67d5-d606-72178d0513f8' -d '{"query": {"bool": {"must": { "match": {"title": "homer"} },"must_not": { "range": { "imdb_rating": { "gt": 7 } }}}}}'

# Easy-to-read version
curl -X POST \
  https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 12ae77e0-3ffa-67d5-d606-72178d0513f8' \
  -d '{
	"query": {
		"bool": {
			"must": { "match": {"title": "homer"} },
			"must_not": { "range": { "imdb_rating": { "gt": 7 } }}
		}
	}
}'
{% endhighlight %}

*Any script with the words 'makes me laugh' (not necessarily in that order)*
{% highlight bash %}
# Copy-and-paste version
# curl -X POST https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search -H 'cache-control: no-cache' -H 'postman-token: 73f5bb29-2276-0013-7eb5-38b65e168a25' -d '{"query": {"match": {"spoken_words": "makes me laugh"}}}'

# Easy-to-read version
curl -X POST \
  https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 73f5bb29-2276-0013-7eb5-38b65e168a25' \
  -d '{
	"query": {
		"match": {
			"spoken_words": "makes me laugh"
		}
	}
}'
{% endhighlight %}

*Any script with the phrase 'makes me laugh' (in that order)*
{% highlight bash %}
# Copy-and-paste version
# curl -X POST https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search -H 'cache-control: no-cache' -H 'postman-token: db2e6a72-23fd-3a96-5f3a-1d23f2425d5a' -d '{"query": {"match_phrase": {"spoken_words": "makes me laugh"}}}'

# Easy-to-read version
curl -X POST \
  https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search \
  -H 'cache-control: no-cache' \
  -H 'postman-token: db2e6a72-23fd-3a96-5f3a-1d23f2425d5a' \
  -d '{
	"query": {
		"match_phrase": {
			"spoken_words": "makes me laugh"
		}
	}
}'
{% endhighlight %}

*Search for 'ECS 110', biasing ECS as a more important term*
{% highlight bash %}
# Copy-and-paste version
# curl -X POST https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search -H 'cache-control: no-cache' -H 'postman-token: 924a7c0a-4c72-43c8-bbd6-7f6564c8351d' -d '{ "query": { "bool": { "should": [{ "match": { "scbcrse_subj_code": { "query":  "ecs 110", "boost": 2 } }},{ "match": { "scbcrse_crse_numb": "ecs 110" }}]}}}'

# Easy-to-read version
curl -X POST \
  https://search-appdev-i5jscncns7bsko2a25cqvhcyni.us-west-2.es.amazonaws.com/simpsons/_search \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 924a7c0a-4c72-43c8-bbd6-7f6564c8351d' \
  -d '{
    "query": {
		"bool": {
		    "should": [
		    	{ "match": { "scbcrse_subj_code": { "query":  "ecs 110", "boost": 2 } }},
		    	{ "match": { "scbcrse_crse_numb": "ecs 110" }}
			]
		}
	}
}'
{% endhighlight %}

Note: The graphical CURL tool used was [Postman](https://www.getpostman.com/).

Slides: [PDF]({{ site.baseurl }}/media/meetings/14/nosql_es.pdf) [PPTX]({{ site.baseurl }}/media/meetings/14/nosql_es.pptx)

Open Source Policy Guideline Update
-
Shawn DeArmond delivered an update on the evolving open source policy guidelines, focusing on both using open source software internally as well as open sourcing UC-produced software.

Contact Shawn for a copy of the hand-out.

Miscellaneous
=
There were **15 individuals in attendance**.
