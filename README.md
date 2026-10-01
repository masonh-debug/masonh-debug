<pre>   ______ _ __     __          __    
  / ____/(_) /_   / /   ____ _/ /_   
 / / __ / / __/  / /   / __ `/ __ \  
/ /_/ // / /_   / /___/ /_/ / /_/ /  
\____//_/\__/  /_____/\__,_/_.___/   

</pre>
```bash
echo "building, breaking, and securing network & systems."
<!-- QUOTE_START -->
> "Money Has Never Made Man Happy, Nor Will It, There Is Nothing In Its Nature To Produce Happiness. The More Of It One Has The More One Wants." — *Benjamin Franklin*
<!-- QUOTE_END -->

  7
   8 winrm quickconfig -q
   9 winrm set winrm/config/service '@{AllowUnencrypted="true"}'
  10 winrm set winrm/config/service/auth '@{Basic="true"}'
  12 New-NetFirewallRule -DisplayName "Ansible WinRM HTTP" -Direction Inbound -LocalPort 5985 -Protocol TCP -Action Allow
  13 winrm enumerate winrm/config/listener
