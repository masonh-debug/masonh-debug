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


