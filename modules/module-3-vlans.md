# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 3: VLANs

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-14  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

* * *

## 🎯 Tujuan Modul

- Menjelaskan bagaimana switch layer 2 meneruskan data.

* * *

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan topik pembelajaran.

### 🔸 Submodul 2: Tinjauan VLAN

- Manfaat desain VLAN: Memperkecil broadcast domain, meningkatkan keamanan, meningkatkan efisiensi IT, mengurangi biaya, performa yang lebih baik, menyederhanakan proyek dan manajemen aplikasi.
- Jenis-jenis VLAN: default, data, native, management, voice.
- Default VLAN: Semua lalu lintas kontrol layer 2 dikaitkan dengan VLAN 1.
- Data VLAN: Memisahkan jaringan menjadi kelompok pengguna atau perangkat.
- Native VLAN: Switch port 802.1Q trunk digunakan untuk mendukung transmisi pengguna VLAN antar switch. Native VLAN digunakan untuk lalu lintas yang tidak memiliki tag VLAN (untagged traffic) pada trunk port.

- Management VLAN: Data VLAN dikonfigurasi secara khusus untuk manajemen lalu lintas jaringan.
- Voice VLAN: VLAN yang mendukung layanan Voice IP (VoIP).

### 🔸 Submodul 3: VLAN di Lingkungan Multi-Switched

- VLAN trunk memungkinkan semua lalu lintas VLAN merambat di antara switch.
- Trunk adalah link point-to-point antara dua perangkat jaringan yang membawa lebih dari satu VLAN.
- VLAN meng-segmentasi broadcast domain langsung dari perangkat layer 2.

### 🔸 Submodul 4: Konfigurasi VLAN

- Rentang VLAN normal diidentifikasi dengan VLAN ID 1 - 1005. File konfigurasi disimpan ke flash memory dengan nama file vlan.dat.
- Rentang VLAN extended diidentifikasi dengan VLAN ID 1006 - 4094. Secara default, file konfigurasi disimpan ke file running-config.
- Langkah-langkah membuat VLAN: Konfigurasi terminal global > VLAN ID > nama VLAN > end.
- Langkah-langkah penetapan switchport access: Konfigurasi terminal global > pilih antarmuka port > switchport mode access > switchport access VLAN ID > end.
- Perintah `delete` dan `no vlan` pada konfigurasi terminal global dapat digunakan untuk menghapus konfigurasi VLAN pada switch. 

### 🔸 Submodul 5: VLAN Trunk
- VLAN trunk adalah link layer 2 antara dua switch yang membawa lalu lintas untuk semua VLAN (kecuali daftar VLAN yang diizinkan dibatasi secara manual atau dinamis).
- Langkah-langkah penetapan switchport trunk: Konfigurasi terminal global > pilih antarmuka port > switchport mode trunk > switchport trunk mode VLAN ID > end.

### 🔸 Submodul 6: Protokol Trunking Dinamis
- Dynamic Trunking Protocol (DTP): Protokol yang memungkinkan switch untuk menegosiasikan trunking dengan perangkat tetangga secara otomatis.
- Mode antarmuka switch: `access`, `dynamic auto`, `dynamic desirable`, dan `trunk`.

***

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Who Hears the Broadcast?
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Mengamati lalu lintas transmisi dan mengetahui perangkat-perangkat yang menerima paket broadcast pada setiap VLAN melalui simulation mode.
- 📁 **File Lab**:[Who Hears the Broadcast? PKA File](../labs/module-3/3.1.4-packet-tracer---who-hears-the-broadcast.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Investigate a VLAN Implementation
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Memahami perbedaan lalu lintas pengiriman paket broadcast pada switch dengan atau tanpa implementasi VLAN melalui simulation mode.
- 📁 **File Lab**: [Investigate a VLAN Implementation PKA File](../labs/module-3/3.2.8-packet-tracer---investigate-a-vlan-implementation.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: VLAN Configuration
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: VLAN pada switch dengan switchport access berhasil dikonfigurasi.
- 📁 **File Lab**: [VLAN Configuration PKA File](../labs/module-3/3.3.12-packet-tracer---vlan-configuration.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure Trunks
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: VLAN pada switch dengan switchport trunk berhasil dikonfigurasi.
- 📁 **File Lab**: [Configure Trunks PKA File](../labs/module-3/3.4.5-packet-tracer---configure-trunks.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure VLANs and Trunking
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Berhasil mengimplementasikan switchport access dan trunk pada konfigurasi VLAN.
- 📁 **File Lab**: [Configure VLANs and Trunking PKA File](../labs/module-3/3.4.6-packet-tracer---configure-vlans-and-trunking---physical-mode.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure DTP
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: VLAN pada switch dikonfigurasi bersama switchport DTP .
- 📁 **File Lab**: [Configure DTP PKA File](../labs/module-3/3.5.5-packet-tracer---configure-dtp.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Implement VLANs and Trunking
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Berhasil mengimplementasikan koneksi VLAN berbasis switchport access, trunking, native, voice, dan DTP.
- 📁 **File Lab**: [Implement VLANs and Trunking PKA File](../labs/module-3/3.6.1-packet-tracer---implement-vlans-and-trunking.pka) - ✅ 100% selesai

***

## 🧠 Catatan Pribadi

💬 Switchport mode access digunakan untuk menghubungkan switch dengan perangkat akhir, sedangkan switchport mode trunk digunakan untuk menghubungkan antar switch atau dengan perangkat jaringan lain yang mendukung VLAN. Kemudian switchport voice disediakan untuk kebutuhan Quality of Service (QOS) pada transmisi suara, seperti Voice IP (VoIP). Selain itu, switchport native sering kali digunakan untuk kebutuhan manajemen switch. 

*** 

## 📎 Referensi Modul
- [Cisco Networking Academy](https://www.netacad.com)  

***

> Ditulis oleh: **Ulil Akbar** pada 2025-06-14.
