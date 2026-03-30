# 🏗️ SOP Struktur Standar Instance (Drafting)

Dokumen ini mendefinisikan struktur folder standar untuk setiap institusi/instansi (Instance) yang bernaung di bawah repositori **naikkelas-agent**. Tujuannya agar terjadi sinkronisasi antara perancangan kurikulum dan pengembangan teknis di platform **naikkelas.id**.

---

## 📂 Struktur Folder Instance

Setiap sub-direktori di bawah folder `instances/` (misal: `koneksi-digital/`) disarankan mengikuti pola ini:

```text
instances/nama-institusi/
├── 00_Master_Plan.md        <-- Visi, Roadmap 3 Bulan, & Strategi Utama
├── 01_Proposal_Eksekutif.md  <-- Dokumen untuk Petinggi/Stakeholder
├── curriculum/              <-- Pusat Materi & Silabus (Mata Kuliah)
│   ├── 10_Pondasi_Umum.md
│   ├── 20_Spesialisasi_A.md
│   └── 30_Spesialisasi_B.md
├── operational/             <-- SOP Pendampingan & Mentor Lapangan
│   └── SOP_Mentor.md
├── assets/                  <-- Tempat penyimpanan aset (Gambar/PDF/Link)
├── feedback/                <-- Hasil kurasi AI & catatan tim (Sandbox)
└── README.md                <-- Daftar Isi & Panduan Tim Institusi
```

---

## 💡 Rationale (Alasan Digunakan)

1.  **Konsistensi AI-Native**: AI Agent (Antigravity, Claude, dll.) dapat menelusuri berbagai instance dengan cepat jika polanya seragam.
2.  **Sistem Penomoran (00, 01, 10, dst.)**: Memberikan urutan logis bagi tim awam dan memudahkan AI dalam menentukan prioritas pembacaan dokumen.
3.  **Pemisahan Strategis**: Membedakan antara dokumen pengambilan keputusan (Petinggi) dengan dokumen eksekusi konten (Tim Kreatif).
4.  **Sandbox Kreatif (`feedback/`)**: Memberikan ruang bagi tim kurikulum untuk mengunggah draf kasar atau link Google Docs sebelum dikurasi oleh AI Agent menjadi modul final di folder `curriculum/`.

---

## 🤝 Alur Kolaborasi Tim & AI

1.  **Drafting Sederhana**: Tim kurikulum menulis materi di platform yang mereka kuasai (Google Docs/MS365).
2.  **Curation**: Link tersebut diberikan kepada sandikodev (Team Lead).
3.  **AI Processing**: AI Agent membaca link tersebut, melakukan brainstorming, dan menaruh draf hasil kurasi di folder `feedback/`.
4.  **Finalization**: Setelah disetujui, draf di `feedback/` dipindahkan ke `curriculum/` sebagai materi siap deploy.

---

## ⚙️ Integrasi Platform (naikkelas.id)

SOP struktur ini dirancang agar kompatibel dengan **Sistem Telemetri Naik Kelas**:
*   Setiap file di `curriculum/` akan dipetakan menjadi modul di database.
*   Header dokumen Markdown di setiap file kurikulum akan digunakan sebagai metadata modul.

---
**Status**: Draft Brainstorming  
**Inisiator**: sandikodev  
**Terakhir Diperbarui**: 2026-03-30
