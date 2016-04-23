
Install VirtualBox, install Vagrant.

In windows, use PowerShell instead of console.

cd to install folder

```
vagrant up
```

If you are running on windows, after installing Vagrant run in console (https://github.com/vovimayhem/vagrant-guest_ansible):

```
vagrant plugin install vagrant-guest_ansible
```


If the page loads but is styled wrong, purge all caches [http://local.tutoringzone.com:8080/admin/purgecaches.php][cache].
[cache]: http://local.tutoringzone.com:8080/admin/purgecaches.php

In order to log in, you will need to edit your hosts file (https://www.google.com/?ion=1&espv=2#q=edit%20hosts%20file). Add the following entry:
```
127.0.0.1 local.tutoringzone.com
```

# README #

This README would normally document whatever steps are necessary to get your application up and running.

### What is this repository for? ###

* Quick summary
* Version
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact