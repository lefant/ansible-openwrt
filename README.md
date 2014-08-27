ansible-openwrt
===============

configure your openwrt system (and variants, cerowrt in my case) using
ansible.

works with the official raw module und some custom modules to avoid
having to run python on the target - no extra dependencies for your
embedded target system.

currently under development. i have a way to set uci values if needed
and run commit at the end if anything changed. i am trying to at least
build a superset of the [config-cerowrt.sh] shell script plus whatever
i will need myself.

be careful with blindly running it, if you connect to your openwrt via
wifi and you change network settings you may lock yourself out.


see host_vars/example-gw.home.lan for how to override the role
defaults in your local clone.


TODO
====
- port official opkg module to shellscript or raw


[config-cerowrt.sh]: https://github.com/richb-hanover/CeroWrtScripts/blob/master/config-cerowrt.sh
