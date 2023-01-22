# O365 Whitelist

## A Whitelist for PiHole and Microsoft Office 365

This is a fork of https://github.com/TheSmashy/O365Whitlist

DNS entries were sourced from Microsoft https://docs.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges?view=o365-worldwide

https://github.com/MicrosoftDocs/microsoft-365-docs/blob/public/microsoft-365/includes/office-365-u.s.-government-gcc-high-endpoints.md


## Installation
You should have python3 installed.  If you don't, go get it.  

**To install the O365 Whitelist**

    git clone https://github.com/TheSmashy/O365Whitlist.git  
    sudo python3 O365Whitlist/scripts/whitelist.py  

**Uninstall**  

    sudo python3 O365Whitlist/scripts/uninstall.py  
    

