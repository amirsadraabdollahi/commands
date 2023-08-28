# virtualization

1. cpu info
```commandline
lscpu
cat /proc/cpuinfo
```
if you see ```hypervisor``` in your cpu info, then this OS is a guest OS and you are in the virtual machine.

2. the ```kvm``` module is a module that manage virtualization.
to see if you have this module or not use this command ```lsmod | grep kvm```

3. ```cloning``` an existing machine is copy the exact same vm with the same config and create new vm.

4. using ```Open Virtualization Format``` to move machines between hypervisors.