# BSIDES_rubber
This repository contains all the code and instructions needed to perform the "Rubber Ducky" Workshop at the Hacking Village of BSides Strasbourg 2024.

## Instructions
Here are 2 scripts that you can try to implement :
  - trigger a rick roll
  - disable windows defender real-time monitoring and firewall

To do so, follow these steps :
  1) try to figure out how to perform these actions if you were a human
  2) try to make less actions as possible (consider using useful shortcuts like windows + R)
  3) script these steps on your rubber ducky
  4) try it and find the issues (which actions are not working properly)
  5) return to step 3 :)

## Ressources
### Rick roll
Link to the video : https://youtu.be/dQw4w9WgXcQ?t=43s

### Disable windows defender
The commands below are commands to run on Administrator Powershell
  Disable real time monitoring : Set-MpPreference -DisableRealtimeMonitoring $true -Force
  See state of RealtimeMonitoring : Get-MpPreference | Select-Object -Property DisableRealtimeMonitoring
  Disable windows defender firewall : Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
