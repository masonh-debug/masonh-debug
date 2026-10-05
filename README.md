<pre>   ______ _ __     __          __    
  / ____/(_) /_   / /   ____ _/ /_   
 / / __ / / __/  / /   / __ `/ __ \  
/ /_/ // / /_   / /___/ /_/ / /_/ /  
\____//_/\__/  /_____/\__,_/_.___/   

</pre>
```bash
echo "building, breaking, and securing network & systems."
<!-- QUOTE_START -->
> "Tolerance Implies No Lack Of Commitment To One'S Own Beliefs. Rather It Condemns The Oppression Or Persecution Of Others." — *John F. Kennedy*
<!-- QUOTE_END -->

Get-NetConnectionProfile
Set-NetConnectionProfile -NetworkCategory Private
winrm invoke Restore winrm/config
winrm quickconfig -q
winrm e winrm/config/listener
New-NetFirewallRule -DisplayName "Ansible WinRM HTTP" -Direction Inbound -LocalPort 5985 -Protocol TCP -Action Allow

#Bidirectional drag and drop vm
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential linux-headers-$(uname -r) dkms -y
sudo mkdir -p /mnt/cdrom
sudo mount /dev/cdrom /mnt/cdrom
cd /mnt/cdrom
sudo ./VBoxLinuxAdditions.run


