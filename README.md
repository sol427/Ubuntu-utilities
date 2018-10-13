# Ubuntu-utilities  
Some simple scripts I wrote to simplify some tasks on my Ubuntu server.  
    
--- duhomes ---  
I often want to monitor the disk usage of some directories, including the different homes and my /var/www, so I wrot this tiny script that display theses informations in a simple way.  
Use :  
 sudo duhomes  
   
--- fail2ban-allstatus ---  
This really simple script displays the status of all the enabled jails in fail2ban.  
Use : 
 sudo fail2ban-allstatus  
   
--- newborn ---  
This scripts creates a user that can only connect to the server via SFTP. The home directory associated with the account is chrooted so that the user can't access anything else than his account. The user can't access the command line. I use this to share files with people I don't trust. I don't trust anyone.  
Use :  
 sudo newborn your_user  
  
--- killuser ---  
This script forces the deletion of an account, and removes the home folder associated even if it doesn't belong to the user. 
Use :  
 sudo killuser your_user  
