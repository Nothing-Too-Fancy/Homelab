# Planning
## Server Specs
- Corsair 200R case
- Gigabyte B85M-D3H Motherboard
- Intel(R) Core(TM) i5-4590 CPU @ 3.30GH
- Nvidia GeForce 960 GPU
- 2x 250GB Samsung SATA SSD
- 1x 1TB HDD
## Proxmox
- Install Proxmox 8.2 VE iso on one 250GB SSD - USB Imager
- Install live VMs on second 250GB SSD
- Backup VMs and Isos on HDD

## Pi Hole w/Unbound
- Raspberry Pi 4B w/ 32GB micro SSD
- DietPi OS
- Install Pi-Hole 
  `curl -sSL https://install.pi-hole.net | bash`
- Configure ASUS gateway to use Pi hole as DNS https://www.asus.com/support/faq/1046062/
- Setup clients to use Pi Hole DNS server if not automatically being routed
- Install Unbound
  `sudo apt install unbound`
- Configure Unbound https://docs.pi-hole.net/guides/dns/unbound/
