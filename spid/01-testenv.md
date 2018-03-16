# Configuring a SPID development environment

Do you want to create a service which accepts users logging in through SPID?
This guide will show you how to create a basic service which uses SPID authentication.


## The test environment

To be able to create a service which accepts SPID users, the very first thing you need to set up is a fake Identity Provider. This way you will have full control over your users and will be able to test many different cases.

Setting up the test environment might be challenging. Luckily, we have a plug-and-play solution, through a Docker container. You can install it easily here:
https://github.com/italia/spid-testenv-docker

Otherwise, just use the shared one at https://idp.spid.gov.it:8080/

## Community resources for SPID integration

The community of Developers Italia maintains many projects aimed at making SPID integration easy. They are libraries, plugins, SDKs covering many programming languages, frameworks and CMSs. You can see a list [here](https://github.com/italia/spid-docs/tree/master/resources-checklist).

### Activity #1:
Many of those projects are not feature complete, so you can help us make them robust by testing them and reporting issues.

### Activity #2:
We have prepared a [feature checklist](https://github.com/italia/spid-docs/tree/master/resources-checklist) which should be applied to the README of each project. Choose a project and help us assess what its features are, and what's missing. Open a pull request to add the checklist to the README file. Your work will be very helpful for developers and the community, as it will provide guidance for further development.
