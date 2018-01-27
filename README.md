# CCB Backup & Bell (ringing) Server Deployment

- Requires Ansible 2.4 or newer
- Expects Raspbian Server host/s

There are 4 roles in this playbook:

## raspbian_prep

Ensures basic utilities are in place including pip (Python), git, ntp, zip, and aptitude.  Upgrades
all existing modules.  Sets up NTP.

## ccb_backup

Sets up ccb_backup user and installs supporting Python packages required by ccb_backup and sets up
backups to run in cron (as well as IP address email on @reboot in cron).

## bells

Installs Raspberry Pi omxplayer for MP3 files.  Creates bells user.  Sets up crontab to play bells at 12pm and 6pm
daily as well as 8:25am on Sundays.

## raspbian_wireless

Sets up wireless SSID and password in wpa_supplicant and reconfigures wlan0 interface.

----

For details on how to use this to set up the Pi, see https://goo.gl/2bzP5p
