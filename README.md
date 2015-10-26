ansible-dwarffortress
========================

Dwarf Fortress provisioned via ansible. Tested using the ansible/ubuntu14.04-ansible docker container

Usage
-----

Within the directory of this project:

    ansible-playbook df_40_20.yml --connection=local

This installs the dependencies for dwarf fortress, and dwarf fortress itself.

If you want to run in text mode

    ansible-playbook textmode.yml --connection=local

This modifies the init.txt configuration file to set PRINT_MODE to TEXT.

### DfHack ###

    ansible-playbook dfhack.yml --connection=local

### Tile sets ###

Coming soon.

### noVNC ###

For whatever reason (running in a docker container?) you might not want to control Dwarf Fortress on the host directly, but instead access from another machine. This is why you can provision noVNC so that DF can be accessed from another computer via the browser.

    ansible-playbook novnc.yml --connection=local

You can point your browser to http://localhost:6080/vnc.html and click connect (there is no password). Remember when running DF to set the DISPLAY:

    DISPLAY=:1 /df_linux/df

Depandancies
------------

Tested with ansible 1.8.2.

Todo
----

* Add the Phoebus tile set.
* Then some more tile sets.
* Create a tutorial version, which adds a saved game that can be used to follow an online tutorial.
* Allow for more stuff to be configured, for example which DISPLAY to use when using noVNC.

Credits
-------

* Obviously Toady One at http://www.bay12games.com for Dwarf Fortress.
* All the guys that maintain the Dwarf Fortress wiki (http://dwarffortresswiki.org/index.php/DF2012:Installation)
* Chris Collins who's project inspired me to use noVNC (https://github.com/DockerDemos/DwarfFortressServer) and what I used to get started.
