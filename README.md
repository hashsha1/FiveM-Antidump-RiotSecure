# RiotSecure
RiotSecure is a Antidump and Config hide resource:

- Hide complete Clientfiles and scripts from user if user dump your server.
- Secures your Config files that contains farming coordinates etc.

## Requirements
* Server
   - esx



## Installation
- Paste the directory into your resource folder.
- Add this in your `server.cfg`:

```
start riotsecure
```
(Or your directory name)

## Adding Scripts to RiotSecure
* Commands:
- riotsecure [SOURCENAME] --WITHOUT []

* Resource Preperation:
- To avoid script failures:
! make sure that your client file in resourcefolder is named to "client.lua" and your config file (if you want to have this also secured) is named to "config.lua".
! make sure in your _resource or fxmanifest of your resource above files are also named to "client.lua" and "config.lua".
! DO NOT USE SUBDIRECTORYS !
! If you wont to include your config file to the secured script then simply rename or temp delete it from resource dictonary and do the 
changes backward after completing the securing command. RiotSecure will include this file by default if its in the resource dictonary.

- If you secured the config you can simply delete it from client scripts in your manifes or _resource file.

- If everything is prepared start/restart your server and use the command "riotsecure [resourcename]" 
RiotSecure will Proceed and replace the client file.
- Done.

Q/A:
- I have secured a script and want to edit the script/config after securing:
RiotSecure will create backup files to your resource path, if you want to do changes to your script, delete the encrypted client.lua (RiotSecure loader file)
and  delete "_original" from client_original.lua and config_original.lua filename. 
Now you have restored your original Scripts, make changes to it and after that just type command "riotsecure [resourcename]" to your console to secure it again.
done.

-I get locales error after securing:
open locales file of your choice, copy its content.
open unsecured client.lua of your script and paste the content on the top of the script.
done. 


# Legal
Copyright (C) 2015-2022 Integer

