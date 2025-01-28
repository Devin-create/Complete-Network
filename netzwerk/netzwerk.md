# Eigenes Netzwerk

## Arbeitsunterteilung
- Jonathan: Switch & Router konfigurieren
- Minel: Switch & Router konfigurieren
- Giacomo: Clients konfigurieren, aufsetzen 
- Kian: Clients konfigurieren, aufsetzen
- Devin: Dokumentieren
- Access Point
- 1 Switch
- X Ethernet Kabel
- DHCP Server

## Adressierung Geräte

| Device        | IP Address    | Subnet Mask    | Gateway     | DNS Server    |
|--------------|--------------|---------------|-------------|--------------|
| **Router**   | 172.16.1.1    | 255.255.255.0 | *N/A*          | *N/A*          |
| **Linux Server** | 172.16.1.10  | 255.255.255.0 | 172.16.1.1  | 172.16.1.10  |
| **Linux Host**   | DHCP  | 255.255.255.0 | 172.16.1.1  | *N/A*  |
| **Windows Host** | DHCP | 255.255.255.0 |  172.16.1.1 | *N/A* |


## Namenskonvention
### Überbegriffe:   1   2§
- ap: Accesspoint 
- sw: Switch
- rt: Router
- pc: Personal Computer / Client
- ds: DHCP Server

### Geräte

- rt01: router
- pc01: Linux Server
***

## IP-Netzwerk
- Klasse B Netzwerk
- 172.16.x.x
- 255.255.255.0 Maske
- 3 Clients
- 1 Router
- 1 Ac
- pc02: Linux Host
- pc03: Windows Host
- sw01: Switch
- ds01: DHCP-Server
- ap01: Accesspoint
  
***
w

## Dokumentation

1. Als Erstes erstellten wir einen Plan, aufgeteilt in einem Netzwerkplan, als auch eine Tabelle, welches die Adressierung visualisiert.  
2. Zunächst hatten wir die All-In-One PCs aufgesetzt und die OS (2x Linux, 1x Windows) neu eingebunden. Dies hatten wir mithilfe eines bootfähigen Stick gemacht, nach dem wir im Bios die Startreihenfolge für das Booten über den Stick geändert hatten. Anschliessend wurden die IPs auf diesen Clients bestummen. 2 wurden mittels DHCP adressiert, und die Adresse für den Ubuntu Server wurde manuell vergeben.
3. Zeitgleich hatten wir auf dem Router NAT eingestellt, und die IP-Adressen modifiziert.
4. Danach installierten wir einen Webserver. Dafür wurde NGINX verwendet. Anschliessend war das Ziel, den Wochenbericht über FTP von dem Laptop auf den Server zu transferieren. Dabei mussten auch Berechtigungen für das transferieren geändert werden.