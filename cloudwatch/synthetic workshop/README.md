# Cloudwatch Synthetics Workshop

## Introduction

You can use Amazon CloudWatch Synthetics to create canaries - configurable scripts that run on a schedule - to monitor your endpoints and APIs. Canaries check the availability and latency of your endpoints and can store load time data and screenshots of the UI as rendered by a headless Chromium browser. They monitor your REST APIs, URLs, and website content, and they can check for unauthorized changes from phishing, code injection and cross-site scripting. They can even check to see if a percentage of a web page has changed from a baseline that you establish.

## Setup

Before we start with the lab, we need to setup few things. 
1. First we are going to setup a static website using S3.
   - Download the static webpage from here    
2. Log into your AWS Account and Create an S3 bucket. 
   - Let call the S3 bucket "observability-workshop-{yourname}"
   - Select your residence region (i.e. ap-southeast-2)
   - Untick "Block all public access". For workshop purpose we want to access the webpage. Also make sure to tick the acknolwedge option for making S3 access public.  Note after the workshop we will disable this option and delete the bucket.  
   ![image](https://user-images.githubusercontent.com/59352356/211769377-bb725844-487b-4f7d-84ba-7ea660425822.png)
![image](https://user-images.githubusercontent.com/59352356/211769499-b78b80fa-dbd8-4e33-bbba-7dbe1745c20c.png)
![image](https://user-images.githubusercontent.com/59352356/211769811-01e15772-d27e-4984-a321-77b70d386fe5.png)
   - Once bucket is created, go to bucket property and enable the "Static website hosting" property. By defalut it is disabled. Also select "Host a static website" and give your home page a name. In this case we will name it "index.html"
   ![image](https://user-images.githubusercontent.com/59352356/211771765-24f9dabb-d0ca-492a-bc08-44ae823039fd.png)
![image](https://user-images.githubusercontent.com/59352356/211771960-5ecf352b-6143-49c7-b48a-40718d1b35ff.png)
   - Next step is to add "Bucket policy" to enable the index.html to be accessable. In the "Bucket Policy Editor" we add the following code. Replace * in the the code with your bucket resource name.
   ```
   {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::Bucket-Name/*"
            ]
        }
    ]
}
   ```
   ![image](https://user-images.githubusercontent.com/59352356/211775465-b72dc80d-0093-4c28-ac18-c4dfc32e30cc.png)


3. Upload the static webpage to the S3 bucket
   - Copy the S3 public endpoint URL for index.html page under the "Bucket website endpoint"   
   ![image](https://user-images.githubusercontent.com/59352356/211775819-402f5873-3d7b-4ee5-8de9-14568cd9ae28.png)

4. Paste the end point URL in your browser. If you have setup everything correctly, you should see webpage render in the browser.

## Lab1: Heartbeat Canary

## Lab2: Exploring Results

## Lab3: Canary Alarms

## Lab4: API Canary

## Lab5: Cleaning Up
