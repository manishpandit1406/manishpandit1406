<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Manish Pandit — AI/ML Engineer</title>
<link rel="icon" type="image/png" href="https://github.com/manishpandit1406.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,500&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0E1420;
    --ink-soft:#161F30;
    --ink-line:#2A3448;
    --paper:#F5F1E6;
    --paper-dim:#EAE3D0;
    --paper-line:#D9D0B8;
    --signal:#FF7A3D;
    --signal-dim:#C75E2C;
    --teal:#2E6B63;
    --muted-on-ink:#8A93AA;
    --muted-on-paper:#75705F;
    --text-on-ink:#F3F0E6;
    --text-on-paper:#161310;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--paper);
    color:var(--text-on-paper);
    font-family:'Inter',sans-serif;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  ::selection{background:var(--signal); color:var(--ink);}
  a{color:inherit; text-decoration:none;}
  .mono{font-family:'JetBrains Mono',monospace;}
  .display{font-family:'Fraunces',serif;}
  .wrap{max-width:1120px; margin:0 auto; padding:0 32px;}

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important; scroll-behavior:auto !important;}
  }

  /* ---------- NAV ---------- */
  nav{
    position:fixed; top:0; left:0; right:0; z-index:100;
    display:flex; align-items:center; justify-content:space-between;
    padding:20px 40px;
    color: #F3F0E6; /* default over dark hero */
    transition: background 0.3s ease, padding 0.3s ease, color 0.3s ease, border-bottom 0.3s ease;
  }
  nav.scrolled {
    background: rgba(245, 241, 230, 0.85); /* paper color semi-transparent */
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    color: var(--text-on-paper); /* dark text over light background */
    padding: 16px 40px;
    border-bottom: 1px solid var(--paper-line);
  }
  .nav-mark{
    font-family:'JetBrains Mono',monospace;
    font-size:14px; font-weight:600; color:inherit;
    letter-spacing:0.01em;
    display:flex; align-items:center; gap:10px;
  }
  .nav-mark img{width:26px; height:26px; border-radius:50%; object-fit:cover; border:1px solid rgba(255,122,61,0.5);}
  .nav-links{display:flex; gap:28px; font-family:'JetBrains Mono',monospace; font-size:12.5px; color:inherit;}
  .nav-links a{opacity:0.75; transition:opacity 0.2s ease;}
  .nav-links a:hover{opacity:1;}
  @media (max-width:720px){ .nav-links{display:none;} }

  /* ---------- HERO ---------- */
  .hero{
    background:var(--ink);
    color:var(--text-on-ink);
    min-height:100svh;
    display:flex; flex-direction:column; justify-content:center;
    position:relative;
    padding:140px 0 80px;
    overflow:hidden;
  }
  .hero-net{position:absolute; inset:0; opacity:0.35; pointer-events:none;}
  .hero-inner{
    position:relative; z-index:2;
    display:flex; justify-content:space-between; align-items:center; gap:40px; flex-wrap:wrap;
  }
  .hero-content{ flex:1; min-width:320px; }
  .hero-photo{
    width: clamp(200px, 25vw, 360px);
    aspect-ratio: 1;
    border-radius: 50%;
    border: 2px solid var(--ink-line);
    background: var(--ink-soft);
    display: flex; align-items: center; justify-content: center;
    overflow: hidden;
    position: relative;
    box-shadow: 0 20px 40px rgba(0,0,0,0.4);
    opacity: 0; transform: translateY(16px);
  }
  .hero-photo img{ width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s ease; }
  .hero-photo:hover img{ transform: scale(1.05); }
  @media (max-width:860px){
    .hero-inner{ flex-direction: column-reverse; align-items: flex-start; }
    .hero-photo{ width: 140px; margin-bottom: 20px; }
  }
  .terminal{
    font-family:'JetBrains Mono',monospace;
    font-size:13.5px;
    color:var(--muted-on-ink);
    background:var(--ink-soft);
    border:1px solid var(--ink-line);
    border-radius:8px;
    padding:16px 20px;
    max-width:560px;
    margin-bottom:36px;
    min-height:96px;
    box-shadow: 0 0 30px rgba(255, 122, 61, 0.04);
    transition: box-shadow 0.4s ease, border-color 0.4s ease;
  }
  .terminal:hover{
    box-shadow: 0 0 50px rgba(255, 122, 61, 0.12);
    border-color: var(--signal-dim);
  }
  .terminal .tline{display:block; margin-bottom:6px; white-space:pre-wrap;}
  .terminal .tprompt{color:var(--signal);}
  .terminal .cursor{display:inline-block; width:7px; height:15px; background:var(--signal); vertical-align:middle; margin-left:2px; animation:blink 1s step-end infinite;}
  @keyframes blink{50%{opacity:0;}}

  .hero h1{
    font-family:'Fraunces',serif;
    font-weight:600;
    font-size:clamp(44px, 8vw, 92px);
    line-height:0.98;
    letter-spacing:-0.01em;
    opacity:0; transform:translateY(16px);
  }
  .hero h1 .accent{font-style:italic; font-weight:500; color:var(--signal);}
  .hero .role{
    font-family:'JetBrains Mono',monospace;
    font-size:15px;
    color:var(--muted-on-ink);
    margin-top:22px;
    max-width:560px;
    line-height:1.6;
    opacity:0; transform:translateY(12px);
  }
  .hero .role b{color:var(--text-on-ink); font-weight:600;}
  .hero-meta{
    margin-top:56px;
    display:flex; gap:40px; flex-wrap:wrap;
    opacity:0; transform:translateY(12px);
  }
  .hero-meta .item{font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--muted-on-ink);}
  .hero-meta .item span{display:block; font-family:'Fraunces',serif; font-size:26px; color:var(--text-on-ink); font-weight:500; margin-top:4px;}
  
  .hero-actions{
    margin-top:48px; display:flex; gap:16px; flex-wrap:wrap;
    opacity:0; transform:translateY(12px);
  }
  .hero-btn{
    font-family:'JetBrains Mono',monospace; font-size:13px; font-weight:600;
    padding:14px 28px; border-radius:100px;
    display:inline-flex; align-items:center; gap:8px;
    transition:all 0.2s ease;
  }
  .hero-btn.primary{ background:var(--signal); color:var(--ink); border:1px solid var(--signal); }
  .hero-btn.primary:hover{ background:#FF8F55; transform:translateY(-2px); box-shadow:0 8px 24px rgba(255,122,61,0.25); }
  .hero-btn.secondary{ background:transparent; color:var(--text-on-ink); border:1px solid var(--ink-line); }
  .hero-btn.secondary:hover{ border-color:var(--signal-dim); color:var(--signal); transform:translateY(-2px); }

  .fade-up{animation:fadeUp 0.9s cubic-bezier(.2,.7,.2,1) forwards;}
  @keyframes fadeUp{to{opacity:1; transform:translateY(0);}}

  .scroll-cue{
    position:absolute; bottom:36px; left:32px;
    font-family:'JetBrains Mono',monospace; font-size:11px; color:var(--muted-on-ink);
    display:flex; align-items:center; gap:10px;
  }
  .scroll-cue .line{width:36px; height:1px; background:var(--muted-on-ink);}

  /* ---------- SECTION SHELL ---------- */
  section{padding:120px 0;}
  .section-label{
    font-family:'JetBrains Mono',monospace;
    font-size:12px; letter-spacing:0.08em; text-transform:uppercase;
    color:var(--signal-dim);
    display:flex; align-items:center; gap:12px;
    margin-bottom:18px;
  }
  .section-label::before{content:''; width:22px; height:1px; background:var(--signal-dim);}
  .section-title{
    font-family:'Fraunces',serif; font-weight:600;
    font-size:clamp(30px, 4vw, 46px);
    letter-spacing:-0.01em;
    max-width:760px;
    margin-bottom:20px;
  }
  .reveal{opacity:0; transform:translateY(24px); transition:opacity 0.8s cubic-bezier(.2,.7,.2,1), transform 0.8s cubic-bezier(.2,.7,.2,1);}
  .reveal.in{opacity:1; transform:translateY(0);}

  /* ---------- ABOUT ---------- */
  .about-grid{
    display:grid; grid-template-columns:1.4fr 1fr; gap:60px; margin-top:48px;
    align-items:start;
  }
  .about-copy p{font-size:17px; line-height:1.75; color:var(--text-on-paper); max-width:56ch;}
  .about-copy p + p{margin-top:16px;}
  .stat-stack{display:flex; flex-direction:column; gap:0;}
  .stat-row{
    padding:20px 0; border-top:1px solid var(--paper-line);
    display:flex; justify-content:space-between; align-items:baseline;
  }
  .stat-row:last-child{border-bottom:1px solid var(--paper-line);}
  .stat-row .label{font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--muted-on-paper); text-transform:uppercase; letter-spacing:0.05em;}
  .stat-row .value{font-family:'Fraunces',serif; font-size:24px; font-weight:600;}
  @media (max-width:860px){ .about-grid{grid-template-columns:1fr;} }

  /* ---------- STACK / SKILLS ---------- */
  .stack{background:var(--ink); color:var(--text-on-ink);}
  .stack .section-title, .stack .section-label{color:var(--text-on-ink);}
  .stack .section-label{color:var(--signal);}
  .stack .section-label::before{background:var(--signal);}
  .stack-grid{
    display:grid; grid-template-columns:repeat(3, 1fr); gap:1px;
    background:var(--ink-line);
    margin-top:48px;
    border:1px solid var(--ink-line);
  }
  .stack-cell{background:var(--ink); padding:28px 26px;}
  .stack-cell h3{
    font-family:'JetBrains Mono',monospace; font-size:11px; text-transform:uppercase;
    letter-spacing:0.08em; color:var(--muted-on-ink); margin-bottom:16px;
  }
  .stack-cell ul{list-style:none;}
  .stack-cell li{
    font-family:'Fraunces',serif; font-size:19px; padding:6px 0;
    border-bottom:1px dashed var(--ink-line);
    display:flex; justify-content:space-between; align-items:center;
  }
  .stack-cell li:last-child{border-bottom:none;}
  .stack-cell li:hover{color:var(--signal);}
  @media (max-width:860px){ .stack-grid{grid-template-columns:1fr;} }

  /* ---------- PROJECTS ---------- */
  .proj{
    border-top:1px solid var(--paper-line);
    padding:52px 0;
    display:grid; grid-template-columns:0.9fr 1.6fr; gap:48px;
  }
  .proj:last-child{border-bottom:1px solid var(--paper-line);}
  .proj-head{position:sticky; top:110px; align-self:start;}
  .proj-tag{font-family:'JetBrains Mono',monospace; font-size:11px; color:var(--signal-dim); text-transform:uppercase; letter-spacing:0.06em; margin-bottom:10px;}
  .proj-name{font-family:'Fraunces',serif; font-weight:600; font-size:32px; line-height:1.15;}
  .proj-sub{font-family:'JetBrains Mono',monospace; font-size:12.5px; color:var(--muted-on-paper); margin-top:10px;}
  .proj-body p{font-size:16px; line-height:1.75; color:var(--text-on-paper); max-width:60ch;}
  .proj-body p + p{margin-top:14px;}
  .proj-chips{display:flex; flex-wrap:wrap; gap:8px; margin-top:22px;}
  .chip{
    font-family:'JetBrains Mono',monospace; font-size:11.5px;
    padding:6px 12px; border:1px solid var(--paper-line); border-radius:100px;
    color:var(--muted-on-paper);
  }
  @media (max-width:860px){ .proj{grid-template-columns:1fr; gap:20px;} .proj-head{position:static;} }

  /* ---------- PUBLICATION ---------- */
  .pub{background:var(--paper-dim);}
  .pub-grid{display:grid; grid-template-columns:280px 1fr; gap:56px; margin-top:48px; align-items:center;}
  .book-cover{
    aspect-ratio:2/3; background:linear-gradient(155deg, var(--ink) 0%, #1C2740 60%, var(--teal) 130%);
    border-radius:4px; position:relative; overflow:hidden;
    box-shadow:0 30px 60px -20px rgba(14,20,32,0.4);
    display:flex; flex-direction:column; justify-content:space-between; padding:26px 22px;
  }
  .book-cover .mark{font-family:'JetBrains Mono',monospace; font-size:10px; color:var(--muted-on-ink); letter-spacing:0.1em; text-transform:uppercase;}
  .book-cover .price{font-family:'Fraunces',serif; font-size:52px; color:var(--signal); font-weight:600; line-height:1;}
  .book-cover .title{font-family:'Fraunces',serif; font-style:italic; font-size:19px; color:var(--text-on-ink); line-height:1.3;}
  .book-cover .byline{font-family:'JetBrains Mono',monospace; font-size:10.5px; color:var(--muted-on-ink);}
  .pub-copy p{font-size:16.5px; line-height:1.75; max-width:58ch;}
  .pub-copy p + p{margin-top:14px;}
  .pub-copy .quote{
    font-family:'Fraunces',serif; font-style:italic; font-size:22px; line-height:1.4;
    margin-top:24px; padding-left:20px; border-left:2px solid var(--signal);
    color:var(--text-on-paper);
  }
  @media (max-width:720px){ .pub-grid{grid-template-columns:1fr;} .book-cover{max-width:220px;} }

  /* ---------- EDUCATION / LANG ---------- */
  .edu-grid{display:grid; grid-template-columns:1.3fr 1fr; gap:60px; margin-top:48px;}
  .edu-card{border-top:1px solid var(--paper-line); padding-top:24px;}
  .edu-school{font-family:'Fraunces',serif; font-size:24px; font-weight:600;}
  .edu-meta{font-family:'JetBrains Mono',monospace; font-size:12.5px; color:var(--muted-on-paper); margin-top:10px; line-height:1.8;}
  .lang-list, .soft-list{list-style:none;}
  .lang-list li{display:flex; justify-content:space-between; padding:14px 0; border-top:1px solid var(--paper-line); font-family:'JetBrains Mono',monospace; font-size:13px;}
  .lang-list li span:last-child{color:var(--muted-on-paper);}
  .soft-list{display:flex; flex-wrap:wrap; gap:8px; margin-top:16px;}
  .soft-list li{font-family:'JetBrains Mono',monospace; font-size:11.5px; padding:6px 12px; background:var(--paper-dim); border-radius:100px;}
  @media (max-width:860px){ .edu-grid{grid-template-columns:1fr;} }

  /* ---------- GITHUB SECTION ---------- */
  .github-section{ background:var(--ink); color:var(--text-on-ink); }
  .github-section .section-title,
  .github-section .section-label{ color:var(--text-on-ink); }
  .github-section .section-label{ color:var(--signal); }
  .github-section .section-label::before{ background:var(--signal); }

  .gh-header{ display:flex; align-items:center; gap:18px; margin-bottom:40px; flex-wrap:wrap; }
  .gh-avatar{
    width:72px; height:72px; border-radius:50%;
    border:2px solid var(--signal);
    overflow:hidden; flex-shrink:0;
  }
  .gh-avatar img{ width:100%; height:100%; object-fit:cover; }
  .gh-name{ font-family:'Fraunces',serif; font-size:26px; font-weight:600; }
  .gh-handle{ font-family:'JetBrains Mono',monospace; font-size:13px; color:var(--muted-on-ink); margin-top:4px; }
  .gh-bio{ font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--muted-on-ink); margin-top:6px; }

  .gh-stats{
    display:grid; grid-template-columns:repeat(4, 1fr);
    gap:1px; background:var(--ink-line);
    border:1px solid var(--ink-line); border-radius:8px;
    margin-bottom:48px;
    overflow:hidden;
  }
  .gh-stat{ background:var(--ink-soft); padding:22px 20px; text-align:center; }
  .gh-stat .gh-stat-val{ font-family:'Fraunces',serif; font-size:30px; font-weight:600; color:var(--text-on-ink); }
  .gh-stat .gh-stat-lbl{ font-family:'JetBrains Mono',monospace; font-size:11px; color:var(--muted-on-ink); text-transform:uppercase; letter-spacing:0.06em; margin-top:4px; }
  @media (max-width:720px){ .gh-stats{ grid-template-columns:repeat(2,1fr); } }
  @media (max-width:400px){ .gh-stats{ grid-template-columns:1fr; } }

  /* Contribution Graph — Year-wise */
  .gh-contrib-wrap{ margin-bottom:48px; }
  .gh-contrib-box{
    border:1px solid var(--ink-line); border-radius:10px;
    background:var(--ink-soft); padding:20px 24px;
    display:flex; gap:24px;
  }
  .gh-heatmap-side{ flex:1; min-width:0; }
  .gh-contrib-count{
    font-family:'Inter',sans-serif; font-size:15px; font-weight:500;
    color:var(--text-on-ink); margin-bottom:16px;
  }
  .gh-contrib-count span{ color:var(--muted-on-ink); font-weight:400; }
  .gh-heatmap-scroll{ overflow-x:auto; }
  .gh-heatmap{
    display:inline-flex; flex-direction:column; gap:4px;
    min-width:max-content;
  }
  .gh-months-row{
    display:flex; padding-left:28px; gap:0;
    font-family:'JetBrains Mono',monospace; font-size:10px; color:var(--muted-on-ink);
    margin-bottom:2px;
  }
  .gh-month-lbl{ display:inline-block; }
  .gh-body-row{ display:flex; gap:4px; align-items:flex-start; }
  .gh-day-lbls{
    display:flex; flex-direction:column; gap:3px; padding-top:2px;
    font-family:'JetBrains Mono',monospace; font-size:9px; color:var(--muted-on-ink);
    width:24px; flex-shrink:0;
  }
  .gh-day-lbls span{ height:11px; line-height:11px; }
  .gh-weeks-grid{ display:flex; gap:3px; }
  .gh-week{ display:flex; flex-direction:column; gap:3px; }
  .gh-cell{
    width:11px; height:11px; border-radius:2px;
    background:rgba(255,255,255,0.04); flex-shrink:0;
    cursor:default; transition:opacity 0.1s;
  }
  .gh-cell:hover{ outline:1px solid rgba(255,255,255,0.4); }
  .gh-cell[data-lv='0']{ background:#161F30; border:1px solid rgba(255,255,255,0.06); }
  .gh-cell[data-lv='e']{ background:transparent; border:none; }
  .gh-cell[data-lv='1']{ background:#0e4429; }
  .gh-cell[data-lv='2']{ background:#006d32; }
  .gh-cell[data-lv='3']{ background:#26a641; }
  .gh-cell[data-lv='4']{ background:#39d353; }
  .gh-legend-row{
    display:flex; align-items:center; gap:5px; margin-top:10px; justify-content:flex-end;
    font-family:'JetBrains Mono',monospace; font-size:10px; color:var(--muted-on-ink);
  }
  .gh-legend-row .gh-cell{ cursor:default; flex-shrink:0; }
  /* Year buttons sidebar */
  .gh-year-side{
    display:flex; flex-direction:column; gap:4px;
    flex-shrink:0; padding-top:36px;
  }
  .gh-yr-btn{
    font-family:'JetBrains Mono',monospace; font-size:12px;
    padding:5px 14px; border-radius:6px;
    border:1px solid transparent; cursor:pointer;
    color:var(--muted-on-ink); background:transparent;
    transition:all 0.15s ease; white-space:nowrap;
  }
  .gh-yr-btn:hover{ color:var(--signal); border-color:var(--signal); }
  .gh-yr-btn.active{ background:var(--signal); color:var(--ink); border-color:var(--signal); font-weight:600; }
  /* Tooltip */
  .gh-tooltip{
    position:fixed; z-index:999;
    background:#1a2236; border:1px solid var(--ink-line);
    color:var(--text-on-ink); font-family:'JetBrains Mono',monospace;
    font-size:11px; padding:6px 10px; border-radius:4px;
    pointer-events:none; white-space:nowrap;
    display:none;
  }
  @media (max-width:720px){
    .gh-contrib-box{ flex-direction:column; gap:12px; }
    .gh-year-side{ flex-direction:row; flex-wrap:wrap; padding-top:0; }
  }

  /* Repos */
  .gh-repos-title{ font-family:'JetBrains Mono',monospace; font-size:12px; text-transform:uppercase; letter-spacing:0.08em; color:var(--muted-on-ink); margin-bottom:20px; }
  .gh-repos{ display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:var(--ink-line); border:1px solid var(--ink-line); border-radius:8px; overflow:hidden; }
  .gh-repo{ background:var(--ink-soft); padding:22px 20px; display:flex; flex-direction:column; gap:8px; transition:background 0.2s ease; }
  .gh-repo:hover{ background:#1C2740; }
  .gh-repo-name{ font-family:'Fraunces',serif; font-size:17px; color:var(--text-on-ink); font-weight:600; }
  .gh-repo-desc{ font-family:'Inter',sans-serif; font-size:13px; color:var(--muted-on-ink); line-height:1.5; flex:1; }
  .gh-repo-meta{ display:flex; gap:16px; font-family:'JetBrains Mono',monospace; font-size:11px; color:var(--muted-on-ink); margin-top:4px; }
  .gh-repo-meta span{ display:flex; align-items:center; gap:4px; }
  .gh-repo-lang{ display:inline-block; width:9px; height:9px; border-radius:50%; background:var(--signal); }
  @media (max-width:860px){ .gh-repos{ grid-template-columns:repeat(2,1fr); } }
  @media (max-width:580px){ .gh-repos{ grid-template-columns:1fr; } }

  .gh-loading{ font-family:'JetBrains Mono',monospace; font-size:13px; color:var(--muted-on-ink); text-align:center; padding:40px; }
  .gh-error{ color:var(--signal); font-family:'JetBrains Mono',monospace; font-size:13px; text-align:center; padding:20px; }

  /* ---------- LEETCODE SECTION ---------- */
  .lc-section{ background:var(--paper-dim); margin-bottom:80px; }
  .lc-contrib-wrap{ max-width:900px; }
  .lc-contrib-title{
    font-family:'JetBrains Mono',monospace; font-size:12px;
    color:var(--muted-on-ink); margin-bottom:16px;
    display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:8px;
  }
  .lc-contrib-title span{ color:var(--text-on-ink); }
  .lc-chart-img{
    width:100%; max-width:900px;
    border-radius:10px;
    border:1px solid var(--ink-line);
    display:block;
    background:var(--ink);
  }

  /* ---------- FOOTER / CONTACT ---------- */
  footer{background:var(--ink); color:var(--text-on-ink); padding:120px 0 48px; position:relative; overflow:hidden;}
  .foot-title{
    font-family:'Fraunces',serif; font-weight:600;
    font-size:clamp(34px, 6vw, 68px); line-height:1.05; letter-spacing:-0.01em;
    max-width:820px;
  }
  .foot-title .accent{color:var(--signal); font-style:italic; font-weight:500;}
  .foot-links{display:flex; flex-wrap:wrap; gap:16px; margin-top:44px;}
  .foot-link{
    font-family:'JetBrains Mono',monospace; font-size:13px;
    border:1px solid var(--ink-line); border-radius:100px;
    padding:12px 22px; color:var(--text-on-ink);
    transition:border-color 0.2s ease, color 0.2s ease;
  }
  .foot-link:hover{border-color:var(--signal); color:var(--signal);}
  .foot-bottom{
    margin-top:60px; padding-top:24px; border-top:1px solid var(--ink-line);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:12px;
    font-family:'JetBrains Mono',monospace; font-size:11.5px; color:var(--muted-on-ink);
  }

  /* ---------- CONTACT FORM ---------- */
  .contact-form-section{
    margin-top:80px;
    padding-top:60px;
    border-top:1px solid var(--ink-line);
  }
  .contact-form-title{
    font-family:'Fraunces',serif; font-weight:600;
    font-size:clamp(24px, 3.5vw, 38px);
    letter-spacing:-0.01em;
    margin-bottom:10px;
  }
  .contact-form-sub{
    font-family:'JetBrains Mono',monospace;
    font-size:13px; color:var(--muted-on-ink);
    margin-bottom:40px;
  }
  .contact-form{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
  }
  .form-group{
    display:flex; flex-direction:column; gap:8px;
  }
  .form-group.full{ grid-column:1 / -1; }
  .form-group label{
    font-family:'JetBrains Mono',monospace;
    font-size:11px; text-transform:uppercase;
    letter-spacing:0.08em; color:var(--muted-on-ink);
  }
  .form-group input,
  .form-group textarea,
  .form-group select{
    background:var(--ink-soft);
    border:1px solid var(--ink-line);
    border-radius:6px;
    padding:14px 16px;
    color:var(--text-on-ink);
    font-family:'Inter',sans-serif;
    font-size:15px;
    outline:none;
    transition:border-color 0.25s ease, box-shadow 0.25s ease;
    resize:none;
    -webkit-appearance:none;
  }
  .form-group input::placeholder,
  .form-group textarea::placeholder{
    color:var(--muted-on-ink);
    opacity:0.6;
  }
  .form-group input:focus,
  .form-group textarea:focus,
  .form-group select:focus{
    border-color:var(--signal);
    box-shadow:0 0 0 3px rgba(255,122,61,0.15);
  }
  .form-group textarea{ min-height:140px; }
  .form-group select option{ background:var(--ink-soft); color:var(--text-on-ink); }
  .form-submit{
    grid-column: 1 / -1;
    display:flex; align-items:center; gap:20px; flex-wrap:wrap;
    margin-top:8px;
  }
  .btn-send{
    font-family:'JetBrains Mono',monospace; font-size:13.5px;
    background:var(--signal); color:var(--ink);
    border:none; border-radius:100px;
    padding:14px 32px;
    cursor:pointer;
    font-weight:600;
    letter-spacing:0.02em;
    transition:background 0.2s ease, transform 0.15s ease, box-shadow 0.2s ease;
    position:relative; overflow:hidden;
  }
  .btn-send:hover{
    background:#FF8F55;
    transform:translateY(-2px);
    box-shadow:0 8px 24px rgba(255,122,61,0.35);
  }
  .btn-send:active{ transform:translateY(0); }
  .btn-send.loading{ pointer-events:none; opacity:0.7; }
  .form-note{
    font-family:'JetBrains Mono',monospace; font-size:11.5px;
    color:var(--muted-on-ink);
  }
  .form-status{
    grid-column:1/-1;
    font-family:'JetBrains Mono',monospace; font-size:13px;
    padding:14px 18px; border-radius:6px;
    display:none;
  }
  .form-status.success{
    display:block;
    background:rgba(46,107,99,0.2);
    border:1px solid var(--teal);
    color:#6ECFC5;
  }
  .form-status.error{
    display:block;
    background:rgba(255,122,61,0.1);
    border:1px solid var(--signal-dim);
    color:var(--signal);
  }
  @media (max-width:620px){
    .contact-form{ grid-template-columns:1fr; }
  }

  /* ---------- MOBILE OPTIMIZATIONS ---------- */
  @media (max-width:720px){
    .wrap { padding: 0 20px; }
    nav { padding: 16px 20px; }
    nav.scrolled { padding: 12px 20px; }
    .hero { padding: 110px 0 60px; min-height: 100svh; }
    section { padding: 80px 0; }
    .proj { padding: 40px 0; }
    footer { padding: 80px 0 32px; }
  }
</style>
</head>
<body>

<nav>
  <a href="#" class="nav-mark">
    <img src="https://github.com/manishpandit1406.png" alt="Manish Pandit">
    Manish Pandit
  </a>
  <div class="nav-links">
    <a href="#about">about</a>
    <a href="#stack">stack</a>
    <a href="#work">work</a>
    <a href="#writing">writing</a>
    <a href="#github">github</a>
    <a href="#leetcode">leetcode</a>
    <a href="#contact">contact</a>
  </div>
</nav>

<header class="hero">
  <svg class="hero-net" id="netSvg" width="100%" height="100%" viewBox="0 0 1200 800" preserveAspectRatio="xMidYMid slice"></svg>
  <div class="wrap hero-inner">
    <div class="hero-content">
      <div class="terminal" id="terminal">
        <span class="tline"><span class="tprompt">&gt;</span> <span id="typed"></span><span class="cursor"></span></span>
      </div>
      <h1 class="display fade-up" id="h1" style="animation-delay:0.1s">Manish Pandit</h1>
      <p class="role fade-up" id="role" style="animation-delay:0.3s">
        <b>AI/ML Engineer</b> &amp; full-stack builder training multi-agent systems, telehealth
        platforms, and the interfaces between people and models — from Greater Noida, India.
      </p>
      <div class="hero-meta fade-up" id="meta" style="animation-delay:0.5s">
        <div class="item">CGPA<span>7.0</span></div>
        <div class="item">FOCUS<span>AI &amp; ML</span></div>
        <div class="item">SHIPPED<span>02 Platforms</span></div>
        <div class="item">PUBLISHED<span>01 Book</span></div>
      </div>
      <div class="hero-actions fade-up" style="animation-delay:0.7s">
        <a href="https://drive.google.com/file/d/18lYohn0bzCu2KWltK1ZSz1sW3lncDiuw/view?usp=sharing" class="hero-btn primary" target="_blank" rel="noopener">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path><polyline points="7 10 12 15 17 10"></polyline><line x1="12" y1="15" x2="12" y2="3"></line></svg>
          Download Resume
        </a>
        <a href="#contact" class="hero-btn secondary">
          Get in Touch
        </a>
      </div>
    </div>
    <div class="hero-photo fade-up" style="animation-delay:0.2s">
      <img src="https://github.com/manishpandit1406.png?size=800" alt="Manish Pandit Photo">
    </div>
  </div>
  <div class="scroll-cue"><span class="line"></span> SCROLL</div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-label reveal">01 — Profile</div>
    <h2 class="section-title reveal">Models are only half the system. The other half is what people do with them.</h2>
    <div class="about-grid">
      <div class="about-copy reveal">
        <p>I'm a B.Tech student in Artificial Intelligence &amp; Machine Learning at Lloyd Institute
        of Engineering and Technology, spending most of my time in the overlap between backend
        engineering and applied AI — the MERN stack on one side, prompt engineering and agentic
        frameworks on the other.</p>
        <p>My strongest work sits at that intersection: a telehealth platform with an AI symptom
        analyzer built into the patient flow, and a document-sharing SaaS tuned for speed at scale.
        I also write — a self-published, independently marketed book on how to actually talk to
        AI systems, from first prompt to production use.</p>
      </div>
      <div class="stat-stack reveal">
        <div class="stat-row"><span class="label">Degree</span><span class="value">B.Tech, AI &amp; ML</span></div>
        <div class="stat-row"><span class="label">Institute</span><span class="value">Lloyd IET</span></div>
        <div class="stat-row"><span class="label">Timeline</span><span class="value">2024 – 2028</span></div>
        <div class="stat-row"><span class="label">Base</span><span class="value">Greater Noida, UP</span></div>
      </div>
    </div>
  </div>
</section>

<section id="stack" class="stack">
  <div class="wrap">
    <div class="section-label reveal">02 — Stack</div>
    <h2 class="section-title reveal">What I build with, daily and otherwise.</h2>
    <div class="stack-grid reveal">
      <div class="stack-cell">
        <h3>Languages</h3>
        <ul><li>Python</li><li>JavaScript</li><li>Java</li><li>C</li><li>SQL</li></ul>
      </div>
      <div class="stack-cell">
        <h3>Backend &amp; Data</h3>
        <ul><li>Node.js</li><li>Express.js</li><li>RESTful APIs</li><li>MongoDB</li><li>PostgreSQL</li></ul>
      </div>
      <div class="stack-cell">
        <h3>Frontend</h3>
        <ul><li>React.js</li><li>Tailwind CSS</li></ul>
      </div>
      <div class="stack-cell">
        <h3>AI / ML</h3>
        <ul><li>Prompt Engineering</li><li>Agentic Frameworks</li><li>Predictive Modeling</li><li>Scikit-learn</li></ul>
      </div>
      <div class="stack-cell">
        <h3>Tools</h3>
        <ul><li>Git</li><li>Docker</li><li>Postman</li><li>Linux</li></ul>
      </div>
      <div class="stack-cell">
        <h3>Working languages</h3>
        <ul><li>English — professional</li><li>Hindi — native</li></ul>
      </div>
    </div>
  </div>
</section>

<section id="work">
  <div class="wrap">
    <div class="section-label reveal">03 — Selected work</div>
    <h2 class="section-title reveal">Two platforms, built end to end.</h2>

    <div class="proj reveal">
      <div class="proj-head">
        <div class="proj-tag">Telehealth · Medical AI</div>
        <div class="proj-name">Medora</div>
        <div class="proj-sub">Full-stack prototype — patient ↔ provider</div>
      </div>
      <div class="proj-body">
        <p>Led development of a full-stack telehealth prototype that connects patients directly
        with specialized healthcare providers, cutting out the friction of finding the right
        specialist.</p>
        <p>Built an AI-powered symptom analyzer into the patient intake flow, giving people a
        preliminary assessment and a more personalized starting point for care before they ever
        speak to a doctor.</p>
        <p>Designed and shipped a responsive Physician Dashboard so providers can manage
        appointments and securely pull up detailed patient medical history in one place, inside
        the same platform.</p>
        <div class="proj-chips">
          <span class="chip">React.js</span><span class="chip">Node.js</span>
          <span class="chip">Express.js</span><span class="chip">MongoDB</span>
          <span class="chip">AI Symptom Analysis</span>
        </div>
      </div>
    </div>

    <div class="proj reveal">
      <div class="proj-head">
        <div class="proj-tag">SaaS · Document Infrastructure</div>
        <div class="proj-name">Libraryy.in</div>
        <div class="proj-sub">Document-sharing &amp; monetization platform</div>
      </div>
      <div class="proj-body">
        <p>Engineered a scalable document monetization platform on the MERN stack, letting users
        upload, share, and earn from the documents they publish.</p>
        <p>Built secure file uploads alongside a custom analytics engine that tracks user
        engagement and behavior across the platform, giving creators visibility into how their
        documents actually perform.</p>
        <p>Went back into the backend to optimize the highest-traffic routes, landing a measured
        <b>20% faster</b> data retrieval on large document sets.</p>
        <div class="proj-chips">
          <span class="chip">MERN Stack</span><span class="chip">PostgreSQL</span>
          <span class="chip">Secure Uploads</span><span class="chip">Analytics Engine</span>
          <span class="chip">Performance Tuning</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="writing" class="pub">
  <div class="wrap">
    <div class="section-label reveal">04 — Writing</div>
    <h2 class="section-title reveal">A field guide to talking with machines.</h2>
    <div class="pub-grid reveal">
      <div class="book-cover">
        <div class="mark">Technical Non-Fiction</div>
        <div class="price">$350K</div>
        <div>
          <div class="title">The $350,000 Worth Prompt</div>
          <div class="byline">Manish Pandit · Amazon KDP</div>
        </div>
      </div>
      <div class="pub-copy">
        <p>I wrote and independently published <i>"$350,000 Worth Prompt: Talking to the AI
        Revolution,"</i> a practical, beginner-facing guide to prompt engineering, AI
        communication, and applying artificial intelligence in everyday and professional
        contexts.</p>
        <p>I ran the entire process myself — content, formatting, cover, and the marketing and
        promotional push after launch — through Amazon KDP.</p>
        <p class="quote">Good prompting isn't a trick. It's a skill you can teach, and I wanted a
        book that actually teaches it.</p>
      </div>
    </div>
  </div>
</section>

<section id="education">
  <div class="wrap">
    <div class="section-label reveal">05 — Education &amp; beyond</div>
    <h2 class="section-title reveal">Where the fundamentals come from.</h2>
    <div class="edu-grid">
      <div class="edu-card reveal">
        <div class="edu-school">Lloyd Institute of Engineering and Technology</div>
        <div class="edu-meta">
          B.Tech, Artificial Intelligence &amp; Machine Learning<br>
          2024 – 2028 · Greater Noida, UP<br>
          Current CGPA: 7.0
        </div>
      </div>
      <div class="reveal">
        <ul class="lang-list">
          <li><span>English</span><span>Professional working proficiency</span></li>
          <li><span>Hindi</span><span>Native proficiency</span></li>
        </ul>
        <ul class="soft-list">
          <li>Critical Thinking</li><li>Problem-Solving</li><li>Time Management</li>
          <li>Adaptability</li><li>Teamwork</li><li>Collaboration</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ===== GITHUB SECTION ===== -->
<section id="github" class="github-section">
  <div class="wrap">
    <div class="section-label reveal">06 — Open Source</div>
    <h2 class="section-title reveal">Code I ship in public.</h2>

    <div id="ghContent" class="reveal">
      <div class="gh-loading">// fetching github data…</div>
    </div>
  </div>
</section>

<!-- ===== LEETCODE SECTION ===== -->
<section id="leetcode" class="lc-section">
  <div class="wrap">
    <div class="section-label reveal">07 — Problem Solving</div>
    <h2 class="section-title reveal">Algorithms, data structures, daily grind.</h2>
    
    <div id="lcContent" class="reveal">
      <div class="gh-loading">// fetching leetcode data…</div>
    </div>
  </div>
</section>

<div class="gh-tooltip" id="ghTooltip"></div>

<footer id="contact">
  <div class="wrap">
    <div class="section-label reveal">08 — Contact</div>
    <h2 class="foot-title reveal">Building something with AI at the core?<br><span class="accent">Let's talk it through.</span></h2>
    <div class="foot-links reveal">
      <a class="foot-link" href="mailto:work.manishpandit1406@gmail.com">work.manishpandit1406@gmail.com</a>
      <a class="foot-link" href="tel:+919971887022">+91 9971887022</a>
      <a class="foot-link" href="https://linkedin.com/in/manish-pandit-6bb183335" target="_blank" rel="noopener">LinkedIn</a>
      <a class="foot-link" href="https://github.com/manishpandit1406" target="_blank" rel="noopener">GitHub</a>
    </div>
    <!-- ===== CONTACT US FORM ===== -->
    <div class="contact-form-section reveal">
      <div class="contact-form-title">Send me a message</div>
      <p class="contact-form-sub">// Prefer async? Fill out the form and I'll reply within 24 hours.</p>

      <form class="contact-form" id="contactForm" novalidate>
        <div class="form-group">
          <label for="cf-name">Your Name</label>
          <input type="text" id="cf-name" name="name" placeholder="Manish Pandit" autocomplete="name" required>
        </div>

        <div class="form-group">
          <label for="cf-email">Email Address</label>
          <input type="email" id="cf-email" name="email" placeholder="hello@example.com" autocomplete="email" required>
        </div>

        <div class="form-group full">
          <label for="cf-subject">Subject</label>
          <input type="text" id="cf-subject" name="subject" placeholder="Brief subject or topic…" required>
        </div>

        <div class="form-group full">
          <label for="cf-message">Message</label>
          <textarea id="cf-message" name="message" placeholder="Tell me what you're building or thinking about…" required></textarea>
        </div>

        <div class="form-submit">
          <button type="submit" class="btn-send" id="btnSend">Send Message →</button>
          <span class="form-note">No spam. Honest reply guaranteed.</span>
        </div>

        <div class="form-status" id="formStatus"></div>
      </form>
    </div>
    <!-- ===== END CONTACT US FORM ===== -->

    <div class="foot-bottom">
      <span>Manish Pandit — Greater Noida, UP</span>
      <span>Built as a portfolio, not a template.</span>
    </div>
  </div>
</footer>

<script>
  /* ---------- GITHUB SECTION ---------- */
  (function(){
    const GH_USER = 'manishpandit1406';
    const API = 'https://api.github.com';
    const tooltip = document.getElementById('ghTooltip');

    function langColor(lang){
      const map = {
        JavaScript:'#f1e05a', Python:'#3572A5', Java:'#b07219',
        TypeScript:'#2b7489', HTML:'#e34c26', CSS:'#563d7c',
        'C++':'#f34b7d', C:'#555555', Shell:'#89e051',
        Go:'#00ADD8', Rust:'#dea584', Ruby:'#701516'
      };
      return map[lang] || '#8A93AA';
    }

    async function fetchGH(){
      const [userRes, reposRes] = await Promise.all([
        fetch(API + '/users/' + GH_USER),
        fetch(API + '/users/' + GH_USER + '/repos?per_page=100&sort=pushed')
      ]);
      if(!userRes.ok) throw new Error('User not found');
      const user  = await userRes.json();
      const repos = await reposRes.json();
      return { user, repos };
    }

    /* ---- Shared state ---- */
    const MONTH_NAMES = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
    let allContribData = null;

    function toLocalISO(d) {
      const y = d.getFullYear();
      const m = String(d.getMonth() + 1).padStart(2, '0');
      const day = String(d.getDate()).padStart(2, '0');
      return `${y}-${m}-${day}`;
    }

    /* ---- Core: build heatmap from date range ---- */
    function renderHeatmap(rangeStart, rangeEnd, label){
      if(!allContribData) return;
      const tooltip = document.getElementById('ghTooltip');
      const today   = new Date();

      const map = {};
      allContribData.contributions.forEach(c => { map[c.date] = c; });

      // Align grid start to Sunday
      const gridStart = new Date(rangeStart);
      gridStart.setDate(gridStart.getDate() - gridStart.getDay());

      // Align grid end to Saturday
      const gridEnd = new Date(rangeEnd);
      const toSat = 6 - gridEnd.getDay();
      if(toSat > 0) gridEnd.setDate(gridEnd.getDate() + toSat);

      const weeks = [];
      let d = new Date(gridStart);
      while(d <= gridEnd){
        const week = [];
        for(let i = 0; i < 7; i++){
          const ds = toLocalISO(d);
          const inRange = d >= rangeStart && d <= rangeEnd;
          const c = map[ds];
          week.push({
            date: ds,
            count: inRange && c ? c.count : 0,
            level: inRange && c ? c.level : (inRange ? 0 : 'e'),
            inRange
          });
          d.setDate(d.getDate() + 1);
        }
        weeks.push(week);
      }

      // Month labels
      let monthsHTML = '';
      let lastMonth  = -1;
      weeks.forEach(week => {
        const firstIn = week.find(c => c.inRange);
        const mm = firstIn ? new Date(firstIn.date).getMonth() : -1;
        if(mm !== -1 && mm !== lastMonth){
          monthsHTML += `<span class="gh-month-lbl" style="width:${14}px">${MONTH_NAMES[mm]}</span>`;
          lastMonth = mm;
        } else {
          monthsHTML += `<span class="gh-month-lbl" style="width:${14}px"></span>`;
        }
      });

      // Weeks grid
      const weeksHTML = weeks.map(week => {
        const cells = week.map(day => {
          const tip = day.inRange
            ? `${day.date}: ${day.count} contribution${day.count!==1?'s':''}`
            : '';
          return `<div class="gh-cell" data-lv="${day.level}" ${tip?`data-tip="${tip}"`:''} title="${tip}"></div>`;
        }).join('');
        return `<div class="gh-week">${cells}</div>`;
      }).join('');

      document.getElementById('gh-contrib-count').innerHTML = label;
      document.getElementById('gh-months-row').innerHTML = monthsHTML;
      document.getElementById('gh-weeks-grid').innerHTML  = weeksHTML;

      // Tooltip events
      document.querySelectorAll('#gh-weeks-grid .gh-cell[data-tip]').forEach(cell => {
        cell.addEventListener('mousemove', e => {
          tooltip.textContent = cell.dataset.tip;
          tooltip.style.display = 'block';
          tooltip.style.left = (e.clientX + 14) + 'px';
          tooltip.style.top  = (e.clientY - 36) + 'px';
        });
        cell.addEventListener('mouseleave', () => { tooltip.style.display='none'; });
      });
    }

    /* ---- Default: last 12 months (rolling) ---- */
    function buildHeatmapLastYear(){
      const today = new Date();
      const start = new Date(today);
      // Go back exactly 52 weeks (364 days) to Sunday
      start.setDate(today.getDate() - 363);
      start.setDate(start.getDate() - start.getDay()); // align to Sunday

      // Count contributions in this window
      const map = {};
      allContribData.contributions.forEach(c => { map[c.date] = c; });
      let total = 0;
      const s = new Date(start), e = new Date(today);
      for(let dd = new Date(s); dd <= e; dd.setDate(dd.getDate()+1)){
        const ds = toLocalISO(dd);
        if(map[ds]) total += map[ds].count;
      }

      let grandTotal = 0;
      for(let k in allContribData.total){
        if(k !== 'lastYear') grandTotal += allContribData.total[k];
      }

      const label = `<strong>${total.toLocaleString()}</strong> contributions in <span>the last year</span> <span style="color:var(--muted-on-ink); font-size:12px; margin-left:8px">(Total: ${grandTotal.toLocaleString()})</span>`;
      renderHeatmap(start, today, label);

      // No year button active in default mode
      document.querySelectorAll('.gh-yr-btn').forEach(b => b.classList.remove('active'));
    }

    /* ---- Year click: show full calendar year ---- */
    function buildHeatmapForYear(year){
      const yearStart = new Date(`${year}-01-01`);
      const yearEnd   = new Date(`${year}-12-31`);
      const today     = new Date();

      const map = {};
      allContribData.contributions.forEach(c => { map[c.date] = c; });
      const total = allContribData.total[year] || 0;

      let grandTotal = 0;
      for(let k in allContribData.total){
        if(k !== 'lastYear') grandTotal += allContribData.total[k];
      }

      const label = `<strong>${total.toLocaleString()}</strong> contributions in <span>${year}</span> <span style="color:var(--muted-on-ink); font-size:12px; margin-left:8px">(Total: ${grandTotal.toLocaleString()})</span>`;
      renderHeatmap(yearStart, yearEnd, label);
    }

    /* ---- Skeleton HTML for the heatmap (filled once API responds) ---- */
    function buildContribSection(username){
      return `
        <div class="gh-contrib-wrap">
          <div class="gh-contrib-box">
            <div class="gh-heatmap-side">
              <div class="gh-contrib-count" id="gh-contrib-count">// Loading contributions&hellip;</div>
              <div class="gh-heatmap-scroll">
                <div class="gh-heatmap">
                  <div class="gh-months-row" id="gh-months-row"></div>
                  <div class="gh-body-row">
                    <div class="gh-day-lbls">
                      <span></span>
                      <span>Mon</span>
                      <span></span>
                      <span>Wed</span>
                      <span></span>
                      <span>Fri</span>
                      <span></span>
                    </div>
                    <div class="gh-weeks-grid" id="gh-weeks-grid">
                      <div style="color:var(--muted-on-ink);font-family:'JetBrains Mono',monospace;font-size:12px;padding:20px">// fetching&hellip;</div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="gh-legend-row">
                Less
                <div class="gh-cell" data-lv="0"></div>
                <div class="gh-cell" data-lv="1"></div>
                <div class="gh-cell" data-lv="2"></div>
                <div class="gh-cell" data-lv="3"></div>
                <div class="gh-cell" data-lv="4"></div>
                More
              </div>
            </div>
            <div class="gh-year-side" id="gh-year-side"></div>
          </div>
        </div>`;
    }

    async function loadContributions(username){
      const res = await fetch(`https://github-contributions-api.jogruber.de/v4/${username}?y=all`);
      if(!res.ok) throw new Error('Contributions API failed');
      allContribData = await res.json();

      // Get all years, sorted descending
      const years = Object.keys(allContribData.total)
        .map(Number)
        .sort((a, b) => b - a);

      // Render year buttons
      const sideEl = document.getElementById('gh-year-side');
      if(sideEl){
        sideEl.innerHTML = years.map(y =>
          `<button class="gh-yr-btn" data-year="${y}" onclick="ghSelectYear(${y})">${y}</button>`
        ).join('');
      }

      // Default: show last 12 months (like GitHub default)
      buildHeatmapLastYear();
    }

    function buildRepos(repos){
      const top = repos.filter(r=>!r.fork).slice(0,6);
      if(!top.length) return '';
      return `
        <div class="gh-repos-title">// pinned repositories</div>
        <div class="gh-repos">
          ${top.map(r=>`
            <a class="gh-repo" href="${r.html_url}" target="_blank" rel="noopener">
              <div class="gh-repo-name">${r.name}</div>
              <div class="gh-repo-desc">${r.description || 'No description provided.'}</div>
              <div class="gh-repo-meta">
                ${r.language ? `<span><i class="gh-repo-lang" style="background:${langColor(r.language)}"></i>${r.language}</span>` : ''}
                <span>⭐ ${r.stargazers_count}</span>
                <span>🍴 ${r.forks_count}</span>
              </div>
            </a>`).join('')}
        </div>`;
    }

    // Global year-select handler — called from year button onclick
    window.ghSelectYear = function(year){
      document.querySelectorAll('.gh-yr-btn').forEach(btn => {
        btn.classList.toggle('active', parseInt(btn.dataset.year) === year);
      });
      buildHeatmapForYear(year);
    };

    fetchGH().then(({ user, repos })=>{
      const totalStars  = repos.reduce((a,r)=>a+r.stargazers_count, 0);
      const followers   = user.followers || 0;

      const html = `
        <div class="gh-header">
          <div class="gh-avatar"><img src="${user.avatar_url}" alt="${user.login} avatar"></div>
          <div>
            <div class="gh-name">${user.name || user.login}</div>
            <div class="gh-handle">@${user.login}</div>
            ${user.bio ? `<div class="gh-bio">${user.bio}</div>` : ''}
          </div>
        </div>
        <div class="gh-stats">
          <div class="gh-stat"><div class="gh-stat-val">${user.public_repos}</div><div class="gh-stat-lbl">Public Repos</div></div>
          <div class="gh-stat"><div class="gh-stat-val">${totalStars}</div><div class="gh-stat-lbl">Total Stars</div></div>
          <div class="gh-stat"><div class="gh-stat-val">${followers}</div><div class="gh-stat-lbl">Followers</div></div>
          <div class="gh-stat"><div class="gh-stat-val">${user.following}</div><div class="gh-stat-lbl">Following</div></div>
        </div>
        ${buildContribSection(GH_USER)}
        ${buildRepos(repos)}
      `;
      document.getElementById('ghContent').innerHTML = html;

      // Now fetch real contribution data
      return loadContributions(GH_USER);
    }).catch(err=>{
      console.error(err);
      document.getElementById('ghContent').innerHTML =
        '<div class="gh-error">// Could not load GitHub data. <a href="https://github.com/manishpandit1406" target="_blank" rel="noopener" style="color:var(--signal)">View on GitHub →</a></div>';
    });
  })();

  /* ---------- LEETCODE SECTION ---------- */
  (function(){
    const LC_USER = 'manishpandit1406';
    const tooltip = document.getElementById('ghTooltip'); // reuse tooltip
    let lcData = null;

    const MONTH_NAMES = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];

    // Convert count to level
    function getLevel(count){
      if(!count) return 0;
      if(count <= 1) return 1;
      if(count <= 3) return 2;
      if(count <= 5) return 3;
      return 4;
    }

    function renderLCHeatmap(startDate, endDate, labelHtml){
      const map = lcData.submissionMap;
      
      const weeks = [];
      let d = new Date(startDate);
      while(d <= endDate){
        const week = [];
        for(let i=0; i<7; i++){
          const ds = d.toISOString().split('T')[0];
          const inRange = (d >= startDate && d <= endDate);
          const count = map[ds] || 0;
          week.push({
            date: ds,
            count: inRange ? count : 0,
            level: inRange ? getLevel(count) : 'e',
            inRange
          });
          d.setDate(d.getDate() + 1);
        }
        weeks.push(week);
      }

      // Month labels
      let monthsHTML = '';
      let lastMonth  = -1;
      weeks.forEach(week => {
        const firstIn = week.find(c => c.inRange);
        const mm = firstIn ? new Date(firstIn.date).getMonth() : -1;
        if(mm !== -1 && mm !== lastMonth){
          monthsHTML += `<span class="gh-month-lbl" style="width:14px">${MONTH_NAMES[mm]}</span>`;
          lastMonth = mm;
        } else {
          monthsHTML += `<span class="gh-month-lbl" style="width:14px"></span>`;
        }
      });

      // Weeks grid
      const weeksHTML = weeks.map(week => {
        const cells = week.map(day => {
          const tip = day.inRange
            ? `${day.date}: ${day.count} submission${day.count!==1?'s':''}`
            : '';
          return `<div class="gh-cell" data-lv="${day.level}" ${tip?`data-tip="${tip}"`:''} title="${tip}"></div>`;
        }).join('');
        return `<div class="gh-week">${cells}</div>`;
      }).join('');

      document.getElementById('lc-contrib-count').innerHTML = labelHtml;
      document.getElementById('lc-months-row').innerHTML = monthsHTML;
      document.getElementById('lc-weeks-grid').innerHTML  = weeksHTML;

      // Tooltips
      document.querySelectorAll('#lc-weeks-grid .gh-cell[data-tip]').forEach(cell => {
        cell.addEventListener('mousemove', e => {
          tooltip.textContent = cell.dataset.tip;
          tooltip.style.display = 'block';
          tooltip.style.left = (e.clientX + 14) + 'px';
          tooltip.style.top  = (e.clientY - 36) + 'px';
        });
        cell.addEventListener('mouseleave', () => { tooltip.style.display='none'; });
      });
    }

    function buildLCHeatmapLastYear(){
      const today = new Date();
      const start = new Date(today);
      start.setDate(today.getDate() - 363);
      start.setDate(start.getDate() - start.getDay()); // align to Sunday

      const map = lcData.submissionMap;
      let total = 0;
      const s = new Date(start), e = new Date(today);
      for(let dd = new Date(s); dd <= e; dd.setDate(dd.getDate()+1)){
        const ds = dd.toISOString().split('T')[0];
        if(map[ds]) total += map[ds];
      }

      const label = `<strong>${total.toLocaleString()}</strong> submissions in <span>the last year</span>`;
      renderLCHeatmap(start, today, label);
    }

    function buildLCSection(){
      return `
        <div class="gh-contrib-wrap">
          <div class="gh-contrib-box">
            <div class="gh-heatmap-side">
              <div class="gh-contrib-count" id="lc-contrib-count">// Loading submissions&hellip;</div>
              <div class="gh-heatmap-scroll">
                <div class="gh-heatmap">
                  <div class="gh-months-row" id="lc-months-row"></div>
                  <div class="gh-body-row">
                    <div class="gh-day-lbls">
                      <span></span><span>Mon</span><span></span><span>Wed</span><span></span><span>Fri</span><span></span>
                    </div>
                    <div class="gh-weeks-grid" id="lc-weeks-grid">
                      <div style="color:var(--muted-on-ink);font-family:'JetBrains Mono',monospace;font-size:12px;padding:20px">// fetching&hellip;</div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="gh-legend-row">
                Less
                <div class="gh-cell" data-lv="0"></div>
                <div class="gh-cell" data-lv="1"></div>
                <div class="gh-cell" data-lv="2"></div>
                <div class="gh-cell" data-lv="3"></div>
                <div class="gh-cell" data-lv="4"></div>
                More
              </div>
            </div>
          </div>
        </div>`;
    }

    async function loadLeetCode(){
      try {
        const [statsRes, profileRes] = await Promise.all([
          fetch('https://alfa-leetcode-api.onrender.com/userProfile/' + LC_USER),
          fetch('https://alfa-leetcode-api.onrender.com/' + LC_USER)
        ]);
        
        if(!statsRes.ok || !profileRes.ok) throw new Error('API failed');
        
        const data = await statsRes.json();
        const profile = await profileRes.json();
        
        if(data.errors || profile.errors) throw new Error('User not found');

        // Convert submissionCalendar (UNIX timestamps) to YYYY-MM-DD map
        const subMap = {};
        if(data.submissionCalendar) {
          const cal = typeof data.submissionCalendar === 'string' ? JSON.parse(data.submissionCalendar) : data.submissionCalendar;
          for(const [ts, count] of Object.entries(cal)){
            const d = new Date(parseInt(ts) * 1000);
            const ds = d.toISOString().split('T')[0];
            subMap[ds] = count;
          }
        }
        
        lcData = {
          ...data,
          submissionMap: subMap
        };

        const accRate = ((data.totalSolved / data.totalQuestions) * 100).toFixed(1);
        const displayName = profile.name || LC_USER;
        const avatarUrl = profile.avatar || '';
        
        const avatarHtml = avatarUrl 
          ? `<img src="${avatarUrl}" alt="${LC_USER} avatar" style="width:100%; height:100%; object-fit:cover;">`
          : `<div style="font-size:40px;">♨</div>`;

        const html = `
          <div class="gh-header">
            <div class="gh-avatar" style="background:linear-gradient(135deg,#FFA116,#FF7A3D); display:flex; align-items:center; justify-content:center; overflow:hidden;">
              ${avatarHtml}
            </div>
            <div>
              <div class="gh-name">${displayName}</div>
              <div class="gh-handle">@${profile.username || LC_USER}</div>
              <div class="gh-bio"><a href="https://leetcode.com/${LC_USER}" target="_blank" rel="noopener" style="color:var(--signal); text-decoration:none;">View LeetCode Profile →</a></div>
            </div>
          </div>
          <div class="gh-stats">
            <div class="gh-stat"><div class="gh-stat-val">${data.totalSolved}</div><div class="gh-stat-lbl">Total Solved</div></div>
            <div class="gh-stat"><div class="gh-stat-val">${data.easySolved} / ${data.mediumSolved} / ${data.hardSolved}</div><div class="gh-stat-lbl">E / M / H</div></div>
            <div class="gh-stat"><div class="gh-stat-val">${data.ranking.toLocaleString()}</div><div class="gh-stat-lbl">Global Rank</div></div>
            <div class="gh-stat"><div class="gh-stat-val">${accRate}%</div><div class="gh-stat-lbl">Acceptance</div></div>
          </div>
          ${buildLCSection()}
        `;
        document.getElementById('lcContent').innerHTML = html;
        buildLCHeatmapLastYear();

      } catch (err) {
        console.error(err);
        document.getElementById('lcContent').innerHTML = '<div class="gh-error">// Could not load LeetCode data.</div>';
      }
    }

    loadLeetCode();
  })();

  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    const btn    = document.getElementById('btnSend');
    const status = document.getElementById('formStatus');
    const name    = document.getElementById('cf-name').value.trim();
    const email   = document.getElementById('cf-email').value.trim();
    const subject = document.getElementById('cf-subject').value;
    const message = document.getElementById('cf-message').value.trim();

    // Basic validation
    if(!name || !email || !subject || !message){
      status.className = 'form-status error';
      status.textContent = '// All fields are required. Please fill them in.';
      return;
    }
    const emailRx = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if(!emailRx.test(email)){
      status.className = 'form-status error';
      status.textContent = '// That email address doesn\'t look right. Try again.';
      return;
    }

    btn.classList.add('loading');
    btn.textContent = 'Sending…';
    status.className = 'form-status';

    fetch('https://api.qwikmailer.in/v1/forms/c2138548-3615-4c8d-a430-c8d9e3c8659d/submit', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({
        "data": {
          "Your Name": name,
          "Email Address": email,
          "Subject": subject,
          "Message": message
        }
      })
    })
    .then(res => res.json())
    .then(data => {
      console.log(data);
      btn.classList.remove('loading');
      btn.textContent = 'Send Message →';
      status.className = 'form-status success';
      status.textContent = '// Message received — I\'ll get back to you within 24 hours. Thanks, ' + name + '!';
      document.getElementById('contactForm').reset();
    })
    .catch(err => {
      console.error(err);
      btn.classList.remove('loading');
      btn.textContent = 'Send Message →';
      status.className = 'form-status error';
      status.textContent = '// Something went wrong. Please try again.';
    });
  });

  // Typewriter in hero terminal
  const typedEl = document.getElementById('typed');
  const phrases = [
    "loading neural weights... [done]",
    "initializing multi-agent system... [done]",
    "init_profile('manish-pandit') -> role: AI/ML Engineer"
  ];
  let ci = 0, pi = 0, deleting = false;
  function typeLoop(){
    const full = phrases[pi];
    if(deleting){
      ci--;
      typedEl.textContent = full.slice(0, ci);
      if(ci === 0){
        deleting = false;
        pi = (pi + 1) % phrases.length;
        setTimeout(typeLoop, 500);
      } else {
        setTimeout(typeLoop, 15);
      }
    } else {
      ci++;
      typedEl.textContent = full.slice(0, ci);
      if(ci === full.length){
        const pause = (pi === phrases.length - 1) ? 3500 : 1000;
        deleting = true;
        setTimeout(typeLoop, pause);
      } else {
        setTimeout(typeLoop, 28);
      }
    }
  }
  typeLoop();

  // Reveal on scroll
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{
      if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); }
    });
  }, {threshold:0.15});
  revealEls.forEach(el=>io.observe(el));

  // Nav scroll state
  const navEl = document.querySelector('nav');
  window.addEventListener('scroll', () => {
    if(window.scrollY > 60) {
      navEl.classList.add('scrolled');
    } else {
      navEl.classList.remove('scrolled');
    }
  });

  // Ambient node network in hero
  const svg = document.getElementById('netSvg');
  const NS = "http://www.w3.org/2000/svg";
  const nodes = [];
  const nodeCount = 32;
  for(let i=0;i<nodeCount;i++){
    nodes.push({
      x: Math.random()*1200,
      y: Math.random()*800,
      vx: (Math.random()-0.5)*0.25,
      vy: (Math.random()-0.5)*0.25
    });
  }
  const lineEls = [];
  const dotEls = [];
  for(let i=0;i<nodeCount;i++){
    const c = document.createElementNS(NS,'circle');
    c.setAttribute('r','2.5');
    c.setAttribute('fill','#FF7A3D');
    c.setAttribute('opacity','0.6');
    svg.appendChild(c);
    dotEls.push(c);
  }
  
  let mx = -1000, my = -1000;
  document.querySelector('.hero').addEventListener('mousemove', e => {
    const rect = svg.getBoundingClientRect();
    mx = e.clientX - rect.left;
    my = e.clientY - rect.top;
  });
  document.querySelector('.hero').addEventListener('mouseleave', () => {
    mx = -1000; my = -1000;
  });

  function dist(a,b){ return Math.hypot(a.x-b.x, a.y-b.y); }
  function render(){
    // clear old lines
    lineEls.forEach(l=>l.remove());
    lineEls.length = 0;
    for(let i=0;i<nodeCount;i++){
      const a = nodes[i];
      a.x += a.vx; a.y += a.vy;
      if(a.x<0||a.x>1200) a.vx*=-1;
      if(a.y<0||a.y>800) a.vy*=-1;
      
      // mouse interaction: connect & repel slightly
      const dMouse = Math.hypot(a.x - mx, a.y - my);
      if(dMouse < 180){
        a.x += (a.x - mx) * 0.008;
        a.y += (a.y - my) * 0.008;
        const l = document.createElementNS(NS,'line');
        l.setAttribute('x1',a.x); l.setAttribute('y1',a.y);
        l.setAttribute('x2',mx); l.setAttribute('y2',my);
        l.setAttribute('stroke', '#FF7A3D');
        l.setAttribute('stroke-width', '1.2');
        l.setAttribute('opacity', (1 - dMouse/180) * 0.8);
        svg.insertBefore(l, svg.firstChild);
        lineEls.push(l);
      }

      dotEls[i].setAttribute('cx', a.x);
      dotEls[i].setAttribute('cy', a.y);
      for(let j=i+1;j<nodeCount;j++){
        const b = nodes[j];
        const d = dist(a,b);
        if(d < 170){
          const l = document.createElementNS(NS,'line');
          l.setAttribute('x1',a.x); l.setAttribute('y1',a.y);
          l.setAttribute('x2',b.x); l.setAttribute('y2',b.y);
          l.setAttribute('stroke', '#3A465F');
          l.setAttribute('stroke-width', '1');
          l.setAttribute('opacity', (1 - d/170) * 0.6);
          svg.insertBefore(l, svg.firstChild);
          lineEls.push(l);
        }
      }
    }
    requestAnimationFrame(render);
  }
  if(!window.matchMedia('(prefers-reduced-motion: reduce)').matches){
    render();
  }
</script>

</body>
</html>
