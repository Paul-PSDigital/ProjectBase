ProjectBase
===========
A Project base to start working with standard setup: Doctrine / ZF2 / PHPUnit / Vagrant / Phing

Using Vagrant
==========
First the Vagrant needs to be installed on your machine, with VirtualBox:
- Vagrant: http://www.vagrantup.com/
- Virtual Box: https://www.virtualbox.org/

It is then required to navigate to tools/vagrant and type: vagrant up

A Virtual Machine will then be configured using puppet as a LAMP server to deliver this project.
Changes made in the project will be synched across to the virtual machine.


Setting up the Project
==========
Before the running the project it will be required to run composer. This fetches the dependencies of
the project from packagist. This configuration assumes you have composer installed on your machine. 
Optionally you can download the composer.phar into the base of the directory and run composer.phar install 
/ php composer.phar install

- Composer: http://getcomposer.org/

Writing / Running Tests
==========
The phpunit.xml file is provided in the root of the project - please define the test directories within this.
A coverage report can be seen on your vagrant host at localhost/coverage-report or browse on your local
file system to src/public. Type . ./src/vendor/bin/phpunit or run your locally installed phpunit in the project
root to generate this report

- PHPUnit: http://phpunit.de/manual/3.8/en/index.html