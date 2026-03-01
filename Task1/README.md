# Task 1: Static Web Hosting in EC2 (Ubuntu + Nginx)

## Objective
To deploy a custom static website (HTML/CSS/JS) on an AWS EC2 Ubuntu instance using the Nginx web server.

## Implementation Steps
1. Repository Setup: Organized local project files (HTML, CSS, JS) into the `Task1_Static_Web_Hosting_EC2` folder and pushed to GitHub.
2. Instance Launch: Launched an Ubuntu EC2 instance (`t2.micro`) with HTTP (Port 80) and SSH (Port 22) enabled in the Security Group.
3. Server Configuration:
   - Connected via SSH.
   - Installed Nginx using `sudo apt install nginx`
   - Started and enabled the Nginx service.
4. Deployment:
   - Cloned the GitHub repository to the server.
   - Moved the web files to the Nginx root directory: `/var/www/html/`
5. Verification: Accessed the website via the EC2 Public IP to confirm the custom page is live.

## Proofs
- EC2.png: AWS EC2 Console showing the instance in 'Running' state.
- website.png: Browser output showing the deployed custom website.
- command.txt: All the command i run in terminal
- cmd.png: terminal screenshot