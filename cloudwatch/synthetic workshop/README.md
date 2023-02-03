# Cloudwatch Synthetics - Heartbeat Canary Workshop

## Introduction

Synthetic tests are important for applications because they allow developers to test the behavior of their software in a controlled environment. Synthetic tests can be used to simulate various scenarios and conditions that may be difficult or impossible to replicate in real-world testing. This can help to identify and fix bugs and other issues before the software is released to users. Additionally, synthetic tests can be used to measure the performance and scalability of an application, allowing developers to optimize and improve its performance. Overall, synthetic testing is a powerful tool for ensuring the quality and reliability of an application.

You can use Amazon CloudWatch Synthetics to create canaries - configurable scripts that run on a schedule - to monitor your endpoints and APIs. Canaries check the availability and latency of your endpoints and can store load time data and screenshots of the UI as rendered by a headless Chromium browser. They monitor your REST APIs, URLs, and website content, and they can check for unauthorized changes from phishing, code injection and cross-site scripting. They can even check to see if a percentage of a web page has changed from a baseline that you establish.


## [Prerequisite](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/setup/README.md)
Prerequisite for learning the heartbeat canary. AWS S3 service will be used to host a static website that will be used in the labs for learning the AWS Sythnetics service.
## [Lab1: Heartbeat Canary](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-heartbeat/README.md)
In this lab, we will learn to create a heartbeat canary that will check the availability of our static website.

## [Lab2: Exploring Results](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-monitoring/README.md)
In this lab, we will explore the monitoring option that comes with the Synthetics.

## [Lab3: Canary Alarms](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-alarms/README.md)
In this lab, we create and alarm and trigger it when availability threshold is breached.

## [Cleaning Up](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-cleanup/README.md)
Finally, clean up all the resource that were created as part of the workshop.
