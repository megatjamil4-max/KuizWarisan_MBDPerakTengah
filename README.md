<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WARISAN MINDA | Majlis Belia Daerah Perak Tengah</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
    --navy: #0f172a;
    --royal-blue: #1e3a8a;
    --perak-yellow: #facc15;
    --perak-gold: #eab308;
    --perak-black: #18181b;
    --red: #dc2626;
    --green: #059669;
    --bg: #f8fafc;
    --surface: #ffffff;
    --border: #e2e8f0;
    --text-main: #0f172a;
    --text-muted: #475569;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
    background-color: var(--bg);
    background-image: radial-gradient(#cbd5e1 0.75px, transparent 0.75px);
    background-size: 24px 24px;
    color: var(--text-main);
    line-height: 1.6;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

/* Header & Navigation */
header {
    background: rgba(15, 23, 42, 0.95);
    backdrop-filter: blur(12px);
    color: white;
    padding: 14px 28px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
    border-bottom: 3px solid var(--perak-yellow);
    box-shadow: 0 4px 20px rgba(0,0,0,0.12);
}

.logo {
    display: flex;
    align-items: center;
    gap: 14px;
}

.logo-svg {
    width: 46px;
    height: 46px;
    background: white;
    border-radius: 50%;
    padding: 2px;
    box-shadow: 0 2px 10px rgba(250, 204, 21, 0.35);
    flex-shrink: 0;
}

.logo-title {
    font-size: 20px;
    font-weight: 800;
    letter-spacing: 0.5px;
    line-height: 1.2;
}

.logo-sub {
    font-size: 11px;
    font-weight: 600;
    color: var(--perak-yellow);
    letter-spacing: 0.8px;
}

/* Buttons */
button {
    cursor: pointer;
    border: none;
    padding: 12px 20px;
    border-radius: 12px;
    font-family: inherit;
    font-weight: 700;
    transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
    font-size: 14px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
}

button:hover:not(:disabled) {
    transform: translateY(-2px);
    box-shadow: 0 6px 16px rgba(0,0,0,0.12);
}

button:active:not(:disabled) {
    transform: translateY(0);
}

button:disabled {
    opacity: 0.45;
    cursor: not-allowed;
}

.primary {
    background: linear-gradient(135deg, var(--perak-yellow), var(--perak-gold));
    color: var(--perak-black);
    box-shadow: 0 4px 14px rgba(234, 179, 8, 0.3);
}

.secondary {
    background: var(--navy);
    color: white;
    border: 1px solid rgba(255,255,255,0.15);
}

.outline {
    background: transparent;
    color: var(--text-main);
    border: 1.5px solid var(--border);
}

.outline:hover {
    background: #f1f5f9;
}

.danger {
    background: var(--red);
    color: white;
}

/* Main Layout */
.container {
    max-width: 900px;
    width: 100%;
    margin: 28px auto;
    padding: 0 18px;
    flex: 1;
}

/* Hero Section */
.hero {
    background: linear-gradient(135deg, #0f172a 0%, #1e3a8a 65%, #172554 100%);
    color: white;
    padding: 48px 32px;
    border-radius: 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 20px 40px -15px rgba(15, 23, 42, 0.35);
    border-bottom: 5px solid var(--perak-yellow);
}

.hero::before {
    content: "";
    position: absolute;
    top: -60px;
    right: -60px;
    width: 240px;
    height: 240px;
    background: radial-gradient(circle, rgba(250, 204, 21, 0.15) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
}

.hero-logo {
    width: 112px;
    height: 112px;
    margin: 0 auto 18px;
    background: white;
    border-radius: 50%;
    padding: 4px;
    box-shadow: 0 8px 25px rgba(0,0,0,0.3);
    display: block;
}

.badge-perak {
    display: inline-block;
    background: rgba(250, 204, 21, 0.15);
    border: 1px solid rgba(250, 204, 21, 0.4);
    color: var(--perak-yellow);
    padding: 6px 14px;
    border-radius: 99px;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 1px;
    margin-bottom: 12px;
}

.hero h1 {
    font-size: 40px;
    font-weight: 800;
    margin: 6px 0;
    letter-spacing: -0.5px;
}

.hero h3 {
    color: #e2e8f0;
    font-weight: 600;
    font-size: 17px;
    letter-spacing: 0.5px;
    margin-bottom: 14px;
}

.hero p {
    color: #cbd5e1;
    max-width: 580px;
    margin: 0 auto 28px;
    font-size: 15px;
}

/* Cards & Grids */
.card {
    background: var(--surface);
    padding: 28px;
    margin-top: 22px;
    border-radius: 20px;
    box-shadow: 0 4px 20px -2px rgba(15, 23, 42, 0.06);
    border: 1px solid var(--border);
}

.card h2 {
    font-size: 22px;
    font-weight: 800;
    color: var(--navy);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.format-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 14px;
    margin: 18px 0 24px;
}

.format-item {
    background: #f8fafc;
    border: 1px solid var(--border);
    padding: 16px;
    border-radius: 14px;
    text-align: center;
}

.format-item .val {
    font-size: 22px;
    font-weight: 800;
    color: var(--royal-blue);
    display: block;
}

.format-item .lbl {
    font-size: 13px;
    color: var(--text-muted);
    font-weight: 600;
}

.hidden {
    display: none !important;
}

/* Form Controls */
label {
    font-weight: 700;
    font-size: 14px;
    color: var(--navy);
    display: block;
    margin-bottom: 6px;
}

input, select {
    width: 100%;
    padding: 13px 16px;
    margin-bottom: 18px;
    border: 1.5px solid var(--border);
    border-radius: 12px;
    font-family: inherit;
    font-size: 15px;
    background: #f8fafc;
    transition: all 0.2s;
}

input:focus, select:focus {
    outline: none;
    background: white;
    border-color: var(--royal-blue);
    box-shadow: 0 0 0 4px rgba(30, 58, 138, 0.1);
}

/* Quiz Interface */
.quiz-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 14px;
}

.pill-tag {
    background: #eff6ff;
    color: var(--royal-blue);
    border: 1px solid #bfdbfe;
    padding: 6px 14px;
    border-radius: 99px;
    font-size: 12px;
    font-weight: 800;
    letter-spacing: 0.5px;
}

.timer-pill {
    background: #fef2f2;
    color: var(--red);
    border: 1px solid #fecaca;
    padding: 6px 14px;
    border-radius: 99px;
    font-size: 13px;
    font-weight: 800;
}

.progress {
    height: 10px;
    background: #e2e8f0;
    border-radius: 99px;
    margin-bottom: 22px;
    overflow: hidden;
}

.progress-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--royal-blue), var(--perak-gold));
    width: 0%;
    border-radius: 99px;
    transition: width 0.35s ease;
}

.q-counter {
    font-size: 13px;
    font-weight: 700;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 8px;
}

.question {
    font-size: 21px;
    font-weight: 700;
    line-height: 1.5;
    color: var(--navy);
    margin-bottom: 20px;
}

.options {
    display: grid;
    gap: 12px;
}

.option {
    background: white;
    border: 1.5px solid var(--border);
    text-align: left;
    width: 100%;
    padding: 16px 18px;
    border-radius: 14px;
    font-size: 15px;
    font-weight: 500;
    color: var(--text-main);
    display: flex;
    align-items: center;
    gap: 14px;
    justify-content: flex-start;
}

.opt-letter {
    width: 32px;
    height: 32px;
    border-radius: 8px;
    background: #f1f5f9;
    color: var(--navy);
    font-weight: 800;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    transition: all 0.2s;
}

.option:hover:not(:disabled) {
    border-color: var(--royal-blue);
    background: #f8fafc;
}

.option:hover:not(:disabled) .opt-letter {
    background: var(--royal-blue);
    color: white;
}

.option.selected {
    background: #eff6ff;
    border: 2px solid var(--royal-blue);
    font-weight: 700;
}

.option.selected .opt-letter {
    background: var(--royal-blue);
    color: var(--perak-yellow);
}

/* Results & Review */
.score-ring {
    width: 140px;
    height: 140px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--navy), var(--royal-blue));
    color: var(--perak-yellow);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 16px auto;
    border: 5px solid var(--perak-yellow);
    box-shadow: 0 10px 25px rgba(15, 23, 42, 0.2);
}

.score-num {
    font-size: 38px;
    font-weight: 800;
    line-height: 1;
}

.score-max {
    font-size: 13px;
    color: white;
    font-weight: 600;
    margin-top: 4px;
}

.review {
    padding: 18px;
    border: 1px solid var(--border);
    margin: 14px 0;
    border-radius: 14px;
}

.correct {
    border-left: 6px solid var(--green);
    background: #f0fdf4;
}

.wrong {
    border-left: 6px solid var(--red);
    background: #fef2f2;
}

/* Table */
table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 12px;
}

th, td {
    text-align: left;
    padding: 14px 12px;
    border-bottom: 1px solid var(--border);
}

th {
    background: #f1f5f9;
    color: var(--navy);
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

tr:hover td {
    background: #f8fafc;
}

/* Custom Modal Dialog (Replaces alert/confirm/prompt) */
.modal-backdrop {
    position: fixed;
    inset: 0;
    background: rgba(15, 23, 42, 0.65);
    backdrop-filter: blur(4px);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 999;
    padding: 16px;
}

.modal-box {
    background: white;
    max-width: 420px;
    width: 100%;
    border-radius: 20px;
    padding: 26px;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    border-top: 5px solid var(--perak-yellow);
    animation: popIn 0.2s ease-out;
}

@keyframes popIn {
    from { opacity: 0; transform: scale(0.95); }
    to { opacity: 1; transform: scale(1); }
}

.modal-title {
    font-size: 19px;
    font-weight: 800;
    color: var(--navy);
    margin-bottom: 8px;
}

.modal-msg {
    font-size: 14px;
    color: var(--text-muted);
    margin-bottom: 18px;
}

.modal-actions {
    display: flex;
    justify-content: flex-end;
    gap: 10px;
}

footer {
    text-align: center;
    padding: 28px 16px;
    color: var(--text-muted);
    font-size: 13px;
    border-top: 1px solid var(--border);
    background: white;
    margin-top: 40px;
}

@media(max-width:600px) {
    .hero h1 { font-size: 30px; }
    .question { font-size: 18px; }
    .card { padding: 20px; }
    header { padding: 12px 16px; }
    .logo-title { font-size: 17px; }
}

/* Gaya Paparan Sijil Dalam Halaman & Cetakan PDF */
.cert-wrapper {
    background: #ffffff;
    border: 12px double #ca8a04;
    padding: 40px 30px;
    text-align: center;
    color: #0f172a;
    border-radius: 8px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.08);
    margin: 10px auto;
    max-width: 800px;
}

.cert-org {
    font-size: 15px;
    font-weight: 800;
    letter-spacing: 2px;
    color: #1e3a8a;
    margin: 8px 0 4px;
}

.cert-title {
    font-family: 'Georgia', serif;
    font-size: 34px;
    font-weight: bold;
    color: #0f172a;
    margin: 6px 0 16px;
    letter-spacing: 1.5px;
}

.cert-name {
    font-family: 'Georgia', serif;
    font-size: 28px;
    font-weight: bold;
    color: #1e3a8a;
    margin: 14px auto;
    border-bottom: 2px solid #ca8a04;
    display: inline-block;
    padding: 0 24px 6px;
    text-transform: uppercase;
}

.cert-score {
    display: inline-block;
    background: #fef9c3;
    border: 1.5px solid #eab308;
    color: #854d0e;
    padding: 8px 22px;
    border-radius: 8px;
    font-weight: 800;
    font-size: 16px;
    margin: 14px 0;
}

@media print {
    body {
        background: white !important;
        margin: 0;
        padding: 0;
    }
    header, footer, #home, #register, #quiz, #result, #leaderboard, #admin, #customModal, .no-print {
        display: none !important;
    }
    .container {
        max-width: 100% !important;
        margin: 0 !important;
        padding: 0 !important;
    }
    #certificateView {
        display: block !important;
    }
    .cert-wrapper {
        border: 12px double #ca8a04 !important;
        box-shadow: none !important;
        margin: 0 auto !important;
        width: 100% !important;
        page-break-inside: avoid;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">
        <svg class="logo-svg" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <defs>
                <path id="topTextPath" d="M 32,100 A 68,68 0 1,1 168,100" />
                <path id="bottomTextPath" d="M 24,100 A 76,76 0 0,0 176,100" />
            </defs>
            <circle cx="100" cy="100" r="95" fill="#ffffff" stroke="#111111" stroke-width="5"/>
            <line x1="8" y1="122" x2="36" y2="112" stroke="#111111" stroke-width="4"/>
            <line x1="192" y1="122" x2="164" y2="112" stroke="#111111" stroke-width="4"/>
            <circle cx="100" cy="100" r="64" fill="#18499e" stroke="#111111" stroke-width="4"/>
            <g fill="#111111">
                <circle cx="100" cy="100" r="46"/>
                <rect x="94" y="45" width="12" height="12" rx="1"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(30 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(60 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(90 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(120 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(150 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(210 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(240 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(270 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(300 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(330 100 100)"/>
            </g>
            <circle cx="100" cy="95" r="32" fill="#18499e"/>
            <path d="M 103,72 A 22,22 0 1,0 103,116 A 18,18 0 1,1 103,72 Z" fill="#f7e81c"/>
            <polygon points="108,78 110,87 118,82 113,90 122,91 114,95 121,101 112,99 114,108 108,101 105,109 104,100 96,105 102,97 94,95 102,91 96,84 104,88" fill="#f7e81c"/>
            <g fill="#f7e81c" stroke="#111111" stroke-width="1">
                <path d="M 66,120 Q 52,88 76,65 Q 64,92 66,120 Z"/>
                <ellipse cx="62" cy="108" rx="4" ry="8" transform="rotate(-35 62 108)"/>
                <ellipse cx="59" cy="96" rx="4" ry="8" transform="rotate(-20 59 96)"/>
                <ellipse cx="62" cy="84" rx="4" ry="8" transform="rotate(5 62 84)"/>
                <ellipse cx="69" cy="73" rx="4" ry="8" transform="rotate(30 69 73)"/>
                <ellipse cx="78" cy="65" rx="4" ry="7" transform="rotate(50 78 65)"/>
                <path d="M 134,120 Q 148,88 124,65 Q 136,92 134,120 Z"/>
                <ellipse cx="138" cy="108" rx="4" ry="8" transform="rotate(35 138 108)"/>
                <ellipse cx="141" cy="96" rx="4" ry="8" transform="rotate(20 141 96)"/>
                <ellipse cx="138" cy="84" rx="4" ry="8" transform="rotate(-5 138 84)"/>
                <ellipse cx="131" cy="73" rx="4" ry="8" transform="rotate(-30 131 73)"/>
                <ellipse cx="122" cy="65" rx="4" ry="7" transform="rotate(-50 122 65)"/>
            </g>
            <path d="M 98,152 L 85,152 L 85,134 L 56,128 L 58,116 L 66,118 L 65,122 L 98,125 Z" fill="#e52421"/>
            <path d="M 102,152 L 115,152 L 115,134 L 144,128 L 142,116 L 134,118 L 135,122 L 102,125 Z" fill="#e52421"/>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="16.5" fill="#111111" letter-spacing="1.2">
                <textPath href="#topTextPath" startOffset="50%" text-anchor="middle">MAJLIS BELIA DAERAH</textPath>
            </text>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="17" fill="#111111" letter-spacing="1.5">
                <textPath href="#bottomTextPath" startOffset="50%" text-anchor="middle">PERAK TENGAH</textPath>
            </text>
        </svg>
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
        <svg class="hero-logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
            <defs>
                <path id="heroTopText" d="M 32,100 A 68,68 0 1,1 168,100" />
                <path id="heroBottomText" d="M 24,100 A 76,76 0 0,0 176,100" />
            </defs>
            <circle cx="100" cy="100" r="95" fill="#ffffff" stroke="#111111" stroke-width="5"/>
            <line x1="8" y1="122" x2="36" y2="112" stroke="#111111" stroke-width="4"/>
            <line x1="192" y1="122" x2="164" y2="112" stroke="#111111" stroke-width="4"/>
            <circle cx="100" cy="100" r="64" fill="#18499e" stroke="#111111" stroke-width="4"/>
            <g fill="#111111">
                <circle cx="100" cy="100" r="46"/>
                <rect x="94" y="45" width="12" height="12" rx="1"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(30 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(60 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(90 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(120 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(150 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(210 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(240 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(270 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(300 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(330 100 100)"/>
            </g>
            <circle cx="100" cy="95" r="32" fill="#18499e"/>
            <path d="M 103,72 A 22,22 0 1,0 103,116 A 18,18 0 1,1 103,72 Z" fill="#f7e81c"/>
            <polygon points="108,78 110,87 118,82 113,90 122,91 114,95 121,101 112,99 114,108 108,101 105,109 104,100 96,105 102,97 94,95 102,91 96,84 104,88" fill="#f7e81c"/>
            <g fill="#f7e81c" stroke="#111111" stroke-width="1">
                <path d="M 66,120 Q 52,88 76,65 Q 64,92 66,120 Z"/>
                <ellipse cx="62" cy="108" rx="4" ry="8" transform="rotate(-35 62 108)"/>
                <ellipse cx="59" cy="96" rx="4" ry="8" transform="rotate(-20 59 96)"/>
                <ellipse cx="62" cy="84" rx="4" ry="8" transform="rotate(5 62 84)"/>
                <ellipse cx="69" cy="73" rx="4" ry="8" transform="rotate(30 69 73)"/>
                <ellipse cx="78" cy="65" rx="4" ry="7" transform="rotate(50 78 65)"/>
                <path d="M 134,120 Q 148,88 124,65 Q 136,92 134,120 Z"/>
                <ellipse cx="138" cy="108" rx="4" ry="8" transform="rotate(35 138 108)"/>
                <ellipse cx="141" cy="96" rx="4" ry="8" transform="rotate(20 141 96)"/>
                <ellipse cx="138" cy="84" rx="4" ry="8" transform="rotate(-5 138 84)"/>
                <ellipse cx="131" cy="73" rx="4" ry="8" transform="rotate(-30 131 73)"/>
                <ellipse cx="122" cy="65" rx="4" ry="7" transform="rotate(-50 122 65)"/>
            </g>
            <path d="M 98,152 L 85,152 L 85,134 L 56,128 L 58,116 L 66,118 L 65,122 L 98,125 Z" fill="#e52421"/>
            <path d="M 102,152 L 115,152 L 115,134 L 144,128 L 142,116 L 134,118 L 135,122 L 102,125 Z" fill="#e52421"/>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="16.5" fill="#111111" letter-spacing="1.2">
                <textPath href="#heroTopText" startOffset="50%" text-anchor="middle">MAJLIS BELIA DAERAH</textPath>
            </text>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="17" fill="#111111" letter-spacing="1.5">
                <textPath href="#heroBottomText" startOffset="50%" text-anchor="middle">PERAK TENGAH</textPath>
            </text>
        </svg>
        <div class="badge-perak">EDISI KHAS 36 SET SOALAN • NEGERI PERAK</div>
        <h1>WARISAN MINDA</h1>
        <h3>SEJARAH NEGERI PERAK, MALAYSIA & SUKAN TRADISIONAL</h3>
        <p>Uji kefahaman anda mengenai khazanah sejarah Negeri Perak, tokoh perjuangan kemerdekaan, dan keunikan warisan budaya tanah air daripada bank 36 set soalan terpilih.</p>
        <div style="display: flex; gap: 12px; justify-content: center; flex-wrap: wrap;">
            <button class="primary" onclick="showRegister()">MULA CABARAN KUIZ →</button>
            <button class="secondary" onclick="showLeaderboard()">🏆 PAPAN MARKAH</button>
        </div>
    </div>

    <div class="card">
        <h2>📋 Format & Struktur Pemarkahan</h2>
        <div class="format-grid">
            <div class="format-item">
                <span class="val">8 Soalan</span>
                <span class="lbl">Rawak (Dari 36 Set Soalan)</span>
            </div>
            <div class="format-item">
                <span class="val">3 Mudah</span>
                <span class="lbl">10 Markah / Soalan</span>
            </div>
            <div class="format-item">
                <span class="val">3 Sederhana</span>
                <span class="lbl">20 Markah / Soalan</span>
            </div>
            <div class="format-item">
                <span class="val">2 Sukar</span>
                <span class="lbl">30 Markah / Soalan</span>
            </div>
        </div>
        <p style="font-size: 14px; color: var(--text-muted); text-align: center;">
            Markah penuh ialah <strong>150 markah</strong>. Sijil penyertaan digital dijana secara automatik selepas tamat kuiz.
        </p>
    </div>
</section>

<!-- PENDAFTARAN -->
<section id="register" class="hidden">
    <div class="card">
        <h2>📝 Pendaftaran Peserta</h2>
        <label>Nama Penuh Peserta <span style="color: var(--red);">*</span></label>
        <input id="nama" placeholder="Masukkan nama penuh anda (untuk cetakan sijil)">

        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 14px;">
            <div>
                <label>Umur</label>
                <input id="umur" type="number" placeholder="Contoh: 16">
            </div>
            <div>
                <label>Tempat Tinggal</label>
                <input id="daerah" placeholder="Contoh: Seri Iskandar / Parit">
            </div>
        </div>

        <label>Mod Cabaran Kuiz</label>
        <select id="mod">
            <option value="santai">Mod Santai (Tiada had masa - sesuai untuk pembelajaran)</option>
            <option value="pertandingan">Mod Pertandingan (30 saat setiap soalan)</option>
        </select>

        <div style="display: flex; gap: 12px; margin-top: 10px;">
            <button class="primary" style="flex: 2;" onclick="mulaKuiz()">MULA MENJAWAB →</button>
            <button class="outline" style="flex: 1;" onclick="home()">KEMBALI</button>
        </div>
    </div>
</section>

<!-- PAPARAN KUIZ -->
<section id="quiz" class="hidden">
    <div class="card">
        <div class="quiz-header">
            <span class="pill-tag" id="tahap"></span>
            <span class="timer-pill" id="timer"></span>
        </div>

        <div class="progress">
            <div class="progress-bar" id="progress"></div>
        </div>

        <div class="q-counter" id="nombor"></div>
        <div class="question" id="soalan"></div>
        <div class="options" id="pilihan"></div>
        
        <div style="margin-top: 24px; display: flex; justify-content: flex-end;">
            <button class="primary" id="next" onclick="seterusnya()" disabled>SETERUSNYA →</button>
        </div>
    </div>
</section>

<!-- KEPUTUSAN -->
<section id="result" class="hidden">
    <div class="card" style="text-align: center;">
        <span class="badge-perak" style="background: #fef9c3; color: #854d0e; border-color: #fde047;">KEPUTUSAN RASMI</span>
        <div class="score-ring">
            <span class="score-num" id="markahNum">0</span>
            <span class="score-max">DARIPADA 150</span>
        </div>
        <h2 id="namaKeputusan" style="justify-content: center; margin-bottom: 6px;"></h2>
        <h3 id="pencapaian" style="color: var(--royal-blue); margin-bottom: 14px;"></h3>
        <div style="display: flex; justify-content: center; gap: 20px; font-size: 14px; font-weight: 700; margin-bottom: 22px;">
            <span id="betul" style="color: var(--green);"></span>
            <span id="salah" style="color: var(--red);"></span>
        </div>
        <div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
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
        <h2>🏆 Papan Markah Tertinggi (Leaderboard)</h2>
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
        <br>
        <button class="outline" onclick="home()">← KEMBALI KE UTAMA</button>
    </div>
</section>

<!-- ADMIN -->
<section id="admin" class="hidden">
    <div class="card">
        <h2>⚙️ Papan Pemuka Admin</h2>
        <div class="format-grid">
            <div class="format-item">
                <span class="val" id="jumlahPeserta">0</span>
                <span class="lbl">Jumlah Penyertaan</span>
            </div>
            <div class="format-item">
                <span class="val" id="purata">0.0</span>
                <span class="lbl">Purata Markah</span>
            </div>
            <div class="format-item">
                <span class="val" id="tertinggi">0</span>
                <span class="lbl">Markah Tertinggi</span>
            </div>
        </div>
        <div style="display: flex; gap: 10px; flex-wrap: wrap; margin-top: 10px;">
            <button class="primary" onclick="exportCSV()">📥 MUAT TURUN REKOD (CSV)</button>
            <button class="danger" onclick="sahkanPadamRekod()">🗑️ PADAM SEMUA REKOD</button>
            <button class="outline" onclick="home()">KELUAR ADMIN</button>
        </div>
    </div>
</section>

<!-- PAPARAN SIJIL DIGITAL (BEBAS POP-UP) -->
<section id="certificateView" class="hidden">
    <div class="no-print" style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; margin-bottom: 16px;">
        <button class="outline" onclick="paparan('result')">← KEMBALI KE KEPUTUSAN</button>
        <div style="display: flex; gap: 10px;">
            <button class="primary" onclick="window.print()">🖨️ CETAK / SIMPAN PDF</button>
        </div>
    </div>

    <div class="cert-wrapper">
        <svg width="105" height="105" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" style="margin-bottom: 6px;">
            <defs>
                <path id="certTopText" d="M 32,100 A 68,68 0 1,1 168,100" />
                <path id="certBottomText" d="M 24,100 A 76,76 0 0,0 176,100" />
            </defs>
            <circle cx="100" cy="100" r="95" fill="#ffffff" stroke="#111111" stroke-width="5"/>
            <line x1="8" y1="122" x2="36" y2="112" stroke="#111111" stroke-width="4"/>
            <line x1="192" y1="122" x2="164" y2="112" stroke="#111111" stroke-width="4"/>
            <circle cx="100" cy="100" r="64" fill="#18499e" stroke="#111111" stroke-width="4"/>
            <g fill="#111111">
                <circle cx="100" cy="100" r="46"/>
                <rect x="94" y="45" width="12" height="12" rx="1"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(30 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(60 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(90 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(120 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(150 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(210 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(240 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(270 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(300 100 100)"/>
                <rect x="94" y="45" width="12" height="12" rx="1" transform="rotate(330 100 100)"/>
            </g>
            <circle cx="100" cy="95" r="32" fill="#18499e"/>
            <path d="M 103,72 A 22,22 0 1,0 103,116 A 18,18 0 1,1 103,72 Z" fill="#f7e81c"/>
            <polygon points="108,78 110,87 118,82 113,90 122,91 114,95 121,101 112,99 114,108 108,101 105,109 104,100 96,105 102,97 94,95 102,91 96,84 104,88" fill="#f7e81c"/>
            <g fill="#f7e81c" stroke="#111111" stroke-width="1">
                <path d="M 66,120 Q 52,88 76,65 Q 64,92 66,120 Z"/>
                <ellipse cx="62" cy="108" rx="4" ry="8" transform="rotate(-35 62 108)"/>
                <ellipse cx="59" cy="96" rx="4" ry="8" transform="rotate(-20 59 96)"/>
                <ellipse cx="62" cy="84" rx="4" ry="8" transform="rotate(5 62 84)"/>
                <ellipse cx="69" cy="73" rx="4" ry="8" transform="rotate(30 69 73)"/>
                <ellipse cx="78" cy="65" rx="4" ry="7" transform="rotate(50 78 65)"/>
                <path d="M 134,120 Q 148,88 124,65 Q 136,92 134,120 Z"/>
                <ellipse cx="138" cy="108" rx="4" ry="8" transform="rotate(35 138 108)"/>
                <ellipse cx="141" cy="96" rx="4" ry="8" transform="rotate(20 141 96)"/>
                <ellipse cx="138" cy="84" rx="4" ry="8" transform="rotate(-5 138 84)"/>
                <ellipse cx="131" cy="73" rx="4" ry="8" transform="rotate(-30 131 73)"/>
                <ellipse cx="122" cy="65" rx="4" ry="7" transform="rotate(-50 122 65)"/>
            </g>
            <path d="M 98,152 L 85,152 L 85,134 L 56,128 L 58,116 L 66,118 L 65,122 L 98,125 Z" fill="#e52421"/>
            <path d="M 102,152 L 115,152 L 115,134 L 144,128 L 142,116 L 134,118 L 135,122 L 102,125 Z" fill="#e52421"/>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="16.5" fill="#111111" letter-spacing="1.2">
                <textPath href="#certTopText" startOffset="50%" text-anchor="middle">MAJLIS BELIA DAERAH</textPath>
            </text>
            <text font-family="Arial, sans-serif" font-weight="900" font-size="17" fill="#111111" letter-spacing="1.5">
                <textPath href="#certBottomText" startOffset="50%" text-anchor="middle">PERAK TENGAH</textPath>
            </text>
        </svg>
        <div class="cert-org">MAJLIS BELIA DAERAH PERAK TENGAH</div>
        <div class="cert-title">SIJIL PENYERTAAN</div>
        <p style="font-size: 15px; color: #334155;">Dengan sukacitanya diperakui bahawa</p>
        <div class="cert-name" id="certNamaPeserta">NAMA PESERTA</div>
        <p style="font-size: 15px; color: #334155;">telah berjaya menyertai dan menamatkan Cabaran Kuiz Interaktif</p>
        <h3 style="color: #0f172a; margin: 10px 0; font-size: 17px;">WARISAN MINDA: SEJARAH NEGERI PERAK & SUKAN TRADISIONAL</h3>
        <div class="cert-score" id="certMarkahPeserta">Pencapaian Markah: 0/150</div>
        <p style="font-size: 13px; color: #475569; margin-top: 8px;" id="certTarikhPeserta">Tarikh Dikeluarkan: -</p>
        <br><br>
        <p style="margin-bottom: 4px;">_________________________________________</p>
        <p style="font-size: 13px; color: #1e293b;"><strong>Pengerusi / Penyelaras Program<br>Majlis Belia Daerah Perak Tengah</strong></p>
    </div>
</section>

<!-- MODAL NOTIFIKASI & ADMIN -->
<div id="customModal" class="modal-backdrop hidden">
    <div class="modal-box">
        <div class="modal-title" id="modalTitle">Makluman</div>
        <div class="modal-msg" id="modalMsg"></div>
        <div id="modalInputWrap" class="hidden">
            <input type="password" id="modalInput" placeholder="Masukkan kata laluan..." onkeydown="if(event.key==='Enter') semakKataLaluanAdmin()">
        </div>
        <div class="modal-actions" id="modalActions"></div>
    </div>
</div>

</div>

<footer>
    <strong>WARISAN MINDA © 2026</strong> • Majlis Belia Daerah Perak Tengah
    <br>
    Memperkasa Jati Diri Belia Melalui Sejarah & Warisan Negeri Perak
</footer>

<script>
// ============================================================
// 1. BANK SOALAN (36 SET SOALAN KOMPREHENSIF PERAK & MALAYSIA)
// ============================================================
const BANK_SOALAN = [
    // --- TAHAP MUDAH (1-12) ---
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Sejarah Negeri Perak",
        soalan: "Apakah nama sungai terpanjang di Negeri Perak yang menjadi nadi tamadun dan sejarah kesultanan Perak sejak abad ke-16?",
        pilihan: ["Sungai Perak", "Sungai Kinta", "Sungai Bernam", "Sungai Dinding"],
        jawapan: 0,
        fakta: "Sungai Perak (sepanjang kira-kira 400 km) mengalir dari Hulu Perak hingga ke Beting Beras Basah di Bagan Datuk, tempat pertabalan Sultan Perak."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Warisan Muzik Perak",
        soalan: "Apakah nama alat muzik tradisional bertali yang sangat sinonim dengan kebudayaan masyarakat Melayu di Daerah Perak Tengah (terutamanya di Lambor dan Bota)?",
        pilihan: ["Gambus", "Sape", "Kompang", "Rebab"],
        jawapan: 0,
        fakta: "Gambus Perak merupakan seni muzik tradisional yang terkenal di daerah Perak Tengah seperti di Kampung Lambor Kiri dan Bota."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Sejarah Negeri Perak",
        soalan: "Siapakah tokoh pahlawan Melayu Perak yang mengetuai penentangan terhadap Residen British pertama di Pasir Salak pada tahun 1875?",
        pilihan: ["Dato' Maharaja Lela", "Tok Janggut", "Mat Kilau", "Dato' Bahaman"],
        jawapan: 0,
        fakta: "Dato' Maharaja Lela bersama Sepuntum dan Dato' Sagor menentang campur tangan British di Pasir Salak, Perak Tengah."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Kraftangan Warisan Perak",
        soalan: "Apakah nama tembikar tradisional berwarna hitam berkilat yang terkenal dihasilkan di Sayong, Kuala Kangsar, Perak?",
        pilihan: ["Labu Sayong", "Tembikar Mambong", "Pasu Sarawak", "Buyung Melaka"],
        jawapan: 0,
        fakta: "Labu Sayong diperbuat daripada tanah liat khas dan dibakar menggunakan sekam padi untuk menghasilkan warna hitam yang menyejukkan air."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Sukan Tradisional Perak",
        soalan: "Apakah nama permainan tradisional berpangkah menggunakan buah keras yang sering dimainkan oleh masyarakat di kampung-kampung sekitar Perak?",
        pilihan: ["Main Porok (Main Buah Keras)", "Batu Seremban", "Konda Kondi", "Tuju Tin"],
        jawapan: 0,
        fakta: "Main Porok menggunakan buah keras yang dipangkah menggunakan kaki (tumit) dan sangat popular di kawasan perkampungan Negeri Perak."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Sukan Tradisional",
        soalan: "Dalam permainan congkak yang digemari di istana dan kampung-kampung di Perak, apakah istilah bagi dua lubang besar di kedua-dua hujung papan?",
        pilihan: ["Rumah Ibu", "Kampung", "Lubuk", "Singgahsana"],
        jawapan: 0,
        fakta: "Dua lubang besar di hujung papan dipanggil 'Rumah Ibu' sebagai tempat simpanan guli/biji, manakala lubang-lubang kecil dipanggil 'Kampung'."
    },
    {
        tahap: "mudah",
        keutamaanPerak: false,
        kategori: "Warisan Malaysia",
        soalan: "Apakah nama layang-layang tradisional Malaysia yang terkenal dengan bentuk bulan sabit di bahagian bawahnya dan sering diterbangkan selepas musim menuai?",
        pilihan: ["Wau Bulan", "Wau Kucing", "Wau Jala Budi", "Wau Merak"],
        jawapan: 0,
        fakta: "Wau Bulan merupakan antara wau tradisional paling ikonik di Malaysia (terutamanya di Kelantan) dan coraknya turut diabadikan pada wang syiling 50 sen serta logo penerbangan negara."
    },
    {
        tahap: "mudah",
        keutamaanPerak: false,
        kategori: "Warisan Tekstil Malaysia",
        soalan: "Apakah nama seni mewarna kain tradisional Malaysia yang menggunakan lilin panas dan canting atau blok tembaga untuk menghasilkan corak flora dan geometri?",
        pilihan: ["Batik", "Songket", "Pua Kumbu", "Tenun Pahang"],
        jawapan: 0,
        fakta: "Batik Malaysia terkenal dengan motif flora (seperti bunga raya dan daun) serta diiktiraf sebagai salah satu warisan seni tekstil utama negara."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Geografi & Warisan Perak",
        soalan: "Di manakah lokasi bersejarah tempat pertabalan rasmi Sultan Perak diadakan di hilir Sungai Perak?",
        pilihan: ["Beting Beras Basah", "Pulau Pangkor", "Teluk Intan", "Kuala Kangsar"],
        jawapan: 0,
        fakta: "Beting Beras Basah di perairan Bagan Datuk/Hilir Perak merupakan lokasi tradisi upacara pertabalan Sultan Perak sejak zaman dahulu."
    },
    {
        tahap: "mudah",
        keutamaanPerak: true,
        kategori: "Tokoh & Sejarah Perak",
        soalan: "Siapakah pembesar Melayu Perak yang membuka kawasan perlombongan bijih timah di Larut dan memajukan bandar Taiping pada abad ke-19?",
        pilihan: ["Long Jaafar", "Ngah Ibrahim", "Sultan Abdullah", "Datok Sagor"],
        jawapan: 0,
        fakta: "Long Jaafar dan anaknya Ngah Ibrahim merupakan pelopor penting pembukaan lombong bijih timah di Larut."
    },
    {
        tahap: "mudah",
        keutamaanPerak: false,
        kategori: "Permainan Tradisional",
        soalan: "Apakah bahan utama yang lazim digunakan untuk menghasilkan buah batu seremban tradisional selain biji getah?",
        pilihan: ["Kain yang diisi pasir atau kacang hijau", "Besi padu", "Plastik keras", "Kayu keras"],
        jawapan: 0,
        fakta: "Batu seremban tradisional biasanya dijahit menggunakan kain kecil dan diisi dengan pasir, beras, atau biji saga/kacang hijau."
    },
    {
        tahap: "mudah",
        keutamaanPerak: false,
        kategori: "Sejarah Kemerdekaan",
        soalan: "Bilakah tarikh rasmi Persekutuan Tanah Melayu mencapai kemerdekaan daripada British?",
        pilihan: ["31 Ogos 1957", "16 September 1963", "31 Ogos 1963", "1 Januari 1957"],
        jawapan: 0,
        fakta: "Kemerdekaan Persekutuan Tanah Melayu diisytiharkan oleh Tunku Abdul Rahman pada 31 Ogos 1957 di Stadium Merdeka."
    },

    // --- TAHAP SEDERHANA (13-24) ---
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Sukan Sungai Perak",
        soalan: "Setiap tahun sempena Hari Keputeraan Sultan Perak di Kuala Kangsar, pelbagai acara sukan air tradisional diadakan di Sungai Perak. Apakah acara utama yang melibatkan pendayung ramai menggunakan perahu panjang?",
        pilihan: ["Lumba Perahu Naga / Perahu Panjang", "Lumba Kolek", "Regatta Lepa", "Lumba Jong"],
        jawapan: 0,
        fakta: "Temasya Sukan Air Kuala Kangsar di Sungai Perak terkenal dengan perlumbaan perahu panjang yang menjadi tradisi sejak zaman berzaman."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Seni Bela Diri Perak",
        soalan: "Apakah nama seni silat warisan asal Negeri Perak yang diasaskan oleh Syed Zainal Abidin Al-Attas dan terkenal di Kuala Kangsar serta Perak Tengah?",
        pilihan: ["Silat Gayongman / Silat Lintau", "Silat Cekak Hanafi", "Silat Lincah", "Silat Kalimah"],
        jawapan: 0,
        fakta: "Silat Lintau dan Silat Sendeng merupakan antara aliran persilatan tradisional yang berkembang pesat di Perak Tengah dan Kuala Kangsar."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Seni & Budaya Perak",
        soalan: "Apakah nama tarian tradisional Negeri Perak yang ditarikan sambil memegang alat logam bergemerincing (anak dabus) dengan iringan nyanyian berzanji?",
        pilihan: ["Tarian Dabus", "Tarian Piring", "Tarian Zapin", "Tarian Inang"],
        jawapan: 0,
        fakta: "Tarian Dabus merupakan tarian tradisional terkenal di Negeri Perak (khususnya di Pasir Panjang, Sitiawan dan Kampung Gajah) yang menggunakan alat logam bergemerincing dikenali sebagai anak dabus."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Sukan Tradisional",
        soalan: "Dalam sukan sepak takraw (sepak raga jaring), apakah peranan utama pemain yang berada di posisi 'Tekong'?",
        pilihan: ["Melakukan sepak mula (servis) dari bulatan tengah gelanggang", "Mengumpan bola kepada perejam di jaring", "Menghadang rejaman pihak lawan di hadapan jaring", "Menjadi ketua pasukan yang menentukan pertukaran pemain"],
        jawapan: 0,
        fakta: "Tekong memulakan permainan dengan melakukan servis setelah bola dilambung oleh salah seorang apit."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Warisan Dunia UNESCO",
        soalan: "Apakah nama teater tradisional Melayu dari negeri Kelantan yang menggabungkan lakonan, tarian, muzik rebab serta nyanyian, dan telah diiktiraf oleh UNESCO pada tahun 2005?",
        pilihan: ["Mak Yong", "Bangsawan", "Mek Mulung", "Wayang Kulit"],
        jawapan: 0,
        fakta: "Mak Yong diiktiraf oleh UNESCO sebagai 'Masterpiece of the Oral and Intangible Heritage of Humanity' pada tahun 2005."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Warisan Sastera & Seni",
        soalan: "Apakah nama seni nyanyian berbalas pantun tradisional masyarakat Melayu dan Baba Nyonya di Melaka yang diiringi alat muzik biola, rebana, dan gong?",
        pilihan: ["Dondang Sayang", "Ghazal", "Boria", "Dikir Barat"],
        jawapan: 0,
        fakta: "Dondang Sayang telah disenaraikan dalam Senarai Wakil Warisan Budaya Tidak Ketara Kemanusiaan UNESCO pada tahun 2018."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Sejarah Pendidikan Perak",
        soalan: "Apakah nama institusi perguruan pertama di Tanah Melayu yang ditubuhkan di Tanjung Malim, Perak pada tahun 1922 untuk melahirkan guru-guru Melayu?",
        pilihan: ["Maktab Perguruan Sultan Idris (SITC)", "Maktab Perguruan Ilmu Khas", "Maktab Tentera Diraja", "Universiti Malaya"],
        jawapan: 0,
        fakta: "SITC (kini Universiti Pendidikan Sultan Idris - UPSI) di Tanjung Malim menjadi pusat nadi nasionalisme awal dan keilmuan Melayu."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Sukan Gasing Perak",
        soalan: "Dalam pertandingan gasing uri tradisional di Perak, apakah bahan yang diletakkan pada paksi gasing semasa berputar bagi mengurangkan geseran dan mengekalkan putaran?",
        pilihan: ["Tahi kelulut / Malam atau minyak kelapa", "Pasir halus", "Gris kenderaan berat", "Air garam"],
        jawapan: 0,
        fakta: "Malam (tahi kelulut) atau minyak kelapa sering digunakan sebagai pelincir tradisional pada patok gasing uri."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Warisan Seni Silat",
        soalan: "Apakah nama senjata pendek tradisional Melayu yang mempunyai mata berlok-lok (berkelok) serta hulu melengkung dan dianggarkan telah wujud sejak zaman Kesultanan Melayu Melaka?",
        pilihan: ["Keris", "Badik", "Tumbuk Lada", "Golok Panjang"],
        jawapan: 0,
        fakta: "Keris merupakan lambang kebesaran dan senjata warisan agung alam Melayu yang diiktiraf UNESCO."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Sejarah Malaysia",
        soalan: "Perjanjian apakah yang ditandatangani pada 1948 bagi menggantikan Malayan Union dan menubuhkan Persekutuan Tanah Melayu?",
        pilihan: ["Perjanjian Persekutuan Tanah Melayu 1948", "Perjanjian Pangkor", "Perjanjian Malaysia 1963", "Perjanjian Bangkok"],
        jawapan: 0,
        fakta: "Perjanjian Persekutuan Tanah Melayu 1948 ditandatangani hasil bantahan keras orang Melayu terhadap Malayan Union."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: true,
        kategori: "Sejarah Perjanjian Perak",
        soalan: "Di manakah Perjanjian Pangkor dimeterai pada 20 Januari 1874 yang menjadi titik permulaan sistem Residen British di Perak?",
        pilihan: ["Pulau Pangkor (atas kapal HMS Pluto)", "Bandar Taiping", "Kuala Kangsar", "Teluk Anson"],
        jawapan: 0,
        fakta: "Perjanjian Pangkor ditandatangani di atas kapal HMS Pluto di perairan Pulau Pangkor antara Gabenor Negeri-Negeri Selat Andrew Clarke dengan Raja Abdullah."
    },
    {
        tahap: "sederhana",
        keutamaanPerak: false,
        kategori: "Sukan Tradisional Wau",
        soalan: "Apakah bahagian struktur wau tradisional yang berfungsi menghasilkan bunyi berdengung apabila ditiup angin di udara?",
        pilihan: ["Tali busur (rembat)", "Ekor wau", "Tanjak wau", "Sayap wau"],
        jawapan: 0,
        fakta: "Tali busur yang dipasang di bahagian atas wau akan bergetar dan menghasilkan bunyi berdengung yang khas apabila diterbangkan tinggi."
    },

    // --- TAHAP SUKAR (25-36) ---
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Sejarah Perang Perak",
        soalan: "Semasa Perang Perak (1875-1876), di manakah lokasi kubu pertahanan strategik tentera British diserang hebat oleh pejuang Melayu di bawah pimpinan Dato' Maharaja Lela dan Dato' Sagor?",
        pilihan: ["Pasir Salak", "Teluk Intan", "Kuala Kangsar", "Bota Kiri"],
        jawapan: 0,
        fakta: "Pasir Salak di tepi Sungai Perak menjadi kubu pertahanan pejuang Melayu sebelum J.W.W. Birch dibunuh di sungai tersebut."
    },
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Perlembagaan & Undang-undang",
        soalan: "Apakah nama manuskrip undang-undang tradisional yang menjadi panduan pentadbiran, agama, adat istiadat, dan hukuman jenayah dalam Kesultanan Perak pada abad ke-18?",
        pilihan: ["Undang-Undang 99 Perak", "Hukum Kanun Melaka", "Undang-Undang Tubuh Kerajaan Perak", "Adat Temenggung"],
        jawapan: 0,
        fakta: "Undang-Undang 99 Perak dibawa oleh Syed Hassan dari Hadhramaut dan mengandungi 99 fasal yang merangkumi aspek ketatanegaraan, kekeluargaan, dan jenayah."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Warisan Kraf Sarawak",
        soalan: "Apakah nama kain tenunan kapas berhias motif tradisional yang ditenun menggunakan teknik ikat oleh kaum Iban di Sarawak serta dianggap sebagai tekstil suci dalam upacara adat?",
        pilihan: ["Pua Kumbu", "Kain Tenun Pahang", "Songket Limar", "Kain Dastar"],
        jawapan: 0,
        fakta: "Pua Kumbu merupakan kain tenunan ikat tradisional masyarakat Iban di Sarawak yang dihasilkan menggunakan pewarna semula jadi dan mempunyai nilai adat yang tinggi."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Warisan Tidak Ketara UNESCO",
        soalan: "Pada tahun 2021, apakah nama seni tekstil tenunan benang emas dan perak tradisional Malaysia yang berjaya disenaraikan oleh UNESCO sebagai Warisan Budaya Tidak Ketara Kemanusiaan?",
        pilihan: ["Songket", "Telepuk", "Tekat", "Keringkam"],
        jawapan: 0,
        fakta: "Songket Malaysia telah diiktiraf oleh UNESCO dalam Senarai Wakil Warisan Budaya Tidak Ketara Kemanusiaan pada Disember 2021."
    },
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Sejarah Tentera & Pertempuran Perak",
        soalan: "Semasa Perang Dunia Kedua (1941-1942), pertempuran sengit antara tentera Berikat (termasuk Batalion ke-2 Askar Melayu) menentang tentera Jepun berlaku di Perak. Apakah nama tapak pertempuran terkenal di Perak utara?",
        pilihan: ["Pertempuran Kampar (Green Ridge)", "Pertempuran Slim River", "Pertempuran Kroh", "Pertempuran Tanjong Malim"],
        jawapan: 0,
        fakta: "Pertempuran Kampar di tapak Green Ridge menyaksikan tentera India, British, dan Askar Melayu menentang hebat kemaraan tentera Jepun pada Januari 1942."
    },
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Tokoh Diraja & Sejarah Perak",
        soalan: "Siapakah Sultan Perak yang merasmikan penubuhan Majlis Agama Islam dan Adat Melayu Perak (MAIPk) serta sangat terkenal dengan ketokohan keintelektualan dan dasar pembaharuan baginda pada awal abad ke-20?",
        pilihan: ["Sultan Idris Murshidul Azzam Shah (Sultan Idris I)", "Sultan Iskandar Shah", "Sultan Yussuf Izzuddin Shah", "Sultan Azlan Shah"],
        jawapan: 0,
        fakta: "Sultan Idris I (Sultan Perak ke-28) memerintah dari 1887 hingga 1916 dan sangat prihatin terhadap kemajuan pendidikan anak bangsa serta pembentukan reka bentuk bandar Taiping dan Kuala Kangsar."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Sejarah Perlembagaan Malaysia",
        soalan: "Apakah nama suruhanjaya bebas antarabangsa yang dipertanggungjawabkan merangka perlembagaan Persekutuan Tanah Melayu yang merdeka pada tahun 1956-1957?",
        pilihan: ["Suruhanjaya Reid", "Suruhanjaya Cobbold", "Suruhanjaya Laporan Jawatankuasa Pelajaran", "Suruhanjaya Semporna"],
        jawapan: 0,
        fakta: "Suruhanjaya Reid yang diketuai oleh Lord Reid menyiapkan draf Perlembagaan Persekutuan Tanah Melayu sebelum dikuatkuasakan pada 31 Ogos 1957."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Sejarah Pembentukan Malaysia",
        soalan: "Apakah nama suruhanjaya yang ditubuhkan pada tahun 1962 untuk menilai pandangan penduduk Sabah dan Sarawak berhubung cadangan pembentukan Malaysia?",
        pilihan: ["Suruhanjaya Cobbold", "Suruhanjaya Reid", "Suruhanjaya Landsborough", "Suruhanjaya MacMichael"],
        jawapan: 0,
        fakta: "Suruhanjaya Cobbold meninjau pendapat rakyat Sabah dan Sarawak dan mendapati majoriti besar menyokong pembentukan Malaysia pada 1963."
    },
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Seni Kraf Emas Perak",
        soalan: "Apakah nama seni sulaman tradisional diraja di Perak yang menggunakan benang emas ke atas kain baldu tebal menggunakan cuban dan mempamerkan motif awan larat?",
        pilihan: ["Seni Tekat Benang Emas (Kelingkan / Tekat Timbul)", "Seni Sulam Kelantan", "Seni Tenun Pahang", "Seni Songket Bungkus"],
        jawapan: 0,
        fakta: "Seni Tekat di Kuala Kangsar (khususnya di Kampung Sayong dan sekitar Perak) terkenal sebagai seni kraftangan diraja warisan turun-temurun."
    },
    {
        tahap: "sukar",
        keutamaanPerak: true,
        kategori: "Geografi & Sejarah Perak Tengah",
        soalan: "Apakah nama pulau atau beting pasir di Sungai Perak yang menjadi titik pertemuan penting laluan air tradisional antara daerah Perak Tengah, Hilir Perak, dan Manjung?",
        pilihan: ["Pulau Tiga / Lambor", "Pulau Pangkor", "Pulau Banding", "Pulau Sembilan"],
        jawapan: 0,
        fakta: "Kawasan sekitar Pulau Tiga dan Lambor di Daerah Perak Tengah kaya dengan sejarah kesultanan lama serta penempatan tradisional masyarakat pesisir sungai."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Warisan Seni Silat Melayu",
        soalan: "Dalam falsafah persilatan tradisional Melayu, apakah maksud ungkapan 'Berguru Kepada Allah, Berpaut Kepada Sunnah' dalam pembentukan jati diri pendekar?",
        pilihan: ["Prinsip tauhid dan integriti moral yang menjadi teras ketinggian akhlak pesilat", "Kemahiran menyerang musuh tanpa senjata", "Teknik pernafasan dalam menangkis pukulan", "Larangan menyertai pertandingan silat moden"],
        jawapan: 0,
        fakta: "Seni silat tradisional Melayu bukan sahaja mementingkan aspek pertahanan fizikal, malah mengutamakan nilai kerohanian, disiplin, dan ketakwaan."
    },
    {
        tahap: "sukar",
        keutamaanPerak: false,
        kategori: "Rukun Negara Malaysia",
        soalan: "Bilakah prinsip Rukun Negara diisytiharkan secara rasmi kepada seluruh rakyat Malaysia bagi memupuk perpaduan nasional selepas peristiwa 13 Mei 1969?",
        pilihan: ["31 Ogos 1970", "31 Ogos 1957", "16 September 1963", "1 Januari 1971"],
        jawapan: 0,
        fakta: "Rukun Negara diisytiharkan oleh Seri Paduka Baginda Yang di-Pertuan Agong pada 31 Ogos 1970 sempena sambutan Hari Kemerdekaan ke-13."
    }
];

let peserta = {};
let soalanDipilih = [];
let jawapanPeserta = [];
let indeks = 0;
let masa = 30;
let timer;
let pilihanAktif = null;
let mulaMasa;

// ============================================================
// 2. SISTEM MODAL KUSTOM (MENGGANTIKAN ALERT / CONFIRM / PROMPT)
// ============================================================
function tutupModal() {
    document.getElementById("customModal").classList.add("hidden");
    document.getElementById("modalInputWrap").classList.add("hidden");
    document.getElementById("modalInput").value = "";
}

function paparNotifikasi(tajuk, mesej) {
    document.getElementById("modalTitle").textContent = tajuk;
    document.getElementById("modalMsg").textContent = mesej;
    document.getElementById("modalInputWrap").classList.add("hidden");
    document.getElementById("modalActions").innerHTML = `
        <button class="primary" onclick="tutupModal()">FAHAM</button>
    `;
    document.getElementById("customModal").classList.remove("hidden");
}

function bukaAdminModal() {
    document.getElementById("modalTitle").textContent = "🔐 Log Masuk Admin";
    document.getElementById("modalMsg").textContent = "Sila masukkan kata laluan pentadbir (Lalai: warisan123):";
    document.getElementById("modalInputWrap").classList.remove("hidden");
    document.getElementById("modalActions").innerHTML = `
        <button class="outline" onclick="tutupModal()">BATAL</button>
        <button class="primary" onclick="semakKataLaluanAdmin()">MASUK</button>
    `;
    document.getElementById("customModal").classList.remove("hidden");
    setTimeout(() => document.getElementById("modalInput").focus(), 100);
}

function semakKataLaluanAdmin() {
    const pwd = document.getElementById("modalInput").value;
    if (pwd === "warisan123") {
        tutupModal();
        paparan("admin");
        dashboard();
    } else {
        document.getElementById("modalMsg").innerHTML = `<span style="color: var(--red); font-weight: 700;">Kata laluan tidak sah. Sila cuba lagi.</span>`;
        document.getElementById("modalInput").value = "";
        document.getElementById("modalInput").focus();
    }
}

function sahkanPadamRekod() {
    document.getElementById("modalTitle").textContent = "⚠️ Pengesahan Padam Rekod";
    document.getElementById("modalMsg").textContent = "Adakah anda pasti ingin memadam semua rekod penyertaan peserta secara kekal? Tindakan ini tidak boleh diundur.";
    document.getElementById("modalInputWrap").classList.add("hidden");
    document.getElementById("modalActions").innerHTML = `
        <button class="outline" onclick="tutupModal()">BATAL</button>
        <button class="danger" onclick="laksanaPadamRekod()">YA, PADAM SEMUA</button>
    `;
    document.getElementById("customModal").classList.remove("hidden");
}

function laksanaPadamRekod() {
    localStorage.removeItem("warisanData");
    tutupModal();
    dashboard();
    paparNotifikasi("Rekod Dipadam", "Semua rekod penyertaan peserta telah berjaya dibersihkan daripada sistem.");
}

// ============================================================
// 3. NAVIGASI & PEMILIHAN SOALAN RAWAK (KEUTAMAAN PERAK)
// ============================================================
function paparan(id) {
    const halaman = ["home", "register", "quiz", "result", "leaderboard", "admin", "certificateView"];
    halaman.forEach(x => document.getElementById(x).classList.add("hidden"));
    document.getElementById(id).classList.remove("hidden");
    window.scrollTo({ top: 0, behavior: 'smooth' });
}

function home() {
    clearInterval(timer);
    paparan("home");
}

function showRegister() {
    paparan("register");
}

function rawak(array) {
    let a = [...array];
    for (let i = a.length - 1; i > 0; i--) {
        let j = Math.floor(Math.random() * (i + 1));
        [a[i], a[j]] = [a[j], a[i]];
    }
    return a;
}

// Fungsi memilih soalan rawak dengan keutamaan tinggi (70% pemberat) kepada soalan Negeri Perak & 30% Warisan Malaysia
function pilihSoalanKeutamaanPerak(tahap, bilangan) {
    let kolamPerak = rawak(BANK_SOALAN.filter(q => q.tahap === tahap && q.keutamaanPerak));
    let kolamUmum = rawak(BANK_SOALAN.filter(q => q.tahap === tahap && !q.keutamaanPerak));
    let hasil = [];

    for (let i = 0; i < bilangan; i++) {
        if (kolamPerak.length > 0 && (Math.random() < 0.70 || kolamUmum.length === 0)) {
            hasil.push(kolamPerak.pop());
        } else if (kolamUmum.length > 0) {
            hasil.push(kolamUmum.pop());
        } else if (kolamPerak.length > 0) {
            hasil.push(kolamPerak.pop());
        }
    }
    return hasil;
}

function mulaKuiz() {
    let nama = document.getElementById("nama").value.trim();
    if (!nama) {
        paparNotifikasi("Maklumat Tidak Lengkap", "Sila masukkan nama penuh anda sebelum memulakan cabaran kuiz.");
        return;
    }

    peserta = {
        nama: nama,
        umur: document.getElementById("umur").value || "-",
        daerah: document.getElementById("daerah").value.trim() || "Perak Tengah",
        mod: document.getElementById("mod").value
    };

    // Jumlah 8 Soalan: 3 Mudah (30m) + 3 Sederhana (60m) + 2 Sukar (60m) = 150 Markah Maksimum
    let mudah = pilihSoalanKeutamaanPerak("mudah", 3);
    let sederhana = pilihSoalanKeutamaanPerak("sederhana", 3);
    let sukar = pilihSoalanKeutamaanPerak("sukar", 2);

    soalanDipilih = [...mudah, ...sederhana, ...sukar];
    jawapanPeserta = [];
    indeks = 0;
    mulaMasa = Date.now();

    paparan("quiz");
    paparSoalan();
}

// ============================================================
// 4. LOGIK PAPARAN SOALAN & PEMARKAHAN
// ============================================================
function paparSoalan() {
    clearInterval(timer);
    pilihanAktif = null;

    let q = soalanDipilih[indeks];
    let jumlahSoalan = soalanDipilih.length;
    let lencanaPerak = q.keutamaanPerak ? " • 🟡⚫⚪ PERAK" : " • 🇲🇾 MALAYSIA";

    document.getElementById("tahap").textContent = q.tahap.toUpperCase() + " | " + q.kategori + lencanaPerak;
    document.getElementById("nombor").textContent = "SOALAN " + (indeks + 1) + " DARIPADA " + jumlahSoalan;
    document.getElementById("soalan").textContent = q.soalan;
    document.getElementById("progress").style.width = (((indeks + 1) / jumlahSoalan) * 100) + "%";
    document.getElementById("next").disabled = true;
    document.getElementById("next").textContent = indeks === (jumlahSoalan - 1) ? "HANTAR JAWAPAN ✓" : "SOALAN SETERUSNYA →";

    let pilihan = rawak(q.pilihan.map((teks, i) => ({ teks: teks, betul: i === q.jawapan })));
    q.pilihanRawak = pilihan;

    let html = "";
    pilihan.forEach((p, i) => {
        html += `
        <button class="option" onclick="pilihJawapan(${i})">
            <span class="opt-letter">${String.fromCharCode(65 + i)}</span>
            <span>${p.teks}</span>
        </button>
        `;
    });
    document.getElementById("pilihan").innerHTML = html;

    if (peserta.mod === "pertandingan") {
        masa = 30;
        kiraMasa();
    } else {
        document.getElementById("timer").textContent = "🌿 MOD SANTAI";
    }
}

function pilihJawapan(i) {
    if (pilihanAktif !== null) return;
    pilihanAktif = i;

    let q = soalanDipilih[indeks];
    let betul = q.pilihanRawak[i].betul;

    jawapanPeserta[indeks] = { pilihan: i, betul: betul };

    let buttons = document.querySelectorAll(".option");
    buttons.forEach((b, n) => {
        if (n === i) {
            b.classList.add("selected");
        }
        b.disabled = true;
    });

    document.getElementById("next").disabled = false;
}

function kiraMasa() {
    document.getElementById("timer").textContent = "⏱️ " + masa + " SAAT";
    timer = setInterval(() => {
        masa--;
        document.getElementById("timer").textContent = "⏱️ " + masa + " SAAT";
        if (masa <= 0) {
            clearInterval(timer);
            jawapanPeserta[indeks] = { pilihan: null, betul: false };
            seterusnya(true);
        }
    }, 1000);
}

function seterusnya(auto = false) {
    if (pilihanAktif === null && !auto) {
        paparNotifikasi("Pilih Jawapan", "Sila pilih satu jawapan sebelum meneruskan ke soalan berikutnya.");
        return;
    }

    clearInterval(timer);

    if (indeks < soalanDipilih.length - 1) {
        indeks++;
        paparSoalan();
    } else {
        keputusan();
    }
}

function keputusan() {
    clearInterval(timer);
    let markah = 0;
    let betul = 0;
    let markahTahap = { mudah: 10, sederhana: 20, sukar: 30 };
    let jumlahSoalan = soalanDipilih.length;

    soalanDipilih.forEach((q, i) => {
        if (jawapanPeserta[i]?.betul) {
            markah += markahTahap[q.tahap];
            betul++;
        }
    });

    let salah = jumlahSoalan - betul;
    let tempoh = Math.round((Date.now() - mulaMasa) / 1000);

    let rekod = {
        nama: peserta.nama,
        umur: peserta.umur,
        daerah: peserta.daerah,
        markah: markah,
        betul: betul,
        salah: salah,
        masa: tempoh,
        tarikh: new Date().toISOString(),
        semakan: soalanDipilih.map((q, i) => ({
            soalan: q.soalan,
            pilihan: (jawapanPeserta[i]?.pilihan === null || jawapanPeserta[i]?.pilihan === undefined)
                ? "Tidak dijawab (Tamat masa)"
                : q.pilihanRawak[jawapanPeserta[i].pilihan].teks,
            jawapanBetul: q.pilihan[q.jawapan],
            betul: !!jawapanPeserta[i]?.betul,
            fakta: q.fakta
        }))
    };

    let data = JSON.parse(localStorage.getItem("warisanData") || "[]");
    data.push(rekod);
    localStorage.setItem("warisanData", JSON.stringify(data));

    paparan("result");

    document.getElementById("markahNum").textContent = markah;
    document.getElementById("namaKeputusan").textContent = peserta.nama;
    document.getElementById("betul").textContent = "✓ Betul: " + betul + " soalan";
    document.getElementById("salah").textContent = "✕ Salah: " + salah + " soalan";

    let pencapaian =
        markah >= 120 ? "CEMERLANG! PAKAR WARISAN PERAK 🌟" :
        markah >= 80 ? "SANGAT BAGUS! 👍" :
        markah >= 50 ? "MEMUASKAN 💡" :
        "TERUSKAN USAHA BELAJAR! 💪";

    document.getElementById("pencapaian").textContent = pencapaian;
    paparSemakan(rekod.semakan);
}

function paparSemakan(data) {
    let html = "";
    data.forEach((q, i) => {
        html += `
        <div class="review ${q.betul ? "correct" : "wrong"}">
            <div style="font-weight: 700; margin-bottom: 6px; color: var(--navy);">${i + 1}. ${q.soalan}</div>
            <p style="font-size: 14px; margin: 4px 0;">Jawapan anda: <strong>${q.pilihan}</strong></p>
            <p style="font-size: 14px; margin: 4px 0; color: var(--green);">Jawapan tepat: <strong>${q.jawapanBetul}</strong></p>
            <p style="font-size: 13px; margin-top: 8px; padding-top: 8px; border-top: 1px dashed rgba(0,0,0,0.1); color: var(--text-muted);">
                💡 <strong>Info Warisan:</strong> ${q.fakta}
            </p>
        </div>
        `;
    });
    document.getElementById("semakan").innerHTML = html;
}

// ============================================================
// 5. LEADERBOARD, SIJIL & ADMIN
// ============================================================
function showLeaderboard() {
    paparan("leaderboard");
    let data = JSON.parse(localStorage.getItem("warisanData") || "[]");
    data.sort((a, b) => b.markah - a.markah || a.masa - b.masa);

    let html = "";
    data.forEach((p, i) => {
        let pingat = i === 0 ? "🥇 " : i === 1 ? "🥈 " : i === 2 ? "🥉 " : "";
        html += `
        <tr>
            <td><strong>${pingat}#${i + 1}</strong></td>
            <td><strong>${p.nama}</strong></td>
            <td>${p.daerah}</td>
            <td><span class="pill-tag">${p.markah} / 150</span></td>
        </tr>
        `;
    });

    document.getElementById("ranking").innerHTML = html || `
    <tr><td colspan="4" style="text-align: center; color: var(--text-muted); padding: 24px;">Belum ada rekod penyertaan setakat ini. Jadilah peserta pertama!</td></tr>
    `;
}

function sijil() {
    let nama = peserta.nama || "Peserta";
    let markah = document.getElementById("markahNum").textContent + "/150";
    let tarikh = new Date().toLocaleDateString("ms-MY", { day: 'numeric', month: 'long', year: 'numeric' });

    document.getElementById("certNamaPeserta").textContent = nama;
    document.getElementById("certMarkahPeserta").textContent = "Pencapaian Markah: " + markah;
    document.getElementById("certTarikhPeserta").textContent = "Tarikh Dikeluarkan: " + tarikh;

    paparan("certificateView");
    setTimeout(() => {
        window.print();
    }, 300);
}

function dashboard() {
    let data = JSON.parse(localStorage.getItem("warisanData") || "[]");
    let jumlah = data.length;
    let purata = jumlah ? data.reduce((s, x) => s + x.markah, 0) / jumlah : 0;
    let tertinggi = jumlah ? Math.max(...data.map(x => x.markah)) : 0;

    document.getElementById("jumlahPeserta").textContent = jumlah;
    document.getElementById("purata").textContent = purata.toFixed(1) + "/150";
    document.getElementById("tertinggi").textContent = tertinggi + "/150";
}

function exportCSV() {
    let data = JSON.parse(localStorage.getItem("warisanData") || "[]");
    if (data.length === 0) {
        paparNotifikasi("Tiada Rekod", "Belum ada data penyertaan peserta untuk dimuat turun.");
        return;
    }
    let csv = "Nama,Umur,Tempat Tinggal,Markah,Betul,Salah,Masa (Saat)\n";
    data.forEach(p => {
        csv += `"${p.nama}",${p.umur},"${p.daerah}",${p.markah},${p.betul},${p.salah},${p.masa}\n`;
    });

    let blob = new Blob(["\ufeff" + csv], { type: "text/csv;charset=utf-8;" });
    let link = document.createElement("a");
    link.href = URL.createObjectURL(blob);
    link.download = "warisan-minda-perak-tengah.csv";
    link.click();
    URL.revokeObjectURL(link.href);
}
</script>

</body>
</html>