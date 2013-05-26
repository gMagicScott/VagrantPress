VagrantPress
============

Vagrant and Chef provisioning for WordPress development. **This is a new project. This README is more of a guide about how this _should_ work, not necessarily how it _does_ work**.

## The Goal ##

This project is designed to be a submodule of your WordPress project.

```bash
mkdir my-project
cd my-project
curl -sS http://gmagicscott.github.io/VagrantPress/installer | bash
vagrant up
```

## How that happens ##

- Initializes a new git repo in your current directory
- Adds VagrantPress as a submodule in the `Vagrantfolder` directory
- Interactive prompts gather basic site information
- Generates a `Vagrantfile` in the current directory with the options you provide


## During the Chef run... ##

Start off with a base Ubuntu 12.04.* base box
- Set the clock
- Install NGINX
- Install Percona's fork of MySQL
- Install PHP
- Install APC
- Install git
- Install WP-CLI
- Create a WordPress site based on Mark Jaquith's WordPress Skeleton

## You should be able to ##
- Access WP-CLI by a Vagrant plugin, so you don't have to live inside a `vagrant ssh`
