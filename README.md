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
Installing the base virtual env is outlined below.    
```bash
$ pip install virtualenv
$ virtualenv ENV
$ source bin/activate
```
## Virtualenvwrapper
To install `virtualenvwrapper`, we follow a similar pattern.    
### Install the package
Use pip to install the package.
```bash
$ pip install virtualenvwrapper
```
### Create a home directory for all your projects/envs
Now that we've installed `virtualenvwrapper`, let's start using it. We'll first set an environmental variable `WORKON_HOME`, and point it to our target folder `/Envs` rather than the default `~/.virtualenvs` location. 
```bash
$ export WORKON_HOME=~/Envs
$ mkdir -p $WORKON_HOME
```

### Change Shell Start up File Path
```bash
$ source /usr/local/bin/virtualenvwrapper.sh
```

### Create new environments/projects   
We can make a new environment by using `mkvirtualenv` followed by your desired environment name. 
```bash
$ mkvirtualenv env_1
$ mkvirtualenv env_2
$ mkvirtualenv env_3
```
**Useful Option:** Use `-r` to specify a file containing a list of packages you'd like installed upon construction of the environment. 

### View Available Environments    
We can view environments using `ls` with our environmental variable, or `lsvirtualenv`. 
```bash
$ ls $WORKON_HOME

# Or simply
lsvirtualenv
```

### Swap projects/environments    
Moving between environments is pleasantly simple, we can call `workon` with a desired environment name.
```bash
(env_1)$ workon env_2
```

### Remove an environment
We can remove environments with `rmvirtualenv` with the target name, but if it's an active directory we have to deactivate our instance first, which we'll do next. 
```bash
rmvirtualenv env_1
```

### Deactivate
If you wanted to remove `env_1` while you're already engaged with it, you'd first deactivate with `deactivate`. This will remove the parenthesized name on the left. 
```bash
(env_1)$ deactivate
```

### Virtualenv Directory Shortcut
To quickly hop to your virtual environment home directory, you can call `cdvirtualenv`.
```bash
(env_1)$ cdvirtualenv
```
