# Configuring a SPID development environment

Do you want to create a service which accepts users logging in through SPID?
This guide will show you how to create a basic service which uses SPID authentication.


## The test environment

To be able to create a service which accepts SPID users, the very first thing you need to set up is a fake Identity Provider. This way you will have full control over your users and will be able to test many different cases.

Setting up the test environment might be challenging. Luckily, we have a plug-and-play solution, through a Docker container. You can install it easily here:
https://github.com/italia/spid-testenv-docker

## Creating a service

There are a lot of technological choices possible for creating your service.

### Case 1: using our Ansible Playbook
https://github.com/italia/spid-sp-playbook


### Case 2: using an authentication plugin


## Publishing your service



## References
