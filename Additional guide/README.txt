                   .:                     :,                                          
,:::::::: ::`      :::                   :::                                          
,:::::::: ::`      :::                   :::                                          
.,,:::,,, ::`.:,   ... .. .:,     .:. ..`... ..`   ..   .:,    .. ::  .::,     .:,`   
   ,::    :::::::  ::, :::::::  `:::::::.,:: :::  ::: .::::::  ::::: ::::::  .::::::  
   ,::    :::::::: ::, :::::::: ::::::::.,:: :::  ::: :::,:::, ::::: ::::::, :::::::: 
   ,::    :::  ::: ::, :::  :::`::.  :::.,::  ::,`::`:::   ::: :::  `::,`   :::   ::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  :::::: ::::::::: ::`   :::::: ::::::::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  .::::: ::::::::: ::`    ::::::::::::::: 
   ,::    ::.  ::: ::, ::`  ::: ::: `:::.,::   ::::  :::`  ,,, ::`  .::  :::.::.  ,,, 
   ,::    ::.  ::: ::, ::`  ::: ::::::::.,::   ::::   :::::::` ::`   ::::::: :::::::. 
   ,::    ::.  ::: ::, ::`  :::  :::::::`,::    ::.    :::::`  ::`   ::::::   :::::.  
                                ::,  ,::                               ``             
                                ::::::::                                              
                                 ::::::                                               
                                  `,,`


http://www.thingiverse.com/thing:2975949
The complete BLTouch/3DTouch guide for Creality printers (CR-10/s,Ender 2,Ender 3) for Auto Bed Leveling UPDATED by dannyw281 is licensed under the Creative Commons - Attribution - Non-Commercial - No Derivatives license.
http://creativecommons.org/licenses/by-nc-nd/3.0/

# Summary

**28-06-2018 - People are having issues trying to obtain the Pin 27 adapter board, there is another way around this which is a little more complicated but doesn't require the board here http://jonathanlundstrom.me/2017/10/23/cr-10-bltouch-firmware/**

**26-06-2018 - Added version 3 to add suggested changes to CR-10/Ender 3 section to make things more clear, use this version instead of v1 or v2!**

**25-06-2018 - Added a version 2 of the guide due to issues in v1, this addresses most of the issues below with more photos and screenshots to look at for installation, you should definitely use this instead of v1!**

I've tried to make this guide as simple as possible with all the resources you need in one place or linked to it, sections include;

**Before you start**
	
**Printers**	
CR-10s /S4/S5/Mini	
Ender 2	
Ender 3/CR-10	

**Configuring Z offset**	

**Start-up GCODE**
CR-10/s
Ender 2	
Ender 3
	
**Misc & Extras**	
Remove all boot screens for faster boot times	
Control ooze while bed levelling runs (Simplify3D)
CR-10 stock to CR-10s board

**This guide was created with the firmware included in the guide, please use the hyperlink in the guide to download this firmware to make sure all instructions match and make sense.**

***For CR-10 and Ender 3 please use pin 27 not 29 like it says in the guide, sorry this was over looked when creating! So please be sure to use #define* servo0_pin 27.**

I hope this helps and this is clear enough to follow, if not leave a comment here or contact me directly through my Ender 3 group here, **https://www.facebook.com/groups/Ender3dp/**.
Feel free to also join my brand new Ender 5 group - **https://www.facebook.com/groups/ender5/**

I decided to add what I've dubbed the 'Dice of Decisions' for a little bit of fun for them times when you just cant think of what to print.

This guide uses TH3D Firmware, Thank you guys over at TH3D for the awesome firmware to work it!

**To avoid any confusion, if you're using the V2.1 CR-10s board follow the same pin out for the sensor as shown in the v2.0 wiring diagram.**

**I would really appreciate it if you could tip me a couple of dollars for this guide but if not don't worry about it :) thank you to the people who have so far, you're the best!**

Looking to buy an Creality product for yourself? Purchase one from Creality's brand new factory direct store with their new improved support and after care system in place to help you with any issues you may encounter after buying and using your printer.
**https://www.creality3donline.com/?ShareCode=422ZKRK2**

# Where did you buy the parts?

**Sensors -**

3Dtouch (What I used with this guide) - https://www.aliexpress.com/item/32840691571/32840691571.html?productId=32840691571&aff_platform=default&cpt=1529931025359&sk=IjDpQ1T&aff_trace_key=ce19ae1143c94d87b33a5e63a50c2bb4-1529931025359-04766-IjDpQ1T&terminal_id=5a3da06b42084cc2972a42de867a309a

**or**

Genuine BLTouch - 
https://www.ebay.co.uk/itm/BL-Touch-Auto-level-Sensor-GENUINE-Geeetech-Delta-Anet-A8-3d-printer-parts-/322573193669

**For Boot Loader -**

Genuine Arduino Uno  - https://www.aliexpress.com/item/32838136070/32838136070.html?productId=32838136070&aff_platform=default&cpt=1529931599125&sk=ce8RdGy1&aff_trace_key=dbd5aeeb78ca44d58cf6825b736dc335-1529931599125-03168-ce8RdGy1&terminal_id=5a3da06b42084cc2972a42de867a309a

**or**

Clone Arduino Uno - 
https://www.aliexpress.com/item/high-quality-One-set-UNO-R3-CH340G-MEGA328P-for-Arduino-UNO-R3-NO-USB-CABLE/32697443734.html?productId=32697443734&aff_platform=default&cpt=1529931636115&sk=cs4SHwSV&aff_trace_key=2566048d28c54a04abb50521b57aa538-1529931636115-05610-cs4SHwSV&terminal_id=5a3da06b42084cc2972a42de867a309a
**or**
USBISP - https://www.aliexpress.com/item/Free-Shipping-2PCS-USBASP-10PIN-TO-6PIN-ADAPTER-New-USBASP-USBISP-AVR-Programmer-USB-ATMEGA8-ATMEGA128/1807010158.html?productId=1807010158&aff_platform=default&cpt=1529931842888&sk=IRD8Jat&aff_trace_key=c3b53b6e0ed54c08a845a93eca4d1991-1529931842888-06650-IRD8Jat&terminal_id=5a3da06b42084cc2972a42de867a309a
**Either of these will work fine**

**Jumper cables for arduino -

I recommend getting the Multi-set of jumpers they do as you will need 5x female to male and 1x male to female.** https://www.aliexpress.com/item/Free-Shipping-Dupont-line-120pcs-lot-30cm-male-to-male-male-to-female-and-female-to/32656693879.html?productId=32656693879&aff_platform=default&cpt=1529931865598&sk=cIbx8XVR&aff_trace_key=f654f142d1864c8596124046167b23f2-1529931865598-08632-cIbx8XVR&terminal_id=5a3da06b42084cc2972a42de867a309a

These are AliExpress affiliate links I have added above so if you buy something from the links I will get a little bit back from this, Thank you if you chose to I appreciate it :)