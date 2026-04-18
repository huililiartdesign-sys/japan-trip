<!DOCTYPE html>

<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>日本17天旅遊行程</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --ink:#1a1410;--cream:#f0ebe0;--soft:#e8e0d0;
  --accent:#c0392b;--gold:#c9a84c;--muted:#8a7e72;
  --green:#3d7a5c;--blue:#2c5f8a;--metro:#e65c00;
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent;}
body{background:var(--cream);font-family:'Noto Sans TC',sans-serif;color:var(--ink);min-height:100vh;max-width:430px;margin:0 auto;padding-bottom:72px;}
.panel{display:none;}.panel.active{display:block;}

/* ── Header ── */
.hdr{background:var(–ink);padding:16px 18px 0;position:sticky;top:0;z-index:100;}
.hdr-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;}
.hdr-title{font-size:20px;font-weight:700;color:var(–gold);}
.hdr-badge{background:var(–accent);color:white;font-size:10px;padding:4px 10px;border-radius:20px;font-weight:700;}
.hdr-sub{font-size:10px;color:var(–muted);letter-spacing:2px;text-transform:uppercase;margin-top:1px;}

/* ── Tab Bar ── */
.tabs{position:fixed;bottom:0;left:50%;transform:translateX(-50%);width:100%;max-width:430px;background:var(–ink);display:flex;border-top:1px solid rgba(255,255,255,.08);z-index:100;}
.tab{flex:1;background:none;border:none;color:var(–muted);font-family:‘Noto Sans TC’,sans-serif;font-size:11px;padding:10px 4px;cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:3px;position:relative;}
.tab .ic{font-size:18px;}
.tab.active{color:var(–gold);}
.tab.active::after{content:’’;position:absolute;top:0;left:25%;right:25%;height:2px;background:var(–gold);border-radius:0 0 2px 2px;}

/* ── Day Chips ── */
.chips-wrap{padding:12px 16px 0;overflow-x:auto;white-space:nowrap;scrollbar-width:none;}
.chips-wrap::-webkit-scrollbar{display:none;}
.chips-lbl{font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(–muted);margin-bottom:6px;display:block;}
.chips{display:inline-flex;gap:6px;padding-bottom:10px;}
.chip{display:inline-flex;flex-direction:column;align-items:center;background:white;border:1.5px solid var(–soft);border-radius:12px;padding:5px 9px;cursor:pointer;min-width:48px;}
.chip.active{background:var(–ink);border-color:var(–ink);color:white;}
.chip.active .cn{color:var(–gold);}
.chip.has{border-color:var(–gold);}
.cl{font-size:8px;color:var(–muted);letter-spacing:1px;}
.chip.active .cl{color:rgba(255,255,255,.5);}
.cn{font-size:14px;font-weight:700;}
.cdot{width:4px;height:4px;border-radius:50%;background:var(–gold);margin-top:2px;}
.chip.active .cdot{background:var(–accent);}

/* ── Day Content ── */
.day-wrap{padding:14px 14px 20px;}
.day-hdr{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:14px;padding-bottom:12px;border-bottom:1px solid var(–soft);}
.dn{font-family:‘DM Mono’,monospace;font-size:10px;color:var(–accent);letter-spacing:2px;text-transform:uppercase;}
.dt{font-size:17px;font-weight:700;margin-top:2px;}
.dd{font-size:11px;color:var(–muted);margin-top:2px;}
.tl{font-size:9px;color:var(–muted);text-align:right;}
.ta{font-family:‘DM Mono’,monospace;font-size:15px;font-weight:500;color:var(–green);}

/* ── Timeline ── */
.tline{display:flex;flex-direction:column;}
.irow{display:flex;align-items:stretch;}
.tcol{width:50px;flex-shrink:0;display:flex;flex-direction:column;align-items:center;padding-top:12px;}
.tbub{font-family:‘DM Mono’,monospace;font-size:11px;font-weight:500;color:var(–blue);background:rgba(44,95,138,.1);border-radius:8px;padding:3px 4px;text-align:center;line-height:1.2;white-space:nowrap;min-width:42px;}
.tbub.mt{color:var(–metro);background:rgba(230,92,0,.1);}
.tl-line{flex:1;width:2px;background:var(–soft);margin:4px 0;border-radius:1px;}
.bcol{flex:1;padding:10px 0 10px 6px;}

/* ── Item Card ── */
.icard{background:white;border-radius:14px;overflow:hidden;box-shadow:0 2px 10px rgba(26,20,16,.06);border:1px solid rgba(201,168,76,.15);margin-bottom:10px;}
.icard.em{border-color:var(–gold);box-shadow:0 0 0 2px rgba(201,168,76,.2);}
.ic-in{padding:11px 12px;}
.itop{display:flex;justify-content:space-between;align-items:center;margin-bottom:5px;}
.itag{font-size:10px;padding:2px 7px;border-radius:20px;font-weight:500;}
.tag-transport{background:#e8f0f8;color:var(–blue);}
.tag-food{background:#fef3e0;color:#c17d00;}
.tag-sight{background:#e8f5ee;color:var(–green);}
.tag-stay{background:#f5e8f5;color:#7b3fa0;}
.tag-shop{background:#fde8e8;color:var(–accent);}
.tag-festival{background:#fff3e0;color:#e65c00;}
.icost{font-family:‘DM Mono’,monospace;font-size:12px;color:var(–green);font-weight:500;}
.iname-row{display:flex;align-items:center;gap:5px;}
.iname{font-size:14px;font-weight:600;}
.mapbtn{background:none;border:none;cursor:pointer;font-size:13px;padding:0 1px;opacity:.6;}
.inote{font-size:11px;color:var(–muted);margin-top:4px;line-height:1.5;}
.snotes{display:flex;flex-direction:column;gap:3px;margin-top:6px;}
.snote{font-size:11px;background:var(–cream);border-radius:6px;padding:3px 8px;display:flex;gap:5px;align-items:flex-start;}
.snb{color:var(–gold);font-size:8px;margin-top:3px;flex-shrink:0;}
.ebtns{display:none;gap:6px;padding:0 10px 9px;}
.icard.em .ebtns{display:flex;}
.ebtn{flex:1;background:var(–cream);border:none;border-radius:8px;padding:6px;font-size:11px;cursor:pointer;color:var(–ink);font-family:‘Noto Sans TC’,sans-serif;}
.dbtn{background:none;border:1px solid #f0d0d0;border-radius:8px;padding:6px 10px;font-size:11px;cursor:pointer;color:var(–accent);}

/* ── Metro Card ── */
.mcard{background:linear-gradient(135deg,#1a1410,#2c1a0e);border-radius:14px;overflow:hidden;margin-bottom:10px;box-shadow:0 2px 10px rgba(26,20,16,.12);}
.mcard.em{box-shadow:0 0 0 2px rgba(201,168,76,.4);}
.mhdr{padding:9px 12px 7px;display:flex;align-items:center;gap:7px;border-bottom:1px solid rgba(255,255,255,.08);}
.mico{font-size:16px;}
.mtitle{font-size:13px;font-weight:600;color:white;}
.mfare{font-family:‘DM Mono’,monospace;font-size:11px;color:var(–gold);margin-left:auto;}
.mlines{padding:7px 12px 9px;display:flex;flex-direction:column;gap:5px;}
.mline{display:flex;align-items:center;gap:6px;}
.mlbadge{font-size:10px;font-weight:700;padding:2px 7px;border-radius:10px;font-family:‘DM Mono’,monospace;white-space:nowrap;flex-shrink:0;}
.mldesc{font-size:11px;color:rgba(255,255,255,.65);}
.mlfare{font-family:‘DM Mono’,monospace;font-size:11px;color:var(–gold);margin-left:auto;flex-shrink:0;}
.mnote{font-size:10px;color:rgba(255,255,255,.4);padding:0 12px 7px;}
.mebtns{display:none;gap:6px;padding:0 12px 9px;}
.mcard.em .mebtns{display:flex;}
.mebtn{flex:1;background:rgba(255,255,255,.08);border:none;border-radius:8px;padding:6px;font-size:11px;cursor:pointer;color:rgba(255,255,255,.8);font-family:‘Noto Sans TC’,sans-serif;}
.mebtn.d{color:#e57373;background:rgba(229,115,115,.12);}

/* ── Add Buttons ── */
.add-btn{display:flex;align-items:center;justify-content:center;gap:6px;width:100%;background:none;border:1.5px dashed var(–soft);border-radius:12px;padding:12px;color:var(–muted);font-size:13px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;margin-top:4px;}
.add-metro-btn{display:flex;align-items:center;justify-content:center;gap:6px;width:100%;background:none;border:1.5px dashed rgba(230,92,0,.3);border-radius:12px;padding:12px;color:var(–metro);font-size:13px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;margin-top:6px;}
.empty{text-align:center;padding:40px 20px;color:var(–muted);}
.empty .ei{font-size:36px;margin-bottom:10px;}
.empty p{font-size:13px;line-height:1.8;}

/* ── FAB ── */
.fabs{position:fixed;bottom:82px;right:18px;display:flex;flex-direction:column-reverse;align-items:flex-end;gap:10px;z-index:200;}
.fab{width:50px;height:50px;border-radius:50%;border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 16px rgba(0,0,0,.25);font-size:20px;}
.fab:active{transform:scale(.92);}
.fab-add{background:var(–accent);color:white;}
.fab-edit{background:var(–ink);color:var(–gold);font-size:17px;}
.fab-edit.on{background:var(–gold);color:var(–ink);}

/* ── Overview ── */
.ov-wrap{padding:14px;}
.ov-grid{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:16px;}
.ov-card{background:white;border-radius:13px;padding:12px;box-shadow:0 2px 8px rgba(26,20,16,.06);}
.ov-lbl{font-size:9px;color:var(–muted);letter-spacing:1.5px;text-transform:uppercase;}
.ov-val{font-size:22px;font-weight:700;margin-top:3px;font-family:‘DM Mono’,monospace;}
.ov-sub{font-size:10px;color:var(–muted);margin-top:2px;}
.sec-lbl{font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(–muted);margin-bottom:9px;}
.region-list{display:flex;flex-direction:column;gap:8px;}
.region-item{background:white;border-radius:12px;padding:11px 13px;display:flex;justify-content:space-between;align-items:center;box-shadow:0 2px 6px rgba(26,20,16,.05);border-left:4px solid var(–gold);}
.ri-name{font-size:14px;font-weight:600;}
.ri-days{font-size:11px;color:var(–muted);margin-top:2px;}
.ri-tag{font-size:11px;color:var(–muted);}

/* ── QR / Ticket Panel ── */
.qr-wrap{padding:14px 14px 20px;}
.qr-edit-bar{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;}
.qr-edit-btn{background:var(–ink);color:var(–gold);border:none;border-radius:20px;padding:6px 16px;font-size:12px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;font-weight:600;}
.qr-edit-btn.on{background:var(–gold);color:var(–ink);}
.ticket-list{display:flex;flex-direction:column;gap:12px;}

/* Ticket Card */
.ticket{background:white;border-radius:16px;overflow:hidden;box-shadow:0 2px 12px rgba(26,20,16,.08);}
.ticket.em{box-shadow:0 0 0 2px var(–gold);}
.ticket-top{padding:14px 14px 10px;}
.ticket-name{font-size:15px;font-weight:700;}
.ticket-desc{font-size:12px;color:var(–muted);margin-top:3px;line-height:1.5;}
.ticket-date{font-size:11px;color:var(–blue);margin-top:5px;font-family:‘DM Mono’,monospace;}
.ticket-type{font-size:10px;padding:2px 8px;border-radius:20px;font-weight:600;display:inline-block;margin-top:5px;}
.type-ticket{background:#e8f5ee;color:var(–green);}
.type-coupon{background:#fff3e0;color:#c17d00;}
.type-pass{background:#e8f0f8;color:var(–blue);}

/* QR / Image area - full width, tall */
.ticket-img-area{margin:0;position:relative;}
.ticket-img-filled{width:100%;aspect-ratio:1/1;max-height:320px;object-fit:contain;background:#f8f8f8;display:block;cursor:pointer;}
.ticket-img-filled:active{opacity:.85;}
.ticket-upload-area{width:100%;height:200px;background:var(–cream);border-top:1px dashed var(–soft);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px;cursor:pointer;position:relative;}
.ticket-upload-area input[type=file]{position:absolute;inset:0;opacity:0;cursor:pointer;width:100%;height:100%;}
.upload-ico{font-size:36px;}
.upload-txt{font-size:12px;color:var(–muted);text-align:center;line-height:1.7;}
.img-action-bar{display:flex;border-top:1px solid var(–soft);}
.img-action-btn{flex:1;background:none;border:none;padding:10px;font-size:12px;color:var(–muted);cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;display:flex;align-items:center;justify-content:center;gap:4px;}
.img-action-btn:not(:last-child){border-right:1px solid var(–soft);}

/* Ticket edit buttons */
.ticket-ebtns{display:none;gap:6px;padding:10px 14px 12px;}
.ticket.em .ticket-ebtns{display:flex;}
.t-ebtn{flex:1;background:var(–cream);border:none;border-radius:8px;padding:7px;font-size:12px;cursor:pointer;color:var(–ink);font-family:‘Noto Sans TC’,sans-serif;}
.t-dbtn{background:none;border:1px solid #f0d0d0;border-radius:8px;padding:7px 12px;font-size:12px;cursor:pointer;color:var(–accent);}

/* Add ticket btn */
.add-ticket-btn{display:flex;align-items:center;justify-content:center;gap:7px;width:100%;background:none;border:1.5px dashed var(–soft);border-radius:14px;padding:14px;color:var(–muted);font-size:13px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;margin-top:4px;}
.add-ticket-btn:active{border-color:var(–gold);color:var(–gold);}

/* Fullscreen image viewer */
.img-viewer{position:fixed;inset:0;background:rgba(0,0,0,.95);z-index:500;display:none;align-items:center;justify-content:center;flex-direction:column;}
.img-viewer.open{display:flex;}
.img-viewer img{max-width:100%;max-height:85vh;object-fit:contain;border-radius:4px;}
.img-viewer-close{position:absolute;top:20px;right:20px;background:rgba(255,255,255,.15);border:none;color:white;width:36px;height:36px;border-radius:50%;font-size:18px;cursor:pointer;display:flex;align-items:center;justify-content:center;}
.img-viewer-name{color:rgba(255,255,255,.7);font-size:13px;margin-top:14px;text-align:center;padding:0 20px;}

/* ── Modals ── */
.overlay{position:fixed;inset:0;background:rgba(26,20,16,.55);z-index:300;display:none;align-items:flex-end;justify-content:center;}
.overlay.open{display:flex;}
.sheet{background:white;border-radius:24px 24px 0 0;width:100%;max-width:430px;max-height:92vh;overflow-y:auto;position:relative;}
.sheet-handle{width:36px;height:4px;background:var(–soft);border-radius:2px;margin:14px auto 0;}
.sheet-inner{padding:14px 18px 36px;}
.sheet-title{font-size:16px;font-weight:700;margin-bottom:14px;}
.sheet-close{position:absolute;top:14px;right:16px;background:var(–cream);border:none;width:28px;height:28px;border-radius:50%;font-size:13px;cursor:pointer;color:var(–muted);}
.map-frame{width:100%;height:300px;border-radius:12px;border:none;margin-top:6px;background:var(–cream);}

/* Form */
.form{display:flex;flex-direction:column;gap:11px;}
.fg{display:flex;flex-direction:column;gap:4px;}
.fl{font-size:10px;color:var(–muted);letter-spacing:1.5px;text-transform:uppercase;}
.fi,.fta{background:var(–cream);border:1.5px solid var(–soft);border-radius:10px;padding:9px 11px;font-size:14px;font-family:‘Noto Sans TC’,sans-serif;color:var(–ink);width:100%;outline:none;}
.fi:focus,.fta:focus{border-color:var(–gold);}
.fta{resize:vertical;min-height:60px;}
.frow{display:flex;gap:9px;}.frow .fg{flex:1;}
.btn-save{background:var(–ink);color:var(–gold);border:none;border-radius:12px;padding:13px;font-size:14px;font-weight:700;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;}
.btn-del{background:none;color:var(–accent);border:1.5px solid var(–accent);border-radius:12px;padding:11px;font-size:13px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;}
.tag-row{display:flex;flex-wrap:wrap;gap:5px;}
.topt{padding:4px 11px;border-radius:20px;border:1.5px solid var(–soft);font-size:12px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;background:white;}
.topt.sel{background:var(–ink);color:white;border-color:var(–ink);}
.sne{display:flex;flex-direction:column;gap:5px;}
.snrow{display:flex;gap:5px;align-items:center;}.snrow .fi{flex:1;}
.rmsn{background:none;border:1px solid var(–soft);border-radius:8px;padding:7px 9px;font-size:12px;cursor:pointer;color:var(–muted);flex-shrink:0;}
.addsn{background:none;border:1.5px dashed var(–soft);border-radius:8px;padding:7px;font-size:12px;color:var(–muted);cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;width:100%;}
.mle{display:flex;flex-direction:column;gap:8px;}
.mlrow{background:var(–cream);border-radius:10px;padding:9px;display:flex;flex-direction:column;gap:5px;}
.mlrt{display:flex;gap:5px;}
.rmml{background:none;border:1px solid var(–soft);border-radius:8px;padding:6px 9px;font-size:12px;cursor:pointer;color:var(–accent);flex-shrink:0;}
.addml{background:none;border:1.5px dashed var(–soft);border-radius:8px;padding:8px;font-size:12px;color:var(–muted);cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;width:100%;}
.cps{display:flex;gap:5px;flex-wrap:wrap;margin-top:3px;}
.cp{width:22px;height:22px;border-radius:5px;cursor:pointer;border:2.5px solid transparent;}
.cp.sel{border-color:var(–ink);}

/* Ticket type selector */
.type-row{display:flex;gap:6px;}
.typeopt{flex:1;padding:8px 4px;border-radius:10px;border:1.5px solid var(–soft);font-size:12px;cursor:pointer;font-family:‘Noto Sans TC’,sans-serif;background:white;text-align:center;}
.typeopt.sel{background:var(–ink);color:white;border-color:var(–ink);}
</style>

</head>
<body>

<div class="hdr">
  <div class="hdr-top">
    <div>
      <div class="hdr-title">🇯🇵 日本之旅</div>
      <div class="hdr-sub">2025 · 17 DAYS</div>
    </div>
    <div class="hdr-badge">5/12 → 5/28</div>
  </div>
</div>

<div class="tabs">
  <button class="tab active" onclick="switchTab('it')" id="tab-it"><span class="ic">📅</span>行程</button>
  <button class="tab" onclick="switchTab('ov')" id="tab-ov"><span class="ic">📊</span>總覽</button>
  <button class="tab" onclick="switchTab('qr')" id="tab-qr"><span class="ic">🎫</span>票券</button>
</div>

<!-- ITINERARY -->

<div id="panel-it" class="panel active">
  <div class="chips-wrap">
    <span class="chips-lbl">選擇日期</span>
    <div class="chips" id="chips"></div>
  </div>
  <div class="day-wrap" id="dayWrap"></div>
</div>

<!-- OVERVIEW -->

<div id="panel-ov" class="panel">
  <div class="ov-wrap">
    <div class="ov-grid">
      <div class="ov-card"><div class="ov-lbl">總天數</div><div class="ov-val" style="color:var(--blue)">17</div><div class="ov-sub">5/12 – 5/28</div></div>
      <div class="ov-card"><div class="ov-lbl">預計花費</div><div class="ov-val" style="color:var(--green)" id="ovBudget">¥0</div><div class="ov-sub">行程合計</div></div>
      <div class="ov-card"><div class="ov-lbl">已規劃景點</div><div class="ov-val" style="color:var(--accent)" id="ovSpots">0</div><div class="ov-sub">個項目</div></div>
      <div class="ov-card"><div class="ov-lbl">住宿城市</div><div class="ov-val" style="color:var(--gold)">4</div><div class="ov-sub">東京/金澤/京都/大阪</div></div>
    </div>
    <div class="sec-lbl">地區行程</div>
    <div class="region-list">
      <div class="region-item" style="border-color:#e74c3c"><div><div class="ri-name">🗼 東京</div><div class="ri-days">第1–5天 · 5/12–5/16</div></div><div class="ri-tag">東京都</div></div>
      <div class="region-item" style="border-color:#3498db"><div><div class="ri-name">🏔️ 金澤</div><div class="ri-days">第6–8天 · 5/17–5/19</div></div><div class="ri-tag">石川縣</div></div>
      <div class="region-item" style="border-color:#9b59b6"><div><div class="ri-name">⛩️ 京都</div><div class="ri-days">第9–15天 · 5/20–5/26</div></div><div class="ri-tag">京都府</div></div>
      <div class="region-item" style="border-color:#f39c12"><div><div class="ri-name">🦀 大阪</div><div class="ri-days">第16–17天 · 5/26–5/28</div></div><div class="ri-tag">大阪府</div></div>
    </div>
  </div>
</div>

<!-- QR / TICKET -->

<div id="panel-qr" class="panel">
  <div class="qr-wrap">
    <div class="qr-edit-bar">
      <div class="sec-lbl" style="margin:0">票券 &amp; 折價券</div>
      <button class="qr-edit-btn" id="qrEditBtn" onclick="toggleQREdit()">✏️ 編輯</button>
    </div>
    <div class="ticket-list" id="ticketList"></div>
    <button class="add-ticket-btn" onclick="openAddTicket()">＋ 新增票券 / 折價券</button>
  </div>
</div>

<!-- FABs (itinerary only) -->

<div class="fabs" id="fabs">
  <button class="fab fab-add" onclick="openAddItem()">＋</button>
  <button class="fab fab-edit" id="fabEdit" onclick="toggleEdit()">✏️</button>
</div>

<!-- Fullscreen Image Viewer -->

<div class="img-viewer" id="imgViewer" onclick="closeViewer()">
  <button class="img-viewer-close" onclick="closeViewer()">✕</button>
  <img id="viewerImg" src="" alt="">
  <div class="img-viewer-name" id="viewerName"></div>
</div>

<!-- Map Modal -->

<div class="overlay" id="mapOv" onclick="ocl(event,'mapOv',closeMap)">
  <div class="sheet">
    <div class="sheet-handle"></div>
    <div class="sheet-inner">
      <button class="sheet-close" onclick="closeMap()">✕</button>
      <div class="sheet-title" id="mapTitle">地圖</div>
      <iframe id="mapFrame" class="map-frame" loading="lazy" allowfullscreen referrerpolicy="no-referrer-when-downgrade" src="about:blank"></iframe>
    </div>
  </div>
</div>

<!-- Item Edit Modal -->

<div class="overlay" id="itemOv" onclick="ocl(event,'itemOv',closeItem)">
  <div class="sheet">
    <div class="sheet-handle"></div>
    <div class="sheet-inner">
      <button class="sheet-close" onclick="closeItem()">✕</button>
      <div class="sheet-title" id="itemTitle">新增行程</div>
      <div class="form" id="itemForm"></div>
    </div>
  </div>
</div>

<!-- Metro Modal -->

<div class="overlay" id="metroOv" onclick="ocl(event,'metroOv',closeMetro)">
  <div class="sheet">
    <div class="sheet-handle"></div>
    <div class="sheet-inner">
      <button class="sheet-close" onclick="closeMetro()">✕</button>
      <div class="sheet-title" id="metroTitle">交通路線</div>
      <div class="form" id="metroForm"></div>
    </div>
  </div>
</div>

<!-- Ticket Modal -->

<div class="overlay" id="ticketOv" onclick="ocl(event,'ticketOv',closeTicket)">
  <div class="sheet">
    <div class="sheet-handle"></div>
    <div class="sheet-inner">
      <button class="sheet-close" onclick="closeTicket()">✕</button>
      <div class="sheet-title" id="ticketTitle">新增票券</div>
      <div class="form" id="ticketForm"></div>
    </div>
  </div>
</div>

<script>
var curDay = 1;
var editMode = false;
var qrEditMode = false;
var editItemKey = null;
var editMetroKey = null;
var editTicketId = null;

var MC = ['#e74c3c','#e67e22','#f39c12','#2ecc71','#16a085','#3498db','#2980b9','#9b59b6','#e91e63','#607d8b'];
var TN = {transport:'交通',food:'美食',sight:'景點',stay:'住宿',shop:'購物',festival:'祭典'};

// ── Data (empty) ──
var data = {days:{}};
for (var i = 1; i <= 17; i++) {
  data.days[String(i)] = {title:'第' + i + '天', subtitle:'', transit:[], items:[]};
}

var tickets = [];

// ── Chips ──
function renderChips() {
  var w = document.getElementById('chips');
  var h = '';
  for (var i = 1; i <= 17; i++) {
    var d = data.days[String(i)];
    var has = (d.items && d.items.length > 0) || (d.transit && d.transit.length > 0);
    h += '<div class="chip' + (i === curDay ? ' active' : '') + (has ? ' has' : '') + '" onclick="selDay(' + i + ')">';
    h += '<span class="cl">DAY</span><span class="cn">' + i + '</span>';
    if (has) h += '<div class="cdot"></div>';
    h += '</div>';
  }
  w.innerHTML = h;
}

function selDay(n) {
  curDay = n;
  renderChips();
  renderDay();
  setTimeout(function() {
    var c = document.querySelectorAll('.chip');
    if (c[n-1]) c[n-1].scrollIntoView({behavior:'smooth', block:'nearest', inline:'center'});
  }, 50);
}

// ── Day Content ──
function renderDay() {
  var w = document.getElementById('dayWrap');
  var d = data.days[String(curDay)];
  var cost = 0;
  (d.items || []).forEach(function(it) { cost += (it.cost || 0); });
  (d.transit || []).forEach(function(tr) { (tr.lines || []).forEach(function(l) { cost += (parseInt(l.fare) || 0); }); });

  var h = '<div class="day-hdr">';
  h += '<div><div class="dn">DAY ' + curDay + '</div>';
  h += '<div class="dt">' + d.title + '</div>';
  h += '<div class="dd">2025年5月' + (11 + curDay) + '日' + (d.subtitle ? ' · ' + d.subtitle : '') + '</div></div>';
  h += '<div><div class="tl">預算合計</div><div class="ta">¥' + cost.toLocaleString() + '</div></div></div>';
  h += '<div class="tline">' + buildItems(d) + '</div>';
  h += '<button class="add-btn" onclick="openAddItem()">＋ 新增行程項目</button>';
  h += '<button class="add-metro-btn" onclick="openAddMetro()">🚇 新增交通路線</button>';
  w.innerHTML = h;
}

function buildItems(d) {
  var all = [];
  (d.transit || []).forEach(function(t) { all.push({type:'m', data:t, st:t.time||'00:00'}); });
  (d.items || []).forEach(function(it) { all.push({type:'i', data:it, st:it.time||'00:00'}); });
  all.sort(function(a,b) { return a.st < b.st ? -1 : 1; });
  if (!all.length) return '<div class="empty"><div class="ei">✏️</div><p>這天還沒有行程<br>點底部 ＋ 新增！</p></div>';
  var h = '';
  for (var i = 0; i < all.length; i++) {
    var last = (i === all.length - 1);
    h += all[i].type === 'm' ? buildMetro(all[i].data, last) : buildItem(all[i].data, last);
  }
  return h;
}

function buildItem(it, last) {
  var sn = it.subnotes || [];
  var snH = '';
  if (sn.length) {
    snH = '<div class="snotes">';
    for (var i = 0; i < sn.length; i++) snH += '<div class="snote"><span class="snb">&#9670;</span>' + sn[i] + '</div>';
    snH += '</div>';
  }
  var mb = it.location ? '<button class="mapbtn" onclick="openMap(\'' + ej(it.location) + '\',\'' + ej(it.name) + '\')">📍</button>' : '';
  var eb = editMode ? '<div class="ebtns"><button class="ebtn" onclick="openEditItem(' + curDay + ',' + it.id + ')">✏️ 編輯</button><button class="dbtn" onclick="delItem(' + curDay + ',' + it.id + ')">🗑</button></div>' : '';
  var h = '<div class="irow"><div class="tcol">';
  h += it.time ? '<div class="tbub">' + it.time + '</div>' : '<div style="height:20px"></div>';
  if (!last) h += '<div class="tl-line"></div>';
  h += '</div><div class="bcol"><div class="icard' + (editMode ? ' em' : '') + '">';
  h += '<div class="ic-in"><div class="itop">';
  h += it.tag ? '<span class="itag tag-' + it.tag + '">' + (TN[it.tag]||it.tag) + '</span>' : '<span></span>';
  h += it.cost > 0 ? '<span class="icost">¥' + it.cost.toLocaleString() + '</span>' : '<span></span>';
  h += '</div><div class="iname-row"><span class="iname">' + it.name + '</span>' + mb + '</div>';
  if (it.note) h += '<div class="inote">' + it.note + '</div>';
  h += snH + '</div>' + eb + '</div></div></div>';
  return h;
}

function buildMetro(m, last) {
  var tf = 0;
  (m.lines||[]).forEach(function(l) { tf += (parseInt(l.fare)||0); });
  var lH = '';
  (m.lines||[]).forEach(function(l) {
    lH += '<div class="mline"><span class="mlbadge" style="background:' + (l.color||'#333') + ';color:white">' + l.badge + '</span>';
    lH += '<span class="mldesc">' + (l.desc||'') + '</span>';
    if (parseInt(l.fare) > 0) lH += '<span class="mlfare">¥' + parseInt(l.fare).toLocaleString() + '</span>';
    lH += '</div>';
  });
  var eb = editMode ? '<div class="mebtns"><button class="mebtn" onclick="openEditMetro(' + curDay + ',\'' + m.id + '\')">✏️ 編輯</button><button class="mebtn d" onclick="delMetro(' + curDay + ',\'' + m.id + '\')">🗑 刪除</button></div>' : '';
  var h = '<div class="irow"><div class="tcol">';
  h += m.time ? '<div class="tbub mt">' + m.time + '</div>' : '<div style="height:20px"></div>';
  if (!last) h += '<div class="tl-line" style="background:rgba(230,92,0,.2)"></div>';
  h += '</div><div class="bcol"><div class="mcard' + (editMode ? ' em' : '') + '">';
  h += '<div class="mhdr"><span class="mico">🚇</span><span class="mtitle">' + m.title + '</span>';
  if (tf > 0) h += '<span class="mfare">¥' + tf.toLocaleString() + '</span>';
  h += '</div><div class="mlines">' + lH + '</div>';
  if (m.note) h += '<div class="mnote">' + m.note + '</div>';
  h += eb + '</div></div></div>';
  return h;
}

function ej(s) { return (s||'').replace(/\\/g,'\\\\').replace(/'/g,"\\'").replace(/"/g,'\\"'); }

// ── Edit Mode ──
function toggleEdit() {
  editMode = !editMode;
  var f = document.getElementById('fabEdit');
  if (editMode) { f.classList.add('on'); f.textContent = '✅'; }
  else { f.classList.remove('on'); f.textContent = '✏️'; }
  renderDay();
}

// ── QR Edit Mode ──
function toggleQREdit() {
  qrEditMode = !qrEditMode;
  var b = document.getElementById('qrEditBtn');
  if (qrEditMode) { b.classList.add('on'); b.textContent = '✅ 完成'; }
  else { b.classList.remove('on'); b.textContent = '✏️ 編輯'; }
  renderTickets();
}

// ── Map ──
function openMap(loc, name) {
  document.getElementById('mapTitle').textContent = '📍 ' + name;
  document.getElementById('mapFrame').src = 'https://maps.google.com/maps?q=' + encodeURIComponent(loc + ' Japan') + '&output=embed&hl=zh-TW&zoom=15';
  document.getElementById('mapOv').classList.add('open');
}
function closeMap() {
  document.getElementById('mapOv').classList.remove('open');
  setTimeout(function() { document.getElementById('mapFrame').src = 'about:blank'; }, 400);
}

// ── Item Forms ──
function openAddItem() { editItemKey = null; buildItemForm('新增行程', {time:'',name:'',note:'',cost:0,tag:'sight',location:'',subnotes:[]}); }
function openEditItem(day, id) {
  var items = data.days[String(day)].items;
  var it = null;
  for (var i = 0; i < items.length; i++) { if (items[i].id === id) { it = items[i]; break; } }
  if (!it) return;
  editItemKey = {day:day, id:id};
  buildItemForm('編輯行程', it);
}
function buildItemForm(title, it) {
  document.getElementById('itemTitle').textContent = title;
  var tags = ['transport','food','sight','stay','shop','festival'];
  var tn = {transport:'🚆 交通',food:'🍜 美食',sight:'🗼 景點',stay:'🏨 住宿',shop:'🛍 購物',festival:'🎉 祭典'};
  var sn = it.subnotes || [];
  var snH = '';
  for (var i = 0; i < sn.length; i++) snH += '<div class="snrow" id="snr-' + i + '"><input class="fi" value="' + sn[i].replace(/"/g,'&quot;') + '"><button type="button" class="rmsn" onclick="rmSN(' + i + ')">✕</button></div>';
  var tH = '';
  for (var j = 0; j < tags.length; j++) tH += '<button type="button" class="topt' + (it.tag === tags[j] ? ' sel' : '') + '" data-tag="' + tags[j] + '" onclick="selT(this)">' + tn[tags[j]] + '</button>';
  var h = '<div class="frow"><div class="fg"><label class="fl">時間</label><input class="fi" id="fi-time" placeholder="10:00" value="' + (it.time||'') + '"></div>';
  h += '<div class="fg"><label class="fl">費用 (円)</label><input class="fi" id="fi-cost" type="number" value="' + (it.cost||0) + '"></div></div>';
  h += '<div class="fg"><label class="fl">名稱</label><input class="fi" id="fi-name" value="' + (it.name||'').replace(/"/g,'&quot;') + '"></div>';
  h += '<div class="fg"><label class="fl">備注</label><textarea class="fta" id="fi-note">' + (it.note||'') + '</textarea></div>';

h += ‘<div class="fg"><label class="fl">地點（地圖用）</label><input class=“fi” id=“fi-loc” placeholder=“例：浅草寺 東京都” value=”’ + (it.location||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">類型</label><div class="tag-row">’ + tH + ‘</div></div>’;
h += ‘<div class="fg"><label class="fl">小備注</label><div class="sne" id="snEd">’ + snH + ‘</div><button type="button" class="addsn" onclick="addSN()">＋ 新增小備注</button></div>’;
h += ‘<button class="btn-save" onclick="saveItem()">💾 儲存</button>’;
if (editItemKey) h += ‘<button class="btn-del" onclick="delItemCur()">🗑 刪除</button>’;
document.getElementById(‘itemForm’).innerHTML = h;
document.getElementById(‘itemOv’).classList.add(‘open’);
}
function addSN() {
var ed = document.getElementById(‘snEd’);
var i = ed.querySelectorAll(’.snrow’).length;
ed.insertAdjacentHTML(‘beforeend’, ‘<div class="snrow" id="snr-' + i + '"><input class="fi" placeholder="備注內容"><button type="button" class="rmsn" onclick="rmSN(' + i + ')">✕</button></div>’);
}
function rmSN(i) { var r = document.getElementById(‘snr-’+i); if(r) r.remove(); }
function selT(btn) { document.querySelectorAll(’.topt’).forEach(function(b){b.classList.remove(‘sel’);}); btn.classList.add(‘sel’); }
function saveItem() {
var name = document.getElementById(‘fi-name’).value.trim();
if (!name) { alert(‘請輸入名稱’); return; }
var time = document.getElementById(‘fi-time’).value.trim();
var note = document.getElementById(‘fi-note’).value.trim();
var cost = parseInt(document.getElementById(‘fi-cost’).value) || 0;
var loc = document.getElementById(‘fi-loc’).value.trim();
var te = document.querySelector(’.topt.sel’);
var tag = te ? te.getAttribute(‘data-tag’) : ‘sight’;
var sns = [];
document.querySelectorAll(’#snEd input’).forEach(function(inp) { var v = inp.value.trim(); if(v) sns.push(v); });
var dk = String(editItemKey ? editItemKey.day : curDay);
if (editItemKey) {
var arr = data.days[dk].items;
for (var i = 0; i < arr.length; i++) {
if (arr[i].id === editItemKey.id) { arr[i].time=time;arr[i].name=name;arr[i].note=note;arr[i].cost=cost;arr[i].location=loc;arr[i].tag=tag;arr[i].subnotes=sns; break; }
}
} else {
data.days[dk].items.push({id:Date.now(),time:time,name:name,note:note,cost:cost,location:loc,tag:tag,subnotes:sns});
}
closeItem(); saveData(); renderChips(); renderDay(); updateOv();
}
function delItem(day, id) {
if (!confirm(‘確定刪除？’)) return;
var dk = String(day);
data.days[dk].items = data.days[dk].items.filter(function(i){return i.id!==id;});
saveData(); renderChips(); renderDay(); updateOv();
}
function delItemCur() {
if (!editItemKey || !confirm(‘確定刪除？’)) return;
delItem(editItemKey.day, editItemKey.id);
closeItem();
}
function closeItem() { document.getElementById(‘itemOv’).classList.remove(‘open’); editItemKey = null; }

// ── Metro Forms ──
function openAddMetro() { editMetroKey = null; buildMetroForm(‘新增交通路線’, {title:’’,time:’’,note:’’,lines:[{badge:’’,color:’#e74c3c’,desc:’’,fare:’’}]}); }
function openEditMetro(day, mid) {
var tr = data.days[String(day)].transit;
var m = null;
for (var i = 0; i < tr.length; i++) { if (tr[i].id === mid) { m = tr[i]; break; } }
if (!m) return;
editMetroKey = {day:day, id:mid};
buildMetroForm(‘編輯交通路線’, m);
}
function buildMetroForm(title, m) {
document.getElementById(‘metroTitle’).textContent = title;
var ls = m.lines || [{badge:’’,color:’#e74c3c’,desc:’’,fare:’’}];
var lH = ‘’;
for (var i = 0; i < ls.length; i++) lH += mlHTML(ls[i], i);
var h = ‘<div class="frow"><div class="fg" style="flex:2"><label class="fl">路線標題</label><input class=“fi” id=“mf-title” placeholder=“例：南千住 到 上野” value=”’ + (m.title||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">時間</label><input class="fi" id="mf-time" placeholder="09:00" value="' + (m.time||'') + '"></div></div>’;
h += ‘<div class="fg"><label class="fl">備注</label><input class=“fi” id=“mf-note” value=”’ + (m.note||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">路線明細</label><div class="mle" id="mlEd">’ + lH + ‘</div><button type="button" class="addml" onclick="addML()">＋ 新增換乘路線</button></div>’;
h += ‘<button class="btn-save" onclick="saveMetro()">💾 儲存</button>’;
if (editMetroKey) h += ‘<button class="btn-del" onclick="delMetroCur()">🗑 刪除</button>’;
document.getElementById(‘metroForm’).innerHTML = h;
document.getElementById(‘metroOv’).classList.add(‘open’);
}
function mlHTML(l, i) {
var ps = ‘’;
for (var ci = 0; ci < MC.length; ci++) ps += ‘<div class="cp' + (l.color===MC[ci]?' sel':'') + '" style="background:' + MC[ci] + '" data-color="' + MC[ci] + '" onclick="selMC(' + i + ',this)"></div>’;
return ‘<div class="mlrow" id="mlr-' + i + '"><div class="mlrt"><input class=“fi” style=“flex:1” id=“mlb-’ + i + ‘” placeholder=“線名” value=”’ + (l.badge||’’).replace(/”/g,’"’) + ‘”><input class="fi" style="width:65px" id="mlf-' + i + '" type="number" placeholder="円" value="' + (l.fare||'') + '"><button type="button" class="rmml" onclick="rmML(' + i + ')">✕</button></div><input class=“fi” id=“mld-’ + i + ‘” placeholder=“說明” value=”’ + (l.desc||’’).replace(/”/g,’"’) + ‘”><div class="cps" id="mlc-' + i + '">’ + ps + ‘</div></div>’;
}
function addML() {
var ed = document.getElementById(‘mlEd’);
var i = ed.querySelectorAll(’.mlrow’).length;
ed.insertAdjacentHTML(‘beforeend’, mlHTML({badge:’’,color:MC[i%MC.length],desc:’’,fare:’’}, i));
}
function rmML(i) { var r = document.getElementById(‘mlr-’+i); if(r) r.remove(); }
function selMC(i, el) { document.getElementById(‘mlc-’+i).querySelectorAll(’.cp’).forEach(function(p){p.classList.remove(‘sel’);}); el.classList.add(‘sel’); }
function getMLs() {
var rows = document.querySelectorAll(’#mlEd .mlrow’);
var res = [];
for (var i = 0; i < rows.length; i++) {
var ri = rows[i].id.replace(‘mlr-’,’’);
var sc = rows[i].querySelector(’.cp.sel’);
var b = document.getElementById(‘mlb-’+ri);
if (!b || !b.value.trim()) continue;
res.push({badge:b.value.trim(), desc:(document.getElementById(‘mld-’+ri)||{}).value||’’, fare:(document.getElementById(‘mlf-’+ri)||{}).value||’’, color:sc?sc.getAttribute(‘data-color’):’#333’});
}
return res;
}
function saveMetro() {
var title = document.getElementById(‘mf-title’).value.trim();
if (!title) { alert(‘請輸入路線標題’); return; }
var time = document.getElementById(‘mf-time’).value.trim();
var note = document.getElementById(‘mf-note’).value.trim();
var lines = getMLs();
var dk = String(editMetroKey ? editMetroKey.day : curDay);
if (!data.days[dk].transit) data.days[dk].transit = [];
if (editMetroKey) {
var tr = data.days[dk].transit;
for (var i = 0; i < tr.length; i++) { if (tr[i].id === editMetroKey.id) { tr[i].title=title;tr[i].time=time;tr[i].note=note;tr[i].lines=lines; break; } }
} else {
data.days[dk].transit.push({id:‘t’+Date.now(),title:title,time:time,note:note,lines:lines});
}
closeMetro(); saveData(); renderChips(); renderDay(); updateOv();
}
function delMetro(day, mid) {
if (!confirm(‘確定刪除？’)) return;
var dk = String(day);
data.days[dk].transit = data.days[dk].transit.filter(function(t){return t.id!==mid;});
saveData(); renderChips(); renderDay(); updateOv();
}
function delMetroCur() {
if (!editMetroKey || !confirm(‘確定刪除？’)) return;
delMetro(editMetroKey.day, editMetroKey.id);
closeMetro();
}
function closeMetro() { document.getElementById(‘metroOv’).classList.remove(‘open’); editMetroKey = null; }

// ── Tickets ──
function renderTickets() {
var w = document.getElementById(‘ticketList’);
if (!tickets.length) {
w.innerHTML = ‘<div class="empty"><div class="ei">🎫</div><p>還沒有票券<br>點底部＋新增！</p></div>’;
return;
}
var h = ‘’;
for (var i = 0; i < tickets.length; i++) {
var t = tickets[i];
var typeLabel = t.type === ‘coupon’ ? ‘折價券’ : t.type === ‘pass’ ? ‘通票/Pass’ : ‘門票’;
var typeCls = ‘type-’ + (t.type||‘ticket’);
h += ‘<div class="ticket' + (qrEditMode ? ' em' : '') + '" id="tk-' + t.id + '">’;

```
// Info section
h += '<div class="ticket-top">';
h += '<div class="ticket-name">' + t.name + '</div>';
if (t.desc) h += '<div class="ticket-desc">' + t.desc + '</div>';
if (t.date) h += '<div class="ticket-date">' + t.date + '</div>';
h += '<span class="ticket-type ' + typeCls + '">' + typeLabel + '</span>';
h += '</div>';

// Image area
h += '<div class="ticket-img-area">';
if (t.img) {
  // Large image - tap to zoom
  h += '<img class="ticket-img-filled" src="' + t.img + '" alt="' + t.name + '" onclick="openViewer(\'' + ej(t.img) + '\',\'' + ej(t.name) + '\')">';
  // Action bar below image
  h += '<div class="img-action-bar">';
  h += '<button class="img-action-btn" onclick="openViewer(\'' + ej(t.img) + '\',\'' + ej(t.name) + '\')">🔍 放大查看</button>';
  h += '<label class="img-action-btn" style="cursor:pointer">📷 更換圖片<input type="file" accept="image/*" style="display:none" onchange="uploadTicketImg(' + t.id + ',this)"></label>';
  h += '</div>';
} else {
  // Upload placeholder
  h += '<div class="ticket-upload-area">';
  h += '<div class="upload-ico">📷</div>';
  h += '<div class="upload-txt">點此上傳 QR Code<br>條碼 / 票券截圖</div>';
  h += '<input type="file" accept="image/*" onchange="uploadTicketImg(' + t.id + ',this)">';
  h += '</div>';
}
h += '</div>';

// Edit buttons (only in edit mode)
h += '<div class="ticket-ebtns"><button class="t-ebtn" onclick="openEditTicket(' + t.id + ')">✏️ 編輯資訊</button><button class="t-dbtn" onclick="delTicket(' + t.id + ')">🗑 刪除</button></div>';
h += '</div>';
```

}
w.innerHTML = h;
}

function uploadTicketImg(id, input) {
var f = input.files[0]; if (!f) return;
var r = new FileReader();
r.onload = function(e) {
for (var i = 0; i < tickets.length; i++) { if (tickets[i].id === id) { tickets[i].img = e.target.result; break; } }
saveData(); renderTickets();
};
r.readAsDataURL(f);
}

function openAddTicket() { editTicketId = null; buildTicketForm(‘新增票券’, {name:’’,desc:’’,date:’’,type:‘ticket’}); }
function openEditTicket(id) {
var t = null;
for (var i = 0; i < tickets.length; i++) { if (tickets[i].id === id) { t = tickets[i]; break; } }
if (!t) return;
editTicketId = id;
buildTicketForm(‘編輯票券’, t);
}
function buildTicketForm(title, t) {
document.getElementById(‘ticketTitle’).textContent = title;
var types = [‘ticket’,‘coupon’,‘pass’];
var tnames = {ticket:‘🎟 門票’,coupon:‘🏷 折價券’,pass:‘🎫 通票/Pass’};
var tH = ‘’;
for (var i = 0; i < types.length; i++) tH += ‘<button type="button" class="typeopt' + ((t.type||'ticket')===types[i]?' sel':'') + '" data-type="' + types[i] + '" onclick="selType(this)">’ + tnames[types[i]] + ‘</button>’;
var h = ‘<div class="fg"><label class="fl">票券名稱</label><input class=“fi” id=“tf-name” placeholder=“例：日光東照宮門票” value=”’ + (t.name||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">說明</label><input class=“fi” id=“tf-desc” placeholder=“例：成人票 1300円” value=”’ + (t.desc||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">使用日</label><input class=“fi” id=“tf-date” placeholder=“例：Day 3 · 5/14” value=”’ + (t.date||’’).replace(/”/g,’"’) + ‘”></div>’;
h += ‘<div class="fg"><label class="fl">類型</label><div class="type-row">’ + tH + ‘</div></div>’;
h += ‘<button class="btn-save" onclick="saveTicket()">💾 儲存</button>’;
if (editTicketId) h += ‘<button class="btn-del" onclick="delTicketCur()">🗑 刪除</button>’;
document.getElementById(‘ticketForm’).innerHTML = h;
document.getElementById(‘ticketOv’).classList.add(‘open’);
}
function selType(btn) { document.querySelectorAll(’.typeopt’).forEach(function(b){b.classList.remove(‘sel’);}); btn.classList.add(‘sel’); }
function saveTicket() {
var name = document.getElementById(‘tf-name’).value.trim();
if (!name) { alert(‘請輸入票券名稱’); return; }
var desc = document.getElementById(‘tf-desc’).value.trim();
var date = document.getElementById(‘tf-date’).value.trim();
var te = document.querySelector(’.typeopt.sel’);
var type = te ? te.getAttribute(‘data-type’) : ‘ticket’;
if (editTicketId) {
for (var i = 0; i < tickets.length; i++) { if (tickets[i].id === editTicketId) { tickets[i].name=name;tickets[i].desc=desc;tickets[i].date=date;tickets[i].type=type; break; } }
} else {
tickets.push({id:Date.now(),name:name,desc:desc,date:date,type:type,img:null});
}
closeTicket(); saveData(); renderTickets();
}
function delTicket(id) {
if (!confirm(‘確定刪除？’)) return;
tickets = tickets.filter(function(t){return t.id!==id;});
saveData(); renderTickets();
}
function delTicketCur() {
if (!editTicketId || !confirm(‘確定刪除？’)) return;
var id = editTicketId;
tickets = tickets.filter(function(t){return t.id!==id;});
closeTicket(); saveData(); renderTickets();
}
function closeTicket() { document.getElementById(‘ticketOv’).classList.remove(‘open’); editTicketId = null; }

// ── Tab ──
function switchTab(tab) {
[‘it’,‘ov’,‘qr’].forEach(function(t) {
document.getElementById(‘panel-’+t).classList.toggle(‘active’, t===tab);
document.getElementById(‘tab-’+t).classList.toggle(‘active’, t===tab);
});
document.getElementById(‘fabs’).style.display = tab === ‘it’ ? ‘flex’ : ‘none’;
}

// ── Overview ──
function updateOv() {
var total = 0, spots = 0;
Object.keys(data.days).forEach(function(k) {
var d = data.days[k];
(d.items||[]).forEach(function(it){total+=(it.cost||0);spots++;});
(d.transit||[]).forEach(function(tr){(tr.lines||[]).forEach(function(l){total+=(parseInt(l.fare)||0);});});
});
var e1 = document.getElementById(‘ovBudget’); if(e1) e1.textContent = ‘¥’+total.toLocaleString();
var e2 = document.getElementById(‘ovSpots’); if(e2) e2.textContent = spots;
}

function ocl(e, id, fn) { if (e.target === document.getElementById(id)) fn(); }

// ── Image Viewer ──
function openViewer(src, name) {
document.getElementById(‘viewerImg’).src = src;
document.getElementById(‘viewerName’).textContent = name;
document.getElementById(‘imgViewer’).classList.add(‘open’);
}
function closeViewer() {
document.getElementById(‘imgViewer’).classList.remove(‘open’);
}

// ── LocalStorage 儲存 ──
function saveData() {
try {
localStorage.setItem(‘japan_trip_data’, JSON.stringify(data));
localStorage.setItem(‘japan_trip_tickets’, JSON.stringify(tickets));
} catch(e) {}
}
function loadData() {
try {
var d = localStorage.getItem(‘japan_trip_data’);
var t = localStorage.getItem(‘japan_trip_tickets’);
if (d) data = JSON.parse(d);
if (t) tickets = JSON.parse(t);
} catch(e) {}
}

// ── Init ──
loadData();
renderChips();
renderDay();
renderTickets();
updateOv();
setTimeout(function() {
var c = document.querySelectorAll(’.chip’);
if (c[0]) c[0].scrollIntoView({inline:‘start’});
}, 100);
</script>

</body>
</html>
