# jenkins-aws-demo
- First, create two EC2 instances using the Terraform AWS provider and name them (jenkins-master) and (jenkins-agent-1). 
- For the master EC2 instance (jenkins-master), configure inbound rules to allow SSH, HTTP, HTTPS, and a custom TCP port 8080 for Jenkins access.
-  For the agent EC2 instance (jenkins-agent-1), only enable SSH access.
-  After that, SSH into both the master (jenkins-master) and the agent (jenkins-agent-1) using their public IP addresses in two separate terminal windows.
-   Use Ubuntu as the OS for both instances because it's easier to set up for this project.
-  Once logged into the instances, install Jenkins on the master so you can access the Jenkins UI. Also install Node.js, since the application is a Node.js app. Additionally, install Docker, which is helpful for container-based builds and deployments.
-  Next, on the agent machine, generate an SSH key pair (public and private).
-  Copy the public key from the agent to the master, allowing the master to connect to the agent via SSH.
-   After setting up the key-based connection, access the Jenkins dashboard by opening the master’s public IP followed by port 8080 in a browser. ----> Once Jenkins is ready, create a new credential in Jenkins for GitHub access or SSH authentication.
-    Then, in Jenkins, add a new node with a label like ubuntu—this will act as the agent node that Jenkins uses to run jobs.
-  Open GitHub and create a new repository. Push the Node.js app files (like app.js, package.json, and Jenkinsfile) into the repo. The Jenkinsfile should define the pipeline steps.
- After all files are pushed to GitHub, go back to Jenkins and create a new pipeline job.
-  Link this job to your GitHub repository and trigger a build
![Screenshot (43)](https://github.com/user-attachments/assets/1fb312e9-3565-44fd-a17b-7fbf1ecdc436)
![Screenshot (48)](https://github.com/user-attachments/assets/49b99853-27b1-4a02-b2ab-8112590b7c9f)
![Screenshot (49)](https://github.com/user-attachments/assets/ec999c89-1b13-446a-a1e3-359c7cbff3ba)
![Screenshot (50)](https://github.com/user-attachments/assets/7d622e5b-88ec-4c53-bb64-04b3bff8e955)
