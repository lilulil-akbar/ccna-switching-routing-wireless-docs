# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 5: STP Concepts

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-18  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

---

## 🎯 Tujuan Modul

- Menjelaskan bagaimana *STP* memungkinkan redundansi pada jaringan *Layer 2*.

---

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan topik pembelajaran.

### 🔸 Submodul 2: Tujuan STP

- *STP* merupakan kependekan dari *Spanning Tree Protocol*.
- Redundansi adalah bagian penting dari desain hirarkis jaringan untuk menghilangkan titik kegagalan tunggal dan mencegah gangguan layanan kepada pengguna.
- *Spanning Tree Protocol (STP)* adalah protokol jaringan *loop-prevention* yang memungkinkan redundansi sambil menciptakan topologi *loop-free* pada jaringan *Layer 2*. *IEEE 802.1D* merupakan standar *bridging* asli untuk *STP*.
- Terlalu banyak jalur *frame* akibat redundansi yang tidak terkendali dapat mengakibatkan terjadinya *loop Layer 2*.
- *Broadcast storm* adalah kondisi di mana jaringan dibanjiri oleh paket *broadcast* dalam jumlah sangat besar selama periode waktu tertentu. Masalah ini bisa disebabkan oleh perangkat keras yang rusak (seperti *NIC* bermasalah) atau akibat *loop Layer 2* dalam jaringan.

### 🔸 Submodul 3: Operasi STP

- Langkah-langkah membangun topologi *loop-free* mencakup: memilih *root bridge*, memilih *port root*, memilih *port designated*, dan memilih *port alternatif* (blocked).
- Dalam proses memilih *root bridge*, *Spanning Tree Algorithm (STA)* akan menunjuk satu *switch* dengan nilai prioritas terendah sebagai *root bridge* dan menggunakannya sebagai titik referensi semua perhitungan jalur. Jika nilai *Bridge ID (BID)* yang digunakan adalah default, maka pemilihan dilakukan berdasarkan *MAC address* dengan nilai heksadesimal terendah.
- Setelah *root bridge* ditentukan, *STA* akan menentukan jalur terbaik menuju *root bridge* dari semua tujuan di dalam *broadcast domain*. Jalur terbaik ini disebut sebagai *internal root path cost*, yang dihitung berdasarkan jumlah *cost* dari masing-masing *port* yang dilalui hingga mencapai *root bridge*.
- Setiap *switch* non-root akan memilih satu *port root*, yaitu port yang memiliki *path cost* keseluruhan paling rendah ke *root bridge*.
- Setiap segmen jaringan antara dua *switch* akan memiliki satu *port designated*. Port ini adalah port yang memiliki jalur terbaik menuju *root bridge* dibandingkan pasangannya dalam segmen tersebut.
- Jika suatu port bukan *port root* maupun *port designated*, maka port tersebut menjadi *port alternatif* yang berada dalam kondisi *blocking* untuk mencegah terbentuknya *loop*.
- Selama proses ini, *switch* saling bertukar informasi melalui *Bridge Protocol Data Unit (BPDU)*. Setiap *BPDU* mengandung *Bridge ID (BID)*, yang terdiri dari *Bridge Priority*, *Extended System ID*, dan *MAC address* dari *switch* pengirim.
- Nilai *BID* memiliki rentang dari 0 hingga 61440 dengan kenaikan setiap 4096. Nilai yang lebih rendah lebih disukai.
- *Extended System ID* adalah angka desimal yang ditambahkan ke prioritas *bridge* dalam *BID* untuk mengidentifikasi *VLAN* pada *BPDU* tersebut.
- Jika dua *switch* memiliki prioritas dan *Extended System ID* yang sama, maka *switch* dengan *MAC address* terendah (dalam format heksadesimal) akan menang.
- Jika terdapat beberapa jalur dengan *cost* yang sama, maka pemilihan *port root* dilakukan berdasarkan: *BID* pengirim terendah, prioritas *port* pengirim terendah, dan *port ID* pengirim terendah.
- Proses konvergensi *STP* bergantung pada tiga jenis *timer*, yaitu: *Hello Timer*, *Forward Delay Timer*, dan *Max Age Timer*.
- Status *port* dalam *STP* terdiri dari lima keadaan: *Blocking*, *Listening*, *Learning*, *Forwarding*, dan *Disabled*.

### 🔸 Submodul 4: Evolusi STP

- *Spanning Tree Protocol (STP)* adalah versi orisinal dari *IEEE 802.1D* (termasuk edisi 1998 dan sebelumnya) yang menciptakan topologi *loop-free* dalam jaringan dengan jalur redundan.
- *Per-VLAN Spanning Tree (PVST+)* adalah pengembangan dari *Cisco* terhadap *STP*, yang menyediakan instance *Spanning Tree* terpisah untuk setiap *VLAN*.
- *Rapid Spanning Tree Protocol (RSTP)*, yang distandarkan sebagai *IEEE 802.1w*, merupakan evolusi dari *STP* dengan konvergensi yang jauh lebih cepat.
- *IEEE 802.1D-2004* adalah revisi terbaru dari standar *STP* yang menggabungkan fitur *RSTP*.
- *Rapid PVST+* menyediakan pemisahan instance *IEEE 802.1w* per *VLAN*, serta mendukung fitur-fitur tambahan seperti *PortFast*, *BPDU Guard*, *BPDU Filter*, *Root Guard*, dan *Loop Guard*.
- *Multiple Spanning Tree Protocol (MSTP)* memungkinkan pemetaan beberapa *VLAN* ke dalam satu instance *Spanning Tree*.
- *Multiple Spanning Tree (MST)* mendukung hingga 16 instance *RSTP* dan memungkinkan penggabungan banyak *VLAN* dengan topologi logis dan fisik yang sama ke dalam instance umum. Masing-masing instance mendukung fitur yang sama seperti *Rapid PVST+*.

---

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Investigate STP Loop Prevention  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Mengamati dan menginvestigasi mekanisme *STP* pada *switch*.  
- 📁 **File Lab**:[Investigate STP Loop Prevention PKA File](../labs/module-5/5.1.9-packet-tracer---investigate-stp-loop-prevention.pka) - ✅ 100% selesai

---

## 🧠 Catatan Pribadi

💬  Perintah `show spanning-tree` berfungsi untuk membantu proses troubleshooting pada switch serta memastikan apakah switch tersebut berperan sebagai root bridge atau tidak.

---

## 📎 Referensi Modul

- [Cisco Networking Academy](https://www.netacad.com)

---

> Ditulis oleh: **Ulil Akbar** pada 2025-06-18.