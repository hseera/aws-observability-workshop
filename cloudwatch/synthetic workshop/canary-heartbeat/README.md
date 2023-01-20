# Setup

Now that we have done the setup, this lab will walk you through on how to setup a heartbeat canary.

1. Navigate to CloudWatch and select "Synthetics Canaries" option
   
   ![image](https://user-images.githubusercontent.com/59352356/213642385-b2f280b0-84e8-48f0-9b07-522965f0e392.png)

2. Click on the "Create Canary" button![image](https://user-images.githubusercontent.com/59352356/213642849-b871568d-265b-4c7d-872b-d0be31162c8e.png)

3. Select "Use a blueprint" option and Blueprint type as "Heartbeat monitoring"  ![image](https://user-images.githubusercontent.com/59352356/213643751-83b04890-3a2c-4a25-b83d-e728b63fc31b.png)

4. Under Canary option, give a name to your hearbeat canary test. Let's call it "{firstname}-canary". And add the end point to the static website we created in the setup lab.
   
   ![image](https://user-images.githubusercontent.com/59352356/213644225-89e0bce0-eb2f-486b-b3a4-d5c3b31fb1da.png)

5. Leave the Script editor option as it is.
6. In the Schedule section let's change the run frequency of the canary to be 1min. This is will give enough data points to visualize the result 

   ![image](https://user-images.githubusercontent.com/59352356/213644509-496c2218-7117-4ccd-8891-86005fe7931a.png)

7. Leave data retention to default value.

   ![image](https://user-images.githubusercontent.com/59352356/213644690-a58e64df-db30-416b-8f22-29d3b1b31b26.png)

8. Leave data storage option empty and select "Create a new role" under access permissions.

   ![image](https://user-images.githubusercontent.com/59352356/213648086-88c30a32-b28d-4159-8855-61f0c68276e4.png)

9. Leave all other options as it is and click "Create canary".

   ![image](https://user-images.githubusercontent.com/59352356/213648225-110573a8-ef36-49f4-9120-2e10b587b890.png)

