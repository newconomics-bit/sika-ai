# SIKA — Software Requirements Specification (SRS)

**Status:** Draft v0.1
**Sumber:** PRD SIKA v0.1 (Draft awal)
**Platform:** Responsive web app, mobile-first
**Pengujian awal:** 3 pengguna
**Pendekatan AI:** Multi-provider, evidence-based research, bertahap

---

## 1. Pendahuluan

### 1.1 Tujuan Dokumen

Dokumen ini adalah Software Requirements Specification (SRS) untuk SIKA, asisten AI yang berfokus pada ekonomi, bisnis, dan keuangan. SRS ini diturunkan dari PRD SIKA v0.1 dan mendefinisikan persyaratan yang dapat diuji sebagai dasar pengembangan dan verifikasi.

Dokumen ini tidak mengubah PRD. Jika terdapat perbedaan antara SRS dan PRD, PRD adalah otoritas yang lebih tinggi.

### 1.2 Visi Produk

Menjadi asisten riset dan pengambilan keputusan yang membantu masyarakat memahami ekonomi, bisnis, dan keuangan secara lebih kritis, terstruktur, dan berbasis bukti.

### 1.3 Prinsip Produk

1. Evidence over confidence.
2. Verifiable claims over unsupported claims.
3. Transparency over false certainty.
4. Useful analysis over unnecessary complexity.
5. Responsible AI usage over uncontrolled model calls.
6. Modular architecture over unnecessary dependencies.
7. Measurable quality over unverified completion claims.

---

## 2. Daftar Persyaratan Fungsional

Setiap persyaratan fungsional memiliki ID unik dalam format `FUNC-###`. Persyaratan ini diturunkan dari PRD Bagian 4 (Ruang Lingkup Versi Pertama), Bagian 6 (Arsitektur Produk), dan Bagian 7 (Pengendalian Biaya AI).

### 2.1 AI Assistant (P0)

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-001 | Sistem MENERIMA pertanyaan terkait ekonomi, bisnis, dan keuangan dalam bahasa alami. | PRD 4.1.A | P0 |
| FUNC-002 | Sistem MENGHASILKAN jawaban yang relevan dengan konteks pertanyaan pengguna (relevansi dievaluasi berdasarkan kaitan jawaban dengan topik dan konteks pertanyaan). | PRD 4.1.A | P0 |
| FUNC-003 | Sistem MENYAMPAIKAN keterbatasan apabila informasi tidak memadai untuk menjawab pertanyaan (ketercukupan informasi dievaluasi berdasarkan sumber yang tersedia dan kebutuhan analisis). | PRD 4.1.A | P0 |
| FUNC-004 | Sistem TIDAK MENGAKU telah melakukan pencarian atau verifikasi apabila proses tersebut tidak dilakukan. | PRD 4.1.A | P0 |
| FUNC-005 | Sistem MENANGANI kegagalan provider AI tanpa kehilangan kendali atas alur aplikasi. | PRD 4.1.A | P0 |

### 2.2 Evidence-Based Research (P0)

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-006 | Sistem MAMPU menjalankan proses riset bertahap untuk pertanyaan yang memerlukan bukti eksternal. | PRD 4.1.B | P0 |
| FUNC-007 | Proses riset meliputi: memahami pertanyaan, menentukan kebutuhan informasi, menyusun strategi pencarian, mengambil sumber eksternal, memeriksa relevansi, membandingkan temuan, menyusun analisis, dan memeriksa dukungan bukti sebelum menyampaikan kesimpulan. | PRD 4.1.B | P0 |
| FUNC-008 | Sumber yang digunakan dalam riset HARUS benar-benar diperoleh melalui proses yang dijalankan oleh sistem. | PRD 4.1.B | P0 |
| FUNC-009 | Klaim yang didukung sumber HARUS dapat ditelusuri ke sumber yang benar-benar digunakan. | PRD 4.1.B | P0 |
| FUNC-010 | Sistem MEMERIKSA tanggal publikasi dan periode data ketika relevan untuk klaim riset. | PRD 4.1.B | P0 |
| FUNC-011 | Sumber yang tidak mendukung suatu klaim TIDAK BOLEH digunakan seolah-olah mendukung klaim tersebut. | PRD 4.1.B | P0 |
| FUNC-012 | Jika sumber tidak cukup, SISTEM HARUS menyatakan keterbatasannya. | PRD 4.1.B | P0 |
| FUNC-013 | Sistem HARUS membedakan hasil pencarian, hasil verifikasi, dan kesimpulan analitis dalam output riset. | PRD 4.1.B | P0 |

### 2.3 Business Analysis (P1)

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-014 | Sistem MEMBANTU pengguna menganalisis ide bisnis, biaya, pendapatan, margin, risiko, dan skenario. | PRD 4.2.C | P1 |
| FUNC-015 | Sistem MENJELAHKAN asumsi yang digunakan dalam analisis bisnis. | PRD 4.2.C | P1 |
| FUNC-016 | Sistem MENUNJUKKAN rumus atau dasar perhitungan yang relevan untuk analisis bisnis. | PRD 4.2.C | P1 |
| FUNC-017 | Sistem MEMBEDAKAN data yang diberikan pengguna dari estimasi sistem. | PRD 4.2.C | P1 |
| FUNC-018 | Sistem TIDAK MENYAJIKAN proyeksi sebagai hasil yang pasti. | PRD 4.2.C | P1 |
| FUNC-019 | Sistem MENGUNGKAPKAN data yang masih dibutuhkan untuk memperkuat analisis bisnis. | PRD 4.2.C | P1 |

### 2.4 Conversation History (P1)

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-020 | Sistem MENGIZINKAN pengguna menyimpan dan membuka kembali percakapan. | PRD 4.2.D | P1 |
| FUNC-021 | Percakapan HARUS terhubung dengan identitas pemiliknya. | PRD 4.2.D | P1 |
| FUNC-022 | Pengguna TIDAK DAPAT membaca percakapan milik akun lain. | PRD 4.2.D | P1 |
| FUNC-023 | Akses data HARUS diperiksa di backend, bukan hanya disembunyikan di antarmuka. | PRD 4.2.D | P1 |
| FUNC-024 | Kebijakan penyimpanan dan penghapusan data HARUS ditentukan sebelum rilis publik. | PRD 4.2.D | P1 |

### 2.5 Multi-User and Data Isolation

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-025 | Sistem HARUS dirancang untuk banyak pengguna sejak awal. | PRD 6.2 | P0 |
| FUNC-026 | Identitas pengguna HARUS dikelola secara aman. | PRD 6.2 | P0 |
| FUNC-027 | Akses ke data HARUS diperiksa di backend. | PRD 6.2 | P0 |
| FUNC-028 | Data setiap pengguna HARUS diisolasi dari pengguna lain. | PRD 6.2 | P0 |
| FUNC-029 | Batas penggunaan HARUS diterapkan per pengguna. | PRD 6.2 | P0 |
| FUNC-030 | Aktivitas penting HARUS dicatat sesuai kebutuhan keamanan. | PRD 6.2 | P0 |
| FUNC-031 | Tidak ada akses lintas akun tanpa izin yang sah. | PRD 6.2 | P0 |

### 2.6 AI Provider Gateway

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-032 | Sistem HARUS dapat menggunakan lebih dari satu penyedia model AI. | PRD 6.1 | P0 |
| FUNC-033 | Konfigurasi provider HARUS berada di backend. | PRD 6.1 | P0 |
| FUNC-034 | API key TIDAK BOLEH dikirim ke browser. | PRD 6.1 | P0 |
| FUNC-035 | Provider HARUS dapat dipilih berdasarkan kebijakan, kemampuan, ketersediaan, dan biaya. | PRD 6.1 | P0 |
| FUNC-036 | Kegagalan provider HARUS dicatat dan ditangani secara terkontrol. | PRD 6.1 | P0 |
| FUNC-037 | Retry HARUS dibatasi. | PRD 6.1 | P0 |
| FUNC-038 | Pergantian provider TIDAK BOLEH mengabaikan kebutuhan kualitas tugas. | PRD 6.1 | P0 |
| FUNC-039 | Sistem HARUS mencatat model yang digunakan dan penggunaan yang relevan untuk evaluasi. | PRD 6.1 | P0 |
| FUNC-040 | Akses gratis HANYA digunakan jika memenuhi ketentuan layanan terkait. | PRD 6.1 | P0 |

### 2.7 Pengendalian Penggunaan AI (Biaya)

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-041 | Penggunaan model HARUS dikendalikan dari backend. | PRD 7 | P0 |
| FUNC-042 | Sistem HARUS menerapkan batas request per pengguna. | PRD 7 | P0 |
| FUNC-043 | Sistem HARUS menerapkan batas pemanggilan model per tugas. | PRD 7 | P0 |
| FUNC-044 | Sistem HARUS menerapkan batas token input dan output. | PRD 7 | P0 |
| FUNC-045 | Sistem HARUS menerapkan batas iterasi riset. | PRD 7 | P0 |
| FUNC-046 | Sistem HARUS menerapkan batas retry. | PRD 7 | P0 |
| FUNC-047 | Sistem HARUS mencatat penggunaan per provider dan model. | PRD 7 | P0 |
| FUNC-048 | Sistem HARUS menangani kondisi kuota habis. | PRD 7 | P0 |
| FUNC-049 | Sistem HARUS menghentikan proses ketika batas penggunaan tercapai. | PRD 7 | P0 |
| FUNC-050 | Ketika kuota habis, SISTEM HARUS memberikan informasi yang jelas. | PRD 7 | P0 |
| FUNC-051 | Sistem TIDAK BOLEH menganggap bahwa provider lain pasti tersedia saat kuota habis. | PRD 7 | P0 |

### 2.8 Standar Bukti dan Kualitas Jawaban

| ID | Persyaratan | Sumber PRD | Prioritas |
|----|-------------|------------|-----------|
| FUNC-052 | Sistem HARUS membedakan empat kategori informasi: fakta terverifikasi, asumsi, interpretasi, dan ketidakpastian. | PRD 5 | P0 |
| FUNC-053 | Kategori informasi TIDAK BOLEH diperlakukan sebagai label yang otomatis menjamin kebenaran. | PRD 5 | P0 |
| FUNC-054 | Sistem HARUS memiliki mekanisme pengujian untuk menilai apakah pelabelan dan kesimpulan sesuai dengan bukti. | PRD 5 | P0 |
| FUNC-055 | Evaluasi sumber eksternal HARUS mencakup: relevansi, kesesuaian dengan klaim, kredibilitas penerbit, kemutakhiran, konsistensi angka/tanggal/satuan, pertentangan antar-sumber, dan keterbatasan data/metode. | PRD 5 | P0 |

---

## 3. Persyaratan Nonfungsional

Persyaratan nonfungsional diturunkan dari PRD Bagian 9 (Persyaratan Nonfungsional) dan Bagian 8 (Keamanan dan Privasi).

### 3.1 Kinerja

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-001 | Aplikasi HARUS responsif pada perangkat seluler. | PRD 9 |
| NFR-002 | Target waktu respons HARUS ditentukan setelah lingkungan deployment dan karakteristik tugas diketahui. | PRD 9 |

### 3.2 Keandalan

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-003 | Kegagalan satu layanan TIDAK BOLEH menyebabkan proses berulang tanpa batas atau kehilangan kendali aplikasi. | PRD 9 |

### 3.3 Skalabilitas

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-004 | Fondasi HARUS mendukung penambahan pengguna tanpa memerlukan perombakan mendasar terhadap pemisahan data dan kontrol akses. | PRD 9 |

### 3.4 Kemudahan Pemeliharaan

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-005 | Integrasi provider, alur riset, autentikasi, dan antarmuka HARUS memiliki batas tanggung jawab yang jelas. | PRD 9 |

### 3.5 Observabilitas

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-006 | Sistem HARUS mencatat informasi yang cukup untuk mengevaluasi error, penggunaan AI, biaya, dan hasil pengujian tanpa mengumpulkan data sensitif secara berlebihan. | PRD 9 |

### 3.6 Aksesibilitas

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-007 | Antarmuka HARUS dapat digunakan pada layar HP dengan struktur navigasi dan teks yang jelas. | PRD 9 |

### 3.7 Keamanan dan Privasi

| ID | Persyaratan | Sumber PRD |
|----|-------------|------------|
| NFR-008 | Rahasia aplikasi HARUS disimpan di sisi server. | PRD 8 |
| NFR-009 | Input pengguna HARUS diperlakukan sebagai data yang tidak otomatis tepercaya. | PRD 8 |
| NFR-010 | Konten eksternal TIDAK BOLEH mengesampingkan instruksi sistem hanya karena ditemukan dalam proses riset. | PRD 8 |
| NFR-011 | Akses data HARUS dibatasi sesuai identitas dan izin pengguna. | PRD 8 |
| NFR-012 | Kesalahan TIDAK BOLEH membocorkan kredensial atau informasi internal sensitif. | PRD 8 |
| NFR-013 | Log TIDAK BOLEH menyimpan data sensitif tanpa kebutuhan dan kontrol yang jelas. | PRD 8 |
| NFR-014 | Pemanggilan alat eksternal HARUS dibatasi sesuai izin. | PRD 8 |
| NFR-015 | Proses audit dan pengujian keamanan HARUS dilakukan dengan bukti yang dapat ditinjau. | PRD 8 |

---

## 4. Persyaratan Alur Riset dan Pemeriksaan Bukti

Persyaratan berikut menggambarkan alur riset yang diharapkan dan mekanisme pemeriksaan bukti, diturunkan dari PRD Bagian 4.1.B dan Bagian 5.

### 4.1 Alur Riset

1. **Memahami pertanyaan:** Sistem menganalisis pertanyaan pengguna untuk menentukan apakah bukti eksternal diperlukan.
2. **Menentukan kebutuhan informasi:** Sistem mengidentifikasi jenis informasi yang diperlukan untuk menjawab pertanyaan.
3. **Menyusun strategi pencarian:** Sistem merencanakan pendekatan pencarian sumber eksternal.
4. **Mengambil sumber eksternal:** Sistem mengambil sumber melalui layanan pencarian yang dikonfigurasi.
5. **Memeriksa relevansi:** Sistem memverifikasi apakah sumber yang ditemukan relevan dengan klaim.
6. **Membandingkan temuan:** Sistem membandingkan informasi dari berbagai sumber dan mengidentifikasi pertentangan.
7. **Menyusun analisis:** Sistem menyusun analisis berdasarkan temuan yang diverifikasi.
8. **Memeriksa dukungan bukti:** Sistem memverifikasi bahwa klaim didukung oleh sumber yang benar sebelum menyampaikan kesimpulan.

### 4.2 Pemeriksaan Bukti

| ID | Persyaratan Pemeriksaan | Kriteria Penerimaan |
|----|------------------------|---------------------|
| EVID-001 | Sumber benar-benar diperoleh melalui proses yang dijalankan | Bukti eksekusi proses pencarian dapat ditinjau |
| EVID-002 | Klaim dapat ditelusuri ke sumber | Setiap klaim yang didukung sumber memiliki referensi ke sumber yang spesifik |
| EVID-003 | Tanggal publikasi diperhatikan | Tanggal publikasi dicantumkan untuk klaim yang bergantung pada waktu |
| EVID-004 | Sumber tidak mendukung klaim tidak digunakan | Tidak ada klaim yang mengaitkan sumber yang tidak mendukungnya |
| EVID-005 | Sumber tidak cukup dinyatakan | Sistem mengeluarkan pernyataan keterbatasan saat sumber tidak memadai |
| EVID-006 | Beda hasil pencarian, verifikasi, dan kesimpulan | Output riset secara jelas memisahkan ketiga komponen tersebut |

---

## 5. Persyaratan AI Provider Gateway

Persyaratan berikut menggambarkan gateway untuk penyedia model AI multi-provider, diturunkan dari PRD Bagian 6.1.

| ID | Persyaratan | Kriteria Penerimaan |
|----|-------------|---------------------|
| GATE-001 | Konfigurasi provider berada di backend | Tidak ada konfigurasi provider yang disimpan atau diekspose di frontend |
| GATE-002 | API key tidak dikirim ke browser | Tidak ada API key yang muncul dalam request dari browser |
| GATE-003 | Provider dapat dipilih berdasarkan kebijakan, kemampuan, ketersediaan, dan biaya | Sistem mendukung pemilihan provider berdasarkan kebijakan, kemampuan, ketersediaan, dan biaya yang dikonfigurasi di backend |
| GATE-004 | Kegagalan provider dicatat dan ditangani secara terkontrol | Log error tersedia; sistem tidak crash saat provider gagal |
| GATE-005 | Retry dibatasi | Jumlah retry maksimum dikonfigurasi dan dapat ditinjau |
| GATE-006 | Pergantian provider tidak mengabaikan kebutuhan kualitas tugas | Pergantian provider mempertahankan standar kualitas yang ditetapkan untuk tugas |
| GATE-007 | Sistem mencatat model dan penggunaan untuk evaluasi | Log penggunaan mencatat model yang digunakan dan metrik penggunaan yang relevan |
| GATE-008 | Akses gratis hanya jika memenuhi ketentuan layanan | Sistem hanya menggunakan endpoint gratis yang sesuai dengan ToS provider |

---

## 6. Persyaratan Multi-User dan Isolasi Data

Persyaratan berikut menggambarkan isolasi data dan kontrol akses multi-user, diturunkan dari PRD Bagian 6.2 dan Bagian 4.2.D.

| ID | Persyaratan | Kriteria Penerimaan |
|----|-------------|---------------------|
| MULTI-001 | Identitas pengguna dikelola secara aman | Sistem autentikasi mengonfirmasi identitas pengguna sebelum memberikan akses |
| MULTI-002 | Akses ke data diperiksa di backend | Setiap request data divalidasi otorisasi di lapisan backend |
| MULTI-003 | Data setiap pengguna diisolasi | Pengguna A tidak dapat mengakses data, percakapan, atau riwayat milik pengguna B |
| MULTI-004 | Batas penggunaan diterapkan per pengguna | Setiap pengguna memiliki kuota penggunaan yang terpisah dan dilacak |
| MULTI-005 | Aktivitas penting dicatat sesuai kebutuhan keamanan | Log audit mencatat aktivitas yang relevan dengan keamanan |
| MULTI-006 | Tidak ada akses lintas akun tanpa izin yang sah | Tidak ada mekanisme yang memungkinkan akses data lintas akun tanpa otorisasi |

---

## 7. Pengendalian Penggunaan AI

Persyaratan berikut menggambarkan kontrol penggunaan model AI, diturunkan dari PRD Bagian 7.

| ID | Persyaratan | Kriteria Penerimaan |
|----|-------------|---------------------|
| USAGE-001 | Penggunaan model dikendalikan dari backend | Semua pemanggilan model melewati lapisan kontrol backend |
| USAGE-002 | Batas request per pengguna | Sistem menolak request yang melebihi batas per pengguna |
| USAGE-003 | Batas pemanggilan model per tugas | Sistem membatasi jumlah pemanggilan model untuk satu tugas |
| USAGE-004 | Batas token input dan output | Sistem membatasi jumlah token input dan output per pemanggilan |
| USAGE-005 | Batas iterasi riset | Sistem membatasi jumlah iterasi dalam proses riset |
| USAGE-006 | Batas retry | Sistem membatasi jumlah percobaan ulang saat kegagalan |
| USAGE-007 | Pencatatan penggunaan per provider dan model | Log penggunaan mencakup detail per provider dan model |
| USAGE-008 | Penanganan kuota habis | Sistem memberikan respons yang jelas saat kuota habis |
| USAGE-009 | Penghentian proses saat batas tercapai | Sistem menghentikan proses saat batas penggunaan tercapai |
| USAGE-010 | Informasi yang jelas saat kuota habis | Pesan error atau pemberitahuan kuota habis disampaikan dalam bahasa yang digunakan pengguna, tanpa jargon teknis yang tidak perlu |
| USAGE-011 | Tidak mengasumsikan provider lain tersedia | Sistem tidak mengalihkan ke provider lain secara otomatis tanpa verifikasi ketersediaan |

---

## 8. Error Handling

Persyaratan berikut menggambarkan penanganan kesalahan dalam sistem, diturunkan dari PRD Bagian 4.1.A, Bagian 6.1, dan Bagian 8.

| ID | Persyaratan | Kriteria Penerimaan |
|----|-------------|---------------------|
| ERR-001 | Kegagalan provider AI tidak menyebabkan kehilangan kendali aplikasi | Aplikasi tetap responsif saat provider gagal |
| ERR-002 | Kegagalan provider dicatat | Log error mencakup detail kegagalan provider |
| ERR-003 | Kesalahan tidak membocorkan kredensial | Pesan error tidak menyertakan API key, kredensial, atau informasi sensitif |
| ERR-004 | Log tidak menyimpan data sensitif tanpa kontrol | Log audit tidak mencakup data sensitif pengguna tanpa kebutuhan yang jelas |
| ERR-005 | Kegagalan satu layanan tidak menyebabkan proses berulang tanpa batas | Sistem memiliki mekanisme pembatas pada retry dan loop error |
| ERR-006 | Sistem menangani kegagalan pencarian web | Sistem memberikan respons yang sesuai saat layanan pencarian tidak tersedia |

---

## 9. Kriteria Penerimaan yang Dapat Diuji

Kriteria penerimaan berikut diturunkan dari PRD Bagian 11 (Indikator Keberhasilan) dan Bagian 10 (Strategi Pengujian).

| ID | Kriteria Penerimaan | Metode Verifikasi |
|----|---------------------|-------------------|
| ACC-001 | Alur utama dapat diselesaikan oleh ketiga pengguna pengujian | Pengujian fungsional oleh 3 pengguna pengujian |
| ACC-002 | Pengguna dapat mengakses fitur sesuai izin | Pengujian otorisasi dan kontrol akses |
| ACC-003 | Tidak ditemukan kebocoran data lintas akun pada skenario pengujian yang ditentukan | Pengujian isolasi data antar-pengguna |
| ACC-004 | Klaim riset dapat ditelusuri ke sumber yang benar-benar digunakan | Verifikasi referensi sumber dalam output riset |
| ACC-005 | Sistem tidak mengaku pencarian yang tidak dilakukan dan tidak mengarang sumber | Pengujian skenario: pencarian tidak dijalankan, dan pencarian tidak menemukan sumber |
| ACC-006 | Perhitungan pada skenario uji sesuai dengan hasil yang diharapkan | Pengujian perhitungan analisis bisnis |
| ACC-007 | Penggunaan model tercatat dan batas penggunaan berfungsi | Verifikasi log penggunaan dan pengujian batas |
| ACC-008 | Kegagalan provider ditangani secara terkendali | Pengujian simulasi kegagalan provider |
| ACC-009 | Integration test untuk backend, database, provider, dan layanan pencarian telah lulus | Eksekusi integration test suite |
| ACC-010 | Contract test untuk integrasi eksternal telah lulus | Eksekusi contract test |
| ACC-011 | Test isolasi data antar-pengguna telah lulus | Eksekusi test isolasi data |
| ACC-012 | Test batas penggunaan dan kegagalan provider telah lulus | Eksekusi test batas penggunaan |
| ACC-013 | Test keamanan yang relevan dengan arsitektur telah lulus | Eksekusi test keamanan |
| ACC-014 | Evaluasi kualitas jawaban dan dukungan bukti telah dilakukan | Evaluasi kualitas output AI |
| ACC-015 | Regression test setelah perubahan telah lulus | Eksekusi regression test suite |
| ACC-016 | Pengujian alur utama pada perangkat seluler telah dilakukan | Pengujian pada perangkat seluler |
| ACC-017 | Setiap langkah alur riset berbasis bukti dapat diverifikasi secara individu | Pengujian setiap langkah riset secara terpisah dengan bukti eksekusi yang dapat ditinjau: (1) memahami pertanyaan — verifikasi catatan analisis awal tersedia; (2) menentukan kebutuhan informasi — verifikasi daftar kebutuhan tercatat; (3) menyusun strategi pencarian — verifikasi strategi tersusun dan diterapkan; (4) mengambil sumber eksternal — verifikasi log pencarian dan daftar sumber tersedia; (5) memeriksa relevansi sumber terhadap klaim — verifikasi penilaian relevansi per sumber tersedia; (6) membandingkan temuan dan mengidentifikasi pertentangan — verifikasi dokumen perbandingan temuan tersedia; (7) menyusun analisis — verifikasi dokumen analisis disusun berdasarkan temuan; (8) memeriksa dukungan bukti sebelum menyampaikan kesimpulan — verifikasi setiap klaim memiliki referensi sumber (ACC-004) |
| ACC-018 | Evaluasi sumber eksternal mencakup relevansi, kesesuaian sumber dengan klaim, kredibilitas penerbit, pemeriksaan tanggal publikasi dan periode data, konsistensi angka/tanggal/satuan, konflik sumber, dan keterbatasan data/metode | Evaluasi setiap sumber eksternal terhadap kriteria relevansi, kesesuaian dengan klaim, kredibilitas, kemutakhiran, konsistensi, konflik, dan keterbatasan |
| ACC-019 | Kebijakan penyimpanan dan penghapusan data ditentukan dan dokumentasi tersedia sebelum rilis publik | Verifikasi keberadaan dokumen kebijakan retensi dan penghapusan data sebelum rilis |
| ACC-020 | Akses gratis hanya digunakan pada endpoint yang memenuhi ketentuan layanan penyedia | Verifikasi bahwa hanya endpoint gratis yang sesuai ToS provider yang digunakan |

ACC-010 dan ACC-015 adalah kriteria pengujian lintas sistem yang berasal dari PRD Section 10 (Strategi Pengujian). ACC-010 (contract test untuk integrasi eksternal) dipetakan ke delapan requirement dalam matriks traceability (FUNC-032, FUNC-033, FUNC-035, FUNC-038, NFR-004, NFR-005, GATE-001, GATE-003, GATE-006). ACC-015 (regression test setelah perubahan) tidak dipetakan ke requirement manapun dalam Requirements Traceability Matrix, dan hal ini disengaja karena regression test merupakan kewajiban pengujian lintas sistem, bukan untuk satu requirement individual. Keberadaan keduanya dalam dokumen ini tidak berarti pengujian telah dilaksanakan atau lulus; keduanya hanya mendefinisikan kewajiban pengujian yang kelak harus diuji.

---

## 10. Requirements Traceability Matrix

Matriks ini memetakan persyaratan SRS ke bagian PRD yang relevan dan kriteria penerimaan yang dapat diuji. Matriks berisi 107 baris pemetaan, satu per ID persyaratan unik SRS (55 FUNC, 15 NFR, 6 EVID, 8 GATE, 6 MULTI, 11 USAGE, 6 ERR). Beberapa persyaratan dipetakan ke lebih dari satu kriteria penerimaan, sehingga total relasi SRS ke ACC adalah 129.

| ID SRS | ID PRD | Deskripsi Singkat | Kriteria Penerimaan |
|--------|--------|-------------------|---------------------|
| FUNC-001 | PRD 4.1.A | Terima pertanyaan bahasa alami | ACC-001 |
| FUNC-002 | PRD 4.1.A | Jawaban relevan dengan konteks | ACC-001 |
| FUNC-003 | PRD 4.1.A | Sampaikan keterbatasan informasi | ACC-001 |
| FUNC-004 | PRD 4.1.A | Tidak mengaku pencarian yang tidak dilakukan | ACC-005 |
| FUNC-005 | PRD 4.1.A | Tangani kegagalan provider | ACC-008 |
| FUNC-006 | PRD 4.1.B | Riset bertahap | ACC-004 |
| FUNC-007 | PRD 4.1.B | Langkah-lengkap riset | ACC-004, ACC-017 |
| FUNC-008 | PRD 4.1.B | Sumber diperoleh melalui proses | ACC-004 |
| FUNC-009 | PRD 4.1.B | Klaim dapat ditelusuri ke sumber | ACC-004 |
| FUNC-010 | PRD 4.1.B | Tanggal publikasi diperhatikan | ACC-018 |
| FUNC-011 | PRD 4.1.B | Sumber tidak mendukung tidak dipakai | ACC-005 |
| FUNC-012 | PRD 4.1.B | Sumber tidak cukup dinyatakan | ACC-005 |
| FUNC-013 | PRD 4.1.B | Beda pencarian, verifikasi, kesimpulan | ACC-004 |
| FUNC-014 | PRD 4.2.C | Analisis bisnis | ACC-006 |
| FUNC-015 | PRD 4.2.C | Jelaskan asumsi | ACC-006 |
| FUNC-016 | PRD 4.2.C | Rumus perhitungan | ACC-006 |
| FUNC-017 | PRD 4.2.C | Beda data pengguna vs estimasi | ACC-006 |
| FUNC-018 | PRD 4.2.C | Proyeksi bukan hasil pasti | ACC-006 |
| FUNC-019 | PRD 4.2.C | Ungkap data yang dibutuhkan | ACC-006 |
| FUNC-020 | PRD 4.2.D | Simpan dan buka percakapan | ACC-001 |
| FUNC-021 | PRD 4.2.D | Percakapan terhubung identitas | ACC-002 |
| FUNC-022 | PRD 4.2.D | Tidak bisa baca percakapan orang lain | ACC-003 |
| FUNC-023 | PRD 4.2.D | Akses data diperiksa di backend | ACC-002, ACC-009 |
| FUNC-024 | PRD 4.2.D | Kebijakan penyimpanan sebelum rilis | ACC-019 |
| FUNC-025 | PRD 6.2 | Dukungan banyak pengguna | ACC-003 |
| FUNC-026 | PRD 6.2 | Identitas aman | ACC-002 |
| FUNC-027 | PRD 6.2 | Akses data diperiksa di backend | ACC-002, ACC-009 |
| FUNC-028 | PRD 6.2 | Isolasi data pengguna | ACC-003, ACC-011 |
| FUNC-029 | PRD 6.2 | Batas penggunaan per pengguna | ACC-007, ACC-012 |
| FUNC-030 | PRD 6.2 | Aktivitas penting dicatat | ACC-013 |
| FUNC-031 | PRD 6.2 | Tidak ada akses lintas akun | ACC-003, ACC-011 |
| FUNC-032 | PRD 6.1 | Multi-provider AI | ACC-010 |
| FUNC-033 | PRD 6.1 | Konfigurasi provider di backend | ACC-010 |
| FUNC-034 | PRD 6.1 | API key tidak ke browser | ACC-014 |
| FUNC-035 | PRD 6.1 | Seleksi provider berdasarkan kebijakan | ACC-010 |
| FUNC-036 | PRD 6.1 | Kegagalan provider dicatat dan ditangani | ACC-008 |
| FUNC-037 | PRD 6.1 | Retry dibatasi | ACC-013 |
| FUNC-038 | PRD 6.1 | Pergantian provider tidak abaikan kualitas | ACC-010 |
| FUNC-039 | PRD 6.1 | Catat model dan penggunaan | ACC-007 |
| FUNC-040 | PRD 6.1 | Akses gratis sesuai ketentuan | ACC-020 |
| FUNC-041 | PRD 7 | Kontrol penggunaan dari backend | ACC-007 |
| FUNC-042 | PRD 7 | Batas request per pengguna | ACC-007, ACC-012 |
| FUNC-043 | PRD 7 | Batas pemanggilan model per tugas | ACC-007, ACC-012 |
| FUNC-044 | PRD 7 | Batas token input/output | ACC-007, ACC-012 |
| FUNC-045 | PRD 7 | Batas iterasi riset | ACC-007, ACC-012 |
| FUNC-046 | PRD 7 | Batas retry | ACC-007, ACC-012 |
| FUNC-047 | PRD 7 | Catat penggunaan per provider dan model | ACC-007 |
| FUNC-048 | PRD 7 | Tangani kuota habis | ACC-007, ACC-012 |
| FUNC-049 | PRD 7 | Hentikan proses saat batas tercapai | ACC-007, ACC-012 |
| FUNC-050 | PRD 7 | Informasi jelas saat kuota habis | ACC-007 |
| FUNC-051 | PRD 7 | Tidak mengasumsikan provider lain tersedia | ACC-008 |
| FUNC-052 | PRD 5 | Empat kategori informasi | ACC-014 |
| FUNC-053 | PRD 5 | Kategori bukan jaminan kebenaran | ACC-014 |
| FUNC-054 | PRD 5 | Mekanisme pengujian pelabelan | ACC-014 |
| FUNC-055 | PRD 5 | Evaluasi sumber eksternal | ACC-018 |
| NFR-001 | PRD 9 | Responsif seluler | ACC-016 |
| NFR-002 | PRD 9 | Target waktu respons ditentukan nanti | (Open decision) |
| NFR-003 | PRD 9 | Kegagalan tidak menyebabkan loop tanpa batas | ACC-008 |
| NFR-004 | PRD 9 | Skalabilitas tanpa perombakan | ACC-010 |
| NFR-005 | PRD 9 | Batas tanggung jawab jelas | ACC-009 |
| NFR-006 | PRD 9 | Observabilitas tanpa data sensitif berlebihan | ACC-014 |
| NFR-007 | PRD 9 | Aksesibilitas layar HP | ACC-016 |
| NFR-008 | PRD 8 | Rahasia di sisi server | ACC-014 |
| NFR-009 | PRD 8 | Input sebagai data tidak tepercaya | ACC-014 |
| NFR-010 | PRD 8 | Konten eksternal tidak mengesampingkan instruksi | ACC-014 |
| NFR-011 | PRD 8 | Akses data sesuai identitas | ACC-002 |
| NFR-012 | PRD 8 | Kesalahan tidak bocorkan kredensial | ACC-014 |
| NFR-013 | PRD 8 | Log tidak simpan data sensitif | ACC-014 |
| NFR-014 | PRD 8 | Pemanggilan alat eksternal sesuai izin | ACC-014 |
| NFR-015 | PRD 8 | Audit dengan bukti yang dapat ditinjau | ACC-014 |
| EVID-001 | PRD 4.1.B | Sumber diperoleh melalui proses | ACC-004 |
| EVID-002 | PRD 4.1.B | Klaim dapat ditelusuri | ACC-004 |
| EVID-003 | PRD 4.1.B | Tanggal publikasi diperhatikan | ACC-004 |
| EVID-004 | PRD 4.1.B | Sumber tidak mendukung tidak dipakai | ACC-005 |
| EVID-005 | PRD 4.1.B | Sumber tidak cukup dinyatakan | ACC-005 |
| EVID-006 | PRD 4.1.B | Beda komponen riset | ACC-004 |
| GATE-001 | PRD 6.1 | Konfigurasi provider di backend | ACC-010 |
| GATE-002 | PRD 6.1 | API key tidak ke browser | ACC-013 |
| GATE-003 | PRD 6.1 | Seleksi provider | ACC-010 |
| GATE-004 | PRD 6.1 | Kegagalan provider ditangani | ACC-008 |
| GATE-005 | PRD 6.1 | Retry dibatasi | ACC-012 |
| GATE-006 | PRD 6.1 | Pergantian provider tidak abaikan kualitas | ACC-010 |
| GATE-007 | PRD 6.1 | Catat model dan penggunaan | ACC-007 |
| GATE-008 | PRD 6.1 | Akses gratis sesuai ketentuan | ACC-020 |
| MULTI-001 | PRD 6.2 | Identitas aman | ACC-002 |
| MULTI-002 | PRD 6.2 | Akses data diperiksa di backend | ACC-002 |
| MULTI-003 | PRD 6.2 | Isolasi data | ACC-003, ACC-011 |
| MULTI-004 | PRD 6.2 | Batas penggunaan per pengguna | ACC-007, ACC-012 |
| MULTI-005 | PRD 6.2 | Aktivitas penting dicatat | ACC-013 |
| MULTI-006 | PRD 6.2 | Tidak ada akses lintas akun | ACC-003, ACC-011 |
| USAGE-001 | PRD 7 | Kontrol backend | ACC-007 |
| USAGE-002 | PRD 7 | Batas request per pengguna | ACC-007, ACC-012 |
| USAGE-003 | PRD 7 | Batas pemanggilan model per tugas | ACC-007, ACC-012 |
| USAGE-004 | PRD 7 | Batas token | ACC-007, ACC-012 |
| USAGE-005 | PRD 7 | Batas iterasi riset | ACC-007, ACC-012 |
| USAGE-006 | PRD 7 | Batas retry | ACC-007, ACC-012 |
| USAGE-007 | PRD 7 | Catat penggunaan per provider | ACC-007 |
| USAGE-008 | PRD 7 | Penanganan kuota habis | ACC-007, ACC-012 |
| USAGE-009 | PRD 7 | Hentikan proses saat batas tercapai | ACC-007, ACC-012 |
| USAGE-010 | PRD 7 | Informasi jelas kuota habis | ACC-007 |
| USAGE-011 | PRD 7 | Tidak mengasumsikan provider lain | ACC-008 |
| ERR-001 | PRD 4.1.A | Kegagalan provider tidak kehilangan kendali | ACC-008 |
| ERR-002 | PRD 6.1 | Kegagalan provider dicatat | ACC-008 |
| ERR-003 | PRD 8 | Kesalahan tidak bocorkan kredensial | ACC-014 |
| ERR-004 | PRD 8 | Log tidak simpan data sensitif | ACC-014 |
| ERR-005 | PRD 9 | Tidak ada loop error tanpa batas | ACC-008 |
| ERR-006 | PRD 4.1.B | Tangani kegagalan pencarian web | ACC-008 |

---

## 11. Keputusan Terbuka dan Risiko

### 11.1 Keputusan yang Belum Final (dari PRD Bagian 13 dan Section 6.2)

Berikut adalah daftar keputusan yang belum boleh dianggap diputuskan, sesuai dengan PRD Bagian 13 dan PRD Section 6.2:

1. Pilihan framework frontend dan backend.
2. Teknologi autentikasi pengguna belum ditentukan (PRD Section 6.2).
3. Pilihan database dan layanan hosting.
4. Penyedia dan implementasi pencarian web belum ditentukan (PRD Section 4.1.B).
5. Model AI yang dipakai untuk setiap jenis tugas.
6. Kebijakan retensi dan penghapusan data.
7. Anggaran operasional bulanan.
8. Kebijakan penggunaan setelah kuota gratis habis.
9. Ambang numerik untuk kinerja dan kualitas.
10. Model bisnis dan monetisasi.
11. Lisensi distribusi produk.

### 11.2 Risiko yang Teridentifikasi

| Risiko | Dampak | Mitigasi | Status |
|--------|--------|----------|--------|
| Web search provider belum ditentukan | Tidak dapat memulai integrasi pencarian | Ditunda ke tahap desain teknis | Terbuka |
| Model AI untuk setiap tugas belum ditentukan | Tidak dapat mengonfigurasi provider gateway | Ditunda ke tahap desain teknis | Terbuka |
| Nilai numerik batas penggunaan belum ditetapkan | Tidak dapat mengimplementasi pengendalian biaya | Ditentukan setelah pengujian awal | Terbuka |
| Kebijakan retensi dan penghapusan data belum ditentukan | Tidak dapat mengimplementasi Conversation History secara penuh | Ditentukan sebelum rilis publik | Terbuka |
| Target waktu respons belum ditentukan | Tidak dapat mengukur kinerja | Ditentukan setelah deployment dan karakteristik tugas diketahui | Terbuka |
| Teknologi autentikasi belum ditentukan | Tidak dapat mengimplementasi isolasi data dan akses pengguna | Ditunda ke tahap desain teknis | Terbuka |
| Database dan hosting belum ditentukan | Tidak dapat menyimpan data pengguna secara terisolasi | Ditunda ke tahap desain teknis | Terbuka |
| Audit keamanan belum dilakukan | Risiko keamanan tidak teridentifikasi | Dilakukan pada Tahap 5 | Terbuka |

### 11.3 Catatan

- Semua keputusan terbuka di atas tercantum dalam PRD Bagian 13, Section 6.2, dan Section 4.1.B dan tidak boleh dianggap diputuskan.
- Nilai numerik untuk batas penggunaan, kinerja, dan kualitas ditentukan setelah pengujian awal dan evaluasi kuota aktual, sesuai PRD Bagian 7 dan 11.
- Teknologi autentikasi belum ditentukan, sesuai PRD Bagian 6.2.
- Database dan hosting belum ditentukan, sesuai PRD Bagian 6.2.
- Detail kontrol, ancaman, dan prosedur verifikasi keamanan akan ditentukan dalam dokumen Security & Verification Plan terpisah, sesuai PRD Bagian 8.

---

## 12. Referensi

- PRD SIKA v0.1 (Draft awal) — dokumen sumber untuk SRS ini.
- SIKA Product Vision — asisten riset dan pengambilan keputusan berbasis bukti untuk ekonomi, bisnis, dan keuangan.

---

*Dokumen ini adalah rancangan spesifikasi perangkat lunak, bukan bukti bahwa implementasi, integrasi, atau pengujian telah dilakukan.*