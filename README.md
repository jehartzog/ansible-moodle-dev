# README #

This is an example of how to get a local dev server up and running without any interaction or configuration.

Note that the database dump and development private key files were removed from this example, so you will need to use your own web application files!

### How do I get set up? ###

* Install [VirtualBox](https://www.virtualbox.org)
* Install [Vagrant](https://www.vagrantup.com)
* If using Windows, run `$ vagrant plugin install vagrant-guest_ansible` to allow [Ansible to run inside the guest VM](https://github.com/vovimayhem/vagrant-guest_ansible).
* Run `$ vagrant up` and watch the magic!
* Once complete, visit http://localhost:8080 to see the page up and running

### End result ###

* Vagrant will:
  * Download and setup up the Ubuntu VM, and run the ansible playlist against it
  * Forward localhost port 8080 to the VM port 80
  * Create a link between the VM web application files and the host "../html" directory to allow for local file editing
  
* The ansible playlist will:
  * Install and configure Apache to serve the PHP application
  * Install and configure MariaDB (MySQL replacement), and import a database dump (database dump not included)
  * Clone the GIT repo for the web application into the webserver directory and set permissions (repo private key not included)
  * Create a moodledata directly and set permissions

### Other Tips ###

* When working on your local machine, you will want to edit your [hosts file](https://www.google.com/?ion=1&espv=2#q=edit%20hosts%20file) and add the following line. This will allow third-party tools (Facebook login, other embeds) that restrict based on domain name to load properly.
```
127.0.0.1 yourdomain.com
```
* Depending on the snapshop you take, if your Moodle site comes up with incorrect styles you may need to purge all caches <http://localhost.com:8080/admin/purgecaches.php>.

### Questions? ###

* I created this to show how easy it was to use Vagrant and Ansible to provision and manage a local moodle development webserver. No need to struggle with a Windows stack with a complex GUI configuration that requires significant set up time each time you shift computers.
