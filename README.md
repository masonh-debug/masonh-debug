<pre>   ______ _ __     __          __    
  / ____/(_) /_   / /   ____ _/ /_   
 / / __ / / __/  / /   / __ `/ __ \  
/ /_/ // / /_   / /___/ /_/ / /_/ /  
\____//_/\__/  /_____/\__,_/_.___/   

</pre>
```bash
echo "building, breaking, and securing network & systems."
<!-- QUOTE_START -->
> "Study me as much as you like, you will not know me, for I differ in a hundred ways from what you see me to be. Put yourself behind my eyes and see me as I see myself, for I have chosen to dwell in a place you cannot see." — *Rumi*
<!-- QUOTE_END -->

Get-NetConnectionProfile
Set-NetConnectionProfile -NetworkCategory Private
winrm invoke Restore winrm/config
winrm quickconfig -q
winrm e winrm/config/listener
New-NetFirewallRule -DisplayName "Ansible WinRM HTTP" -Direction Inbound -LocalPort 5985 -Protocol TCP -Action Allow

#Bidirectional drag and drop VM
# click Devices and insert Guest Addition CD
#bring up a terminal and input these commands

sudo apt update && sudo apt upgrade -y
sudo apt install build-essential linux-headers-$(uname -r) dkms -y
sudo mkdir -p /mnt/cdrom
sudo mount /dev/cdrom /mnt/cdrom
cd /mnt/cdrom
sudo ./VBoxLinuxAdditions.run
#last step restart VM

