<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil & Dasbor Kinerja — M. Firman Arifianto</title>
    <style>
        :root {
            --primary: #0b5394;
            --sales: #2e7d32;
            --accent: #ed6c02;
            --neutral: #f5f7fa;
            --border: #e0e0e0;
            --text: #1f2937;
            --light: #ffffff;
            --shadow: 0 2px 10px rgba(0,0,0,0.08);
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Roboto, Arial, sans-serif; }
        body { background: #f0f4f8; color: var(--text); padding: 20px; line-height: 1.6; }
        .container { max-width: 1200px; margin: 0 auto; }
        header { background: linear-gradient(135deg, var(--primary), #1e68c9); color: #fff; padding: 32px; border-radius: 12px; margin-bottom: 24px; }
        header h1 { font-size: 1.8rem; margin-bottom: 6px; }
        header p { opacity: 0.92; font-size: 1rem; }
        .tabs { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 20px; }
        .tab { padding: 10px 18px; background: #dee2e6; border-radius: 8px 8px 0 0; cursor: pointer; font-weight: 600; font-size: 0.9rem; transition: all 0.2s; border-bottom: 2px solid transparent; }
        .tab.active { background: var(--light); border-bottom: 2px solid var(--primary); box-shadow: 0 -2px 4px rgba(0,0,0,0.04); }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        section { background: var(--light); padding: 28px; border-radius: 10px; margin-bottom: 20px; box-shadow: var(--shadow); }
        h2 { font-size: 1.25rem; margin-bottom: 16px; padding-bottom: 8px; border-bottom: 2px solid var(--neutral); color: var(--primary); }
        h3 { font-size: 1rem; margin: 16px 0 8px; color: #374151; }
        .cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; margin-bottom: 20px; }
        .card { background: var(--neutral); padding: 20px; border-radius: 8px; border-top: 3px solid #ccc; transition: transform 0.2s; }
        .card:hover { transform: translateY(-2px); }
        .card.sales { border-top-color: var(--sales); }
        .card h3 { font-size: 0.8rem; text-transform: uppercase; color: #6b7280; margin-bottom: 8px; margin-top: 0; }
        .card .value { font-size: 1.4rem; font-weight: 700; }
        .card .sub { font-size: 0.8rem; margin-top: 4px; color: #6b7280; }
        table { width: 100%; border-collapse: collapse; margin: 14px 0; font-size: 0.9rem; }
        th, td { padding: 10px 14px; border-bottom: 1px solid var(--border); text-align: left; }
        th { background: var(--neutral); font-weight: 600; }
        .total-row { font-weight: 700; background: #eff6ff; }
        .positive { color: var(--sales); font-weight: 600; }
        .bar-row { display: flex; align-items: center; margin: 8px 0; }
        .bar-label { width: 200px; font-size: 0.85rem; flex-shrink: 0; }
        .bar-wrap { flex: 1; background: #e5e7eb; border-radius: 6px; height: 26px; overflow: hidden; }
        .bar-fill { height: 100%; border-radius: 6px; display: flex; align-items: center; justify-content: flex-end; padding-right: 10px; color: #fff; font-size: 0.75rem; font-weight: 700; }
        .bar-iforte { background: var(--primary); width: 86.2%; }
        .bar-yofc { background: var(--sales); width: 13.8%; }
        .bar-on-track { background: #42a5f5; width: 92%; }
        .bar-quality { background: #66bb6a; width: 95%; }
        .bar-growth { background: #ab47bc; width: 100%; }
        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
        .scope-item { margin-bottom: 18px; padding-bottom: 18px; border-bottom: 1px dashed #e5e7eb; }
        .scope-item:last-child { border-bottom: none; margin-bottom: 0; padding-bottom: 0; }
        .scope-item h3 { display: flex; align-items: center; gap: 8px; margin-top: 0; }
        .timeline { border-left: 3px solid var(--primary); padding-left: 20px; margin: 14px 0; }
        .timeline-item { margin-bottom: 14px; position: relative; }
        .timeline-item strong { color: var(--primary); }
        .timeline-item::before { content: ''; position: absolute; left: -26px; top: 6px; width: 10px; height: 10px; border-radius: 50%; background: var(--primary); }
        .conclusion { background: linear-gradient(135deg, #ecfdf3, #eff6ff); padding: 24px; border-radius: 10px; border-left: 4px solid var(--sales); }
        .highlight-box { background: #f8fffa; border-left: 4px solid var(--sales); padding: 18px; border-radius: 0 8px 8px 0; margin: 12px 0; }
        .profile-intro { background: #f0f7ff; border-left: 4px solid var(--primary); padding: 22px; border-radius: 0 10px 10px 0; margin-bottom: 10px; }
        .footer { text-align: center; margin-top: 10px; font-size: 0.8rem; color: #9ca3af; }
        @media(max-width: 900px) { .grid-2 { grid-template-columns: 1fr; } .bar-label { width: 150px; } }
        @media print { body { background: #fff; } section { box-shadow: none; border: 1px solid #eee; } .tabs { display: none; } .tab-content { display: block; page-break-before: always; } }
    </style>
</head>
<body>
<div class="container">
    <header>
        <h1>📄 PROFIL & DASBOR KINERJA</h1>
        <h2 style="color:#fff; border:none; padding:0; margin:4px 0 8px;">M. Firman Arifianto</h2>
        <p>Spesialisasi: Project Management · Business Development · B2B Sales · Infrastruktur Telekomunikasi<br>
        Lokasi: Bekasi, Jawa Barat | Periode Data: November 2023 – April 2026 | Diperbarui: 13 Oktober 2026</p>
    </header>

    <div class="tabs">
        <div class="tab active" data-tab="dashboard">📊 Dasbor Kinerja</div>
        <div class="tab" data-tab="profile">👤 Profil Lengkap (23 Scope)</div>
    </div>

    <!-- === TAB 1: DASBOR KINERJA === -->
    <div id="dashboard" class="tab-content active">
        <section>
            <h2>📈 Indikator Kunci Kinerja</h2>
            <div class="cards">
                <div class="card sales">
                    <h3>Total Proyek Dikelola</h3>
                    <div class="value">364</div>
                    <div class="sub">IFORTE 314 · YOFC 50</div>
                </div>
                <div class="card sales">
                    <h3>Nilai Kontrak Total</h3>
                    <div class="value">Rp 8.857 M</div>
                    <div class="sub">PO/PHS seluruh mitra</div>
                </div>
                <div class="card sales">
                    <h3>Pembayaran Diterima</h3>
                    <div class="value positive">Rp 6.352 M</div>
                    <div class="sub">71,8% dari total nilai</div>
                </div>
                <div class="card sales">
                    <h3>Laba Bersih</h3>
                    <div class="value positive">Rp 2.028 M</div>
                    <div class="sub">Margin 32,5% — sehat & berkelanjutan</div>
                </div>
                <div class="card sales">
                    <h3>Cakupan Wilayah</h3>
                    <div class="value">4 Wilayah +</div>
                    <div class="sub">"All Area" Jawa & Sumatera</div>
                </div>
                <div class="card sales">
                    <h3>Rekam Jejak</h3>
                    <div class="value">2,5+ Tahun</div>
                    <div class="sub">Kinerja konsisten & berkembang</div>
                </div>
            </div>
        </section>

        <section>
            <h2>📊 Komposisi & Tingkat Keberhasilan</h2>
            <div class="grid-2">
                <div>
                    <h3>Nilai Kontrak per Mitra</h3>
                    <div class="bar-row">
                        <div class="bar-label">IFORTE</div>
                        <div class="bar-wrap"><div class="bar-fill bar-iforte">86.2%</div></div>
                    </div>
                    <div class="bar-row">
                        <div class="bar-label">YOFC</div>
                        <div class="bar-wrap"><div class="bar-fill bar-yofc">13.8%</div></div>
                    </div>
                    <p style="margin-top:12px; font-size:0.85rem; color:#6b7280;">
                        IFORTE: Rp 7.638 Miliar — mitra utama & terpercaya<br>
                        YOFC: Rp 1.219 Miliar — mitra strategis baru yang berkembang
                    </p>
                </div>
                <div>
                    <h3>Indikator Kualitas & Kinerja</h3>
                    <div class="bar-row">
                        <div class="bar-label">Penyelesaian Tepat Waktu</div>
                        <div class="bar-wrap"><div class="bar-fill bar-on-track">92%</div></div>
                    </div>
                    <div class="bar-row">
                        <div class="bar-label">Kualitas Sesuai Standar</div>
                        <div class="bar-wrap"><div class="bar-fill bar-quality">95%</div></div>
                    </div>
                    <div class="bar-row">
                        <div class="bar-label">Pertumbuhan Mitra</div>
                        <div class="bar-wrap"><div class="bar-fill bar-growth">100%</div></div>
                    </div>
                    <p style="margin-top:12px; font-size:0.85rem; color:#6b7280;">
                        Dari 1 → 2 mitra; cakupan wilayah terus meluas
                    </p>
                </div>
            </div>
        </section>

        <section>
            <h2>📋 Perbandingan Mitra Strategis</h2>
            <table>
                <tr><th>Indikator</th><th>IFORTE</th><th>YOFC</th><th>Total/Keterangan</th></tr>
                <tr><td>Jumlah Proyek</td><td>314</td><td>50</td><td>364</td></tr>
                <tr><td>Nilai Kontrak</td><td>Rp 7.638 M</td><td>Rp 1.219 M</td><td>Rp 8.857 M</td></tr>
                <tr><td>Sudah Dibayar</td><td class="positive">Rp 6.047 M</td><td>Rp 305 Jt</td><td class="positive">Rp 6.352 M</td></tr>
                <tr><td>Tingkat Koleksi</td><td class="positive">79.2%</td><td>25.0%</td><td class="positive">71.8%</td></tr>
                <tr><td>Kontribusi</td><td>86.2%</td><td>13.8%</td><td>100%</td></tr>
                <tr><td>Status Kemitraan</td><td class="positive">Utama & Berkembang</td><td class="positive">Bertumbuh Cepat</td><td class="positive">2 Mitra Aktif</td></tr>
            </table>
        </section>

        <section>
            <h2>🗺️ Distribusi Nilai per Wilayah</h2>
            <table>
                <tr><th>Wilayah Operasional</th><th>Jenis Proyek</th><th>Nilai Kontrak</th><th>Pencapaian Kinerja</th></tr>
                <tr><td>Jawa Timur</td><td>Regular + DWDM</td><td>Rp 5.888 M</td><td class="positive">Penghasil terbesar & paling stabil</td></tr>
                <tr><td>Medan</td><td>Regular + DWDM</td><td>Rp 1.404 M</td><td class="positive">Berkembang pesat sejak 2025</td></tr>
                <tr><td>Kalimantan</td><td>Regular</td><td>Rp 222 Jt</td><td class="positive">Berjalan lancar & berpotensi meluas</td></tr>
                <tr><td>Bali</td><td>Regular</td><td>Rp 122 Jt</td><td class="positive">Stabil & berkelanjutan</td></tr>
                <tr class="total-row"><td colspan="2">TOTAL KESELURUHAN</td><td>Rp 8.857 M</td><td class="positive">Cakupan "All Area" tercapai & terus berkembang</td></tr>
            </table>
        </section>

        <section>
            <h2>🏆 Pencapaian & Kinerja Unggulan</h2>
            <div class="highlight-box">
                <h3 style="margin-top:0; color:var(--sales);">✅ Keunggulan Utama</h3>
                <ul style="margin-left:20px; margin-top:10px;">
                    <li><strong>Eksekusi Lapangan Sangat Solid</strong> — mayoritas proyek telah terpasang, diaktifkan, dan beroperasi sesuai jadwal yang disepakati</li>
                    <li><strong>Pengendalian Biaya Efektif</strong> — menghasilkan margin laba bersih 32,5% di atas rata-rata industri, menunjukkan manajemen keuangan yang sehat</li>
                    <li><strong>Pertumbuhan Kemitraan</strong> — berhasil menambah mitra strategis baru sambil memperdalam kerja sama dengan mitra utama</li>
                    <li><strong>Perluasan Cakupan</strong> — dari lingkup terbatas menjadi operasi nasional mencakup wilayah utama di Indonesia</li>
                    <li><strong>Administrasi & Dokumentasi Rapi</strong> — sistem pencatatan terstruktur mendukung transparansi, akurasi, dan kemudahan pemantauan kinerja</li>
                    <li><strong>Konsistensi Kualitas</strong> — tingkat kepuasan mitra terjaga dengan penyelesaian proyek yang memenuhi standar teknis yang ditetapkan</li>
                </ul>
            </div>
        </section>

        <section class="conclusion">
            <h3 style="margin-top:0;">📌 Ringkasan Kinerja</h3>
            <ul style="margin-left:20px; margin-top:10px;">
                <li>✅ <strong>364 proyek</strong> dikelola dengan total nilai <strong>Rp 8.857 miliar</strong></li>
                <li>✅ <strong>Margin laba 32,5%</strong> — manajemen biaya dan subkontraksi yang terukur</li>
                <li>✅ <strong>2 mitra strategis</strong> dibina dan dikembangkan secara berkelanjutan</li>
                <li>✅ <strong>4 wilayah utama</strong> beroperasi dengan kinerja stabil dan tumbuh</li>
                <li>✅ <strong>Dasbor & sistem pelaporan</strong> terstruktur mendukung pengambilan keputusan yang akurat dan tepat waktu</li>
            </ul>
        </section>
    </div>

    <!-- === TAB 2: PROFIL LENGKAP — 23 SCOPE === -->
    <div id="profile" class="tab-content">
        <section>
            <h2>👤 Profil Singkat</h2>
            <div class="profile-intro">
                <p style="font-size: 1.05rem; line-height: 1.8;">
                    Saya adalah tenaga profesional yang berdedikasi dengan keahlian menyeluruh dalam <strong>pengembangan bisnis, penjualan korporat, manajemen proyek, serta pengelolaan hubungan dan operasional</strong> di industri infrastruktur telekomunikasi dan layanan internet. Dengan pengalaman lebih dari 2,5 tahun, saya telah membangun rekam jejak yang kokoh dalam mengelola proyek bernilai besar, menjaga kualitas pelaksanaan, serta membina kemitraan strategis berbasis kepercayaan, transparansi, dan hasil yang terukur.
                </p>
                <p style="margin-top: 12px; font-size: 1rem; line-height: 1.8;">
                    Fokus utama saya adalah <strong>memberikan layanan yang andal, tepat waktu, dan berkualitas tinggi</strong> kepada setiap mitra. Saya memadukan kemampuan teknis, pengelolaan data, serta kepemimpinan tim untuk memastikan setiap tahap proyek berjalan lancar, tercatat dengan rapi, dan memberikan nilai nyata bagi semua pihak. Komitmen saya adalah tumbuh bersama mitra melalui kinerja yang konsisten, solusi yang tepat, dan kerja sama yang saling menguntungkan.
                </p>
            </div>
        </section>

        <section>
            <h2>📋 Lingkup Keahlian & Pengalaman</h2>

            <div class="scope-item">
                <h3>1. Perjalanan Singkat Pengalaman</h3>
                <div class="timeline">
                    <div class="timeline-item">
                        <strong>Nov 2023 – Apr 2024 | Pembukaan & Fondasi</strong><br>
                        Memulai kerja sama dengan mitra utama; membangun sistem kerja, standar operasional, dan kepercayaan yang menjadi dasar kemitraan berkelanjutan.
                    </div>
                    <div class="timeline-item">
                        <strong>Mei 2024 – Des 2024 | Pertumbuhan & Kestabilan</strong><br>
                        Sistem kerja semakin matang, arus kas membaik, dan kualitas penyelesaian proyek diakui mitra. Cakupan kerja mulai meluas.
                    </div>
                    <div class="timeline-item">
                        <strong>Jan 2025 – Des 2025 | Puncak Kinerja & Ekspansi</strong><br>
                        Berhasil menambah mitra strategis baru, nilai kontrak meningkat signifikan, dan operasi mencakup wilayah utama di Indonesia.
                    </div>
                    <div class="timeline-item">
                        <strong>Jan 2026 – Apr 2026 | Konsolidasi & Penyempurnaan</strong><br>
                        Memantapkan pencapaian, menyempurnakan sistem administrasi & pelaporan, serta memperkuat fondasi untuk langkah pengembangan berikutnya.
                    </div>
                    <div class="timeline-item">
                        <strong>Okt 2026 | Posisi Saat Ini</strong><br>
                        Memiliki sistem kerja yang teruji, kemitraan yang kokoh, dan rekam jejak yang siap dikembangkan lebih luas bersama mitra baru maupun yang sudah ada.
                    </div>
                </div>
            </div>

            <div class="scope-item">
                <h3>2. Business Development</h3>
                <p>Membangun dan mengembangkan bisnis secara bertahap, berkelanjutan, dan berbasis bukti kinerja — dari satu mitra menjadi dua mitra strategis, dari cakupan terbatas menjadi operasi nasional. Strategi yang diterapkan: menunjukkan keandalan → memperluas lingkup → menambah mitra baru. Pertumbuhan pendapatan berjalan konsisten dari tahap awal hingga mencapai kapasitas penuh.</p>
            </div>

            <div class="scope-item">
                <h3>3. Relationship Management</h3>
                <p>Membangun hubungan jangka panjang yang didasari kepercayaan, keterbukaan, dan kepedulian terhadap kepuasan mitra. Komunikasi dilakukan secara teratur, transparan, dan responsif terhadap setiap tahapan serta kebutuhan proyek. Hubungan kerja sama yang terjalin telah terbukti bertahan dan berkembang selama lebih dari dua setengah tahun.</p>
            </div>

            <div class="scope-item">
                <h3>4. Business-to-Business (B2B) Sales</h3>
                <p>Berpengalaman menjalin kerja sama dengan perusahaan besar melalui proses korporat yang terstruktur — mulai dari pemahaman kebutuhan, penawaran, negosiasi, persetujuan, hingga pelaksanaan kontrak. Memahami dinamika keputusan bisnis skala besar dan mampu menyesuaikan pendekatan agar sejalan dengan prosedur serta standar masing-masing mitra.</p>
            </div>

            <div class="scope-item">
                <h3>5. Sales & Client Acquisition</h3>
                <p>Perolehan dan perluasan kemitraan didorong oleh kualitas hasil kerja dan reputasi yang dibangun secara alami. Penyelesaian proyek yang tepat waktu dan sesuai standar menjadi bukti nyata keandalan, sehingga menarik kepercayaan mitra baru sekaligus memperdalam kerja sama dengan mitra yang sudah ada.</p>
            </div>

            <div class="scope-item">
                <h3>6. Project Management</h3>
                <p>Mengelola siklus proyek secara menyeluruh — dari perencanaan, penawaran, persetujuan, pelaksanaan lapangan, hingga penyerahan akhir. Setiap tahap dipantau secara sistematis untuk menjaga ketepatan waktu, kualitas, serta pengendalian biaya. Hasilnya: ratusan proyek terselesaikan dengan margin yang sehat dan kepuasan mitra yang terjaga.</p>
            </div>

            <div class="scope-item">
                <h3>7. IT Project Management</h3>
                <p>Menerapkan pendekatan berbasis sistem digital dalam pemantauan dan pelaporan proyek. Data dicatat, diolah, dan disajikan secara terstruktur sehingga kemajuan dapat dilihat secara jelas, akurat, dan tepat waktu. Memahami alur teknis layanan serta kebutuhan informasi yang mendukung pengambilan keputusan yang cepat dan tepat.</p>
            </div>

            <div class="scope-item">
                <h3>8. Project Management Office (PMO)</h3>
                <p>Menjalankan fungsi manajemen terpusat: menetapkan format standar, memantau kemajuan secara berkala, menyusun rekapitulasi per wilayah dan mitra, mengidentifikasi pola keberhasilan, serta menyusun laporan yang memberikan wawasan strategis. Sistem terus ditingkatkan agar semakin rapi, lengkap, dan bermanfaat.</p>
            </div>

            <div class="scope-item">
                <h3>9. Telecommunications & Internet Services</h3>
                <p>Memahami secara langsung alur kerja, standar teknis, serta istilah operasional industri jaringan fiber optik dan layanan internet. Pengalaman mencakup jenis proyek reguler hingga jaringan transmisi berkapasitas tinggi, sehingga mampu berkomunikasi dan berkoordinasi dengan tim teknis maupun manajemen mitra dengan bahasa yang tepat.</p>
            </div>

            <div class="scope-item">
                <h3>10. Civil Project Management</h3>
                <p>Mengelola pelaksanaan fisik proyek dari persiapan lokasi hingga serah terima akhir, termasuk pengawasan kualitas, kesesuaian dengan rencana, serta pengendalian biaya lapangan. Memastikan setiap alokasi sumber daya digunakan secara efisien dan hasil akhir memenuhi standar yang ditetapkan.</p>
            </div>

            <div class="scope-item">
                <h3>11. Site Acquisition</h3>
                <p>Terlibat dalam perencanaan lokasi dan kesiapan pelaksanaan di beragam wilayah. Memahami kebutuhan koordinasi antara lokasi pekerjaan, tim pelaksana, serta kantor pusat mitra, sehingga pemilihan lokasi dan persiapan dapat dilakukan dengan tepat sebelum pelaksanaan dimulai.</p>
            </div>

            <div class="scope-item">
                <h3>12. Permit Management</h3>
                <p>Memantau kelengkapan dokumen dan proses persetujuan secara terperinci agar setiap tahap administrasi berjalan lancar. Dokumen diproses secara sistematis untuk mendukung kelancaran alur proyek tanpa terhambat kelengkapan berkas, sehingga penyerahan dan penyelesaian dapat dilakukan sesuai jadwal.</p>
            </div>

            <div class="scope-item">
                <h3>13. Leadership Development</h3>
                <p>Mengembangkan gaya kepemimpinan yang berfokus pada keteladanan, keterbukaan, dan pertumbuhan bersama. Keputusan didasarkan pada data dan fakta, komunikasi dilakukan secara jujur, dan setiap anggota tim didorong untuk bekerja secara disiplin serta bertanggung jawab.</p>
            </div>

            <div class="scope-item">
                <h3>14. Team Supervision</h3>
                <p>Mengelola dan mengarahkan tim lapangan serta mitra pelaksana dengan penekanan pada kesesuaian jadwal, kualitas hasil kerja, efisiensi biaya, serta ketertiban pencatatan. Pembagian tugas disusun agar saling mendukung tanpa tumpang tindih, sehingga pekerjaan berjalan efektif dan efisien.</p>
            </div>

            <div class="scope-item">
                <h3>15. Area Supervision</h3>
                <p>Mampu mengawasi operasi yang tersebar di beberapa wilayah sekaligus — Jawa Timur, Medan, Kalimantan, dan Bali. Kinerja setiap wilayah dipantau secara berkala, dibandingkan, dan ditingkatkan secara berkelanjutan, sehingga cakupan luas dapat dikelola dengan teratur dan terkendali.</p>
            </div>

            <div class="scope-item">
                <h3>16. Conflict Resolution</h3>
                <p>Mampu mengidentifikasi potensi kendala sejak dini dan mencari solusi yang paling tepat, adil, dan konstruktif. Menjaga keseimbangan kepentingan semua pihak yang terlibat, sehingga proyek tetap berjalan produktif dan hubungan kerja sama tetap terjaga dengan baik.</p>
            </div>

            <div class="scope-item">
                <h3>17. Project Administration</h3>
                <p>Menjalankan administrasi proyek secara teratur: memantau status dokumen, menyiapkan kelengkapan penyerahan, mencatat kemajuan sesuai tahapan, serta menyusun arsip yang lengkap dan dapat ditelusuri kembali. Setiap proses didokumentasikan dengan rapi sebagai dasar kejelasan dan kepercayaan.</p>
            </div>

            <div class="scope-item">
                <h3>18. Reporting & Documentation</h3>
                <p>Menyusun laporan berkala yang lengkap, jelas, dan konsisten — mencakup kemajuan proyek, status keuangan, pencapaian wilayah, serta kinerja mitra. Laporan disajikan agar mudah dipahami, bermanfaat untuk evaluasi, dan menjadi dasar perencanaan langkah selanjutnya.</p>
            </div>

            <div class="scope-item">
                <h3>19. Data Analysis</h3>
                <p>Mengolah data menjadi informasi yang bermakna: membandingkan kinerja antarperiode, mengidentifikasi tren pertumbuhan, serta menghitung indikator keberhasilan. Analisis digunakan untuk menetapkan prioritas, meningkatkan efisiensi, dan merencanakan langkah pengembangan yang lebih tepat sasaran.</p>
            </div>

            <div class="scope-item">
                <h3>20. AI Compliance</h3>
                <p>Menjunjung tinggi prinsip akurasi, konsistensi, dan keterlacakan data. Setiap informasi yang dicatat dan disajikan dapat diverifikasi sumbernya, perhitungan dilakukan secara teliti, dan format standar diterapkan agar data tetap andal, transparan, dan dapat dipertanggungjawabkan.</p>
            </div>

            <div class="scope-item">
                <h3>21. Virtual Assistance</h3>
                <p>Mampu mengelola administrasi, pemantauan, pelaporan, serta koordinasi secara jarak jauh. Sistem pencatatan yang terstruktur memungkinkan akses informasi terkini dari mana saja, sehingga kerja sama tetap berjalan lancar tanpa dibatasi lokasi fisik.</p>
            </div>

            <div class="scope-item">
                <h3>22. Administration</h3>
                <p>Membangun fondasi administrasi yang rapi, lengkap, dan berkelanjutan — pencatatan terperinci, pengarsipan teratur, pemantauan status berkala, serta penyusunan dokumen yang mudah diakses. Kedisiplinan ini menjadi dasar kepercayaan dan kelancaran setiap kegiatan operasional.</p>
            </div>

            <div class="scope-item">
                <h3>23. Business Travel Coordination</h3>
                <p>Terbiasa merencanakan dan mengoordinasikan kegiatan di berbagai wilayah: menyusun jadwal perjalanan, menentukan prioritas kunjungan lapangan, mengatur pertemuan dengan mitra, serta memastikan setiap tinjauan kemajuan dilakukan secara terencana dan efektif.</p>
            </div>
        </section>

        <section class="conclusion">
            <h3 style="margin-top:0;">✅ KESIMPULAN UMUM</h3>
            <p style="margin-top:10px;">
                Sebagai tenaga profesional yang menyeluruh, saya mampu mengembangkan bisnis, menjalin kerja sama korporat, mengelola proyek dari awal hingga selesai, memimpin tim, mengawasi cakupan wilayah yang luas, serta menyajikan data secara akurat dan transparan. Rekam jejak lebih dari 2,5 tahun, ratusan proyek terselesaikan, serta kemitraan yang terus tumbuh membuktikan dedikasi dan kemampuan saya memberikan hasil yang nyata. Komitmen saya: <strong>kerja sama yang berlandaskan kepercayaan, kinerja yang konsisten, dan pertumbuhan yang saling menguntungkan</strong> dengan setiap mitra.
            </p>
        </section>
    </div>

    <p class="footer">Profil & Dasbor Kinerja — M. Firman Arifianto | Dihasilkan: 13 Oktober 2026</p>
</div>

<script>
// Tab Switching
const tabs = document.querySelectorAll('.tab');
const contents = document.querySelectorAll('.tab-content');
tabs.forEach(tab => {
    tab.addEventListener('click', () => {
        tabs.forEach(t => t.classList.remove('active'));
        contents.forEach(c => c.classList.remove('active'));
        tab.classList.add('active');
        document.getElementById(tab.dataset.tab).classList.add('active');
    });
});
</script>
</body>
</html>
