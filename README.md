# Three-Tier-AWS-Web-Application
A containerized web application deployed on AWS with private database connectivity, load balancing, and centralized monitoring.
Architecture

Networking: Custom VPC with public, private application, and isolated database subnets across two Availability Zones.

Compute: Amazon EC2 running Dockerized Nginx and Flask services.

Database: Private Amazon RDS for MySQL with encryption enabled.

Traffic management: Internet-facing Application Load Balancer forwarding HTTP traffic to the application.

Monitoring: CloudWatch container logs and an unhealthy-target alarm integrated with Amazon SNS email notifications.

Operations: Validated container recovery after an EC2 reboot and tested the application through the ALB endpoint.

Technologies

AWS VPC, EC2, RDS, Application Load Balancer, IAM, Systems Manager Session Manager, Docker, Docker Compose, CloudWatch, SNS, Linux, Flask, MySQL, Nginx.

Validation

Verified application responses through the ALB.

Confirmed Flask could retrieve records from RDS.

Verified container logging in CloudWatch.

Configured unhealthy-target alerting through SNS.

Tested container recovery after an EC2 reboot.

Cost-conscious deployment

The AWS infrastructure was used for validation and then scheduled for teardown to avoid ongoing resource charges. Screenshots and architecture documentation preserve evidence of the working deployment.

Source: Adapted from the Docker Awesome Compose nginx-flask-mysql sample, with AWS infrastructure, private RDS integration, and monitoring configuration.
