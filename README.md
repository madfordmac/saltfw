# saltfw
So you have multiple hosts with public exposure, and they're all running
fail2ban or some other tool to watch the logs of public services and look for
brute-force password attempts and block those nefarious hosts at the firewall.
Wouldn't it be great if your hosts could share that information so that if any
host encounters a bad actor, everybody is immune? Wouldn't it be great if such
a tool could look for groups of IP addresses so those Chinese botnets didn't
have to get blocked one at a time? Wouldn't you love to have pretty graphs of
what's going on? Saltfw to the rescue!

## Assumptions
* All hosts are part of a saltstack deployment. Salt is used to push updated configs.
* All hosts have a trusted private network to communicate on.

## Requirements
* Python

### Additional Requirements for Master Node
* Redis database – used for IP aggregation
