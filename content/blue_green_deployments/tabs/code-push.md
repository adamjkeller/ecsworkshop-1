---
title: "Embedded tab content"
disableToc: true
hidden: true
---

#### Push the source code to the CodeCommit repository
The stack created an empty CodeCommit repository - `demo-app`. Now we will populate it with a sample demo application.

#### Clone the demo application
```bash
cd ~/environment
git clone https://github.com/smuralee/nginx-example.git
```

#### Update the remote origin URL
Change the remote origin to the CodeCommit repository. You can get the repository URL from the output value of `BlueGreenUsingEcsStack.ecsBlueGreenCodeRepo` in the stack output. Here I am assuming the region is `us-east-1`

```bash
cd ~/environment/nginx-example
git remote set-url origin https://git-codecommit.us-east-1.amazonaws.com/v1/repos/demo-app
```

#### Verify the remote origin url is pointing to the CodeCommit repository
```bash
git remote -v
```

#### Edit the `index.html`. We change the `background-color` to `green`
```html
<head>
  <title>Demo Application</title>
</head>
<body style="background-color: green;">
  <h1 style="color: white; text-align: center;">
    Demo application - hosted with ECS
  </h1>
</body>
```


#### Push the code to the CodeCommit repository
```bash
git add .
git commit -m "Changed background to green"
git push
``` 

#### This will trigger the deployment pipeline

![blue-green-aws-console-3](/images/blue-green-aws-console-3.png)

#### Click on the `Amazon ECS (Blue/Green)` and we will see the ongoing task replacement

![blue-green-aws-console-4](/images/blue-green-aws-console-4.png)

Let's go to next tab - **Deployment & Testing**

