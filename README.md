************************************************************************************************************
 Temporary Update/hacked Version to avoid "Jigsaw" (and all other) error messaages crashing the server.  
 All Credit goes to original developer, all I have done here is comment out one line in his code.        
************************************************************************************************************
 I have not provided the EXEs - but you can compile them yourself by:                                    
 1) Clone this repository, saving all files to any folder on your local PC                               
 2) Download "AutoIt" development kit from here (min version 3.3.14.5):                                  
    https://www.autoitscript.com/site/autoit/downloads/                                                  
 3) Use "Compile Script to Exe .." (32 or 64 bit depending on your platform)                             
    First compile mcbeplay.au3 into mcbeplay.exe (using custom icon included in repo)                    
    Then compile bds.au3 into bds.exe (using custom icon included in repo)                               
 4) Copy the 2 new files to your server location (backup your exiting exes) and start server             

 One thing to note - my virus scanner didn't like the compiled exe's which freaked me out at             
 first, but then after some online investigation it appears AutoIt's compiled exe's can                  
 have signatures in it which can trigger a 'Generic' virus alert.                                        

 I checked the au3 files thoroughly that are included in the build and there was nothing                 
 nefarious in there, and AutoIt has been an industry standard for many years now so I trust              
 the dev kit.                                                                                            

 In the end I had to add an exception for those files in my scanner software to let me run.              

************************************************************************************************************

# MCBEPlay
Server GUI &amp; Management for Minecraft Bedrock

# MCBEPlay | Foxy's Bedrock Dedicated Server System for Windows 10
# Version: 3.5
# Made for MC Bedrock Edition 1.14+



# KNOWN ISSUES #
----------------
Bug BDS-2733
Link: https://bugs.mojang.com/browse/BDS-2733)
This bug prevents the system from copying two key world files during a backup whilst the server is running preventing regular backups.

# WHAT IS IT? #
---------------

MCBEPlay is primarly a GUI for the official BDS System, supplied by Mojang, that enables you to control and manage your Minecraft Bedrock Edition Server with little to know knowledge of server systems.
It is also a powerful tool that will automatically save, backup, restart and roll back your server when it faces issues.
The system is very flexible and can be controlled via the options.txt files.

The MCBEPlay directory can be placed in any folder on any drive of your Windows 10 device.

Required Files:
  mcbeplay.exe 		- The GUI
  bds.exe 			- Invisible process that talks directly to the bds server
  options.txt 		- File for configuring MCBEPlay

  These files MUST be kept in the same directory.

Directories (Will be auto generated when mcbeplay.exe first runs):
  tmp					- Where critical temporary files will be generated
  - This directory has to be in the same folder as the the mcbeplay.exe file above

  BDS					- Where the official BDS software will reside
  logs					- Where the log files will be generated and stored
  saves					- Where backups will be generated and stored
  - These directories do not have to be in the same folder or even on the same drive as the maind mcbeplay.exe and bds.exe files.

# HOW TO INSTALL #
------------------
	1. Unizip the mcbeplay.zip file into a folder on your PC.
	2. Download the official BDS server software from here: https://www.minecraft.net/en-us/download/server/bedrock/
	3. Unzip the official BDS server software into the BDS folder inside of your MCBEplay folder you created in step 1.
	4. Go into the BDS folder and run the bedrock_server.exe file to start the raw bedrock server.
	5. Once it is running, type "stop" into the server console, and hit return. The bedrock_server.exe window will close.
	6. Go back into your root MCBEplay folder and open up the options.txt file
	7. Set server_dir to the BDS folder where this bedrock_server.exe file is. e.g. C:\MCBEPlay\BDS
	8. Set world_dir to the worlds folder that was created inside of your BDS folder. e.g. C:\MCBEPlay\BDS\worlds
	9. Set save_dir to wherever you want your backups to be saved
	10. Set the log_dir to wherever you want your logs files to be saved
	11. Feel free to tweak the other options to your preferences later, but for now lets move on to step 12.
	12. Run mcbeplay.exe. The GUI will open up with some options. If don't click "Start" the server keepalive system will kick in and attempt to start the server after a few seconds.
	13. If you don't have keep alive turned on, hit start to start your server.
	14. If the above steps were done correctly, your server should now be up and running.
	
I would suggest at this point using the server.properties file (found in the BDS folder), to tweak the settings of your server so that it's setup how you need it.
