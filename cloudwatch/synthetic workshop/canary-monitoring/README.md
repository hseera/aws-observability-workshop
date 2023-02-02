# Monitor Canary

Now that we have created the heartbeat canary, this lab will walk you through all the components of monitoring your canary and explore the results of the heartbeat canary created earlier.

1. On the Canary window, you will see a few details about canaries. In the details about the canaries that you have created:
   -  Status visually shows how many of your canaries have passed their most recent runs.
   -  Groups displays the groups you have created, and displays how many of them have failing or alarming canaries.
   -  Slowest performers displays the group and the Region with the slowest-performing canaries.

   ![image](https://user-images.githubusercontent.com/59352356/213904517-d5e78058-ff82-4afc-a5b8-f6d7ecb8cfa6.png)


2. Select the syntetic canary you have just created.

   ![image](https://user-images.githubusercontent.com/59352356/213904247-fe03baf0-f25c-4f5e-859b-c34805ee5cc1.png)

3. On the Canary page, you will see a few details and multiple tabs.

   ![image](https://user-images.githubusercontent.com/59352356/213904280-2ba99304-b087-480a-b87d-8f34f2fd6f6d.png)

   -  Summary - 
   -  The Availability tab - displays information about the recent runs of this canary.
      -  Under Canary runs - you can choose one of the lines to see details about that run.
      -  The Steps tab - displays a list of the canary's steps, each step's status, failure reason, URL after step execution, screenshots, and duration of step execution. If the canary has active tracing enabled, you can also choose Traces to see tracing information from the canary's runs.
   -  The Monitoring tab - displays graphs of the CloudWatch metrics published by this canary.
   -  The Configuration tab - displays configuration and schedule information about the canary.
   -  The Groups tab - displays the groups that this canary is associated with, if any.
   -  The Tags tab - displays the tags associated with the canary.
 
 ## Availability tab
 ![image](https://user-images.githubusercontent.com/59352356/213904862-4c096480-55a8-4cf9-ac17-98c269a791bd.png)

###   Steps
   ![image](https://user-images.githubusercontent.com/59352356/213904624-5e8d5aa5-cadf-4c89-af0b-349dafdfc492.png)
###   Screenshots
   ![image](https://user-images.githubusercontent.com/59352356/213904643-4b2d8f9e-c2c4-42a4-b8ac-dae0872978a5.png)
###   Logs
   ![image](https://user-images.githubusercontent.com/59352356/213904655-8b0a8cef-f4ba-4757-947e-eb021e462922.png)
###   HAR
   ![image](https://user-images.githubusercontent.com/59352356/213904665-b687aae0-4e13-42ee-8df4-d01ca213fe60.png)


## Monitoring tab
   ![image](https://user-images.githubusercontent.com/59352356/213904688-ee9ba227-d29d-4040-87d9-06aa56de54ed.png)

## Configuration tab
   ![image](https://user-images.githubusercontent.com/59352356/213904735-7dd8081a-4c66-4c7c-a0f2-af87c1b90943.png)

## Groups tab
   ![image](https://user-images.githubusercontent.com/59352356/213904778-fc5e0d02-fddf-46e5-a08f-c4a768dcdc2a.png)
   
## Tag tab
   ![image](https://user-images.githubusercontent.com/59352356/213904805-0f9cf604-ed92-4267-b0f5-ffe7d6427341.png)


In next lab, we are going to setup an [alarm](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-alarms/README.md).

