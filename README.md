# Problem statement
a bunch of powershell scripts to support patching windows machines in siloed domains that sometimes work

# Assumptions
- All machines are domain joined
- Users are domain admins
- Machines are servers of same OS 2022 datacenter or server core
- Patch files need to be copied to the distant machine
- Machine needs to report success or failure or pending reboot
- Machines in hypervisor may or may not be accessible from outside

# Issues
- Copying files to the server core systems inside the hypervisor is a problem and requires 'connect'

# Architecture
- Util machines (hyper v hosts)
- DCs and wacs are running inside UTIL machines
