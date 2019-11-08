# upandrun #

A very simple vagrant environment for getting up and running with Puppet Enterprise. 

This repo provides you with a complete, yet simple environment that consists of a master (CentOS7), as well as a Linux (CentOS7) and Windows VM.

Shout out to Grace Andrews for putting this together and Jamie Mickelson for showing it to me! I have updated this fork to include a wrapper shell script that allows you to set the PE version at start up.

## Pre-Steps ##

Before cloning this repo, you'll have to install both [Vagrant](https://www.vagrantup.com/) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads). 

For downloads : https://puppet.com/download-puppet-enterprise/thank-you

Once both are installed, you'll be able to do the following steps from your CLI:

```
'git clone https://github.com/hsnodgrass/upandrun'

'cd upandrun'

**`start.sh` will use either a command line arg (first preference) or the envar `UAR_PE_VER` to determine which PE version should be downloaded. The default version is `2018.1.3`.**

./start.sh 2019.2.0

**OR**

export UAR_PE_VER='2019.2.0'
./start.sh

**OR to use default version**

./start.sh

**To verify that the vagrant boxes are up**

vagrant status

**ssh into each box individually**

'vagrant ssh /master/'
'vagrant ssh /linux/'
to ssh into the windows box, you'll need remote desktop
```

In order to get into your boxes, you can either ssh in from your command line, or you can use the VirtualBox interface. You can read more on Vagrant commands in their [docs](https://www.vagrantup.com/docs/cli/). 

You can also see your console in the browser by going to 'https://192.168.50.4'. This should give you a view of the GUI for continued management of your nodes. The default user name is `admin` and the default password is `puppetlabs`.
