# Hue Test - web based local hub commands

Demo Site: http://huetest.azurewebsites.net

To use the site, first generate a hue API key using PowerShell. Replace the bridge IP below with yours.

$Bridge = "192.168.1.81"
$Body = @{devicetype = "TestHueApp#Testing"} | ConvertTo-Json
Invoke-RestMethod -Uri "http://$Bridge/api" -Method "Post" -Body $Body

Hit the button on top of the Hub then run the PowerShell commands, this will return your API key.

Enter the Hub IP along with the key on the site, this will save into a cookie to prevent you needing to re-enter it each time.