# AWS Observability Workshop

## AWS Observability
AWS provides native monitoring, logging, alarming, and dashboards with Amazon CloudWatch and tracing through AWS X-Ray . When deployed together, they provide the 3 pillars (Metric, Logs & Traces) of an observability solution. The whole AWS Observability ecosystem looks like this.

![image](https://user-images.githubusercontent.com/59352356/211727325-3d42f3fd-3a8d-419d-ada3-3f829f7f6770.png)


## [1. CloudWatch Synthetics Workshop](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/README.md)
CloudWatch Synthetics is an orchestration service, which offers synthetic monitoring to continuously verify application or services performance and availability.

This workshop is designed to provide you with an environment and step by step guide to help you learn on how to use AWS Synthetics service. In this workshop you will learn:
  1.  Create a synthentic heartbeat canary using blueprint
  2.  How to explore canary result and getting comfortable monitoring it
  3.  Set up an alarm when canary doesn't meet the availability requirement


### Getting Started
**IMPORTANT NOTE:** Deploying the heartbeat demo website in your AWS account will create and consume AWS resources, which will cost money. In addition, some features such as SNS notification require users to provide a valid email address to demonstrate working of alarm service. Therefore, to avoid ongoing charges and to clean up all data, be sure to follow all workshop clean up instructions and shutdown/remove all resources once you are finished.

**Workshop [link](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/README.md)**
