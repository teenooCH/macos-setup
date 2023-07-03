# Setup macOS with ansible

## Prerequisite

1. Enable ssh on new system  
   System Preferences -> Sharing -> Remote Login
2. Copy ssh pub key to new system  
   ``ssh-copy-id user@10.11.12.13``
3. Install Developer Tools (Python3) on new system  
   ``xcode-select --install``
4. Make sure no password is needed on new system  
   Add _NOPASSWD:_ to the user or group with ``visudo``  
   > This is only necessary for the installation of homebrew 
   > and can be removed after the very first run during which
   > homebrew will be installed

## Apply Base configuration

```
ansible-playbook [-i 10.11.12.13, [-u user]] macos.yml
```
> Mind the comma ',' after the IP address.

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
