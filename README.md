# RDS with EC2 Connection™ – Build Your Own Cloud Database Architecture

An interactive, beginner-friendly lab that teaches how to connect an **Amazon Linux 2023 EC2** instance to an **Amazon RDS MySQL** database over a private VPC connection (TCP 3306).

Built by **Cloud Messenger™** · Learn • Build • Visualize • Troubleshoot • Grow ☁️

## Features
- Nine clickable learning stages with autoplay (5 s), Pause/Resume, Previous/Next, Reset and a progress bar
- Animated architecture: Windows PC → SSH 22 → EC2 → TCP 3306 → RDS, with glowing SQL packets
- Terminal simulator (Git Bash/SSH, dnf install, `mysql -h … -P 3306 -u admin -p`)
- SQL simulator (`SHOW DATABASES`, `CREATE DATABASE`, `USE`, `CREATE TABLE`, `INSERT`, `SELECT`)
- Copy-command buttons and AWS terminology tooltips
- Troubleshooting lab (8 scenarios) with cleanup checklist
- Knowledge-check quiz with explanations and a celebration animation

## Run locally
No build step or dependencies. Open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on GitHub Pages
1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**, choose the `main` branch and `/ (root)`.
3. Your lab will be live at `https://<your-user>.github.io/<repo>/`.

## The key command
```bash
mysql -h <RDS-ENDPOINT> -P 3306 -u admin -p
```
The RDS security group must allow inbound TCP 3306 **from the EC2 security group** – never from `0.0.0.0/0`.

## Best practices covered
- Restrict SSH (22) to your IP; keep RDS private
- Use strong, unique credentials; never commit passwords to GitHub
- Same Region/VPC for EC2 and RDS
- Delete the RDS instance and terminate EC2 when finished to avoid charges

## Roadmap
- Animated AWS Console walkthroughs for Steps 1–3
- Secrets Manager, IAM roles and cross-AZ transfer cost modules

## Links
- GitHub: https://github.com/Cloud-Messenger
- Website: https://cloudmessenger.in/
- LinkedIn: https://www.linkedin.com/in/ulhas-narwade-aws-certified-devops

#AWS #AmazonRDS #EC2 #AmazonLinux #MySQL #Database #VPC #SecurityGroups #DevOps #CloudComputing #CloudMessenger
