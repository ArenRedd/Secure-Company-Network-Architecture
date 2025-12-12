# HSRP Failover Test

This document describes the HSRP failover test.

## Test Plan

1. Start a continuous ping from a PC to its default gateway.
2. Shut down the interface on the active core switch that connects to the PC's VLAN.
3. Verify that the standby core switch takes over and the ping is successful.

## Expected Result

- The ping should drop a few packets and then resume.
- The standby router should become the active router.
