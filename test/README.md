# Cloudwatch Synthetics Workshop

## Introduction

AWS. When deployed together, they provide the 3 pillars (Metric, Logs & Traces) of an observability solution. The whole AWS Observability ecosystem looks like this.

![image](https://user-images.githubusercontent.com/59352356/211727325-3d42f3fd-3a8d-419d-ada3-3f829f7f6770.png)

For our workshop, we are going to focus on Cloudwatch Synthetics services. 

You can use Amazon CloudWatch Synthetics to create canaries - configurable scripts that run on a schedule - to monitor your endpoints and APIs. Canaries check the availability and latency of your endpoints and can store load time data and screenshots of the UI as rendered by a headless Chromium browser. They monitor your REST APIs, URLs, and website content, and they can check for unauthorized changes from phishing, code injection and cross-site scripting. They can even check to see if a percentage of a web page has changed from a baseline that you establish.

## Setup

Before we start with the lab, we need to setup few things. 
1. First we are going to setup a static website using S3.
   - Download the static webpage from here    
2. Log into your AWS Account and Create an S3 bucket
3. Upload the static webpage to the S3 bucket
   - Make sure the webpage is publically accessable. We are going to be hitting the webpage endpoint as part of our workshop.
   - Copy the S3 public endpoint URL
4. Paste the end point URL in your browser. If you have setup everything correctly, you should see the following message in the browser.

## Lab1: Heartbeat Canary

## Lab2: Exploring Results

## Lab3: Canary Alarms

## Lab4: API Canary

## Lab5: Cleaning Up
