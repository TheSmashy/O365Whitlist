# M365 Whitelist for Pi-hole

Curated allow and deny lists to keep Microsoft 365 services working (Outlook, Teams, SharePoint, OneDrive) while blocking telemetry noise.

This repo is for Enterprise/Worldwide tenants.  
For GCC, see the fork here: [obiwantoby/O365Whitlist](https://github.com/obiwantoby/O365Whitlist).

## What it does

✅ Keeps M365 functional

✅ Blocks known telemetry endpoints

✅ Easy to apply, easy to roll back

## Quick Start

**1. Back up Pi-hole first (seriously):**

```bash
sudo cp /etc/pihole/gravity.db /etc/pihole/gravity.db.bak.$(date +%s)
```

**2. Clone:**

```bash
git clone https://github.com/TheSmashy/O365Whitlist.git
cd O365Whitlist
```

**3. Apply lists:**

```bash
python3 scripts/whitelist.py
pihole -g
pihole restartdns
```

**4. Roll back if you break Teams/Outlook:**

```bash
python3 scripts/uninstall.py
sudo cp /etc/pihole/gravity.db.bak.<timestamp> /etc/pihole/gravity.db
pihole -g
pihole restartdns
```

## Notes

Tested on Pi-hole v5. Works on v6, but you’ll likely add lists via Adlists instead of directly editing gravity.db.

Critical endpoints like `login.microsoftonline.com` are never denied. Don’t modify them unless you want authentication loops.

Regex rules are optional—start with exact lists first.

## Credits

Original project: TheSmashy (this repo)

GCC fork: [obiwantoby/O365Whitlist](https://github.com/obiwantoby/O365Whitlist)

## Disclaimer

This is community-maintained. Use at your own risk. Back up before applying.
