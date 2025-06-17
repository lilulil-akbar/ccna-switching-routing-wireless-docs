# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 4: Inter-VLAN Routing

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-16  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

* * *

## 🎯 Tujuan Modul

- Pemecahan masalah Inter-VLAN routing pada perangkat layer 3.

* * *

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan topik pembelajaran.

### 🔸 Submodul 2: Operasi Inter-VLAN Routing

- Inter-VLAN routing adalah proses meneruskan lalu lintas paket jaringan dari satu VLAN menuju VLAN yang lain.
- Perangkat yang mendukung Inter-VLAN routing: Router atau switch layer 3.
- Opsi Inter-VLAN routing: Legacy Inter-VLAN routing, Router-on-a-stick, Layer 3 Switch menggunakan Switch Virtual Interface (SVI).
- Legacy Inter-VLAN routing: Digunakan untuk solusi legacy, dan tidak dapat diskalakan (scalable) dengan baik. Dalam implementasinya satu antarmuka router digunakan untuk satu VLAN.
- Router-on-a-stick: Solusi yang dapat diterima untuk jaringan kecil hingga menengah. Dalam implementasinya menggunakan sub-interfaces yang dikonfigurasi untuk kebutuhan VLAN.
- Switch Layer 3 menggunakan SVI: Solusi yang paling dapat diskalakan untuk organisasi menengah hingga besar. Dalam implementasinya, konfigurasi dilakukan pada port SVI.

### 🔸 Submodul 3: Router-on-a-stick Inter-VLAN Routing

- Langkah-langkah konfigurasi VLAN dan trunking pada switch: Buat ID dan beri nama VLAN > buat antarmuka management > konfigurasi port access > konfigurasi port trunk.
- Langkah-langkah konfigurasi sub-interfaces pada router: R1# `interface [interface_id.subinterface_id]` > `encapsulation dot1q [vlan_id] native` > `ip address [ip-address subnet-mask]` > `no shutdown` > exit.
- Perintah-perintah untuk verifikasi koneksi dan troubleshooting: `ping`, `show ip route`, `show ip interface brief`, `show interfaces trunk`, `show interfaces`.

### 🔸 Submodul 4: Inter-VLAN Routing Menggunakan Switch Layer 3

- Switch layer 3 menggunakan switching berbasis perangkat keras untuk mencapai tingkat pemrosesan paket yang lebih tinggi daripada router.
- Langkah-langkah konfigurasi switch layer 3: Buat VLAN > buat antarmuka SVI VLAN > konfigurasi port access > aktifkan layanan routing IP.
- Jika VLAN dapat dijangkau oleh perangkat Layer 3 lainnya, maka mereka harus dikonfigurasi menggunakan routing statis atau dinamis. 
- Perintah `no switchport` dapat digunakan untuk mengalihkan antarmuka switch layer 2 menjadi antarmuka switch layer 3.

### 🔸 Submodul 5: Pemecahan Masalah Inter-VLAN Routing 

- Masalah umum Inter-VLAN: VLAN hilang, masalah port trunk pada switch, masalah port access pada switch, dan masalah konfigurasi pada router.
- Perintah-perintah untuk verifikasi koneksi dan troubleshooting: `show vlan`, `show interface [interface id] switchport`.

***

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Configure Router-on-a-Stick Inter-VLAN Routing
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Inter-VLAN router-on-a-stick routing berhasil diimplementasikan.
- 📁 **File Lab**: [Configure Router-on-a-Stick Inter-VLAN Routing PKA File](../labs/module-4/4.2.7-packet-tracer---configure-router-on-a-stick-inter-vlan-routing.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure Layer 3 Switching and Inter-VLAN Routing
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Inter-VLAN layer 3 switching berhasil diimplementasikan dengan menggunakan routing IPv4 dan IPv6.
- 📁 **File Lab**: [Configure Layer 3 Switching and Inter-VLAN Routing PKA File](../labs/module-4/4.3.8-packet-tracer---configure-layer-3-switching-and-inter-vlan-routing.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Troubleshoot Inter-VLAN Routing
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Berhasil menganalisa dan melakukan perbaikan miskonfigurasi pada perangkat, berbasis topologi logis.
- 📁 **File Lab**: [Troubleshoot Inter-VLAN Routing PKA File](../labs/module-4/4.4.8-packet-tracer---troubleshoot-inter-vlan-routing.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Troubleshoot Inter-VLAN Routing
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Berhasil menganalisa dan melakukan perbaikan mis-konfigurasi pada perangkat, berbasis topologi fisik.
- 📁 **File Lab**: [Troubleshoot Inter-VLAN Routing PKA File](../labs/module-4/4.4.9-packet-tracer---troubleshoot-inter-vlan-routing---physical-mode.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Inter-VLAN Routing Challenge
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Berhasil menyelesaikan tantangan dalam implementasi Inter-VLAN router-on-a-stick routing .
- 📁 **File Lab**: [Inter-VLAN Routing Challenge](../labs/module-4/4.5.1-packet-tracer---inter-vlan-routing-challenge.pka) - ✅ 100% selesai
***

## 🧠 Catatan Pribadi

💬  Perintah `switchport trunk native vlan` berfungsi untuk menangani lalu lintas untagged melalui trunk dengan menetapkan VLAN default, sedangkan `switchport trunk allowed vlan` membatasi lalu lintas tagged berdasarkan daftar VLAN yang diizinkan. Keduanya perlu dikonfigurasi dengan tepat dan konsisten agar komunikasi antar VLAN melalui trunk berjalan dengan benar dan aman.

*** 

## 📎 Referensi Modul
- [Cisco Networking Academy](https://www.netacad.com)  

***

> Ditulis oleh: **Ulil Akbar** pada 2025-06-16.
