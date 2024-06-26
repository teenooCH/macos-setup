Homebrew
========

Install Homebrew and update the repository.  
If configured install/remove taps, fonts, formulae and casks.

The installation of Homebrew is done with the official install script from Homebrew.

Requirements
------------

None.

Role Variables
--------------

    - homebrew_update_packages  
      Update all repositories. Default is true.

    - homebrew_upgrade_packages  
      Upgrade all installed packages. Default is false.

    - homebrew_taps
      List of all taps to be installed/removed.

    - homebrew_fonts
      List of all fonts to be installed/removed.

    - homebrew_packages
      List of all packages to be installed/removed.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: myMacBook
      roles:
        - role: homebrew
          vars:
            homebrew_upgrade_packages: true
            homebrew_taps:
              - homebrew/cask-fonts
            homebrew_fonts:
              - font-meslo-lg-nerd-font
            homebrew_packages:
              - bat
              - name: coreutils
                state: absent
              - htop

License
-------

MIT

Author Information
------------------

Tinu
