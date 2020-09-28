--- 
layout: post
title: Getting CHDK working on the Canon S5 IS from Mac OS X
created: 1208740413
categories: 
- canon
- Canon PowerShot
- Canon S5 IS
- CHDK
- digital camera
- firmware
- RAW
- Mac
- Open Source
---
<p>First, what the heck is <a href="http://chdk.wikia.com/">CHDK</a>??! Basically, it's a "firmware enhancement" for a whole list of Canon PowerShot cameras (supported <a href="http://chdk.wikia.com/wiki/FAQ#Q._What_camera_models_are_supported_by_the_CHDK_program.3F">camera model list here</a>). You follow a process where you copy some files onto your memory card, and instead of your camera booting the "regular" operating system, it boots from the memory card instead.</p>

<p>OK, so what does all THAT mean? Basically, today's digital cameras have operating systems -- software -- that runs many of their features. In fact, software is some times one of the main difference between "lower end" cameras and the higher end Digital SLRs. By loading this software onto your camera, you get access to a whole host of other features. The <a href="http://chdk.wikia.com/wiki/CHDK_in_Brief#A_sampling_of_those_additional_features.2Ffunctionality.">CHDK in Brief page has a list of those additional features</a> -- the three of most interest to be so far are 1) enabling RAW mode, 2) exposure times as long as 65 seconds and 3)
exposure times as little as 1/10,000 of a second. There are all sorts of other scripts that can actual be loaded and run on the camera as well. I'm interested in checking out the intervalometer aka timelapse scripts.</p>

<p>So, I spent perhaps 3 hours on Friday, cursing and swearing after the first 30 minutes, swapping my SD card between my computer and my camera, trying to get this stuff working. Looks like most people that are messing with this are on Windows or Linux, and getting this working on the Mac presents some special challenges.</p>

<p>Here are the steps (and yak shaving) that I had to do to get CHDK running on my Canon S5 IS. This assumes that you won't run screaming from using the Terminal, and are at least going to be OK cut and pasting commands in.</p>
<!--break-->

<p><strong>WORK IN PROGRESS for 4GB+ cards</strong> -- theoretically creating two partitions will mean that the CHDK software sees the second FAT32 partition with the majority of space, but Id didn't get this working. I bought a second 2GB card and it took me only 5 minutes to quickly hexedit it to be bootable and copy the files across.</p>

<ol>
<li><p>First, check to see what firmware your camera is running, so you know what file to download. This is nice and easy, and pretty much works 100% of the time. We'll also ease into the Terminal usage by having you navigate into your downloads folder.</p>
<code>cd ~/Downloads</code>
<p>If you're not on Leopard, you won't have a default Downloads folder, so go to your desktop instead -- we'll assume that you'll put all your temporary files there.</p>
<code>cd ~/Desktop</code>
<p>Next, create an empty file named 'vers.req'. This is easy!</p>
<code>touch vers.req</code>
<p>Now, copy this file to your memory card. You don't have to use the Terminal, you can go ahead and drag and drop it. Now the top level of your memory card will contain the 'vers.req' file. Eject it, and put it into your camera.</p>
<p>Turn on your camera on (in "playback" mode). Hold down the "SET" button, then also hit the "DISP" button. You'll see a gray overlay on the screen with white lettering. In the middle of the screen it will saw something like "Firmware Ver GM1.01B" (assuming you have a Canon PowerShot S5 IS). If you keep hitting the "DISP" button, you'll get some more info, including total shots you've taken with the camera. I'm at 3590 pictures!</p>
<p>OK, that's it for step 1.</p>
</li>
<li><p>Figure out which firmware enhancement your camera can / should use, based on the firmware detected in step 1 and this <a href="http://chdk.wikia.com/wiki/Firmware_Comparisons">Firmware comparisons list</a>. Probably you'll end up using the <a href="http://malbe.nm.ru/chdk/">Allbest</a> version, so select the one for your camera and firmware version and download and unzip it. If you've got a newer camera, you'll have just one 'DISKBOOT.BIN' file in zip, otherwise you'll also have a 'PS.FIR' file. If you do have this second file, things are simple and you can <a href="http://chdk.wikia.com/wiki/FAQ#Q._How_can_I_make_the_CHDK_program_load_automatically_at_startup.3F">follow instructions on how to make the CHDK program load automatically at startup</a>. If not, read on.</p></li>
<li><p>If your card is 2GB or smaller, you can <em>skip this step</em>. You might want to format your card in your camera just to have a clean card.</p>
<p>I have a 4GB card, so I went through this pain. In this step, we're going to partition your memory card.</p>

<a href="http://www.flickr.com/photos/boris/2429798754/" title="Getting CHDK working on the Mac - Disk Utility partition by bmann, on Flickr"><img src="http://farm4.static.flickr.com/3280/2429798754_a1e6b5bc7e_m.jpg" width="240" height="215" alt="Getting CHDK working on the Mac - Disk Utility partition" /></a>

<p>Open Disk Utility with your memory card inserted into a card reader on your system. Select the top level device (e.g. '3.8GB SanDisk SDDR-113' in my case), and you'll see a "Partition" tab in the right hand pane. Click on that, and in all likelihood you've the "Current" scheme is one partition. From the dropdown, select "2 Partitions", and make the "Untitled 1" that appears as small as possible. The right hand side, under Volume Information, will say some number like 536 MB next to size, and the default format will be set to Mac OS Extended. First, change the format to "MS-DOS (FAT)" (the name should switch to "UNTITLED 1" in all caps). Then, in the size box, type in "32". There will now be an asterisk next to the name. Go ahead and change it to something descriptive, like "BOOT".</p>
<p>Now select the second partition, and also change the format to "MS-DOS (FAT)" -- the name will again change to be "UNTITLED 2". Go ahead and give it a descriptive name -- I call mine "4GB_BORIS". Once you're done and are happy with the names, click on the "Apply" button. Voila! You now have a memory card with 2 partitions, which should both be mounted on your desktop as "BOOT" and "4GB_BORIS" (or whatever names you gave them). Next step!</p>
</li>
<li><p>If you skipped the last step because you have a 2GB or smaller card, welcome back! Everyone needs to do this step, which involves installing the <a href="http://www.macports.org">MacPorts</a> program, which lets you have access to a bunch of Linux utilities and programs that have been ported to work on Mac OS X. It's actually relatively straightforward.</p>
<p>Go ahead and follow the <a href="http://www.macports.org/install.php">MacPorts install instructions</a>. I went for the Leopard DMG file and installed the package.</p>
<p>As it says in the install instructions, after the install completes, open a new Terminal window, and run the following command:</p>
<code>sudo port -v selfupdate</code>
<p>If it prompts you for a password, enter your Mac user password. A bunch of gobbledygook will run across the screen, and then it should end in a message something like:</p>
<code>
The MacPorts installation is not outdated and so was not updated
selfupdate done!</code>
<p>Yay! Now you're ready to install a truly scary program: hexedit!</p>
</li>
<li>Why MacPorts? So that we can do *this* step. Open the Terminal again, and type in the following command to install hexedit:</p>
<code>sudo port install hexedit</code>
<p>Again with the gobbledygook, and then hexedit should be successfully installed.</p>
</li>
<li>Now here comes scariness: you're going to edit the innards of your memory cards boot partition directly. First, back to Disk Utility. Select the small or "BOOT" partition and click on "Info". You'll get a pop up window. The Disk Identifier should say something like 'disk1s1', and the File System *must*say 'MS-DOS (FAT16)' -- go back and re-partition if needed until you can get the two partitions. If all is well, then, with the "BOOT" partition still selected, click on the "Unmount" button.</li>
<li>Now, open a new Terminal window and type in:</p>
<code>hexedit /dev/disk1s1</code>

<a href="http://www.flickr.com/photos/boris/2429798792/" title="Getting CHDK working on the Mac - hexedit by bmann, on Flickr"><img src="http://farm3.static.flickr.com/2155/2429798792_78d59e5a4e.jpg" width="500" height="260" alt="Getting CHDK working on the Mac - hexedit" /></a>

<p>Where 'disk1s1' should be whatever you found using the Info command. Now you've got a scary looking window filled with text. Use the arrow keys to move the cursor over until the bottom indicator displays '0x40'. Now hit tab, and the cursors will jump over to the right hand side (ASCII mode). Type in 'BOOTDISK', then hit 'Ctl-X', type in 'Y' when it asks to save, and you're done with crazy hexedit.</p>
<p>Head back to Disk Utility, select the "BOOT" partition and hit the "Mount" button. The "BOOT" partition should again appear on your desktop.</p>
</li>
<li><p>Last step! Copy the "DISKBOOT.BIN" file onto your "BOOT" partition. Drag and drop works fine, and feel free to copy over the "vers.req" file, too. Now, eject your memory card and toggle the "Lock" switch on the side, and insert it back into your camera.</p>
<p>If all has worked correctly, you'll see a blue splash screen that says "Allbest 50" among other things. You'll have a percentage battery indicator, a numbered indicator of how many RAW shots you can take (RAW takes up about 10MB+ of space per shot). Pressing the printer / ALT button next to the viewfinder will bring up an additional screen for working with scripts. You can now follow instructions on the <a href="http://chdk.wikia.com/wiki/UBASIC">user scripting basics page</a> to add new features to your camera by copying different scripts. Good luck!</p>
</li>
</ol>

<p>The info was compiled from blood, sweat, and tears of getting this onto my own camera. You'll want to check out the following links:</p>
<ul>
<li>The main <a href="http://chdk.wikia.com">CHDK wiki</a></li>
<li><a href="http://chdk.wikia.com/wiki/Bootable_SD_card">Making a bootable SD card</a>, which lists Windows / Linux / Mac instructions, including the use of hexedit.</li>
<li>The <a href="http://chdk.setepontos.com/">CHDK forums</a></li>
<li>The <a href="http://chdk.wikia.com/wiki/FAQ/Mac">CHDK Mac FAQ</a> -- this lists a bunch of stuff about strang settings on unzipped files, but I never had to follow these steps.</li>
<li>Some advanced info on <a href="http://chdk.setepontos.com/index.php/topic,255.0/topicseen.html">autobooting for large card sizes</a>, which I'm hoping will eventually let us use the full 4GB / 8GB of space</li>
<li>For Canon S5 IS owners, the <a href="http://www.flickr.com/groups/canonpowershots5is/">Canon S5 IS Group on Flickr</a></li>
</ul>

<p>Comments, additional pointers, or a simple point-and-click Mac utility to make this process unnecessary highly welcomed :P</p>
