
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jadwal Ujian Akhir Semester — SMAN 1 Rikit Gaib</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0a1628;
    --navy-mid: #112240;
    --navy-light: #1d3461;
    --gold: #c9a84c;
    --gold-light: #e8c97a;
    --gold-pale: #f5e8c0;
    --cream: #faf6ee;
    --white: #ffffff;
    --red-accent: #c0392b;
    --green-accent: #1a6b3a;
    --text-muted: #8a9ab5;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--navy);
    font-family: 'DM Sans', sans-serif;
    color: var(--white);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* === BACKGROUND PATTERN === */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      radial-gradient(circle at 20% 20%, rgba(201,168,76,0.07) 0%, transparent 50%),
      radial-gradient(circle at 80% 80%, rgba(29,52,97,0.5) 0%, transparent 50%),
      repeating-linear-gradient(
        45deg,
        transparent,
        transparent 40px,
        rgba(201,168,76,0.015) 40px,
        rgba(201,168,76,0.015) 41px
      );
    pointer-events: none;
    z-index: 0;
  }

  .page-wrap {
    position: relative;
    z-index: 1;
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 24px 80px;
  }

  /* === HEADER === */
  .header {
    text-align: center;
    margin-bottom: 48px;
    animation: fadeDown 0.8s ease both;
  }

  .header-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(201,168,76,0.12);
    border: 1px solid rgba(201,168,76,0.3);
    border-radius: 999px;
    padding: 6px 18px;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold-light);
    margin-bottom: 20px;
  }

  .header-badge::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--gold);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  .header-gov {
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 4px;
  }

  .header-school {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 5vw, 52px);
    font-weight: 900;
    line-height: 1.1;
    background: linear-gradient(135deg, var(--gold-light) 0%, var(--gold) 50%, var(--gold-pale) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 6px;
  }

  .header-sub {
    font-size: 13px;
    color: var(--text-muted);
    letter-spacing: 0.5px;
  }

  .header-divider {
    width: 60px;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    margin: 20px auto;
  }

  .header-title-main {
    font-family: 'Playfair Display', serif;
    font-size: clamp(16px, 3vw, 24px);
    font-weight: 700;
    color: var(--white);
    margin-bottom: 4px;
  }

  .header-title-year {
    font-family: 'DM Mono', monospace;
    font-size: 14px;
    color: var(--gold);
    letter-spacing: 2px;
  }

  /* === LEGEND TABS === */
  .view-tabs {
    display: flex;
    gap: 8px;
    margin-bottom: 32px;
    justify-content: center;
    flex-wrap: wrap;
    animation: fadeUp 0.6s 0.3s ease both;
  }

  .tab-btn {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    color: var(--text-muted);
    padding: 8px 20px;
    border-radius: 8px;
    font-family: 'DM Sans', sans-serif;
    font-size: 13px;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.2s;
    letter-spacing: 0.5px;
  }

  .tab-btn:hover { border-color: var(--gold); color: var(--gold); }
  .tab-btn.active {
    background: var(--gold);
    border-color: var(--gold);
    color: var(--navy);
    font-weight: 600;
  }

  /* === SCHEDULE CARD === */
  .schedule-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(201,168,76,0.2);
    border-radius: 20px;
    overflow: hidden;
    animation: fadeUp 0.7s 0.4s ease both;
    box-shadow: 0 24px 80px rgba(0,0,0,0.4), 0 0 0 1px rgba(201,168,76,0.05) inset;
  }

  .table-wrapper { overflow-x: auto; }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 12.5px;
  }

  /* === TABLE HEAD === */
  thead {
    background: linear-gradient(135deg, var(--navy-light), var(--navy-mid));
    border-bottom: 2px solid rgba(201,168,76,0.4);
  }

  thead tr:first-child th {
    padding: 14px 10px 6px;
    text-align: center;
    font-size: 10px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
    border-right: 1px solid rgba(255,255,255,0.06);
  }

  thead tr:last-child th {
    padding: 6px 10px 12px;
    text-align: center;
    font-size: 11px;
    color: var(--text-muted);
    font-weight: 500;
    border-right: 1px solid rgba(255,255,255,0.06);
  }

  thead tr:first-child th:first-child,
  thead tr:first-child th:nth-child(2),
  thead tr:first-child th:nth-child(3) {
    color: var(--text-muted);
  }

  /* === TABLE BODY === */
  tbody tr {
    border-bottom: 1px solid rgba(255,255,255,0.05);
    transition: background 0.15s;
  }

  tbody tr:hover { background: rgba(201,168,76,0.04); }

  tbody td {
    padding: 9px 10px;
    text-align: center;
    border-right: 1px solid rgba(255,255,255,0.05);
    vertical-align: middle;
    line-height: 1.4;
  }

  /* Day cell */
  .td-day {
    text-align: center;
    padding: 0 8px !important;
    min-width: 70px;
  }

  .day-pill {
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    gap: 2px;
    background: rgba(201,168,76,0.1);
    border: 1px solid rgba(201,168,76,0.25);
    border-radius: 10px;
    padding: 6px 10px;
    width: 100%;
  }

  .day-name {
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 12px;
    color: var(--gold-light);
  }

  .day-date {
    font-family: 'DM Mono', monospace;
    font-size: 9.5px;
    color: var(--text-muted);
  }

  /* Time cell */
  .td-time {
    font-family: 'DM Mono', monospace;
    font-size: 10.5px;
    color: var(--text-muted);
    white-space: nowrap;
    min-width: 110px;
  }

  /* Subject cell */
  .subject-chip {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 6px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.3px;
    white-space: nowrap;
  }

  /* Istirahat row */
  .td-istirahat {
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(255,255,255,0.2);
    background: rgba(255,255,255,0.02);
    padding: 7px !important;
    border-top: 1px dashed rgba(255,255,255,0.07) !important;
    border-bottom: 1px dashed rgba(255,255,255,0.07) !important;
  }

  /* NO column */
  .td-no {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: rgba(255,255,255,0.2);
    min-width: 32px;
  }

  /* Pengawas ruangan cells */
  .td-pengawas {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--text-muted);
    min-width: 28px;
  }

  .td-kode {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    font-weight: 600;
    color: var(--gold);
    min-width: 24px;
  }

  /* === SUBJECT COLORS === */
  .s-pkn    { background: rgba(52,152,219,0.15); color: #5dade2; }
  .s-ekonomi { background: rgba(46,204,113,0.12); color: #58d68d; }
  .s-inggris { background: rgba(155,89,182,0.15); color: #c39bd3; }
  .s-pai    { background: rgba(230,126,34,0.15); color: #f0a050; }
  .s-fiska  { background: rgba(231,76,60,0.13); color: #ec7063; }
  .s-indo   { background: rgba(26,188,156,0.12); color: #48c9b0; }
  .s-geo    { background: rgba(52,152,219,0.12); color: #7fb3d3; }
  .s-bio    { background: rgba(39,174,96,0.14); color: #52be80; }
  .s-kimia  { background: rgba(142,68,173,0.15); color: #a569bd; }
  .s-sos    { background: rgba(211,84,0,0.13); color: #e59866; }
  .s-pjok   { background: rgba(20,143,119,0.13); color: #45b39d; }
  .s-mmu    { background: rgba(52,73,94,0.25); color: #85929e; }
  .s-prakarya { background: rgba(243,156,18,0.13); color: #f4d03f; }
  .s-sej    { background: rgba(192,57,43,0.13); color: #cd6155; }
  .s-tik    { background: rgba(41,128,185,0.15); color: #5dade2; }
  .s-mulok  { background: rgba(26,82,118,0.2); color: #7fb3d3; }
  .s-snb    { background: rgba(109,76,65,0.2); color: #c4a882; }

  /* === KODE PENGAWAS TABLE === */
  .pengawas-section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-top: 24px;
    animation: fadeUp 0.7s 0.6s ease both;
  }

  @media (max-width: 640px) {
    .pengawas-section { grid-template-columns: 1fr; }
  }

  .pengawas-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(201,168,76,0.15);
    border-radius: 16px;
    overflow: hidden;
  }

  .pengawas-card-header {
    background: linear-gradient(135deg, rgba(201,168,76,0.15), rgba(201,168,76,0.05));
    border-bottom: 1px solid rgba(201,168,76,0.2);
    padding: 12px 18px;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
  }

  .pengawas-list {
    padding: 8px 0;
  }

  .pengawas-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 6px 18px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    transition: background 0.15s;
  }

  .pengawas-item:hover { background: rgba(201,168,76,0.04); }
  .pengawas-item:last-child { border-bottom: none; }

  .pengawas-no {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: rgba(255,255,255,0.2);
    min-width: 18px;
  }

  .pengawas-kode {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    font-weight: 700;
    color: var(--gold);
    background: rgba(201,168,76,0.1);
    border: 1px solid rgba(201,168,76,0.2);
    border-radius: 4px;
    padding: 2px 7px;
    min-width: 28px;
    text-align: center;
  }

  .pengawas-name {
    font-size: 12px;
    font-weight: 500;
    color: rgba(255,255,255,0.8);
  }

  /* === FOOTER === */
  .footer-block {
    margin-top: 24px;
    padding: 24px;
    background: rgba(255,255,255,0.02);
    border: 1px solid rgba(201,168,76,0.12);
    border-radius: 16px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    flex-wrap: wrap;
    gap: 16px;
    animation: fadeUp 0.7s 0.8s ease both;
  }

  .footer-note {
    font-size: 11.5px;
    color: var(--text-muted);
    line-height: 1.8;
  }

  .footer-note strong { color: var(--gold-light); }

  .footer-ttd {
    text-align: right;
  }

  .footer-ttd-place {
    font-size: 11px;
    color: var(--text-muted);
    margin-bottom: 32px;
  }

  .footer-ttd-name {
    font-family: 'Playfair Display', serif;
    font-size: 15px;
    font-weight: 700;
    color: var(--gold-light);
    border-top: 1px solid rgba(201,168,76,0.3);
    padding-top: 8px;
  }

  .footer-ttd-nip {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--text-muted);
    margin-top: 2px;
  }

  /* === COPYRIGHT === */
  .copyright-bar {
    margin-top: 32px;
    text-align: center;
    animation: fadeUp 0.7s 1s ease both;
  }

  .copyright-text {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--text-muted);
    background: rgba(201,168,76,0.05);
    border: 1px solid rgba(201,168,76,0.12);
    border-radius: 999px;
    padding: 6px 18px;
    letter-spacing: 0.5px;
  }

  .copyright-text span {
    color: var(--gold);
    font-weight: 600;
  }

  /* === ANIMATIONS === */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.7); }
  }

  /* === SEARCH BAR === */
  .search-bar-wrap {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
    animation: fadeUp 0.6s 0.25s ease both;
  }

  .search-bar {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(201,168,76,0.25);
    border-radius: 10px;
    padding: 10px 18px;
    color: var(--white);
    font-family: 'DM Sans', sans-serif;
    font-size: 13px;
    width: 100%;
    max-width: 360px;
    outline: none;
    transition: border-color 0.2s;
  }

  .search-bar::placeholder { color: var(--text-muted); }
  .search-bar:focus { border-color: var(--gold); }

  /* highlight on search */
  tr.highlight-row { background: rgba(201,168,76,0.1) !important; }
  tr.highlight-row td { opacity: 1 !important; }
  tr.dim-row td { opacity: 0.35; }
  tr.hidden-row { display: none; }

  /* === PRINT === */
  @media print {
    body { background: white; color: black; }
    .tab-btn, .search-bar-wrap, .header-badge { display: none; }
  }
</style>
</head>
<body>
<div class="page-wrap">

  <!-- HEADER -->
  <div class="header">
    <div class="header-badge">Pemerintah Aceh · Dinas Pendidikan Aceh</div>
    <div class="header-gov">SMA Negeri 1 Rikit Gaib</div>
    <div class="header-school">SMA Negeri 1<br>Rikit Gaib</div>
    <div class="header-sub">Jl. H. Ali Umar No. 1 Rikit Gaib Kode Pos 24614</div>
    <div class="header-divider"></div>
    <div class="header-title-main">Jadwal Ujian Dan Daftar Pengawas</div>
    <div class="header-title-main">Ujian Akhir Semester Genap</div>
    <div class="header-title-year">Tahun Pelajaran 2025 / 2026</div>
  </div>

  <!-- SEARCH -->
  <div class="search-bar-wrap">
    <input class="search-bar" type="text" id="searchInput" placeholder="🔍  Cari mata pelajaran, hari, atau kelas...">
  </div>

  <!-- TABS -->
  <div class="view-tabs">
    <button class="tab-btn active" onclick="filterDay('all', this)">Semua Hari</button>
    <button class="tab-btn" onclick="filterDay('SELASA', this)">Selasa</button>
    <button class="tab-btn" onclick="filterDay('RABU', this)">Rabu</button>
    <button class="tab-btn" onclick="filterDay('KAMIS', this)">Kamis</button>
    <button class="tab-btn" onclick="filterDay('JUM\'AT', this)">Jum'at</button>
    <button class="tab-btn" onclick="filterDay('SABTU', this)">Sabtu</button>
    <button class="tab-btn" onclick="filterDay('SENIN', this)">Senin</button>
    <button class="tab-btn" onclick="filterDay('SELASA2', this)">Selasa II</button>
  </div>

  <!-- SCHEDULE TABLE -->
  <div class="schedule-card">
    <div class="table-wrapper">
      <table id="scheduleTable">
        <thead>
          <tr>
            <th rowspan="2">No</th>
            <th rowspan="2">Hari / Tanggal</th>
            <th rowspan="2">Waktu</th>
            <th colspan="5">Kelas</th>
            <th colspan="5">Pengawas Ruangan</th>
            <th rowspan="2">Kode</th>
          </tr>
          <tr>
            <th>X.1</th><th>X.2</th><th>X.3</th><th>XI.1</th><th>XI.2</th>
            <th>1</th><th>2</th><th>3</th><th>4</th><th>5</th>
          </tr>
        </thead>
        <tbody id="tableBody">
        </tbody>
      </table>
    </div>
  </div>

  <!-- PENGAWAS + KODE -->
  <div class="pengawas-section">
    <div class="pengawas-card">
      <div class="pengawas-card-header">Kode Pengawas (A – J)</div>
      <div class="pengawas-list" id="listA"></div>
    </div>
    <div class="pengawas-card">
      <div class="pengawas-card-header">Kode Pengawas (K – T)</div>
      <div class="pengawas-list" id="listB"></div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer-block">
    <div class="footer-note">
      <strong>NB:</strong> # Pengawas harus sudah hadir di sekolah 10 menit sebelum ujian dimulai.<br>
      # Pengawas yang berhalangan harap mencari pengganti masing-masing.
    </div>
    <div class="footer-ttd">
      <div class="footer-ttd-place">Rikit Gaib, 26 Mei 2026<br>Kepala,</div>
      <div class="footer-ttd-name">HAYADDIN, S.Pd, M.Pd</div>
      <div class="footer-ttd-nip">NIP. 19861110 201003 1 001</div>
    </div>
  </div>

  <!-- COPYRIGHT -->
  <div class="copyright-bar">
    <div class="copyright-text">© 2026 <span>Rapa'i</span> — All Rights Reserved</div>
  </div>

</div>

<script>
// ===== DATA =====
const scheduleData = [
  {
    no: 1, day: 'SELASA', date: '02/06/2026', week: 'SELASA',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['PKN','PKN','PKN','PKN','PKN'], pengawas: ['A','B','C','D','E'], kode: '1' },
      { time: '09.15 – 10.30 WIB', subjects: ['EKONOMI','EKONOMI','EKONOMI','MM-L','MM-L'], pengawas: ['F','G','H','I','J'], kode: '2' },
      { time: '10.30 – 11.00', subjects: null, istirahat: true },
      { time: '11.00 – 12.15 WIB', subjects: ['B. INGGRIS','B. INGGRIS','B. INGGRIS','B. INGGRIS','B. INGGRIS'], pengawas: ['K','L','M','N','O'], kode: '3' },
    ]
  },
  {
    no: 2, day: 'RABU', date: '03/06/2026', week: 'RABU',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['PAI','PAI','PAI','PAI','PAI'], pengawas: ['P','Q','R','S','A'], kode: '4' },
      { time: '09.15 – 10.30 WIB', subjects: ['FISKA','FISKA','FISKA','SNB','FISKA'], pengawas: ['B','C','D','E','F'], kode: '5' },
      { time: '10.30 – 11.00', subjects: null, istirahat: true },
      { time: '11.00 – 12.15 WIB', subjects: ['B.INDO','B.INDO','B.INDO','B.INDO','B.INDO'], pengawas: ['G','H','I','J','K'], kode: '6' },
    ]
  },
  {
    no: 3, day: 'KAMIS', date: '04/06/2026', week: 'KAMIS',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['GEOGRAFI','GEOGRAFI','GEOGRAFI','GEOGRAFI-L','GEOGRAFI-L'], pengawas: ['L','M','N','D','E'], kode: '7' },
      { time: '09.15 – 09.45', subjects: null, istirahat: true },
      { time: '09.45 – 11.00 WIB', subjects: ['BIOLOGI','BIOLOGI','BIOLOGI','BIOLOGI-L','BIOLOGI-L'], pengawas: ['Q','R','T','A','B'], kode: '8' },
    ]
  },
  {
    no: 4, day: 'JUM\'AT', date: '05/06/2026', week: "JUM'AT",
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['KIMIA','KIMIA','KIMIA','KIMIA','KIMIA-L'], pengawas: ['C','O','P','T','G'], kode: '9' },
      { time: '09.15 – 09.45', subjects: null, istirahat: true },
      { time: '09.45 – 11.00 WIB', subjects: ['SOSIOLOGI','SOSIOLOGI','SOSIOLOGI','SEJ','SEJ'], pengawas: ['H','I','J','K','L'], kode: '10' },
    ]
  },
  {
    no: 5, day: 'SABTU', date: '06/06/2026', week: 'SABTU',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['PJOK','PJOK','PJOK','PJOK','PJOK'], pengawas: ['M','N','O','P','G'], kode: '11' },
      { time: '09.15 – 09.45', subjects: null, istirahat: true },
      { time: '09.45 – 11.00 WIB', subjects: ['MM-U','MM-U','MM-U','MM-U','MM-U'], pengawas: ['R','S','A','B','C'], kode: '12' },
    ]
  },
  {
    no: 6, day: 'SENIN', date: '08/06/2026', week: 'SENIN',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['PRAKARYA','PRAKARYA','PRAKARYA','PRAKARYA-L','PRAKARYA-L'], pengawas: ['D','E','F','G','H'], kode: '13' },
      { time: '09.15 – 09.45', subjects: null, istirahat: true },
      { time: '09.45 – 11.00 WIB', subjects: ['SEJ','SEJ','SEJ','–','–'], pengawas: ['I','J','K','–','–'], kode: '14' },
    ]
  },
  {
    no: 7, day: 'SELASA', date: '09/06/2026', week: 'SELASA2',
    rows: [
      { time: '08.00 – 09.15 WIB', subjects: ['MULOK','MULOK','MULOK','MULOK','MULOK'], pengawas: ['L','M','N','O','P'], kode: '15' },
      { time: '09.15 – 09.45', subjects: null, istirahat: true },
      { time: '09.45 – 11.00 WIB', subjects: ['TIK','TIK','TIK','–','–'], pengawas: ['T','R','S','–','–'], kode: '16' },
    ]
  }
];

const pengawasData = [
  { no:1, kode:'A', name:'NURKAMILANI, S.Pd' },
  { no:2, kode:'B', name:'MARNIATI, S.Pd' },
  { no:3, kode:'C', name:'MARLIANA, S.Pd' },
  { no:4, kode:'D', name:'INDAH ASTUTI, S.Pd' },
  { no:5, kode:'E', name:'ERNAWATI, S.P' },
  { no:6, kode:'F', name:'SARLINDA, S.Pd' },
  { no:7, kode:'G', name:'FUJI RAHAYU, S.Pd' },
  { no:8, kode:'H', name:'KASMILA, S.Pd' },
  { no:9, kode:'I', name:'HUSIN AKMAL, S.Pd' },
  { no:10, kode:'J', name:'AHMADDIN, S.Pd' },
  { no:11, kode:'K', name:'KHAIRUL, S.PdI' },
  { no:12, kode:'L', name:'SAMSIDAR, S.Pd' },
  { no:13, kode:'M', name:'JULITA, S.Pd' },
  { no:14, kode:'N', name:'RAFIUDIN, S.Pd' },
  { no:15, kode:'O', name:'MARIATI, S.Pd' },
  { no:16, kode:'P', name:'HASMANIDAR, S.Pd' },
  { no:17, kode:'Q', name:'SULAIKA, S.SN' },
  { no:18, kode:'R', name:'AISAH, S.Pd' },
  { no:19, kode:'S', name:'LIDIA ANITA SARI, S.Pd' },
  { no:20, kode:'T', name:'AWALUDDIN, S.Pd' },
];

// Subject CSS class map
const subjectClass = {
  'PKN':'s-pkn','EKONOMI':'s-ekonomi','B. INGGRIS':'s-inggris','B.INGGRIS':'s-inggris',
  'PAI':'s-pai','FISKA':'s-fiska','B.INDO':'s-indo','GEOGRAFI':'s-geo','GEOGRAFI-L':'s-geo',
  'BIOLOGI':'s-bio','BIOLOGI-L':'s-bio','KIMIA':'s-kimia','KIMIA-L':'s-kimia',
  'SOSIOLOGI':'s-sos','SEJ':'s-sej','PJOK':'s-pjok','MM-L':'s-mmu','MM-U':'s-mmu',
  'PRAKARYA':'s-prakarya','PRAKARYA-L':'s-prakarya','TIK':'s-tik','MULOK':'s-mulok','SNB':'s-snb',
};

// Alias pencarian: kata yang diketik pengguna -> teks yang cocok di data
const subjectAlias = [
  { alias: ['kewarganegaraan','ppkn','civics'], target: 'pkn' },
  { alias: ['bahasa inggris','b inggris','english','inggris'], target: 'b. inggris' },
  { alias: ['agama','pendidikan agama','agama islam','islam'], target: 'pai' },
  { alias: ['fisika','physics'], target: 'fiska' },
  { alias: ['bahasa indonesia','b indonesia','indo'], target: 'b.indo' },
  { alias: ['geo','geography'], target: 'geografi' },
  { alias: ['bio','biology'], target: 'biologi' },
  { alias: ['chemistry'], target: 'kimia' },
  { alias: ['sosio','sociology'], target: 'sosiologi' },
  { alias: ['sejarah','history'], target: 'sej' },
  { alias: ['olahraga','penjas','pendidikan jasmani','jasmani'], target: 'pjok' },
  { alias: ['matematika','math','maths','mtk'], target: 'mm' },
  { alias: ['komputer','teknologi informasi','teknologi','informatika'], target: 'tik' },
  { alias: ['muatan lokal'], target: 'mulok' },
  { alias: ['seni','seni budaya'], target: 'snb' },
];

function resolveQuery(input) {
  const lower = input.trim().toLowerCase();
  for (const map of subjectAlias) {
    if (map.alias.some(a => lower.includes(a) || a.includes(lower))) {
      return map.target;
    }
  }
  return lower;
}

function rowMatches(dayData, row, q) {
  if (!q) return true;
  const resolved = resolveQuery(q);
  const rowText = [
    dayData.day, dayData.date,
    row.time,
    ...(row.subjects || []),
    ...(row.pengawas || []),
    row.kode
  ].join(' ').toLowerCase();
  return rowText.includes(q) || rowText.includes(resolved);
}

// ===== RENDER TABLE =====
function renderTable(filter = 'all') {
  const tbody = document.getElementById('tableBody');
  tbody.innerHTML = '';
  const q = currentSearch || '';

  scheduleData.forEach(dayData => {
    if (filter !== 'all' && dayData.week !== filter) return;

    // When searching: tampilkan semua baris di hari ini jika ada satu saja yang cocok
    if (q) {
      const hasMatch = dayData.rows.some(row => {
        if (row.istirahat) return false;
        return rowMatches(dayData, row, q);
      });
      if (!hasMatch) return;
    }

    const rowCount = dayData.rows.length;
    let dayRendered = false;

    dayData.rows.forEach((row, idx) => {
      const tr = document.createElement('tr');
      tr.dataset.week = dayData.week;
      tr.dataset.day = dayData.day;

      if (row.istirahat) {
        tr.innerHTML = `<td colspan="13" class="td-istirahat">— Istirahat —</td>`;
        tbody.appendChild(tr);
        return;
      }

      // Saat search: semua baris di hari ini ditampilkan,
      // baris yang cocok diberi highlight, baris lain diberi style redup
      if (q) {
        if (rowMatches(dayData, row, q)) {
          tr.classList.add('highlight-row');
        } else {
          tr.classList.add('dim-row');
        }
      }

      let html = '';

      // NO + DAY (only on first rendered row per day)
      if (!dayRendered) {
        const visibleCount = dayData.rows.length;

        html += `<td class="td-no" rowspan="${visibleCount}">${dayData.no}</td>`;
        html += `<td class="td-day" rowspan="${visibleCount}">
          <div class="day-pill">
            <span class="day-name">${dayData.day}</span>
            <span class="day-date">${dayData.date}</span>
          </div>
        </td>`;
        dayRendered = true;
      }

      // TIME
      html += `<td class="td-time">${row.time}</td>`;

      // SUBJECTS
      row.subjects.forEach(subj => {
        const cls = subjectClass[subj] || '';
        if (subj === '–') {
          html += `<td><span style="color:rgba(255,255,255,0.15)">—</span></td>`;
        } else {
          html += `<td><span class="subject-chip ${cls}">${subj}</span></td>`;
        }
      });

      // PENGAWAS
      row.pengawas.forEach(p => {
        if (p === '–') {
          html += `<td class="td-pengawas" style="color:rgba(255,255,255,0.15)">—</td>`;
        } else {
          html += `<td class="td-pengawas">${p}</td>`;
        }
      });

      // KODE
      html += `<td class="td-kode">${row.kode}</td>`;

      tr.innerHTML = html;
      tbody.appendChild(tr);
    });
  });
}

// ===== RENDER PENGAWAS =====
function renderPengawas() {
  const listA = document.getElementById('listA');
  const listB = document.getElementById('listB');
  pengawasData.forEach(p => {
    const el = document.createElement('div');
    el.className = 'pengawas-item';
    el.innerHTML = `
      <span class="pengawas-no">${p.no}</span>
      <span class="pengawas-kode">${p.kode}</span>
      <span class="pengawas-name">${p.name}</span>
    `;
    if (p.no <= 10) listA.appendChild(el);
    else listB.appendChild(el);
  });
}

// ===== FILTER =====
function filterDay(week, btn) {
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  currentSearch = '';
  document.getElementById('searchInput').value = '';
  renderTable(week);
}

// ===== SEARCH =====
let currentSearch = '';

document.getElementById('searchInput').addEventListener('input', function() {
  currentSearch = this.value.trim().toLowerCase();
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.querySelectorAll('.tab-btn')[0].classList.add('active');
  renderTable('all');
});

// ===== INIT =====
renderTable();
renderPengawas();
</script>
</body>
</html>
