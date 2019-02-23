# Druss
Druss is an Ansible project that simplify the basic configuration of your Debian environnement. You can select which desktop environnemnt, Ide, browser,... you want in a configuration file and Druss will do the installation for you.
## Getting Started
### Prerequisites

Before using Druss you need to install Ansible 2.7 on your master system.
Here is the instructions from ansible documentation :
```
sudo echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt update
sudo apt install ansible
```
Then you need to have ssh access with root privileges on every system you wish to configure.
### Installing
As an Ansible role, you only need to get the repository (of course, you need to have git install on your system).
```
git clone https://github.com/Siorde/druss.git
```
## Using Druss
### Hosts file
First of all, you need to create a "hosts" file that while inventory all the systems to configure.
In this file you must specify your ssh user who must have the root privileges : ansible_user
And you need to specify for which user the configuration will be apply : host_user
#### Example
```
192.168.0.10  ansible_user=root host_user=toto
192.168.0.11  ansible_user=root host_user=tata
```
### Configuration file
The whole point of Druss is to install elements and their configurations with one configuration file : "roles/druss/vars/main.yml".
So edit the file to match the configuration you want. Each variable is optional.
You can choose :
 - the display manager, and use your a configuration file
 - the IDE
 - the browser
 - the display manager
 - the shell, and use your configuration file
 - the terminal, and use your configuration file
 - the text editor, and use your configuration file
 - the screen save and a shortcut
 - if you want numlock to be set on the login screen
 - if you want your user to be in the sudo group
 - a list a package you want to install
### Running the role
Finaly you just have to lunch the role :
```
ansible-playbook -i /path/to/the/hosts/file /path/to/the/depo/druss/druss.yml
```
## Authors
* **Quentin Aubry** - *Initial work* - [Siorde](https://github.com/Siorde)
## License
This project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details
# druss
An Ansible job that help you configure your Debian environnement
