# nxos
####SCRIPT: autoconfig.py 

Script is an enhancement to the GIT/EEM example in Cisco [NXOS Programmability and Automation book.](http://www.cisco.com/c/dam/en/us/td/docs/switches/datacenter/nexus9000/sw/open_nxos/programmability/guide/Programmability_Open_NX-OS.pdf)  

Script runs in N9k guestshell, triggered by an EEM applet running on Nexus 9k. I've included the EEM config: 'eem-config.txt'.

Here's what's happening:  
1) The running config is copied to bootflash as running.latest.  
2) Guestshell is kicked off with a python script.  
3) We update a counter for reference later.  
4) We move 'config.latest' to a directory on our local git server (running as git bare server on the N9k).  
5) We then do a push onto our internal gitlist server.  

Here's a link to setting up a [git bare server.](https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server)

There are a few free git repository viewers such as GitLab or GitList. I used GitList. [Documentation link is here.](https://github.com/klaussilveira/gitlist/blob/master/INSTALL.md)


If you run into authentication challenges, check out this [link.](http://superuser.com/questions/338511/how-do-i-disable-password-prompts-when-doing-git-push-pull)  
  
####SCRIPT show-mac-interface.py

Update the python script with your creditials.  
Enter and IP Address and output will return : MAC address and interface from which the MAC was learned. Helps in quick troublshooting.  

#Postman for ACI  
Included is a postman collection with environmentals. Just update your environmentals and you should be able to make configs to your APIC via the collection.  

***todo: convert the collection into python calls***





