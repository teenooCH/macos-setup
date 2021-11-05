# Setup macOS with ansible
## Prerequisite
1. Install [Homebrew](https://brew.sh)
1. Install ansible with Homebrew:
   `` brew install ansible``
## Apply Base configuration
```
ansible-pull -U https://github.com/teenooCH/ansible.git
```
Add more packages by selecting one or more of following tags

|tag|description|
|---|-----------|
|devel|development packages|
|office|office packages|
|security|security related packages|
|v12n|virtualization|
|full|everything above|

