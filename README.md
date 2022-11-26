# Jarkom-Modul-4-E09-2022

## Anggota
1. Azzura Ferliani Ramadhani (5025201190)
2. Ingwer Ludwig Nommensen (5025201259)

## VLSM Menggunakan CPT
### Pembagian Subnet

![Screenshot 2022-11-26 at 21 10 39](https://user-images.githubusercontent.com/54592376/204093023-5ce392f2-a035-41cf-afea-12c5ac613215.jpg)

### Penentuan Jumlah Alamat IP
Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melabel netmask berdasarkan jumlah IP yang dibutuhkan.

![image](https://user-images.githubusercontent.com/54592376/204093086-f3c4e9e2-f0ab-4981-b1df-6a86d8a34300.png)


### Pembentukan Pohon IP
Subnet besar yang dibentuk memiliki NID 10.26.0.0 dengan netmask /20 sehingga pembagian IP berdasarkan NID dan netmask dihitung sesuai dengan pohon berikut.

![image](https://user-images.githubusercontent.com/54592376/204093190-5e4637d1-0793-454f-a845-6b5f95af233b.png)

### Link Untuk Subnetting Tree
https://docs.google.com/spreadsheets/d/1bWAXPEen_DKGcyY5cPj9wx_7p0HTvHXv--l4YTv-AGs/edit?usp=sharing

### Subnet + IP
Selanjutnya menyesuaikan pembagian IP sesuai dengan subnet yang telah dibagi berdasarkan pohon diatas pada topologi. Setelah itu akan didapatkan pembagian IP untuk tiap nodenya.
![image](https://user-images.githubusercontent.com/54592376/204093217-02ffdeaa-d716-40fa-9a05-06f44c42ffcc.png)
![image](https://user-images.githubusercontent.com/54592376/204093248-5370f381-0de1-42c6-b881-4e3f4218e049.png)

## CIDR Menggunakan GNS3
### Pembagian Subnet
![image](https://user-images.githubusercontent.com/52819640/204092727-9cf78359-fd09-4ba6-a13e-12a5fdb7ab03.png)
### Proses CIDR
![image](https://user-images.githubusercontent.com/52819640/204092744-711c6283-36a4-486f-ba64-2061a2eec266.png)
![image](https://user-images.githubusercontent.com/52819640/204092761-573cea33-c345-4def-a9a7-127a4ccff906.png)
![image](https://user-images.githubusercontent.com/52819640/204092772-9ca10f1d-910f-461d-a556-24ca3e7a541d.png)
![image](https://user-images.githubusercontent.com/52819640/204092781-43734f4c-bc2e-4ce2-b23c-3c698d9b71a0.png)
![image](https://user-images.githubusercontent.com/52819640/204092845-3e618e21-6629-42ae-89ba-734fb2306d45.png)
![image](https://user-images.githubusercontent.com/52819640/204092864-0085bf5b-0b8c-4f99-8014-8f0c2352c235.png)
![image](https://user-images.githubusercontent.com/52819640/204092887-471dba69-fae3-41b3-abee-c4ce5e9935c1.png)
![image](https://user-images.githubusercontent.com/52819640/204092903-6fe2b40c-71c0-44d4-884e-485caf46a01f.png)
### CIDR Tree
![CIDR Tree drawio](https://user-images.githubusercontent.com/52819640/204092973-74cfb0d4-f588-4f7e-b9ec-b1581390f86d.png)
### Network Configuration
#### The Resonance
```
auto lo
iface lo inet loopback

auto eth1
iface eth1 inet static
        address 10.26.132.1
        netmask 255.255.255.252

auto eth2  
iface eth2 inet static
        address 10.26.130.1
        netmask 255.255.255.252

auto eth3
iface eth3 inet static
        address 10.26.96.1
        netmask 255.255.255.252

auto eth4
iface eth4 inet static
        address 10.26.32.1
        netmask 255.255.255.252
```
#### The Beast
```
auto eth0
iface eth0 inet static
        address 10.26.132.2
        netmask 255.255.255.252
        gateway 10.26.132.1
```
#### The Magical
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.130.2
        netmask 255.255.255.252
        gateway 10.14.130.1

auto eth1
iface eth1 inet static
        address 10.26.128.1
        netmask 255.255.254.0
```
#### The Instrument
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.96.2
        netmask 255.255.255.252
        gateway 10.26.96.1

auto eth1
iface eth1 inet static
        address 10.26.68.1
        netmask 255.255.255.252

auto eth2
iface eth2 inet static
        address 10.26.81.1
        netmask 255.255.255.252

auto eth3
iface eth3 inet static
        address 10.26.72.0
        netmask 255.255.255.128
```
#### The Order 
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.32.2
        netmask 255.255.255.252
        gateway 10.26.32.1

auto eth1
iface eth1 inet static
        address 10.26.16.1
        netmask 255.255.255.192

auto eth2
iface eth2 inet static
        address 10.26.8.1
        netmask 255.255.255.252
```
#### Haines
```
auto eth0
iface eth0 inet static
       address 10.26.128.2
       netmask 255.255.254.0
       gateway 10.26.128.1
```
#### Corvekt
```
auto eth0
iface eth0 inet static
      address 10.26.128.3
      netmask 255.255.254.0
      gateway 10.26.128.1
```
#### The Profound
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.26.81.2
      netmask 255.255.255.252
      gateway 10.26.81.1

auto eth2
iface eth2 inet static
      address 10.26.80.129
      netmask 255.255.255.128

auto eth1
iface eth1 inet static
      address 10.26.80.1
      netmask 255.255.255.128
```
#### The Firefist
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.26.68.2
      netmask 255.255.255.252
      gateway 10.26.68.1

auto eth1
iface eth1 inet static
      address 10.26.66.1
      netmask 255.254.0.0

auto eth2
iface eth2 inet static
      address 10.26.64.1
      netmask 255.255.255.0
```
#### The Order
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.32.2
        netmask 255.255.255.252
        gateway 10.26.32.1

auto eth1
iface eth1 inet static
        address 10.26.16.1
        netmask 255.255.255.192

auto eth2
iface eth2 inet static
        address 10.26.8.1
        netmask 255.255.255.252
```
#### Ashof
```
auto eth0
iface eth0 inet static
       address 10.26.16.2
       netmask 255.255.255.192
       gateway 10.26.16.1
```
#### The Minister
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.8.2
        netmask 255.255.255.252
        gateway 10.26.8.1

auto eth1
iface eth1 inet static
        address 10.26.1.1
        netmask 255.255.255.252

auto eth2
iface eth2 inet static
        address 10.26.4.1
        netmask 255.255.252.0
```
#### The Dauntless
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.1.2
        netmask 255.255.255.252
        gateway 10.26.1.1

auto eth1
iface eth1 inet static
        address 10.26.0.1
        netmask 255.255.255.0
```
#### Spendrow
```
auto eth0
iface eth0 inet static
        address 10.26.80.130
        netmask 255.255.255.128
        gateway 10.26.80.129
```
#### Helga
```
auto eth0
iface eth0 inet static
        address 10.26.80.2
        netmask 255.255.255.128
        gateway 10.26.80.2
```
#### Oakleave
```
auto eth0
iface eth0 inet static
        address 10.26.66.2
        netmask 255.254.0.0
        gateway 10.26.66.1
```
#### Keith
```
auto eth0
iface eth0 inet static
       address 10.26.64.3
       netmask 255.255.255.0
       gateway 10.26.64.1
```
#### The Queen
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.26.64.2
        netmask 255.255.255.0
        gateway 10.26.64.1

auto eth1
iface eth1 inet static
        address 10.26.65.1
        netmask 255.255.255.252
```
#### The Witch
```
auto eth0
iface eth0 inet static
        address 10.26.65.2
        netmask 255.255.255.252
        gateway 10.26.65.1
```
#### Phanora
```
auto eth0
iface eth0 inet static
       address 10.26.0.2
       netmask 255.255.254.0
       gateway 10.26.0.1
```
#### Johan
```
auto eth0
iface eth0 inet static
       address 10.26.0.3
       netmask 255.255.254.0
       gateway 10.26.0.1
```
#### Guideau
```
auto eth0
iface eth0 inet static
       address 10.26.4.2
       netmask 255.255.252.0
       gateway 10.26.4.1
```
### Routing CIDR
#### The Profound
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.26.81.1
```

#### The Queen
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.26.64.1
```

#### The Magical
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.26.130.1
```

#### The Dauntless
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.26.1.1
```

#### The Firefist
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.26.68.1
```
