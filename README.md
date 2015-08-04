ansible-openwrt
===============

Configure your [openwrt] system (and variants, cerowrt in my case) using
[ansible].

Works with the official raw module und some custom modules to avoid
having to run python on the target - no extra dependencies for your
embedded target system.

Currently under development. I have a way to set uci values if needed
and run commit at the end if anything changed. I am trying to at least
build a superset of the [config-cerowrt.sh] shell script plus whatever
i will need myself.

Be careful with blindly running it, if you connect to your openwrt via
wifi and you change network settings you may lock yourself out.

See `host_vars/example-gw.home.lan` for how to override the role
defaults in your local clone.


Installation (ansible-galaxy and librarian)
-------------------------------------------

In an attempt to make this more reusable, I am trying to move all the
roles to [ansible galaxy] and use [librarian-ansible] to manage
dependencies. librarian-ansible uses the `Ansiblefile` to declare the
external playbooks that ansible-openwrt requires.

To automatically retrieve dependencies:

    cd ansible-openwrt
    gem install librarian-ansible
    librarian-ansible install


Contributors
------------

Jan Wagner ([waha on github] pointed out that the uci module needs to
return json and contributed related fixes allowing it to work with
recent versions of ansible.


TODO
----
- port official opkg module to shellscript or raw
- how to manage /etc/dropbear_authorized_keys? port file to sh?

[openwrt]: https://openwrt.org/
[ansible]: http://www.ansible.com/
[config-cerowrt.sh]: https://github.com/richb-hanover/CeroWrtScripts/blob/master/config-cerowrt.sh
[ansible galaxy]: https://galaxy.ansible.com/list#/users/3407
[librarian-ansible]: https://github.com/bcoe/librarian-ansible
[waha on github]: https://github.com/waja
