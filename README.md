# OS-Reservation-Project

To run of different machines on the same network(in case of WSL):
   -Enable port forwarding and diable firewall
   -For port forwarding: 
      Run on Windows Powershell as admin: netsh interface portproxy add v4tov4 listenaddress=0.0.0.0 listenport=8080 connectaddress=<server ip> connectport=8080
      Replace with actual ip of your server
   - To disable Firewall:
     Open Windows Firewall Settings:
     Open Windows Defender Firewall. Open Advanced Settings. Create a New Inbound Rule.
     Select Rule Type: Specify Port: Choose TCP (or TCP/UDP if necessary).
     Select Specific local ports and enter the port number you want to open (e.g., 8080).
     Allow the Connection: Choose Allow the connection and click Next.
     Profile Selection: Select when this rule applies:
     You can select all profiles if unsure, but make sure to at least select Private for most local network connections.
