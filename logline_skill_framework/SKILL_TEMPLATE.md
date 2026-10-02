---
name: nama-skill-kustom
description: >-
  [WAJIB DIISI DENGAN JELAS] Jelaskan secara spesifik kapan agent HARUS menggunakan skill ini
  dan kapan TIDAK BOLEH menggunakannya. Gunakan sudut pandang orang ketiga.
  Contoh: "Gunakan skill ini ketika user meminta pembuatan sistem quest RPG berbasis Luau di Roblox,
  atau pembuatan skrip dialog interaktif. Jangan gunakan untuk script UI umum."
---

# [Nama Skill]

Ringkasan 1-2 paragraf mengenai tujuan utama dan kapabilitas yang disediakan oleh skill ini.

---

## 1. Prerequisites & Environment Setup

Sebelum menjalankan skill ini, pastikan prasyarat berikut terpenuhi:
- Tools/Dependencies yang dibutuhkan: `[Sebutkan tool, misal: Python 3, Rojo, Luau CLI]`
- File atau direktori konfigurasi yang harus dicek terlebih dahulu.

---

## 2. Core Workflow (Langkah Eksekusi)

Ikuti langkah-langkah berikut secara berurutan:

### Langkah 1: Persiapan & Validasi Input
- Validasi parameter atau konteks yang diberikan oleh user.
- Jika ada file referensi tambahan, baca melalui:
  - Dokumentasi mendalam: [detailed_rules.md](./references/detailed_rules.md)
  - Contoh implementasi: [standard_example.md](./examples/standard_example.md)

### Langkah 2: Eksekusi Utama
1. Jalankan helper script jika ada:
   ```bash
   python ./scripts/helper.py --arg value
   ```
2. Tulis/modifikasi file yang ditargetkan dengan mengikuti pola desain yang telah ditentukan.

### Langkah 3: Verifikasi & Self-Check
- Periksa hasil eksekusi:
  - Pastikan tidak ada syntax error / linting error.
  - Verifikasi output sesuai format yang diharapkan user.
  - Lakukan unit check / assertion test.

---

## 3. Strict Rules & Constraints (DOs & DON'Ts)

### DO (Wajib Dilakukan):
- [Aturan wajib 1]
- [Aturan wajib 2]
- [Aturan wajib 3]

### DON'T (Dilarang Keras):
- [Larangan 1 - misal: Jangan hardcode path tanpa validasi]
- [Larangan 2 - misal: Jangan ubah file original tanpa konfirmasi/duplikasi]
- [Larangan 3 - misal: Jangan gunakan placeholder]

---

## 4. Error Handling & Fallbacks

| Kondisi Error / Hambatan | Tindakan Pemulihan (Recovery Action) |
| :--- | :--- |
| **Tool / Command Gagal** | [Langkah perbaikan atau pesan klarifikasi ke user] |
| **Input Tidak Lengkap** | [Tanyakan klarifikasi spesifik sebelum mengambil asumsi] |
| **Konflik File / Dependency** | [Langkah fallback atau alternatif non-destruktif] |
