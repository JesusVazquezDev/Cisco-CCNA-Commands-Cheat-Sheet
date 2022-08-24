# Cisco-Commands-Cheat-Sheet




:red_circle: ***Commands To Move Between Modes***
| Command  | Purpose | 
|:----------:|:-------------:|
| `enable`| Enter privilege mode | 
`config t` or `configure terminal` | Enter configuration mode
`interface` *fastethernet/number* | Enters interface configuration mode for the specified fast ethernet interface
`line` | Enter line configuration mode
`vlan` *vlan-id* | Enter to configuration vlan mode
`logout`/ `disable` | 	Exit User mode
`exit` / `end` | Return to previous mode 


:red_circle: ***Basic Configuration***

| Command  | Purpose | 
|:----------:|:-------------:|
`hostname` *name* | Sets a host name to the current Cisco network device
`reload` | 	Reboot the device
`copy` *from-location to-location* | copie a file (or set of files) from one location to another
`copy running-config startup-config` | It saves the configuration when the device reloads, it loads the latest configuration file.
