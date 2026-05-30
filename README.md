<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NHS Class Routine 2026</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Fraunces:opsz,wght@9..144,300;9..144,600;9..144,700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --ink: #0f1623;
  --paper: #f7f4ef;
  --cream: #ede9e2;
  --rule: #d4cfc6;
  --accent: #c0392b;
  --gold: #b8860b;
  --blue: #1a3a6b;
  --green: #1a5c3a;
  --muted: #7a7468;
  --highlight: #fff9e6;
  --shadow: 0 2px 12px rgba(15,22,35,0.09);
  --shadow-lg: 0 8px 40px rgba(15,22,35,0.15);
}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'DM Sans',sans-serif;background:var(--paper);color:var(--ink);min-height:100vh;}

/* ── HEADER ── */
.masthead{background:var(--ink);color:var(--paper);padding:0;}
.masthead-inner{max-width:1600px;margin:0 auto;padding:18px 24px 0;display:flex;align-items:flex-end;justify-content:space-between;gap:16px;flex-wrap:wrap;}
.masthead h1{font-family:'Fraunces',serif;font-size:clamp(22px,3vw,34px);font-weight:700;letter-spacing:-0.5px;line-height:1.1;}
.masthead h1 span{color:#e8b84b;font-weight:300;}
.masthead-meta{font-family:'DM Mono',monospace;font-size:11px;color:rgba(247,244,239,0.5);text-transform:uppercase;letter-spacing:1px;margin-top:4px;}
.masthead-actions{display:flex;gap:8px;align-items:center;flex-wrap:wrap;}
.day-strip{background:var(--blue);display:flex;overflow-x:auto;scrollbar-width:none;}
.day-strip::-webkit-scrollbar{display:none;}
.day-btn{flex:1;min-width:90px;padding:10px 16px;border:none;background:transparent;color:rgba(247,244,239,0.6);font-family:'DM Mono',monospace;font-size:11px;text-transform:uppercase;letter-spacing:1.5px;cursor:pointer;transition:all .2s;border-bottom:2px solid transparent;white-space:nowrap;}
.day-btn:hover{color:var(--paper);}
.day-btn.active{color:#e8b84b;border-bottom-color:#e8b84b;background:rgba(255,255,255,0.05);}

/* ── TOOLBAR ── */
.toolbar{max-width:1600px;margin:0 auto;padding:14px 24px;display:flex;gap:10px;align-items:center;flex-wrap:wrap;border-bottom:1px solid var(--rule);}
.search-wrap{position:relative;flex:1;min-width:180px;}
.search-wrap input{width:100%;padding:8px 12px 8px 36px;border:1.5px solid var(--rule);border-radius:6px;font-family:'DM Sans',sans-serif;font-size:13px;background:white;outline:none;transition:border .2s;}
.search-wrap input:focus{border-color:var(--blue);}
.search-icon{position:absolute;left:11px;top:50%;transform:translateY(-50%);color:var(--muted);font-size:14px;}
.btn{display:inline-flex;align-items:center;gap:6px;padding:8px 16px;border-radius:6px;border:none;cursor:pointer;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;transition:all .18s;white-space:nowrap;}
.btn-ink{background:var(--ink);color:var(--paper);}
.btn-ink:hover{background:#2a3545;}
.btn-blue{background:var(--blue);color:white;}
.btn-blue:hover{background:#0f2450;}
.btn-red{background:var(--accent);color:white;}
.btn-red:hover{background:#a93226;}
.btn-gold{background:var(--gold);color:white;}
.btn-gold:hover{background:#9a7009;}
.btn-ghost{background:transparent;color:var(--ink);border:1.5px solid var(--rule);}
.btn-ghost:hover{background:var(--cream);}
.btn-sm{padding:6px 12px;font-size:12px;}
.view-tabs{display:flex;gap:2px;background:var(--cream);border-radius:7px;padding:3px;}
.view-tab{padding:6px 14px;border:none;background:transparent;border-radius:5px;cursor:pointer;font-family:'DM Sans',sans-serif;font-size:12px;font-weight:500;color:var(--muted);transition:all .18s;}
.view-tab.active{background:white;color:var(--ink);box-shadow:0 1px 4px rgba(0,0,0,0.1);}

/* ── MAIN ── */
.main{max-width:1600px;margin:0 auto;padding:20px 24px;}

/* ── ROUTINE TABLE ── */
.table-card{background:white;border-radius:10px;box-shadow:var(--shadow);overflow:hidden;margin-bottom:20px;}
.table-card-header{padding:14px 20px;border-bottom:1px solid var(--rule);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:8px;}
.table-card-title{font-family:'Fraunces',serif;font-size:18px;font-weight:600;color:var(--ink);}
.table-wrap{overflow-x:auto;}
table{width:100%;border-collapse:collapse;font-size:12.5px;}
thead{position:sticky;top:0;z-index:10;}
thead tr{background:var(--ink);}
th{padding:10px 12px;text-align:center;color:var(--paper);font-family:'DM Mono',monospace;font-size:11px;text-transform:uppercase;letter-spacing:1px;font-weight:400;white-space:nowrap;border-right:1px solid rgba(255,255,255,0.07);}
th.teacher-col{text-align:left;width:80px;}
th:last-child{border-right:none;}
td{padding:0;border-bottom:1px solid var(--rule);border-right:1px solid var(--rule);vertical-align:top;}
td:last-child{border-right:none;}
tr:last-child td{border-bottom:none;}
tr:hover td{background:#fafaf8;}
.teacher-cell{padding:10px 12px;font-family:'DM Mono',monospace;font-size:12px;font-weight:500;color:var(--blue);white-space:nowrap;vertical-align:middle;background:var(--paper)!important;border-right:2px solid var(--rule)!important;position:sticky;left:0;z-index:5;}

/* ── PERIOD CELL ── */
.period-wrapper{min-height:56px;padding:0;position:relative;}
.period-content{padding:7px 10px;min-height:56px;display:flex;flex-direction:column;justify-content:center;gap:2px;cursor:pointer;transition:background .15s;}
.period-content:hover{background:var(--highlight);}
.period-content:hover .cell-edit-hint{opacity:1;}
.cell-class{font-family:'DM Mono',monospace;font-size:11px;font-weight:500;color:var(--ink);}
.cell-subj{font-size:11px;color:var(--muted);}
.cell-edit-hint{font-size:9px;color:var(--gold);opacity:0;transition:opacity .15s;margin-top:1px;}
.cell-empty{min-height:56px;cursor:pointer;}
.cell-empty:hover{background:rgba(184,134,11,0.05);}
.cell-empty-inner{height:56px;display:flex;align-items:center;justify-content:center;}
.plus-icon{font-size:14px;color:var(--rule);transition:color .15s;}
.cell-empty:hover .plus-icon{color:var(--gold);}

/* cell color coding */
.cell-sc{border-top:3px solid #1a5c3a;}
.cell-math{border-top:3px solid #1a3a6b;}
.cell-eng{border-top:3px solid #6b1a3a;}
.cell-bng{border-top:3px solid #6b4e1a;}
.cell-hist{border-top:3px solid #4a1a6b;}
.cell-geo{border-top:3px solid #1a5a6b;}
.cell-psc{border-top:3px solid #6b1a1a;}
.cell-che{border-top:3px solid #3a6b1a;}
.cell-bio{border-top:3px solid #1a6b5a;}
.cell-phy{border-top:3px solid #6b3a1a;}
.cell-com{border-top:3px solid #1a4a6b;}
.cell-other{border-top:3px solid #888;}
.cell-changed{border-top-color:var(--gold)!important;background:#fffbf0;}

/* stats bar */
.stats-bar{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:18px;}
.stat-pill{background:white;border:1px solid var(--rule);border-radius:8px;padding:10px 16px;display:flex;flex-direction:column;align-items:center;gap:2px;min-width:90px;box-shadow:var(--shadow);}
.stat-num{font-family:'Fraunces',serif;font-size:24px;font-weight:600;color:var(--ink);line-height:1;}
.stat-label{font-size:11px;color:var(--muted);text-transform:uppercase;letter-spacing:0.5px;}

/* change log */
.change-log{background:white;border-radius:10px;box-shadow:var(--shadow);padding:16px 20px;margin-bottom:20px;}
.change-log-title{font-family:'Fraunces',serif;font-size:16px;font-weight:600;margin-bottom:12px;}
.change-item{display:flex;align-items:flex-start;gap:12px;padding:10px 0;border-bottom:1px solid var(--rule);}
.change-item:last-child{border-bottom:none;}
.change-tag{font-family:'DM Mono',monospace;font-size:10px;background:var(--cream);border-radius:4px;padding:2px 7px;white-space:nowrap;flex-shrink:0;}
.change-old{color:var(--accent);text-decoration:line-through;font-size:12px;}
.change-arrow{color:var(--muted);}
.change-new{color:var(--green);font-weight:500;font-size:12px;}

/* ── MODAL ── */
.overlay{display:none;position:fixed;inset:0;background:rgba(15,22,35,0.6);z-index:200;align-items:center;justify-content:center;padding:20px;backdrop-filter:blur(2px);}
.overlay.open{display:flex;}
.modal{background:var(--paper);border-radius:12px;padding:28px;width:100%;max-width:440px;box-shadow:var(--shadow-lg);max-height:90vh;overflow-y:auto;}
.modal-title{font-family:'Fraunces',serif;font-size:20px;font-weight:700;color:var(--ink);margin-bottom:4px;}
.modal-close{float:right;background:none;border:none;font-size:20px;cursor:pointer;color:var(--muted);line-height:1;}
.modal-ctx{background:var(--cream);border-radius:6px;padding:10px 14px;font-family:'DM Mono',monospace;font-size:12px;margin-bottom:18px;color:var(--muted);}
.modal-ctx strong{color:var(--ink);}
.form-field{margin-bottom:14px;}
.form-label{display:block;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:0.5px;color:var(--muted);margin-bottom:6px;}
.form-input{width:100%;border:1.5px solid var(--rule);border-radius:6px;padding:9px 12px;font-family:'DM Mono',monospace;font-size:13px;background:white;color:var(--ink);outline:none;transition:border .2s;}
.form-input:focus{border-color:var(--blue);}
.modal-actions{display:flex;gap:8px;margin-top:6px;flex-wrap:wrap;}
.base-ref{font-size:11px;color:var(--muted);margin-bottom:16px;font-family:'DM Mono',monospace;}
.base-ref span{color:var(--accent);}

/* ── LEGEND ── */
.legend{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:16px;}
.legend-item{display:flex;align-items:center;gap:5px;font-size:11px;color:var(--muted);}
.legend-dot{width:10px;height:10px;border-radius:2px;}

/* teacher view */
.teacher-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:14px;margin-bottom:20px;}
.teacher-card{background:white;border-radius:10px;box-shadow:var(--shadow);overflow:hidden;}
.teacher-card-head{background:var(--blue);color:white;padding:12px 16px;display:flex;align-items:center;justify-content:space-between;}
.teacher-code{font-family:'DM Mono',monospace;font-size:16px;font-weight:500;}
.teacher-periods-count{font-size:11px;opacity:0.7;font-family:'DM Mono',monospace;}
.teacher-day-row{display:flex;gap:1px;padding:12px;}
.teacher-day-slot{flex:1;background:var(--cream);border-radius:4px;padding:5px 4px;text-align:center;}
.teacher-day-label{font-family:'DM Mono',monospace;font-size:8px;color:var(--muted);text-transform:uppercase;margin-bottom:2px;}
.teacher-period-list{font-size:9px;color:var(--ink);}

@media(max-width:700px){
  .masthead-inner{flex-direction:column;align-items:flex-start;}
  .main{padding:14px;}
  .toolbar{padding:10px 14px;}
  th,td{font-size:11px;}
  .period-content{padding:5px 7px;min-height:48px;}
}
@media print{
  header,.toolbar,.masthead-actions,.day-strip,.modal,.change-log,.legend,.stats-bar,.cell-edit-hint,.plus-icon{display:none!important;}
  body{background:white;}
  table{font-size:10px;}
  .teacher-cell{background:var(--paper)!important;-webkit-print-color-adjust:exact;}
}

/* ── PROVISIONAL ── */
.prov-banner{background:linear-gradient(90deg,#7b1fa2,#4a148c);color:white;border-radius:10px;padding:14px 20px;margin-bottom:16px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:10px;}
.prov-banner-title{font-family:'Fraunces',serif;font-size:17px;font-weight:600;}
.prov-banner-sub{font-size:12px;opacity:0.8;margin-top:2px;}
.absent-chips{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:18px;}
.absent-chip{display:flex;align-items:center;gap:7px;padding:7px 14px;border-radius:20px;border:1.5px solid var(--rule);background:white;cursor:pointer;font-size:13px;font-family:'DM Mono',monospace;transition:all .18s;user-select:none;}
.absent-chip:hover{border-color:#7b1fa2;background:#f3e5f5;}
.absent-chip.marked{background:#fce4ec;border-color:#c62828;color:#c62828;font-weight:600;}
.chip-dot{width:8px;height:8px;border-radius:50%;background:#4caf50;flex-shrink:0;}
.absent-chip.marked .chip-dot{background:#c62828;}
.prov-card{background:white;border-radius:10px;box-shadow:var(--shadow);overflow:hidden;margin-bottom:16px;}
.prov-card-head{background:linear-gradient(90deg,#4a148c,#6a1b9a);color:white;padding:12px 18px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:6px;}
.prov-card-head h3{font-family:'Fraunces',serif;font-size:15px;font-weight:600;}
.prov-period-row{border-bottom:1px solid var(--rule);padding:12px 18px;display:grid;grid-template-columns:50px 1fr;gap:12px;align-items:start;}
.prov-period-row:last-child{border-bottom:none;}
.prov-pnum{font-family:'DM Mono',monospace;font-size:22px;font-weight:500;color:#7b1fa2;padding-top:4px;}
.prov-items{display:flex;flex-direction:column;gap:8px;}
.prov-item{display:flex;align-items:center;gap:8px;flex-wrap:wrap;}
.tag-absent{font-family:'DM Mono',monospace;font-size:11px;background:#fce4ec;color:#c62828;border-radius:4px;padding:2px 7px;white-space:nowrap;border:1px solid #ef9a9a;}
.tag-class{font-family:'DM Mono',monospace;font-size:11px;background:var(--cream);border-radius:4px;padding:2px 7px;color:var(--ink);}
.tag-subj{font-family:'DM Mono',monospace;font-size:11px;color:var(--muted);padding:2px 0;}
.prov-arrow{color:var(--rule);font-size:12px;}
.prov-sel{border:1.5px solid var(--rule);border-radius:6px;padding:5px 10px;font-family:'DM Mono',monospace;font-size:12px;background:white;outline:none;min-width:100px;transition:border .18s;}
.prov-sel:focus{border-color:#7b1fa2;}
.prov-sel.assigned{background:#e8f5e9;border-color:#2e7d32;color:#1b5e20;}
.notice-card{background:#f3e5f5;border:1.5px solid #ce93d8;border-radius:10px;padding:16px 20px;margin-bottom:16px;}
.notice-card-title{font-family:'Fraunces',serif;font-size:15px;font-weight:600;color:#4a148c;margin-bottom:10px;display:flex;align-items:center;gap:8px;}
.notice-row{display:flex;align-items:center;gap:8px;padding:7px 0;border-bottom:1px solid #e1bee7;font-size:13px;flex-wrap:wrap;}
.notice-row:last-child{border-bottom:none;}
.ntag-period{font-family:'DM Mono',monospace;font-size:10px;background:#ce93d8;color:white;border-radius:4px;padding:2px 6px;flex-shrink:0;}
.ntag-absent{color:#c62828;text-decoration:line-through;font-size:12px;font-family:'DM Mono',monospace;}
.ntag-sub{color:#1b5e20;font-weight:700;font-family:'DM Mono',monospace;}
.ntag-class{font-size:11px;color:var(--muted);font-family:'DM Mono',monospace;}
.prov-empty{text-align:center;padding:50px 20px;color:var(--muted);}
.prov-empty .emoji{font-size:36px;display:block;margin-bottom:10px;}
</style>
</head>
<body>

<header>
  <div class="masthead">
    <div class="masthead-inner">
      <div>
        <div class="masthead-meta">Class Routine · 2025–26 Session</div>
        <h1>NHS <span>Timetable</span></h1>
      </div>
      <div class="masthead-actions">
        <button class="btn btn-gold btn-sm" onclick="resetAll()">↩ Reset All</button>
        <button class="btn btn-ghost btn-sm" onclick="window.print()">🖨 Print</button>
      </div>
    </div>
    <div class="day-strip" id="dayStrip"></div>
  </div>
</header>

<div class="toolbar">
  <div class="view-tabs">
    <button class="view-tab active" onclick="setView('routine')">📋 Routine</button>
    <button class="view-tab" onclick="setView('teacher')">👤 By Teacher</button>
    <button class="view-tab" onclick="setView('changes')">✏️ Changes</button>
    <button class="view-tab" onclick="setView('provisional')">🔄 Provisional</button>
  </div>
  <div class="search-wrap">
    <span class="search-icon">🔍</span>
    <input type="text" id="searchBox" placeholder="Search teacher / class / subject…" oninput="applySearch()">
  </div>
  <select id="classFilter" onchange="renderView()" style="padding:8px 12px;border:1.5px solid var(--rule);border-radius:6px;font-family:'DM Sans',sans-serif;font-size:13px;background:white;outline:none;">
    <option value="">All Classes</option>
    <option value="V">Class V</option>
    <option value="VI">Class VI</option>
    <option value="VII">Class VII</option>
    <option value="VIII">Class VIII</option>
    <option value="IX">Class IX</option>
    <option value="X">Class X</option>
    <option value="XI">Class XI</option>
    <option value="XII">Class XII</option>
  </select>
</div>

<div class="main" id="mainArea"></div>

<!-- Edit Modal -->
<div class="overlay" id="editOverlay">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-title">Edit Period</div>
    <div class="modal-ctx" id="editCtx"></div>
    <div class="base-ref" id="editBaseRef"></div>
    <div class="form-field">
      <label class="form-label">Class &amp; Section</label>
      <input class="form-input" id="editClass" list="classList" placeholder="e.g. IX-A, XII C+D…">
      <datalist id="classList">
        <option value="VA"><option value="VB"><option value="VC"><option value="VD">
        <option value="VIA"><option value="VIB"><option value="VIC"><option value="VID">
        <option value="VIIA"><option value="VIIB"><option value="VIIC"><option value="VIID">
        <option value="VIIIA"><option value="VIIIB"><option value="VIIIC"><option value="VIIID">
        <option value="IXA"><option value="IXB"><option value="IXC"><option value="IXD">
        <option value="XA"><option value="XB"><option value="XC"><option value="XD">
        <option value="XIA"><option value="XIB"><option value="XIC"><option value="XID">
        <option value="XI C+D"><option value="XI A+B">
        <option value="XIIA"><option value="XIIB"><option value="XIIC"><option value="XIID">
        <option value="XII C+D"><option value="XII A+B">
      </datalist>
    </div>
    <div class="form-field">
      <label class="form-label">Subject</label>
      <input class="form-input" id="editSubject" list="subjectList" placeholder="e.g. MATH, ENG, HIST…">
      <datalist id="subjectList">
        <option value="MATH"><option value="ENG"><option value="BENG"><option value="HIST">
        <option value="GEO"><option value="PSC"><option value="LSC"><option value="CHE">
        <option value="PHY"><option value="BIO"><option value="COMP"><option value="P.ED">
        <option value="W.ED"><option value="AP"><option value="GN"><option value="GK">
        <option value="GC"><option value="SC"><option value="LIB"><option value="EDU">
        <option value="COST"><option value="BSTD"><option value="ACCT"><option value="POLS">
        <option value="HINDI"><option value="PRAC"><option value="TH"><option value="GM">
        <option value="HW"><option value="E.ED"><option value="G.SC"><option value="G.M">
        <option value="ECO"><option value="BNG"><option value="BEG">
      </datalist>
    </div>
    <div class="form-field">
      <label class="form-label">Note (optional)</label>
      <input class="form-input" id="editNote" placeholder="e.g. TH, PRAC, (TH)…">
    </div>
    <div class="modal-actions">
      <button class="btn btn-blue" style="flex:1;justify-content:center" onclick="saveEdit()">💾 Save</button>
      <button class="btn btn-red btn-sm" onclick="clearCell()">🗑 Clear</button>
      <button class="btn btn-ghost btn-sm" onclick="revertCell()">↩ Revert</button>
      <button class="btn btn-ghost btn-sm" onclick="closeModal()">Cancel</button>
    </div>
  </div>
</div>

<script>
// ════════════════════════════════════════════════════════════
// DATA — Full routine from PDF (teacher × period × day)
// Format: teacherCode → { day → [p1, p2, … p8] }
// Each period: "CLASS SUBJ NOTE" or "" for free
// ════════════════════════════════════════════════════════════

const DAYS = ['Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];
const PERIODS = 8;

// Teacher list with codes
const TEACHERS = [
  'KCD','TR','SS1','SB1','SB2','JGG','SP1','AKM','BB1','SB3',
  'LBS','SP2','AG1','JM','DC','AB1','SB4','CRM','AB2','DN',
  'TA','BB2','AG2','AM','SB5','SRM','SM','SP3','BKM','MM1',
  'BKG','SD','SKG','MM2','AR','SSD','BD2','NB','DS','SS3',
  'HNM','KKD','UB','PG','AJ','BD1','BM2','AD2','AC','SS2',
  'SG','TS','PC','PKS','MR.COMM'
];

// Full base data extracted from PDF
// Format per cell: [classSection, subject, note?]
// "" = free period
const BASE = {
  Monday: {
    KCD: [["XIID","PHY","TH"],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["KCD","",""]],
    TR:  [["","",""],["XIB","ENG",""],["XIA","ENG",""],["XD","ENG",""],["XA","ENG",""],["","",""],["","",""],["TR","",""]],
    SS1: [["","",""],["","",""],["XIIA","BNG",""],["XIB","BENG",""],["XIIB","BENG",""],["","",""],["","",""],["SS1","",""]],
    SB1: [["","",""],["","",""],["","",""],["VIB","GEO",""],["IXC","GEO",""],["XA","GEO",""],["XB","GEO",""],["SB1","",""]],
    SB2: [["","",""],["","",""],["","",""],["","",""],["IXB","HIST",""],["VID","HIST",""],["VIIC","HIST",""],["XC","HIST",""],["SB2","",""]],
    JGG: [["","",""],["","",""],["","",""],["","",""],["","",""],["VC","MATH",""],["VB","AP",""],["VC","GK",""],["JGG","",""]],
    SP1: [["","",""],["","",""],["","",""],["","",""],["VIA","ENG",""],["XC","ENG",""],["VIIIC","ENG",""],["VIIB","ENG",""],["SP1","",""]],
    AKM: [["","",""],["","",""],["","",""],["","",""],["XB","MATH",""],["VIIA","MATH",""],["IXB","PSC",""],["XD","PSC",""],["AKM","",""]],
    BB1: [["","",""],["","",""],["","",""],["","",""],["VIIIA","ENG",""],["VIB","ENG",""],["VIIIC","ENG",""],["","",""],["BB1","",""]],
    SB3: [["","",""],["","",""],["","",""],["","",""],["IXA","MATH",""],["IXD","MATH",""],["VIIIC","MATH",""],["VIB","MATH",""],["SB3","",""]],
    LBS: [["XD","LSC",""],["XA","LSC",""],["","",""],["VIIIA","LSC",""],["IXD","LSC",""],["","",""],["VIID","LSC",""],["","",""],["LBS","",""]],
    SP2: [["","",""],["","",""],["","",""],["","",""],["VA","MATH",""],["XC","MATH",""],["VIIID","MATH",""],["VID","MATH",""],["VIID","MATH",""],["SP2","",""]],
    AG1: [["","",""],["","",""],["","",""],["","",""],["XIIC","CHE",""],["XID","CHE",""],["VIIID","PSC",""],["VIID","PSC",""],["AG1","",""]],
    JM:  [["","",""],["","",""],["","",""],["","",""],["VIIIA","PSC",""],["VIIB","MATH",""],["VIIC","PSC",""],["VIIIC","PSC",""],["VIIIA","PSC",""],["JM","",""]],
    DC:  [["","",""],["","",""],["","",""],["","",""],["","",""],["XIC+D","ENG",""],["IXA","ENG",""],["VB","ENG",""],["DC","",""]],
    AB1: [["","",""],["","",""],["","",""],["","",""],["VID","ENG",""],["XIB","ENG",""],["VIID","ENG",""],["VIIID","ENG",""],["AB1","",""]],
    SB4: [["","",""],["","",""],["","",""],["","",""],["XIIC+D","PRAC",""],["XIIC+D","PRAC",""],["XC","LSC",""],["IXC","LSC",""],["SB4","",""]],
    CRM: [["","",""],["","",""],["","",""],["","",""],["","",""],["XIC+D","MATH",""],["IXC","MATH",""],["XA","MATH",""],["CRM","",""]],
    AB2: [["","",""],["","",""],["","",""],["","",""],["XA","PSC",""],["XIIC+D","PRAC",""],["XIIC+D","PRAC",""],["IXD","PSC",""],["XIC","PHY",""],["AB2","",""]],
    DN:  [["","",""],["","",""],["","",""],["","",""],["","",""],["XIIC+D","PRAC",""],["XIIC+D","PRAC",""],["XB","PSC",""],["DN","",""]],
    TA:  [["","",""],["","",""],["","",""],["","",""],["","",""],["XB","ENG",""],["VIC","ENG",""],["IXC","ENG",""],["VC","ENG",""],["VIIA","ENG",""],["TA","",""]],
    BB2: [["","",""],["","",""],["","",""],["","",""],["VIC","BENG",""],["VIIC","BENG",""],["VA","BENG",""],["VIIA","W.ED",""],["VIIID","W.ED",""],["BB2","",""]],
    AG2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIB","MATH",""],["VB","MATH",""],["VIIA","MATH",""],["AG2","",""]],
    AM:  [["","",""],["","",""],["","",""],["","",""],["","",""],["VIC","P.ED",""],["VIIB","GEO",""],["VB","AP",""],["AM","",""]],
    SB5: [["","",""],["","",""],["","",""],["","",""],["","",""],["VIIB","HIST",""],["IXA","HIST",""],["VIB","HIST",""],["XA","HIST",""],["VIIC","HIST",""],["SB5","",""]],
    SRM: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIA","HIST",""],["XIIA","HIST",""],["IXC","HIST",""],["XD","HIST",""],["SRM","",""]],
    SM:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIIA","ENG",""],["IXD","ENG",""],["VIIC","ENG",""],["VA","ENG",""],["SM","",""]],
    SP3: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIID","GEO",""],["VIIIC","GEO",""],["VID","GEO",""],["IXA","GEO",""],["SP3","",""]],
    BKM: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["IXB","MATH",""],["XD","MATH",""],["VIC","MATH",""],["BKM","",""]],
    MM1: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["IXD","BENG",""],["XIC+D","BENG",""],["XIA","BNG",""],["MM1","",""]],
    BKG: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIA","SC",""],["VIC","SC",""],["VC","AP",""],["VID","W.ED",""],["VIIB","E.ED",""],["BKG","",""]],
    SD:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIID","BENG",""],["XA","BENG",""],["XC","BENG",""],["IXB","BENG",""],["SD","",""]],
    SKG: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIB","COST",""],["XIB","BSTD",""],["SKG","",""]],
    MM2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XC","GEO",""],["VIIID","GEO",""],["XIIA","GEO",""],["XIA","GEO",""],["PRAC","XIA GEO",""],["MM2","",""]],
    AR:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIA","GEO",""],["VID","BENG",""],["VA","AP",""],["IXD","GEO",""],["AR","",""]],
    SSD: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIIB","ENG",""],["IXB","ENG",""],["VIIB","ENG",""],["XIIC+D","ENG",""],["SSD","",""]],
    BD2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VID","BENG",""],["VIA","BENG",""],["XIA","EDU",""],["XIIA","EDU",""],["BD2","",""]],
    NB:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIIC","LSC",""],["XIIC+D","BIO",""],["XIC+D","TH",""],["XB","LSC",""],["NB","",""]],
    DS:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIC","MATH",""],["VIIIA","MATH",""],["VIA","MATH",""],["XIIC+D","MATH",""],["DS","",""]],
    SS3: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["IXC","PSC",""],["XC","PSC",""],["XIIC","TH-PHY",""],["XID","PHY",""],["SS3","",""]],
    HNM: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VB","BNG",""],["XD","BENG",""],["IXA","BENG",""],["IXB","BENG",""],["HNM","",""]],
    KKD: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIA+B","LIB",""],["VIIID","LIB",""],["IXB","LIB",""],["XIC+D","LIB",""],["KKD","",""]],
    UB:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["IXD","HIST",""],["XB","HIST",""],["VIC","HIST",""],["UB","",""]],
    PG:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIID","CHE","TH"],["XIC","CHE",""],["VIIB","PSC",""],["PG","",""]],
    AJ:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["AJ","",""]],
    BD1: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIIC","BENG",""],["VIID","BENG",""],["VIIA","BENG",""],["VIB","BENG",""],["BD1","",""]],
    BM2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["IXC","BENG",""],["XB","BENG",""],["VIIIA","BENG",""],["VIIB","BENG",""],["BM2","",""]],
    AD2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIID","HIST",""],["VC","AP",""],["VIIC","GEO",""],["AD2","",""]],
    AC:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIIC+D","TH",""],["XIIC+D","PRAC",""],["XIIC+D","PRAC",""],["XIC+D","TH",""],["XIIA+B","PRAC",""],["XIIA+B","PRAC",""],["AC","",""]],
    SS2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VB","GN",""],["SS2","",""]],
    SG:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XD","COMP",""],["SG","",""]],
    TS:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIA","COMP",""],["VIIIA","COMP",""],["VA","COMP",""],["VIA","COMP",""],["IXA","COMP",""],["TS","",""]],
    PC:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["PC","",""]],
    PKS: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["VIIC","HINDI",""],["VIID","HINDI",""],["VIIIC","HINDI",""],["VIIID","HINDI",""],["PKS","",""]],
    "MR.COMM":[["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["XIIB","ACCT",""],["XIIB","COST",""],["XIIB","BSTD",""],["XIB","ACCT",""],["MR.COMM","",""]],
  },
  // Tuesday – Thursday – Friday use simplified but correct key periods from PDF
  Tuesday: {
    KCD: [["VIID","PSC",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["KCD","",""]],
    TR:  [["","",""],["VID","ENG",""],["IXA","ENG",""],["VIIB","ENG",""],["XIA","ENG",""],["","",""],["","",""],["TR","",""]],
    SS1: [["","",""],["XA","BENG",""],["","",""],["XIC+D","BNG",""],["XIA","BENG",""],["IXC","BENG",""],["","",""],["SS1","",""]],
    SB1: [["","",""],["","",""],["VIB","GEO",""],["IXC","GEO",""],["","",""],["","",""],["","",""],["SB1","",""]],
    SB2: [["","",""],["","",""],["","",""],["IXB","HIST",""],["VIIA","HIST",""],["VIA","HIST",""],["VIIC","HIST",""],["SB2","",""]],
    JGG: [["","",""],["","",""],["","",""],["","",""],["VIA","MATH",""],["VIC","MATH",""],["VC","MATH",""],["JGG","",""]],
    SP1: [["","",""],["VB","ENG",""],["","",""],["VIIIC","ENG",""],["VC","AP",""],["VB","ENG",""],["","",""],["SP1","",""]],
    AKM: [["","",""],["","",""],["","",""],["XB","MATH",""],["IXD","MATH",""],["VIIA","MATH",""],["XD","PSC",""],["IXA","PSC",""],["AKM","",""]],
    BB1: [["","",""],["VIIA","ENG",""],["","",""],["IXB","ENG",""],["XC","ENG",""],["VIIA","ENG",""],["","",""],["BB1","",""]],
    SB3: [["","",""],["IXA","MATH",""],["","",""],["VIIIC","MATH",""],["VIIC","GM",""],["VIIB","MATH",""],["","",""],["SB3","",""]],
    LBS: [["XD","LSC",""],["","",""],["","",""],["VIC","SC",""],["IXC","LSC",""],["IXD","LSC",""],["XA","LSC",""],["LBS","",""]],
    SP2: [["VA","MATH",""],["","",""],["","",""],["VID","MATH",""],["XC","MATH",""],["VIID","MATH",""],["VIIID","MATH",""],["SP2","",""]],
    AG1: [["XIIC","CHE",""],["","",""],["","",""],["VA","MATH",""],["XIC","CHEM",""],["VIID","PSC",""],["XIC+D","PRAC",""],["XIC+D","PRAC",""],["AG1","",""]],
    JM:  [["VIIIA","PSC",""],["","",""],["","",""],["VB","AP",""],["VIIIC","PSC",""],["VA","AP",""],["VIIIA","GSC",""],["JM","",""]],
    DC:  [["XIIC+D","ENG",""],["","",""],["","",""],["VIIID","ENG",""],["XA","ENG",""],["VIA","ENG",""],["XIIB","ENG",""],["DC","",""]],
    AB1: [["VID","ENG",""],["","",""],["","",""],["XIIA","ENG",""],["XB","ENG",""],["XIB","ENG",""],["VIID","ENG",""],["AB1","",""]],
    SB4: [["","",""],["","",""],["","",""],["IXA","LSC",""],["XIC+D","TH",""],["XIIC+D","BIO",""],["XC","LSC",""],["SB4","",""]],
    CRM: [["","",""],["","",""],["","",""],["XIIC+D","MATH",""],["XA","MATH",""],["IXC","MATH",""],["CRM","",""]],
    AB2: [["","",""],["","",""],["","",""],["XA","PSC",""],["XIID","PHY",""],["IXD","PSC",""],["","",""],["AB2","",""]],
    DN:  [["","",""],["","",""],["","",""],["","",""],["XID","CHE",""],["XIIC","CHEM",""],["","",""],["DN","",""]],
    TA:  [["","",""],["","",""],["","",""],["IXC","ENG",""],["VIIIA","ENG",""],["VA","ENG",""],["VIC","ENG",""],["TA","",""]],
    BB2: [["","",""],["VIC","BENG",""],["","",""],["VIC","BENG",""],["VIA","BENG",""],["VIID","W.ED",""],["","",""],["BB2","",""]],
    AG2: [["","",""],["IXB","MATH",""],["","",""],["VIB","MATH",""],["VIIB","MATH",""],["VB","MATH",""],["","",""],["AG2","",""]],
    AM:  [["","",""],["","",""],["","",""],["VA","P.ED",""],["VID","P.ED",""],["VIIC","P.ED",""],["","",""],["AM","",""]],
    SB5: [["","",""],["VIIB","HIST",""],["","",""],["VC","AP",""],["VIIID","HIST",""],["IXA","HIST",""],["XA","HIST",""],["SB5","",""]],
    SRM: [["","",""],["","",""],["","",""],["XIA","HIST",""],["IXC","HIST",""],["VIIIC","HIST",""],["XD","HIST",""],["SRM","",""]],
    SM:  [["XIIA","ENG",""],["","",""],["","",""],["XIC+D","ENG",""],["VIB","ENG",""],["XD","ENG",""],["IXD","ENG",""],["VIIC","ENG",""],["SM","",""]],
    SP3: [["XB","GEO",""],["","",""],["","",""],["VIID","GEO",""],["IXA","GEO",""],["VID","GEO",""],["VIIIC","GEO",""],["SP3","",""]],
    BKM: [["","",""],["","",""],["","",""],["XD","MATH",""],["IXB","MATH",""],["XB","MATH",""],["","",""],["BKM","",""]],
    MM1: [["","",""],["","",""],["","",""],["IXD","BENG",""],["XIIA","B",""],["XIIC+D","BENG",""],["XIB","BENG",""],["MM1","",""]],
    BKG: [["","",""],["","",""],["","",""],["VIB","SC",""],["VA","AP",""],["VC","AP",""],["","",""],["BKG","",""]],
    SD:  [["VIIID","BENG",""],["","",""],["","",""],["VIIID","BENG",""],["XD","BENG",""],["IXA","BENG",""],["VID","BENG",""],["SD","",""]],
    SKG: [["XIIB","BSTD",""],["","",""],["","",""],["XIB","ACCT",""],["XIIB","BSTD",""],["XIIB","COST",""],["XIB","BSTD",""],["SKG","",""]],
    MM2: [["XC","GEO",""],["","",""],["","",""],["XC","GEO",""],["XIA","GEO",""],["VIIID","GEO",""],["IXB","GEO",""],["MM2","",""]],
    AR:  [["IXD","GEO",""],["","",""],["","",""],["VIIA","GEO",""],["XD","GEO",""],["IXD","GEO",""],["VIIIA","GEO",""],["VIC","GEO",""],["AR","",""]],
    SSD: [["XIIB","ENG",""],["","",""],["","",""],["VC","ENG",""],["XIIC+D","ENG",""],["VIIC","ENG",""],["XD","ENG",""],["SSD","",""]],
    BD2: [["VC","BENG",""],["","",""],["","",""],["XIIA","EDU",""],["VIIC","BENG",""],["VC","BENG",""],["VA","BENG",""],["VIIB","BEG",""],["BD2","",""]],
    NB:  [["VIIIC","LSC",""],["","",""],["","",""],["XB","LSC",""],["IXB","LSC",""],["XIC+D","PRAC",""],["XIC+D","PRAC",""],["NB","",""]],
    DS:  [["","",""],["","",""],["","",""],["VIIC","MATH",""],["VIIIA","MATH",""],["IXA","MATH",""],["XIC+D","MATH",""],["XC","MATH",""],["DS","",""]],
    SS3: [["IXC","PSC",""],["","",""],["","",""],["XIIC","PSC",""],["VIIID","PSC",""],["XIC+D","PRAC",""],["XIC+D","PRAC",""],["SS3","",""]],
    HNM: [["","",""],["","",""],["","",""],["VB","BENG",""],["XB","BENG",""],["XC","BENG",""],["VIIIA","BENG",""],["VIIA","BENG",""],["HNM","",""]],
    KKD: [["","",""],["","",""],["","",""],["VIIC","LIB",""],["XIIB","LIB",""],["XA","LIB",""],["XIIC+D","LIB",""],["VIIIA","LIB",""],["KKD","",""]],
    UB:  [["","",""],["","",""],["","",""],["IXD","HIST",""],["XIIA","HIS",""],["VIIID","HIST",""],["XB","HIST",""],["UB","",""]],
    PG:  [["VIIC","PSC",""],["","",""],["","",""],["XC","PSC",""],["IXC","PSC",""],["XIID","CHEM",""],["","",""],["PG","",""]],
    AJ:  [["","",""],["","",""],["","",""],["VIA","SC",""],["VIIA","LSC",""],["VID","SC",""],["VIIB","LSC",""],["AJ","",""]],
    BD1: [["VIID","BENG",""],["","",""],["","",""],["VIIIC","BENG",""],["VIB","BENG",""],["VIID","BENG",""],["VIIA","BNG",""],["BD1","",""]],
    BM2: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["BM2","",""]],
    AD2: [["VIA","GEO",""],["","",""],["","",""],["VIID","HIST",""],["VIC","HIST",""],["VIIC","GEO",""],["VIA","GEO",""],["AD2","",""]],
    AC:  [["","",""],["","",""],["","",""],["XIA+B","TH",""],["XIC+D","TH",""],["XIIC+D","TH",""],["","",""],["AC","",""]],
    SS2: [["","",""],["","",""],["","",""],["XIB","GC",""],["XIB","GC",""],["","",""],["","",""],["SS2","",""]],
    SG:  [["","",""],["","",""],["","",""],["XIB","GC",""],["","",""],["","",""],["","",""],["SG","",""]],
    TS:  [["","",""],["","",""],["","",""],["VB","COMP",""],["VB","COMP",""],["VIB","COMP",""],["VIB","COMP",""],["TS","",""]],
    PC:  [["XIA","POLS",""],["","",""],["","",""],["VIIIA","HIST",""],["XIA","POLS",""],["XIIA","POLS",""],["","",""],["PC","",""]],
    PKS: [["","",""],["","",""],["","",""],["VIIB","HINDI",""],["VIIIA","HINDI",""],["VIIA","HINDI",""],["VIIID","HINDI",""],["PKS","",""]],
    "MR.COMM":[["XIB","ACCT",""],["","",""],["","",""],["XIB","ACCT",""],["XIIB","BSTD",""],["XIIB","ACC",""],["XIIB","COST",""],["MR.COMM","",""]],
  },
  Wednesday: {
    KCD: [["","",""],["VIID","PSC",""],["XID","PHY",""],["XID","PHY",""],["","",""],["","",""],["XB","PSC",""],["KCD","",""]],
    TR:  [["","",""],["XIIC+D","ENG",""],["","",""],["VIC","ENG",""],["VIIB","ENG",""],["","",""],["","",""],["TR","",""]],
    SS1: [["","",""],["XIIB","BENG",""],["","",""],["XIIA","BNG",""],["XIIC+D","BENG",""],["","",""],["","",""],["SS1","",""]],
    SB1: [["VIB","GEO",""],["XIIA","GEO",""],["","",""],["XIA","GEO",""],["XA","GEO",""],["VIIIC","GEO",""],["","",""],["SB1","",""]],
    SB2: [["IXB","HIST",""],["VIA","HIST",""],["","",""],["XC","HIST",""],["VID","HIS",""],["VIIIC","HIST",""],["","",""],["SB2","",""]],
    JGG: [["","",""],["","",""],["VB","AP",""],["","",""],["","",""],["VC","MATH",""],["","",""],["JGG","",""]],
    SP1: [["VID","ENG",""],["VIIB","ENG",""],["","",""],["IXC","ENG",""],["VIIIC","ENG",""],["XC","ENG",""],["","",""],["SP1","",""]],
    AKM: [["XB","MATH",""],["","",""],["IXD","MATH",""],["VIIIC","MATH",""],["","",""],["IXA","PSC",""],["VIIA","MATH",""],["AKM","",""]],
    BB1: [["","",""],["VIB","ENG",""],["","",""],["","",""],["VIID","ENG",""],["","",""],["","",""],["BB1","",""]],
    SB3: [["IXA","MATH",""],["XA","MATH",""],["","",""],["VIC","MATH",""],["VIIB","MATH",""],["","",""],["","",""],["SB3","",""]],
    LBS: [["","",""],["","",""],["IXD","LSC",""],["VIB","LSC",""],["IXC","LSC",""],["","",""],["","",""],["LBS","",""]],
    SP2: [["VA","MATH",""],["","",""],["VID","MATH",""],["VIID","MATH",""],["IXC","MATH",""],["","",""],["","",""],["SP2","",""]],
    AG1: [["XIID","CHE","TH"],["XA","PSC",""],["","",""],["IXB","PSC",""],["XID","CHE",""],["","",""],["","",""],["AG1","",""]],
    JM:  [["VIIIA","PSC",""],["VIIB","MATH",""],["","",""],["VIIIC","PSC",""],["XD","PSC",""],["","",""],["","",""],["JM","",""]],
    DC:  [["","",""],["IXA","ENG",""],["","",""],["VIA","ENG",""],["XIIB","ENG",""],["XA","ENG",""],["","",""],["DC","",""]],
    AB1: [["VID","ENG",""],["VIIID","ENG",""],["","",""],["IXD","ENG",""],["XB","ENG",""],["","",""],["","",""],["AB1","",""]],
    SB4: [["XC","LSC",""],["XIC+D","TH",""],["","",""],["IXA","LSC",""],["XC","LSC",""],["VIIC","LSC",""],["VIIID","G.SC",""],["SB4","",""]],
    CRM: [["XA","MATH",""],["","",""],["IXC","MATH",""],["VIIID","MATH",""],["VIIIA","G.M",""],["VIID","MATH",""],["","",""],["CRM","",""]],
    AB2: [["XA","PSC",""],["XIC","PHY",""],["","",""],["VB","MATH",""],["IXD","PSC",""],["","",""],["VIIC","GSC",""],["AB2","",""]],
    DN:  [["","",""],["XB","PSC",""],["","",""],["","",""],["XIC","CHE",""],["","",""],["","",""],["DN","",""]],
    TA:  [["VIIIA","ENG",""],["","",""],["VIIIA","ENG",""],["VA","ENG",""],["VIC","ENG",""],["","",""],["","",""],["TA","",""]],
    BB2: [["VIC","BENG",""],["VIB","W.ED",""],["","",""],["","",""],["VA","BENG",""],["","",""],["","",""],["BB2","",""]],
    AG2: [["XIC+D","MATH",""],["","",""],["XD","MATH",""],["VIIIA","MATH",""],["VIB","MATH",""],["","",""],["","",""],["AG2","",""]],
    AM:  [["","",""],["VIIA","P.ED",""],["","",""],["VIID","P.ED",""],["VIIIA","GEO",""],["VIIB","GEO",""],["","",""],["AM","",""]],
    SB5: [["VIIB","HIST",""],["","",""],["VA","AP",""],["","",""],["XA","HIST",""],["","",""],["","",""],["SB5","",""]],
    SRM: [["XIIA","HIST",""],["XIIA","HIST",""],["","",""],["XD","HIST",""],["IXC","HIST",""],["VIIA","HIST",""],["","",""],["SRM","",""]],
    SM:  [["","",""],["XIA","ENG",""],["","",""],["VC","HW",""],["XD","ENG",""],["","",""],["","",""],["SM","",""]],
    SP3: [["VIID","GEO",""],["IXA","GEO",""],["","",""],["VID","GEO",""],["VA","AP",""],["","",""],["","",""],["SP3","",""]],
    BKM: [["","",""],["VIIC","MATH",""],["","",""],["XB","MATH",""],["XIIC+D","MATH",""],["IXB","MATH",""],["","",""],["BKM","",""]],
    MM1: [["IXD","BENG",""],["XIB","BENG",""],["","",""],["XIC+D","BNG",""],["XIA","BNG",""],["VIIIC","BNG",""],["","",""],["MM1","",""]],
    BKG: [["VIA","SC",""],["VA","AP",""],["","",""],["VB","AP",""],["VIIIA","W.ED",""],["","",""],["","",""],["BKG","",""]],
    SD:  [["","",""],["VID","BENG",""],["","",""],["XC","BENG",""],["IXA","BENG",""],["","",""],["","",""],["SD","",""]],
    SKG: [["XIIB","COST",""],["XIIB","COST",""],["","",""],["XIB","COST",""],["","",""],["","",""],["","",""],["SKG","",""]],
    MM2: [["","",""],["IXB","GEO",""],["","",""],["VIIID","GEO",""],["VIID","GEO",""],["","",""],["","",""],["MM2","",""]],
    AR:  [["","",""],["VIIA","GEO",""],["","",""],["VIC","GEO",""],["XD","GEO",""],["","",""],["","",""],["AR","",""]],
    SSD: [["XD","ENG",""],["XIB","ENG",""],["","",""],["IXB","ENG",""],["VC","ENG",""],["","",""],["","",""],["SSD","",""]],
    BD2: [["","",""],["XIA","EDU",""],["","",""],["VIA","BENG",""],["VIIC","BNG",""],["","",""],["","",""],["BD2","",""]],
    NB:  [["VIIIC","LSC",""],["XIIC+D","BIO",""],["","",""],["","",""],["IXB","LSC",""],["","",""],["","",""],["NB","",""]],
    DS:  [["VIIC","MATH",""],["XC","MATH",""],["","",""],["VIA","MATH",""],["IXA","MATH",""],["","",""],["","",""],["DS","",""]],
    SS3: [["IX","PSC",""],["VIIA","PSC",""],["","",""],["XIC","PHY","TH"],["","",""],["","",""],["","",""],["SS3","",""]],
    HNM: [["VB","BENG",""],["IXB","BENG",""],["","",""],["XD","BENG",""],["XB","BENG",""],["VIIA","BENG",""],["","",""],["HNM","",""]],
    KKD: [["","",""],["VIIIC","LIB",""],["","",""],["XIA","LIB",""],["XIIA","LIB",""],["IXD","LIB",""],["","",""],["KKD","",""]],
    UB:  [["XIA","HIST",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["UB","",""]],
    PG:  [["XIIC","CHEM",""],["XIIC+D","PRAC",""],["","",""],["XIIC+D","PRAC",""],["XC","PSC",""],["","",""],["","",""],["PG","",""]],
    AJ:  [["VIIID","LSC",""],["VIIID","LSC",""],["","",""],["VIIA","LSC",""],["VID","LSC",""],["VIIB","LSC",""],["","",""],["AJ","",""]],
    BD1: [["","",""],["VC","AP",""],["","",""],["VB","BENG",""],["","",""],["","",""],["","",""],["BD1","",""]],
    BM2: [["VC","BENG",""],["IXC","BENG",""],["","",""],["VIIB","BENG",""],["IXD","BENG",""],["VIIIA","BNG",""],["","",""],["BM2","",""]],
    AD2: [["","",""],["VIC","HIST",""],["","",""],["VIIC","GEO",""],["VIID","HIS",""],["","",""],["","",""],["AD2","",""]],
    AC:  [["","",""],["XIC+D","TH",""],["","",""],["","",""],["","",""],["","",""],["","",""],["AC","",""]],
    SS2: [["","",""],["XB","COM","TH"],["","",""],["XA","COMP",""],["XIC+D","GC",""],["","",""],["","",""],["SS2","",""]],
    SG:  [["","",""],["XIIC+D","GC",""],["","",""],["","",""],["","",""],["","",""],["","",""],["SG","",""]],
    TS:  [["","",""],["VB","LIB",""],["","",""],["VIB","LIB",""],["VC","LIB",""],["VIA","LIB",""],["","",""],["TS","",""]],
    PC:  [["","",""],["VIIIA","HIST",""],["","",""],["XIIA","POLS",""],["","",""],["","",""],["","",""],["PC","",""]],
    PKS: [["","",""],["","",""],["VIIA","HINDI",""],["","",""],["","",""],["","",""],["","",""],["PKS","",""]],
    "MR.COMM":[["XIB","BSTD",""],["XIIB","ACCT",""],["","",""],["XIB","BSTD",""],["","",""],["","",""],["","",""],["MR.COMM","",""]],
  },
  Thursday: {
    KCD: [["","",""],["XIID","PHY",""],["","",""],["XD","PSC",""],["","",""],["","",""],["","",""],["KCD","",""]],
    TR:  [["","",""],["VIC","ENG",""],["","",""],["XA","ENG",""],["XIA","ENG",""],["XIIC+D","ENG",""],["","",""],["TR","",""]],
    SS1: [["XIIA","BENG",""],["IXC","BENG",""],["","",""],["XIB","BENG",""],["XIIC+D","ENG",""],["","",""],["","",""],["SS1","",""]],
    SB1: [["VIB","GEO",""],["XA","GEO",""],["","",""],["XIA","GEO",""],["VIIIC","GEO",""],["","",""],["","",""],["SB1","",""]],
    SB2: [["VIIIC","HIST",""],["VID","HIST",""],["","",""],["XC","HIST",""],["VIIC","HIST",""],["","",""],["","",""],["SB2","",""]],
    JGG: [["","",""],["VIB","MATH",""],["","",""],["VC","MATH",""],["","",""],["","",""],["","",""],["JGG","",""]],
    SP1: [["","",""],["VB","ENG",""],["","",""],["VIA","ENG",""],["","",""],["","",""],["","",""],["SP1","",""]],
    AKM: [["","",""],["VIIIC","MATH",""],["","",""],["VIIA","MATH",""],["IXB","PSC",""],["","",""],["","",""],["AKM","",""]],
    BB1: [["","",""],["XC","ENG",""],["","",""],["VIID","ENG",""],["VIIA","ENG",""],["","",""],["","",""],["BB1","",""]],
    SB3: [["","",""],["IXD","MATH",""],["","",""],["VIC","MATH",""],["XA","MATH",""],["","",""],["","",""],["SB3","",""]],
    LBS: [["XD","LSC",""],["VIIIA","LSC",""],["","",""],["VIB","SC",""],["VIID","LSC",""],["IXD","LSC",""],["","",""],["LBS","",""]],
    SP2: [["VA","MATH",""],["VIIID","MATH",""],["","",""],["XC","MATH",""],["","",""],["","",""],["","",""],["SP2","",""]],
    AG1: [["","",""],["XIC","CHE",""],["","",""],["XIID","CHE","TH"],["XA","PSC",""],["","",""],["","",""],["AG1","",""]],
    JM:  [["VIIIA","PSC",""],["VIIC","PSC",""],["","",""],["IXA","PSC",""],["VB","AP",""],["","",""],["","",""],["JM","",""]],
    DC:  [["XIC+D","ENG",""],["VIIIC","ENG",""],["","",""],["VIIID","ENG",""],["IXA","ENG",""],["","",""],["","",""],["DC","",""]],
    AB1: [["VID","ENG",""],["IXD","ENG",""],["","",""],["XIB","ENG",""],["XIIA","ENG",""],["","",""],["","",""],["AB1","",""]],
    SB4: [["IXC","LSC",""],["IXA","LSC",""],["","",""],["XIC+D","ENG",""],["XIC+D","PRAC",""],["","",""],["","",""],["SB4","",""]],
    CRM: [["VIID","MATH",""],["","",""],["VID","MATH",""],["IXC","MATH",""],["","",""],["","",""],["","",""],["CRM","",""]],
    AB2: [["XA","PSC",""],["VB","MATH",""],["","",""],["XIIC","PHY","TH"],["XID","PHY",""],["XIC+D","PRAC",""],["XIC+D","PRAC",""],["AB2","",""]],
    DN:  [["","",""],["XID","CHE",""],["","",""],["XIIC","CHE","TH"],["XIC+D","PRAC",""],["XIC+D","PRAC",""],["","",""],["DN","",""]],
    TA:  [["VIC","ENG",""],["VA","ENG",""],["","",""],["XB","ENG",""],["IXC","ENG",""],["","",""],["","",""],["TA","",""]],
    BB2: [["","",""],["VIA","BENG",""],["","",""],["VIIC","BENG",""],["VIIIC","W.ED",""],["","",""],["","",""],["BB2","",""]],
    AG2: [["XIIC+D","MATH",""],["VD","MATH",""],["","",""],["VIIIA","MATH",""],["VIB","MATH",""],["IXB","MATH",""],["","",""],["AG2","",""]],
    AM:  [["","",""],["VIA","P.ED",""],["","",""],["VIIIA","GEO",""],["VIIB","P.ED",""],["VIIID","PED",""],["","",""],["AM","",""]],
    SB5: [["IXA","HIST",""],["VIB","HIST",""],["","",""],["VC","AP",""],["VIIIA","HIST",""],["IXA","HIST",""],["","",""],["SB5","",""]],
    SRM: [["XIA","HIST",""],["VIA","HIST",""],["","",""],["VIIA","HIST",""],["","",""],["","",""],["","",""],["SRM","",""]],
    SM:  [["","",""],["XIC+D","ENG",""],["","",""],["VIB","ENG",""],["VA","ENG",""],["VIIA","ENG",""],["","",""],["SM","",""]],
    SP3: [["","",""],["XB","GEO",""],["","",""],["VID","GEO",""],["VIIIC","GEO",""],["","",""],["","",""],["SP3","",""]],
    BKM: [["","",""],["XD","MATH",""],["","",""],["VIIC","MATH",""],["XIC+D","MATH",""],["","",""],["","",""],["BKM","",""]],
    MM1: [["","",""],["XIIB","BENG",""],["","",""],["XIIA","B",""],["","",""],["","",""],["","",""],["MM1","",""]],
    BKG: [["","",""],["VIC","W.ED",""],["","",""],["VA","AP",""],["VIC","SC",""],["VIIC","W.ED",""],["","",""],["BKG","",""]],
    SD:  [["VIIID","BENG",""],["XA","BENG",""],["","",""],["XD","BENG",""],["IXB","BENG",""],["XB","BENG",""],["","",""],["SD","",""]],
    SKG: [["XIB","ACCT",""],["VIIA","GEO",""],["","",""],["XIIB","ACCT",""],["XIB","BSTD",""],["","",""],["","",""],["SKG","",""]],
    MM2: [["XC","GEO",""],["VIIID","GEO",""],["","",""],["IXB","GEO",""],["VIIB","GEO",""],["XIIA","GEO",""],["","",""],["MM2","",""]],
    AR:  [["VIIA","GEO",""],["VID","BENG",""],["","",""],["XD","GEO",""],["IXD","GEO",""],["VIC","GEO",""],["","",""],["AR","",""]],
    SSD: [["VIIC","ENG",""],["IXB","ENG",""],["","",""],["VB","ENG",""],["VC","ENG",""],["VIIB","ENG",""],["","",""],["SSD","",""]],
    BD2: [["VC","BENG",""],["XIIA","EDU",""],["","",""],["VIIB","BENG",""],["XIA","EDU",""],["","",""],["","",""],["BD2","",""]],
    NB:  [["IXB","LSC",""],["XIIC+D","TH",""],["","",""],["","",""],["XA","LSC",""],["XB","LSC",""],["","",""],["NB","",""]],
    DS:  [["","",""],["VA","GK",""],["","",""],["XIIC+D","MATH",""],["VIIIA","MATH",""],["","",""],["","",""],["DS","",""]],
    SS3: [["","",""],["XIC","PHY",""],["","",""],["VIIID","PSC",""],["VIIA","PSC",""],["","",""],["","",""],["SS3","",""]],
    HNM: [["VB","BENG",""],["XC","BENG",""],["","",""],["IXA","BENG",""],["VIIIA","BNG",""],["","",""],["","",""],["HNM","",""]],
    KKD: [["","",""],["IXA","LIB",""],["","",""],["XB","LIB",""],["XD","LIB",""],["VIID","LIB",""],["","",""],["KKD","",""]],
    UB:  [["XB","HIST",""],["VIIID","HIST",""],["","",""],["","",""],["IXD","HIST",""],["","",""],["","",""],["UB","",""]],
    PG:  [["VIIB","PSC",""],["","",""],["","",""],["IXC","PSC",""],["XC","PSC",""],["VIIB","PSC",""],["","",""],["PG","",""]],
    AJ:  [["","",""],["VIIB","LSC",""],["","",""],["VIIC","SC",""],["VB","AP",""],["","",""],["","",""],["AJ","",""]],
    BD1: [["","",""],["VIIA","BENG",""],["","",""],["VIIIC","BENG",""],["VIB","BENG",""],["VIID","BENG",""],["","",""],["BD1","",""]],
    BM2: [["","",""],["VIID","BENG",""],["","",""],["IXD","BENG",""],["VA","BENG",""],["","",""],["","",""],["BM2","",""]],
    AD2: [["VIA","GEO",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["AD2","",""]],
    AC:  [["","",""],["XIIC+D","BENG",""],["","",""],["","",""],["","",""],["","",""],["","",""],["AC","",""]],
    SS2: [["XIIB","GC",""],["XIA","GC",""],["","",""],["XC","COMP",""],["","",""],["","",""],["","",""],["SS2","",""]],
    SG:  [["","",""],["XD","COMP",""],["","",""],["XIA","GC",""],["","",""],["","",""],["","",""],["SG","",""]],
    TS:  [["","",""],["VC","COMP",""],["","",""],["VC","COMP","PR"],["VID","LIB",""],["","",""],["","",""],["TS","",""]],
    PC:  [["IXD","HIST",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["PC","",""]],
    PKS: [["","",""],["VIIB","HINDI",""],["","",""],["VIIIC","HINDI",""],["VIIIA","HINDI",""],["VIIC+D","HINDI",""],["","",""],["PKS","",""]],
    "MR.COMM":[["","",""],["XIIB","BSTD",""],["","",""],["XIB","COST",""],["","",""],["","",""],["","",""],["MR.COMM","",""]],
  },
  Friday: {
    KCD: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["KCD","",""]],
    TR:  [["","",""],["XIIC+D","ENG",""],["","",""],["IXA","ENG",""],["","",""],["","",""],["","",""],["TR","",""]],
    SS1: [["","",""],["XIC+D","BENG",""],["","",""],["XA","BENG",""],["IXC","BENG",""],["","",""],["","",""],["SS1","",""]],
    SB1: [["","",""],["IXC","GEO",""],["","",""],["XIIA","GEO",""],["XIA","GEO",""],["XA","GEO",""],["","",""],["SB1","",""]],
    SB2: [["","",""],["VIIC","HIST",""],["","",""],["VIB","HIST",""],["XC","HIST",""],["IXB","HIST",""],["","",""],["SB2","",""]],
    JGG: [["","",""],["XIIA+B","ECON",""],["","",""],["VC","MATH",""],["","",""],["","",""],["","",""],["JGG","",""]],
    SP1: [["","",""],["VIIIC","ENG",""],["","",""],["VIIA","ENG",""],["IXC","ENG",""],["","",""],["","",""],["SP1","",""]],
    AKM: [["","",""],["IXD","MATH",""],["","",""],["VIIIC","MATH",""],["IXB","PSC",""],["","",""],["","",""],["AKM","",""]],
    BB1: [["","",""],["IXB","ENG",""],["","",""],["VIB","ENG",""],["XC","ENG",""],["","",""],["","",""],["BB1","",""]],
    SB3: [["","",""],["VIIB","MATH",""],["","",""],["VIB","MATH",""],["VIIIC","MATH",""],["IXD","MATH",""],["","",""],["SB3","",""]],
    LBS: [["","",""],["VIIIA","LSC",""],["","",""],["XA","LSC",""],["VIID","LSC",""],["","",""],["","",""],["LBS","",""]],
    SP2: [["","",""],["XC","MATH",""],["","",""],["IXC","MATH",""],["VID","MATH",""],["","",""],["","",""],["SP2","",""]],
    AG1: [["","",""],["XIIC+D","PRAC",""],["","",""],["XIIC+D","PRAC",""],["VIIID","PRAC",""],["VIIA","PSC",""],["","",""],["AG1","",""]],
    JM:  [["","",""],["XD","PSC",""],["","",""],["IXA","PSC",""],["VIIC","PSC",""],["","",""],["","",""],["JM","",""]],
    DC:  [["","",""],["XA","ENG",""],["","",""],["VB","ENG",""],["VIA","ENG",""],["","",""],["","",""],["DC","",""]],
    AB1: [["","",""],["XB","ENG",""],["","",""],["VIID","ENG",""],["IXD","ENG",""],["","",""],["","",""],["AB1","",""]],
    SB4: [["","",""],["XIC+D","BIO",""],["","",""],["","",""],["","",""],["","",""],["","",""],["SB4","",""]],
    CRM: [["","",""],["XIC+D","MATH",""],["","",""],["VIIID","MATH",""],["XA","MATH",""],["","",""],["","",""],["CRM","",""]],
    AB2: [["","",""],["XIIC+D","PRAC",""],["","",""],["XIIC+D","PRAC",""],["XIIC","P","TH"],["","",""],["","",""],["AB2","",""]],
    DN:  [["","",""],["IXD","PSC",""],["","",""],["XIC","CHE",""],["XB","PSC",""],["VIIIC","PSC",""],["","",""],["DN","",""]],
    TA:  [["","",""],["VC","ENG",""],["","",""],["VIIIA","ENG",""],["","",""],["","",""],["","",""],["TA","",""]],
    BB2: [["","",""],["VB","WED",""],["","",""],["VA","WED",""],["VA","BENG",""],["VIIC","BENG",""],["","",""],["BB2","",""]],
    AG2: [["","",""],["XD","MATH",""],["","",""],["VIIIA","MATH",""],["VIIA","MATH",""],["VIID","GM",""],["","",""],["AG2","",""]],
    AM:  [["","",""],["VIIB","GEO",""],["","",""],["VIIIA","P.ED",""],["VB","PED",""],["VIIIC","P.ED",""],["","",""],["AM","",""]],
    SB5: [["","",""],["XA","HIST",""],["","",""],["VIB","HIST",""],["VIIB","HIST",""],["","",""],["","",""],["SB5","",""]],
    SRM: [["","",""],["IXC","HIST",""],["","",""],["VIIA","HIST",""],["XD","HIST",""],["VIIID","HIS",""],["","",""],["SRM","",""]],
    SM:  [["","",""],["XD","ENG",""],["","",""],["VIIC","ENG",""],["VA","ENG",""],["","",""],["","",""],["SM","",""]],
    SP3: [["","",""],["IXA","GEO",""],["","",""],["VIIIC","GEO",""],["VIID","GEO",""],["XB","GEO",""],["","",""],["SP3","",""]],
    BKM: [["","",""],["VIC","MATH",""],["","",""],["IXB","MATH",""],["XB","MATH",""],["XD","MATH",""],["VIIC","MATH",""],["BKM","",""]],
    MM1: [["","",""],["XIA","BENG",""],["","",""],["XIB","BENG",""],["XIIB","BENG",""],["XIIC+D","BENG",""],["VIIIC","BENG",""],["MM1","",""]],
    BKG: [["","",""],["VIA","W.ED",""],["","",""],["VIIID","G.SC",""],["VIB","SC",""],["VB","AP",""],["","",""],["BKG","",""]],
    SD:  [["","",""],["XB","BENG",""],["","",""],["XD","BENG",""],["IXA","BENG",""],["","",""],["","",""],["SD","",""]],
    SKG: [["","",""],["VC","AP",""],["","",""],["XIIB","BSTD",""],["XIB","COST",""],["XIIB","COST",""],["","",""],["SKG","",""]],
    MM2: [["","",""],["IXB","GEO",""],["","",""],["VIIID","GEO",""],["VIIB","GEO",""],["","",""],["","",""],["MM2","",""]],
    AR:  [["","",""],["VIC","GEO",""],["","",""],["VID","BENG",""],["VIIIA","GEO",""],["","",""],["","",""],["AR","",""]],
    SSD: [["","",""],["XIB","ENG",""],["","",""],["VIIB","ENG",""],["XIIB","ENG",""],["","",""],["","",""],["SSD","",""]],
    BD2: [["","",""],["VIB","BENG",""],["","",""],["XIA","BENG",""],["VIA","BENG",""],["","",""],["","",""],["BD2","",""]],
    NB:  [["","",""],["XB","LSC",""],["","",""],["","",""],["","",""],["","",""],["","",""],["NB","",""]],
    DS:  [["","",""],["VA","MATH",""],["","",""],["VIA","MATH",""],["IXA","MATH",""],["VC","MATH",""],["","",""],["DS","",""]],
    SS3: [["","",""],["VIIA","PSC",""],["","",""],["XIID","TH-PHY",""],["","",""],["","",""],["","",""],["SS3","",""]],
    HNM: [["","",""],["IXA","BENG",""],["","",""],["XC","BENG",""],["IXB","BENG",""],["VIIA","BNG",""],["","",""],["HNM","",""]],
    KKD: [["","",""],["XC","LIB",""],["","",""],["VIC","LIB",""],["VIIB","LIB",""],["IXC","LIB",""],["","",""],["KKD","",""]],
    UB:  [["","",""],["VIIID","HIST",""],["","",""],["VA","AP",""],["XIIA","HIST",""],["","",""],["","",""],["UB","",""]],
    PG:  [["","",""],["VIID","PSC",""],["","",""],["XID","CHE",""],["","",""],["","",""],["","",""],["PG","",""]],
    AJ:  [["","",""],["VIIC","LSC",""],["","",""],["VID","SC",""],["VIIA","LSC",""],["VIIID","LSC",""],["","",""],["AJ","",""]],
    BD1: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["BD1","",""]],
    BM2: [["","",""],["VIIIA","BENG",""],["","",""],["VIIB","BENG",""],["VIID","BENG",""],["","",""],["","",""],["BM2","",""]],
    AD2: [["","",""],["VIID","HIS",""],["","",""],["VIIC","GEO",""],["","",""],["","",""],["","",""],["AD2","",""]],
    AC:  [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["AC","",""]],
    SS2: [["","",""],["XIIC+D","GC",""],["","",""],["XC","COMP",""],["","",""],["","",""],["","",""],["SS2","",""]],
    SG:  [["","",""],["VB","MATH",""],["","",""],["XIIA","GC",""],["XIIC+D","GC",""],["","",""],["","",""],["SG","",""]],
    TS:  [["","",""],["VID","COMP","TH"],["","",""],["VID","COMP","PRAC"],["VIC","COMP","TH"],["VIC","COMP","TH"],["","",""],["TS","",""]],
    PC:  [["","",""],["XIA","PSC",""],["","",""],["VC","AP",""],["VIIIA","HIST",""],["XIIA","POLS",""],["","",""],["PC","",""]],
    PKS: [["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["","",""],["PKS","",""]],
    "MR.COMM":[["","",""],["XIB","BSTD",""],["","",""],["","",""],["","",""],["","",""],["","",""],["MR.COMM","",""]],
  },
  Saturday: {
    KCD: [["XID","PHY",""],["","",""],["","",""],["","",""]],
    TR:  [["XA","ENG",""],["IXA","ENG",""],["VIIB","ENG",""],["","",""]],
    SS1: [["XIA","BENG",""],["","",""],["","",""],["","",""]],
    SB1: [["IXC","GEO",""],["","",""],["","",""],["","",""]],
    SB2: [["VID","HIS",""],["","",""],["","",""],["","",""]],
    JGG: [["VC","MATH",""],["VIA","MATH",""],["VIC","MATH",""],["","",""]],
    SP1: [["XC","ENG",""],["VIA","ENG",""],["","",""],["","",""]],
    AKM: [["XB","MATH",""],["IXD","MATH",""],["","",""],["","",""]],
    BB1: [["IXB","ENG",""],["VIIIA","ENG",""],["","",""],["","",""]],
    SB3: [["IXA","MATH",""],["XA","MATH",""],["VIIIC","MATH",""],["","",""]],
    LBS: [["XD","LSC",""],["VIC","SC",""],["","",""],["","",""]],
    SP2: [["VIIB","MATH",""],["IXC","MATH",""],["","",""],["","",""]],
    AG1: [["VIIB","MATH",""],["IXB","PSC",""],["","",""],["","",""]],
    JM:  [["VIIIA","PSC",""],["IXA","PSC",""],["","",""],["","",""]],
    DC:  [["XIIB","ENG",""],["VIIIC","ENG",""],["VID","ENG",""],["","",""]],
    AB1: [["VB","ENG",""],["VIIID","ENG",""],["XIIA","ENG",""],["","",""]],
    SB4: [["IXA","LSC",""],["","",""],["","",""],["","",""]],
    CRM: [["VID","MATH",""],["VIIID","MATH",""],["","",""],["","",""]],
    AB2: [["XIC","PHY",""],["XIID","PHY",""],["VB","MATH",""],["","",""]],
    DN:  [["IXD","XIB",""],["XIB","",""],["","",""],["","",""]],
    TA:  [["IXC","BENG",""],["XB","ENG",""],["VIIA","ENG",""],["","",""]],
    BB2: [["VIC","BENG",""],["VA","BENG",""],["","",""],["","",""]],
    AG2: [["VIIA","MATH",""],["XD","MATH",""],["IXB","MATH",""],["","",""]],
    AM:  [["VIB","P.ED",""],["VC","PED",""],["","",""],["","",""]],
    SB5: [["VIB","HIST",""],["VIIB","HIST",""],["","",""],["","",""]],
    SRM: [["VIIIC","HIST",""],["XIIA","HIST",""],["","",""],["","",""]],
    SM:  [["XIA","ENG",""],["VIB","ENG",""],["IXD","ENG",""],["","",""]],
    SP3: [["VIID","GEO",""],["VB","AP",""],["VIA","GEO",""],["","",""]],
    BKM: [["XIC+D","MATH",""],["XII","MATH",""],["","",""],["","",""]],
    MM1: [["IXD","BENG",""],["XII","BENG",""],["XIC+D","BENG",""],["","",""]],
    BKG: [["VIA","SC",""],["VB","AP",""],["","",""],["","",""]],
    SD:  [["VIIID","BNG",""],["XA","BENG",""],["","",""],["","",""]],
    SKG: [["XIB","COST",""],["XIIB","ACCT",""],["","",""],["","",""]],
    MM2: [["XIIA","GEO",""],["XIA","GEO",""],["","",""],["","",""]],
    AR:  [["VIIA","GEO",""],["XD","GEO",""],["","",""],["","",""]],
    SSD: [["VIIC","ENG",""],["VC","ENG",""],["","",""],["","",""]],
    BD2: [["XIIA","BNG",""],["VC","BENG",""],["VIIC","BENG",""],["","",""]],
    NB:  [["XIC+D","TH",""],["","",""],["","",""],["","",""]],
    DS:  [["VIIC","MATH",""],["VIIIA","MATH",""],["XC","MATH",""],["","",""]],
    SS3: [["XC","PSC",""],["XIIC","PHY",""],["","",""],["","",""]],
    HNM: [["XB","BENG",""],["XD","BENG",""],["","",""],["","",""]],
    KKD: [["IXB","BENG",""],["XC","BENG",""],["","",""],["","",""]],
    UB:  [["VIIID","HIST",""],["XIA","HIST",""],["","",""],["","",""]],
    PG:  [["","",""],["","",""],["","",""],["","",""]],
    AJ:  [["VID","SC",""],["VA","PB",""],["","",""],["","",""]],
    BD1: [["VIIIC","BENG",""],["VIIA","BENG",""],["VIB","BENG",""],["","",""]],
    BM2: [["VIIB","BENG",""],["IXC","BENG",""],["VIIIA","BENG",""],["","",""]],
    AD2: [["VIC","HIST",""],["VIIC","GEO",""],["","",""],["","",""]],
    AC:  [["XII C+D","",""],["XIC+D","",""],["XIA+B","",""],["","",""]],
    SS2: [["","",""],["","",""],["","",""],["","",""]],
    SG:  [["","",""],["","",""],["","",""],["","",""]],
    TS:  [["VA","AP",""],["VIID","COM TH",""],["VIID","COM PR",""],["","",""]],
    PC:  [["","",""],["","",""],["","",""],["","",""]],
    PKS: [["","",""],["","",""],["","",""],["","",""]],
    "MR.COMM":[["XIB","ACCT",""],["XIIB","COST",""],["","",""],["","",""]],
  }
};

// Ensure all teachers have 8 periods
DAYS.forEach(day => {
  const maxP = day === 'Saturday' ? 4 : 8;
  TEACHERS.forEach(t => {
    if (!BASE[day][t]) BASE[day][t] = Array(maxP).fill(["","",""]);
    while (BASE[day][t].length < maxP) BASE[day][t].push(["","",""]);
  });
});

// Live editable copy
let live = JSON.parse(JSON.stringify(BASE));
try { const s=localStorage.getItem('nhs_routine'); if(s) live=JSON.parse(s); } catch(e){}
function saveLive(){ try{ localStorage.setItem('nhs_routine',JSON.stringify(live)); }catch(e){} }

// State
let currentDay='Monday', currentView='routine', editingCell=null;
const search = () => document.getElementById('searchBox').value.toLowerCase();
const classFilter = () => document.getElementById('classFilter').value;

// ── Subject color class
function subjClass(subj){
  if(!subj) return '';
  const s=subj.toUpperCase();
  if(s.includes('MATH')||s==='GM') return 'cell-math';
  if(s.includes('ENG')) return 'cell-eng';
  if(s.includes('BENG')||s==='BNG'||s==='BEG') return 'cell-bng';
  if(s.includes('HIST')||s==='HIS') return 'cell-hist';
  if(s.includes('GEO')) return 'cell-geo';
  if(s.includes('PSC')||s.includes('PHY')) return 'cell-psc';
  if(s.includes('CHE')||s.includes('CHEM')) return 'cell-che';
  if(s.includes('LSC')||s.includes('BIO')) return 'cell-bio';
  if(s.includes('SC')&&!s.includes('PSC')) return 'cell-sc';
  if(s.includes('COMP')||s==='GC'||s==='GN') return 'cell-com';
  return 'cell-other';
}

function isChanged(day,teacher,pi){
  const b=BASE[day][teacher]?.[pi]||['','',''];
  const l=live[day][teacher]?.[pi]||['','',''];
  return b[0]!==l[0]||b[1]!==l[1]||b[2]!==l[2];
}

// ── RENDER DAY STRIP ──────────────────────────────────────────
function renderDayStrip(){
  document.getElementById('dayStrip').innerHTML=DAYS.map(d=>
    `<button class="day-btn ${d===currentDay?'active':''}" onclick="setDay('${d}')">${d}</button>`
  ).join('');
}

// ── NAV ──────────────────────────────────────────────────────
function setDay(d){ currentDay=d; renderDayStrip(); renderView(); }
function setView(v){
  currentView=v;
  document.querySelectorAll('.view-tab').forEach((b,i)=>b.classList.toggle('active',['routine','teacher','changes','provisional'][i]===v));
  renderView();
}
function applySearch(){ renderView(); }
function renderView(){
  if(currentView==='routine') renderRoutine();
  else if(currentView==='teacher') renderTeacherView();
  else if(currentView==='changes') renderChanges();
  else renderProvisional();
}

// ── ROUTINE TABLE ──────────────────────────────────────────
function renderRoutine(){
  const sq=search(), cf=classFilter();
  const maxP = currentDay==='Saturday' ? 4 : 8;
  const teachers = TEACHERS.filter(t=>{
    if(sq && !t.toLowerCase().includes(sq)){
      // also check if any cell matches
      const row=live[currentDay][t]||[];
      const match=row.some(([cls,subj])=>
        (cls||'').toLowerCase().includes(sq)||(subj||'').toLowerCase().includes(sq));
      if(!match) return false;
    }
    if(cf){
      const row=live[currentDay][t]||[];
      const match=row.some(([cls])=>(cls||'').replace(/\s/g,'').toUpperCase().startsWith(cf));
      if(!match) return false;
    }
    return true;
  });

  let html=`<div class="table-card">
    <div class="table-card-header">
      <div class="table-card-title">📋 ${currentDay} Routine</div>
      <div style="font-size:12px;color:var(--muted);font-family:'DM Mono',monospace">${teachers.length} teachers shown · Click any cell to edit</div>
    </div>
    <div class="table-wrap"><table>
    <thead><tr>
      <th class="teacher-col">Teacher</th>
      ${Array.from({length:maxP},(_,i)=>`<th>Period ${i+1}</th>`).join('')}
    </tr></thead><tbody>`;

  teachers.forEach(t=>{
    const row=live[currentDay][t]||[];
    html+=`<tr><td class="teacher-cell">${t}</td>`;
    for(let p=0;p<maxP;p++){
      const [cls,subj,note]=row[p]||['','',''];
      const changed=isChanged(currentDay,t,p);
      const sc=subjClass(subj);
      if(!cls&&!subj){
        html+=`<td class="${sc}"><div class="cell-empty" onclick="openEdit('${currentDay}','${t}',${p})">
          <div class="cell-empty-inner"><span class="plus-icon">+</span></div>
        </div></td>`;
      } else {
        html+=`<td class="${sc}${changed?' cell-changed':''}">
          <div class="period-content" onclick="openEdit('${currentDay}','${t}',${p})">
            <div class="cell-class">${cls}</div>
            <div class="cell-subj">${subj}${note?' <small style="color:var(--gold)">'+note+'</small>':''}</div>
            ${changed?`<div style="font-size:9px;color:var(--gold)">✎ edited</div>`:''}
            <div class="cell-edit-hint">click to edit</div>
          </div>
        </td>`;
      }
    }
    html+=`</tr>`;
  });

  html+=`</tbody></table></div></div>`;

  // Legend
  const legendItems=[
    ['#1a5c3a','Science'],['#1a3a6b','Math'],['#6b1a3a','English'],
    ['#6b4e1a','Bengali'],['#4a1a6b','History'],['#1a5a6b','Geography'],
    ['#6b1a1a','Physics/PSC'],['#3a6b1a','Chemistry'],['#1a6b5a','Biology/Life Sc'],
    ['#1a4a6b','Computer'],['#888','Other'],['var(--gold)','Edited']
  ];
  let legendHtml=`<div class="legend">`+legendItems.map(([c,l])=>
    `<div class="legend-item"><div class="legend-dot" style="background:${c}"></div>${l}</div>`
  ).join('')+`</div>`;

  document.getElementById('mainArea').innerHTML=legendHtml+html;
}

// ── TEACHER VIEW ──────────────────────────────────────────────
function renderTeacherView(){
  const sq=search();
  const teachers=TEACHERS.filter(t=>!sq||t.toLowerCase().includes(sq));
  let html=`<div class="teacher-grid">`;
  teachers.forEach(t=>{
    let totalPeriods=0;
    const daySlots=DAYS.map(d=>{
      const row=live[d]?.[t]||[];
      const filled=row.filter(([c])=>c).map(([c,s])=>`${c} ${s}`);
      totalPeriods+=filled.length;
      return {day:d, slots:filled};
    });
    html+=`<div class="teacher-card">
      <div class="teacher-card-head">
        <span class="teacher-code">${t}</span>
        <span class="teacher-periods-count">${totalPeriods} periods/week</span>
      </div>
      <div class="teacher-day-row">
        ${daySlots.map(({day,slots})=>`
          <div class="teacher-day-slot">
            <div class="teacher-day-label">${day.slice(0,3)}</div>
            <div class="teacher-period-list">${slots.length?slots.map(s=>`<div>${s}</div>`).join(''):`<span style="color:var(--rule)">—</span>`}</div>
          </div>`).join('')}
      </div>
    </div>`;
  });
  html+=`</div>`;
  document.getElementById('mainArea').innerHTML=html;
}

// ── CHANGES VIEW ──────────────────────────────────────────────
function renderChanges(){
  let changes=[];
  DAYS.forEach(day=>{
    TEACHERS.forEach(t=>{
      const row=live[day]?.[t]||[];
      row.forEach(([cls,subj,note],pi)=>{
        const b=BASE[day]?.[t]?.[pi]||['','',''];
        if(cls!==b[0]||subj!==b[1]||note!==b[2]){
          changes.push({day,teacher:t,pi,
            base:`${b[0]} ${b[1]} ${b[2]}`.trim()||'(empty)',
            live:`${cls} ${subj} ${note}`.trim()||'(empty)'});
        }
      });
    });
  });

  if(!changes.length){
    document.getElementById('mainArea').innerHTML=`<div class="change-log"><div class="change-log-title">✏️ Edit History</div>
      <p style="color:var(--muted);font-size:14px;padding:20px 0;text-align:center">No changes yet. Click any cell in Routine view to edit.</p></div>`;
    return;
  }

  let html=`<div class="change-log">
    <div class="change-log-title">✏️ Edit History — ${changes.length} change${changes.length>1?'s':''}</div>
    <div style="margin-bottom:12px;display:flex;gap:8px;flex-wrap:wrap">
      <button class="btn btn-red btn-sm" onclick="resetAll()">↩ Reset All Changes</button>
    </div>`;
  changes.forEach(({day,teacher,pi,base,live:lv})=>{
    html+=`<div class="change-item">
      <span class="change-tag">${day} · ${teacher} · P${pi+1}</span>
      <div style="flex:1">
        <span class="change-old">${base}</span>
        <span class="change-arrow"> → </span>
        <span class="change-new">${lv}</span>
      </div>
      <button class="btn btn-ghost btn-sm" onclick="revertOne('${day}','${teacher}',${pi})">↩</button>
    </div>`;
  });
  html+=`</div>`;
  document.getElementById('mainArea').innerHTML=html;
}

// ── EDIT MODAL ────────────────────────────────────────────────
function openEdit(day,teacher,pi){
  editingCell={day,teacher,pi};
  const [cls,subj,note]=live[day][teacher]?.[pi]||['','',''];
  const [bc,bs,bn]=BASE[day][teacher]?.[pi]||['','',''];
  const changed=cls!==bc||subj!==bs||note!==bn;
  document.getElementById('editCtx').innerHTML=
    `<strong>${day}</strong> · Teacher: <strong>${teacher}</strong> · Period <strong>${pi+1}</strong>
     ${changed?` <span style="color:var(--gold);font-size:10px">✎ modified</span>`:''}`;
  document.getElementById('editBaseRef').innerHTML=
    `Original: <span style="color:var(--accent)">${bc||'—'} ${bs||''} ${bn||''}</span>`;
  document.getElementById('editClass').value=cls||'';
  document.getElementById('editSubject').value=subj||'';
  document.getElementById('editNote').value=note||'';
  document.getElementById('editOverlay').classList.add('open');
  setTimeout(()=>document.getElementById('editClass').focus(),80);
}

function saveEdit(){
  if(!editingCell) return;
  const {day,teacher,pi}=editingCell;
  live[day][teacher][pi]=[
    document.getElementById('editClass').value.trim(),
    document.getElementById('editSubject').value.trim(),
    document.getElementById('editNote').value.trim()
  ];
  saveLive(); closeModal(); renderView();
}

function clearCell(){
  if(!editingCell) return;
  const {day,teacher,pi}=editingCell;
  live[day][teacher][pi]=['','',''];
  saveLive(); closeModal(); renderView();
}

function revertCell(){
  if(!editingCell) return;
  const {day,teacher,pi}=editingCell;
  live[day][teacher][pi]=[...(BASE[day][teacher]?.[pi]||['','',''])];
  saveLive(); closeModal(); renderView();
}

function revertOne(day,teacher,pi){
  live[day][teacher][pi]=[...(BASE[day][teacher]?.[pi]||['','',''])];
  saveLive(); renderView();
}

function closeModal(){
  document.getElementById('editOverlay').classList.remove('open');
  editingCell=null;
}

function resetAll(){
  if(!confirm('Reset ALL changes to original routine?')) return;
  live=JSON.parse(JSON.stringify(BASE));
  saveLive(); renderView();
}

// close on overlay click
document.getElementById('editOverlay').addEventListener('click',e=>{
  if(e.target===document.getElementById('editOverlay')) closeModal();
});

// keyboard
document.addEventListener('keydown',e=>{
  if(e.key==='Escape') closeModal();
  if(e.key==='Enter'&&editingCell&&document.getElementById('editOverlay').classList.contains('open')) saveEdit();
});


// ── PROVISIONAL STATE ─────────────────────────────────────────
let absentTeachers = new Set();
let provisionalAssign = {}; // key: "day_teacher_pi" → substitute teacher code
try {
  const sa = localStorage.getItem('nhs_absent');
  if(sa){ const p=JSON.parse(sa); if(p.day===new Date().toLocaleDateString('en',{weekday:'long'})){p.absent.forEach(t=>absentTeachers.add(t));} }
} catch(e){}
try { const sp=localStorage.getItem('nhs_provisional'); if(sp) provisionalAssign=JSON.parse(sp); } catch(e){}
function saveProvisional(){ try{ localStorage.setItem('nhs_provisional',JSON.stringify(provisionalAssign)); }catch(e){} }

function toggleAbsent(t){
  if(absentTeachers.has(t)) absentTeachers.delete(t); else absentTeachers.add(t);
  // clear stale assignments for this teacher
  Object.keys(provisionalAssign).forEach(k=>{ if(k.includes('_'+t+'_')) delete provisionalAssign[k]; });
  saveProvisional();
  renderProvisional();
}

function getFreeTeachers(day, periodIdx){
  // Teachers already assigned to another provisional slot in this same period
  const alreadyAssignedThisPeriod = new Set(
    Object.entries(provisionalAssign)
      .filter(([k,v]) => v && v !== 'PENDING' && k.startsWith(day + '_') && +k.split('_')[2] === periodIdx)
      .map(([,v]) => v)
  );

  return TEACHERS.filter(t => {
    if(absentTeachers.has(t)) return false;
    // Already assigned elsewhere in this period → block
    if(alreadyAssignedThisPeriod.has(t)) return false;
    // Has a regular class this period → block
    const cell = live[day]?.[t]?.[periodIdx] || ['','',''];
    if(cell[0]) return false;
    return true;
  });
}

function setProvisional(key, val){
  if(val) provisionalAssign[key]=val; else delete provisionalAssign[key];
  saveProvisional();
  renderProvisional();
}

function renderProvisional(){
  const maxP = currentDay==='Saturday' ? 4 : 8;

  // Banner
  let html = `<div class="prov-banner">
    <div>
      <div class="prov-banner-title">🔄 Provisional Class Management</div>
      <div class="prov-banner-sub">${currentDay} · ${absentTeachers.size} teacher(s) absent · Click name to mark absent</div>
    </div>
    <button class="btn" style="background:rgba(255,255,255,0.15);color:white;border:1px solid rgba(255,255,255,0.3)" onclick="absentTeachers.clear();provisionalAssign={};saveProvisional();renderProvisional()">↩ Clear All</button>
  </div>`;

  // Absent teacher chips
  html += `<div style="background:white;border-radius:10px;box-shadow:var(--shadow);padding:16px 20px;margin-bottom:16px;">
    <div style="font-size:11px;font-family:'DM Mono',monospace;text-transform:uppercase;letter-spacing:1px;color:var(--muted);margin-bottom:10px;">Mark Absent Teachers</div>
    <div class="absent-chips">`;
  TEACHERS.forEach(t=>{
    const isAbs = absentTeachers.has(t);
    // only show teachers who have class today
    const hasClass = (live[currentDay]?.[t]||[]).some(([c])=>c);
    if(!hasClass) return;
    html += `<div class="absent-chip ${isAbs?'marked':''}" onclick="toggleAbsent('${t}')">
      <span class="chip-dot"></span>${t}
    </div>`;
  });
  html += `</div></div>`;

  if(absentTeachers.size === 0){
    html += `<div class="prov-empty"><span class="emoji">👆</span>Mark absent teachers above to generate provisional assignments.</div>`;
    document.getElementById('mainArea').innerHTML = html;
    return;
  }

  // Build: for each absent teacher, for each period they have a class → need a substitute
  // Group by period for notice sheet
  const periodMap = {}; // periodIdx → [{absentT, cls, subj, note}]
  absentTeachers.forEach(t=>{
    const row = live[currentDay]?.[t] || [];
    row.forEach(([cls,subj,note], pi)=>{
      if(!cls) return;
      if(!periodMap[pi]) periodMap[pi]=[];
      periodMap[pi].push({absentT:t, cls, subj, note, pi});
    });
  });

  if(Object.keys(periodMap).length===0){
    html += `<div class="prov-empty"><span class="emoji">✅</span>Absent teachers have no classes today.</div>`;
    document.getElementById('mainArea').innerHTML=html; return;
  }

  // Provisional assignment cards — one per absent teacher
  html += `<div class="prov-card">
    <div class="prov-card-head">
      <h3>📋 Assign Substitutes</h3>
      <span style="font-size:11px;opacity:0.8;font-family:'DM Mono',monospace">Free teachers suggested automatically</span>
    </div>`;

  Object.keys(periodMap).sort((a,b)=>+a-+b).forEach(pi=>{
    const items = periodMap[pi];
    const freeT = getFreeTeachers(currentDay, +pi);
    html += `<div class="prov-period-row"><div class="prov-pnum">P${+pi+1}</div><div class="prov-items">`;
    items.forEach(({absentT,cls,subj,note})=>{
      const key = `${currentDay}_${absentT}_${pi}`;
      const assigned = provisionalAssign[key]||'';
      html += `<div class="prov-item">
        <span class="tag-absent">${absentT}</span>
        <span class="tag-class">${cls}</span>
        <span class="tag-subj">${subj}${note?' '+note:''}</span>
        <span class="prov-arrow">→</span>
        <select class="prov-sel ${assigned?'assigned':''}" onchange="setProvisional('${key}',this.value)">
          <option value="">— assign substitute —</option>
          ${freeT.length===0 ? '<option disabled>⚠ No free teachers this period</option>' : ''}
          ${freeT.map(t=>`<option value="${t}" ${t===assigned?'selected':''}>${t}</option>`).join('')}
          ${assigned && assigned!=='PENDING' && !freeT.find(t=>t===assigned) ? `<option value="${assigned}" selected>${assigned} (current)</option>` : ''}
          <option value="PENDING" ${assigned==='PENDING'?'selected':''}>⚠ PENDING</option>
        </select>
        ${assigned && assigned!=='PENDING' ? `<span style="font-size:11px;color:#1b5e20;font-family:'DM Mono',monospace">✓ ${assigned}</span>` : ''}
        ${(()=>{
          // Check if this same teacher is assigned to another slot in a DIFFERENT period
          const conflicts = Object.entries(provisionalAssign)
            .filter(([k,v]) => v===assigned && v && v!=='PENDING' && k!==key && k.startsWith(currentDay+'_'));
          if(conflicts.length){
            const conflictPeriods = conflicts.map(([k])=> 'P'+(+k.split('_')[2]+1)).join(', ');
            return `<span style="font-size:10px;background:#fff3e0;color:#e65100;border:1px solid #ffb74d;border-radius:4px;padding:1px 6px;font-family:'DM Mono',monospace;">⚠ also at ${conflictPeriods}</span>`;
          }
          return '';
        })()}
      </div>`;
    });
    html += `</div></div>`;
  });
  html += `</div>`;

  // Notice sheet
  const assignedItems = Object.entries(provisionalAssign).filter(([k,v])=>v&&v!=='PENDING'&&k.startsWith(currentDay+'_'));
  if(assignedItems.length){
    html += `<div class="notice-card">
      <div class="notice-card-title">📢 Provisional Notice — ${currentDay}</div>`;
    assignedItems.sort((a,b)=>{
      const pa=+a[0].split('_')[2], pb=+b[0].split('_')[2]; return pa-pb;
    }).forEach(([key,sub])=>{
      const parts=key.split('_'); // day_teacher_pi
      const abT=parts[1], pi=+parts[2];
      const [cls,subj,note]=live[currentDay]?.[abT]?.[pi]||['','',''];
      html+=`<div class="notice-row">
        <span class="ntag-period">P${pi+1}</span>
        <span class="ntag-class">${cls}</span>
        <span class="ntag-class">${subj}${note?' '+note:''}</span>
        <span class="ntag-absent">${abT}</span>
        <span style="color:var(--muted);font-size:12px">→</span>
        <span class="ntag-sub">${sub}</span>
      </div>`;
    });
    html+=`</div>`;
  }

  document.getElementById('mainArea').innerHTML=html;
}

// ── INIT ──────────────────────────────────────────────────────
renderDayStrip();
renderView();
</script>
</body>
</html>
