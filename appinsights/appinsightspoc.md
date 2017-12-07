# POC: Application Insights with Contoso Expenses

* [Introduction](#introduction)
* [Learning Objectives](#learning-objectives)
* [Prerequisites](#prerequisites)
* []()

## Abstract
The goal of this POC is to walkthrough the ... TODO

## Learning Objectives
After completing this exercise, you will be able to:
* TODO

## Prerequisites
To complete this POC:
* Application Insights overview (link to content?)
    * Understand the difference between Traditional Monitoring & Continuous Monitoring
    * Understand the differences in monitoring requirements and how Application Insights with Azure Monitoring & Analytics helps address all these visibility concerns
    * Understand the diverse ecosystem around Ingestion, Exploration, Export & Correlation
* Deploy the Contoso Expenses application (ADD link to both options - dpeloy everything from scratch and deploy with arm template)
* A Microsoft Azure subscription (with Contributor access)
* 

## Estimated time to complete this module
Self-guided


## Review Contoso Expenses App


## Create dashboard for App Insights

* Open the Azure portal.
* Click on **+New dashboard**.
* Add name for the dashboard (e.g. App Insights POC).
* Click on **Done customizing**.
* Open the **Resource Group** where the application was deployed and click on the **Pin** icon to pin the Resource Group blade to the dashboard. 


## Monitor Azure web app performance

You can configure monitoring by instrumenting the app in either of two ways:
* **Run-time** - You can select a performance monitoring extension when your web app is already live. It isn't necessary to rebuild or re-install your app. You get a standard set of packages that monitor response times, success rates, exceptions, dependencies, and so on.
* **Build time** - You can install a package in your app in development. This option is more versatile. In addition to the same standard packages, you can write code to customize the telemetry or to send your own telemetry. You can log specific activities or record events according to the semantics of your app domain.

More info at [Monitor Azure web app performance](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-azure-web-apps#run-time-or-build-time)


### (Option 1) Run-time - configure Application Insights for a live Web App

* From the Azure portal **open** the **ContosoExpense Web app** (under App Services or under the Resource Group where the application was deployed).

* Follow steps from [Run time instrumentation with Application Insights](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-azure-web-apps#run-time-instrumentation-with-application-insights)

### (Option 2) Build time 

TODO



## Health Check
## Application Map, Failure Diagnostics & Snapshot Debugging
## Performance Monitoring & Profiling
## Visual Studio Integration
## Analytics with Machine Learning
## Take Actions with Azure Monitor & Alerting
## Customer Insights
## Application Insights REST APIs
