## How to run:

 ansible-playbook --ask-become-pass --verbose --ask-pass  setup.yml

 ansible-playbook --ask-become-pass --verbose --ask-pass  setup.yml --skip-tags "prereq"


## after the above command:
as super user run:

/sbin/vboxconfig

#to enalbe routing to virtual machines is necessary make a vbox interface
to create de interface use:
    VBoxManage hostonlyif create
and to change the default ip address:
    VBoxManage hostonlyif ipconfig vboxnet0 --ip 192.168.1.130 --netmask 255.255.255.0

note: vboxnet0 is the first interface created, could be necessary change it to vboxnetX

#is also necessary activate the arp_proxy on both intherfaces:
echo 1 > /proc/sys/net/ipv4/conf/eth1/proxy_arp