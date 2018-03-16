## Nginx provisioning with Ansible & Vagrant

### Synopsis
[Vagrant] and [VirtualBox] (or some other VM provider, eg. [HyperV]) can be used to quickly build or rebuild virtual servers. This shows how to use them to provision an [Nginx] server.

#### Prerequisites
  1. Download and Install [VirtualBox]
  2. Download and Install [Vagrant]
  3. Install [Ansible]

#### Installations on WSL
 - Install [VirtualBox] on the Windows guest
 - Install [Vagrant] & [Ansible] on the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
 - Add the following to the user's bash profile: `.bashrc`
 ```shell
 # Vagrant WSL-Windows Access
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
export VAGRANT_WSL_WINDOWS_ACCESS_USER_HOME_PATH="/mnt/c"
export PATH=$PATH:"/mnt/c/Program Files/Oracle/VirtualBox"
 ```
 *Refer to [Vagrant on WSL](https://www.vagrantup.com/docs/other/wsl.html) for further options*

 #### Usage
 - Within the folder containing the `Vagrantfile` run
```shell
$ vagrant up --provision
```
- Open browser to see Nginx loading page on: `127.0.0.1:8080`

[Vagrant]: https://www.vagrantup.com/downloads.html "Vagrant"
[VirtualBox]: https://www.virtualbox.org/wiki/Downloads "VirtualBox"
[Ansible]: https://www.ansible.com/ "Ansible"
[HyperV]: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/ "HyperV"
[Nginx]: https://www.nginx.com/ "Nginx"

