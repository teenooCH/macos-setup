git_repositories
================

Install all configured git repositories.

Requirements
------------

Git.

Role Variables
--------------

git_repositories
- repository: git, SSH, or HTTP(S) protocol address of the git repository.
- destination: The path of where the repository should be checked out.
- depth: Default = 1. If set to 0 the complete repo is cloned.
- update: Default = true.
- version: Default = "HEAD".
- remote: Default = "origin".
- ssh_options: Options git will pass to ssh when used as protocol.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: myMacBook
      roles:
        - role: git_repositories
          vars:
            git_repositories:
              - repository: "https://github.com/foo/bar.git"
                destination: "~/.foobar"
              - repository: "https://github.com/foo/baz.git"
                destination: "/vol1/foobaz"
                update: false
                version: "master"

License
-------

MIT

Author Information
------------------

Tinu
