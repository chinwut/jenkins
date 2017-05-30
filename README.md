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
