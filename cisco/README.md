# Intro to Cisco devices (routers or switches)

The Internetworking Operating System[2] (IOS) is a family of proprietary network operating systems used on several router and network switch models manufactured by Cisco Systems. The system is a package of routing, switching, internetworking, and telecommunications functions integrated into a multitasking operating system. Although the IOS code base includes a cooperative multitasking kernel, most IOS features have been ported to other kernels, such as Linux and QNX, for use in Cisco products.

Not all Cisco networking products run IOS. Exceptions include some Cisco Catalyst switches, which run IOS XE, and Cisco ASR routers, which run either IOS XE or IOS XR; both are Linux-based operating systems. For data center environments, Cisco Nexus switches (Ethernet) and Cisco MDS switches (Fibre Channel) both run Cisco NX-OS, also a Linux-based operating system.

## Ansible Modules

To see all the modules available: [Collections in the Cisco Namespace](https://docs.ansible.com/ansible/latest/collections/cisco/index.html)

* Cisco IOS devices: [Ansible Network Collection for Cisco IOS devices.](https://docs.ansible.com/ansible/latest/collections/cisco/ios/index.html#plugins-in-cisco-ios)
* Cisco IOS XE devices:
* Cisco IOS XR devices: [Ansible Network Collection for Cisco IOSXR devices.](https://docs.ansible.com/ansible/latest/collections/cisco/iosxr/index.html#plugins-in-cisco-iosxr)
* Cisco NS-OS devices: [Ansible Network Collection for Cisco NXOS devices.](https://docs.ansible.com/ansible/latest/collections/cisco/nxos/index.html#plugins-in-cisco-nxos)

## Upgrading IOS on Cisco Devices

*NOTE: https://www.cisco.com/c/en/us/td/docs/routers/C8000V/Configuration/c8000v-installation-configuration-guide/m_upgrading_c8000v.html#con_1115789*

Be sure to thoroughly test and verify automation processes before involving production resources.

Upgrading IOS on Cisco devices typically involves these steps, each of which can be automated with Ansible:

- Gather information (facts).
- Obtain an updated image and copy it to device flash.
- Set the device to boot from the new image.
- Ensure that the running configuration is saved and backed up.
- Reload the device.
- Verify connectivity and functionality when the boot sequence finishes.