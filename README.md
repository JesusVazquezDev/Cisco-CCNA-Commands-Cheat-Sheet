# Cisco-Commands-Cheat-Sheet

# Basic Commands

| Command  | Purpose | 
|:----------:|:-------------:|
`config t` or `configure terminal` | Enter configuration mode
`copy` *from-location to-location* | copie a file (or set of files) from one location to another
`copy running-config startup-config` | It saves the configuration when the device reloads, it loads the latest configuration file
`copy startup-config running-config` | Saves the startup configuration into the running configuration
 `description` *<name-string>* | Set a description to the interface
 `duplex` *<auto / full / half>* |	Sets the interface duplex
 `enable`| Enter privilege mode | 
 `enable secret` *<password>* | Enables secret passwords hashed with the MD5 algorithm
`exit` / `end` | Return to previous mode 
`hostname` *name* | Sets a host name to the current Cisco network device
`interface` *fastethernet/number* | Enters interface configuration mode for the specified fast ethernet interface
`ip domain-lookup` | Enables domain lookup service
`ip default-gateway` *<ip address>* | Sets the default gateway for the router
 `line` | Enter line configuration mode
`logout`/ `disable` | 	Exit User mode
 `no shutdown` | turns up the interface
 `ping` *<target IP / hostname>* | Diagnoses basic network connectivity
 `reload` | 	Reboot the device
`show ip route` | Display the current state of the routing table
`shutdown` |  Shuts down the interface
 `speed` <10 / 100 / 1000 / auto> | Sets the speed of an interface or configure it as auto
 `show interface status` | Displays the interface line status
 `show mac address-table` | Displays the MAC address table
 `show interfaces switchport` | 	Displays configuration settings about all the switch port interfaces
 `switchport mode access` | 	In the interface configuration mode, the command assigns the interface link type as an access link
 `show vtp status` |  Displays all vtp status
 `write erase` / `erase startup-config` | Deletes the startup config
 
 # Basic show Commads
 | Command  | Purpose | 
 |:----------:|:-------------:|
 `show running-config` | Display the current configuration
 `show startup-config` | Display the configuration at startup
 `show interfaces` | Displays detailed information about interface status
 `show ip protocols` | 
 `show ip interface` |  Displays the status for each interface
 `show ip interface brief` | 
 `show ip route` |



 
# Vlan Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
`vlan` *vlan-id* | Enter to configuration vlan mode
`show vlan/ show vlan brief` | Lists each VLAN and all interfaces assigned to that VLAN but does not include trunks


 
 
 # RIP Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
 `router rip` | Enter RIP configuration mode
 `version 2` | RIP version 2 
 `no auto-summary` | Modify the default RIPv2 behavior of automatic summarization
 `show ip rip database` | Displays the contents of the RIP routing database

 
 
 # EIGRP Configuration Commands 
  | Command  | Purpose | 
|:----------:|:-------------:|
 `router eigrp <Autonomous system number> ` | Enter EIGRP config mode 
 `eigrp router id` |
 
 
 # OSPF Configuration Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
 `router ospf ` [*number*] | Enter OSPF config mode
 `passive-interface` [interface] | Stop sending 'Hello' messages of the specified interface
 `router-id` <number> | Set an OSPF router ID in ip format 
 `clear ip ospf` | Rest OSPF
 `auto-cost bandwidth` *megabits per second* | Change the refrence bandwidth
 `ip ospf cost`  *cost*| Manually configure the OSPF cost 
 `ip ospf [process-id] area [area]`  | Activate OSPF on an interface
 `ip priority [Priority]` | Change the OSPF interface priority 
 `ip ospf process` | Rest the OSPF process
 `ip ospf network` *type* | Manually configure the network type 
 `bandwidth` *<bandwidth in kilobits>* | Change the interface bandwidth 
 `show ip interface ospf` *brief* | Disable each OSPF-enabled interface
 `show ip ospf interface`  *interface* | 
 `show ip ospf neighbor` | Disable OSPF neighbors 
 `switchport mode trunk` |  Set the interface  link type as a trunk link 
 `show interfaces trunk` |  Displays information about the operational trunks along with their VLANs


 
 

# STP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `spanning-tree mode rapid-pvst` | Configures the device for Rapid Per VLAN Spanning Tree protocol
 `show interfaces trunk` |  Displays information about the operational trunks along with their VLANs

# CDP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `cdp run` |
 `cdp enable` |
 `show cdp` | Shows whether CDP is enabled globally
 `show cdp neighbors` |  Displays all CDP neighbors

# LLDP Configuration Commands 
| Command  | Purpose | 
 |:----------:|:-------------:|
 `show lldp` | Displays global information for LLDP
 `lldp run` | 

 
# Clock & NTP Configuration Commands 
| Command  | Purpose | 
|:----------:|:-------------:|
 `clock set hh:mm:ss {day/month} {month/day} year` | Manually configure the software clock 
 `calendar set hh:mm:ss {day/month} {month/day} year` | Manually configure the hardware clock 
 `clock timezone  <name of time zone> [minuits-offest]` | Configure the timezone 
 `clock update calendar` | Synchronize the hardware to the software's time 
 `clock read calender` | Synchronize the software to the calender's time
 `clock summer-time reccuring <name> <start> <end> [offest]` | Automatically configure summer time
 `ntp server <IP>` | Configure ntp server
 `ntp master` [number] | Manually configure an device to act like an ntp sever
 `ntp peer <IP address>` | Symmetric active mode 
 `ntp authenticate` | Enable NTP authentication
 `ntp authentication-key <key number> md5 <key>` | Create the authentication key(s)
 `ntp trusted-key <key-number>` | Specified which key(s) is trusted
 `ip nat` *<inside / outside>* | It designate whether the interface is the inside or outside of NAT
 `show clock` | View the time 
 `show clock detail` | View the time source of the device 
 `show calendar` | View the calendar 
 `show ntp status` | View the ntp status
 `show ntp associations` | View all the servers you configured 
 
 
 
 # DNS Configuration Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
  `ip dns server` | Enables DNS service
  `dns-server` *<IP address>* | Sets the DNS server IP address for the DHCP clients


 # SYSLOG Configuration Commands 
 | Command  | Purpose | 
|:----------:|:-------------:|
`show logging` |  Displays the state of system logging (syslog) and the contents of the standard system logging buffer
 `logging` <*ip address*> | Determines the Syslog server to send log messages


 
