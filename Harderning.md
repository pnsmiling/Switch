```python
service timestamps debug datetime msec localtime show-timezone
: This command adds a timestamp with milliseconds and the local time zone to debug messages.

service timestamps log datetime msec localtime show-timezone
: This command adds a timestamp with milliseconds and the local time zone to log messages.

no ip http server
: This command disables the HTTP server, preventing access to the device's configuration via HTTP.

no ip http secure-server
: This command disables the HTTPS server, preventing secure access to the device's configuration via HTTP.

cdp run
: This command enables Cisco Discovery Protocol (CDP), allowing the device to discover and share information with neighboring Cisco devices.

lldp run
: This command enables Link Layer Discovery Protocol (LLDP), which is an industry-standard protocol for network devices to exchange information about their identities and capabilities with neighbors.

no ip domain lookup
: This command disables DNS lookups on the device, which can speed up command entry if DNS resolution is slow.

no ip source-route
: This command disables the use of source routing, which can be a security risk.

no ip bootp server
: This command disables the BOOTP server functionality, used for assigning IP addresses to network devices during boot-up.

service password-encryption
: This command encrypts passwords in the device's configuration to enhance security.

no tftp-server flash
:<name of loss.bin: This command removes the TFTP server configuration for the specified file from the flash memory.

no tftp-server flash:vlan.dat
: This command removes the TFTP server configuration for the VLAN database file from flash memory.

no tftp-server nvram:startup-config hostname (config)
: This command removes the TFTP server configuration for the startup configuration file stored in the NVRAM.

no tftp-server nvram:private-config
: This command removes the TFTP server configuration for the private configuration file stored in NVRAM.

no ip tftp source-interface Vlan100
: This command removes the TFTP source interface configuration for VLAN 100.

enable secret security
: This command sets an encrypted enable secret password for privileged mode access.

username manulife privilege 15 secret 5 $151H29$2010qNKUjjSOnFJwwCAl
: This command creates a local user account with the username "manulife," assigns it privilege level 15 (full access), and sets an encrypted password.
```
```python
vtp mode transparent
vtp version 2
vtp domain MFC-VN

The above commands configure the VLAN Trunking Protocol (VTP) mode as "transparent," meaning the switch does not participate in VTP updates and doesn't synchronize VLAN configurations with other switches. Then, it creates several VLANs with specific names and VLAN IDs for different purposes in the network.
```
