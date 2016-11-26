Installs and configures sentry version 8.7.0
===================================

I wrote this ansible playbook in such a way that it installs sentry version(8.7.0) in AWS EC2 instances.

In AWS create an EC2 instance and give a DNS name with PUBLIC dns and in inventory file append the DNS.


> **Example:**
> 
> [sentry]
> DNS name

To execute this playbook you have to execute:

> $ ansible-playbook sentrysetup.yml


once the playbook executed successfully on the EC2 instance you will be able to access sentry GUI by giving the DNS name as the url.



Open <i class="icon-file"></i>sentrysetup.yml file you have to <i class="icon-pencil"></i> rename the credentials according to your requirements.

Here, <i class="icon-folder-open"></i> sentry-8.7.0 is the ansible role.

**sentry.server** in **sentrysetup.yml** takes the DNS name and configures the sentry.

For the **sentry.secretkey** you have create a new key from [here](http://www.miniwebtool.com/django-secret-key-generator/)  to set the secret_key setting under the sentry namespace to a unique key that acts as a signing token in production environments.



