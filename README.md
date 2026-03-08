🚀 Hands-on with Ansible Automation: Deploying Apache Using Roles
I recently worked on a small automation project using Ansible, where I created a role to deploy and configure an Apache web server in a structured and reusable way.
🔧 Project Overview
In this project, I created a role called appache that performs the following tasks:
• Installs the httpd (Apache) package
• Starts and enables the Apache service
• Copies a custom index.html file to /var/www/html/index.html
• Deploys an Apache configuration file using a Jinja2 template (node1.conf.j2)
• Places the configuration inside /etc/httpd/conf.d/node1.conf
• Uses Ansible handlers to restart the Apache service only when the configuration changes
📂 Role Structure
roles/appache
tasks/main.yml → Install package, start service, copy files
handlers/main.yml → Restart httpd when notified
templates/node1.conf.j2 → Apache configuration template
files/index.html → Web page content
▶️ A playbook was then created to call the role and apply it to the target hosts, making the deployment clean, modular, and reusable.
💡 What I Learned
• How to structure Ansible projects using roles
• Using templates (Jinja2) to manage configuration files dynamically
• Implementing handlers and notifications for efficient service management
• Writing reusable and maintainable infrastructure automation code
This project helped me understand how Infrastructure as Code (IaC) can simplify server configuration and deployment.
Looking forward to building more automation projects with Ansible, Linux, and DevOps tools.
hashtag#Ansible hashtag#DevOps hashtag#Automation hashtag#Linux hashtag#InfrastructureAsCode hashtag#Apache hashtag#ConfigurationManagement
