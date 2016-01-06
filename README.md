# Mirage

**This is very much a work in progress! There is still a lot of work to be done in terms of tidying up the CSS and making the theme more configurable**

A modern feeling theme for Jenkins CI server.

### Screenshots

<img src="http://unfinisheddev.com/assets/mirage-dashbord.jpg" alt="Jenkins Dashboard" />

<img src="http://unfinisheddev.com/assets/mirage-console-output.jpg" alt="Jenkins Console Output" />

<img src="http://unfinisheddev.com/assets/mirage-configure.jpg" alt="Jenkins Configuration Screen" />

## Installation in Jenkins

If you want everybody who accesses your Jenkins server to see this theme you will need access to install plugins and configure the system.

1. Install [Jenkins Simple Theme Plugin](https://wiki.jenkins-ci.org/display/JENKINS/Simple+Theme+Plugin)
2. Install [jQuery Plugin](https://wiki.jenkins-ci.org/display/JENKINS/jQuery+Plugin)
2. Upload the `dist/mirage.min.css`, `dist/mirage.min.js` and `logo.png` files to a location that is acceesible over HTTP to all your visitors (the `userContent` directory of your Jenkins install is a simple location for this)
3. In Jenkins, click "Manage Jenkins", then "Configure System", then specify the CSS and Javascript URL's for this theme in the Theme section. If you are hosting this theme in `userContent` and using Jenkins default settings, you would enter the following URLs

```
http://<your-jenkins-url>:8080/userContent/mirage.min.css
http://<your-jenkins-url>:8080/userContent/mirage.min.js
```

## Development Instructions

If you want to modify the theme or create a pull request then you'll need to ensure you have a few pre-requisites installed.

* NodeJS
* Grunt
* Vagrant
* VirtualBox
* Ansible

### Vagrant Environment

The Vagrantfile will create a CentOS 7 virtual machine and install Jenkins, the simple theme plugin and jquery plugin.

It will also syncronise the `./build` directory in the repository to the `/var/lib/jenkins/userContent` directory in the virutal machine, allowing you to easily add the theme to the Jenkins and test updates to the styles and scripts.

#### Ansible

The Vagrantfile will require [Ansible to be installed](http://docs.ansible.com/ansible/intro_installation.html) and available in the path for the provisioning to run.

## This is *NOT* an Attack on Jenkins

This theme is not an attack or criticism of Jenkins of the developers of Jenkins in anyway! I've used a number of CI servers and I continue to be impressed how it matches and often beats the features and reliabilty of those others that charge for usage.

I made this theme as a bit of fun and learning opportunity. I hope people like it and use it but this theme is useless without Jenkins, remember that.
