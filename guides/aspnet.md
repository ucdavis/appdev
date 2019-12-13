---
layout: page
title: .NET Platform Recommendations
permalink: /guides/aspnet
---

Curabitur accumsan facilisis libero hendrerit finibus. Aenean condimentum volutpat lacus a maximus. Curabitur elementum pharetra tortor, ac aliquam est tempor tempus. Duis nec efficitur orci.

# Source Control

UC Davis has a thriving GitHub organization at [https://github.com/ucdavis/](https://github.com/ucdavis/).
It is available to utilize for free if you are affiliated with UC Davis, for public or private repos and unlimited collaborators.

More information on the GitHub service, including how to get started, is available at [https://itcatalog.ucdavis.edu/service/github](https://itcatalog.ucdavis.edu/service/github)

# License

We recommend that applications built at UC Davis be released under an [open source license](https://developers.ucdavis.edu/opensource/) whenever possible.  Following the spirit of [the UCOP Open Access Policy](https://osc.universityofcalifornia.edu/open-access-at-uc/open-access-policy/), in which all research articles authored by faculty are made available to the public, we believe the software we create should also be available to the public.   

# .NET Framework

Both ASP.NET 4.x and ASP.NET Core are enterprise-grade, fully supported platforms for building modern applications.  [Both are great choices](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/choose-aspnet-framework) for building applications at UC Davis.

**For building new applications ASP.NET Core is recommended** for several reasons:

1. [.NET 5 (the next major release)](https://devblogs.microsoft.com/dotnet/introducing-net-5/) will be the single framework going forward.  It will be built on .NET Core and will leave behind some features of .NET 4.x (like Web Forms, WCF, WWF, etc)
1. ASP.NET Core works on Windows, macOS, or Linux, which gives the widest array of options for application deployment.
1. ASP.NET Core is has much [higher performance](https://github.com/aspnet/benchmarks) and less overhead, which is very useful when doing cloud deployments.

# Authentication

Authentication at UC Davis is mainly based around using the [CAS Authentication Service](https://itcatalog.ucdavis.edu/service/central-authentication-service-cas), but you may also consider using basic (username/password) authentication or social logins.  

## Using CAS

The recommended library for using CAS is [https://github.com/IUCrimson/AspNet.Security.CAS](https://github.com/IUCrimson/AspNet.Security.CAS).  In development use [https://ssodev.ucdavis.edu/cas/](https://ssodev.ucdavis.edu/cas/) as your server base url, and in product it'll be [https://cas.ucdavis.edu/cas](https://cas.ucdavis.edu/cas).  Don't forget to register your application with [http://casmgr.ucdavis.edu/](http://casmgr.ucdavis.edu/) before you deploy to production.

## Password or Social Logins

Using the [ASP.NET Core Identity Prodvider](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity) is the simplest and most secure way to get started.  You can even view the [entire source code](https://github.com/aspnet/AspNetCore/tree/master/src/Identity) for the provider if you wish, though it isn't necessary.

# JavaScript Integration

If you want to use JavaScript or TypeScript to provide a rich client-side experience, we recommend checking out the React and Angular templates that are [built into the `dotnet new` command](https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/react).

# Testing

There are many different ways to test your code, and with ASP.NET Core it's simple to write some [unit tests](https://docs.microsoft.com/en-us/dotnet/core/testing/) and/or [integration tests](https://docs.microsoft.com/en-us/aspnet/core/test/integration-tests).  Try writing a few unit tests to cover an important part of your code first and then expand from there once you get the hang of it.  Integration tests are often very useful since they test the way components work together, like to make sure your code won't save an invalid object (ex: a person with no name).

Any of the three officially supported libraries, MSTest, XUnit and NUnit should work just fine for most cases, but **we recommend xUnit** because it's easy to use and well supported.

# Logging

Logging is [built into ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging), but by default you only get logging to the console or EventLog.  This is helpful during debugging but it is still useful (and sometimes required by policy) to log in production.

If you are using [Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview) you can utilize the [Application Insights trace logging](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging#azure-application-insights-trace-logging) for some basic logs.

We recommend using [Serilog](https://github.com/serilog/serilog-aspnetcore) for more structured logging.  It is simple to integrate and can write logs out to [almost any log provider you can think of](https://github.com/serilog/serilog/wiki/Provided-Sinks), from AWS CloudWatch to Azure Analytics to Sentry to Elasticsearch to Stackify and many more.

# Continuous Integration

Using a Continuous Integration (CI) system is a great way to constantly and consistently test and build your code.  Popular CI systems at UC Davis include [Jenkins](https://jenkins.io/) and [Azure Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines/).

We recommend using [Azure Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines/) because it is cloud hosted, can run tons of languages on any platform, and integrates seemlessly with GitHub.  It even has a Continuous Deployment component which can deploy code to AWS, Azure, GCP, or locally.  Azure Pipelines is free for open source projects and is included with Visual Studio Subscriptions (MSDN).