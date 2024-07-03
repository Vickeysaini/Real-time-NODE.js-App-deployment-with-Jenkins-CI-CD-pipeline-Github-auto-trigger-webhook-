# Deployment of end-to-end application in node.js using Jenkins CICD with GitHub Integration

---

| &nbsp; | &nbsp; |
| --- | ----------- |
| **Objective** | - Deploy end-to-end application in node.js using Jenkins CICD with GitHub Integration <br>- Trigger Jenkins pipeline automatically once the code is pushed on GitHub |
| **Approach** | - Using Amazon's Elastic Compute Cloud (EC2) for running application on the Amazon Web Services (AWS) infrastructure <br>- Containerize application by creating Dockerfile<br>- Integrate GitHub with Jenkins using Webhook |
| **Impact** | - Jenkins pipeline triggers automatically once the code is pushed on GitHub</br>- Accomplish faster quality releases by automating CI/CD pipelines |
<br>

**Primary Technology:** Github, Docker, Jenkins, aws EC2 service
<br><br>

![Design Thinking Whiteboard in Yellow Blue Basic Style](https://user-images.githubusercontent.com/102405945/211872655-4ed92a9f-bf03-41bc-ac92-043594863cd8.png)


<br><br>
---

## 1. Creating a Node App
Before we write any CI/CD pipeline we need an application to test and deploy. We are going to build a simple **to-do application** in node.js. Then, create new repository under your GitHub account and name it “node-todo-cicd”.
![1](https://user-images.githubusercontent.com/102405945/211755449-e0c617d8-a9fe-4250-83ad-0ca258a10bbc.png)


## 2. Creating AWS EC2 instance

### 2.1 Creating AWS EC2 instance
After logging into your AWS account, search for EC2
![2](https://user-images.githubusercontent.com/102405945/211756038-f8e88d8f-7e73-4818-974f-e8df7023b5b0.png)

Select **Instances(running)**
![3](https://user-images.githubusercontent.com/102405945/211756073-a00f53a0-d24b-4b9a-a6e7-ba4e4e3d4395.png)

Click **Launch instances**
![4](https://user-images.githubusercontent.com/102405945/211756098-ef0517b6-21f5-4f87-b126-877e4848bf3f.png)

Enter Name and select **Ubuntu**
![5](https://user-images.githubusercontent.com/102405945/211756124-6936130d-84e4-4c9d-8faa-755ff9ddf514.png)

Select **t2.micro** as Instance type and create new key pair to connect to the server
![6](https://user-images.githubusercontent.com/102405945/211756138-1ffe145b-1902-4ab3-99cc-ca2b83688491.png)

Enter **key pair name** and select **RSA** as Key pair type and **.pem** as Private key file format. Then, click **Create key pair**
![7](https://user-images.githubusercontent.com/102405945/211756153-68eb2114-beb3-437c-b7e9-702d32c936fb.png)
R
# Real-time NODE.js App deployment with Jenkins CI CD pipeline|Github auto trigger webhook 





## Step 1: Install NodeJS and NPM using nvm
Install node version manager (nvm) by typing the following at the command line.

```bash
sudo su -
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
Activate nvm by typing the following at the command line.

```bash
. ~/.nvm/nvm.sh
```

Use nvm to install the latest version of Node.js by typing the following at the command line.

```bash
nvm install node
```

Test that node and npm are installed and running correctly by typing the following at the terminal:

```bash
node -v
npm -v
```

## Step 2: Install Git and clone repository from GitHub
To install git, run below commands in the terminal window:

```bash
sudo apt-get update -y
sudo apt-get install git -y
```

Just to verify if system has git installed or not, please run below command in terminal:
```bash
git — version
```

This command will print the git version in the terminal.

Run below command to clone the code repository from Github:

```bash
Git Clone : https://github.com/Aseemakram19/nodejs-on-ec2-youtube.git
Branch Master.
```

Get inside the directory and Install Packages

```bash
cd nodejs-on-ec2
npm install
```

Start the application
To start the application, run the below command in the terminal:

```bash
npm start
```

