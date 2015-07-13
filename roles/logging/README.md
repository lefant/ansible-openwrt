openwrt-logging
==============

configure logging aspects of your openwrt system.
compare: [http://wiki.openwrt.org/doc/uci/system]


Role Variables
--------------


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

Jan Wagner, [http://blog.waja.info/]



[http://wiki.openwrt.org/doc/uci/system]: http://wiki.openwrt.org/doc/uci/system
[lefant.openwrt-uci]: https://galaxy.ansible.com/list#/roles/1645
[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]: https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml
[http://e.lefant.net/]: http://e.lefant.net/
