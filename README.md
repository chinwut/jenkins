# jenkins

# Installation

## Unix/Linux
## Debian/Ubuntu
  On Debian-based distributions, such as Ubuntu, you can install Jenkins through apt.
  Recent versions are available in an apt repository. Older but stable LTS versions are in this apt
  repository.

    wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ >
    /etc/apt/sources.list.d/jenkins.list'
    sudo apt-get update
    sudo apt-get install jenkins
## OS X
  To install from the website, using a package:
  *Download the latest package
  *Open the package and follow the instructions
  Jenkins can also be installed using brew:
  
### Install the latest release version
    brew install jenkins
### Install the LTS version
    brew install jenkins-lts

## Docker
  You must have Docker properly installed on your machine. See the Docker installation guide for details.

### First, pull the official jenkins image from Docker repository.
    docker pull jenkins
    
### Next, 
    docker run -d -p 49001:8080 -v $PWD/jenkins:/var/jenkins_home -t jenkins
    
run a container using this image and map data directory from the container to the host
e.g inthe example below /var/jenkins_home from the container is mapped to jenkins/ directory from the
current path on the host. Jenkins 8080 port is also exposed to the host as 49001.

### In the terminal window, we'll use the cat command to display the password:

    sudo cat /var/lib/jenkins/secrets/initialAdminPassword
