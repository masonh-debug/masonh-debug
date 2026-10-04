<pre>   ______ _ __     __          __    
  / ____/(_) /_   / /   ____ _/ /_   
 / / __ / / __/  / /   / __ `/ __ \  
/ /_/ // / /_   / /___/ /_/ / /_/ /  
\____//_/\__/  /_____/\__,_/_.___/   

</pre>
```bash
echo "building, breaking, and securing network & systems."
<!-- QUOTE_START -->
> "Creativity is the key to success in the future, and primary education is where teachers can bring creativity in children at that level." — *Abdul Kalam*
<!-- QUOTE_END -->

  7
   8 winrm quickconfig -q
   9 winrm set winrm/config/service '@{AllowUnencrypted="true"}'
  10 winrm set winrm/config/service/auth '@{Basic="true"}'
  12 New-NetFirewallRule -DisplayName "Ansible WinRM HTTP" -Direction Inbound -LocalPort 5985 -Protocol TCP -Action Allow
  13 winrm enumerate winrm/config/listener
