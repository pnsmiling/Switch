```pyhon
UDLD Configuration:
udld aggressive
: Globally enables UDLD in aggressive mode,
 which actively detects unidirectional links
and puts the interface into the errdisable state
 if such a link is detected.

udld message time 10
: Sets the UDLD message interval to 10 seconds,
 which is the time interval between UDLD protocol packets.

Spanning Tree Configuration:
spanning-tree mode rapid-pvst
: Configures the Spanning Tree Protocol to use Rapid
Per-VLAN Spanning Tree (Rapid-PVST) mode, providing
faster convergence for each VLAN.

spanning-tree loopguard default
: Enables Loop Guard on all ports that are not in a
PortFast or an EtherChannel operational state.
Loop Guard helps prevent potential bridging loops
caused by unidirectional links.

spanning-tree portfast bpduguard default
: Enables BPDU Guard on all PortFast-enabled ports
. BPDU Guard disables the port if it receives a BPDU, helping to prevent loops.

Port-channels Configuration:
interface Port-channel #
: Configures a Port-channel interface.
Replace "#" with the desired port-channel number.

description Connect to Switchostname - Manulife Monitor
: Provides a description for the Port-channel interface.

switchport
: Enables Layer 2 switching on the interface.

switchport mode trunk
: Sets the interface to trunk mode, allowing
 it to carry traffic for multiple VLANs.

switchport trunk allowed vlan xx
: Specifies which VLANs are allowed on the trunk
. Replace "xx" with the desired VLAN numbers.
```
```python
Trunk Ports Configuration:
interface TenGigabitEthernetx/x/X
: Configures a Ten Gigabit Ethernet interface.
 Replace "x/x/X" with the desired interface number.

description Connect to Switchostname_Portinfo - Manulife Monitor
: Provides a description for the Ten Gigabit Ethernet interface.

switchport
: Enables Layer 2 switching on the interface.

switchport mode trunk
: Sets the interface to trunk mode, allowing it to carry traffic for multiple VLANs.

switchport trunk allowed vlan xx
: Specifies which VLANs are allowed on the trunk.
 Replace "xx" with the desired VLAN numbers.

channel-group # mode active
: Adds the interface to a port-channel group.
Replace "#" with the desired port-channel number,
 matching the previously configured Port-channel interface.
```
```python

```
