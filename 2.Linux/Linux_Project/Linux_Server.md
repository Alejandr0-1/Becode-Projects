# Step 1: Server Setup:

- Choose a Linux distribution that best suits the requirements 

- Set up a virtual machine (VM) for the server.

- Install the chosen Linux distribution on the server VM without a graphical user interface

- Update the system packages to ensure you have the latest software versions.

-----

# Step 2:  DHCP Server Configuration:

- Install the isc-dhcp-server package on the server:

" sudo apt-get install isc-dhcp-server "


- Configure the DHCP server to provide IP addresses to the local internal network:

- Edit the DHCP configuration file '/etc/dhcp/dhcpd.conf' to define the DHCP scope,including IP range, subnet mask, default gateway and DNS server.

- Start and enable the DHCP service to run at startup:

   " sudo systemctl start isc-dhcp-server "


----


# Step 3:  DNS Server Configuration:

- Install the bind package on the server:

   " sudo apt-get install bind9 "


- Configure the DNS server to resolve internal resources and use a redirector for external resources:

- Edit the DNS configuration file (/etc/bind/named.conf) to define internal zone and set up the redirector.

- Create DNS zone files for internal resources (library's domain, internal website).

- Restart the DNS service:

   " sudo systemctl restart bind9 "


----


# Step 4:  HTTP and MariaDB Server Configuration:

- Install the required packages for the HTTP server and MariaDB:

   " sudo apt-get install apache2 mariadb-server "

- Configure the HTTP server to host the GLPI internal website:

- Copy the GLPI files to the appropriate directory (e.g., /var/www/html).

- Configure MariaDB for the GLPI website:

- Create a new database and user, granting necessary privileges.

- Import the GLPI database schema into the MariaDB server.

- Restart the HTTP and MariaDB services:

   "sudo systemctl restart apache2 // sudo systemctl restart mariadb"


----


# Step 5: Weekly Backup:

- Create a script to automate the backup of configuration files for each service into a single compressed archive.

- Set up a cron job to execute the backup script on a weekly basis.


-----


# Step 6: Server Remote Management (SSH):

- ensure the SSH server is installed on the server:

   " sudo apt-get install openssh-server "


- Configure SSH to allow remote access and ensure it uses secure settings.

- Restart the SSH service:

   " sudo systemctl restart ssh "


-----

# Step 7: Workstation Setup:

- Install the necessary applications (LibreOffice, Gimp, Mullvad browser) on the workstation VM.

- Configure the workstation to use automatic addressing (DHCP) for obtaining an IP address.


-----


# Step 8: '/home' Folder on Separate Partition:

- Create a separate partition on the workstation VM's disk for the /home folder.

- Mount the separate partition to the /home directory.

- Update the /etc/fstab file to automatically mount the partition at boot.


-----

# Step 9: Remote User Assistance:

- Choose and implement a solution for remotely assisting user like TeamViewer, AnyDesk or SSH with port forwarding.

- Configure the solution to allow remote access to the workstation securely.


