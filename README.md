<header>



# Activity: AWS Elastic Beanstalk

<!-- Note to translators: This activity is unique to the CUR-TF-100-ACCLFO-2 course. -->

## Overview

This activity provides you with an Amazon Web Services (AWS) account where an AWS Elastic Beanstalk environment has been pre-created for you. You will deploy code to it and observe the AWS resources that make up the Elastic Beanstalk environment.

## Duration

This activity takes approximately **30 minutes** to complete.

------------


## Accessing the AWS Management Console

Access your AWS Management Console using a root account or IAM admin user. 

## Task 1: Access the Elastic Beanstalk environment
##### Open the Elastic Beanstalk console using this link: [Elastic Beanstalk console](https://console.aws.amazon.com/elasticbeanstalk/home#/gettingStarted?applicationName=getting-started-app "Elastic Beanstalk console")


   A page titled **Getting started** should open, and it should show **Create a web app** page.  
[![Web APP](https://elasticbeanstalkworkshop.s3.amazonaws.com/page1.png "Web APP")](https://elasticbeanstalkworkshop.s3.amazonaws.com/page1.png "Web APP")
## Task 2: Deploy a Sample Application. 
 
###  To create an example application

1. Open the Elastic Beanstalk console using this link: https://console.aws.amazon.com/elasticbeanstalk/home#/gettingStarted?applicationName=getting-started-app
2. Optionally add application tags.

5. For Platform, choose  **Docker** as a platform.
6. Select upload application code, then select local file for the *source code origin*.
Choose **Choose File**, then navigate to and open the **docker.zip** file that you just downloaded.
> You could also use the S3 url of docker.zip (https://elasticbeanstalkworkshop.s3.amazonaws.com/docker.zip), which will upload the source code from the s3 bucket into the Elastic Beanstalk console. 
7. Finally, click on create application button. 
 ![deployment](https://elasticbeanstalkworkshop.s3.amazonaws.com/page2.png "deployment")
- This will deploy the sample application code. 
- During the environment creation process, the console tracks progress and displays events.
- When all of the resources are launched and the EC2 instances running the application pass health checks, the environment's health changes to Ok. 
- You can now use your web application's website.

After the deployment is complete, choose the URL value near the top of the screen.
![url](https://elasticbeanstalkworkshop.s3.amazonaws.com/page3.png "url")

### The web application that you deployed displays.

![Final Result](https://elasticbeanstalkworkshop.s3.amazonaws.com/page4.png "Final Result")

Congratulations, you have successfully deployed an application on Elastic Beanstalk!

## Task 3: Explore your environment.



14. Back in the Elastic Beanstalk console, choose **Configuration** in the left pane.

    Notice the details here.

    For example, in the **Instances** row, it indicates the Monitoring interval, EC2 Security groups, and Root volume type details of the Amazon Elastic Compute Cloud (Amazon EC2) instances that are hosting your web application.

15. Scroll to the bottom of the page to the **Database** row.

    The **Database** row does not have any details, because the environment does not include a database.
15. In the **Database** row, choose **Edit**.

    Note that you could easily add a database to this environment if you wanted to: you only need to set a few basic configurations and choose **Apply**. (However, for the purposes of this activity, you do not need to add a database.)
17. In the left panel, choose **Monitoring**.

    Browse through the charts to see the kinds of information that are available to you.

&nbsp;
&nbsp;
## Task 4: Explore the AWS resources that support your application

18. From the **Services** menu, choose **EC2**

    

19. Choose **Instances**.

    Note that two instances that support your web application are running (they both contain *samp* in their names). 

    

20. If you want to continue exploring the Amazon EC2 service resources that were created by Elastic Beanstalk, feel free to explore them. You will find:

    - A *security group* with port 80 open
    - A *load balancer* that both instances belong to
    - An *Auto Scaling group* that runs from two to six instances, depending on the network load

     Though Elastic Beanstalk created these resources for you, you still have access to them.

## Activity complete

<i class="icon-flag-checkered"></i> Congratulations! You have completed the activity.

## Task 5: Clean up

1. Delete all application versions.
 1. Open the Elastic Beanstalk console, and in the Regions list, select your AWS Region.
 2. In the navigation pane, choose **Applications**, and then choose ** getting-started-app**.
 3. In the navigation pane, find your application's name and choose Application versions.
 4. On the Application versions page, select all application versions that you want to delete.
 5. Choose Actions, and then choose Delete.
 6. Choose Delete, and then choose Done.
2. Terminate the environment.
  1. In the navigation pane, choose getting-started-app, and then choose GettingStartedApp-env in the environment list.
 2. Choose Environment actions, and then choose Terminate Environment.
 3. Confirm that you want to terminate GettingStartedApp-env by typing the environment name, and then choose Terminate.
 4. Delete the getting-started-app application.
3. In the navigation pane, choose the getting-started-app.
 1. Choose Actions, and then choose Delete application.
 2. Confirm that you want to delete getting-started-app by typing the application name, and then choose Delete.
