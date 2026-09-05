# Dev & Data Engineering Suite — 29 Computational Tools

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3.0+-003B57?style=flat-square&logo=sqlite&logoColor=white)](https://sqlite.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4+-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)

Platform utilitas mandiri yang mengintegrasikan 29 modul komputasi rekayasa perangkat lunak, administrasi jaringan IPv4, hardening keamanan sistem, data wrangling/inspeksi tabular, dan kalkulator hardware server.

---

## 4 Pilar Utama & Inventaris Modul

### 1. Jaringan & Infrastruktur Server (5 Modul)
1. **IP Subnetting & VLSM Calculator:** Menghitung Network ID, Broadcast, Subnet Mask, Host Range, dan representasi biner IPv4 (RFC 791/RFC 4632).
2. **Port Directory & Firewall Rules:** Direktori pencarian port standar dan generator syntax firewall otomatis untuk Linux UFW, iptables, dan Mikrotik RouterOS.
3. **Bandwidth & Data Transfer Estimator:** Kalkulator durasi migrasi server dan backup data dengan faktor efisiensi TCP/IP overhead (80-90%).
4. **Streaming Bitrate & Storage Estimator:** Kalkulasi bandwidth ingest/egress dan kapasitas disk rekaman DVR untuk Nginx RTMP, HLS, dan RTSP.
5. **Cron Task Scheduler Builder:** Visualizer crontab 5-field dengan simulasi jadwal eksekusi 5 waktu mendatang.

### 2. Keamanan Sistem & Hardening (6 Modul)
6. **Auth & Security Service:** Registrasi pengguna, hashing password Bcrypt (Salt 10), penerbitan token JWT stateless, dan penyimpanan SQLite.
7. **Security Headers Analyzer:** Audit kepatuhan HTTP Security Headers standar OWASP (CSP, HSTS, X-Frame-Options, MIME-sniffing) dengan kalkulasi skor grade A+ hingga F.
8. **Crypto Hash & Integrity Verifier:** Perhitungan hash SHA-256, SHA-512, SHA-1, MD5, dan HMAC via Web Crypto API untuk verifikasi integritas file.
9. **Password Entropy & Brute-Force Estimator:** Kalkulator bit entropi Shannon dan estimasi waktu retak serangan CPU vs GPU cluster.
10. **Security Payload Encoder / Decoder:** Sanitasi dan konversi multi-format: Base64, Hexadecimal, URL-Encoding, HTML Entities, dan Unicode.
11. **JWT Inspector & Claims Debugger:** Dekonstruksi struktur Header, Payload claims, expiry timestamp, dan verifikasi signature HMACSHA256.

### 3. Data & Rekayasa Backend (9 Modul)
12. **Tabular Data Cleaner & Imputation Studio:** Pembersihan data kotor, deduplikasi, imputasi missing values (mean, median, mode), format tanggal ISO-8601, dan ekspor skrip Python Pandas.
13. **Dataset Integration & Quality Control (QC) Inspector:** Penilaian skor kesehatan dataset, deteksi outlier statistik Tukey's IQR ($1.5 \times \text{IQR}$), dan simulasi table join relasional (Inner, Left, Right, Full).
14. **Periodic Report & KPI Monitoring Dashboard:** Rekapitulasi laporan operasional harian/mingguan/bulanan dengan variance analysis dan tracking capaian target.
15. **Spreadsheet Formula Simulator & Data Reshaper:** Simulasi dua arah XLOOKUP/VLOOKUP, Pivot Table GroupBy matrix, dan konversi syntax ke SQL/Pandas.
16. **NLP Sentiment & Data Analyzer:** Ingesti file CSV ulasan dan kalkulasi compound polarity score sentimen berbasis VADER NLP.
17. **Inventory & Warehouse CRUD Sandbox:** Simulasi manajemen inventaris aset berbasis RESTful HTTP methods (GET, POST, PUT, DELETE) dengan low-stock trigger.
18. **Library Management System:** Pengelolaan katalog buku relasional dan transaksi peminjaman dengan integritas transaksi ACID SQLite.
19. **JSON to SQL / CSV Converter:** Transformasi array JSON mentah menjadi skema DDL `CREATE TABLE`, batch `INSERT INTO` DML, dan CSV terstruktur.
20. **Nginx Access Log Analyzer:** Parsing regex access log server untuk statistik kode status 2xx/4xx/5xx dan aggregasi top IP pengunjung.

### 4. Utilitas & Hardware (9 Modul)
21. **API Health & Latency Checker:** Pengujian latensi RTT (ms) endpoint REST API real-time dan formatted JSON payload inspection.
22. **Image Optimizer & Converter:** Kompresi gambar Canvas client-side dan konversi format WebP/PNG/JPG menghemat hingga 70% ukuran file.
23. **Real-Time Currency Calculator:** Kalkulator kurs valuta asing live (USD, IDR, EUR, SGD, JPY) dengan cache offline LocalStorage.
24. **Typing Speed & Accuracy Test:** Uji benchmark kecepatan ketik 60 detik dengan metrik Words Per Minute (WPM) dan akurasi %.
25. **RAID Storage & Capacity Calculator:** Kalkulasi kapasitas usable, parity overhead, dan fault tolerance drive untuk RAID 0, 1, 5, 6, dan 10.
26. **PC Power Supply (PSU) Calculator:** Estimasi konsumsi daya listrik komponen PC (CPU, GPU, RAM, NVMe, HDD, Fans) untuk standarisasi PC deployment kantor.
27. **Tech News & Feeds Scraper:** Ekstraksi feed berita teknologi otomatis.
28. **Regex Tester & Validator:** Evaluator pola Regular Expression dengan match highlighter visual dan template preset umum.
29. **Markdown Live Editor & Preview:** Editor markdown real-time dengan render HTML semantik, tabel, code block, dan fitur salin HTML.

---

## Struktur Direktori

```text
dev-tools/
├── index.html                  # Antarmuka Web Utama (29 Tools & Modal Workspace)
├── app.js                      # Master Registry 29 Tools, Filter Kategori & i18n
├── js/                         # Modul JavaScript Setiap Tool
│   ├── code-snippets.js        # Database Source Code Asli Inspector
│   ├── data-cleaner-studio.js  # Tabular Data Wrangling & Imputasi
│   ├── data-qc-inspector.js    # Quality Control & Relational Table Joiner
│   ├── kpi-monitoring-dashboard.js # Dashboard KPI & Laporan Berkala
│   ├── spreadsheet-formula-engine.js # XLOOKUP Simulator & Pivot Matrix
│   ├── subnet-calculator.js    # IPv4 / CIDR / VLSM Subnetting Engine
│   ├── firewall-generator.js   # Linux UFW / iptables / Mikrotik Builder
│   ├── bandwidth-estimator.js  # Estimasi Throughput & Durasi Transfer
│   ├── streaming-calculator.js # Kalkulator Bitrate RTMP/HLS & Storage
│   ├── cron-builder.js         # Generator Crontab Linux 5-Field
│   ├── auth-sandbox.js         # Simulasi Autentikasi Bcrypt & JWT
│   ├── security-headers.js     # Audit OWASP HTTP Security Headers
│   ├── crypto-hash.js          # Web Crypto API SHA-256 / SHA-512 / MD5
│   ├── password-entropy.js     # Entropi Shannon & Estimasi Cracking GPU
│   ├── payload-encoder.js      # Base64 / Hex / URL / Unicode Sanitizer
│   ├── jwt-debugger.js         # Inspector Claims & Verifier Signature JWT
│   ├── ai-data-analyzer.js     # Analisis Sentimen NLP & Chart.js
│   ├── inventory-sandbox.js    # CRUD Asset SQLite Database Simulation
│   ├── library-sandbox.js      # Relational Library Circulation System
│   ├── json-sql-converter.js   # Batch JSON ke SQL DDL/DML Transformer
│   ├── log-analyzer.js         # Parser Regex Log Nginx & Top IP
│   ├── api-checker.js          # Pinger Latensi REST API
│   ├── image-optimizer.js      # Canvas Image Resizer & WebP Converter
│   ├── currency-converter.js   # Live Multi-Currency Forex Calculator
│   ├── typing-test.js          # Uji Kecepatan Ketik WPM 60 Detik
│   ├── news-scraper.js         # Scraper Berita Teknologi
│   ├── raid-calculator.js      # Kalkulator Kapasitas & Redundansi RAID
│   ├── psu-calculator.js       # Estimasi Wattage PSU PC Deployment
│   ├── regex-tester.js         # Evaluator Regular Expression Interaktif
│   ├── markdown-preview.js     # Live Markdown-to-HTML Renderer
│   └── i18n.js                 # Bilingual Translation Engine (ID / EN)
├── python-modules/             # Source Code Python CLI & Backend
│   ├── analyzer.py             # Script Pandas & VADER Sentiment
│   ├── scraper.py              # Script BeautifulSoup Web Scraping
│   └── requirements.txt        # Dependensi Python
├── LICENSE                     # Lisensi MIT
└── README.md                   # Dokumentasi Teknis Repositori
```

---

## Panduan Instalasi & Eksekusi

### 1. Menjalankan Web Suite Lokal
Aplikasi bersifat client-side modular tanpa build step yang rumit:
```bash
git clone https://github.com/InfiniteNull/dev-tools.git
cd dev-tools

# Jalankan dengan web server lokal sederhana (Python):
python -m http.server 8000
```
Buka di browser: `http://localhost:8000`

### 2. Menjalankan Modul Python Backend
```bash
cd python-modules
pip install -r requirements.txt

# Menjalankan script analisis data & VADER NLP:
python analyzer.py

# Menjalankan script web scraping:
python scraper.py
```

---

## Live Deployment
Aplikasi aktif dan dapat diakses publik pada GitHub Pages:  
👉 **[https://infinitenull.github.io/dev-tools/](https://infinitenull.github.io/dev-tools/)**

---

## Kontak & Lisensi
* **Pengembang:** Rizki Ananda, S.Kom ([@InfiniteNull](https://github.com/InfiniteNull))
* **Almamater:** S1 Informatika — Universitas Potensi Utama
* **Lisensi:** MIT License
