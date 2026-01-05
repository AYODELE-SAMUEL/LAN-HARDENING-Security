 Definition
Port security is a LAN switch security feature that limits the number of MAC
addresses allowed on a switch port.

## Objectives
- Prevent unauthorized access
- Protect the network from MAC flooding
- Improve LAN security

## Types of Violations
- Protect
- Restrict
- Shutdown

## Conclusion
Port security helps secure LAN environments by controlling device access.


## Network Configuration
## cisco commands
     
Switch> enable
Switch# configure terminal
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
Switch(config-if)# switchport port-security maximum 1
Switch(config-if)# switchport port-security violation shutdown
Switch(config-if)# switchport port-security mac-address sticky
