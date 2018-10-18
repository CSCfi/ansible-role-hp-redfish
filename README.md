ansible-role-hp-redfish
=========

A role that fetches HP's ilorest tool from https://github.com/HewlettPackard/python-redfish-utility/releases and then installs it

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

curl

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-hp-redfish }

Can we do this?
------------

A) HP also publishes debs, MSI and .pkg. Would be cool if the role supported those OSs too

B) Would be sweet to use github_release ansible module but then this role would require specifying a github token I think?

<pre>
- name: Get latest release of test repo using username and password. Ansible 2.4.
  github_release:
    user: HewlettPackard
    repo: python-redfish-utility
    action: latest_release
</pre>

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
