# TASK
## Introduction 
Task involves setting up and configuring a firewall using Firewalld with nftables on a Linux virtual machine. The task specifies the use of three zones: trusted-zone, internal-zone, and public-zone.

### Zones
The firewalld service handles rule groups through entities known as zones. These zones consist of rules that determine which traffic is permitted based on the level of trust in the network. By assigning network interfaces to specific ```zones```, the firewall governs the allowed behavior accordingly.

### Rule Permanence
In Firewalld, rules can either be applied to the active runtime ruleset or be set as permanent. By default, when adding or modifying a rule, it only affects the current running firewall configuration. However, after the next system reboot or reload of the firewalld service, only the permanent rules will persist.

For most operations using the firewall-cmd command, you can include the ```--permanent``` flag to specify that the changes should be applied to the permanent configuration.