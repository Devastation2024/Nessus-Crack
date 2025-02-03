# Nessus-Crack
Nessus cracked version [for debian system]
The installation script is suitable for Debian system and can be successfully installed on Kali Linux.
- Download :
nessus_ubuntu.sh
- change the url in the script as needed 
"echo " o downloading Nessus.."
curl -A Mozilla --request GET \
  --url 'https://www.tenable.com/downloads/api/v2/pages/nessus/files/Nessus-10.8.3-ubuntu1604_amd64.deb' \
  --output 'Nessus-latest-ubuntu1404_amd64.deb' &>/dev/null"

- Grant execute permission : chmod +x nessus_ubuntu.sh
- Use the sudo  to execute nessus_ubuntu.sh (please wait patiently) for about 10-15 minutes.
- Open the following web page to access Nessus.
  
                        https://127.0.0.1:11127/
                                     or
                        https://serveripaddress:11127/
  default login : admin
  default password : ddosi

- Nessus start and stop service commands

   Startup :

       sudo systemctl start nessusd && systemctl --no-pager status nessusd

  Stop :
  
       sudo systemctl stop nessusd && systemctl --no-pager status nessusd

- Uninstall method

Stop the Nessus service : sudo systemctl stop nessusd && systemctl --no-pager status nessusd

- Modify the properties of the /opt/nessus/ folder
  
       chattr -i -R /opt/nessus/
  
- Uninstall Nessus

        apt remove nessus

- Precautions
 Issue: After a system or Nessus reboot, the Scan button may temporarily become unavailable.

 Cause: Nessus is reconfiguring plugins.

 Solution: Just wait patiently for 3 to 5 minutes.


Tested working on ubuntu-24.04.1 with Nessus-10.8.3

