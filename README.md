<<<<<<< HEAD
# Druss
Druss is an Ansible project that help you configure your Debian environnement. For example you can install your desktop manager, your favorite shell and your IDE with one configuration file. For now this project only fits my configuration, but i will add more soon.
## Getting Started
### Prerequisites

Before using Druss you need to install Ansible on your system.
```
sudo apt install ansible
```
Then you need to have ssh acces as root on every system you wish to configure.
### Installing
To use Druss, you only need to clone the repositorie
```
git clone https://github.com/Siorde/druss.git
```
## Using Druss
### Hosts file
First of all, you need to create a "hosts" file that while iventory all the systems to configure.
```
192.168.0.10  ansible_user=root host_user=toto
192.168.0.11  ansible_user=root host_user=tata
```
Where "toto" and "tata" are the users to whom we want to apply the configuration.
### Configuration file
Then you have to complete the configuration file that define the configuration you want to apply on the hosts. This file is "roles/druss/vars/main.yml". Every variables is explain in this file.
### Running the role
Finaly you just have to lunch the role :
```
ansible-playbook -i /path/to/the/hosts/file /path/to/the/depo/druss/druss.yml
```
## Authors
* **Quentin Aubry** - *Initial work* - [Siorde](https://github.com/Siorde)
## License
This project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details
=======
# druss
An Ansible job that help you configure your Debian environnement 
>>>>>>> d55e7a9bd194efb7a70257eef9df4818fa5acb9f
