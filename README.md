# O365 Whitelist

## A Whitelist for PiHole and Microsoft Office 365

This is a script that will add exact and regex whitelist entries for use with Microsoft 365.  It will also add some blacklist entries.  I've been testing this whitelist for the past six months working from home using and adminstering O365 with PiHole as my DNS.  I have a comprehensive set of block lists and some regex entries, so I've added some additonal entries that I've found may be required if you're in that situation.  Also, there is a lot of telemery in Microsoft 365, so blacklist entries are added as well.

DNS entries were sourced from Microsoft https://docs.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges?view=o365-worldwide
Not every entry was added as some are not required and some could be considered malicous.

Most of this project is based off the work of Anudeep, visit his page and give him money: https://github.com/anudeepND/whitelist

This has been tested on version 5 of PiHole, it really relies on the database to make regex entries.  There is a text whitelist, but I have no idea if it'll work.  I haven't tested this with docker, so I'll do that later and add support and directions.

## Installation
You should have python3 installed.  If you don't, go get it.  

**To install the O365 Whitelist**

    git clone https://github.com/TheSmashy/O365Whitlist.git  
    sudo python3 O365Whitlist/scripts/whitelist.py  

**Uninstall**  

    sudo python3 O365Whitlist/scripts/uninstall.py  
