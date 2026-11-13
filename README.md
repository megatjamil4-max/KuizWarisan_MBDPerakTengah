<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WARISAN MINDA | Majlis Belia Daerah Perak Tengah</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
 --navy:#0f172a;
 --blue:#1e3a8a;
 --yellow:#facc15;
 --gold:#eab308;
 --red:#dc2626;
 --green:#059669;
 --bg:#f8fafc;
 --border:#e2e8f0;
 --muted:#475569;
}

* {
 box-sizing:border-box;
 margin:0;
 padding:0;
}

body {
 font-family:'Plus Jakarta Sans',sans-serif;
 background:var(--bg);
 background-image:radial-gradient(#cbd5e1 .75px,transparent .75px);
 background-size:24px 24px;
 color:var(--navy);
 line-height:1.6;
 min-height:100vh;
 display:flex;
 flex-direction:column;
}

header {
 background:rgba(15,23,42,.97);
 color:white;
 padding:12px 24px;
 display:flex;
 justify-content:space-between;
 align-items:center;
 position:sticky;
 top:0;
 z-index:100;
 border-bottom:3px solid var(--yellow);
}

.logo {
 display:flex;
 align-items:center;
 gap:12px;
}

.logo img {
 width:48px;
 height:48px;
 object-fit:contain;
 background:white;
 border-radius:50%;
 padding:3px;
}

.logo-title {
 font-size:19px;
 font-weight:800;
}

.logo-sub {
 font-size:10px;
 font-weight:700;
 color:var(--yellow);
 letter-spacing:.6px;
}

button {
 cursor:pointer;
 border:0;
 padding:12px 19px;
 border-radius:12px;
 font-family:inherit;
 font-weight:700;
 font-size:14px;
 display:inline-flex;
 align-items:center;
 justify-content:center;
 gap:8px;
 transition:.2s;
}

button:hover:not(:disabled) {
 transform:translateY(-2px);
}

button:disabled {
 opacity:.45;
 cursor:not-allowed;
}

.primary {
 background:linear-gradient(135deg,var(--yellow),var(--gold));
 color:#18181b;
}

.secondary {
 background:var(--navy);
 color:white;
}

.outline {
 background:white;
 color:var(--navy);
 border:1.5px solid var(--border);
}

.danger {
 background:var(--red);
 color:white;
}

.container {
 max-width:900px;
 width:100%;
 margin:28px auto;
 padding:0 18px;
 flex:1;
}

.hero {
 background:linear-gradient(135deg,#0f172a,#1e3a8a 65%,#172554);
 color:white;
 padding:42px 28px;
 border-radius:24px;
 text-align:center;
 border-bottom:5px solid var(--yellow);
 box-shadow:0 20px 40px -15px #0f172a55;
}

.hero-logo {
 width:105px;
 height:105px;
 object-fit:contain;
 background:white;
 border-radius:50%;
 padding:4px;
 margin:0 auto 16px;
 display:block;
}

.badge-perak {
 display:inline-block;
 background:#facc1525;
 border:1px solid #facc1566;
 color:var(--yellow);
 padding:6px 14px;
 border-radius:99px;
 font-size:12px;
 font-weight:800;
 letter-spacing:.7px;
 margin-bottom:12px;
}

.hero h1 {
 font-size:40px;
 font-weight:800;
 margin:6px 0;
}

.hero h3 {
 font-size:16px;
 color:#e2e8f0;
 margin-bottom:14px;
}

.hero p {
 color:#cbd5e1;
 max-width:580px;
 margin:0 auto 24px;
 font-size:14px;
}

.card {
 background:white;
 padding:26px;
 margin-top:22px;
 border-radius:20px;
 box-shadow:0 4px 20px -2px #0f172a10;
 border:1px solid var(--border);
}

.card h2 {
 font-size:21px;
 font-weight:800;
 margin-bottom:16px;
 display:flex;
 gap:10px;
}

.format-grid {
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
 gap:12px;
 margin:18px 0 22px;
}

.format-item {
 background:#f8fafc;
 border:1px solid var(--border);
 padding:15px;
 border-radius:14px;
 text-align:center;
}

.format-item .val {
 font-size:21px;
 font-weight:800;
 color:var(--blue);
 display:block;
}

.format-item .lbl {
 font-size:12px;
 color:var(--muted);
 font-weight:600;
}

.hidden {
 display:none!important;
}

label {
 font-weight:700;
 font-size:14px;
 display:block;
 margin-bottom:6px;
}

input,select {
 width:100%;
 padding:13px 15px;
 margin-bottom:17px;
 border:1.5px solid var(--border);
 border-radius:12px;
 font:inherit;
 font-size:14px;
 background:#f8fafc;
}

input:focus,select:focus {
 outline:none;
 border-color:var(--blue);
 background:white;
 box-shadow:0 0 0 3px #1e3a8a15;
}

.quiz-header {
 display:flex;
 justify-content:space-between;
 align-items:center;
 flex-wrap:wrap;
 gap:10px;
 margin-bottom:14px;
}

.pill-tag {
 background:#eff6ff;
 color:var(--blue);
 border:1px solid #bfdbfe;
 padding:6px 12px;
 border-radius:99px;
 font-size:12px;
 font-weight:800;
}

.timer-pill {
 background:#fef2f2;
 color:var(--red);
 padding:6px 12px;
 border-radius:99px;
 font-size:13px;
 font-weight:800;
}

.progress {
 height:10px;
 background:#e2e8f0;
 border-radius:99px;
 margin-bottom:22px;
 overflow:hidden;
}

.progress-bar {
 height:100%;
 background:linear-gradient(90deg,var(--blue),var(--gold));
 width:0;
 transition:width .3s;
}

.q-counter {
 font-size:12px;
 font-weight:800;
 color:var(--muted);
 margin-bottom:8px;
}

.question {
 font-size:20px;
 font-weight:700;
 line-height:1.5;
 margin-bottom:20px;
}

.options {
 display:grid;
 gap:12px;
}

.option {
 background:white;
 border:1.5px solid var(--border);
 text-align:left;
 width:100%;
 padding:15px;
 border-radius:14px;
 font-size:14px;
 font-weight:500;
 color:var(--navy);
 display:flex;
 align-items:center;
 gap:13px;
 justify-content:flex-start;
}

.opt-letter {
 width:32px;
 height:32px;
 border-radius:8px;
 background:#f1f5f9;
 display:inline-flex;
 align-items:center;
 justify-content:center;
 font-weight:800;
 flex-shrink:0;
}

.option:hover:not(:disabled) {
 border-color:var(--blue);
 background:#f8fafc;
}

.option.selected {
 background:#eff6ff;
 border:2px solid var(--blue);
 font-weight:700;
}

.option.selected .opt-letter {
 background:var(--blue);
 color:var(--yellow);
}

.score-ring {
 width:140px;
 height:140px;
 border-radius:50%;
 background:linear-gradient(135deg,var(--navy),var(--blue));
 color:var(--yellow);
 display:flex;
 flex-direction:column;
 align-items:center;
 justify-content:center;
 margin:16px auto;
 border:5px solid var(--yellow);
}

.score-num {
 font-size:38px;
 font-weight:800;
 line-height:1;
}

.score-max {
 font-size:12px;
 color:white;
 margin-top:5px;
}

.review {
 padding:17px;
 border:1px solid var(--border);
 margin:13px 0;
 border-radius:14px;
}

.correct {
 border-left:6px solid var(--green);
 background:#f0fdf4;
}

.wrong {
 border-left:6px solid var(--red);
 background:#fef2f2;
}

.table-wrap {
 overflow-x:auto;
}

table {
 width:100%;
 border-collapse:collapse;
 margin-top:12px;
 min-width:500px;
}

th,td {
 text-align:left;
 padding:12px;
 border-bottom:1px solid var(--border);
 font-size:13px;
}

th {
 background:#f1f5f9;
 color:var(--navy);
 font-size:12px;
}

.modal-backdrop {
 position:fixed;
 inset:0;
 background:#0f172a99;
 backdrop-filter:blur(4px);
 display:flex;
 align-items:center;
 justify-content:center;
 z-index:999;
 padding:16px;
}

.modal-box {
 background:white;
 max-width:420px;
 width:100%;
 border-radius:20px;
 padding:25px;
 border-top:5px solid var(--yellow);
}

.modal-title {
 font-size:19px;
 font-weight:800;
 margin-bottom:8px;
}

.modal-msg {
 font-size:14px;
 color:var(--muted);
 margin-bottom:18px;
}

.modal-actions {
 display:flex;
 justify-content:flex-end;
 gap:10px;
}

footer {
 text-align:center;
 padding:25px 15px;
 color:var(--muted);
 font-size:12px;
 border-top:1px solid var(--border);
 background:white;
 margin-top:40px;
}

/* =========================================
   SIJIL DIGITAL
========================================= */

.cert-wrapper {
 background:white;
 border:10px double #ca8a04;
 padding:35px 28px;
 text-align:center;
 color:#0f172a;
 border-radius:5px;
 box-shadow:0 10px 30px #0001;
 margin:10px auto;
 max-width:800px;
}

.cert-logo {
 width:100px;
 height:100px;
 object-fit:contain;
 margin:0 auto 8px;
}

.cert-org {
 font-size:14px;
 font-weight:800;
 letter-spacing:1.5px;
 color:var(--blue);
 margin:5px 0;
}

.cert-title {
 font-family:Georgia,serif;
 font-size:32px;
 font-weight:bold;
 margin:8px 0 15px;
}

.cert-name {
 font-family:inherit;
 font-size:13px;
 font-weight:800;
 color:var(--blue);
 margin:14px auto;
 border-bottom:2px solid #ca8a04;
 display:inline-block;
 padding:0 20px 6px;
 text-transform:uppercase;
 max-width:100%;
 overflow-wrap:anywhere;
}

.cert-score {
 display:inline-block;
 background:#fef9c3;
 border:1.5px solid #eab308;
 color:#854d0e;
 padding:8px 20px;
 border-radius:8px;
 font-weight:800;
 font-size:14px;
 margin:13px 0;
}

/* =========================================
   TANDATANGAN - IMEJ DI ATAS GARIS
========================================= */

.cert-signature {
 position:relative;
 margin-top:25px;
 text-align:center;
 padding-top:65px;
}

.signature-image {
 position:absolute;
 top:0;
 left:50%;
 transform:translateX(-50%);
 display:block;
 width:140px;
 height:65px;
 object-fit:contain;
 z-index:2;
}

.signature-line {
 position:absolute;
 top:45px;
 left:50%;
 transform:translateX(-50%);
 width:280px;
 max-width:80%;
 border-top:1px solid #777;
 margin:0;
 z-index:3;
}

.signature-name {
 position:relative;
 font-size:13px;
 font-weight:800;
 text-transform:uppercase;
 margin-top:5px;
}

.signature-position {
 font-size:12px;
 line-height:1.6;
 color:#334155;
 font-weight:600;
}

/* =========================================
   CETAK SIJIL A4 LANDSCAPE
========================================= */

@page {

    size: A4 landscape;

    margin: 8mm;

}

@media print {

    html, body {

        margin: 0 !important;

        padding: 0 !important;

        width: 100% !important;

        min-height: 0 !important;

        background: white !important;

        display: block !important;

        overflow: visible !important;

    }

    /* Sembunyikan semua kandungan asal */

    body * {

        visibility: hidden !important;

    }

    /* Paparkan sijil sahaja */

    #certificateView,

    #certificateView * {

        visibility: visible !important;

    }

    #certificateView {

        display: block !important;

        position: absolute !important;

        top: 0 !important;

        left: 0 !important;

        width: 100% !important;

        margin: 0 !important;

        padding: 0 !important;

        background: white !important;

    }

    #certificateView .no-print {

        display: none !important;

    }

    .cert-wrapper {

        display: flex !important;

        flex-direction: column !important;

        justify-content: center !important;

        align-items: center !important;

        position: relative !important;

        width: 100% !important;

        height: 190mm !important;

        min-height: 0 !important;

        max-width: none !important;

        margin: 0 !important;

        padding: 10mm 15mm !important;

        border: 8px double #ca8a04 !important;

        box-shadow: none !important;

        overflow: hidden !important;

        break-inside: avoid !important;

        page-break-inside: avoid !important;

        -webkit-print-color-adjust: exact !important;

        print-color-adjust: exact !important;

    }

    .cert-logo {

        width: 75px !important;

        height: 75px !important;

    }

    .cert-title {

        font-size: 28px !important;

    }

    .cert-name,

    .signature-name {

        font-size: 13px !important;

    }

    .cert-signature {

        position: relative !important;

        margin-top: 15px !important;

        padding-top: 65px !important;

    }

    .signature-image {

        position: absolute !important;

        top: 0 !important;

        left: 50% !important;

        transform: translateX(-50%) !important;

        width: 140px !important;

        height: 65px !important;

        object-fit: contain !important;

        z-index: 2 !important;

    }

    .signature-line {

        position: absolute !important;

        top: 45px !important;

        left: 50% !important;

        transform: translateX(-50%) !important;

        width: 280px !important;

        max-width: 80% !important;

        z-index: 1 !important;

    }

}

/* PAPARAN TELEFON */

@media(max-width:600px) {

 .hero {
  padding:32px 18px;
 }

 .hero h1 {
  font-size:30px;
 }

 .hero h3 {
  font-size:13px;
 }

 .card {
  padding:19px;
 }

 header {
  padding:10px 14px;
 }

 .logo-title {
  font-size:16px;
 }

 .logo-sub {
  font-size:9px;
 }

 .question {
  font-size:18px;
 }

 .cert-wrapper {
  padding:25px 15px;
 }

 .cert-title {
  font-size:25px;
 }
}
</style>
</head>

<body>

<header>
 <div class="logo">
  <img src="logo-mbd.png" alt="Logo Majlis Belia Daerah Perak Tengah">
  <div>
   <div class="logo-title">WARISAN MINDA</div>
   <div class="logo-sub">MAJLIS BELIA DAERAH PERAK TENGAH</div>
  </div>
 </div>
 <button class="secondary" onclick="bukaAdminModal()">ADMIN</button>
</header>

<div class="container">

<!-- HALAMAN UTAMA -->
<section id="home">
 <div class="hero">
  <img src="logo-mbd.png" class="hero-logo" alt="Logo MBD Perak Tengah">
  <div class="badge-perak">EDISI KHAS 36 SET SOALAN • NEGERI PERAK</div>
  <h1>WARISAN MINDA</h1>
  <h3>SEJARAH NEGERI PERAK, MALAYSIA & SUKAN TRADISIONAL</h3>
  <p>Uji kefahaman anda mengenai khazanah sejarah Negeri Perak, tokoh perjuangan kemerdekaan dan keunikan warisan budaya tanah air.</p>

  <div style="display:flex;gap:12px;justify-content:center;flex-wrap:wrap">
   <button class="primary" onclick="showRegister()">MULA CABARAN KUIZ →</button>
   <button class="secondary" onclick="showLeaderboard()">🏆 PAPAN MARKAH</button>
  </div>
 </div>

 <div class="card">
  <h2>📋 Format & Struktur Pemarkahan</h2>
  <div class="format-grid">
   <div class="format-item"><span class="val">8 Soalan</span><span class="lbl">Rawak daripada 36 soalan</span></div>
   <div class="format-item"><span class="val">3 Mudah</span><span class="lbl">10 markah setiap soalan</span></div>
   <div class="format-item"><span class="val">3 Sederhana</span><span class="lbl">20 markah setiap soalan</span></div>
   <div class="format-item"><span class="val">2 Sukar</span><span class="lbl">30 markah setiap soalan</span></div>
  </div>
  <p style="font-size:13px;color:var(--muted);text-align:center">Markah penuh ialah <strong>150 markah</strong>. Sijil digital dijana selepas kuiz tamat.</p>
 </div>
</section>

<!-- PENDAFTARAN -->
<section id="register" class="hidden">
 <div class="card">
  <h2>📝 Pendaftaran Peserta</h2>

  <label>Nama Penuh Peserta *</label>
  <input id="nama" maxlength="120" placeholder="Masukkan nama penuh untuk sijil">

  <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px">
   <div>
    <label>Umur</label>
    <input id="umur" type="number" min="1" max="120" placeholder="Contoh: 16">
   </div>
   <div>
    <label>Tempat Tinggal</label>
    <input id="daerah" maxlength="100" placeholder="Seri Iskandar / Parit">
   </div>
  </div>

  <label>Mod Cabaran Kuiz</label>
  <select id="mod">
   <option value="santai">Mod Santai (Tiada had masa)</option>
   <option value="pertandingan">Mod Pertandingan (30 saat setiap soalan)</option>
  </select>

  <div style="display:flex;gap:10px">
   <button class="primary" style="flex:2" onclick="mulaKuiz()">MULA MENJAWAB →</button>
   <button class="outline" style="flex:1" onclick="home()">KEMBALI</button>
  </div>
 </div>
</section>

<!-- KUIZ -->
<section id="quiz" class="hidden">
 <div class="card">
  <div class="quiz-header">
   <span class="pill-tag" id="tahap"></span>
   <span class="timer-pill" id="timer"></span>
  </div>

  <div class="progress"><div class="progress-bar" id="progress"></div></div>
  <div class="q-counter" id="nombor"></div>
  <div class="question" id="soalan"></div>
  <div class="options" id="pilihan"></div>

  <div style="margin-top:24px;display:flex;justify-content:flex-end">
   <button class="primary" id="next" onclick="seterusnya()" disabled>SETERUSNYA →</button>
  </div>
 </div>
</section>

<!-- KEPUTUSAN -->
<section id="result" class="hidden">
 <div class="card" style="text-align:center">
  <span class="badge-perak" style="background:#fef9c3;color:#854d0e;border-color:#fde047">KEPUTUSAN RASMI</span>

  <div class="score-ring">
   <span class="score-num" id="markahNum">0</span>
   <span class="score-max">DARIPADA 150</span>
  </div>

  <h2 id="namaKeputusan" style="justify-content:center;margin-bottom:5px"></h2>
  <h3 id="pencapaian" style="color:var(--blue);margin-bottom:14px"></h3>

  <div style="display:flex;justify-content:center;gap:20px;font-size:14px;font-weight:700;margin-bottom:22px;flex-wrap:wrap">
   <span id="betul" style="color:var(--green)"></span>
   <span id="salah" style="color:var(--red)"></span>
  </div>

  <div style="display:flex;gap:10px;justify-content:center;flex-wrap:wrap">
   <button class="primary" onclick="sijil()">🖨️ CETAK SIJIL DIGITAL</button>
   <button class="secondary" onclick="showLeaderboard()">🏆 LEADERBOARD</button>
   <button class="outline" onclick="home()">HALAMAN UTAMA</button>
  </div>
 </div>

 <div class="card">
  <h2>📖 Semakan Jawapan & Fakta Warisan</h2>
  <div id="semakan"></div>
 </div>
</section>

<!-- LEADERBOARD -->
<section id="leaderboard" class="hidden">
 <div class="card">
  <h2>🏆 Papan Markah Tertinggi</h2>
  <div class="table-wrap">
   <table>
    <thead>
     <tr>
      <th>Kedudukan</th>
      <th>Nama Peserta</th>
      <th>Tempat Tinggal</th>
      <th>Markah</th>
     </tr>
    </thead>
    <tbody id="ranking"></tbody>
   </table>
  </div>
  <br>
  <button class="outline" onclick="home()">← KEMBALI KE UTAMA</button>
 </div>
</section>

<!-- ADMIN -->
<section id="admin" class="hidden">
 <div class="card">
  <h2>⚙️ Papan Pemuka Admin</h2>

  <div class="format-grid">
   <div class="format-item"><span class="val" id="jumlahPeserta">0</span><span class="lbl">Jumlah Penyertaan</span></div>
   <div class="format-item"><span class="val" id="purata">0.0</span><span class="lbl">Purata Markah</span></div>
   <div class="format-item"><span class="val" id="tertinggi">0</span><span class="lbl">Markah Tertinggi</span></div>
  </div>

  <div style="display:flex;gap:10px;flex-wrap:wrap">
   <button class="primary" onclick="exportCSV()">📥 MUAT TURUN REKOD CSV</button>
   <button class="danger" onclick="sahkanPadamRekod()">🗑️ PADAM SEMUA REKOD</button>
   <button class="outline" onclick="home()">KELUAR ADMIN</button>
  </div>

  <p style="font-size:12px;color:var(--muted);margin-top:15px">Nota: Rekod disimpan dalam storan pelayar pada peranti ini sahaja.</p>
 </div>
</section>

<!-- SIJIL -->
<section id="certificateView" class="hidden">

 <div class="no-print" style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:10px;margin-bottom:16px">
  <button class="outline" onclick="paparan('result')">← KEMBALI KE KEPUTUSAN</button>
  <button class="primary" onclick="window.print()">🖨️ CETAK / SIMPAN PDF</button>
 </div>

 <div class="cert-wrapper">

  <img src="logo-mbd.png" class="cert-logo" alt="Logo Majlis Belia Daerah Perak Tengah">

  <div class="cert-org">MAJLIS BELIA DAERAH PERAK TENGAH</div>

  <div class="cert-title">SIJIL PENYERTAAN</div>

  <p style="font-size:14px;color:#334155">Dengan sukacitanya diperakui bahawa</p>

  <div class="cert-name" id="certNamaPeserta">NAMA PESERTA</div>

  <p style="font-size:14px;color:#334155">telah berjaya menyertai dan menamatkan Cabaran Kuiz Interaktif</p>

  <h3 style="color:#0f172a;margin:10px 0;font-size:16px">
   WARISAN MINDA: SEJARAH NEGERI PERAK & SUKAN TRADISIONAL
  </h3>

  <div class="cert-score" id="certMarkahPeserta">Pencapaian Markah: 0/150</div>

  <p style="font-size:12px;color:#475569;margin-top:8px" id="certTarikhPeserta">
   Tarikh Dikeluarkan: -
  </p>

  <div class="cert-signature">
   <img src="tandatangan.png" alt="Tandatangan Pengerusi" class="signature-image">
   <div class="signature-line"></div>
   <div class="signature-name">MEGAT MUHAMMAD JAMIL BIN MEGAT AZAHAR</div>
   <div class="signature-position">
    PENGERUSI<br>
    MAJLIS BELIA DAERAH PERAK TENGAH
   </div>
  </div>

 </div>
</section>

<!-- MODAL -->
<div id="customModal" class="modal-backdrop hidden">
 <div class="modal-box">
  <div class="modal-title" id="modalTitle">Makluman</div>
  <div class="modal-msg" id="modalMsg"></div>

  <div id="modalInputWrap" class="hidden">
   <input type="password" id="modalInput" placeholder="Masukkan kata laluan..."
    onkeydown="if(event.key==='Enter')semakKataLaluanAdmin()">
  </div>

  <div class="modal-actions" id="modalActions"></div>
 </div>
</div>

</div>

<footer>
 <strong>WARISAN MINDA © 2026</strong> • Majlis Belia Daerah Perak Tengah<br>
 Memperkasa Jati Diri Belia Melalui Sejarah & Warisan Negeri Perak
</footer>

<script>

/* =========================================
   BANK SOALAN - 36 SOALAN
========================================= */

const DATA_SOALAN = [

["mudah","Sejarah Negeri Perak","Apakah nama sungai terpanjang di Negeri Perak yang menjadi nadi tamadun dan sejarah kesultanan Perak sejak abad ke-16?",["Sungai Perak","Sungai Kinta","Sungai Bernam","Sungai Dinding"],0,"Sungai Perak mengalir dari Hulu Perak hingga ke Beting Beras Basah di Bagan Datuk.",1],

["mudah","Warisan Muzik Perak","Apakah nama alat muzik tradisional bertali yang sinonim dengan kebudayaan masyarakat Melayu di Lambor dan Bota?",["Gambus","Sape","Kompang","Rebab"],0,"Gambus Perak merupakan seni muzik tradisional yang terkenal di Perak Tengah.",1],

["mudah","Sejarah Negeri Perak","Siapakah tokoh pahlawan Melayu Perak yang mengetuai penentangan terhadap Residen British di Pasir Salak pada tahun 1875?",["Dato' Maharaja Lela","Tok Janggut","Mat Kilau","Dato' Bahaman"],0,"Dato' Maharaja Lela bersama Dato' Sagor menentang campur tangan British di Pasir Salak.",1],

["mudah","Kraftangan Warisan Perak","Apakah nama tembikar tradisional berwarna hitam berkilat yang terkenal di Sayong, Kuala Kangsar?",["Labu Sayong","Tembikar Mambong","Pasu Sarawak","Buyung Melaka"],0,"Labu Sayong diperbuat daripada tanah liat dan dibakar menggunakan sekam padi.",1],

["mudah","Sukan Tradisional Perak","Apakah nama permainan tradisional berpangkah menggunakan buah keras yang dimainkan di kampung sekitar Perak?",["Main Porok","Batu Seremban","Konda Kondi","Tuju Tin"],0,"Main Porok menggunakan buah keras dan merupakan permainan tradisional masyarakat kampung.",1],

["mudah","Sukan Tradisional","Dalam permainan congkak, apakah istilah bagi dua lubang besar di kedua-dua hujung papan?",["Rumah Ibu","Kampung","Lubuk","Singgahsana"],0,"Dua lubang besar dipanggil rumah ibu manakala lubang kecil dipanggil kampung.",1],

["mudah","Warisan Malaysia","Apakah nama layang-layang tradisional Malaysia yang terkenal dengan bentuk bulan sabit?",["Wau Bulan","Wau Kucing","Wau Jala Budi","Wau Merak"],0,"Wau Bulan merupakan antara wau tradisional paling ikonik di Malaysia.",0],

["mudah","Warisan Tekstil Malaysia","Apakah nama seni mewarna kain menggunakan lilin panas dan canting atau blok tembaga?",["Batik","Songket","Pua Kumbu","Tenun Pahang"],0,"Batik Malaysia terkenal dengan motif flora dan geometri.",0],

["mudah","Geografi & Warisan Perak","Di manakah lokasi bersejarah tempat pertabalan rasmi Sultan Perak di hilir Sungai Perak?",["Beting Beras Basah","Pulau Pangkor","Teluk Intan","Kuala Kangsar"],0,"Beting Beras Basah di perairan Bagan Datuk merupakan lokasi tradisi pertabalan Sultan Perak.",1],

["mudah","Tokoh & Sejarah Perak","Siapakah pembesar Melayu Perak yang membuka kawasan perlombongan bijih timah di Larut?",["Long Jaafar","Ngah Ibrahim","Sultan Abdullah","Dato' Sagor"],0,"Long Jaafar dan anaknya Ngah Ibrahim merupakan pelopor perlombongan bijih timah di Larut.",1],

["mudah","Permainan Tradisional","Apakah bahan yang lazim digunakan untuk menghasilkan buah batu seremban tradisional?",["Kain diisi pasir atau kacang hijau","Besi padu","Plastik keras","Kayu keras"],0,"Batu seremban lazimnya dijahit daripada kain kecil dan diisi pasir atau biji-bijian.",0],

["mudah","Sejarah Kemerdekaan","Bilakah tarikh rasmi Persekutuan Tanah Melayu mencapai kemerdekaan daripada British?",["31 Ogos 1957","16 September 1963","31 Ogos 1963","1 Januari 1957"],0,"Kemerdekaan Persekutuan Tanah Melayu diisytiharkan pada 31 Ogos 1957.",0],

["sederhana","Sukan Sungai Perak","Apakah acara utama yang melibatkan pendayung ramai menggunakan perahu panjang di Sungai Perak?",["Lumba Perahu Panjang","Lumba Kolek","Regatta Lepa","Lumba Jong"],0,"Perlumbaan perahu panjang merupakan antara tradisi sukan air di Sungai Perak.",1],

["sederhana","Seni Bela Diri Perak","Apakah nama aliran persilatan tradisional yang berkembang di Kuala Kangsar dan Perak?",["Silat Lintau","Silat Cekak Hanafi","Silat Lincah","Silat Kalimah"],0,"Silat Lintau dan Silat Sendeng antara aliran persilatan yang berkembang di Perak.",1],

["sederhana","Seni & Budaya Perak","Apakah nama tarian tradisional Negeri Perak yang menggunakan alat logam bergemerincing dikenali sebagai anak dabus?",["Tarian Dabus","Tarian Piring","Tarian Zapin","Tarian Inang"],0,"Tarian Dabus terkenal di kawasan Pasir Panjang, Sitiawan dan Kampung Gajah.",1],

["sederhana","Sukan Tradisional","Dalam sepak takraw, apakah peranan utama pemain di posisi Tekong?",["Melakukan sepak mula atau servis","Mengumpan bola","Menghadang rejaman","Menentukan pertukaran pemain"],0,"Tekong memulakan permainan dengan melakukan servis.",0],

["sederhana","Warisan Dunia UNESCO","Apakah nama teater tradisional Melayu dari Kelantan yang menggabungkan lakonan, tarian dan muzik rebab?",["Mak Yong","Bangsawan","Mek Mulung","Wayang Kulit"],0,"Mak Yong diiktiraf UNESCO pada tahun 2005.",0],

["sederhana","Warisan Sastera & Seni","Apakah nama seni nyanyian berbalas pantun tradisional masyarakat Melayu dan Baba Nyonya di Melaka?",["Dondang Sayang","Ghazal","Boria","Dikir Barat"],0,"Dondang Sayang disenaraikan UNESCO pada tahun 2018.",0],

["sederhana","Sejarah Pendidikan Perak","Apakah nama institusi perguruan yang ditubuhkan di Tanjung Malim pada tahun 1922?",["Maktab Perguruan Sultan Idris (SITC)","Maktab Perguruan Ilmu Khas","Maktab Tentera Diraja","Universiti Malaya"],0,"SITC kini dikenali sebagai Universiti Pendidikan Sultan Idris (UPSI).",1],

["sederhana","Sukan Gasing Perak","Apakah bahan tradisional yang digunakan sebagai pelincir pada paksi gasing uri?",["Malam atau minyak kelapa","Pasir halus","Gris kenderaan","Air garam"],0,"Malam atau minyak kelapa digunakan untuk mengurangkan geseran pada paksi gasing.",1],

["sederhana","Warisan Seni Silat","Apakah nama senjata pendek tradisional Melayu yang mempunyai mata berlok-lok dan hulu melengkung?",["Keris","Badik","Tumbuk Lada","Golok Panjang"],0,"Keris merupakan lambang kebesaran dan senjata warisan alam Melayu.",0],

["sederhana","Sejarah Malaysia","Perjanjian apakah yang ditandatangani pada 1948 bagi menggantikan Malayan Union?",["Perjanjian Persekutuan Tanah Melayu 1948","Perjanjian Pangkor","Perjanjian Malaysia 1963","Perjanjian Bangkok"],0,"Perjanjian 1948 menubuhkan Persekutuan Tanah Melayu.",0],

["sederhana","Sejarah Perjanjian Perak","Di manakah Perjanjian Pangkor dimeterai pada 20 Januari 1874?",["Atas kapal HMS Pluto di Pulau Pangkor","Bandar Taiping","Kuala Kangsar","Teluk Anson"],0,"Perjanjian Pangkor dimeterai di atas kapal HMS Pluto.",1],

["sederhana","Sukan Tradisional Wau","Apakah bahagian wau yang menghasilkan bunyi berdengung apabila ditiup angin?",["Tali busur atau busur wau","Ekor wau","Tanjak wau","Sayap wau"],0,"Busur wau bergetar apabila ditiup angin lalu menghasilkan bunyi berdengung.",0],

["sukar","Sejarah Perang Perak","Di manakah lokasi kubu pertahanan pejuang Melayu yang dikaitkan dengan penentangan terhadap British pada 1875?",["Pasir Salak","Teluk Intan","Kuala Kangsar","Bota Kiri"],0,"Pasir Salak menjadi lokasi penting penentangan terhadap campur tangan British.",1],

["sukar","Perlembagaan & Undang-undang","Apakah nama manuskrip undang-undang tradisional Kesultanan Perak yang mengandungi 99 fasal?",["Undang-Undang 99 Perak","Hukum Kanun Melaka","Undang-Undang Tubuh Kerajaan Perak","Adat Temenggung"],0,"Undang-Undang 99 Perak mengandungi fasal berkaitan pentadbiran, kekeluargaan dan jenayah.",1],

["sukar","Warisan Kraf Sarawak","Apakah nama kain tenunan kapas berhias motif tradisional masyarakat Iban di Sarawak?",["Pua Kumbu","Kain Tenun Pahang","Songket Limar","Kain Dastar"],0,"Pua Kumbu merupakan kain tenunan ikat tradisional masyarakat Iban.",0],

["sukar","Warisan Tidak Ketara UNESCO","Apakah nama seni tekstil tenunan benang emas dan perak Malaysia yang disenaraikan UNESCO pada 2021?",["Songket","Telepuk","Tekat","Keringkam"],0,"Songket Malaysia disenaraikan UNESCO pada Disember 2021.",0],

["sukar","Sejarah Tentera Perak","Apakah nama tapak pertempuran terkenal di Perak utara semasa kemaraan tentera Jepun pada 1941-1942?",["Pertempuran Kampar (Green Ridge)","Pertempuran Slim River","Pertempuran Kroh","Pertempuran Tanjong Malim"],0,"Pertempuran Kampar di Green Ridge menyaksikan tentangan terhadap kemaraan Jepun.",1],

["sukar","Tokoh Diraja Perak","Siapakah Sultan Perak yang dikenali dengan usaha memajukan pendidikan dan pembaharuan pada awal abad ke-20?",["Sultan Idris Murshidul Azzam Shah","Sultan Iskandar Shah","Sultan Yussuf Izzuddin Shah","Sultan Azlan Shah"],0,"Sultan Idris I memerintah Perak dari 1887 hingga 1916.",1],

["sukar","Sejarah Perlembagaan Malaysia","Apakah nama suruhanjaya bebas yang merangka Perlembagaan Persekutuan Tanah Melayu menjelang kemerdekaan?",["Suruhanjaya Reid","Suruhanjaya Cobbold","Suruhanjaya Laporan Jawatankuasa Pelajaran","Suruhanjaya Semporna"],0,"Suruhanjaya Reid menyediakan draf Perlembagaan Persekutuan Tanah Melayu.",0],

["sukar","Sejarah Pembentukan Malaysia","Apakah nama suruhanjaya yang ditubuhkan pada 1962 untuk meninjau pandangan penduduk Sabah dan Sarawak?",["Suruhanjaya Cobbold","Suruhanjaya Reid","Suruhanjaya Landsborough","Suruhanjaya MacMichael"],0,"Suruhanjaya Cobbold meninjau pandangan penduduk Sabah dan Sarawak tentang pembentukan Malaysia.",0],

["sukar","Seni Kraf Emas Perak","Apakah nama seni sulaman tradisional Perak yang menggunakan benang emas di atas kain baldu?",["Tekat Benang Emas","Seni Sulam Kelantan","Seni Tenun Pahang","Seni Songket Bungkus"],0,"Seni tekat di Kuala Kangsar merupakan kraftangan warisan Perak.",1],

["sukar","Geografi & Sejarah Perak Tengah","Apakah nama kawasan pulau yang mempunyai hubungan dengan sejarah penempatan tradisional di Sungai Perak?",["Pulau Tiga","Pulau Pangkor","Pulau Banding","Pulau Sembilan"],0,"Kawasan Pulau Tiga dan sekitar Lambor mempunyai sejarah penempatan tradisional di Perak Tengah.",1],

["sukar","Warisan Seni Silat Melayu","Dalam falsafah persilatan Melayu, apakah maksud prinsip berguru kepada Allah dan berpaut kepada sunnah?",["Tauhid dan integriti moral sebagai asas akhlak pesilat","Kemahiran menyerang tanpa senjata","Teknik pernafasan","Larangan menyertai pertandingan moden"],0,"Persilatan tradisional turut menekankan kerohanian, disiplin dan akhlak.",0],

["sukar","Rukun Negara Malaysia","Bilakah Rukun Negara diisytiharkan secara rasmi selepas peristiwa 13 Mei 1969?",["31 Ogos 1970","31 Ogos 1957","16 September 1963","1 Januari 1971"],0,"Rukun Negara diisytiharkan pada 31 Ogos 1970.",0]

];

const BANK_SOALAN = DATA_SOALAN.map(x=>({
 tahap:x[0],
 kategori:x[1],
 soalan:x[2],
 pilihan:x[3],
 jawapan:x[4],
 fakta:x[5],
 keutamaanPerak:!!x[6]
}));

/* =========================================
   PEMBOLEH UBAH SISTEM
========================================= */

let peserta={};
let soalanDipilih=[];
let jawapanPeserta=[];
let indeks=0;
let masa=30;
let timer=null;
let pilihanAktif=null;
let mulaMasa=0;
let rekodSemasa=null;

const ADMIN_PASSWORD="warisan123";
const STORAGE_KEY="warisanData";

function escapeHTML(value) {
 return String(value??"").replace(/[&<>"']/g,c=>({
  "&":"&amp;",
  "<":"&lt;",
  ">":"&gt;",
  '"':"&quot;",
  "'":"&#39;"
 }[c]));
}

function bacaRekod() {
 try {
  const data=JSON.parse(localStorage.getItem(STORAGE_KEY)||"[]");
  return Array.isArray(data)?data:[];
 } catch(e) {
  return [];
 }
}

function simpanRekod(data) {
 try {
  localStorage.setItem(STORAGE_KEY,JSON.stringify(data));
  return true;
 } catch(e) {
  paparNotifikasi("Ralat Simpanan","Storan pelayar penuh atau tidak tersedia. Rekod tidak dapat disimpan.");
  return false;
 }
}

/* =========================================
   MODAL
========================================= */

function tutupModal() {
 document.getElementById("customModal").classList.add("hidden");
 document.getElementById("modalInputWrap").classList.add("hidden");
 document.getElementById("modalInput").value="";
}

function paparNotifikasi(tajuk,mesej) {
 document.getElementById("modalTitle").textContent=tajuk;
 document.getElementById("modalMsg").textContent=mesej;
 document.getElementById("modalInputWrap").classList.add("hidden");
 document.getElementById("modalActions").innerHTML=
  '<button class="primary" onclick="tutupModal()">FAHAM</button>';
 document.getElementById("customModal").classList.remove("hidden");
}

function bukaAdminModal() {
 document.getElementById("modalTitle").textContent="🔐 Log Masuk Admin";
 document.getElementById("modalMsg").textContent="Sila masukkan kata laluan pentadbir.";
 document.getElementById("modalInputWrap").classList.remove("hidden");

 document.getElementById("modalActions").innerHTML=
  '<button class="outline" onclick="tutupModal()">BATAL</button><button class="primary" onclick="semakKataLaluanAdmin()">MASUK</button>';

 document.getElementById("customModal").classList.remove("hidden");
 setTimeout(()=>document.getElementById("modalInput").focus(),100);
}

function semakKataLaluanAdmin() {
 const pwd=document.getElementById("modalInput").value;

 if(pwd===ADMIN_PASSWORD) {
  tutupModal();
  paparan("admin");
  dashboard();
 } else {
  document.getElementById("modalMsg").textContent="Kata laluan tidak sah. Sila cuba lagi.";
  document.getElementById("modalInput").value="";
  document.getElementById("modalInput").focus();
 }
}

function sahkanPadamRekod() {
 document.getElementById("modalTitle").textContent="⚠️ Pengesahan Padam Rekod";
 document.getElementById("modalMsg").textContent="Adakah anda pasti mahu memadam semua rekod penyertaan? Tindakan ini tidak boleh diundur.";
 document.getElementById("modalInputWrap").classList.add("hidden");

 document.getElementById("modalActions").innerHTML=
  '<button class="outline" onclick="tutupModal()">BATAL</button><button class="danger" onclick="laksanaPadamRekod()">YA, PADAM SEMUA</button>';

 document.getElementById("customModal").classList.remove("hidden");
}

function laksanaPadamRekod() {
 localStorage.removeItem(STORAGE_KEY);
 tutupModal();
 dashboard();
 paparNotifikasi("Rekod Dipadam","Semua rekod penyertaan pada pelayar ini telah dipadam.");
}

/* =========================================
   NAVIGASI
========================================= */

function paparan(id) {
 const halaman=[
  "home","register","quiz","result",
  "leaderboard","admin","certificateView"
 ];

 halaman.forEach(x=>document.getElementById(x).classList.add("hidden"));
 document.getElementById(id).classList.remove("hidden");
 window.scrollTo({top:0,behavior:"smooth"});
}

function home() {
 clearInterval(timer);
 timer=null;
 paparan("home");
}

function showRegister() {
 paparan("register");
}

function rawak(array) {
 const a=[...array];

 for(let i=a.length-1;i>0;i--) {
  const j=Math.floor(Math.random()*(i+1));
  [a[i],a[j]]=[a[j],a[i]];
 }

 return a;
}

function pilihSoalanKeutamaanPerak(tahap,bilangan) {
 let perak=rawak(BANK_SOALAN.filter(q=>q.tahap===tahap&&q.keutamaanPerak));
 let umum=rawak(BANK_SOALAN.filter(q=>q.tahap===tahap&&!q.keutamaanPerak));
 let hasil=[];

 for(let i=0;i<bilangan;i++) {
  if(perak.length&&(Math.random()<.7||!umum.length)) {
   hasil.push(perak.pop());
  } else if(umum.length) {
   hasil.push(umum.pop());
  } else if(perak.length) {
   hasil.push(perak.pop());
  }
 }

 return rawak(hasil);
}

/* =========================================
   MULA KUIZ
========================================= */

function mulaKuiz() {
 const nama=document.getElementById("nama").value.trim();

 if(!nama) {
  paparNotifikasi("Maklumat Tidak Lengkap","Sila masukkan nama penuh peserta.");
  return;
 }

 peserta={
  nama,
  namaAsal:nama,
  umur:document.getElementById("umur").value||"-",
  daerah:document.getElementById("daerah").value.trim()||"Perak Tengah",
  mod:document.getElementById("mod").value
 };

 soalanDipilih=[
  ...pilihSoalanKeutamaanPerak("mudah",3),
  ...pilihSoalanKeutamaanPerak("sederhana",3),
  ...pilihSoalanKeutamaanPerak("sukar",2)
 ];

 if(soalanDipilih.length!==8) {
  paparNotifikasi("Ralat Bank Soalan","Bank soalan tidak mencukupi untuk memulakan kuiz.");
  return;
 }

 jawapanPeserta=[];
 indeks=0;
 mulaMasa=Date.now();

 paparan("quiz");
 paparSoalan();
}

/* =========================================
   PAPARAN SOALAN
========================================= */

function paparSoalan() {
 clearInterval(timer);
 timer=null;
 pilihanAktif=null;

 const q=soalanDipilih[indeks];

 const tahapLabel={
  mudah:"MUDAH",
  sederhana:"SEDERHANA",
  sukar:"SUKAR"
 };

 document.getElementById("tahap").textContent=
  tahapLabel[q.tahap]+" | "+q.kategori+
  (q.keutamaanPerak?" • PERAK":" • MALAYSIA");

 document.getElementById("nombor").textContent=
  `SOALAN ${indeks+1} DARIPADA ${soalanDipilih.length}`;

 document.getElementById("soalan").textContent=q.soalan;

 document.getElementById("progress").style.width=
  ((indeks+1)/soalanDipilih.length*100)+"%";

 document.getElementById("next").disabled=true;

 document.getElementById("next").textContent=
  indeks===7?"HANTAR JAWAPAN ✓":"SETERUSNYA →";

 q.pilihanRawak=rawak(q.pilihan.map((teks,i)=>({
  teks,
  betul:i===q.jawapan
 })));

 document.getElementById("pilihan").innerHTML=
  q.pilihanRawak.map((p,i)=>`
   <button class="option" onclick="pilihJawapan(${i})">
    <span class="opt-letter">${String.fromCharCode(65+i)}</span>
    <span>${escapeHTML(p.teks)}</span>
   </button>
  `).join("");

 if(peserta.mod==="pertandingan") {
  masa=30;
  kiraMasa();
 } else {
  document.getElementById("timer").textContent="🌿 MOD SANTAI";
 }
}

function pilihJawapan(i) {
 if(pilihanAktif!==null)return;

 pilihanAktif=i;
 clearInterval(timer);
 timer=null;

 const q=soalanDipilih[indeks];
 const betul=q.pilihanRawak[i].betul;

 jawapanPeserta[indeks]={
  pilihan:i,
  betul
 };

 document.querySelectorAll(".option").forEach((b,n)=>{
  if(n===i)b.classList.add("selected");
  b.disabled=true;
 });

 document.getElementById("next").disabled=false;

 if(peserta.mod==="pertandingan") {
  document.getElementById("timer").textContent="✓ JAWAPAN DIREKOD";
 }
}

function kiraMasa() {
 document.getElementById("timer").textContent="⏱️ "+masa+" SAAT";

 timer=setInterval(()=>{
  masa--;
  document.getElementById("timer").textContent="⏱️ "+masa+" SAAT";

  if(masa<=0) {
   clearInterval(timer);
   timer=null;

   jawapanPeserta[indeks]={
    pilihan:null,
    betul:false
   };

   pilihanAktif=-1;
   seterusnya(true);
  }
 },1000);
}

function seterusnya(auto=false) {
 if(pilihanAktif===null&&!auto) {
  paparNotifikasi("Pilih Jawapan","Sila pilih satu jawapan sebelum meneruskan.");
  return;
 }

 clearInterval(timer);
 timer=null;

 if(indeks<soalanDipilih.length-1) {
  indeks++;
  paparSoalan();
 } else {
  keputusan();
 }
}

/* =========================================
   KEPUTUSAN
========================================= */

function keputusan() {
 clearInterval(timer);
 timer=null;

 let markah=0;
 let betul=0;

 const nilai={
  mudah:10,
  sederhana:20,
  sukar:30
 };

 soalanDipilih.forEach((q,i)=>{
  if(jawapanPeserta[i]?.betul) {
   markah+=nilai[q.tahap];
   betul++;
  }
 });

 const salah=soalanDipilih.length-betul;
 const tempoh=Math.round((Date.now()-mulaMasa)/1000);

 const semakan=soalanDipilih.map((q,i)=>{
  const j=jawapanPeserta[i];

  return {
   soalan:q.soalan,
   pilihan:
    j?.pilihan===null||j?.pilihan===undefined
     ?"Tidak dijawab (Tamat masa)"
     :q.pilihanRawak[j.pilihan].teks,
   jawapanBetul:q.pilihan[q.jawapan],
   betul:!!j?.betul,
   fakta:q.fakta
  };
 });

 rekodSemasa={
  nama:peserta.nama,
  umur:peserta.umur,
  daerah:peserta.daerah,
  markah,
  betul,
  salah,
  masa:tempoh,
  tarikh:new Date().toISOString(),
  semakan
 };

 const data=bacaRekod();
 data.push(rekodSemasa);
 simpanRekod(data);

 paparan("result");

 document.getElementById("markahNum").textContent=markah;
 document.getElementById("namaKeputusan").textContent=peserta.nama;
 document.getElementById("betul").textContent="✓ Betul: "+betul+" soalan";
 document.getElementById("salah").textContent="✕ Salah: "+salah+" soalan";

 document.getElementById("pencapaian").textContent=
  markah>=120?"CEMERLANG! PAKAR WARISAN PERAK 🌟":
  markah>=80?"SANGAT BAGUS! 👍":
  markah>=50?"MEMUASKAN 💡":
  "TERUSKAN USAHA BELAJAR! 💪";

 paparSemakan(semakan);
}

function paparSemakan(data) {
 document.getElementById("semakan").innerHTML=
  data.map((q,i)=>`
   <div class="review ${q.betul?"correct":"wrong"}">
    <div style="font-weight:700;margin-bottom:6px">
     ${i+1}. ${escapeHTML(q.soalan)}
    </div>

    <p style="font-size:13px;margin:4px 0">
     Jawapan anda: <strong>${escapeHTML(q.pilihan)}</strong>
    </p>

    <p style="font-size:13px;margin:4px 0;color:var(--green)">
     Jawapan tepat: <strong>${escapeHTML(q.jawapanBetul)}</strong>
    </p>

    <p style="font-size:12px;margin-top:8px;padding-top:8px;border-top:1px dashed #ddd;color:var(--muted)">
     💡 <strong>Info Warisan:</strong> ${escapeHTML(q.fakta)}
    </p>
   </div>
  `).join("");
}

/* =========================================
   LEADERBOARD
========================================= */

function showLeaderboard() {
 paparan("leaderboard");

 const data=bacaRekod().sort(
  (a,b)=>b.markah-a.markah||a.masa-b.masa
 );

 document.getElementById("ranking").innerHTML=
  data.length
   ?data.map((p,i)=>{
    const pingat=
     i===0?"🥇 ":
     i===1?"🥈 ":
     i===2?"🥉 ":"";

    return `
     <tr>
      <td><strong>${pingat}#${i+1}</strong></td>
      <td><strong>${escapeHTML(p.nama)}</strong></td>
      <td>${escapeHTML(p.daerah)}</td>
      <td><span class="pill-tag">${Number(p.markah)||0} / 150</span></td>
     </tr>
    `;
   }).join("")
   :`<tr><td colspan="4" style="text-align:center;padding:24px">Belum ada rekod penyertaan.</td></tr>`;
}

/* =========================================
   SIJIL DIGITAL
========================================= */

function sijil() {
 if(!rekodSemasa) {
  paparNotifikasi("Tiada Rekod","Rekod keputusan peserta tidak ditemui.");
  return;
 }

 document.getElementById("certNamaPeserta").textContent=peserta.nama;

 document.getElementById("certMarkahPeserta").textContent=
  "Pencapaian Markah: "+rekodSemasa.markah+"/150";

 const tarikh=new Date(rekodSemasa.tarikh).toLocaleDateString(
  "ms-MY",
  {
   day:"numeric",
   month:"long",
   year:"numeric"
  }
 );

 document.getElementById("certTarikhPeserta").textContent=
  "Tarikh Dikeluarkan: "+tarikh;

 paparan("certificateView");
}

/* =========================================
   DASHBOARD ADMIN
========================================= */

function dashboard() {
 const data=bacaRekod();
 const jumlah=data.length;

 const purata=jumlah
  ?data.reduce((s,x)=>s+(Number(x.markah)||0),0)/jumlah
  :0;

 const tertinggi=jumlah
  ?Math.max(...data.map(x=>Number(x.markah)||0))
  :0;

 document.getElementById("jumlahPeserta").textContent=jumlah;
 document.getElementById("purata").textContent=purata.toFixed(1)+"/150";
 document.getElementById("tertinggi").textContent=tertinggi+"/150";
}

/* =========================================
   EXPORT CSV
========================================= */

function exportCSV() {
 const data=bacaRekod();

 if(!data.length) {
  paparNotifikasi("Tiada Rekod","Belum ada rekod peserta untuk dimuat turun.");
  return;
 }

 const rows=[
  ["Nama","Umur","Tempat Tinggal","Markah","Betul","Salah","Masa (Saat)","Tarikh"],
  ...data.map(p=>[
   p.nama,
   p.umur,
   p.daerah,
   p.markah,
   p.betul,
   p.salah,
   p.masa,
   p.tarikh
  ])
 ];

 const csv=rows.map(row=>
  row.map(v=>'"'+String(v??"").replace(/"/g,'""')+'"').join(",")
 ).join("\r\n");

 const blob=new Blob(
  ["\ufeff"+csv],
  {type:"text/csv;charset=utf-8;"}
 );

 const url=URL.createObjectURL(blob);
 const link=document.createElement("a");

 link.href=url;
 link.download="warisan-minda-perak-tengah.csv";

 document.body.appendChild(link);
 link.click();
 link.remove();

 setTimeout(()=>URL.revokeObjectURL(url),1000);
}

/* Tutup modal apabila latar belakang ditekan */

document.getElementById("customModal").addEventListener("click",e=>{
 if(e.target.id==="customModal")tutupModal();
});

/* Semakan bank soalan */

console.info("WARISAN MINDA: "+BANK_SOALAN.length+" soalan dimuatkan.");

</script>
</body>
</html>
