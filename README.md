# Setting up Dev Env
![MicrosoftTeams-image.png](MicrosoftTeams-image.png)
## Installation of Vagrant, VirtualBox and Ruby
- https://github.com/khanmaster/vb_vagrant_installtion for steps
### Vagrant commands
- `vagrant up` to launch vm
- `vagrant destroy` to delete everything
- `vagrant reload` to reload any new instructions in Vagrantfile
- `vagrant halt` pauses VM  
- `vagrant` displays command options
- Let's `ssh` into our VM and launch nginx web-server
- use `apt-get` package manager in Linux - for Mac homebrew (or brew)
- to use command in `admin` use `sudo` before the command
- `sudo apt-get upgrade -y` - `-y` sets any "Do you want to do this y/n" to yes automatically
- `sudo apt-get update -y`
- `ping www.bbc.co.uk`
- to work in admin all the time(not recommended) `sudo su` and you will land in admin mode
- We will install nginx in guest machine/VM/ubuntu 16.04
- launch default nginx page in host machine's browser
- to come out of VM `exit`
- `systemctl status <package>` to verify installation and running of packages
- can use `systemctl` to restart with `restart` and `start` in place of `status`
- `vagrant plugin install vagrant-hostsupdater` run in host machine GitBash/terminal


- Let's automate the tasks we manually did previously
- create a file (using `sudo nano filename`) called `provision.sh` containing:
- `sudo apt-get update -y`
- `sudo apt-get upgrade -y`
- `sudo apt-get install nginx`
- `systemctl status nginx`
- must have `#!/bin/bash` as first line for linux to recognise


- one command will run all the above commands from the .sh file
- to run `provision.sh` we need to give file permissions and make this file executable
- to change permissions we use `chmod` with required permssion then file name (`+x` for executable)
- `chmod +x provision.sh`, once executable will be different colour in terminal/GitBash
- `sudo ./filename` to execute

- http://permissions-calculator.org/ for more permissions, can use numbers instead of letters
- `chmod 777 filename` to make executable
- `ll` lists directories with current permissions
- `man` added before a linux command gives more details - `ls man` etc
- wildcards `*` can be used to select everything with certain extension etc, `rm -rf *.txt` will delete all txt files

- to end a process (`ps aux` shows list of running processes) use `sudo kill <PID number>`
- pike symbol | can be used to search more specifically