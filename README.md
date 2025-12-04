# AdminBypass-Windows

this is a kit to bypass or obtain administrator privileges on a restricted pc ( Windows )

# WARNING !
Without the admins consent, bruteforce and fake UAC are illegal !
You have been warned !
If a restricted pc is from a company or organization ( school, work ), it is likely that they can see if an admin is logged and detect unusual activity.

---

# Invoke method
> Find the template file in RunFiles/RunAsInvoker
this method is to bypass the admin popup when trying to run files with protection, this will not work on files that need admin perms to actually access protected sections of the retricted pc.

Make sure to have the file you want to execute ( we will call it ftex ) and the template file in the same folder
then edit the template file and change "file_name.extension" to the name of ftex.
> Include the file extension !
then save the template file and run it, that's it : )

---

# BruteForce method
> Find the files in AdminDirectAttack/Bruteforce
this method will try to find the password of an admin user on your pc, this may not work if the password is not in the library.
> The library include 110k common passwords
Make sure to have both files in the same folder
execute userbruteforce.bat

options :
1. User list
2. Find password
3. Exit

In the list of users, find a user with an SID ending with "500" with "OK" status. Remember the username
Then in the find password option write the username in the TARGET input

---

# Fake UAC method
> Find the files in Psychology/fakeuac
this method will prompt a fake UAC ( window for admin auth )

show this to your administrator saying this poped up randomly and you can't remove it ( pressing no will just show the popup again seconds later )
if the admin approves a cmd panel will open in the background, this panel can execute any command an admin could.
example to change a user password ( even an admin )
```bash
net user username newpassword
```
