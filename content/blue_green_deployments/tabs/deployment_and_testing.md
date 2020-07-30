---
title: "Embedded tab content"
disableToc: true
hidden: true
---
#### You will see blue deployment on port `80`

![blue-deployment](/images/blue-deployment.png)

#### Here is task replacement by CodeDeploy

![blue-green-task-replacement](/images/blue-green-task-replacement.png)

Once **Step 2:** is completed, you can test the application on the test port `8080`

#### You will see green deployment on the test port `8080`

![green-deployment](/images/green-deployment.png)

#### After Step 3, production port `80` will show green deployment

* We had a seamless traffic shifting from blue to green using `CodeDeployDefault.ECSLinear10PercentEvery1Minutes`
* This shifts 10 percent of traffic every minute until all traffic is shifted
* We have completed a successful Blue/Green deployment
* Let's go to next tab - **Config Files** to understand the configurations



