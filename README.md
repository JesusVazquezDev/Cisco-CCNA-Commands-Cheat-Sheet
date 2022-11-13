# Cisco-Commands-Cheat-Sheet
Here you can find the CISCO cli commands you have to learn for the CCNA.



# CISCO Modes
| Mode | Description | 
|:----------:|:-------------:|
Router> | User mode
Router# | Privilege mode
Router(config)# | Global Config mode 
Router(config-if) | Interface mode
Router(config-vlan)# | Vlan config mode
Router(config-router)# | router config mode



# Basic Commands

| Command  | Purpose | 
|:----------:|:-------------:|
 `enable`| Enters privilege mode 
 `configure terminal` | Enters configuration mode
 `description` *<name-string>* | Sets a description to the interface
`hostname` *name* | Sets a host name to the current Cisco network device
`interface` *fastethernet/number* | Enters interface configuration mode for the specified fast ethernet interface
`copy` *from-location to-location* | copie a file (or set of files) from one location to another
`copy running-config startup-config` | It saves the configuration when the device reloads, it loads the latest configuration file
`copy startup-config running-config` | Saves the startup configuration into the running configuration
 `write` / `write memory` | Save the current configuration
 `write erase` / `erase startup-config` | Deletes the startup config
`reload` | 	Reboots the device
 `exit` / `end` | Returns to previous mode 
 `logout`/ `disable` | 	Exit User mode
 `shutdown` |  Shuts down the interface
 `no shutdown` | turns up the interface
 
 # Basic show Commads
 | Command  | Purpose | 
 |:----------:|:-------------:|
 `show running-config` | Displays the current configuration
 `show startup-config` | Displays the configuration at startup
 `show interfaces` | Displays detailed information about interface status
 `show ip protocols` | Displays all the configured routing protocols 
 `show ip interface` |  Displays the status for each interface
 `show interface status` | Displays the interface line status
 `show mac address-table` | Displays the MAC address table



 
# Vlan Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
`vlan` *vlan-id* | Enter to configuration vlan mode
`show vlan/ show vlan brief` | Lists each VLAN and all interfaces assigned to that VLAN but does not include trunks
`switchport mode trunk/access` |  Set the interface  link type as a trunk or access
`show interfaces trunk` |  Displays information about the operational trunks along with their VLANs
`switchport trunk encapsulation dot1q` | 	Sets the 802.1Q encapsulation on the trunk port
`switchport voice vlan <vlan id>` | Configures a voice VLan 

 
 
 # RIP Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
 `router rip` | Enters RIP configuration mode
 `version 2` | RIP version 2 
 `no auto-summary` | Modifys the default RIPv2 behavior of automatic summarization
 `show ip rip database` | Displays the contents of the RIP routing database
 `debug ip rip` | Enables RIP debugging

 
 
 # EIGRP Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
 `router eigrp <Autonomous system number> ` | Enters EIGRP config mode 
 `eigrp router id` | Configures EIGRP router ID
 `no auto-summary ` | Modifys the default EIGRP behavior of automatic summarization
 `show ip eigrp neighbors` |  Disables EIGRP neighbors 
 
 
 # OSPF Configuration Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
 `router ospf ` *number* | Enters OSPF config mode
 `passive-interface` *interface* | Stops sending 'Hello' messages of the specified interface
 `router-id` *number* | Sets an OSPF router ID in ip format 
 `clear ip ospf` | Rests OSPF
 `auto-cost bandwidth` *megabits per second* | Change the refrence bandwidth
 `ip ospf cost`  *cost*| Manually configure the OSPF cost 
 `ip ospf [process-id] area [area]`  | Activates OSPF on an interface
 `ip priority [Priority]` | Changes the OSPF interface priority 
 `ip ospf process` | Rests the OSPF process
 `ip ospf network` *type* | Manually configure the network type 
 `ip ospf database` |  Displays the contents of the OSPF routing database
 `bandwidth` *<bandwidth in kilobits>* | Changes the interface bandwidth 
 `show ip interface ospf` *brief* | Disables each OSPF-enabled interface
 `show ip ospf interface`  *interface* |  Displays the specified OSPF interface
 `show ip ospf neighbor` | Disables OSPF neighbors 
 

# HSRP Configuration Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
 `standby` *group number* | Configures HSRP
 `standby version 2` | HSRP version 2 
 `standby <group number> ip` *IP address* | Configures the virtual IP address
 `standby <group number> priority` *value* | Manually configure the active router
 `standby <group number> preempt` | Enables preemption
 `show standby` | Displays global information for HSRP
 
 

# STP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `spanning-tree portfast` | Enables portfast
 `spanning-tree portfast bpdguard default` | Enables BPDU Gurad on all portfast interfaces
 `spanning-tree bpdguard enable` | Enbales BPDU Gurad 
 `spanning-tree mode` *mode* | Configures  STP mode
 `spanning-tree vlan <vlan number> root primary` | Configures the root bridge
 `spanning-tree vlan <vlan number> root secondary` | Configures the secondary root bridge
 `show spanning-tree` | Displays global information for STP

# CDP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `cdp run` | Enables cdp 
 `cdp enable` | Enables cdp
 `show cdp` | Displays global information for CDPDisplays global information for LLDP
 `show cdp neighbors` |  Displays all CDP neighbors

# LLDP Configuration Commands 
| Command  | Purpose | 
 |:----------:|:-------------:|
 `lldp run` | Enables LLDP 
 `show lldp` | Displays global information for LLDP
 `show lldp neighbors` | Displays the list of LLDP neighbors
 `show lldp neighbors detail` | Displays more details from the list of LLDP neighbors

 
# Clock & NTP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `clock set hh:mm:ss {day/month} {month/day} year` | Manually configure the software clock 
 `calendar set hh:mm:ss {day/month} {month/day} year` | Manually configure the hardware clock 
 `clock timezone  <name of time zone> [minuits-offest]` | Configures the timezone 
 `clock update calendar` | Synchronizes the hardware to the software's time 
 `clock read calender` | Synchronizes the software to the calender's time
 `clock summer-time reccuring <name> <start> <end> [offest]` | Automatically configure summer time
 `ntp server <IP>` | Configures ntp server
 `ntp master` [number] | Manually configure an device to act like an ntp sever
 `ntp peer <IP address>` | Symmetric active mode 
 `ntp authenticate` | Enable NTP authentication
 `ntp authentication-key <key number> md5 <key>` | Create the authentication key(s)
 `ntp trusted-key <key-number>` | Specified which key(s) is trusted
 `show clock` | View the time 
 `show clock detail` | View the time source of the device 
 `show calendar` | View the calendar 
 `show ntp status` | View the ntp status
 `show ntp associations` | View all the servers you configured 


# DNS  Configuration Commands 
### Windows Commads
| Command  | Purpose | 
|:----------:|:-------------:|
`ipconfig /displaydns` | View the DNS cache
`ipconfig /flushdns` | Clears the DNS cache 
### IOS Commands
| Command  | Purpose | 
|:----------:|:-------------:|
`ip dns server` | Configures a router as a DNS server 
`ip host <host> <IP address>` | Configures a list of mappings 
`ip name-server <IP address>` | Configures an external DNS server
`ip domain-name` *name* | Conﬁgures a DNS domain name 
`ip domain lookup` | Enables DNS lookup
`show hosts` | Disables the configured and learned hosts 
 

 # DHCP Configuration Commands
 ### Windows Commads
 | Command  | Purpose | 
|:----------:|:-------------:|
 `ipconfig /release` | Releases the DHCP learned IP address
 `ipconfig /renew` | Gets an IP address from a DHCP server
 
 ### IOS Commands
  | Command  | Purpose | 
|:----------:|:-------------:|
`ip dhcp excluded-address <low-address> <high-address>` | Specifies IP addresses that a DHCP server should not assign to DHCP clients
`ip dhcp pool` *name* | Creates a DHCP pool / Entres DHCP config mode
`network <network-number> <mask>` | Configures the network number and mask for a DHCP address pool 
`default-router <address>` | Specifies the default router list for a DHCP client
 `lease` *days* *hours* *minuts*| Configures the lease time 
 `lease infinit` | 
 `show dhcp biding` | Displays all of the DHCP clients
 `ip helper-address` *address* | Configure a DHCP relay-agent
 `ip address dhcp` | Configures a DHCP client 


# SNMP Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
`snmp-server contact` *contact* | Configures contact infomation 
`snmp-server location` *location* | Configures the location of the SNMP server
`snmp-server community <string> ro`| Configures the community strings (read only)
`snmp-server community <string> rw` |  Configures the community strings (read/write)
`snmp-server host <host> version 2c <string>` | Configures the NMC address
`snmp-server enable traps snmp linkdown linkup` | 
`snmp-server enable traps config` | 

 # SYSLOG Commnads
  | Command  | Purpose | 
|:----------:|:-------------:|
 `logging console` *level* | Configures logging to the console line 
 `logging monitor` *level key-word* | Configures logging to the VTY lines
 `logging buffered ` *size* *level*  | Configures logging to the buffer
 `logging <server-ip>`/ `logging host <server-ip>` | Configures logging to an external server
 `logging trap <level>` | Limits messages that are logged to the syslog servers based on severity
 `logging synchronus` | Prevents every logging output from immediately interrupting the console session
 `terminal monitor` | Sends a copy of all syslog messages to Telnet or SSH 
 `service timestamps log` *datetime* / *uptime* | Enables timestamps
 `service squence-numbers` | Enable squence numbers
 
 # Console Port Security Commands
  | Command  | Purpose | 
|:----------:|:-------------:|
 `line console 0` | Enters console configuration mode
 `passowrd <passowrd>`  | Sets up a passowrd
 `login` | Requires a user to enter the passowrd to access the CLI 
 `login local` | login with the username
 `exec-timeout <minuits> <seconds>` | Log out after a certain period of incativity 

 
 # SHH Commands 
   | Command  | Purpose | 
|:----------:|:-------------:|
 `crypto key generate rsa` | Creates the keys that are required by SSH
 `ip ssh version 2` | Restricts SSH version 2 only 
 `ip domain name <name>` | Configures a domain name 
 `tranport input ssh` | Limits connection to SSH only 
 `show ip ssh` | Shows if SSH is enabled or not 
 `line vty 0 15` | Access all VTY lines
 
 
 # FTP & TFTP Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
 `ip ftp username <username>` | Configures a username 
 `ip ftp password <pasword>` | Configures a passowrd
 `copy ftp: flash:` |  Copies files from a FTP server the device flash
 `copy tftp: flash:` | Copies files from a TFTP server the device flash
 `boot system flash <file name>` | Configures the new IOS
 `delete flash:<file name>` | Deletes a file
 `show file systems` | View the file systems on a CISCO IOS 
 `show flash` | View the contents of flash
 
 
 # NAT Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
 `ip nat` *inside* / *outside* | Designatea an inside or outside interface
 `ip nat inside source <inside local ip> <inside global ip>` |  Configures the one-to-one ip mappings
 `ip nat inside source list <acess-list> pool <pool-name>` | Configures dynamic NAT by mapping to the ACL pool
 ` ip nat inside source list <acess-listacess-list> pool <pool-name> overload` | Configures PAT
 `ip nat inside source list <acess-list> interface <interface> overload` | Configures PAT
 `show ip nat translations` | 
 `show ip nat statistics`
 `clear ip nat translation *` | Clears the NAT translation table 

 
# Port security Commands
  | Command  | Purpose | 
|:----------:|:-------------:|
 `switchport port-security` | Enables port security
 `switchport port-security mac-address <mac address>` |  Adds a MAC address to the list of secure MAC addresses
 `switchport port-security aging time <minutes / inactivity>` | Configures the aging time 
 `switchport port-security violation <shutdown / restrict / protect>` |  Sets the action to be taken when a security violation is detected
 `switchport port-security maximum maximum` | Sets the maximum number of secure MAC addresses on the port
 `switchport port-security mac-address sticky` | Enables sticky secure mac address 
 `switchport port-security mac-address sticky <mac address>` | Configures a sticky mac address
 `errdisable recovery cause psecure-violation` | Re-enables an interface
 `show port-security interface <interface>` | Displays information about security options configured on the interface

 
 # DHCP Snooping Commands 
   | Command  | Purpose | 
|:----------:|:-------------:|
 `ip dhcp snooping` | Enables DHCP snooping globally
 `ip dhcp snooping vlan <vlan-num>` | Enables DHCP snooping on the specified VLan 
 `ip dhcp snooping trust` | Configures an interface as a trusted port 
 `ip dhcp snooping rate limit rate <packets per second>` | Configures DHCP rate limitation
 `errdisable recovery cause dhcp-rate-limit` | Enables  errdisable recovery for DHCP rate limiting
 `no ip dhcp snooping information option` | Disables DHCP option 82 
 `show ip dhcp snooping biding` | 
 
 
# DAI Configuration
   | Command  | Purpose | 
|:----------:|:-------------:|
 `ip arp  inspection vlan <vlan-num>` | Enables DAI
 `ip arp inspection trust` | Configures an interface as a trusted port 
 `ip arp inspection validate <dst-mac / src-mac / ip>` |
 `ip arp inspection limit rate ` | Configures DAI rate limiting
 `errdiable recovery cause arp-inspection` | Manually re-enable disabled interfaces
 `show ip arp inspection` | Displays the summury of the DAI configuration
