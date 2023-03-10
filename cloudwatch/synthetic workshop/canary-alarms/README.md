# Create Canary Alarm

Now that we are able to monitor the canary, let's set up an alarm to alert us when there is a failure. We are going to setup an alarm that will send an email when there is a failure. You can also add hooks to send the message to other communication channels such as Slack.

There are three ways, to setup an alarm:
1. When you are creating the canary during the initial creation of the canary,
2. Editing an existing canary
3. Or through the CloudWatch alarm console. We are going to cover the second method. Updating an existing canary with an alarm.

In this lab:
  - We will alarm based off the SuccessPercent metric, so that when it drops below 90% within a specific period, we will get an email notification through an SNS topic.
  - We will also create an SNS topic as part of the alarm creation, but you can also use an existing SNS topic.
  - Finally we will create a situation that will trigger the alarm.

1. From the the AWS CloudWatch console, select Synthetics Canaries, and choose the canary you created in the first lab. Click on the Actions->Edit option.

  ![image](https://user-images.githubusercontent.com/59352356/216474997-982c051d-60d1-432d-8829-c8454a27d067.png)

2. Scroll to the CloudWatch Alarms section and expand it.

  ![image](https://user-images.githubusercontent.com/59352356/214961960-2c5862cf-d5a2-444a-b4eb-32502a6f255c.png)

3. Choose to Add new alarm.
4. Select the following condition for the alarm:
    - Metric name: SuccessPercent
    - Alarm Condition: Lower
    - Threshold: 90%
    - Period: 5 minutes
  
  ![image](https://user-images.githubusercontent.com/59352356/214962240-0f3c6aa8-83fb-4d31-959f-f43818617b99.png)

5. Next you need to define the notification channel for the alarm. In this example we will create a new SNS topic.
6. Click save to save the canary.
7. From the the AWS CloudWatch console, select Alarms and choose **"All alarms"** option. This will show all existing alarms.
  
  ![image](https://user-images.githubusercontent.com/59352356/216475236-333cd6f0-ab13-4598-95fa-7340eb30ff50.png)

8. Select the alarm you just created, and click on Actions -> Edit
  
  ![image](https://user-images.githubusercontent.com/59352356/216475335-5252a837-0344-43b4-bacf-c4567f18f7d1.png)

9. Leave the first page as is and click on Next button
  
  ![image](https://user-images.githubusercontent.com/59352356/214963723-0f177151-4e3b-4114-a3a2-7a40caae1d3e.png)
  
10. Click on "Add Notification" button to expand it. Set the following:
  - Choose to Create new topic.
  - Give the topic a name: I will call my topic "Synthetics-AWSWorkshop".
  - Enter your own email address to receive the alarm. I have set my gmail account to receive an alarm
  
  ![image](https://user-images.githubusercontent.com/59352356/214964555-3bde4d4c-5251-49dd-9075-413641f9f93d.png)
  
11. Click on **"Create topic"** to create an sns notification.
  
  ![image](https://user-images.githubusercontent.com/59352356/214965094-856cfb93-4b08-4864-b67a-e8ce133ae57e.png)
  
12. Click on "Update Alarm" button
  
  ![image](https://user-images.githubusercontent.com/59352356/214964701-552da4a2-5b2a-4eed-8fcc-bb0c696d0a5a.png)
  
13. You may see the following message on the alarm page.
  
  ![image](https://user-images.githubusercontent.com/59352356/214965344-0b99c25b-d520-4406-84f5-1c65b2cacb95.png)
  
14. Check your email to confirm the subscription. Once confirmed you will see the following message.
  - **Check your spam folder for the email if you do not see in the inbox.**

15. You will receive an email the next time the alarm is triggered. 
  - To test it, let's disable access to the S3 bucket so we can't access the website, or you can update the script's end point to point to an invalid address. Let us now keep an eye on our canary.

   ![image](https://user-images.githubusercontent.com/59352356/213904946-6b86f67b-c7b0-4a0d-9faa-2970bdc6e7e6.png)
   
   ![image](https://user-images.githubusercontent.com/59352356/213904966-49a7177c-9d7f-469e-9d98-d4e8ac1b24b4.png)
 - Here is an sample example of an email received when alarm is triggered.
   
   ![image](https://user-images.githubusercontent.com/59352356/216478075-54d8b8f6-cefa-471d-a135-03d3ebdfea48.png)


  




