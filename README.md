# Title: My Journey into DevOps: Setting Up NGINX on Ubuntu

**Introduction**
As part of my DevOps learning journey, I was tasked with setting up and configuring NGINX on a fresh Ubuntu server. This task was designed to help me gain hands-on experience with web server configuration and deployment. Here’s how I approached it, the challenges I faced, and what I learned along the way.

**Approach to Completing the Task**
Provisioning the Server: I started by setting up an Ubuntu 24.04 LTS server on AWS, t2.micro instance was used. My security group allowed all traffic including SSH access (port 22) and HTTP traffic (port 80) from anywhere. Once done, I connected to the instance using ssh client(Mobaxterm).

**Installing NGINX:** 
Using the terminal, I updated the package list and installed NGINX with the command: 
```
sudo apt upgrade && sudo apt update -y
sudo apt install nginx -y
```
Verified that installation was completed successfully, also it is up and running:
```
sudo systemctl status nginx
```
**Creating a Custom HTML Page:** 
I created a simple HTML file at /var/www/html/index.html with the message: “Welcome to DevOps Stage 0 - Tolulope Ojo/Ops-ack”.
```
<!DOCTYPE html>
<html>
<head>
<title>Welcome to DevOps Stage 0</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to DevOps Stage 0-Tolulope Ojo/Ops-ack</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```
**Restarted NGINX to apply changes**
```
sudo systemctl restart nginx
```
**Testing the Configuration:** 
After ensuring NGINX was running, I accessed the server’s public IP in my browser and saw the custom page.
![NGINX success page](https://github.com/user-attachments/assets/1d1e80e9-0437-48b3-91f6-012da5ba8918)

## **Challenges Faced**
**Firewall Issues:** 
Initially, I couldn’t access the server because the firewall was blocking HTTP traffic. I resolved this by allowing all traffic for the inbound rule on AWS.

## **Deployed Website**
http://54.89.218.226/

## **Learning and Professional Growth**
This task taught me the basics of web server configuration and how to troubleshoot common issues. It also reinforced my understanding of Linux commands and server management. As someone aspiring to become a DevOps engineer, this hands-on experience was invaluable. 

## References
• DevOps Engineers -  https://hng.tech/hire/devops-engineers
• Cloud Engineers -  https://hng.tech/hire/cloud-engineers
• Site Reliability Engineers -  https://hng.tech/hire/site-reliability-engineers
• Platform Engineers -  https://hng.tech/hire/platform-engineers
• Infrastructure Engineers -  https://hng.tech/hire/infrastructure-engineers
• Kubernetes Specialists -  https://hng.tech/hire/kubernetes-specialists
• AWS Solutions Architects -  https://hng.tech/hire/aws-solutions-architects
• Azure DevOps Engineers -  https://hng.tech/hire/azure-devops-engineers
• Google Cloud Engineers -  https://hng.tech/hire/google-cloud-engineers
• CI/CD Pipeline Engineers -  https://hng.tech/hire/ci-cd-pipeline-engineers
• Monitoring/Observability Engineers -  https://hng.tech/hire/monitoring-observability-engineers
• Automation Engineers -  https://hng.tech/hire/automation-engineers
• Docker Specialists -  https://hng.tech/hire/docker-specialists
• Linux Developers -  https://hng.tech/hire/linux-developers
• PostgreSQL Developers -  https://hng.tech/hire/postgresql-developers


## **Conclusion**
Completing this task was a rewarding experience that deepened my understanding of NGINX and server configuration. I’m excited to continue my DevOps journey and tackle more advanced challenges in the future.
