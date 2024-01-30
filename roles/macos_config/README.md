macos_config
============

Configure a macOs system.
- templates
- files

Requirements
------------

None.

Role Variables
--------------

    - macos_config_templates
      - source:  
        Local path to a file to copy to the remote server.

      - destination:  
        Remote absolute path where the file should be copied to.

      - backup:  
        Default = false.

      - mode:  
        Default = 0640.

    - macos_config_files
      - source:  
        Local path to a file to copy to the remote server.

      - destination:  
        Remote absolute path where the file should be copied to.

      - backup:  
        Default = false.

      - mode:  
        Default = 0640.

Dependencies
------------

None.

Example Playbook
----------------

Make sure the variables used in the templates are set.

    - hosts: servers
      roles:
        - role: macos_config
          vars:
            macos_config_templates:
              - source: "zshrc.j2"
                destination: "~/.zshrc"
                backup: true
              - source: "gitignore.j2"
                destination: "~/.gitignore"
              - source: "vimrc.j2"
                destination: "~/.vimrc"
            macos_config_files:
              - source: "files/p10k.zsh"
                destination: "~/.p10k.zsh"
                backup: true

License
-------

MIT

Author Information
------------------

Tinu
