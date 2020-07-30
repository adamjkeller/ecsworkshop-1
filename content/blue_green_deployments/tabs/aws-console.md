---
title: "Embedded tab content"
disableToc: true
hidden: true
---

#### Navigate to the LoadBalancer endpoint
You can use the output value of `BlueGreenUsingEcsStack.ecsBlueGreenLBDns`. This is deployed using a demo docker image from docker registry. We will now modify this deployment using the CodePipeline built by the CDK stack in the previous section.

![blue-deployment](/images/blue-deployment.png)

#### Navigate to the AWS console

* When you navigate to the AWS console, you will see a CodePipeline with a failure. I am using `us-east-1 - N. Virginia` region. Choose the region where you had deployed the CDK stack

![aws-console-1](/images/blue-green-aws-console-1.png)

* Click on the pipeline and you can see this is due to missing source code in the CodeCommit repository

![aws-console-2](/images/blue-green-aws-console-2.png)

* We will fix this by cloning a demo application repo and pushing into CodeCommit
* We will change the background of this application to green
* Let's go to next tab - **Update CodeCommit**





