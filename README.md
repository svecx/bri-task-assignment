# README

## Deskripsi Repository

Repository ini digunakan untuk mendukung proses **penarikan data harian**, **validasi data**, dan **pembuatan report**.
Struktur folder pada repository terdiri dari beberapa bagian utama sebagai berikut:

---

# Struktur Folder

## `helper/`

Folder ini berisi file pendukung yang **wajib tersedia** agar script dapat berjalan dengan baik.

Fungsi helper:

* Menyimpan file referensi
* Menyimpan konfigurasi tambahan
* Menyimpan template atau dependency pendukung proses validasi

> **Catatan:**
> Pastikan seluruh file di dalam folder `helper` tersedia sebelum menjalankan script.

---

## `script/`

Folder ini berisi source code atau script yang digunakan untuk melakukan:

* Validasi data
* Pengolahan data
* Perbandingan data antar table
* Otomatisasi proses checking

Format file umumnya berupa:

* `.ipynb`
* `.py`

---

## `working_instruction/`

Folder ini berisi dokumen langkah pengerjaan (Working Instruction) yang digunakan sebagai panduan proses:

* Penarikan data
* Validasi data
* Inject data
* Upload hasil data

Format file:

* `.docx`

---

# Tugas Utama Harian

Berikut merupakan tugas utama yang wajib dikerjakan setiap hari:

---

## 1. Check RO IGT ISB & Inject Data SUSPECT

### Dokumen Working Instruction

`Penarikan data harian – Check RO IGT ISB (DB02) & Inject data SUSPECT_FBTI_IGT_ISB (ZPAPM0009).docx`

### Aktivitas

* Melakukan pengecekan data RO IGT ISB
* Melakukan inject data suspect ke SAP menggunakan T-Code `ZPAPM0009`

---

## 2. Penarikan Data PAR

### Dokumen Working Instruction

`Penarikan data harian – Data PAR (CDPAR, LNPAR, DDPAR, GLINT).docx`

### Data yang Diambil

* CDPAR
* LNPAR
* DDPAR
* GLINT

### Ketentuan Folder

Seluruh hasil penarikan data wajib dijadikan satu folder dengan format nama:

```text
(ddmmyy)_PAR
```

Contoh:

```text
250526_PAR
```

### Upload File

Setelah seluruh data selesai dikumpulkan, upload folder tersebut ke halaman berikut:

[BRIDrive Upload Page](https://bridrive.bri.co.id/u/d/f4420ac5e9df487bb3ac/?utm_source=chatgpt.com)

---

## 3. Validasi Data ZFPSL_PRDCTGRP

### Dokumen Working Instruction

`Penarikan data harian – Data ZFPSL_PRDCTGRP NSE16H.docx`

### Script Validasi

Validasi dilakukan menggunakan file:

```text
PERBANDINGAN_KODE_PRODUK_DAN_CURRENCY_ANTARA_TABLE_PAR2_(DD_CD_LN)_DENGAN_ZFPSL_PRDCTGRP.ipynb
```

### Aktivitas

* Melakukan penarikan data `ZFPSL_PRDCTGRP`
* Menjalankan notebook validasi
* Membandingkan:

  * Kode Produk
  * Currency
  * Data antar table PAR dan ZFPSL_PRDCTGRP

---

# Alur Pengerjaan

1. Baca Working Instruction pada folder `working_instruction`
2. Siapkan seluruh file pada folder `helper`
3. Jalankan script pada folder `script`
4. Lakukan validasi data
5. Simpan hasil sesuai format penamaan
6. Upload hasil ke BRIDrive apabila diperlukan

---

# Catatan Penting

* Pastikan format nama file dan folder sesuai standar.
* Pastikan seluruh data berhasil tervalidasi sebelum upload.
* Jangan mengubah struktur folder repository.
* Gunakan script sesuai Working Instruction yang tersedia.
