# Windows Server 2022 Active Directory Lab
A virtualized lab demonstrating deployment of Windows Server 2022 as a domain controller, DNS/DHCP configuration, and Windows 11 client domain integration for enterprise simulation.

- Windows Server 2022 (Domain Controller, DNS, DHCP)
- Windows 11 Pro (Clients)
- VirtualBox (Virtualization)
- Active Directory, DHCP, DNS, Reverse Lookup Zones

Installed Windows Server 2022 in VirtualBox
    
    -  Named the VM
      
![DCName](DCName.png)

    - Allocated 4GB Ram and 2 Processors
![DCHardware](DCHardware.png)

    - Allocated 50 GB of hard disk space
      
![DCHardDisk](DCHardDisk.png)

    - Created a new network for the server and client machines to connect to

![DCNetwork](DCNetwork.png)

    - Manually set static IP of server to 10.0.0.4 and DNS IP addresses to Google's DNS servers
    
![DC1CMD](DC1CMD.png)

    - Installed Active Directory, DHCP, and DNS roles via the server manager

![DCServerRoles](DCServerRoles.png)

    - Configured DNS manager with Forward and Reverse Lookup Zones with A records for lab.com

![DNSSetup](DNSSetup.png)

    - Configured a new scope for the DHCP role, with an IP range of 10.0.0.100 - 10.0.0.200

![DHCP-Scope](DHCP-Scope.png)

    - Created two users to test with the two client PC's I created later
![CreateUsers](CreateUsers.png)

    - Here is the CMD showing everything running properly
![CompletedPowershell](CompletedPowershell.png)

    - Created to virtual machines named Client-1 and Client-2
    
![Client1Creation](Client1Creation.png)

    - Client 1 and 2 screenshots of getting IP addresses from the DHCP server on the same virtual network

![Client-1-CMD](Client-1-CMD.png) ![Client-2-CMD](Client-2-CMD.png)

    - Ping and nslookup results for client 1 and 2
![Client-1-Ping-Lookup](Client-1-Ping-Lookup.png) ![Client-2-Ping-lookup](Client-2-Ping-lookup.png)

    - Client 1 and 2 successful joining of the lab.com domain
![Client-1-Lab-Join](Client-1-Lab-Join.png) ![Client-2-Lab-Join](Client-2-Lab-Join.png)

    - Client 1 and 2 successful signing in after being joined to the lab.com domain

![Client-1-Signed-in](Client-1-Signed-in.png) ![Client-2-signed-in](Client-2-signed-in.png)
