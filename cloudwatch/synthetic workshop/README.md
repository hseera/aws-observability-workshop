# Cloudwatch Synthetics - Heartbeat Canary Workshop

## Introduction

Synthetic tests are important for applications because they allow developers to test the behavior of their software in a controlled environment. Synthetic tests can be used to simulate various scenarios and conditions that may be difficult or impossible to replicate in real-world testing. This can help to identify and fix bugs and other issues before the software is released to users. Additionally, synthetic tests can be used to measure the performance and scalability of an application, allowing developers to optimize and improve its performance. Overall, synthetic testing is a powerful tool for ensuring the quality and reliability of an application.

You can use Amazon CloudWatch Synthetics to create canaries - configurable scripts that run on a schedule - to monitor your endpoints and APIs. Canaries check the availability and latency of your endpoints and can store load time data and screenshots of the UI as rendered by a headless Chromium browser. They monitor your REST APIs, URLs, and website content, and they can check for unauthorized changes from phishing, code injection and cross-site scripting. They can even check to see if a percentage of a web page has changed from a baseline that you establish.


## [Setup](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/setup/README.md)

## [Lab1: Heartbeat Canary](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-heartbeat/README.md)

## [Lab2: Exploring Results](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-monitoring/README.md)

## [Lab3: Canary Alarms](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-alarms/README.md)

## [Cleaning Up](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-cleanup/README.md)
