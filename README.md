### How to attach an Instance which is created already in AWS to an ASG

1. Create an AMI of the desired Instance.
2. Create Launch Configuration. 

Please note : Choose the newly created AMI.

Here I'm taking an AMI of the already created instance named webserver. 

![image](https://github.com/jijinmichael/ASG-Instance-Management/assets/134680540/14df8059-b587-4246-b3cb-6ab90d4f4835)

3. Create an Auto Scaling Group with the above LC.

Please note : The Group size must be 

Desired capacity = 0 

Minimum capacity = 0

Maximum capacity = 1

In the context of auto scaling, the desired minimum and maximum values for the group size refer to the range of instances that an auto scaling group can scale between based on the workload demands.

The desired minimum value represents the lower limit or the minimum number of instances that the auto scaling group should maintain, even during periods of low demand. This ensures that there are always a certain number of instances available to handle incoming requests.

The desired maximum value represents the upper limit or the maximum number of instances that the auto scaling group can scale up to when there is high demand. This allows the group to dynamically increase its capacity to handle increased traffic or workload.

By specifying these desired minimum and maximum values, you provide guidelines to the auto scaling system on how many instances it should maintain within the group at any given time. The actual number of instances will be automatically adjusted based on the scaling policies and conditions defined, such as CPU utilization, network traffic, or other metrics that you configure.

![image](https://github.com/jijinmichael/ASG-Instance-Management/assets/134680540/6775bc69-717b-4245-93e4-241e9debbfd0)

4. Then go to the instance >> instance settings >> Attach to Auto Scaling Group.

![image](https://github.com/jijinmichael/ASG-Instance-Management/assets/134680540/62ac273f-9031-4ac7-bff5-d952cf9c62e5)

Then attach the instance to ASG.

![image](https://github.com/jijinmichael/ASG-Instance-Management/assets/134680540/5d39c546-bade-4f95-bc9e-ed8e95b81c91)

Then you will get an activity history like below.

![WhatsApp Image 2023-05-24 at 18 02 04 (1)](https://github.com/jijinmichael/ASG-Instance-Management/assets/134680540/66645e3e-7b91-47cc-b2c5-036b777d505c)
