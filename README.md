# Azure Infrastructure as Code – Terraform og Ansible

## Oversikt

Dette prosjektet viser hvordan man kan bruke **Terraform** til å opprette infrastruktur i **Microsoft Azure**, og **Ansible** til å konfigurere en Linux-server.

Oppsettet består av to virtuelle maskiner i samme virtuelle nettverk, men i forskjellige subnett.

- **VM1** fungerer som **Ansible controller**
- **VM2** fungerer som **managed node**

Terraform brukes til å opprette infrastrukturen i Azure, mens Ansible brukes til å konfigurere VM2 fra VM1.

---

# Arkitektur

Terraform oppretter følgende ressurser i Azure:

- Resource Group
- Virtual Network
- 2 Subnets
- 2 Network Security Groups
- Public IP
- 2 Network Interfaces
- 2 Linux Virtual Machines

## Nettverk

Virtual Network:
