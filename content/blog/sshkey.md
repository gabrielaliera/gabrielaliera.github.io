---
title: "Troubleshooting SSH Key Issues with My Digital Ocean Droplet"
description: ""
dateString: "August 12, 2023 - "
ShowWordCount: true
ShowReadingTime: true
draft: false
tags: ["Major League Hacking", "Docker", "Bash", "Digital Ocean", "Git","Linux","Docker Compose","YAML"]
weight: 101
cover:
    #image: "/blog/mlh-week1-6/cover.png"
---

In this week's learning journey as a **Production Engineer Intern** at **Major League Hacking**, I delved into the realm of **continuous integration and deployment**. In the preceding weeks, our deployment process involved manual steps of SSHing into our virtual private server (VPS) hosted on Digital Ocean and executing a script. This script was responsible for fetching the latest commits from our repository's main branch, updating our virtual private server, orchestrating Docker container shutdown and restart, and ultimately refreshing our application using Docker Compose.

To streamline and automate this process, I embarked on creating a robust deployment workflow through GitHub Actions. However, deploying via GitHub Actions necessitates configuring SSH environments to establish a connection with my VPS. This configuration involves handling sensitive information, such as IP addresses, usernames, passwords, and particularly, my SSH private key, which was vital for secure authentication.

Yet, a hiccup emerged in the form of an accidental overwrite of my local SSH public and private keys so I couldn't upload my private key to Github🙈😅. Consequently, I had to rectify this situation by uploading the new SSH public key to my existing Droplet on Digital Ocean.

Here's a step-by-step account of how I resolved this issue:

1. **Generate a New SSH Key**:<br>To begin the process, I generated a fresh SSH key by executing the command:

```ssh-keygen -t rsa -C "A comment to help remember this key in the future"```

2. **Locate and Save the Keys**:<br>I navigated to the ```.ssh``` directory on my local machine and securely saved the newly generated keys. For this, I found using Visual Studio Code as an effective tool for viewing the files.

3. **Access Droplet Through Digital Ocean Dashboard**:<br>By utilizing Digital Ocean's manual access feature on the droplet dashboard, I logged into my Droplet.

4. **Navigate to SSH Directory**:<br>Inside the Droplet's system, I navigated to the ```~/.ssh``` directory.

5. **Update Authorized Keys**:<br>The next step was to add my SSH public key to the ```authorized_keys``` file in the directory using the vim text editor. This file contains the list of public keys that allow user access to the server.

6. **Secure GitHub Secrets**:<br>Back on GitHub, I moved on to my repository's settings and accessed GitHub secrets. Here, I securely added the SSH private key to further enable secure communication between my deployment workflow and my VPS.

With these adjustments completed, my deployment workflow was successfully reconfigured, ensuring seamless access to my VPS and smooth deployment of updates. This experience underscored the importance of managing and safeguarding SSH keys to ensure the integrity and security of our deployment processes. 

Even better, following my grasp of incorporating SSH public keys into my VPS, I took it a step further by generating an entirely new set of SSH keys dedicated to deployment purposes. This clear demarcation allowed me to maintain a clear distinction between my personal SSH access and the keys used specifically for deployment.