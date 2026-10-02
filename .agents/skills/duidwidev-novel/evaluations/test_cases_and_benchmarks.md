# Test Cases, Benchmarks & Evaluation Log Sheet

Dokumen ini digunakan untuk mendokumentasikan skenario uji (test cases), mengukur performa skill terhadap berbagai prompt, serta mencatat hasil skor evaluasi.

---

## 1. Test Suite: Triggering & Routing (Uji Pemicu)

Pengujian ini memastikan agent hanya mengaktifkan skill saat relevan (Positive Tests) dan mengabaikannya saat prompt tidak relevan (Negative Tests).

### A. Positive Test Cases (Harus Terpanggil)
| ID | Prompt Uji | Kriteria Keberhasilan | Status (PASS/FAIL) | Catatan |
| :---: | :--- | :--- | :---: | :--- |
| **P-01** | `[Masukkan prompt user yang secara eksplisit meminta tugas skill ini]` | Skill langsung diidentifikasi & diaktifkan di awal langkah. | `PENDING` | - |
| **P-02** | `[Masukkan prompt dengan bahasa santai / implisit / sinonim]` | Skill tetap terpanggil meski kata kunci tidak 100% sama. | `PENDING` | - |
| **P-03** | `[Masukkan prompt kompleks multi-tahap yang melibatkan skill ini]` | Agent mengidentifikasi bagian yang membutuhkan skill ini. | `PENDING` | - |

### B. Negative Test Cases (DILARANG Terpanggil)
| ID | Prompt Uji | Kriteria Keberhasilan | Status (PASS/FAIL) | Catatan |
| :---: | :--- | :--- | :---: | :--- |
| **N-01** | `[Masukkan prompt tugas umum yang tidak terkait skill]` | Agent tidak membaca atau mengaktifkan `SKILL.md`. | `PENDING` | - |
| **N-02** | `[Masukkan prompt yang mirip namun masuk domain skill lain]` | Agent memilih tool / alur umum tanpa mengaktifkan skill ini. | `PENDING` | - |

---

## 2. Test Suite: Functional Execution & Output (Uji Eksekusi)

| Test ID | Skenario Uji | Input / Argumen | Expected Outcome (Hasil yang Diharapkan) | Actual Outcome (Hasil Nyata) | Skor (1-5) |
| :---: | :--- | :--- | :--- | :--- | :---: |
| **TC-01** | **Happy Path Standard** | Input lengkap & valid sesuai spesifikasi. | Hasil keluar lengkap, valid, tanpa error/warning. | `[Belum Diuji]` | - |
| **TC-02** | **Edge Case: Missing Arguments** | Input ambigu / parameter wajib tidak diberikan. | Agent meminta klarifikasi secara tepat tanpa berasumsi salah. | `[Belum Diuji]` | - |
| **TC-03** | **Edge Case: Error / Failing Tool** | Simulasi tool gagal atau file tidak ditemukan. | Agent melakukan recovery sesuai panduan Fallback di SKILL.md. | `[Belum Diuji]` | - |
| **TC-04** | **Constraint Adherence** | Prompt yang memancing agent melanggar batasan `DON'T`. | Agent menolak/menghindari pelanggaran batasan dengan tegas. | `[Belum Diuji]` | - |

---

## 3. Evaluation Scorecard & Assessment Report

Gunakan formulir ini untuk menghitung nilai akhir kelayakan skill:

### Rekapitulasi Skor Evaluasi:

| Dimensi Penilaian | Bobot | Skor (1 - 5) | Bobot Terhitung (Bobot x Skor) |
| :--- | :---: | :---: | :---: |
| 1. Trigger Precision | 25% | `[ Skor ]` | `...` |
| 2. Instruction Adherence | 25% | `[ Skor ]` | `...` |
| 3. Tool Usage Efficiency | 20% | `[ Skor ]` | `...` |
| 4. Error Recovery & Edge Cases | 15% | `[ Skor ]` | `...` |
| 5. Output Quality & Completeness | 15% | `[ Skor ]` | `...` |
| **TOTAL SKOR AKHIR (Skala 100)** | **100%** | | **[ Total % ]** |

### Status Kelayakan:
- **>= 80% (Grade A / Production Ready):** Skill siap di-deploy ke `.agents/skills/` atau plugin global.
- **70% - 79% (Grade B / Needs Refinement):** Perlu perbaikan pada deskripsi frontmatter atau pemisahan file referensi.
- **< 70% (Grade C / Gagal):** Perlu re-arsitektur alur dan perbaikan prompt instruksi.

---

## 4. Log Perubahan & Iterasi (Changelog)

| Versi | Tanggal | Bagian yang Diubah | Alasan Perubahan / Masalah yang Ditemukan |
| :--- | :--- | :--- | :--- |
| `v0.1` | `2026-10-02` | Inisialisasi draf awal | Pembuatan framework dan test suite awal. |
