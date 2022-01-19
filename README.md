# Cloud9 Setup
Setup instructions and scripts for using AWS Cloud 9 for C++ Development

## Introduction

This method for C++ development can be used when all else fails. It is not simple, and there are several steps involved, but it will work on anything with a browser. It uses a free AWS (Amazon Web Services) account along with a cloud-based development environment called Cloud9 to build complex C++ applications on an AWS server using a browser-based IDE. You will also have to install CMake in your cloud enviroment, and setup SSH authentication for using GitHub.

## Step 1. Make an AWS Account

- Go to the following address and sign up for an AWS account:
https://portal.aws.amazon.com/billing/signup#/start
- You will have to enter a payment method, but AWS will not charge you anything unless you upgrade your account in the future. 
- Select the “Basic Support – Free” plan.

## Step 2. Setup Cloud9 on your AWS Account

- Go to your AWS console here:
https://console.aws.amazon.com/console/home?region=us-east-1
- Click the “Services” menu at the top left, then click “Developer Tools”, and then “Cloud9”
- Click the “Create Environment” button
- Name the environment elct350, and add ELCT 350 for the description. (Ignore the “AWS Root Login Detected” warning).
- Click “Next Step”
- On the Configure Settings Page, don't change the default settings, click “Next Step”
- Review and commit your options on the next page.
- Cloud 9 will take some time to initialize. When it’s done, bookmark the page. The URL will look like:
https://console.aws.amazon.com/cloud9/ide/...

## Step 3. Install Cmake to Cloud9

- Find your bash terminal the Cloud IDE (should be at the bottom, and is a window in a tab that starts with "bash ~ ip-..."). If you don't see it, go to Window > New Terminal and open open.
- Run the following command in the terminal:
```sudo yum install cmake3```
- When asked to confirm the downland, reply with "y"
- It is complete when you see "Complete!" in the terminal

## Step 3. Create SSH Key on Cloud9

- In the Cloud9 IDE, open a terminal window by going to menu item Window > New Terminal
- Make a new ssh key by entering the following command into the terminal:
```ssh-keygen -t rsa```
- DO NOT ADD A FILENAME OR A PASSWORD. Simply press Enter at the prompts.
- Get the contents of the public key file with the terminal command:
```cat /home/ec2-user/.ssh/id_rsa.pub```
- Copy the contents of the file from the terminal to yout clipboard of a text file. The key starts with "ssh-rsa ...".

## Step 4. Add SSH Key to GitHub

- Log into your GitHub account, go to Settings, and go to "SSH and GPG Keys" on the left panel
- Click the green "New SSH Key" to add a new key. Put "aws" as the title, and paste the contents of the id_rsa.pub file into the box you got from step 3 above.

## Step 5. Clone this Repo to Cloud9

- Add your username to git by running the command in terminal with your GitHub username:
````git config --global user.name YOUR_USER_NAME_HERE```
- Clone this repository by running the command in terminal:
```git clone git@github.com:ELCT-350/cloud9-setup.git```

## Step 7. Build and Run the HelloCloud9 Program

- Navigate to the repository in the file explorer on the left and open the file "hello.cpp" by double clicking
- 



