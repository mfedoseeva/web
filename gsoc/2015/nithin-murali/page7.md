# Build tools

26 Jun 2015

###rc_init_ws This will initialize a Robocomp workspace in the current/specified directory.


```
rc_init_ws [path]

```



###rcbuild When invoked form workspace without any arguments if not inside source path, it will build all the non-ignored components inside the workspace, if inside any component source directory it will build only that component. But if a component is specified it will build it.


```
 rcbuild [-h] [-i | --doc | --installdoc] [component]

```



The `doc` will generate documentation, `installdoc` will install the docs to install path, `install` will build and install the components. currently you can only generate docs for one component at a time.

###rccomp This dosent have much functions as of now. `rccomp list` will list all the components.

###rced when invoked as component-name file-name. it will open the the file in the component. if multiple files with same name exists, it will give choices and will ask you to choose one. It uses the editor specified in $EDITOR by default, if not present it will use `vim`.

<div class="highlighter-rouge">

```
rced [-h] component file

```



###rcrun Using rcrun you can start, stop or force stop any component from anywhere. You can also start a component in debug mode, given you have the required _config file_ in the _etc_ directory. If you have specified a config file then rcrun will use it to start the component. By default rcrun will use the `config` config file in `etc` directory, if not found it will search for `generic_config` if not found it will use any of config files present.If the debug flag is set, it will search for a config file that ends with _.debug_.


```
rcrun [-h] [-s START |-st STOP | -fst FSTOP] [-d | -cf CFILE | -c CONFIG] [-is] [component]

```


###rccd Using this you can cd into the component directory given the component name.


```
rccd component

```


* * *

Nithin Murali