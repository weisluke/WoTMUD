# WoTMUD
WoTMUD triggers/aliases/scripts/timers/keys/buttons/maps

The purpose of this repository is to host a collection of files for playing the Wheel of Time Multi-User Dungeon, WoTMUD (http://www.wotmud.org/), on Mudlet, and provide an easy method of downloading and installing these files from the Mudlet command line. Please read through the following information and instructions below carefully before proceeding, and follow the steps in order, in order (hah!) to get started with a map and communications window. 

I'd like to give some thanks to the following people for their assistance/contributions/suggestions:

Jomin and Vadi, two of the Mudlet makers

Saal and Groderick, for making available their own scripts (particularly a mapper) many years ago that got me started with Mudlet, and which form the backbone of much of the material present here

Darth, for being my guinea pig and initially testing things years ago

Hope

Keim

Lea

Enoch

Draz

Pounds

Exodio


# Connecting to the game

These files are for Mudlet (https://www.mudlet.org/), a client that can be used to connect to various MUD games. Mudlet can be downloaded at https://www.mudlet.org/download/ for Windows, Linux, and macOS.

1. Open Mudlet. WoTMUD is one of the default profiles in Mudlet, so you can either (1) click on that profile and (4) connect, or (2) and (3) create a new profile with WoTMUD's information to (4) connect.
![mudlet_login_1](https://user-images.githubusercontent.com/52049495/137241355-72d43d03-b406-49ad-8623-3eb2d646b96b.png)

At this point if you are new to WoTMUD, I would recommend checking out our forums (https://forums.wotmud.info/) or game Discord server (https://forums.wotmud.info/viewtopic.php?f=74&t=7300) for more information. There is a Newbie Guide (https://forums.wotmud.info/viewtopic.php?f=76&t=12535) that should walk you through some of the basics of the game. At the very least, you need to have a character created that you can login to in order to proceed with the setup below.

I should be able to be reached by tagging @weisluke in the Discord (preferably in the "#mudclient_helpdesk" channel) if you have questions about this guide or need help.

# Downloading and installing the package handler
   
1. Click on the file "wotpack_installer.mpackage" above. It will take you to a new page.
![wotpack_installer_1](https://user-images.githubusercontent.com/52049495/137250032-2c2aef39-d8a9-47da-806a-dfdfaf5f21d9.png)

2. Click on the "Download" button. This should download the file and save it in your computer's default "Downloads" directory.
   1. Alternatively, you can right click on the "Downloads" button and "Save link as" to save it to a specific spot on your computer, e.g. the desktop.
![wotpack_installer_2](https://user-images.githubusercontent.com/52049495/137240737-23e0e19f-5c7e-49de-a497-06e431b414aa.png)

3. Login to the MUD with Mudlet and open Packages -> Package Manager from the top toolbar of icons, and click the "Install new package" button at the bottom of the window that pops up. Navigate to the location you saved the wotpack_installer.mpackage file, select it, and click open. 
![mudlet_packages_1](https://user-images.githubusercontent.com/52049495/137245638-82093947-ec96-4d65-96fb-632570e2612a.png)

4. You should see an automatic help message from the package installation on your screen. If so, you can then close the Package Manager.
   1. If not, try typing "wotpack help" into the command line and hit enter.
   2. If no help message appears, something likely went wrong. Reach out for help. 

Assuming everything worked properly, what you have just installed is a script that will handle downloading and installing other triggers/aliases/scripts/timers/keys/buttons/maps from this repository via commands sent through the Mudlet command line.

5. You will notice that your font changed after installing this package. Unless you're a male channeler who's already tainted, you will probably want to change the font to something other than Comic Sans. You can open Settings -> Main display, and from there change the font and font size. Additionally, I would recommend making sure that the box marked "Echo Lua errors to the main console" is checked. This will assist with possible debugging, both if you need help, or if you eventually start making your own aliases/triggers/scripts.
![mudlet_settings_1](https://user-images.githubusercontent.com/52049495/137246210-491b3c45-3d6f-452e-9896-fbad996c51fd.png)
6. Additionally, you can change the default command separator in Settings -> Input line. For users who are unfamiliar, this allows you to type, e.g., "smile;wave" and have the commands "smile" and "wave" sent to the MUD separately. The default command separator is ";;", although many people prefer a single semi-colon ";" instead.
![mudlet_settings_2](https://user-images.githubusercontent.com/52049495/137246430-b1498db2-4918-456c-8d11-73e31e1b2739.png)

# Installing map scripts and a map file
<details>
<summary>Click to expand.</summary>
   
1. The first step for installing these map scripts is to remove the generic mapper by going to Packages->Package Manager, clicking on the "generic_mapper", and then clicking "Remove packages". After that, you will need to restart Mudlet and login again. DO NOT SKIP THIS STEP.
![mapper_install_1](https://user-images.githubusercontent.com/52049495/137246750-164a86ff-137a-4be5-8f59-8f9a0544736c.png)

2. Make sure that you have the following settings on the MUD (by typing them into the command line):
   1. "color complete" on. The mapper scripts need the room name colors to properly work.
   2. "brief" off. The mapper will work with brief mode on, just not as well (though still pretty dang well if I do say so myself, given the limitations of picking out rooms from only name and exit combinations). 
3. Type "wotpack install mapper" into the command line and hit enter.
![mapper_install_2](https://user-images.githubusercontent.com/52049495/137254629-cf6e9d2e-8676-40c0-af78-cd6bd581a6f6.png)

4. If things are successful, you should receive some messages along the lines of "(wotpack_installer): New mapper_scripts successfully installed." A help message should pop up. A new window should appear in the top right of the screen as well, though it will say that there are no rooms in the map. This is because we need to download the map file. 
![mapper_install_3](https://user-images.githubusercontent.com/52049495/137247489-22d1b16a-27a7-40c3-9331-ebfcf809c1b1.png)

5. Type "map update". You should again receive some messages about the map file downloading and installing. This may take a moment depending on your internet speed. Once that is done, the message in the top right map window may change to say that you have a map loaded, but Mudlet doesn't know where you are.
![mapper_install_4](https://user-images.githubusercontent.com/52049495/137247712-21450f8b-c8bd-43af-aec3-742d2730d68f.png)

6. Look at your room. You should see a debugging message next to room names, room exits, and direction and look inputs. This is normal. See if the map centers on your position. If the rooms are too small, you can adjust their size at the bottom of the map window (along with the size of the room exit lines). You can also zoom in by scrolling with your mouse wheel on the map window, or (assuming everything has worked properly up to this point) by entering "map zoom 30" into the Mudlet command line.
![mapper_install_5](https://user-images.githubusercontent.com/52049495/137248267-59c8b130-2dfa-4973-959d-7253f640b772.png)

7. You can type "map debug" to turn off the debug messages. If there are problems with the mapper, these messages can be useful in narrowing down what the issue is. 
![mapper_install_6](https://user-images.githubusercontent.com/52049495/137248345-50ee7931-b074-4cb8-9db0-4c4f890f6f8a.png)

8. You can type "map dock", and the map will snap to the left or right side of the screen when you drag it there. This will make the scroll bar visible without you having to move the map window slightly, and allow you to place the map on the left hand side if you prefer.
![mapper_dock](https://user-images.githubusercontent.com/52049495/137255044-54cb16c4-3511-4d2e-b0e7-9bc88faa334a.png)
   
9. You can have the mapper manually gag room descriptions (while still using them to determine where you are) by typing "map brief". 
![mapper_install_7](https://user-images.githubusercontent.com/52049495/138769138-9061d25d-48ae-4e4d-bbd9-2e5c76c8c9a7.png)

## Changing the map appearance
<details>
<summary>Click to expand.</summary>
The appearance of the map can be further changed with some tabs in the settings window, and some aliases I've built into the map script. I won't go into the full details on those here, but I will show a couple. Feel free to reach out to me if you're interested or have questions about more. 
   
1. You can change the appearance of the room marker by going into Settings -> Mapper, and adjusting the room marker info at the bottom.
![mapper_colors_1](https://user-images.githubusercontent.com/52049495/138770304-4abb42d0-38d4-4ea9-9c7d-b25984faff26.png)

2. You can change the color of the map background, room borders, and room connections, by going to Settings -> Mapper colors.
![mapper_colors_2](https://user-images.githubusercontent.com/52049495/138771022-6db353ab-115d-468f-ae86-035639c82bce.png)

3. Rooms on the map have specific "environments" associated with them, e.g. "inside" "water" "drink" "road" "wilderness" etc. The list of environments can be found by typing "colorlegend". The colors associated with a specific environment can be altered by typing "map color environment color", e.g. "map color inside gray" "map color drink blue". Valid colors can be found by typing "viewcolors", which will open up a Mudlet wiki page.
![mapper_colors_3](https://user-images.githubusercontent.com/52049495/138771675-a4139fc1-0017-4c69-8596-39b3a625d870.png)

4. The mapper displays zone and door information for your room beneath the room exits. The colors these display with can be changed by typing "map zonecolor color" and "map doorcolor color", e.g. "map zonecolor red" and "map doorcolor green". The zone info is a clickable link which will open up the WoTMUD wiki (https://wotmud.fandom.com/wiki/WoTMUD_Wiki) page for that zone. You can choose to hide the zone info by typing "map showzone". Zone and door information is always present in the map window itself. 
![mapper_colors_4](https://user-images.githubusercontent.com/52049495/138772824-22244960-6750-4181-9ef6-7aacd5cca136.png)

</details>
   
</details>

# Installing a communications window script
<details>
<summary>Click to expand.</summary>
   
1. To get a communications window that stores says/chats/narrates/etc, type "wotpack install communications" into the command line and hit enter. Test it out by saying something to ensure that it is capturing things properly. If it looks like it installed correctly, you can type "comms debug" as well. New players can "listen all" to ensure that they have chats and narrates enabled on the MUD.
![communications_install_1](https://user-images.githubusercontent.com/52049495/138774404-6e43800e-0df9-4b52-ad9f-905998516a40.png)
   
2. You can change the color of some fields with, e.g., "comms color yells green".
![communications_install_2](https://user-images.githubusercontent.com/52049495/137254036-2623b282-ecc7-4a45-9d3d-c97d875f0bbb.png)
   
3. Much like the map window, the communications window can be docked by typing "comms dock". This will allow it to snap the left or right side of the screen, and additionally to the top of the screen as well.
![communications_install_3](https://user-images.githubusercontent.com/52049495/138775048-33f9cb9c-984b-42d0-ad52-d820d627d1bf.png)

</details>

# Installing other files

You can type "wotpack view files" to get a list of all possible files available for download. This list is NOT displayed very neatly, hopefully I can change that in the future. You can click on individual files to download and install them, although be careful - installing an individual file that requires other files to function properly may cause issues. You can use commands from the "wotpack help" help message to install particular files, groupings that contain multiple files (e.g. the mapper or comms window), or everything in this repository. Most names should be self explanatory.

As an example, and an introduction to editing my files in Mudlet (which people have found helpful as a stepping stone to creating their own material), expand the section below to see how to install and edit my targeting aliases.

## A simple set of targeting aliases
<details>
<summary>Click to expand.</summary>

Type "wotpack view files" and click on the "targeting" item in the aliases section to download and install them, or type "wotpack install targeting" to install my set of targeting aliases.
![targeting_install_1](https://user-images.githubusercontent.com/52049495/138775890-bc167ef1-b05a-49c7-9b59-499fc3d24ccb.png)
![targeting_install_2](https://user-images.githubusercontent.com/52049495/138775903-1b9fd3a9-488f-4f02-b9bf-df8cde8fe27a.png)
Type "tgt xxx" to set a target. Some specific targets give messages colored by their race on the MUD.
   
"p" is my default alias to "kill target". This can be easily changed. Open up Aliases in Mudlet from the top toolbar, and navigate to the targeting aliases. Expand any subfolders and find the alias to "Attack target". You will see a box named "Pattern:" with "^p$" inside of it. This is a regex pattern that Mudlet matches to either a) send a replacement command to the MUD (as specified in the "Command:" box underneath), or b) execute a sequence of Lua code as specified in the large white space underneath. Regex and Lua are outside the scope of anything I want to cover here currently, but to change the key that you use to "kill target" simply change the "p" to a different letter in the "Pattern:" box. Do NOT, however, get rid of the ^ or $ symbol. Keep them, as they are necessary for Mudlet to match things properly - just change the letter in between to the letter(s) that you would prefer to use.
![targeting_install_3](https://user-images.githubusercontent.com/52049495/138776848-b9761c82-7010-4051-81ec-d0bf204ccfc6.png) 
   
</details>

Two sets of scripts that you might also consider installing are a daily reminder to vote for the WoTMUD at http://www.topmudsites.com/vote-wotmud.html, and a query for the player numbers from https://writtenrealms.com/wot/playground/who/daily that adds the numbers to the "who" list in the game. The writtenrealms site also has other resources for the MUD, such as combat skill chance calculators. Further details can be found on the game's help forum.

# Other Mudlet information
<details>
<summary>Click to expand.</summary>
   
Mudlet stores your profile information at (on Windows at least) C:/users/USERNAME/.config/mudlet/profiles/PROFILENAME

E.g., for me, C:/users/lukew/.config/mudlet/profiles/WoTMUD

Inside this folder, there are two subfolders that may be of interest.
![mudlet_profile](https://user-images.githubusercontent.com/52049495/137252774-496ed920-6d9a-42d2-867c-4c550f4ef682.png)

One is named "current", and inside you will find .xml files with filenames corresponding to various dates and times. These files are copies of your profile. It is sometimes useful to back them up on a regular basis, just in case something ever goes wrong with your profile. You can also use those files to easily transfer your profile from one machine to another (copy the file on one machine or upload it to a cloud based service, and then save it in the same location on the new machine, making sure that it is the only file in that folder).
The other folder, "log", contains the log files of the MUD output, if you have enabled logging. You can check whether logging is enabled by either paying attention to the initial lines of Mudlet output when you log in, which tells where the file is being saved (if logging is enabled), or checking that the logging button in the bottom right corner of Mudlet is enabled.
![mudlet_logging](https://user-images.githubusercontent.com/52049495/137253004-3b51b1e3-ee44-47dd-b3df-36367045b189.png)
   
</details>
