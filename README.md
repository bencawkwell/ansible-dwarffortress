ansible-dwarffortress
========================

Dwarf Fortress provisioned via ansible. Tested using the ansible/ubuntu14.04-ansible docker container

Usage
-----

Within the directory of this project:

    ansible-playbook df_40_20.yml --connection=local

This installs the dependancies for dwarf fortress, and dwarf fortress itself.

If you want to run in text mode

    ansible-playbook textmode.yml --connection=local

This modifies the init.txt configuration file to set PRINT_MODE to TEXT.

### DfHack ###

    ansible-playbook dfhack.yml --connection=local

### Tile sets ###

Coming soon.

Depandancies
------------

Tested with ansible 1.8.2.

Todo
----

* Add the Phoebus tile set.
* Add noVnc.
* Add some more tile sets.
* Create a tutorial version, which adds a saved game that can be used to follow an online tutorial.

Credits
-------

* Obviously Toady One at http://www.bay12games.com for Dwarf Fortress.
* All the guys that maintain the Dwarf Fortress wiki (http://dwarffortresswiki.org/index.php/DF2012:Installation)
