# Rencana Proyek Minggu ke-1 (Project Plan)

**Mata Kuliah:** Teknologi Internet of Things (IoT) — INF-3xx | S1 Informatika FT UNIB
**Sub-CPMK 1.1:** PjBL & CBL (Kasus A DAS Air Bengkulu & Toolchain Lab-0)

Dokumen operasional rencana kerja Minggu 1 berbasis PjBL terpadu CBL. Memuat pembagian 4 peran rekayasa anggota tim, matriks checklist tugas, target waktu, dan luaran wajib.

---

## 1. Identitas Kelompok & Pembagian Peran Rekayasa

| Nama Anggota Tim | Peran Rekayasa | Tanggung Jawab Utama (Software Stack) |
|---|---|---|
| Kenia Nurma Feblia | Project Manager & Dashboard Engineer | Manajemen papan Kanban, koordinasi tim, integrasi LK-1, proposal PjBL, & alur dashboard/UI. |
| Primanda Nafissa Alfiansyah | Device & Firmware Engineer | Skema Wokwi (`diagram.json`), firmware ESP32 non-blocking (`millis`), DHT22, & GPIO/LED. |
| Hesi Desta Lestari | Back-End & Data Engineer | Serialisasi payload JSON telemetri, desain API/broker, & skema basis data time-series. |
| M. Dimas Al-Shiddiq | Security & DevOps Engineer | Inisialisasi repo Git 5 folder, `.gitignore`, feature branching, & analisis keamanan awal. |

---

## 2. Matriks Rencana Kerja Minggu 1 (Checklist & PJ)

| Sts | Deskripsi Kegiatan / Sub-Tugas | Penanggung Jawab (PJ) | Target | Luaran (Deliverable) |
|:--:|---|---|---|---|
| [ ] | Instalasi VS Code, PlatformIO IDE, Python 3.10+, & Wokwi License | Seluruh Tim (PJ: Kenia) | Hari 1 (Lab) | Environment VS Code & Wokwi siap |
| [ ] | Inisialisasi repositori Git 5 folder (`/firmware`, `/edge-gateway`, `/backend-api`, `/docker`, `/docs`) | M. Dimas Al-Shiddiq | Hari 1 (Lab) | Remote repo GitHub/GitLab terbentuk |
| [ ] | Konfigurasi `.gitignore` (`.pio/`, `.env`) & feature branching model | M. Dimas Al-Shiddiq | Hari 1 (Lab) | File `.gitignore` & feature branch remote |
| [ ] | Penyusunan `platformio.ini`, `wokwi.toml`, & `diagram.json` (ESP32 + DHT22 + LED + Button) | Primanda Nafissa A. | Hari 1 (Lab) | Rangkaian virtual Wokwi valid |
| [ ] | Eksperimen komparasi program blocking (`delay`) vs non-blocking (`millis`) | Primanda Nafissa A. | Hari 1 (Lab) | Tabel pengamatan respons tombol |
| [ ] | Serialisasi & pengujian output JSON telemetri pada Serial Monitor | Hesi Desta Lestari | Hari 1 (Lab) | Log telemetri JSON valid |
| [ ] | Diskusi Kasus A (Sistem Peringatan Dini Banjir DAS Air Bengkulu) (40 menit) | Kenia Nurma F. (Fasilitator) | Hari 2 (Kuliah) | Catatan kesepakatan analisis kasus |
| [ ] | Pemetaan Lapisan 1 (Perception) & Lapisan 2 (Transport/Edge) pada LK-1 | Primanda Nafissa A. | Hari 2 (Kuliah) | Isian LK-1 Lapisan 1 & 2 |
| [ ] | Pemetaan Lapisan 3 (Middleware), 4 (App), & 5 (Business/Security) pada LK-1 | Hesi Desta L. & M. Dimas A. | Hari 2 (Kuliah) | Isian LK-1 Lapisan 3, 4, 5 & Security |
| [ ] | Finalisasi, konsolidasi, & unggah Lembar Kerja Kasus 1 (LK-1) ke LMS | Kenia Nurma Feblia | Hari 3 | Dokumen LK-1 terunggah di LMS (1%) |
| [ ] | Penyelesaian Problem Set C1–C6 pada `docs/laporan-minggu-01.md` | Seluruh Tim (Lead: Kenia) | Hari 4 | File `docs/laporan-minggu-01.md` di Git |
| [ ] | Verifikasi unjuk kerja & paraf Asisten Laboratorium (Ceklis Lab-0) | Kenia Nurma Feblia | Hari 4 (Lab) | Ceklis lulus Praktikum Minggu 1 |
| [ ] | Brainstorming ide awal PjBL Bengkulu (persiapan Proposal Milestone 1) | Kenia Nurma Feblia & Tim | Hari 5 | Draf judul & rumusan masalah PjBL |

---

## 3. Action Plan Spesifik Setiap Anggota Tim

### Kenia Nurma Feblia — Project Manager & Dashboard Engineer
- Memimpin koordinasi awal tim, menyusun papan tugas (Kanban), dan mengawasi progres mingguan.
- Memfasilitasi diskusi Studi Kasus A (DAS Air Bengkulu) dan mengonsolidasi isian Lembar Kerja Kasus 1 (LK-1).
- Mengunggah dokumen LK-1 tepat waktu ke LMS Universitas Bengkulu (bobot: 1% NA).
- Mengkoordinasikan penyusunan `docs/laporan-minggu-01.md` dan memimpin persiapan ide awal Proposal Proyek PjBL (Milestone 1).

### Primanda Nafissa Alfiansyah — Device & Firmware Engineer
- Menyiapkan berkas konfigurasi `firmware/platformio.ini` dengan library Adafruit DHT dan ArduinoJson.
- Merancang diagram rangkaian virtual ESP32 + DHT22 + LED + Pushbutton pada `firmware/diagram.json` dan `wokwi.toml`.
- Menulis program firmware ESP32 berbasis `millis()` (non-blocking) di `firmware/src/main.cpp`.
- Melakukan eksperimen komparasi mode blocking (`delay`) vs non-blocking dan mencatat data respons tombol.

### Hesi Desta Lestari — Back-End & Data Engineer
- Memastikan struktur payload telemetri JSON memenuhi spesifikasi standar (`device_id`, `seq`, `uptime_ms`, `temp_c`, `hum_pct`, `alert`).
- Menguji validitas format JSON yang dikirim ESP32 melalui Serial Monitor pada Wokwi Simulator.
- Menganalisis kebutuhan skema data dan middleware untuk dikontribusikan pada bagian Lapisan 3 LK-1.
- Menghitung estimasi ukuran payload dan kebutuhan bandwidth/kuota data bulanan untuk laporan praktikum.

### M. Dimas Al-Shiddiq — Security & DevOps Engineer
- Menginisialisasi repositori Git kelompok dengan struktur 5 direktori standar (`/firmware`, `/edge-gateway`, `/backend-api`, `/docker`, `/docs`).
- Membuat berkas `.gitignore` untuk mengecualikan folder build `.pio/`, `.env`, dan cache Python dari repositori.
- Mengatur branching model (feature branches per peran) dan mengarahkan remote repository ke GitHub/GitLab kelompok.
- Menganalisis aspek keamanan topik MQTT dan potensi ancaman tanpa TLS/ACL untuk bagian Lapisan 5 LK-1.

---

## 4. Luaran Wajib (Deliverables) & Ceklis Verifikasi

**4 Luaran Utama Minggu 1:**

1. **Lembar Kerja Kasus 1 (LK-1):** Dokumen analisis arsitektur 5-lapis DAS Air Bengkulu di LMS UNIB (1% NA).
2. **Repositori Git Kelompok:** GitHub/GitLab dengan 5 folder standar, `.gitignore`, dan commit dari 4 anggota tim.
3. **Code Base ESP32 & Wokwi:** Firmware ESP32 non-blocking dengan telemetri JSON valid pada Wokwi.
4. **Laporan Praktikum-0 (Lab-0):** Berkas `docs/laporan-minggu-01.md` di Git + paraf ceklis Asisten Lab.
