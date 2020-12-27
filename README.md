# ubuntu-ansible-config

My ansible configuration files for Ubuntu systems.

It is tested on Ubuntu 20.04 LTS and may or may not work on other distros and versions.

It basically installs some packages I always want ready to go, and sets a more complete dark mode.

It also installs an optional desktop environment based on i3 tiling window manager called Regolith.

## Usage

Make sure the host_user is set to your username.

Cutting and pasting the following commands into a terminal will do just that:

    sudo apt update
    sudo apt install git ansible
    sudo ansible-pull -U https://github.com/lab1702/ubuntu-ansible-config.git --extra-vars "host_user=$USER"

## Notes

This installs bpytop which needs a bit more config if you want to use it.

I'm leaving it out of the ansible file for now.

    sudo snap connect bpytop:mount-observe
    sudo snap connect bpytop:network-control
    sudo snap connect bpytop:hardware-observe
    sudo snap connect bpytop:system-observe
    sudo snap connect bpytop:process-control
    sudo snap connect bpytop:physical-memory-observe
