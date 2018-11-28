# SettingUpVirtualEnvWrapper
Cataloging the process for later reference

# Why use virtualenvwrapper?     
<img src="https://github.com/ajh1143/ajh1143.github.io/blob/master/Images/venv/venv-2.jpeg" class="inline"/><br> 
Easy organization of multiple virtual environments and simple streamlined commands.   

### Key Features     
* Places all of your virtual environments in a single directory.
* Wrappers for creating/copying/removing environments.
* Single command to switch between environments.
* Tab completion. 
* User-defined operation hooks.
* Plugin system for generating extensions.

## Installation Process    
### Basic virtualenv    
```bash
$ pip install virtualenv
$ virtualenv ENV
$ source bin/activate
```
## Virtualenvwrapper

### Install the package
```bash
$ pip install virtualenvwrapper
```
### Create a home directory for all your projects/envs
```bash
$ export WORKON_HOME=~/Envs
$ mkdir -p $WORKON_HOME
```

### Change Shell Start up File Path
```bash
$ source /usr/local/bin/virtualenvwrapper.sh
```

### Create new environments/projects    
```bash
$ mkvirtualenv env_1
$ mkvirtualenv env_2
$ mkvirtualenv env_3
```
**Useful Option**: Use -r to specify a file containing a list of packages you'd like installed upon construction of the environment.

### View Available Environments    
```bash
$ ls $WORKON_HOME

#or simply

$ lsvirtualenv
```

### Swap projects/environments    
```bash
(env_1)$ workon env_2
```

### Remove an environment
```bash
rmvirtualenv env_1
```

### Deactivate
```bash
(env_1)$ deactivate
```

### Virtualenv Directory Shortcut
```bash
(env_1)$ cdvirtualenv
```
