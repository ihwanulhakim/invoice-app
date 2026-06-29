# 🧾 Aplikasi Cetak Faktur Penjualan

Aplikasi berbasis web single-file untuk mencetak & mengunduh faktur penjualan secara otomatis dari file Excel `.xlsx` / `.xls`.

**Dibuat oleh:** Ihwanul Hakim

🔗 **Live App:** [https://ihwanulhakim.github.io/invoice-app/](https://ihwanulhakim.github.io/invoice-app/)

---

## ✨ Fitur

- 📂 **Upload Excel** — drag & drop atau klik, support `.xlsx` dan `.xls`
- 💾 **Auto-simpan di browser** — file tersimpan di IndexedDB, tidak hilang saat refresh
- 🔍 **Pencarian invoice** — cari berdasarkan Nomor Faktur, Nama Customer, Total Harga, atau Jumlah Item
- 🗂️ **3 Mode tampilan:**
  - **A — Gabung:** invoice dengan nomor faktur yang sama digabung jadi 1 faktur
  - **B — Pisah:** setiap baris Excel jadi faktur terpisah, item susulan diberi badge
  - **C — Gabung + Label:** digabung, item susulan ditandai label di dalam tabel
- 🖨️ **Cetak / Print PDF** — print dialog browser untuk invoice aktif
- 📥 **Print Semua** — print semua invoice sekaligus via browser
- 📑 **Print Pilihan** — pilih invoice tertentu dengan checkbox lalu cetak
- ⬇️ **Download PDF Ini** — download PDF invoice yang sedang aktif
- 📦 **Download Semua PDF** — render satu per satu lalu kemas jadi 1 file `.zip`
- ✅ **Download Terpilih** — download hanya invoice yang dicentang, dikemas jadi `.zip`


## 🛠️ Penggunaan Lokal

Cukup buka `index.html` langsung di browser — tidak perlu server, tidak perlu install apapun.

> **Catatan:** Fitur IndexedDB (auto-simpan file Excel) memerlukan browser modern (Chrome, Edge, Firefox, Safari).

---

## 📋 Format Excel yang Didukung

Aplikasi mendeteksi kolom secara otomatis berdasarkan nama kolom. Kolom yang dikenali:

| Data | Nama kolom yang dikenali |
|---|---|
| Nomor Invoice | kolom yang mengandung kata `invoice` |
| Nama Customer | `Nama` / `nama` |
| Nomor SJ | mengandung `surat jalan` / `packingslip` |
| Nomor SO | mengandung `sales order` / `salesid` |
| Nomor PO | mengandung `no po` / `customerref` |
| Nomor Kendaraan | mengandung `no kendaraan` |
| Alamat | mengandung `alamat` |
| NPWP | mengandung `npwp` |
| Qty | mengandung `qty` / `kuantitas` / `jumlah` |
| Harga Satuan | mengandung `price` / `harga satuan` |
| Kode Barang | mengandung `item` / `kode barang` |
| Nama Barang | mengandung `nama barang` |
| Tanggal | mengandung `date` / `tanggal` / `invoicedate` |