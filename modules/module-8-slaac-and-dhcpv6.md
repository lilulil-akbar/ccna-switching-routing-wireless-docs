## 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 7: SLAAC and DHCPv6

**Platform**: [Cisco Networking Academy](https://www.netacad.com)
**Tanggal Belajar**: 2025-06-28
**Tipe Pembelajaran**: Instructor-led
**Instruktur**: **Ziad Sobri**
**Institusi**: Universitas Mitra Indonesia

---

## 🎯 Tujuan Modul

* Mengonfigurasi alokasi alamat dinamis pada jaringan *IPv6*.

---

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

* Memberikan gambaran umum mengenai topik yang akan dibahas dalam modul ini.

### 🔸 Submodul 2: Penetapan *IPv6 GUA*

* *SLAAC* merupakan singkatan dari *Stateless Address Autoconfiguration*.
* Hal pertama yang perlu diperhatikan dalam penggunaan *SLAAC* atau *DHCPv6* adalah memahami konsep *Global Unicast Address (GUA)* dan *Link-Local Address (LLA)*.
* Dalam pesan *ICMPv6*, terdapat tiga *flag* utama yang digunakan untuk menentukan opsi alokasi dinamis yang tersedia bagi *host*, yaitu *A flag*, *O flag*, dan *M flag*.

  * *A flag* (Address Autoconfiguration): digunakan saat *SLAAC* digunakan untuk menghasilkan *IPv6 GUA*.
  * *O flag* (Other Configuration): digunakan saat konfigurasi tambahan diperoleh dari *stateless DHCPv6 server*.
  * *M flag* (Managed Address Configuration): digunakan saat seluruh konfigurasi alamat diperoleh dari *stateful DHCPv6 server*.

### 🔸 Submodul 3: SLAAC

* Metode *SLAAC* memungkinkan setiap *host* membentuk alamat *IPv6 GUA* secara otomatis tanpa perlu layanan *DHCPv6 server*.
* Dalam implementasi *SLAAC*, tidak ada sistem terpusat yang menyimpan informasi pengalamatan, sehingga *host* menghasilkan alamatnya sendiri.
* *Router Advertisement (RA)* adalah pesan *ICMPv6* yang dikirim secara berkala (setiap 200 detik) oleh *router* untuk memberi informasi konfigurasi jaringan kepada *host*.
* *Host* juga dapat mengirim pesan *Router Solicitation (RS)* untuk meminta *RA* dari *router*.
* Ketika *host* menerima pesan *RA*, ia akan membentuk pengenal antarmuka 64-bit dengan dua metode yang tersedia: *randomly generated* atau *EUI-64*.

  * *Randomly generated*: ID antarmuka dibuat secara acak, seperti yang digunakan di *Windows 10*.
  * *EUI-64*: ID antarmuka dibentuk berdasarkan *MAC address* 48-bit dari perangkat.
* Proses *Duplicate Address Detection (DAD)* digunakan untuk memastikan bahwa alamat *IPv6 GUA* yang dibentuk tidak bentrok dengan perangkat lain. Hal ini dilakukan dengan mengirim pesan *Neighbor Solicitation (NS)*, dan apabila tidak ada *Neighbor Advertisement (NA)* yang diterima sebagai respons, maka alamat dianggap unik dan valid.

### 🔸 Submodul 4: DHCPv6

* Alur kerja *DHCPv6* dimulai dari pengiriman pesan *RS* oleh *host* → diterima dan dibalas *RA* oleh *router* → *host* mengirim *DHCPv6 SOLICIT* → *DHCPv6 server* merespons dengan *ADVERTISE* → *host* mengirim *REQUEST* → *server* mengirim *REPLY*.
* Pada *Stateless DHCPv6*, *host* membentuk alamat *IPv6* sendiri menggunakan *prefix* dari *RA* dan pengenal antarmuka internal, lalu mengirim pesan *INFORMATION-REQUEST* ke *DHCPv6 server* untuk mendapatkan informasi konfigurasi tambahan seperti *DNS*.
* Pada *Stateful DHCPv6*, seluruh konfigurasi, termasuk alamat *IPv6*, diberikan oleh *server*, seperti halnya model klasik *DHCPv4*.

### 🔸 Submodul 5: Konfigurasi Server DHCPv6

* Sebuah *router* dapat berperan sebagai *DHCPv6 server*, *client*, maupun *relay agent* tergantung pada perannya di jaringan.

---

## ⚙️ Konfigurasi DHCPv6

### **Konfigurasi DHCPv6 Stateless (Server)**

```bash
R1(config)# ipv6 unicast-routing
R1(config)# ipv6 dhcp pool IPV6-STATELESS
R1(config-dhcpv6)# dns-server 2001:db8:acad:1::254
R1(config-dhcpv6)# domain-name example.com
R1(config-dhcpv6)# exit
R1(config)# interface GigabitEthernet0/0/1
R1(config-if)# description Link to LAN
R1(config-if)# ipv6 address fe80::1 link-local
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# ipv6 nd other-config-flag
R1(config-if)# ipv6 dhcp server IPV6-STATELESS
R1(config-if)# no shut
R1(config-if)# end
```

---

### **Konfigurasi DHCPv6 Stateless (Client)**

```bash
R3(config)# ipv6 unicast-routing
R3(config)# interface g0/0/1
R3(config-if)# ipv6 enable
R3(config-if)# ipv6 address autoconfig
R3(config-if)# end
```

---

### **Konfigurasi DHCPv6 Stateful (Server)**

```bash
R1(config)# ipv6 unicast-routing
R1(config)# ipv6 dhcp pool IPV6-STATEFUL
R1(config-dhcpv6)# address prefix 2001:db8:acad:1::/64
R1(config-dhcpv6)# dns-server 2001:4860:4860::8888
R1(config-dhcpv6)# domain-name example.com
R1(config)# interface GigabitEthernet0/0/1
R1(config-if)# description Link to LAN
R1(config-if)# ipv6 address fe80::1 link-local
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# ipv6 nd managed-config-flag
R1(config-if)# ipv6 nd prefix default no-autoconfig
R1(config-if)# ipv6 dhcp server IPV6-STATEFUL
R1(config-if)# no shut
R1(config-if)# end
```

---

### **Konfigurasi DHCPv6 Stateful (Client)**

```bash
R3(config)# ipv6 unicast-routing
R3(config)# interface g0/0/1
R3(config-if)# ipv6 enable
R3(config-if)# ipv6 address dhcp
R3(config-if)# end
```

---

### **Perintah Verifikasi DHCPv6**

```bash
show ipv6 interface brief
show ipv6 dhcp interface
show ipv6 dhcp pool
show ipv6 dhcp binding
ipconfig /all   ← (di sisi klien Windows)
```

---

## 🌐 Praktik / Simulasi

* Tidak tersedia untuk modul ini.

---

## 🧠 Catatan Pribadi

💬 Pada jaringan *IPv6*, terdapat dua metode utama untuk konfigurasi alamat secara dinamis: *SLAAC* dan *DHCPv6*. *SLAAC* memungkinkan *host* membentuk alamat sendiri tanpa intervensi *server*, sementara *DHCPv6* (baik *stateless* maupun *stateful*) menyediakan mekanisme untuk mengatur konfigurasi jaringan dari sisi *server*. Pemahaman terhadap *RA*, *RS*, *NS*, *NA* dan *flag* ICMPv6 sangat penting dalam menentukan metode mana yang sedang digunakan.

---

## 📎 Referensi Modul

* [Cisco Networking Academy](https://www.netacad.com)

---

> Ditulis oleh: **Ulil Akbar** pada 2025-06-28.
