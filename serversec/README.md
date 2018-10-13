# serversec  

servecsec is a script that install and configure some security tools.  
Must be executed as root.  
You are encouraged to go document yourself about the differents tools used in this script. This script only install some basic configuration for every tools. It will be updated with more advanced configuration in a near future (hopefully). Anyway, if you use this script, you should check the configuration files associated with the tools installed (as mentionned in post installation guide), some of them can ben updated with your email adress if you want to receive notifications, some other can be customized concerning certain security settings.

--- iptables ---  
https://wiki.debian.org/iptables  
The iptables script contained in the repo is copied to /etc/init.d. It contain a basic configuration for a web and mail server.  
  
--- portsentry ---  
https://www.symantec.com/connect/articles/portsentry-attack-detection-part-one  
portsentry is installed. The user must have to press enter at some point of the installation. A config file with basic configuration (portsentry.conf) is then copied to /etc/portsentry/ to replace the unedited one. Feel free to update it with your own configuration.  
  
--- fail2ban ---  
https://www.fail2ban.org/wiki/index.php/Main_Page  
fail2ban is installed, and the jail.local file contained int config_files is copied to /etc/fail2ban/jail.local. Feel free to enable or disable jails. Please check that everything works of with your system with "sudo service fail2ban status". If it's not ok, there must be an active jail for a service you don't use.  
  
--- snort ---  
https://www.snort.org/  
https://rules.emergingthreats.net/  
snort is installed. The user must provide the name of the network interface snort will be listening on during the installation. You can find it with running "ifconfig". The config file (oinkmaster.conf) is then replaced by an updated one.  
/!\ Caution : the ruleset used by this script is vor snort-2.9.0, if the current version of snort isn't 2.9.0, you may have to reload the ruleset. To do that, edit the url leading to the .tar.gz containing the rules with your version number, then run "sudo oinkmaster -o /etc/snort/rules". You will be notified during the execution of the script if your ruleset isn't correctly installed.
config file : /etc/oinkmaster  
  
--- rkhunter ---  
https://www.tecmint.com/install-rootkit-hunter-scan-for-rootkits-backdoors-in-linux/
rkhunter is installed, and some basic configuration file is installed.



- apt install logcheck logcheck-database binutils
- ajouter à la fin du script (ou dans le logcheck ou dans un fichier spécial "post_installation_guide)) une liste des fichiers de config à aller voir
