# Create Heartbeat Canary

Now that we have done the setup, this lab will walk you through on how to setup a heartbeat canary. In this lab we will create a heartbeat canary from the blueprint.
A heartbeat canary checks a webpage/URL and will consider the check successful if a URL returns an http status code of 2xx.

1. Navigate to CloudWatch and select **"Synthetics Canaries"** option
   
   ![image](https://user-images.githubusercontent.com/59352356/213642385-b2f280b0-84e8-48f0-9b07-522965f0e392.png)

2. Click on the "Create Canary" button
   ![image](https://user-images.githubusercontent.com/59352356/213642849-b871568d-265b-4c7d-872b-d0be31162c8e.png)

3. Select "Use a blueprint" option and Blueprint type as **"Heartbeat monitoring"**  
   ![image](https://user-images.githubusercontent.com/59352356/213643751-83b04890-3a2c-4a25-b83d-e728b63fc31b.png)

4. Under Canary option, give a name to your hearbeat canary test. Let's call it "{firstname}-canary". And add the end point to the static website we created in the setup lab.
   
   ![image](https://user-images.githubusercontent.com/59352356/213858891-159a440b-e43b-46b4-8899-36920104779a.png)

5. Leave the Script editor option as it is.
6. In the Schedule section let's change the run frequency of the canary to be 1min. This is will give enough data points to visualize the result 

   ![image](https://user-images.githubusercontent.com/59352356/213644509-496c2218-7117-4ccd-8891-86005fe7931a.png)

7. Leave data retention to default value.

   ![image](https://user-images.githubusercontent.com/59352356/213644690-a58e64df-db30-416b-8f22-29d3b1b31b26.png)

8. Leave data storage option empty and select **"Create a new role"** under access permissions.

   ![image](https://user-images.githubusercontent.com/59352356/213858960-e4fa4879-5514-4645-9801-035f5a01f6fb.png)

9. Leave all other options as is and click **"Create canary"**. If successful, you will see **"Canaries"** page with your canary listed in the list.

   ![image](https://user-images.githubusercontent.com/59352356/213859049-cc0b87c8-25b6-4fbf-b72e-0e8f85e1e4bc.png)

Congrats, you have successfully created your first heartbeart canary in AWS. In next lab, we will look at the [monitoring](https://github.com/hseera/aws-observability-workshop/blob/main/cloudwatch/synthetic%20workshop/canary-monitoring/README.md).
