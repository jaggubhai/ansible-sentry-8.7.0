Installs and configures sentry version 8.7.0
===================================

I wrote this ansible playbook in such a way that it installs sentry version(8.7.0) in AWS EC2 instances.

In AWS create an EC2 instance and give a DNS name with PUBLIC dns and in inventory file append the DNS.


> **Example:**
> 
> [sentry]

To execute this playbook you have to execute:

> $ ansible-playbook sentrysetup.yml


once the playbook executed successfully on the EC2 instance you will be able to access sentry GUI by giving the DNS name.