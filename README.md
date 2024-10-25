Ansible via Teleport

```
tsh login --proxy connectcarolina.teleport.sh
tsh config > -F ./teleport_ssh_config
```

The `teleport_ssh_config` file will match all hosts that fit the pattern `*.connectcarolina.teleport.sh` and run it through Teleport.

Here's a quick command to generate the inventory file

```
% tsh ls -f names | sed 's/$/\.connectcarolina.teleport.sh/g' | tee inventory
los-1.connectcarolina.teleport.sh
occ-12.connectcarolina.teleport.sh
occ-13.connectcarolina.teleport.sh
occ-14.connectcarolina.teleport.sh
occ-15.connectcarolina.teleport.sh
occ-16.connectcarolina.teleport.sh
occ-4.connectcarolina.teleport.sh
```
