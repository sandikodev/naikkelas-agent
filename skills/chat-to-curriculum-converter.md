# Skill: Chat-to-Curriculum Converter (Operator Awal)

Skill ini dirancang untuk memungkinkan operator awam (melalui Telegram/WhatsApp) untuk secara cepat merumuskan draf kurikulum yang mendalam hanya dengan instruksi singkat.

## 🔷 INPUT SCHEMA (Dari Chat)
Operator mengirimkan pesan dengan elemen:
1.  **Nama Institusi/Instansi**.
2.  **Judul Kursus**.
3.  **Jumlah Modul** (Opsional, default: 4).
4.  **Fokus Utama** (Mindset vs Skill).
5.  **Instruksi Khusus** (Misal: "Sertakan video YouTube" atau "Harus ada tugas praktis").

## 🔷 AGENT PROCESSING LOGIC
Saat menerima input tersebut, AI Agent wajib:
1.  **Brainstorming Struktur**: Menentukan 20% Mindset dan 80% Skill sesuai aturan platform.
2.  **Penamaan Terstandar**: Membuat file dengan prefix angka (00, 01, 10, dll.).
3.  **Integrasi Aksi**: Menyisipkan setidaknya satu **Knowledge Check (KC)** per modul yang relevan dengan topik.
4.  **Gaya Bahasa**: Menggunakan bahasa yang "Akrab & Komunikatif" sesuai standar `naikkelas-agent`.

## 🔷 OUTPUT MAPPING (Ke Folder Instance)
Agen secara otomatis akan menempatkan draf tersebut ke:
- `instances/[nama-institusi]/00_Master_Plan.md`
- `instances/[nama-institusi]/curriculum/[nomor]_[judul].md`

---

## 📝 CONTOH EKSEKUSI (SIMULASI)
**Pesan Chat**: 
> "Buat draf kelas Ternak Lele Modern buat Yayasan Maju Makmur, 3 modul aja, fokus ke cara jualan hasil panen juga ya."

**Agent Action**:
1.  Membangun folder `instances/yayasan-maju-makmur/`.
2.  Menyusun `00_Master_Plan.md` dengan visi "Kemandirian Ekonomi Maju Makmur".
3.  Menyusun `curriculum/10_Mindset_Pembudidaya.md` (20% Why).
4.  Menyusun `curriculum/20_Teknik_Kolam_Bioflok.md` (How).
5.  Menyusun `curriculum/30_Strategi_Market_Lokal.md` (How & Monetisasi).
