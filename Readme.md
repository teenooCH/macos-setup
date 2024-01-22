# Setup macOS with ansible

## Prerequisite

1. Enable ssh on the remote system  
   System Preferences -> Sharing -> Remote Login  
   or  
   ```sudo systemsetup -setremote on```
2. Copy ssh pub key to the remote system  
   ``ssh-copy-id user@10.11.12.13``
3. Install Developer Tools (Python3) on the remote system  
   ``xcode-select --install``

## Apply Base configuration

```
ansible-playbook [-i 10.11.12.13, [-u user]] macos.yml [--ask-become-pass]
```
> Mind the comma ',' after the IP address.

> The ``--ak-become-pass`` is only necessary for the installation 
> of homebrew at the very first run.

Add more packages by selecting one or more of following tags

| tag        | description               |
|------------|---------------------------|
| devel      | development packages      |
| mas        | Mac App Store packages    |
| navigation | navigation packages       |
| office     | office packages           |
| security   | security related packages |
| v12n       | virtualization            |
| full       | everything above          |

## Caveats

- In UTM VMs the terminal App _Kitty_ does not work. It needs OpenGL, which is not available in UTM.  
  Use ``terminal`` instead and set the font to _MesloLGM Nerd Font Mono_ in the profiles.
- For the Mac App Store (mas) an Apple-ID is needed. You must be logged in to be able to install Apps.
