**ACLs (Access Control Lists) dans la configuration du routeur**

| ACL | Interface | Action | Protocole | Source | Destination | Service |
|---|---|---|---|---|---|---|
| ACL-INV | GigabitEthernet1/0.10 | :heavy_check_mark: | **IP** | 192.168.10.0/24 | 192.168.10.0/24 | Tout |
| ACL-INV | GigabitEthernet1/0.10 | :x: | **IP** | 192.168.10.0/24 | 192.168.0.0/16 | Tout |
| ACL-INV | GigabitEthernet1/0.10 | :heavy_check_mark: | **IP** | 192.168.10.0/24 | 0.0.0.0/0 | Tout |
| ACL-ALL | GigabitEthernet1/0.50 | :heavy_check_mark: | **DNS** | Tout | 192.168.50.0/24 | TCP, UDP |
| ACL-ALL | GigabitEthernet1/0.50 | :heavy_check_mark: | **DHCP** | Tout | 192.168.50.0/24 | UDP |
| ACL-ALL | GigabitEthernet1/0.50 | :heavy_check_mark: | **HTTP** | Tout | 192.168.50.0/24 | TCP |
| ACL-ALL | GigabitEthernet1/0.50 | :heavy_check_mark: | **TFTP** | Tout | 192.168.50.0/24 | UDP |
| ACL-ALL | GigabitEthernet1/0.50 | :heavy_check_mark: | **IP** | 192.168.20.0/24 | 0.0.0.0/0 | Tout |
| ACL-v-ADM | GigabitEthernet1/0.20 | :heavy_check_mark: | **ICMP** | Tout | Tout | Echo Reply |
| ACL-v-ADM | GigabitEthernet1/0.20 | :x: | **IP** | 192.168.30.0/24 | 192.168.20.0/24 | Tout |
| ACL-v-ADM | GigabitEthernet1/0.20 | :x: | **IP** | 192.168.40.0/24 | 192.168.20.0/24 | Tout |
| ACL-v-ADM | GigabitEthernet1/0.20 | :heavy_check_mark: | **TCP, UDP** | 192.168.50.0/24 | 192.168.20.0/24 | Tout |
| ACL-ADM-v-WAN | GigabitEthernet1/0.20 | :x: | **IP** | 192.168.50.0/24 | Tout | Tout |
| ACL-ADM-v-WAN | GigabitEthernet1/0.20 | :x: | **IP** | 192.168.20.0/24 | Tout | Tout |
| ACL-ADM-v-WAN | GigabitEthernet1/0.20 | :x: | **IP** | 192.168.40.0/24 | Tout | Tout |
| ACL-ADM-v-WAN | GigabitEthernet1/0.20 | :heavy_check_mark: | **IP** | Tout | Tout | Tout |
| D_FR_WAN | GigabitEthernet0/0 | :heavy_check_mark: | **ICMP** | Tout | Tout | Echo Reply |
| D_FR_WAN | GigabitEthernet0/0 | :heavy_check_mark: | **IP** | 192.168.0.0/16 | Tout | Tout |
| D_FR_WAN | GigabitEthernet0/0 | :heavy_check_mark: | **IP** | 10.0.0.2 | Tout | Tout |
| D_FR_WAN | GigabitEthernet0/0 | :heavy_check_mark: | **IP** | 10.0.0.3 | Tout | Tout |
| D_FR_WAN | GigabitEthernet0/0 | :x: | **IP** | Tout | Tout | Tout |

**Explication**

* **ACL-INV** permet le trafic IP entre les hôtes du sous-réseau
