Usage:
start.sh -p start # Deploys the project
start.sh -p update # Restarts docker containers, pushing any changes added to specified image on DockerHub to live

Deployment involves:
Two EC2 instances for running backend app written on Node.js
EC2 instance for load balancer on Nginx with less-connections logic
EC2 instance for webserver, running index.php page
EC2 instance for monitoring of backend servers, implemented with prometheus

API entry points: / and /ring-ring on 80 port of load balancer

IP addresses of API servers are added to monitoring automatically

Architecture provided on image:

![Arhitecutre image](https://github.com/Crocodility/Devops_task/blob/main/diagram.png)
