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

Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
Start-Service sshd
Set-Service -Name sshd -StartupType 'Automatic'

