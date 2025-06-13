# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 1: Basic Device Configuration

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Modul Ke**: 1 dari 16  
**Tanggal Belajar**: 2025-06-12  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

* * *

## 🎯 Tujuan Modul

- Konfigurasi perangkat menggunakan praktik keamanan terbaik.

* * *

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Unduh dan pasang perangkat lunak Cisco Packet Tracer
- Memulai Cisco Packet Tracer

### 🔸 Submodul 2: Konfigurasi Switch dengan Pengaturan Awal

- Urutan boot pada switch cisco IOS: Memuat program Power-On-Self-Test (POST) > Memuat perangkat lunak bootloader/bootstrap > Inisialisasi low-level CPU > Inisialisasi flash file sistem > Cari dan muat IOS default > Muat startup-config > Setup mode.
- Program POST memeriksa sub-sistem CPU. Ini menguji CPU, DRAM, dan bagian dari perangkat flash yang membentuk sistem file flash.
- Antarmuka switch virtual interface (SVI) digunakan untuk akses manajemen jarak jauh/remote.

### 🔸 Submodul 3: Konfigurasi Port Switch

- Komunikasi full-duplex adalah proses pengiriman dan penerimaan data dapat dilakukan secara serentak.
- Komunikasi half-duplex adalah proses pengiriman dan penerimaan data dilakukan satu-per-satu.
- Fitur Auto-MDIX - Antarmuka port secara otomatis mendeteksi jenis koneksi kabel yang diperlukan (straight-through atau crossover) dan mengkonfigurasi koneksi dengan tepat.

### 🔸 Submodul 4: Amankan Akses Jarak Jauh

- Sesi protokol telnet menggunakan transmisi plaintext yang tidak aman.
- Protokol SSH menyediakan enkripsi yang kuat untuk transmisi jarak jauh.

### 🔸 Submodul 5: Konfigurasi Router Dasar

- Konfigurasi pengaturan awal router sama seperti switch.
- Salah satu fitur yang membedakan antara router dan switch adalah dukungan jenis antarmuka port.
- Dukungan antarmuka pada router: Gigabit Ethernet, High-Speed WAN Interface Card (HWIC) slots, serial, DSL, dan antarmuka kabel.

### 🔸 Submodul 6: Verifikasi Jaringan yang Terhubung Langsung

- Perintah untuk verifikasi antarmuka dan status: `show ip interface brief`, `show ipv6 interface brief`, `show running-config interface`, `show ip route`, `show ipv6 route`.
- Perintah untuk filtering output dari perintah `show`: `section`, `include`, `exclude`, `begin`.

* * *

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Logical and Physical Mode Exploration
- 🔧 **Tools**: Packet Tracer, CLI, Telnet, Utilitas Ping
- 🔄 **Hasil**: Menjelajahi antarmuka topologi logis dan fisik Cisco Packet Tracer, disertai konfigurasi pengaturan awal pada router melalui port USB konsole.
- 📁 **File Lab**: [Logical and Physical Mode Exploration PKA File](../labs/module-1/1.0.5-packet-tracer---logical-and-physical-mode-exploration.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Basic Switch Configuration
- 🔧 **Tools**: Packet Tracer, CLI, SSH, Telnet, Utilitas Ping
- 🔄 **Hasil**: Manajemen switch dasar dengan koneksi VLAN melalui port USB konsole.
- 📁 **File Lab**: [Basic Switch Configuration PKA File](../labs/module-1/1.1.7-packet-tracer---basic-switch-configuration---physical-mode.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure SSH
- 🔧 **Tools**: Packet Tracer, CLI, SSH, Telnet, Utilitas Ping
- 🔄 **Hasil**: Konfigurasi dan aktifkan fitur login via koneksi SSH pada switch.
- 📁 **File Lab**: [Configure SSH PKA File](../labs/module-1/1.3.6-packet-tracer---configure-ssh.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure Router Interfaces
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Konfigurasi antarmuka router menggunakan alamat IPv4 dan IPv6, masing-masing jaringan berhasil memberikan respon menggunakan utilitas `ping`.
- 📁 **File Lab**: [Configure Router Interfaces PKA File](../labs/module-1/1.4.7-packet-tracer---configure-router-interfaces.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Verify Directly Connected Networks
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Kesalahan konfigurasi pada router telah berhasil diperbaiki dan koneksi jaringan kembali normal.
- 📁 **File Lab**: [Verify Directly Connected Networks PKA File](../labs/module-1/1.5.10-packet-tracer---verify-directly-connected-networks.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Implement a Small Network
- 🔧 **Tools**: Packet Tracer, CLI, Utilitas Ping
- 🔄 **Hasil**: Membangun topologi jaringan kecil, host di jaringan yang berbeda berhasil memberikan respon menggunakan utilitas `ping`.
- 📁 **File Lab**: [Implement a Small Network PKA File](../labs/module-1/1.6.1-packet-tracer---implement-a-small-network.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Configure Basic Router Settings
- 🔧 **Tools**: Packet Tracer, CLI, SSH, Utilitas Ping
- 🔄 **Hasil**: Berhasil membangun topologi jaringan sederhana dengan implementasi konfigurasi router dasar.
- 📁 **File Lab**: [Configure Basic Router Settings PKA File](../labs/module-1/1.6.2-packet-tracer----configure-basic-router-settings---physical-mode.pka) - ✅ 100% selesai

* * *

## 🧠 Catatan Pribadi

💬 Terdapat dua jenis switch, yaitu managed dan unmanaged. Pada switch managed, disarankan untuk mengkonfigurasi alamat ip default gateway ketika switch diaktifkan fitur manajemen jarak jauh menggunakan telnet atau SSH.

* * *

## 📎 Referensi Modul
[Cisco Networking Academy](https://www.netacad.com)  

* * *

## 📄 Lisensi

Dokumentasi ini disusun berdasarkan proses belajar pribadi dari kursus Cisco Networking Academy dan **tidak menyertakan materi berbayar atau berlisensi resmi dari Cisco** seperti soal kuis, slide, atau konten tertutup lainnya.

Lisensi: [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/). Lihat detail lisensi di [LICENSE.md](./LICENSE.md)

* * *

> Ditulis oleh: **Ulil Akbar** pada 12 Juni 2025.