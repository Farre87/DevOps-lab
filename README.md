# DevOps-Lab

Ett automatiserat infrastrukturprojekt byggt med Vagrant, Ansible och VirtualBox.

## Beskrivning

Detta projekt bygger en komplett IT-infrastruktur med 4 virtuella maskiner:

- **control** - Ansible kontrollnod (192.168.56.20)
- **webserver** - nginx webbserver med HTTPS (192.168.56.21)
- **database** - PostgreSQL databasserver (192.168.56.22)
- **client** - Testklient (192.168.56.23)

## Tekniker och verktyg

- Vagrant - Automatisk skapning av VM:ar
- VirtualBox - Virtualisering
- Ansible - Konfigurationsautomation
- nginx - Webbserver med HTTPS
- PostgreSQL - Databas
- UFW - Brandvagg
- OpenSSL - CA certifikat och HTTPS
- SSH - Sakra anslutningar med nyckelpar

## Sakerhet

- UFW brandvagg pa alla servrar
- Endast port 22 (SSH) oppet pa alla servrar
- Port 80 och 443 oppet pa webservern
- Port 5432 endast tillganglig fran control
- HTTPS med CA-signerat certifikat
- SSH-nyckelbaserad autentisering
