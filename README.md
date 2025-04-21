# Planning
## Server Specs
- Corsair 200R case
- Gigabyte B85M-D3H Motherboard
- Intel(R) Core(TM) i5-4590 CPU @ 3.30GH
- Nvidia GeForce 960 GPU
- 2x 250GB Samsung SATA SSD
- 1x 1TB HDD
## Proxmox - 192.168.50.2
- Proxmox 8.4 VE in ZFS Mirror(Raid1) x2 250GB SSD
- Shared Proxmox boot os and VM/CT store
- 1TB HDD for Data store

## Pi Hole w/Unbound - 192.168.50.129
- Raspberry Pi 4B w/ 32GB micro SSD
- DietPi OS
- Install Pi-Hole 
  `curl -sSL https://install.pi-hole.net | bash`
- Configure ASUS gateway to use Pi hole as DNS https://www.asus.com/support/faq/1046062/
- Setup clients to use Pi Hole DNS server if not automatically being routed
- Install Unbound
  `sudo apt install unbound`
- Configure Unbound https://docs.pi-hole.net/guides/dns/unbound/
- Set Unbound address as upstream DNS server on Pi Hole admin page  
  ![image](https://github.com/user-attachments/assets/91d00f39-6e84-4599-b8e5-ca3cb42add2d)

