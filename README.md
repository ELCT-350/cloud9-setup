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

## Step 3. Setup SSH Key on Cloud9

- In the Cloud9 IDE, open a terminal window by going to menu item Window > New Terminal
- Make a new ssh key by entering the following command into the terminal:
```ssh-keygen -t rsa```
- When prompted, name the key "cloud9key" and enter a passphrase of your choosing. Remember the passphrase. It cannot be recovered.
- Open the newly created cloud9key.pub in the file explorer on the left by double clicking it. Keep Cloud9 open. You will need the contents of this file in the next step.

## Step 4. Add SSH Key to your GitHub account

- Back in Cloud9, copy the contents of the cloud9key.pub to the clipboard. It should start with "ssh-rsa ..."
- Log into your GitHub account, go to settings, and go to SSH and GPG Keys on the left panel
- Add a new key. The name of the key should be "cloud9key". Paste the contents of the cloud9key.pub file into the box.

## Step 5. Clone this Repo to Cloud9

## Step 6. Install CMake to Cloud9

## Step 7. Build and Run the Test Program


