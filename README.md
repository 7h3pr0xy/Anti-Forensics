# Anti-Forensics

Anti-forensics is the art of leaving no trace on your computer, it is combating common forensic tools in preventing any penetration for forensic tests on your computer. Anti-Forensics can pretty much be summed up in one famous quote:
 
 
"Make it hard for them to find you, and impossible for them to prove they've found you." 
 
Because Linux installations are pretty much already secured, this guide will only focus on Windows. Windows is a security nightmare, but what if I were to tell you there was a way around this, a way to make Windows secure? VPNs, proxies, and Tor only get you so far, but what do you do when they've traced it to your computer? Anti-forensics is designed for this situation, to prevent them from proving you've done anything wrong even if they have your computer.
 
With that being said, let's get started.
 
 
Disabling Time Stamps
 
Using TimeStamps, forensic experts can build a 'digital time-line', this can be very compelling evidence when cross-referenced with other known evidence. In order to strengthen security, we must disable these logs.
 
 
Step 1.) User Assist File
 
There is a registry setting that keeps logs and dates of all launch programs, forensic experts can use this to build a digital timeline, we must disable this for computer security. 
 
Navigate to 'HKEY_Current_User\Software\Microsoft\Windows\Currentvers ion\Explorer\Userassist' . You should see two subkeys called Count, delete both these keys. Now right-click the UserAssist key and create a new key named 'Settings'. In this key create DWORD value named NoLog, set the value to 1. 
 
Windows will no longer store hidden logs of the exact times you have been accesing files, therefore forensics experts can no longer use these hidden logs to create a digital timeline.
 
Step 2.) Last Access Logs
 
Next we will disable the last access in Windows. What last access is is a setting on Windows that allows you to see when you opened, modified, and/or created files on your computer and is similar to the UserAssist registry key. By disabling this forensic experts won't as easily be able to tell when you've been accessing programs or files on your computer. 
 
To disable last access open command prompt on your computer, if on Vista or Windows 7 make sure to run as administrator. In command prompt type the following: 
 
fsutil behavior set disablelastaccess 1
 
Last access has now been disabled, in order for it to take effect you must restart your computer. 
 
 
Encrypting Your Computer
 
 
It is very important to make sure that your computer is encrypted, in the case an unwanted visitor is trying to access your computer, they will not be able to access to computer if it is encrypted. 
 
 
Step 1.) VeraCrypt
 
To encrypt your computer, you can use Veracrypt, a free program that allow you to encrypt your computer. When encrypting with VeraCrypt, you have two options; the first one is to create a hidden container. A hidden container is an operating system that is impossible prove exists. 
 
When creating a hidden container you will have three different passwords:
 
1. The First would be for your decoy system, the operating system you would show someone forcing you to login your computer.
 
2. The second password would be for your outer volume, the operating system you would show someone forcing you to login to the second partition on your computer (a second partition is require computer for your hidden container is.
 
3. Third password is for the hidden operating system on the second partition of your computer, this operating system is placed in the inner volume, and is impossible to prove exists (It appears to be RAW data).
 
The second option is to just encrypt your hard-drive. This is also very secure, but you may be forced to give up your password due to court-order (In this situation, if you are a VERY good lier, you could simply say 'I forgot', but you would have to make it believable.) With normal drive encryption, your computer is just as secure encryption wise, and you will have a single password.
 
 
Step 2.) Encrypt Your Keystrokes
 
You need to protect yourself from keyloggers. As strange as it may sound even the government has keyloggers, a few years ago the law speculation about CIPAV, a government spyware known to send the users IP address, Mac address, open ports, operating system, installed applications, default web browser, visited URLs, logged in user, etc...
 
In order to protect yourself from keyloggers, you should encrypt your keystrokes. You can do this using a software called 'Keyscrambler'. Please note, you should NOT use the free version of Keyscrambler, you should only use the Premium version, which costs a decent some of money. (-Cough- ThePirateBay.se -Cough-). 
 
Keyscrambler Premium supports 170 programs, including windows logon, most web browsers, and popular IM programs (i.e. Skype).
 
 
Making Encryption Secure
 
Encryption is pointless if it can be easily bypassed or overcome. You need to make sure that the encryption is secure too.
 
 
Step 1.) Make Sure Your Password Is Strong
 
Even with your computer encrypted, it is still vulnerable. Make sure your password is good (for optimal security, your password should be twenty or more characters, with symbols, numbers, and random capitals, and a special symbol (like ALT+1456) really increase security). 
 
If you password is not strong enough, you can change it by right clicking your encrypted drive in VeraCrypt and selecting 'Change Password'.
 
Step 2.) Create A Locked Screen Saver
 
Encryption is pointless if the feds get to your computer while its running. They can use live forensic tools that don't require the movement or shutdown of a computer. A very simple technique to overcome this is to create a locked screen saver. 
 
To create a locked screen saver in Windows Vista or Windows 7;
 
Right click your desktop and click on 'Personalize'. In the bottom left hand corner you should see 'Screen Saver', click that. Now, check 'On Resume, Display Logon Screen', and set 'Wait' to 5. Now, underneath that you may set what you want your screen saver to be. 
 
Now you must go to your Control Panel. Click on System and Securtiy, now click on 'Power Options' find your selected plan and click 'Change plan settings.' Now, set 'Turn Of Display' to 5 minutes. Voila! You have now created a locked screen saver.
 
Step 3.) Get A Good Anti-Virus
 
This may seem obvious, but all this is pointless if you get infected with a keylogger that takes screen shots. Having a good anti-virus is one of the most important things you can do. Now, listen up. AVG, Avast, McCafe, Norton? They all SUCK. The only Anti-Virus you should even consider are ESET Nod32 and Kaspersky, BitDefender is also pretty good.
These anti-virus programs are expensive, but you can torrent them from ThePirateBay.se, just make sure you find one with a lot of seeders.
 
 
Disabling Windows Hibernation
 
You may as well hand your computer over to the feds if they raid your house and your computer is in hibernation. Also, putting your computer into hibernation is pretty much just taking a screen shot of your RAM that gets saved to your hard drive.
 
To disable hibernation in Windows Vista/7/8:
 
Open your Control Panel. Click System and Security, then click 'Power Options'. Click 'Change plan settings' for you current power plan.
 
Now click 'Change advanced power settings'. Expand 'Sleep', then expand 'Hibernate After'. Enter “0" for 'Setting:' to set hibernate to 'Never'. 
 
Hibernation is now disabled.
 
 
Disable and Remove USB Logs
 
Next on the list of Anti-Forensics in to disable logs of USB activity, flash drives, etc... This can be valuable if you have a flash drive with sensitive data and you don't want any logs of it ever being plugged it to your computer.
 
 
 
Step 1.) Delete the USBSTOR Registry Setting
 
The USBSTOR setting contains history of plugged in USB devices. 
 
To delete it, hit the WINDOWS Home Button + R at the same time. This will open up 'Run'; type: "Regedit" (without quotes). Browse to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\USBSTOR
 
Now, right click 'USBSTOR' and hit 'Delete', then confirm that you want to delete the key. Now, the key has been deleted.
 
Step 2.) Delete The Setupapi.log File
 
The Setuppapi.log is a plain-text file that stores the list of installed USB devices and their drivers. We will delete it with a program called CCleaner. 
 
CCleaner is actually one of the best anti-forensic tools out there, and its free. For Instructions on using CCleaner, Please see the 'CCleaner' section of this guide.
 
 
Windows Security Misc.
 
This is for the shit that has to do with windows anti-forensic security, but wasn't big enough to have its own section. That does NOT mean this section isn't important, the stuff in here may actually be the most important in the whole guide.
 
 
Step 1.) Disable System Restore Points
 
System Restore points can be used to bring your computer back to a date when it wasn't secure and can also be used to restore overwritten files. 
 
To disable System Restore points, right click 'Computer' and click 'Properties'. Now click 'Advanced System Settings'. Under 'System Protection' click 'Configure'.
 
Now, select 'Turn Of System Protection' and apply it.
 
Step 2.) Disable 'Send Error Report to Microsoft
 
This is self-explanitory, we obviously don't want microsoft having logs of all our crashed programs. 
 
To do this, go to your start menu and search 'problem reporting settings' and then click on 'Choose How To Report Problems'. Click 'Change Report Settings For All Users' and then set it to 'Never check for solutions'.
 
 
Step 3.) Wipe With CCleaner
 
This is the heart of Anti-Forensics right here. CCleaner is actually one of the most powerful Anti-Forensic tools, -IF- used correctly. 
 
As it turns out, when deleting files, you DO NOT need to do multiple overwrites. With modern hard-drives, one overwrite really is enough to delete a file beyond repair, even though it is popular belief that you need several overwrites to be secure. 
 
With CCleaner, I would recommend three overwrites, just in case it misses something the first time around (remember, it is a free software).
 
Once you have CCleaner installed, run it (AS ADMIN), go to 'Settings' and make sure you have it set to overwrite deleted data with three passes. 
 
Go back to 'Cleaner' and check EVERYTHING. I mean EVERYTHING, and hit 'Run Cleaner'. You might want to leave this on overnight.
 
Do this every time you are done with a major hacking job. When using normally (what should be every time you are done with your computer), uncheck 'Wipe Free Space', this will cut down the time from hours to a few minutes.
 
Step 4.) Disable Debugging Upon Failure
 
This keeps logs of your computers failures and blue screen info.
 
To disable it, right click 'Computer' and go to 'Advanced System Settings', now go to 'Start Up and Recovery'. Now, set 'Debugging Information' to 'None'.
 
Step 5.) Disable Windows Event Logging
 
Windows keeps logs of all events on the computer. First, before we disable, we must clear all the logs. 
 
To disable it, go to Control Panel then System and Security. Now, click Administrative Tools, and then Event Viewer. In either pane of the Event Viewer window, right-click System and then select Clear All Events, you will get a window that says: "Do you want to save 'System' before clearing it?", click 'No'. 
 
Now we must disable Windows Event Logging. Go to 'Run' and type in 'msconfig', then go to 'Services' and make sure 'Hide all Microsoft Services' is UNCHECKED. Now scroll down until you find 'Windows Event Logging', and UNCHECK it. 
 
Now restart your computer right away.
 
Step 5.) Disable StandBy In Registry
 
Disable 'Stand By'. Just create a new text document and add this:
 
Code:
Windows Registry Editor Version 5.00 
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Servic es\ACPI\Parameters] "AMLIMaxCTObjs"=hex:04,00,00,00 "Attributes"=dword:0070 [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Servic es\ACPI\Parameters\WakeUp] "FixedEventMask"=hex:20,05 "FixedEventStatus"=hex:00,84 "GenericEventMask"=hex:18,50,00,10 "GenericEventStatus"=hex:10,00,ff,00
 
 
 
Then save as a .REG file, and run it. Click okay when prompted for confirmation.
 
 
Preventing From Being Found In The Traced In The First Place
 
 
You should never be tracked in the first place. Follow these guide lines to stay anonymous:
 
1.) Use a no log VPN, such as nVPN, or Anonymous VPN, both of these are excellent and highly secure. Offshore is better than onshore.
2.) Use Tor for web browsing you wouldn't want the FBI, or your ISP looking at.
3.) Never release personal information online and use different aliases. Never connect ANY real information to your hacking alias. Build fake information if you are paranoid.
4.) Assume the FBI has the IP logs of every website in the world.
5.) Use SSH tunneling to an offshore shell on top of your VPN for extra security.
6.) Don't get lazy, and be patient.
 
 
TIPS: 
 
NEVER Have Personal Information On Your Hacking Computer (Facebook, Twitter, Pictures, etc...)
 
Always Use SSL Versions Of Websites, There Are Add-Ons To Many Browsers That Will Do This For You
 
NEVER Talk About Hacking In Emails, Use Encrypted Chat Services (Skype Works If On VPN, And ChatCrypt Is A Good One)
 
Ideally, there should be nothing incriminating in your home, or at least too incriminating. No crack, no ectasy. Marijuana is okay in some states as long as its under an ounce (It will just be a fine.)
 
Don't Use Credit Cards Anywhere Near Places You Use Wi-Fi To Hack From, And Remember, They DO Have Security Cameras.
 
#1 TIP: If the cops show (with a warrant), You don't say a WORD. A NOT A SINGLE SOUND SHOULD EXIT YOUR MOUTH. You don't say 'I want my lawyer', you don't say 'Don't touch that', you say NOTHING. If you even your mouth for a SECOND, and say ANYTHING, even if its only 'Hi', consider yourself screwed. YOUR MOUTH SHOULD NEVER BE OPEN.
 
Enjoy!
