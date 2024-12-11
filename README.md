This project was made as part of OS LAB MINI PROJECT 
Created by CS GROUP 1 (Roll No: 1- 10)

*Important Note: Follow the instructions below to successfully run the project*
*All the code files need to be present on both the server and client machines in order to run the login file function)

-> Compile the files in the following order (It is important to compile the server and client files before running the login file):

   gcc reservation_server.c -o server

   gcc reservation_client.c -o client

   gcc login.c -o login

-> Run the login file by the following command:
    ./login

-> First time run:
    Make sure to uncomment the init_file() line. This will initialize the seat.txt file for a fresh run.


Provided code will work for server and client(s) running on the same machine. 
In order to run it from different machines on the same network, follow the steps below:

To run of different machines on the same network:
(*These are the steps to be followed if the server is running on WSL*):
   -> Enable port forwarding and disable firewall

      -> For port forwarding: 
           ->Run on Windows Powershell as admin: netsh interface portproxy add v4tov4 listenaddress=0.0.0.0 listenport=8080 connectaddress=<server ip> connectport=8080
             (Replace with actual IP address of your server instance, which can be found out by typing "ip addr" in the WSL instance where the server will run)
      
      -> To disable Firewall:
          -> Open Windows Firewall Settings:
          -> Open Windows Defender Firewall. Open Advanced Settings. Create a New Inbound Rule.
          -> Select Rule Type: Specify Port: Choose TCP (or TCP/UDP if necessary).
          -> Select Specific local ports and enter the port number you want to open (e.g., 8080).
          -> Choose Allow the connection and click Next.
          -> Profile Selection: Select when this rule applies:
             (You can select all profiles if unsure, but make sure to at least select Private for most local network connections)

    -> Replace the IP address in the client code with the physical IP address of your server machine (Not the WSL instance)

users.txt file contains the username and hashed password along with the role of the user.
The default admin username: mushkan_kumari 
default admin username: mus123
The role of the user may be changed by manually editing the users.txt

prices.txt file contains the base price of each coach

seat.txt contains the reservation information of each coach(Go through the server code file for more info)








