..
  Copyright (c) Ansible Project
  GNU General Public License v3.0+ (see LICENSE or https://www.gnu.org/licenses/gpl-3.0.txt)
  SPDX-License-Identifier: GPL-3.0-or-later

.. _ansible_collections.community.openwrt.docsite.howto_guide:


Community OpenWrt How-To Guide
==============================

Welcome to the Community OpenWrt How-To Guide! This is a collection of recipes that will help you
using the ``community.openwrt`` role in real world scenarios.

Most OpenWrt devices have a very small footprint and there is no space available to install Python. Based on this constraint, virtually all of the standard Ansible modules are not available.

It is a design rule of ``community.openwrt`` not to require Python, rather providing modules based on shell scripts (``/bin/sh``) instead.

Also by the nature of OpenWrt and its CLI-based ``uci`` tool, you need to be very familiar how
this ecosystem works. Even the creation of a Wifi passwort or a simple forwarding rule can
be challenging.

Below is a list of topics we intend to write How-To documents about. The ones that are not linked to another page are to be considered To-Be-Done (TBD), and they should be added incrementally. Contributions are welcome!

Initial Setup
^^^^^^^^^^^^^

Real Hardware
"""""""""""""

 - Consult the official hardware guide at <https://openwrt.org/toh/start>.
 - Ensure the device is flashed with a compatible OpenWrt firmware image.
 - Default configurations define separate WAN and LAN interfaces; wireless is disabled by default.
 - LAN interfaces typically have an active DHCP server enabled.
 - The LuCI web interface is accessible at `http://192.168.1.1`.

**Note**: Single-interface hardware (e.g., Raspberry Pi) typically defaults the Ethernet port to the LAN zone.
Establishing WAN connectivity requires configuring the onboard WiFi or a USB network adapter.
Be aware that USB adapters often require drivers missing from the base image; bootstrapping initial connectivity
for such hardware is an advanced topic and beyond the scope of this guide.

Verify connectivity via ping, LuCI, or SSH at ``192.168.1.1`` (default: ``root`` / no password).
Consult the OpenWrt documentation for further device-specific instructions.

VM as a router on a hypervisors (Proxmox as exa)
"""""""""""""""""""""""""""""""""""""""""""""""""

- TBD


SSH Installation
^^^^^^^^^^^^^^^^

- Bootstrap
- Initial SSH Key Installation


SSL Certificates
^^^^^^^^^^^^^^^^

- redirect http to https
- acme support
- Install existing ssl certificates


Wifi Setup
^^^^^^^^^^

- 2Ghz / 5Ghz
- Passwords
- Additional Guest Network + isolation


VPN
^^^

- Wireguard Server
- Wireguard Client
- NordVPN or similar
- Netbird
- Tailscale
- Tinc


Advanced networking
^^^^^^^^^^^^^^^^^^^

- VLAN
- VLAN per Hardware Port
- Routing
- Firewall, Port forwarding


Hardware
^^^^^^^^

- Configure the hardware button do do cool things
- Configure the LEDs


Firmware Update
^^^^^^^^^^^^^^^

- CLI / UI Tool installation


Backup/Restore
^^^^^^^^^^^^^^

- Backup
- Restore
- Crontab
