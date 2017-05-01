## Intro

This exercise requires ansible, VirtualBox and Vagrant.  Documentation is online to assist you in those installations.    Once you have installed the prerequisites you can start this exercise with by cloning the repo and running vagrant up.  Each of the items below should be implemented via ansible.  Please follow the directions below, and once complete submit a PR with the changes submitted below for review.

## Directions
#### 1. Fork the repo.

#### 2.    Create another ansible role that does the following:

  - Install FluentD.
  
  - Takes logging output from the docker daemon installed from the docker roles and writes output to a file location of your choice within the VM.  FluentD should be writing the file.  You can select which method to provide the data input to FluentD.
  
  - Download the latest nodeJS linux binaries from nodeJS.org.  Add node and npm ensure that links are used all calling the executables from locations in the existing path.
  
  - To assist in the ability in future troubleshooting install netcat, and nslookup.
  
#### 3.    Add to the existing docker role that does the following.

  - Start the docker registry container from the docker hub and specify a restart policy.
  
  - Select an image from docker hub.  Tag and push it to your local registry.  (Hint: you may have to modify the docker systemd service via a jinja template to push to a unsecure registry.  Make sure you restart the docker daemon as part of this change.)
  
  - Using the official mysql container add a mysql container.  Specify a runtime policy and a custom password of infratest for the root user, and ensure the mysql port is avaiable on the ost.
  
  - Make sure the mysql port is accepting connectings on the host.  Add tasks to the playbook so if the port is not accepting connections the playbook fails.
  
  - Modify the existing OpenResty container so that you can access the web servver from inside the container on the host from port 8081.
  
#### 4.    Submit a PR with your changes.
  