# WoTMUD
WoTMUD triggers/aliases/scripts/timers/keys/buttons/maps

The purpose of this repository is to host a collection of files for playing the WoTMUD on Mudlet, and provide an easy method of downloading and installing these files from the mudlet command line. Please read carefully and follow the steps below in order to get started with a map and communications window.

![wotpack_installer_1](https://user-images.githubusercontent.com/52049495/137240395-f9a6ca92-70fe-49f9-a185-227afe748527.png)

1. Download and save "wotpack_installer.mpackage" somewhere easy to find on your computer.
2. Open Mudlet, open Package Manager (from the top toolbar of icons), and click install.
3. Navigate to the location you saved the .mpackage file, select it, and click open. It should now show up in the list of packages. Click ok.
4. You should see an automatic help message from the package installation on your screen.
   1. If not, try typing "wotpack help" into the command line and hit enter.
   2. If no help message appears, something likely went wrong.

Assuming everything worked properly, what you have just installed is a script that will handle downloading and installing other triggers/aliases/scripts/timers/keys/buttons/maps from this repository via commands sent through the Mudlet command line.

5. To get a map, you will want to uninstall the generic mapper in Package Manager (if it is in there), then reopen Mudlet.
6. Make sure that you have following settings on the MUD:
   1. "color complete" on. The mapper scripts need the room name colors to properly work.
   2. "brief" off. The mapper will work with brief mode on, just not as well (though still pretty dang well if I do say so myself, given the limitations of picking out rooms from only name and exit combinations). In a few steps, after installing the mapper, you can instead type "map brief" to have the mapper scripts manually gag the room descriptions so they don't show up on the screen, while still using them to determine your position.
7. Type "wotpack install mapper" into the command line and hit enter.
   1. If things are successful, you should receive some messages along the lines of "(wotpack_installer): New mapper_scripts successfully installed."
8. When that completes, type "map update". You should again receive some messages about the map file downloading and installing. This may take a moment depending on your internet speed. Once that is done,
   1. Look at your room, and see if the map centers on your position. Then try moving around.
   2. You may see debugging messages next to room names, room exits, and direction inputs. You can type "map debug" to turn them off. If there are problems with the mapper, these messages can be useful in narrowing down what the issue is. 

9. To get a communications window that stores says/chats/nars/etc, type "wotpack install communications". 
   1. If it looks like it installs correctly, you can type "comms debug" as well

12. You can type "wotpack view files" to get a list of all possible files available for download. This list is NOT displayed very neatly, hopefully I can change that in the future. You can use commands from the help message to install particular pieces, or everything. Most names should be self explanatory.


13. Please check the forums (https://forums.wotmud.info/) or the game discord (https://forums.wotmud.info/viewtopic.php?f=74&t=7300) for more assistance if need be. I should be able to be reached by tagging @weisluke in the discord (preferably in the "mudclient_helpdesk" channel)
