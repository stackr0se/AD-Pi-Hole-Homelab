**Goal:** Installing Proxmox on my very old closet pc. Be able to connect it to my thinkpad laptop instead of using the vga monitor. 

## Steps
1. **BIOS Configuration:** Accessed BIOS (F10) and enabled Intel VT-x and VT-d for virtualization support. Set "After Power Loss" to "Power On" to ensure the headless server automatically recovers from power outages.
2. **Media Creation:** Flashed the Proxmox VE ISO to a USB drive via ThinkPad (Arch Linux).
3. **Installation:** Booted the HP PC from USB, wiped the internal drive, and installed Proxmox. 
4. **Network Configuration:** Assigned a static IP (`192.168.0.50`) outside the DHCP scope of the CenturyLink gateway to ensure reliable management access.
5. **Headless Migration:** Disconnected the physical monitor, keyboard, and mouse. All management is now conducted remotely via the web UI (`https://192.168.0.50:8006`).

## Notes
When logging in, the user name is "root" not your email address.
## Result
Proxmox is successfully running headless and accessible via the management laptop.

![Proxmox Dashboard](../screenshots/01-proxmox-dashboard.png)
