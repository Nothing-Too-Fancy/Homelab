## Server Specs
- Corsair 200R case
- Gigabyte B85M-D3H Motherboard
- Intel(R) Core(TM) i5-4590 CPU @ 3.30GH
- Nvidia GeForce 960 GPU
- 2x 250GB Samsung SATA SSD
- 3x 14TB HDD
## [[Proxmox]] - 192.168.50.2
- Proxmox 8.4 VE in ZFS Mirror(Raid1) x2 250GB SSD
- Shared Proxmox boot OS and VM/CT store
- 14TB HDD in Raid1Z (Raid 5) for Data store
## [[Pi Hole]] w/Unbound - 192.168.50.129
- Raspberry Pi 4B w/ 32GB micro SSD
- DietPi OS
- Install Pi-Hole 
  `curl -sSL https://install.pi-hole.net | bash`
- Configure ASUS gateway to use Pi hole as DNS https://www.asus.com/support/faq/1046062/
- DHCP reserve 192.168.50.129
- Setup clients to use Pi Hole DNS server if not automatically being routed
- Install Unbound
  `sudo apt install unbound`
- Configure Unbound https://docs.pi-hole.net/guides/dns/unbound/
- Set Unbound address as upstream DNS server on Pi Hole admin page  
  ![image](https://github.com/user-attachments/assets/91d00f39-6e84-4599-b8e5-ca3cb42add2d)

	

## [[PiVPN]] - 192.168.50.129
- Same Raspberry Pi as PiHole
- Install PiVPN
  `curl -L https://install.pivpn.io | bash`
- Install as Wireguard
- Port forward static IP:51820 UDP

## [[Syncthing]] - 192.168.50.200 (Proxmox Container CT100)
- Used as a central point to sync files across devices
- default admin port 8384

## [[Active Directory]] [[Domain Controller]] (Proxmox VM 101)
