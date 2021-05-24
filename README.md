# vEOS-on-CML
Throwing up a sample node and image definition as they were so hard to find

[Original Source](https://community.cisco.com/t5/cisco-modeling-labs-discussions/arista-veos-on-cml/m-p/4095542#M567)

## Notes for MLAG setups
EOS expects that the second least significant bit, in the first octet of the OUI - the U/L bit, is set to 0. For the purposes of MLAG peering, EOS will then set this bit to 1, indicating *locallly administered*. 

This generally causes issues in KVM-based setups, as KVM tends to have the base mac configured with something that has the U/L bit set to 1.
