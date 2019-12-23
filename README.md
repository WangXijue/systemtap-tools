# systemtap-tools

## compile kernel module
sudo stap -p4 -DMAXSKIPPED=9999 -m ik -g inject_delay_vhostnet.stp vhost-12995 100

## load kernel module
$ sudo staprun ik.ko

# turn on/off inject
$ echo on | sudo tee /proc/systemtap/ik/inject
$ echo off | sudo tee /proc/systemtap/ik/inject

