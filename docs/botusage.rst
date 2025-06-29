****************
Bot Usage
****************

The YaPB User Menu (yb menu)
================================

Main Menu
-----------------

Pressing the "=" key in game a menu with the following options should appear on your screen

.. figure:: images/main_menu.png
    :align: center

    This is the YaPB user menu
    
1. **Control Bots** - A menu that adds or removes bots from the game.
2. **Features** - A menu that configures the type of weapons used by bots, opens the graph editor menu, toggles debug mode and controls bots commands.
3. **Fill Server** - A menu that fills the server with bots with the specified parameters.
4. **End Round** - Kills all bots for the end of round.

Bots Control Menu
---------------------

.. figure:: images/bots_control_menu.png
    :align: center

    Bots Control Menu
    
1. **Quick add bot** - This does what it says. It quickly adds a Bot giving him a random name, team, difficulty and model. Difficulty will be chosen randomly between your yb_difficulty_min/yb_difficulty_max values specified in yapb.cfg.
2. **Add specific bot** - Allows you specify all things (except name) for adding a single Bot.

.. figure:: images/bots_difficulty_level.png
    :align: center

    This lets You choose a difficulty for the specific Bot.
    
.. figure:: images/bots_personality_menu.png
    :align: center

    This lets You choose a personality for the specific Bot.

.. figure:: images/select_team_menu.png
    :align: center

    This lets You choose a team for the specific Bot.

.. figure:: images/ct_class_select.png
    :align: center

    This lets You choose a class for the specific Bot. (for CT Team)

.. figure:: images/t_class_select.png
    :align: center

    This lets You choose a class for the specific Bot. (for T Team)
    
3. **Remove random bot** - removes a random bot.
4. **Remove all bots** - removes all bots from the server.
5. **Bot removal menu** - A menu that allows you to remove a bot from the server specified in the list.


Bots Features Menu
-----------------------

.. figure:: images/bots_features_menu.png
    :align: center

    Bots Features Menu
    
1. **Weapon mode menu** - A menu that configures the type of weapons used by bots.

.. figure:: images/bots_weapon_mode.png
    :align: center

    Bots Weapon Mode Menu

2. **Graph editor** - Opens the graph editor.
3. **Select personality** - Adds a bot with the currently set difficulty with personality setting.
4. **Toggle debug mode** - Enables or disables debug mode.
5. **Command menu** - Opens the bot command menu.

.. figure:: images/bot_commandmenu.png
    :align: center

    Bot Command Menu
    
1. **Make double jump** - Forces the nearest teammate bot to crouch next to you to make double jump.
2. **Finish double jump** - Releases the bot after the first command, it must get up and go about his business.
3. **Drop the C4 bomb** - Forces the bot carrying the bomb to drop it at you.
4. **Drop the weapon** - Makes the teammate bot throw a weapon at you.

.. Note:: Bot will only throw a weapon at you when it have a primary weapon and 2000 or more dollars in the account.

Graph Editor
------------------

.. figure:: images/graph_editor_page1.png
    :align: center

    Graph Editor Menu (Page 1)
    
1. **Show/Hide nodes** - Show or hide the display of nodes.
2. **Cache node** - Cache node for future use.
3. **Create path** - Opens the menu for creating path connections.
4. **Delete path** - Removes the path from selected node.
5. **Add node** - Opens the menu for selecting the type for adding node.
6. **Delete node** - Removes the node you are standing on.
7. **Set autopath distance** - Opens the autopath distance setting menu.
8. **Set radius** - Opens the node radius setting menu.
9. **Next...** - Goes to the second page of the graph editor menu.

.. figure:: images/graph_editor_page2.png
    :align: center

    Graph Editor Menu (Page 2)

1. **Debug goal** - Opens a menu for debugging bot walkability to a specified node.
2. **Auto node placement on/off** - Enables or disables automatic node placement.
3. **Set flags** - Opens the menu for selecting flags for a node.
4. **Save graph** - Saves nodes into graph file with path integrity check.
5. **Save without checking** - Saves nodes without checking (because of this, there may be problems with the behavior of bots).
6. **Load graph** - Loads nodes from a graph file.
7. **Check graph** - Checks nodes for errors.
8. **Noclip cheat on/off** - Enables or disables noclip cheat.
9. **Previous...** - Goes to the first page of the graph editor menu.


YaPB console commands Summary
==================================

The following main YaPB commands are available:
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb add``                | Adds specific bot into the game. (see below)                                                                                   |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb kick``               | Kicks off the random or specified bot from the game. (see below)                                                               |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb removebots``         | Kicks all the bots from the game. Also available via alias ``yb kickall``. (see below)                                         |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb kill``               | Kills the specified team or all the bots. (see below)                                                                          |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb fill``               | Fills the server (add bots) with specified parameters. (see below)                                                             |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb vote``               | Forces all the bots to vote to specified map.                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb weapons``            | Sets the bots weapon mode to use. (see below)                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb menu``               | Opens the main bot menu.                                                                                                       |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb version``            | Displays version information about bot build.                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb list``               | Lists the bots currently playing on server.                                                                                    |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb cvars``              | Displays all the cvars with their descriptions. (see below)                                                                    |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb graph``              | Handles graph operations.                                                                                                      |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb show_custom``        | Shows the current values from custom.cfg                                                                                       |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb exec``               | Executes a client command on bot entity.                                                                                       |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+

To get help for all commands such as arguments, aliases, etc, type in the console ``yb help``.

If you want to get help for specified command for example ``yb add``, type in the console ``yb help add``.


yb add
---------------

To add a specific bot to the game, with nickname: John Smith, Difficulty: Average, Personality: Careful, Team: Counter-Terrorists, Team Class: SAS, you should type in console ``yb add 1 2 2 3 "John Smith"``

yb add arguments info:
~~~~~~~~~~~~~~~~~~~~~~~~~

**Difficulties**

* ``0`` - Newbie
* ``1`` - Average
* ``2`` - Normal
* ``3`` - Professional
* ``4`` - Godlike

**Personalities**

* ``0`` - Normal
* ``1`` - Aggressive (rusher)
* ``2`` - Careful

**Teams**

* ``0`` - Random
* ``1`` - Terrorists
* ``2`` - Counter-Terrorists

**Team classes**

Terrorists:

* ``0`` - Random
* ``1`` - Phoenix Connexion
* ``2`` - Elite Crew
* ``3`` - Arctic Avengers
* ``4`` - Guerilla Warfare
* ``5`` - Midwest Militia **(Condition Zero only!)**

Counter-Terrorists:

* ``0`` - Random
* ``1`` - Seal Team 6
* ``2`` - GSG-9
* ``3`` - SAS
* ``4`` - GIGN
* ``5`` - Spetsnaz **(Condition Zero only!)**

Correct format for the ``yb add`` command is ``yb add [difficulty] [personality] [team] [model] [name]``. All bot values ​​are selected by numbers (except the bot name).

yb kick
---------------

Type in console ``yb kick`` command to remove the random bot.

If you want to remove the bot from the specified team, you should type in the console ``yb kick t`` to kick a bot from Terrorists team, and ``yb kick ct`` to kick a bot from Counter-Terrorists team.

yb removebots
---------------

You can also use the alias ``yb kickall`` to remove all bots.

If you want to remove bots instantly, add the ``instant`` argument to this command.

Example: ``yb kickall instant``

yb kill
---------------

The ``yb kill`` command kills all the bots. To kill a specific team, such as terrorists you should type in console ``yb kill t`` command. For Counter-Terrorists the command are ``yb kill ct``

The ``silent`` argument disables the ``All bots died...`` message in the console. You should enter the ``yb kill silent`` in console, to kill bots without that message.

yb fill
---------------

To fill the server with random bots type in console ``yb fill 0``.

If you want to fill the server with specific bots, for example: Team: Terrorists, Count: 5, Difficulty: Normal, Personality: Aggressive, you should type in console the follow command ``yb fill 1 5 2 1``.

yb fill arguments info:
~~~~~~~~~~~~~~~~~~~~~~~~~

**Teams**

* ``0`` - Both teams
* ``1`` - Terrorists only
* ``2`` - Counter-Terrorists only

**Difficulties**

* ``0`` - Newbie
* ``1`` - Average
* ``2`` - Normal
* ``3`` - Professional
* ``4`` - Godlike

**Personalities**

* ``0`` - Normal
* ``1`` - Aggressive (rusher)
* ``2`` - Careful

Don't enter the bot personality value if you want bots with random personalities.

Correct format for the ``yb fill`` command is ``yb fill [team] [count] [difficulty] [personality]``.

yb weapons
---------------

To force the bot to use only a certain type of weapon, for example, shotguns, you should type in console the ``yb weapons shotgun`` command.

Allowed values: ``knife|pistol|shotgun|smg|rifle|sniper|standard``.

Standard means that bots will use all weapons.

yb cvars
---------------

This command lists all cvars with their descriptions.

If you want to save all cvars you configured to config, add the ``save`` argument to this command.

You can also save a map-specific config by using the ``save_map`` argument to save the current values of all cvars to ``addons/yapb/conf/maps/map_name.cfg``.

Example: ``yb cvars save``

Also you can narrow your search by entering a word as an argument, instead of looking through a list of all cvars.

To restore the default values of all bot cvars, type ``yb cvars defaults`` in console.

yb exec
---------------

This command allows you to execute a command from a bot entity.

Valid usage is: ``yb exec [user_id] [command]``.

Where ``[user_id]`` is bot's ID, which you can find by entering the ``yb list`` command in the console.

Adding bots to the game
============================

Select ``1. Quick add bot`` from the bot control menu to add a bot with random stats (name, difficulty, personality etc.)
Select ``2. Add specific bot`` from the bot control menu to add a bot with manually specified stats.

Or type in console ``yb_quota x`` where X is amount of adding bots.


Selecting the bot language
=============================

You must open the file ``yapb.cfg`` in the folder ``addons/yapb/conf`` and change the value of yb_language cvar to the next available one.

#. ``en`` - English Language
#. ``ru`` - Russian Language
#. ``de`` - Deutsch Language

For example, write in the config ``yb_language ru`` for Russian Language.

Bot management on a dedicated server
=======================================
To have access to the bot's menus and commands, you need to in a server console specify a password and a key from which the password will be read.

To specify a password, you must enter in the console the following cvar ``yb_password botpassword`` where ``botpassword`` is the password you specified.
To specify a key, you must enter in the console the following cvar ``yb_password_key _ybpw``, where ``_ybpw`` is the key you specified.

Then, in a client console you must enter the following commandline in the console ``setinfo _ybpw botpassword`` to have access to the commands and menus of the bot.
To have access to graph commands, you need to enter in the console the following command ``yb g acquire_editor``. Make sure that no one has entered this command before you, who has the password from the bot. Otherwise, you won't be able to access graph commands until that player removes graph editing rights.

To revoke the rights to edit graphs, you must enter in the console the following command: ``yb g release_editor``.
