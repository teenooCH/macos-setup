macos_applications
==================

Install Appstore Applications.

Requirements
------------

mas application. A CLI for the Appstore.

Role Variables
--------------

macos_applications_apps

Dependencies
------------

homebrew

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: myMacBook
      roles:
         - role: macos_applications
           vars:
             macos_applications_apps:
               - name: "foo bar"
                 id: 123456789

License
-------

MIT

Author Information
------------------

tinu