# Modul 4
## Praktikum Komunikasi Data & Jaringan Komputer

## Anggota Kelompok 
| Nama    | NRP  |
|---------|------|
| Imam Mahmud Dalil Fauzan  | 5027241100  |
| Zaenal Mustofa | 5027241018  |

## Soal Praktikum
[Link Soal Praktikum](/src/Soal%20Praktikum%20Modul%204%20Komdat%20Jarkom%202025.docx)

## Topologi GNS3
![topologi-gns3](/src/topologi-jarkom-modul4-gns.png)

## Topologi Cisco Packet Tracer (CPT)


## Rute
| Urutan | Subnet (Router)           | Rute                                                                     | Kebutuhan Host (Host + 1 Gateway) | Alokasi Host | CIDR |
|-------|----------------------------|---------------------------------------------------------------------------|------------------------------------|--------------|------|
| 1     | LAN Switch9 (Numenor)      | Amonsul > Eregion > Numenor > Switch9 > Arthedain, Mirdain               | 875                                | 1024         | /22  |
| 2     | LAN Switch6 (Anor)         | Amonsul > Minastir > Anor > Switch6 > Beacon, Silmarils                  | 661                                | 1024         | /22  |
| 3     | LAN Switch8 (Erain)        | Amonsul > Eregion > Numenor > Mordor > Erain > Switch8 > Melkor, Khazad  | 503                                | 512          | /23  |
| 4     | LAN Switch7 (Erain)        | Amonsul > Eregion > Numenor > Mordor > Erain > Switch7 > Balrog, Gothmog, Thranduil | 470               | 512          | /23  |
| 5     | LAN Switch2 (Valinor)      | Amonsul > Fornost > Switch1 > Valinor > Switch2 > Shadow, Anarion, Lindon | 299                               | 512          | /23  |
| 6     | LAN Switch12 (Eregion)     | Amonsul > Eregion > Switch12 > Mirkwood, Morgul                          | 126                                | 128          | /25  |
| 7     | LAN Switch11 (Gudur)       | Amonsul > Eregion > Numenor > Gudur > Switch11 > Palantir, Edhil         | 120                                | 128          | /25  |
| 8     | LAN Switch13 (Morgoth)     | Amonsul > Minastir > Amroth > Switch5 > Morgoth > Switch13 > Erendis, Elrond | 62                             | 64           | /26  |
| 9     | LAN Switch4 (Valmar)       | Amonsul > Fornost > Switch1 > Valmar > Switch4 > Imrahil, Utumno, Gwaith | 34                                | 64           | /26  |
| 10    | LAN Switch3 (Valmar)       | Amonsul > Fornost > Switch1 > Valmar > Switch3 > Dorlath, Arnor          | 28                                 | 32           | /27  |
| 11    | LAN Switch10 (Gudur)       | Amonsul > Eregion > Numenor > Gudur >Switch10 > ironCrown, Grond, Hobbiton | 14                               | 16           | /28  |
| 12    | LAN Throne                 | Amonsul > Minastir > Amroth > Switch5 > Throne > Erebor                  | 3                                  | 8            | /29  |
| 13    | Transit-Switch1            | Amonsul > Fornost > Switch1 (ke Valinor, Valmar)                         | 3                                  | 8            | /29  |
| 14    | Transit-Switch13           | Amonsul > Minastir > Amroth > Switch13 (ke Morgoth, Throne)              | 3                                  | 8            | /29  |
| 15    | WAN 1                      | Amonsul > NAT1                                                            | 2                                  | 4            | /30  |
| 16    | WAN 2                      | Amonsul > Fornost                                                         | 2                                  | 4            | /30  |
| 17    | WAN 3                      | Amonsul > Eregion                                                         | 2                                  | 4            | /30  |
| 18    | WAN 4                      | Amonsul > Minastir                                                        | 2                                  | 4            | /30  |
| 19    | WAN 5                      | Amonsul > Eregion > Numenor                                               | 2                                  | 4            | /30  |
| 20    | WAN 6                      | Amonsul > Eregion > Mordor                                                | 2                                  | 4            | /30  |
| 21    | WAN 7                      | Amonsul > Eregion > Numenor > Gudur                                       | 2                                  | 4            | /30  |
| 22    | WAN 8                      | Amonsul > Eregion > Mordor > Erain                                        | 2                                  | 4            | /30  |
| 23    | WAN 9                      | Amonsul > Minastir > Amroth                                               | 2                                  | 4            | /30  |
| 24    | WAN 10                     | Amonsul > Minastir > Anor                                                 | 2                                  | 4            | /30  |
|       | **TOTAL**                  |                                                                           | **3221**                           | **4096**     | **/20** |


## Pembagian IP - VLSM
| Subnet                       | Network ID       | Netmask (/CIDR)              | Broadcast Address   | Range IP                          |
|------------------------------|------------------|------------------------------|----------------------|------------------------------------|
| LAN-S9 (Numenor)            | 192.242.0.0      | 255.255.252.0 (/22)          | 192.242.3.255        | 192.242.0.1 - 192.242.3.254        |
| LAN-S6 (Anor)               | 192.242.4.0      | 255.255.252.0 (/22)          | 192.242.7.255        | 192.242.4.1 - 192.242.7.254        |
| LAN-S8 (Erain)              | 192.242.8.0      | 255.255.254.0 (/23)          | 192.242.9.255        | 192.242.8.1 - 192.242.9.254        |
| LAN-S7 (Erain)              | 192.242.10.0     | 255.255.254.0 (/23)          | 192.242.11.255       | 192.242.10.1 - 192.242.11.254      |
| LAN-S2 (Valinor)            | 192.242.12.0     | 255.255.254.0 (/23)          | 192.242.13.255       | 192.242.12.1 - 192.242.13.254      |
| LAN-S12 (Eregion)           | 192.242.14.0     | 255.255.255.128 (/25)        | 192.242.14.127       | 192.242.14.1 - 192.242.14.126      |
| LAN-S11 (Gudur)             | 192.242.14.128   | 255.255.255.128 (/25)        | 192.242.14.255       | 192.242.14.129 - 192.242.14.254    |
| LAN-S13 (Morgoth)           | 192.242.15.0     | 255.255.255.192 (/26)        | 192.242.15.63        | 192.242.15.1 - 192.242.15.62       |
| LAN-S4 (Valmar)             | 192.242.15.64    | 255.255.255.192 (/26)        | 192.242.15.127       | 192.242.15.65 - 192.242.15.126     |
| LAN-S3 (Valmar)             | 192.242.15.128   | 255.255.255.224 (/27)        | 192.242.15.159       | 192.242.15.129 - 192.242.15.158    |
| LAN-S10 (Gudur)             | 192.242.15.160   | 255.255.255.240 (/28)        | 192.242.15.175       | 192.242.15.161 - 192.242.15.174    |
| LAN-Throne                  | 192.242.15.176   | 255.255.255.248 (/29)        | 192.242.15.183       | 192.242.15.177 - 192.242.15.182    |
| Transit-Switch13 (Fornost)  | 192.242.15.184   | 255.255.255.248 (/29)        | 192.242.15.191       | 192.242.15.185 - 192.242.15.190    |
| Transit-Switch1 (Amroth)    | 192.242.15.192   | 255.255.255.248 (/29)        | 192.242.15.199       | 192.242.15.193 - 192.242.15.198    |
| WAN 1 (nat1-amonsul)        | 192.242.15.200   | 255.255.255.252 (/30)        | 192.242.15.203       | 192.242.15.201 - 192.242.15.202    |
| WAN 2 (amonsul-fornost)     | 192.242.15.204   | 255.255.255.252 (/30)        | 192.242.15.207       | 192.242.15.205 - 192.242.15.206    |
| WAN 3 (amonsul-eregion)     | 192.242.15.208   | 255.255.255.252 (/30)        | 192.242.15.211       | 192.242.15.209 - 192.242.15.210    |
| WAN 4 (amonsul-minastir)    | 192.242.15.212   | 255.255.255.252 (/30)        | 192.242.15.215       | 192.242.15.213 - 192.242.15.214    |
| WAN 5 (eregion-numenor)     | 192.242.15.216   | 255.255.255.252 (/30)        | 192.242.15.219       | 192.242.15.217 - 192.242.15.218    |
| WAN 6 (eregion-mordor)      | 192.242.15.220   | 255.255.255.252 (/30)        | 192.242.15.223       | 192.242.15.221 - 192.242.15.222    |
| WAN 7 (numenor-gudur)       | 192.242.15.224   | 255.255.255.252 (/30)        | 192.242.15.227       | 192.242.15.225 - 192.242.15.226    |
| WAN 8 (mordor-erain)        | 192.242.15.228   | 255.255.255.252 (/30)        | 192.242.15.231       | 192.242.15.229 - 192.242.15.230    |
| WAN 9 (minastir-amroth)     | 192.242.15.232   | 255.255.255.252 (/30)        | 192.242.15.235       | 192.242.15.233 - 192.242.15.234    |
| WAN 10 (minastir-anor)      | 192.242.15.236   | 255.255.255.252 (/30)        | 192.242.15.239       | 192.242.15.237 - 192.242.15.238    |

## Penggabungan - CIDR


## Pembagian IP - CIDR