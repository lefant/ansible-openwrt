openwrt-network
================

network (and dhcp) config of your openwrt system.
compare: [http://wiki.openwrt.org/doc/uci/network] and 
[http://wiki.openwrt.org/doc/uci/dhcp]

Role Variables
--------------

a bunch of per interface settings are all nested in a dict
`network` and another `dhcp` one. the layout is a bit weird because
i use with_subelements. look at the defaults and tasks directory.
if you have a suggestion for how to do it more effectively without
duplication, let me know!

you may want to consider `hash_behaviour=merge` in your ansible.cfg

Dependencies
------------

[lefant.openwrt-uci]

Example Playbook
----------------

[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]

Requirements
------------

must be kept minimal as this is supposed to run on openwrt embedded
systems. in particular we try get by with plain POSIX shell, using
neither python nor bash in any way. lua could be an option as that
seems to be the openwrt scripting language of choice.

License
-------

BSD

Author Information
------------------

Jan Wagner [http://blog.waja.info/]



[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]: https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml
[http://wiki.openwrt.org/doc/uci/network]: http://wiki.openwrt.org/doc/uci/network
[http://wiki.openwrt.org/doc/uci/dhcp]: http://wiki.openwrt.org/doc/uci/dhcp
[lefant.openwrt-uci]: https://galaxy.ansible.com/list#/roles/1645
[http://e.lefant.net/]: http://e.lefant.net/
