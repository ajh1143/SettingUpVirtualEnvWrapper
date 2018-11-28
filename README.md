# SettingUpVirtualEnvWrapper
Cataloging the process for later reference

# Why use virtualenvwrapper?     
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
```
$ pip install virtualenv
$ virtualenv ENV
$ source bin/activate
```
## Virtualenvwrapper

### Install the package
```
$ pip install virtualenvwrapper
```
### Create a home directory for all your projects/envs
```
$ export ENVS_HOME=~/Envs
$ mkdir -p $ENVS_HOME
```

### Change Shell Start up File Path
```
$ source /usr/local/bin/virtualenvwrapper.sh
```

### Create new environments/projects    
```
$ mkvirtualenv env_1
$ mkvirtualenv env_2
$ mkvirtualenv env_3
```

### View Available Environments    
```
$ ls $ENVS_HOME
```

### Swap projects/environments    
```
(env_1)$ workon env_2
```
