macos_applications
==================

Install or deinstal Appstore Applications.

>An App must not appear in both lists at the same time.

Requirements
------------

mas application. A CLI for the Appstore.

Role Variables
--------------

macos_applications_apps
macos_applications_absent

Dependencies
------------

homebrew

Example Playbook
----------------

    - hosts: myMacBook
      roles:
         - role: macos_applications
           vars:
             macos_applications_apps:
               - name: "foo bar"
                 id: 123456789
             macos_applications_absent:
               - name: "foo baz"
                 id: 0987654321

License
-------

MIT

Author Information
------------------

tinu