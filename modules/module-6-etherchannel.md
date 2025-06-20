# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 6: EtherChannel

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-19  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

---

## 🎯 Tujuan Modul

- Melakukan *troubleshooting* pada *EtherChannel* di jalur koneksi antar *switch*.

---

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan umum terhadap materi yang akan dipelajari dalam modul ini.

### 🔸 Submodul 2: Operasi EtherChannel

- *EtherChannel* merupakan teknologi *link aggregation* yang menggabungkan beberapa jalur fisik *Ethernet* menjadi satu saluran logis. Teknologi ini dirancang untuk meningkatkan toleransi kesalahan, membagi beban lalu lintas, menambah kapasitas bandwidth, serta memberikan redundansi pada koneksi antara *switch*, *router*, dan *server*.
- Untuk membangun *EtherChannel*, terdapat dua jenis protokol *autonegotiation* yang dapat digunakan, yaitu *Port Aggregation Protocol (PAgP)* dan *Link Aggregation Control Protocol (LACP)*.
- *PAgP* merupakan protokol eksklusif milik Cisco yang memungkinkan pembentukan *EtherChannel* secara otomatis. Mode konfigurasi pada *PAgP* meliputi: **on**, **PAgP desirable**, dan **PAgP auto**.
- *LACP*, yang merupakan bagian dari standar *IEEE 802.3AD*, juga memungkinkan penggabungan beberapa port fisik menjadi satu kanal logis. Mode *LACP* terdiri atas: **on**, **LACP active**, dan **LACP passive**.

### 🔸 Submodul 3: Konfigurasi EtherChannel

- Beberapa pedoman konfigurasi penting perlu diperhatikan saat mengaktifkan *EtherChannel*, yaitu: seluruh antarmuka *Ethernet* harus mendukung *EtherChannel*, memiliki kecepatan dan mode *duplex* yang sama, tergabung dalam *VLAN* yang sama, serta menggunakan kisaran *VLAN* yang diizinkan seragam jika beroperasi dalam mode *trunking*. Semua antarmuka juga harus memiliki konfigurasi identik untuk memastikan pembentukan *channel* yang stabil.

### 🔸 Submodul 4: Verifikasi dan Troubleshoot EtherChannel

- Untuk memverifikasi keberhasilan konfigurasi *EtherChannel*, beberapa perintah yang digunakan antara lain:  
  `show interfaces port-channel`  
  `show etherchannel summary`  
  `show etherchannel port-channel`  
  `show interfaces etherchannel`
  
- Beberapa kendala umum yang dapat terjadi mencakup: antarmuka yang tidak berada dalam *VLAN* yang sama, antarmuka belum dikonfigurasi sebagai *trunk*, hanya sebagian port dalam *EtherChannel* yang di-*trunking*, atau perbedaan dalam daftar *VLAN allowed*. Selain itu, ketidakcocokan konfigurasi mode negosiasi dinamis pada *PAgP* maupun *LACP* di kedua ujung perangkat juga dapat mencegah pembentukan *EtherChannel*.

---

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Configure EtherChannel  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: *EtherChannel* berhasil dikonfigurasi pada tiga *switch*, serta menetapkan salah satu *switch* sebagai *root bridge*.  
- 📁 **File Lab**: [Configure EtherChannel PKA File](../labs/module-6/6.2.4-packet-tracer---configure-etherchannel.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Troubleshoot EtherChannel  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Berhasil memeriksa konektivitas serta mengidentifikasi dan memperbaiki kesalahan konfigurasi pada koneksi redundan *EtherChannel* antar *switch*. 
- 📁 **File Lab**: [Troubleshoot EtherChannel PKA File](../labs/module-6/6.3.4-packet-tracer---troubleshoot-etherchannel.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Implement EtherChannel  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Berhasil merancang dan mengimplementasikan EtherChannel dalam topologi jaringan berbasis switch. 
- 📁 **File Lab**: [Implement EtherChannel PKA File](../labs/module-6/6.4.1-packet-tracer---implement-etherchannel.pka) - ✅ 100% selesai

---

## 🧠 Catatan Pribadi

💬 Dua protokol *autonegotiation* utama yang digunakan dalam *EtherChannel*, yaitu *PAgP* dan *LACP*, memiliki mode kerja masing-masing. Keduanya menyediakan mode **on**, yang akan memaksa antarmuka untuk tergabung ke dalam *port channel*. Pada *PAgP*, mode **desirable** membuat antarmuka aktif menginisiasi proses negosiasi dengan antarmuka lain, sedangkan mode **auto** bersifat pasif dan hanya merespons jika ada permintaan dari sisi lawan. Sementara itu, *LACP* bekerja dengan prinsip serupa namun dengan penamaan mode yang berbeda, yaitu **active** dan **passive**.

---

## 📎 Referensi Modul

- [Cisco Networking Academy](https://www.netacad.com)

---

> Ditulis oleh: **Ulil Akbar** pada 2025-06-19.
