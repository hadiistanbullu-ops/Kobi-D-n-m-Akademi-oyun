[Kobi Akademi-standart-index.html.html](https://github.com/user-attachments/files/30131813/Kobi.Akademi-standart-index.html.html)
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#0A1628">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Değişim">
<meta name="mobile-web-app-capable" content="yes">
<meta name="description" content="Kotter, ADKAR ve Lewin modellerini 100 senaryo sorusuyla öğren.">
<title>Değişim Liderliği Akademisi</title>
<link rel="manifest" href="manifest.json">
<link rel="apple-touch-icon" href="icons/icon-192.png">
<link rel="icon" href="icons/icon-192.png">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0A1628;--s1:#111E35;--s2:#1A2B47;--s3:#243554;
  --ac:#FF6B35;--ac2:#00D4AA;--ac3:#7B61FF;--gold:#FFD700;
  --tx:#E8EDF5;--mu:#8B9BB4;--bd:rgba(255,255,255,.08);--red:#FF5050;
  --sat:env(safe-area-inset-top,0px);--sab:env(safe-area-inset-bottom,0px);
  --sal:env(safe-area-inset-left,0px);--sar:env(safe-area-inset-right,0px);
}
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
html,body{height:100%;background:var(--bg);color:var(--tx);font-family:'DM Sans',sans-serif;overflow:hidden;}
::-webkit-scrollbar{width:4px;} ::-webkit-scrollbar-track{background:transparent;} ::-webkit-scrollbar-thumb{background:var(--s3);border-radius:4px;}

/* ── PAGE SYSTEM ── */
.pg{position:fixed;inset:0;display:flex;flex-direction:column;opacity:0;pointer-events:none;transition:opacity .3s ease,transform .3s ease;transform:translateY(10px);}
.pg.on{opacity:1;pointer-events:all;transform:translateY(0);}

/* ── SHARED COMPONENTS ── */
.topbar{background:var(--s1);border-bottom:1px solid var(--bd);padding:calc(var(--sat) + 10px) 16px 10px;display:flex;align-items:center;gap:10px;flex-shrink:0;}
.back-btn{width:36px;height:36px;border-radius:10px;background:var(--s2);border:none;color:var(--mu);font-size:18px;display:flex;align-items:center;justify-content:center;cursor:pointer;flex-shrink:0;}
.back-btn:active{background:var(--s3);}
.topbar-title{font-family:'Syne',sans-serif;font-size:15px;font-weight:700;}
.scrollable{flex:1;overflow-y:auto;-webkit-overflow-scrolling:touch;}
.inner{max-width:520px;margin:0 auto;padding:20px 16px calc(var(--sab) + 24px);}

/* ── LANDING ── */
#pg-land .scrollable{background:linear-gradient(160deg,#0A1628 0%,#0F1F3D 50%,#0A1628 100%);}
.land-grid{position:fixed;inset:0;pointer-events:none;background-image:linear-gradient(rgba(123,97,255,.05) 1px,transparent 1px),linear-gradient(90deg,rgba(123,97,255,.05) 1px,transparent 1px);background-size:52px 52px;animation:gm 22s linear infinite;}
@keyframes gm{to{background-position:52px 52px;}}
.orb{position:fixed;border-radius:50%;filter:blur(70px);pointer-events:none;}
.o1{width:350px;height:350px;background:rgba(255,107,53,.1);top:-100px;right:-80px;animation:op 5s ease-in-out infinite;}
.o2{width:280px;height:280px;background:rgba(123,97,255,.1);bottom:-60px;left:-50px;animation:op 5s ease-in-out 2.5s infinite;}
@keyframes op{0%,100%{transform:scale(1);}50%{transform:scale(1.12);}}

.chip{display:inline-flex;align-items:center;gap:7px;background:rgba(255,107,53,.15);border:1px solid rgba(255,107,53,.35);color:var(--ac);font-size:10px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;padding:5px 14px;border-radius:99px;margin-bottom:18px;}
.chip::before{content:'';width:5px;height:5px;background:var(--ac);border-radius:50%;animation:bl 1.2s infinite;}
@keyframes bl{0%,100%{opacity:1;}50%{opacity:.2;}}

.land-title{font-family:'Syne',sans-serif;font-size:clamp(30px,9vw,52px);font-weight:800;line-height:1.05;margin-bottom:12px;}
.land-title em{font-style:normal;background:linear-gradient(135deg,var(--ac),var(--gold));-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.land-sub{font-size:14px;color:var(--mu);line-height:1.7;margin-bottom:22px;font-weight:300;}

/* Install banner */
.install-banner{display:none;background:rgba(0,212,170,.08);border:1px solid rgba(0,212,170,.25);border-radius:15px;padding:14px;margin-bottom:18px;gap:12px;align-items:center;}
.install-banner.show{display:flex;}
.ib-icon{font-size:24px;flex-shrink:0;}
.ib-text{flex:1;font-size:12px;color:var(--mu);line-height:1.5;}
.ib-text strong{color:var(--ac2);font-size:13px;display:block;margin-bottom:2px;}
.ib-btn{font-family:'Syne',sans-serif;font-size:11px;font-weight:700;background:var(--ac2);color:var(--bg);border:none;cursor:pointer;padding:8px 14px;border-radius:99px;flex-shrink:0;transition:transform .15s;}
.ib-btn:active{transform:scale(.95);}

/* Info box */
.ibox{background:var(--s1);border:1px solid var(--bd);border-radius:18px;padding:18px;margin-bottom:18px;}
.ibox-t{font-family:'Syne',sans-serif;font-size:12px;font-weight:700;color:var(--ac2);margin-bottom:12px;display:flex;align-items:center;gap:6px;}
.igrid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px;}
.icard{background:var(--s2);border-radius:11px;padding:11px;border-left:3px solid var(--ac3);}
.icard h4{font-size:10px;font-weight:700;color:var(--ac3);margin-bottom:3px;}
.icard p{font-size:10px;color:var(--mu);line-height:1.5;}
.idesc{font-size:11px;color:var(--mu);line-height:1.65;}
.idesc strong{color:var(--tx);}

/* Stats */
.stats-row{display:flex;justify-content:space-around;margin-bottom:20px;}
.stat{text-align:center;}
.stat-n{font-family:'Syne',sans-serif;font-size:24px;font-weight:800;background:linear-gradient(135deg,var(--ac2),var(--ac3));-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.stat-l{font-size:10px;color:var(--mu);margin-top:2px;}

/* Level cards */
.lev-cards{display:flex;flex-direction:column;gap:11px;margin-bottom:20px;}
.lev-card{background:var(--s1);border:1px solid var(--bd);border-radius:18px;padding:16px;cursor:pointer;transition:transform .15s;position:relative;overflow:hidden;display:flex;align-items:center;gap:13px;}
.lev-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;}
.lc-g::before{background:linear-gradient(90deg,var(--ac2),#4FC3F7);}
.lc-s::before{background:linear-gradient(90deg,var(--ac3),#FF9ECD);}
.lc-x::before{background:linear-gradient(90deg,var(--ac),var(--gold));}
.lev-card:active{transform:scale(.98);}
.lev-ico{width:50px;height:50px;border-radius:13px;display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0;}
.lc-g .lev-ico{background:rgba(0,212,170,.15);}
.lc-s .lev-ico{background:rgba(123,97,255,.15);}
.lc-x .lev-ico{background:rgba(255,107,53,.15);}
.lev-info{flex:1;min-width:0;}
.lev-name{font-family:'Syne',sans-serif;font-size:15px;font-weight:800;margin-bottom:3px;}
.lc-g .lev-name{color:var(--ac2);} .lc-s .lev-name{color:var(--ac3);} .lc-x .lev-name{color:var(--ac);}
.lev-desc{font-size:11px;color:var(--mu);line-height:1.4;margin-bottom:6px;}
.lev-pills{display:flex;gap:5px;flex-wrap:wrap;}
.lev-pill{font-size:9px;padding:2px 7px;border-radius:99px;font-weight:600;background:var(--s2);color:var(--mu);}
.lev-arr{font-size:20px;color:var(--mu);}

/* Model link */
.model-link{background:var(--s2);border:1px solid var(--bd);border-radius:13px;padding:13px 16px;cursor:pointer;display:flex;align-items:center;justify-content:space-between;color:var(--tx);font-size:13px;margin-bottom:8px;}
.model-link:active{background:var(--s3);}

/* ── GAME ── */
.hud{background:var(--s1);border-bottom:1px solid var(--bd);padding:calc(var(--sat)+10px) 16px 10px;display:flex;align-items:center;justify-content:space-between;flex-shrink:0;gap:8px;}
.hud-left{display:flex;align-items:center;gap:8px;}
.hud-info{display:flex;flex-direction:column;}
.hud-logo{font-family:'Syne',sans-serif;font-size:13px;font-weight:700;color:var(--ac);}
.hud-badge{font-size:9px;padding:2px 8px;border-radius:99px;font-weight:700;margin-top:2px;display:inline-block;width:fit-content;}
.bg-g{background:rgba(0,212,170,.15);color:var(--ac2);}
.bg-s{background:rgba(123,97,255,.15);color:var(--ac3);}
.bg-x{background:rgba(255,107,53,.15);color:var(--ac);}
.hud-right{display:flex;gap:6px;}
.hchip{background:var(--s2);border-radius:9px;padding:5px 9px;font-size:11px;font-weight:600;display:flex;align-items:center;gap:4px;}
.cg{color:var(--gold);}.ct{color:var(--ac2);}.cm{color:var(--mu);}
.prog-out{height:3px;background:var(--s2);flex-shrink:0;}
.prog-in{height:100%;transition:width .5s ease;}
.pi-g{background:linear-gradient(90deg,var(--ac2),#4FC3F7);}
.pi-s{background:linear-gradient(90deg,var(--ac3),#FF9ECD);}
.pi-x{background:linear-gradient(90deg,var(--ac),var(--gold));}

.gscroll{flex:1;overflow-y:auto;-webkit-overflow-scrolling:touch;padding:16px 16px calc(var(--sab)+80px);}
.gscroll-d{max-width:680px;margin:0 auto;display:flex;flex-direction:column;gap:14px;}

/* Scenario */
.sc-hdr{background:var(--s1);border-radius:16px;padding:16px;border:1px solid var(--bd);position:relative;overflow:hidden;}
.sc-hdr::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;}
.hg::before{background:linear-gradient(90deg,var(--ac2),#4FC3F7);}
.hs::before{background:linear-gradient(90deg,var(--ac3),#FF9ECD);}
.hx::before{background:linear-gradient(90deg,var(--ac),var(--gold));}
.sc-tag{font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;color:var(--ac);margin-bottom:7px;display:flex;align-items:center;gap:5px;}
.sc-tag::before{content:'';width:4px;height:4px;background:var(--ac);border-radius:50%;}
.sc-ttl{font-family:'Syne',sans-serif;font-size:17px;font-weight:700;margin-bottom:7px;line-height:1.3;}
.sc-sub{font-size:11px;color:var(--mu);}
.sit-box{background:rgba(123,97,255,.07);border:1px solid rgba(123,97,255,.2);border-radius:13px;padding:14px 16px;}
.sit-lbl{font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;color:var(--ac3);margin-bottom:6px;}
.sit-txt{font-size:13px;line-height:1.75;}
.q-txt{font-family:'Syne',sans-serif;font-size:15px;font-weight:700;line-height:1.4;}

/* Options */
.opts{display:flex;flex-direction:column;gap:8px;}
.opt{background:var(--s1);border:1.5px solid var(--bd);border-radius:13px;padding:13px 14px;display:flex;align-items:flex-start;gap:11px;cursor:pointer;transition:all .15s;position:relative;overflow:hidden;user-select:none;}
.opt::before{content:'';position:absolute;left:0;top:0;bottom:0;width:3px;background:transparent;transition:background .15s;}
.opt:active:not(.od){transform:scale(.99);}
.osel{border-color:rgba(255,107,53,.55)!important;background:rgba(255,107,53,.08)!important;}
.osel::before{background:var(--ac)!important;}
.ook{border-color:rgba(0,212,170,.55)!important;background:rgba(0,212,170,.08)!important;}
.ook::before{background:var(--ac2)!important;}
.ono{border-color:rgba(255,80,80,.55)!important;background:rgba(255,80,80,.06)!important;}
.ono::before{background:var(--red)!important;}
.odim{opacity:.25;}.od{cursor:default;}
.oltr{width:28px;height:28px;border-radius:8px;background:var(--s2);flex-shrink:0;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:12px;font-weight:700;color:var(--mu);transition:all .15s;}
.osel .oltr{background:var(--ac);color:#fff;}
.ook .oltr{background:var(--ac2);color:var(--bg);}
.ono .oltr{background:var(--red);color:#fff;}
.otxt{font-size:13px;line-height:1.5;padding-top:2px;}

/* Feedback */
.fb{border-radius:13px;padding:14px 16px;animation:pop .3s cubic-bezier(.34,1.56,.64,1);}
@keyframes pop{from{transform:scale(.95);opacity:0;}to{transform:scale(1);opacity:1;}}
.fbok{background:rgba(0,212,170,.09);border:1px solid rgba(0,212,170,.28);}
.fbno{background:rgba(255,80,80,.07);border:1px solid rgba(255,80,80,.23);}
.fbh{font-family:'Syne',sans-serif;font-size:14px;font-weight:700;margin-bottom:5px;}
.fbok .fbh{color:var(--ac2);}.fbno .fbh{color:var(--red);}
.fbb{font-size:12px;color:var(--mu);line-height:1.6;}
.fb-rev{margin-top:9px;padding:9px 12px;background:rgba(0,212,170,.06);border-radius:9px;border-left:3px solid var(--ac2);}
.fb-rev-l{font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;color:var(--ac2);margin-bottom:3px;}
.fb-rev-t{font-size:12px;color:var(--tx);line-height:1.5;}
.fb-th{margin-top:9px;padding:9px 12px;background:rgba(123,97,255,.07);border-radius:9px;border-left:3px solid var(--ac3);}
.fb-th-l{font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;color:var(--ac3);margin-bottom:3px;}
.fb-th-t{font-size:11px;color:var(--mu);line-height:1.55;}

/* Tip */
.tip{background:var(--s2);border-radius:10px;padding:10px 12px;font-size:11px;color:var(--mu);line-height:1.55;border-left:3px solid var(--ac2);}
.tip-t{font-weight:600;color:var(--ac2);display:block;margin-bottom:3px;}

/* Bottom action bar */
.game-bar{position:fixed;bottom:0;left:0;right:0;background:linear-gradient(to top,var(--bg) 0%,var(--bg) 65%,transparent 100%);padding:8px 16px calc(var(--sab)+12px);display:flex;gap:8px;max-width:100%;}
.btn-sub,.btn-nxt{flex:1;font-family:'Syne',sans-serif;font-size:14px;font-weight:700;padding:15px;border-radius:14px;border:none;cursor:pointer;transition:transform .12s;-webkit-tap-highlight-color:transparent;}
.btn-sub{background:linear-gradient(135deg,var(--ac),#FF8C5A);color:#fff;}
.btn-sub:disabled{opacity:.35;cursor:not-allowed;}
.btn-sub:active:not(:disabled){transform:scale(.97);}
.btn-nxt{background:linear-gradient(135deg,var(--ac),#FF8C5A);color:#fff;}
.btn-nxt:active{transform:scale(.97);}
.btn-ref{background:var(--s2);border:1px solid var(--bd);color:var(--mu);border-radius:14px;padding:15px 13px;font-size:11px;font-weight:600;border:none;cursor:pointer;white-space:nowrap;}
.btn-ref:active{background:var(--s3);}

/* XP popup */
.xppop{position:fixed;top:calc(var(--sat)+64px);right:16px;z-index:9999;background:var(--s1);border:1px solid rgba(0,212,170,.4);border-radius:11px;padding:9px 14px;font-family:'Syne',sans-serif;font-size:12px;font-weight:700;color:var(--ac2);transform:translateX(140%);transition:transform .4s cubic-bezier(.34,1.56,.64,1);pointer-events:none;box-shadow:0 4px 20px rgba(0,0,0,.4);}
.xppop.show{transform:translateX(0);}

/* ── MODELS PAGE ── */
.mod-inner{padding:16px 16px calc(var(--sab)+24px);}
.mod-sec{background:var(--s1);border:1px solid var(--bd);border-radius:18px;padding:18px;margin-bottom:14px;}
.mod-sec-hdr{display:flex;align-items:center;gap:10px;margin-bottom:14px;}
.mod-sec-ico{font-size:24px;}
.mod-sec-ttl{font-family:'Syne',sans-serif;font-size:15px;font-weight:700;}
.mod-badge{font-size:9px;padding:3px 8px;border-radius:99px;font-weight:700;margin-left:auto;}
.mod-steps{display:flex;flex-direction:column;gap:8px;}
.mod-step{display:flex;gap:10px;padding:11px;background:var(--s2);border-radius:11px;}
.ms-num{width:26px;height:26px;border-radius:7px;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:11px;font-weight:800;flex-shrink:0;}
.ms-name{font-size:12px;font-weight:600;margin-bottom:3px;}
.ms-desc{font-size:11px;color:var(--mu);line-height:1.5;}
.mod-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;}
.mod-gc{background:var(--s2);border-radius:11px;padding:12px;}
.mod-gl{font-family:'Syne',sans-serif;font-size:20px;font-weight:800;margin-bottom:3px;}
.mod-gn{font-size:11px;font-weight:600;margin-bottom:3px;}
.mod-gd{font-size:10px;color:var(--mu);line-height:1.5;}
.mod-3col{display:flex;flex-direction:column;gap:8px;}
.mod-3c{background:var(--s2);border-radius:11px;padding:12px;}
.m3ico{font-size:20px;margin-bottom:5px;}
.m3name{font-family:'Syne',sans-serif;font-size:12px;font-weight:700;margin-bottom:4px;}
.m3desc{font-size:11px;color:var(--mu);line-height:1.5;}
.m3tag{font-size:9px;padding:3px 8px;border-radius:99px;font-weight:700;display:inline-block;margin-top:6px;}
.mod-note{margin-top:12px;padding:10px 12px;background:var(--s2);border-radius:10px;font-size:11px;color:var(--mu);line-height:1.6;}
.mod-note strong{color:var(--ac2);}

/* ── RESULTS ── */
.res-bar{position:fixed;bottom:0;left:0;right:0;background:linear-gradient(to top,var(--bg) 0%,var(--bg) 65%,transparent 100%);padding:8px 16px calc(var(--sab)+12px);display:flex;gap:8px;}
.btn-rep{flex:1;font-family:'Syne',sans-serif;font-size:13px;font-weight:700;padding:14px;border-radius:13px;background:var(--s2);color:var(--tx);border:none;cursor:pointer;}
.btn-rep:active{background:var(--s3);}
.btn-home,.btn-mods{font-family:'Syne',sans-serif;font-size:13px;font-weight:700;padding:14px;border-radius:13px;background:var(--s2);color:var(--mu);border:none;cursor:pointer;}
.btn-home:active,.btn-mods:active{background:var(--s3);}

.res-hero{text-align:center;margin-bottom:22px;}
.res-trophy{font-size:60px;display:block;margin-bottom:10px;animation:bnc 1s ease;}
@keyframes bnc{0%,100%{transform:translateY(0);}50%{transform:translateY(-14px);}}
.res-title{font-family:'Syne',sans-serif;font-size:28px;font-weight:800;background:linear-gradient(135deg,var(--gold),var(--ac));-webkit-background-clip:text;-webkit-text-fill-color:transparent;margin-bottom:5px;}
.res-sub{font-size:13px;color:var(--mu);}
.res-banner{border-radius:16px;padding:14px;margin-bottom:16px;display:flex;align-items:center;gap:12px;}
.rb-g{background:rgba(0,212,170,.08);border:1px solid rgba(0,212,170,.25);}
.rb-s{background:rgba(123,97,255,.08);border:1px solid rgba(123,97,255,.25);}
.rb-x{background:rgba(255,107,53,.08);border:1px solid rgba(255,107,53,.25);}
.rb-ico{font-size:26px;}
.rb-txt{font-size:12px;color:var(--mu);line-height:1.55;}
.rb-txt strong{color:var(--tx);}
.res-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:16px;}
.rs{background:var(--s1);border:1px solid var(--bd);border-radius:13px;padding:12px;text-align:center;}
.rs-n{font-family:'Syne',sans-serif;font-size:22px;font-weight:800;margin-bottom:2px;}
.rs-l{font-size:9px;color:var(--mu);}
.res-cert{background:rgba(0,212,170,.07);border:1px solid rgba(0,212,170,.22);border-radius:13px;padding:14px;margin-bottom:14px;font-size:12px;color:var(--mu);line-height:1.65;}
.res-cert strong{color:var(--ac2);}
.res-sec{background:var(--s1);border:1px solid var(--bd);border-radius:15px;padding:16px;margin-bottom:12px;}
.res-sec-t{font-family:'Syne',sans-serif;font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:1.5px;color:var(--mu);margin-bottom:11px;}
.ch-row{display:flex;align-items:center;gap:9px;padding:7px 0;border-bottom:1px solid rgba(255,255,255,.04);}
.ch-row:last-child{border-bottom:none;}
.chi{font-size:15px;flex-shrink:0;}.chn{font-size:11px;font-weight:500;flex:1;min-width:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.chb{flex:2;height:4px;background:rgba(255,255,255,.06);border-radius:99px;overflow:hidden;}
.chf{height:100%;border-radius:99px;transition:width .6s ease;}
.chs{font-family:'Syne',sans-serif;font-size:11px;font-weight:700;flex-shrink:0;}
.rev-c{background:var(--s2);border-radius:13px;padding:13px 14px;margin-bottom:8px;border-left:3px solid var(--bd);}
.rev-ok{border-left-color:var(--ac2);}.rev-no{border-left-color:var(--red);}
.rev-hd{display:flex;justify-content:space-between;align-items:center;gap:8px;margin-bottom:6px;}
.rev-sc{font-size:10px;color:var(--mu);font-family:'Syne',sans-serif;}
.rev-bg{font-size:9px;padding:2px 8px;border-radius:99px;font-weight:600;flex-shrink:0;}
.rbok{background:rgba(0,212,170,.15);color:var(--ac2);}.rbno{background:rgba(255,80,80,.12);color:var(--red);}
.rev-q{font-size:12px;font-weight:600;margin-bottom:7px;line-height:1.4;}
.rev-opts{display:flex;flex-direction:column;gap:3px;}
.ro{padding:4px 8px;border-radius:6px;font-size:11px;display:flex;gap:6px;align-items:flex-start;}
.ro-ok{background:rgba(0,212,170,.1);color:var(--ac2);font-weight:600;}
.ro-no{background:rgba(255,80,80,.08);color:var(--red);text-decoration:line-through;opacity:.8;}
.ro-dim{opacity:.22;}.rl{font-family:'Syne',sans-serif;font-weight:700;flex-shrink:0;}
.rev-ex{margin-top:8px;font-size:10px;color:var(--mu);line-height:1.55;padding-top:8px;border-top:1px solid rgba(255,255,255,.05);}
.nlev{border-radius:15px;padding:15px;margin-bottom:14px;text-align:center;}
.nl-g{background:rgba(0,212,170,.08);border:1px solid rgba(0,212,170,.25);}
.nl-s{background:rgba(123,97,255,.08);border:1px solid rgba(123,97,255,.25);}
.nl-x{background:rgba(255,107,53,.08);border:1px solid rgba(255,107,53,.25);}
.nl-t{font-family:'Syne',sans-serif;font-size:14px;font-weight:800;margin-bottom:5px;}
.nl-s2{font-size:11px;color:var(--mu);margin-bottom:12px;line-height:1.5;}
.btn-nlev{font-family:'Syne',sans-serif;font-size:13px;font-weight:700;background:linear-gradient(135deg,var(--ac),#FF8C5A);color:#fff;border:none;cursor:pointer;padding:13px 28px;border-radius:13px;transition:transform .12s;}
.btn-nlev:active{transform:scale(.97);}
.rot-note{background:rgba(255,215,0,.06);border:1px solid rgba(255,215,0,.2);border-radius:10px;padding:10px 14px;font-size:11px;color:rgba(255,215,0,.8);display:flex;align-items:center;gap:7px;margin-bottom:12px;}

/* ── DESKTOP ENHANCEMENTS ── */
@media(min-width:768px){
  .pg{position:absolute;}
  #pg-land .scrollable .inner,#pg-models .mod-inner,#pg-res .res-inner-wrap{max-width:680px;}
  .gscroll-d{max-width:760px;}
  .igrid{grid-template-columns:repeat(4,1fr);}
  .lev-cards{flex-direction:row;gap:14px;}
  .lev-card{flex:1;flex-direction:column;align-items:flex-start;}
  .lev-arr{display:none;}
  .res-stats{grid-template-columns:repeat(4,1fr);}
  .game-bar{max-width:760px;margin:0 auto;left:50%;transform:translateX(-50%);right:auto;width:100%;}
  .res-bar{max-width:680px;margin:0 auto;left:50%;transform:translateX(-50%);right:auto;width:100%;}
  body::after{content:'';position:fixed;inset:0;background:radial-gradient(ellipse at 20% 20%,rgba(123,97,255,.04),transparent 60%),radial-gradient(ellipse at 80% 80%,rgba(255,107,53,.04),transparent 60%);pointer-events:none;}
}
</style>
</head>
<body>
<div class="xppop" id="xppop">⚡ +80 XP!</div>

<!-- ══════════════════════════════════
     LANDING
══════════════════════════════════ -->
<div id="pg-land" class="pg on">
  <div class="scrollable">
    <div class="land-grid"></div>
    <div class="orb o1"></div><div class="orb o2"></div>
    <div class="inner" style="position:relative;z-index:1">
      <div class="chip">🎮 PWA · Offline · Mobil & Masaüstü</div>
      <h1 class="land-title">Değişim<br><em>Liderliği</em><br>Akademisi</h1>
      <p class="land-sub">Kotter, ADKAR ve Lewin modellerini 100 gerçek senaryo sorusuyla öğren. Ana ekrana ekle, offline oyna.</p>

      <div class="install-banner" id="installBanner">
        <div class="ib-icon">📲</div>
        <div class="ib-text"><strong>Uygulamayı Yükle</strong>Ana ekrana ekle — internet olmadan da çalışır.</div>
        <button class="ib-btn" onclick="installPWA()">Yükle</button>
      </div>

      <div class="ibox">
        <div class="ibox-t">🎮 Platform Hakkında</div>
        <div class="igrid">
          <div class="icard"><h4>🎯 Nasıl Oynanır?</h4><p>Senaryo oku, karar ver. Her oyunda sorular karışır.</p></div>
          <div class="icard"><h4>🔄 100 Soru Havuzu</h4><p>Her oyunda farklı 10 soru. Sonsuz tekrar imkânı.</p></div>
          <div class="icard"><h4>❌ Hata Açıklaması</h4><p>Yanlış cevaplarda doğru yanıt + model referansı gösterilir.</p></div>
          <div class="icard"><h4>📴 Tam Offline</h4><p>Bir kez yükle, internet olmadan oyna. Tam PWA.</p></div>
        </div>
        <p class="idesc"><strong>3 seviye:</strong> Giriş · Orta · Ustalık — Her seviyede 10 soru, toplam <strong>100 soruluk havuz</strong>.</p>
      </div>

      <div class="stats-row">
        <div class="stat"><div class="stat-n">100</div><div class="stat-l">Soru Havuzu</div></div>
        <div class="stat"><div class="stat-n">3</div><div class="stat-l">Seviye</div></div>
        <div class="stat"><div class="stat-n">3</div><div class="stat-l">Model</div></div>
        <div class="stat"><div class="stat-n">📴</div><div class="stat-l">Offline</div></div>
      </div>

      <div class="lev-cards">
        <div class="lev-card lc-g" onclick="startLevel('g')">
          <div class="lev-ico">🌱</div>
          <div class="lev-info">
            <div class="lev-name">Giriş</div>
            <div class="lev-desc">Temel kavramlar, model tanımları ve ilk uygulama senaryoları.</div>
            <div class="lev-pills"><span class="lev-pill">10 Soru</span><span class="lev-pill">~10 dk</span><span class="lev-pill">34 Soruluk Havuz</span></div>
          </div>
          <div class="lev-arr">›</div>
        </div>
        <div class="lev-card lc-s" onclick="startLevel('s')">
          <div class="lev-ico">⚡</div>
          <div class="lev-info">
            <div class="lev-name">Orta</div>
            <div class="lev-desc">Kurumsal senaryolar, koalisyon, direnç ve vizyon yönetimi.</div>
            <div class="lev-pills"><span class="lev-pill">10 Soru</span><span class="lev-pill">~15 dk</span><span class="lev-pill">33 Soruluk Havuz</span></div>
          </div>
          <div class="lev-arr">›</div>
        </div>
        <div class="lev-card lc-x" onclick="startLevel('x')">
          <div class="lev-ico">🔥</div>
          <div class="lev-info">
            <div class="lev-name">Ustalık</div>
            <div class="lev-desc">Çok katmanlı kriz, model sentezi ve stratejik liderlik.</div>
            <div class="lev-pills"><span class="lev-pill">10 Soru</span><span class="lev-pill">~20 dk</span><span class="lev-pill">33 Soruluk Havuz</span></div>
          </div>
          <div class="lev-arr">›</div>
        </div>
      </div>

      <div class="model-link" onclick="goModels()">
        <span>📖 Model Rehberi: Kotter · ADKAR · Lewin</span>
        <span style="color:var(--ac)">›</span>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════
     GAME
══════════════════════════════════ -->
<div id="pg-game" class="pg">
  <div class="hud">
    <div class="hud-left">
      <button class="back-btn" onclick="goHome()">‹</button>
      <div class="hud-info">
        <div class="hud-logo">Değişim Akademisi</div>
        <div class="hud-badge" id="hudBadge">🌱 Giriş</div>
      </div>
    </div>
    <div class="hud-right">
      <div class="hchip">⭐ <span class="cg" id="hScore">0</span></div>
      <div class="hchip">⚡ <span class="ct" id="hXP">0</span></div>
      <div class="hchip cm" id="hPhase">1/10</div>
    </div>
  </div>
  <div class="prog-out"><div class="prog-in" id="progBar" style="width:0%"></div></div>
  <div class="gscroll" id="gscroll">
    <div class="gscroll-d" id="gscrollD"></div>
  </div>
  <div class="game-bar" id="gameBar">
    <button class="btn-ref" onclick="goModels()">📖</button>
    <button class="btn-sub" id="btnSub" onclick="submitAnswer()" disabled>Cevabı Gönder ✓</button>
  </div>
</div>

<!-- ══════════════════════════════════
     MODEL REHBERİ
══════════════════════════════════ -->
<div id="pg-models" class="pg">
  <div class="topbar">
    <button class="back-btn" onclick="goBack()">‹</button>
    <div class="topbar-title">📖 Model Rehberi</div>
  </div>
  <div class="scrollable">
    <div class="mod-inner">

      <div class="mod-sec">
        <div class="mod-sec-hdr">
          <div class="mod-sec-ico">🔄</div>
          <div><div class="mod-sec-ttl">Kotter'ın 8 Adım Modeli</div><div style="font-size:10px;color:var(--mu)">Harvard Business School — Kurumsal değişim</div></div>
          <span class="mod-badge" style="background:rgba(255,107,53,.15);color:var(--ac)">Kurumsal</span>
        </div>
        <div class="mod-steps">
          <div class="mod-step"><div class="ms-num" style="background:rgba(255,107,53,.2);color:var(--ac)">1</div><div><div class="ms-name">Aciliyet Duygusu Yarat</div><div class="ms-desc">Pazar verileri ve rakip analiziyle "neden şimdi?" sorusunu somutlaştır. Yönetimin %75'ini ikna et.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(255,107,53,.2);color:var(--ac)">2</div><div><div class="ms-name">Güçlü Koalisyon Kur</div><div class="ms-desc">Üst + orta yönetim + informal liderler. Her katmandan "change champion" dahil et.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(255,107,53,.2);color:var(--ac)">3</div><div><div class="ms-name">Vizyon ve Strateji Geliştir</div><div class="ms-desc">5 dakikada anlatılabilen, ilham verici vizyon. SMART hedeflerle yol haritası.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(255,107,53,.2);color:var(--ac)">4</div><div><div class="ms-name">Vizyonu İlet</div><div class="ms-desc">Her fırsatta tutarlı iletişim. Yönetici davranışları mesaj taşır. Söylem-eylem çelişkisi öldürücü.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(0,212,170,.2);color:var(--ac2)">5</div><div><div class="ms-name">Geniş Tabanlı Harekete Geç</div><div class="ms-desc">Engelleri kaldır. Çalışanlara değişimi hayata geçirme yetkisi ver.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(0,212,170,.2);color:var(--ac2)">6</div><div><div class="ms-name">Kısa Vadeli Kazanımlar Üret</div><div class="ms-desc">6-18 ayda görünür başarılar planla. Şüphecileri somut kanıtla ikna et.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(0,212,170,.2);color:var(--ac2)">7</div><div><div class="ms-name">Kazanımları Pekiştir</div><div class="ms-desc">Kutla ama rahatlamadan devam et. Değişimi derinleştir ve genişlet.</div></div></div>
          <div class="mod-step"><div class="ms-num" style="background:rgba(0,212,170,.2);color:var(--ac2)">8</div><div><div class="ms-name">Değişimi Kültüre İşle</div><div class="ms-desc">İşe alım, terfi, performans ve ödül sistemlerine entegre et. Kültüre kazınmadan kalıcı olmaz.</div></div></div>
        </div>
      </div>

      <div class="mod-sec">
        <div class="mod-sec-hdr">
          <div class="mod-sec-ico">🎯</div>
          <div><div class="mod-sec-ttl">ADKAR Modeli</div><div style="font-size:10px;color:var(--mu)">Prosci / Jeff Hiatt — Bireysel odak</div></div>
          <span class="mod-badge" style="background:rgba(0,212,170,.15);color:var(--ac2)">Bireysel</span>
        </div>
        <div class="mod-grid">
          <div class="mod-gc"><div class="mod-gl" style="color:var(--ac)">A</div><div class="mod-gn">Awareness</div><div class="mod-gd">"Neden değişmeliyiz?" — İlk engel. Farkındalık olmadan istek oluşmaz.</div></div>
          <div class="mod-gc"><div class="mod-gl" style="color:var(--ac3)">D</div><div class="mod-gn">Desire</div><div class="mod-gd">"Ben de istiyorum." Motivasyon ve sahiplenme; zorlanamaz.</div></div>
          <div class="mod-gc"><div class="mod-gl" style="color:var(--ac2)">K</div><div class="mod-gn">Knowledge</div><div class="mod-gd">"Nasıl yapacağımı biliyorum." Eğitim ve rehberlik gerekir.</div></div>
          <div class="mod-gc"><div class="mod-gl" style="color:var(--gold)">A</div><div class="mod-gn">Ability</div><div class="mod-gd">"Yapabiliyorum." Bilgiyi uygulamaya döküş; koçlukla gelişir.</div></div>
          <div class="mod-gc" style="grid-column:1/-1"><div class="mod-gl" style="color:#FF9ECD">R</div><div class="mod-gn">Reinforcement</div><div class="mod-gd">"Sürdürüyorum." Ödüller ve hesap verebilirlik olmadan eski alışkanlıklar geri döner.</div></div>
        </div>
        <div class="mod-note"><strong>💡 Kritik:</strong> ADKAR doğrusaldır. Kırılma noktasını tespit et, orada müdahale et. Bilgi vermek isteksiz kişiyi değiştirmez.</div>
      </div>

      <div class="mod-sec" style="margin-bottom:24px">
        <div class="mod-sec-hdr">
          <div class="mod-sec-ico">❄️</div>
          <div><div class="mod-sec-ttl">Lewin'in 3 Aşamalı Modeli</div><div style="font-size:10px;color:var(--mu)">Kurt Lewin, 1947 — Temel değişim teorisi</div></div>
          <span class="mod-badge" style="background:rgba(123,97,255,.15);color:var(--ac3)">Temel</span>
        </div>
        <div class="mod-3col">
          <div class="mod-3c"><div class="m3ico">❄️</div><div class="m3name" style="color:var(--ac2)">Çözme (Unfreezing)</div><div class="m3desc">Mevcut durumun analizi. Eski alışkanlıkların yetersizliği kanıtlanır. Güvenli bırakma ortamı sağlanır.</div><span class="m3tag" style="background:rgba(0,212,170,.1);color:var(--ac2)">Hazırlık</span></div>
          <div class="mod-3c"><div class="m3ico">🔄</div><div class="m3name" style="color:var(--ac3)">Değiştirme (Changing)</div><div class="m3desc">Yeni davranışlar hayata geçirilir. Belirsizlik en yüksek dönem. Yoğun iletişim ve destek şart.</div><span class="m3tag" style="background:rgba(123,97,255,.1);color:var(--ac3)">Uygulama</span></div>
          <div class="mod-3c"><div class="m3ico">🔒</div><div class="m3name" style="color:var(--ac)">Dondurma (Refreezing)</div><div class="m3desc">Yeni davranışlar KPI, ödül ve kültüre entegre edilir. Olmadan geri kayma kaçınılmazdır.</div><span class="m3tag" style="background:rgba(255,107,53,.1);color:var(--ac)">Kalıcılık</span></div>
        </div>
        <div class="mod-note"><strong>💡 Kritik:</strong> En çok atlanan adım "dondurma"dır. Sistem entegrasyonu yapılmadan değişim kalıcı olmaz.</div>
      </div>

    </div>
  </div>
</div>

<!-- ══════════════════════════════════
     RESULTS
══════════════════════════════════ -->
<div id="pg-res" class="pg">
  <div class="scrollable">
    <div class="inner res-inner-wrap" id="resInner" style="padding-bottom:calc(var(--sab) + 90px)"></div>
  </div>
  <div class="res-bar">
    <button class="btn-rep" onclick="replaySame()">🔄 Tekrar (Yeni Sorular)</button>
    <button class="btn-mods" onclick="goModels()">📖</button>
    <button class="btn-home" onclick="goHome()">🏠</button>
  </div>
</div>

<script>
const POOL_G=[
{ch:0,sc:'RetailTR — Dijital Adım',sit:'Orta ölçekli perakende şirketinde CEO dijitale geçmek istiyor. Kimse ne yapacağını bilmiyor.',q:"Kotter'ın 8 Adım Modeli'ne göre ilk yapılması gereken nedir?",opts:['Hemen yazılım satın al.','Pazar verisi ve rakip analizi ile aciliyet duygusu oluştur.','Tüm çalışanlara e-posta gönder.','Pilot ekip kur.'],correct:1,ok:"Kotter'ın 1. adımı 'Aciliyet Duygusu Yaratmak'tır. Somut veri olmadan kimse harekete geçmez.",no:'Satın alma veya duyuru erken adımlardır. Önce neden değişilmesi gerektiği hissettirilmeli.',theory:"Kotter Adım 1: Yönetimin %75'i 'değişmemek daha tehlikeli' diye hissetmeden sonraki adımlar boşlukta kalır.",comp:'Vizyon',xp:80},
{ch:0,sc:'TechRise — Vizyon Belgesi',sit:'Şirketin değişim vizyonu 12 sayfalık belgede yazılı. Çalışanlar okumamış.',q:"Kotter'a göre etkili bir vizyonun temel özelliği nedir?",opts:['Ayrıntılı ve kapsamlı olmalı.','5 dakikada anlatılabilir, somut, ilham verici olmalı.','Yalnızca sayısal hedeflerden oluşmalı.','Üst yönetim oluşturup sunmalı.'],correct:1,ok:"Vizyon 'asansör testi'ni geçmeli; 5 dakikada anlatılabilir ve 'ben de istiyorum' hissi uyandırmalı.",no:'Uzun belgeler okunmaz. Kısa, net, ilham verici vizyon gerekir.',theory:"Kotter Adım 3: '30 dakikada anlatılamıyorsa yeterince netleştirilmemiştir.'",comp:'Vizyon',xp:80},
{ch:0,sc:'StartUp360 — Koalisyon',sit:'CEO değişimi destekliyor ama ekip müdürleri ilgisiz. Çalışanlar müdürlerine bakarak yön belirliyor.',q:"Kotter'ın hangi adımı ihmal edildi?",opts:['Adım 1 — Aciliyet Duygusu','Adım 2 — Koalisyon Kurma','Adım 3 — Vizyon Geliştirme','Adım 6 — Kısa Vadeli Kazanım'],correct:1,ok:'Kotter Adım 2: CEO yeterli değil; orta yönetim koalisyona dahil edilmeli.',no:'CEO desteği gerekli ama yeterli değil. Orta yönetim değişimi aşağıya taşır.',theory:'Kotter Adım 2: Koalisyon teknik uzmanlık, kıdem ve informal etki sahibi kişilerden oluşmalı.',comp:'İletişim',xp:80},
{ch:0,sc:'HealthFirst — Sessizlik Riski',sit:"Hastane büyük yapısal değişim planlıyor. Söylentiler yayılıyor. Yönetim 'hazır olmadan konuşmayalım' diyor.",q:'Bu yaklaşımın riski ve doğru adım nedir?',opts:['Risk yok; hazır olunca konuşulur.',"Sessizlik belirsizlik yaratır; proaktif iletişimle 'şu an bildiğimiz şu' mesajı verilmeli.",'Yalnızca üst yönetim bilgilendirilmeli.','Söylentiler kendiliğinden dağılır.'],correct:1,ok:'İletişim boşlukları söylentiyle dolar. Dürüst kısmi iletişim güveni korur.',no:'Sessizlik güvensizlik üretir. Kotter Adım 4 proaktif iletişimi zorunlu kılar.',theory:'Kotter Adım 4: Değişim iletişiminde mükemmel bilgi beklenmez; sık, tutarlı, dürüst iletişim şart.',comp:'İletişim',xp:80},
{ch:0,sc:'LogiStar — Neden Sorusu',sit:"Fabrika müdürü değişimi duyurdu. 3 hafta sonra çalışanlar hâlâ 'Bu bizi neden etkiler?' diyor.",q:'ADKAR modelinde hangi basamak eksik?',opts:['Ability','Knowledge','Reinforcement','Awareness'],correct:3,ok:"'Neden bizi etkiler?' sorusu Farkındalık (Awareness) eksikliğine işaret eder.",no:'Değişimin bireysel etkisi anlaşılmamışsa Awareness basamağı kurulmamış demektir.',theory:'ADKAR-A: Değişimin nedenini ve kişisel etkisini anlamak birinci basamaktır; atlanırsa geri kalanlar işlemez.',comp:'Analiz',xp:80},
{ch:0,sc:'EduNet — Bilgi Açığı',sit:"Yeni öğrenim yönetim sistemi uygulandı. Öğretmenler 'Nasıl kullanacağız?' diye soruyor.",q:'ADKAR modelinde hangi basamak eksik?',opts:['Awareness','Desire','Knowledge','Reinforcement'],correct:2,ok:"'Nasıl?' sorusu Knowledge (Bilgi) eksikliğidir.",no:'Farkındalık ve istek yerinde ama nasıl yapılacağı bilinmiyor; bu Knowledge sorunudur.',theory:'ADKAR-K: Eğitim, süreç dokümantasyonu ve uygulamalı pratik bu basamağı karşılar.',comp:'Analiz',xp:80},
{ch:0,sc:'FinCorp — ERP Direnci',sit:'ERP güncellemesi için eğitimler yapıldı. Çalışanlar yine de eski sistemi kullanıyor.',q:'ADKAR modelinde asıl sorun hangi basamakta?',opts:['Knowledge','Awareness','Desire','Reinforcement'],correct:2,ok:'Bilgi var ama istek (Desire) yok. Motivasyon ve sahiplenme sorunu.',no:'Eğitim aldılar yani Knowledge var. Eski sistemi kullanmak Desire eksikliğini gösterir.',theory:'ADKAR-D: Bilgi vermek isteksiz kişiyi değiştirmez; motivasyon ve bireysel kazanım anlatılmalı.',comp:'Analiz',xp:80},
{ch:0,sc:'ManufaCo — Eski Kalıp',sit:'Üretim hattı robotik sisteme geçecek. Mühendisler eski prosedürlerini bırakmak istemiyor.',q:'Lewin modelinin hangi aşamasında çalışılmalı?',opts:['Changing','Refreezing','Unfreezing','Hiçbirinde; direnç görmezden gelinmeli.'],correct:2,ok:'Eski alışkanlıkların çözülmesi Lewin Unfreezing aşamasıdır.',no:'Eski kalıpları kırmadan yeni kalıplar kurulamaz; Unfreezing atlandı.',theory:"Lewin — Çözme: Mevcut durumun yetersizliği kanıtlanır ve çalışanlar için güvenli bir bırakma ortamı sunulur.",comp:'Analiz',xp:80},
{ch:1,sc:'GlobalEdu — Geri Dönüş',sit:'Okul zinciri yeni değerlendirme sistemini uyguladı. 6. ayda öğretmenler eski yöntemlere döndü.',q:'Lewin modelinde hangi aşama ihmal edildi?',opts:['Unfreezing','Changing','Refreezing','Hepsi doğru uygulandı.'],correct:2,ok:'Geri dönüş Refreezing ihmalini gösterir; yeni davranışlar sisteme entegre edilmedi.',no:'Değişim uygulandı ama pekiştirilmedi; Refreezing olmadan geri kayma kaçınılmazdır.',theory:'Lewin — Dondurma: Yeni davranışlar performans kriterleri ve kültür normlarına entegre edilmeden kalıcı olmaz.',comp:'Sürdürülebilirlik',xp:80},
{ch:1,sc:'AutoTech — Pekiştirme',sit:'Mühendisler yeni metodoloji öğrendi. Ancak performans formu eski kriterleri ölçüyor.',q:'ADKAR hangi son basamağı eksik?',opts:['Awareness','Desire','Ability','Reinforcement'],correct:3,ok:'Ödül sistemi eski davranışı ölçüyorsa Reinforcement basamağı eksiktir.',no:'Bilgi ve yetenek var; eski ölçütlerin korunması Reinforcement ihmalini gösterir.',theory:'ADKAR-R: Ödüller ve performans kriterleri yeni davranışı desteklemezse eski alışkanlıklar geri döner.',comp:'Sürdürülebilirlik',xp:80},
{ch:1,sc:'FinancePro — Koalisyon',sit:'Finans şirketinde risk yönetim sistemi değişiyor. CEO destekliyor, orta düzey yöneticiler sessiz.',q:'Değişim koalisyonu için önce ne yapılmalı?',opts:['Yalnızca CEO ile çalış.','Tüm çalışanlara açık toplantı yap.','Etkili orta düzey yöneticileri belirle ve kazanmaya çalış.','Değişimi danışmana devret.'],correct:2,ok:"Etkili koalisyonlar 'change champion' orta yöneticilerden de oluşur; bunlar değişimi aşağıya taşır.",no:'CEO desteği gerekli ama yeterli değil; orta yönetim dahil edilmeden değişim yüzer.',theory:"Kotter Adım 2: Koalisyon yalnızca tepe değil, örgütün kilit noktalarındaki isimleri kapsamalı.",comp:'İletişim',xp:80},
{ch:1,sc:'TechGroup — Kutlama',sit:'IT dönüşümünün 6. ayında ekipler başarılı sonuç aldı. Yönetim "Vakit yok, kutlamaya gerek yok" diyor.',q:'Bu tutumun riski nedir?',opts:['Risk yok; kutlama zaman kaybıdır.','Kutlanmama motivasyonu düşürür ve şüphecileri ikna fırsatını kaçırır.','Kutlama yalnızca tamamlanmış projelerde yapılır.','Küçük kazanımları kutlamak güvenilirliği zayıflatır.'],correct:1,ok:'Kotter Adım 6: Kazanımlar değişimin mümkün olduğunun kanıtı; kutlanmadan geçilmesi momentum kaybettirir.',no:'Kutlamalar stratejik araçtır; şüphecileri somut kanıtla ikna eden en güçlü mekanizmadır.',theory:'Kotter Adım 6: Planlı görünür ve değişimle açıkça ilişkili kazanımlar seçilip duyurulmalı.',comp:'Liderlik',xp:80},
{ch:1,sc:'CityBank — İletişim',sit:"Banka şubeleri merkezileşiyor. Söylentiler yayıldı. Üst yönetim 'Plan netleşmeden açıklama yapmayalım' diyor.",q:'Doğru iletişim stratejisi nedir?',opts:['Belirsizliği korumak daha sağlıklı.',"Gecikmeli iletişim söylentiyi güçlendirir; 'şu an bildiğimiz şudur' mesajıyla başlanmalı.",'Yalnızca şube müdürlerine açıklama yapılmalı.','Söylentileri araştır, başka bir şey yapma.'],correct:1,ok:'Kısmi dürüst iletişim güveni korur; sessizlik daha büyük söylenti üretir.',no:'Mükemmel bilgi beklenmez; dürüst sık tutarlı iletişim en kötü senaryoyu da yönetir.',theory:'Kotter Adım 4: İletişim boşluğu söylentiyle dolar. Proaktif mesaj belirsizliği yönetir.',comp:'İletişim',xp:80},
{ch:2,sc:'ConsumeCo — Eski Davranış',sit:'6 ay önce başlatılan müşteri deneyimi programı ivme kaybetti; çalışanlar eski davranışlara döndü.',q:"Lewin 'Refreezing' nasıl uygulanmalı?",opts:['Programı kapatıldı ilan et.',"Yeni davranışları KPI'lara, ödüllere ve işe alım kriterlerine entegre et.",'Yalnızca hatırlatma e-postası gönder.','Bir daha değişim projesi başlatma.'],correct:1,ok:'Refreezing yeni davranışların sistemlere ve kültüre kazınmasıdır.',no:'Sistem entegrasyonu yapılmadan davranış değişmez; e-posta yüzeysel bir araçtır.',theory:'Lewin — Dondurma: KPI ödül ve işe alım kriterleri güncellenmezse eski alışkanlıklar geri döner.',comp:'Sürdürülebilirlik',xp:80},
{ch:2,sc:'ManuTech — Sabotaj',sit:"Otomotiv firmasında kalite sistemi uygulanıyor. Fabrika müdürü toplantılarda destekliyor ama çalışanlara 'Bu da geçer' diyor.",q:'Bu davranış hangi Kotter adımını baltalıyor?',opts:['Adım 1 — Aciliyet','Adım 4 — Vizyonu İlet','Adım 3 — Vizyon Geliştir','Adım 8 — Kültüre Entegre'],correct:1,ok:'Adım 4: Yöneticinin davranışları söyleminden güçlü mesaj taşır; çelişki güveni yok eder.',no:'İletişim yalnızca sözel değil; yönetici davranışları en güçlü mesaj taşıyıcısıdır.',theory:"Kotter Adım 4: Yönetici 'yürüyen örnek' olmak zorunda. Söylem-eylem çelişkisi tüm değişim iletişimini geçersiz kılar.",comp:'İletişim',xp:80},
{ch:2,sc:'HealthNet — Akran Öğretimi',sit:"Hemşireler 'Doktorlar benimsemeden biz benimseyemeyiz' diyor. Doktorlar 'İş akışımıza uymaz' diyor.",q:'Bu döngüsel direnci kırmak için ne yapılmalı?',opts:['Önce hemşireleri eğit.',"Kilit doktorları 'süper kullanıcı' yap; akran öğretimi modeli kur ve iş akışı özelleştirmeye ortak et.",'Her iki gruba zorunlu kullanım şartı getir.','Sistemi iki ayrı versiyonla sun.'],correct:1,ok:"Akran öğretimi döngüsel direnci kırar; doktorların 'sahibi' haline geldiği sistem dirençten çıkar.",no:'Yönetim baskısı uyum getirir, benimseme değil. Akranlar arası güven tabanlı öğrenme kalıcıdır.',theory:"ADKAR Ability + Desire: Akran öğretimi hem beceri hem motivasyon sağlar. 'Benim gibi biri kullanıyor' mesajı en güçlü Desire tetikleyicisidir.",comp:'Direnç Yönetimi',xp:80},
{ch:2,sc:'BuildCo — Kültür ve Sistem',sit:'İnşaat firması güvenlik kültürü değişimi başlattı. Yönetim eğitimler yaptı ama saha davranışı değişmedi.',q:'Eğitim yeterli olmadığında bir sonraki adım nedir?',opts:['Daha fazla eğitim ver.','Güvenlik davranışını performans değerlendirme ve terfi kriterlerine entegre et.','Dışarıdan güvenlik müdürü getir.','Ceza sistemini ağırlaştır.'],correct:1,ok:'Kültür eğitimle değil, sistemlerle değişir; KPI ve terfi kriterleri yeni davranışı kalıcı kılar.',no:'Eğitim bilgi verir; sisteme entegrasyon davranışı değiştirir.',theory:'Kotter Adım 8: Yeni davranış işe alım, terfi, performans ve ödül sistemlerine kazınmadan kültür değişmez.',comp:'Değişim Yönetimi',xp:80},
{ch:2,sc:'RetailX — Vizyon Bağlantısı',sit:'Perakende zincirinde vizyon var ama çalışanlar günlük işleriyle bağlantı kuramıyor.',q:'Vizyon-rol bağlantısı nasıl kurulur?',opts:['Vizyonu daha büyük posterlere bas.','Her departman için vizyonun kendi rolüne nasıl bağlandığını kaskad hedeflerle somutlaştır.','CEO video mesajı yayınlasın.','Vizyonu her toplantıda tekrarla.'],correct:1,ok:'Kaskad hedefleme bireysel rolü vizyona bağlar.',no:'Poster veya tekrar yüzeysel. Her çalışanın kendi iş bağlamında anlam üretmesi gerekir.',theory:'Kotter Adım 4 + ADKAR Awareness: Vizyon bireysel anlam üretmeden motivasyon sağlayamaz.',comp:'Vizyon',xp:80},
{ch:0,sc:'TelcoTR — ADKAR Sırası',sit:'Telekom şirketi yeni CRM sistemine geçti. Çalışanlar eğitim aldı ama uygulamıyor.',q:"ADKAR'da doğru müdahale sırası hangisidir?",opts:['Knowledge → Ability → Reinforcement','Awareness → Desire → Knowledge → Ability → Reinforcement','Desire → Awareness → Knowledge','Reinforcement → Awareness → Desire'],correct:1,ok:'ADKAR doğrusal bir modeldir; sıra değişmez ve her basamak bir öncekinin üzerine inşa edilir.',no:'ADKAR sırası önemlidir; herhangi bir basamak atlanırsa model çalışmaz.',theory:'ADKAR: Her basamak bir önkoşuldur. Awareness olmadan Desire, Desire olmadan Knowledge işe yaramaz.',comp:'Analiz',xp:80},
{ch:1,sc:'PharmaGroup — Teknik Direnç',sit:"İlaç firmasında laboratuvar sistemi değişiyor. Araştırmacılar 'Veri bütünlüğünü bozar' diyerek direniyor.",q:'Teknik direnci aşmak için ne yapılmalı?',opts:['Eski sisteme erişimi kes.','Araştırmacıların endişelerini pilot ve test raporu ile yanıtla; onları teknik karar ortağı yap.','Yönetim kararı olduğunu vurgula.','Daha fazla eğitim ver.'],correct:1,ok:'Teknik itirazlar teknik kanıtla çözülür; araştırmacıları ortağa dönüştürmek savunuculuk üretir.',no:'Zorlama uyum üretir, benimseme değil. Ortaklık direnci en aza indirir.',theory:'ADKAR-D + Kotter Adım 5: Teknik uzmanları sürecin tasarımına dahil etmek hem direnç giderir hem kalite artırır.',comp:'Direnç Yönetimi',xp:80},
{ch:1,sc:'EduGroup — Sendika',sit:'Okul zinciri yeni ölçme sistemi kuruyor. Sendika kararlı biçimde karşı çıkıyor.',q:'Sendika ile ilişkiyi nasıl yönetmeli?',opts:['Yasal zorunluluk olarak dayat.','Erken aşamada temsilcileri sürece ortak et ve kaygılarını tasarıma yansıt.','Değişimi gizlice uygula.','Sendikayı görmezden gel.'],correct:1,ok:'Paydaşları erken dahil etmek direnci sahiplenmeye dönüştürür.',no:'Baskı uyum getirir, benimseme değil. Ortak tasarım direnci kırar.',theory:'Kotter Adım 5: Paydaşları erken dahil etmek engelleri kaldırmanın en güçlü yoludur.',comp:'Paydaş Yönetimi',xp:80},
{ch:2,sc:'InsurCo — ADKAR Pekiştirme',sit:'Sigorta şirketinde yeni süreç 1 yıldır uygulanıyor. Çalışanlar doğru yapıyor ama ara ara eski alışkanlıklara dönüyor.',q:"Kalıcılığı sağlamak için ADKAR'ın hangi basamağı güçlendirilmeli?",opts:['Awareness','Desire','Knowledge','Reinforcement'],correct:3,ok:'Ara sıra geri dönüş Reinforcement mekanizmalarının zayıflığını gösterir.',no:'Bilgi yetenek ve istek var; sorun pekiştirme mekanizmalarındadır.',theory:'ADKAR-R: Ödüller, tanıma ve hesap verebilirlik mekanizmaları yeni davranışı kalıcı kılar.',comp:'Sürdürülebilirlik',xp:80},
{ch:0,sc:'BankFirst — Aciliyet Testi',sit:'Yönetim kurulu değişimi onayladı ama çalışanlar neden değişildiğini anlamıyor.',q:'Eksik olan Kotter adımı hangisidir?',opts:['Adım 5 — Harekete Geç','Adım 3 — Vizyon','Adım 1 — Aciliyet Yarat','Adım 8 — Kültür'],correct:2,ok:'Çalışanlar değişimin nedenini anlayamıyorsa Aciliyet Duygusu çalışanlara iletilmemiştir.',no:'Yönetim kurulu onayı yeterli değil; çalışan düzeyinde de aciliyet hissi oluşturulmalı.',theory:'Kotter Adım 1: Aciliyet yalnızca tepede değil, örgütün her katmanında hissedilmelidir.',comp:'Vizyon',xp:80},
{ch:1,sc:'LogiNet — Refreezing',sit:'Lojistik firma süreç iyileştirmeyi tamamladı. 8 ay sonra eski süreçler geri döndü.',q:'Lewin modelinde hangi adım atlandı?',opts:['Unfreezing','Changing','Refreezing','Hiçbiri atlanmadı.'],correct:2,ok:"Geri dönüş Refreezing ihmalinin göstergesi; yeni davranışlar KPI ve prosedürlere entegre edilmedi.",no:'Başarılı uygulama sonrası geri dönüş klasik Refreezing ihmalinin sonucudur.',theory:'Lewin — Refreezing: Yeni davranışı destekleyen yapısal mekanizmalar kurulmadan değişim geçici kalır.',comp:'Sürdürülebilirlik',xp:80},
{ch:2,sc:'AgroTech — Bireysel Anlam',sit:"Tarım teknolojileri şirketinde vizyon var ama saha çalışanları 'Bu beni nasıl etkiler?' soruyor.",q:'Bu boşluğu kapatmak için ne yapılmalı?',opts:['Vizyonu daha sık tekrarla.',"Vizyon-rol bağlantısı kur: Her çalışan için 'sen bu değişimde ne yapacaksın?' sorusunu yanıtla.",'Vizyonu değiştir.','Yalnızca yöneticileri bilgilendir.'],correct:1,ok:'Vizyon bireysel anlam taşımıyorsa motivasyon oluşmaz.',no:'Tekrar yüzeysel çözümdür; bireysel bağlantı kurulmadan vizyon boş kalır.',theory:'ADKAR Awareness + Kotter Adım 4: Bireysel bağlantı kurulamayan vizyon teoride kalır.',comp:'Vizyon',xp:80},
{ch:0,sc:'DigitalHR — Hız Baskısı',sit:"İK müdürü 'Rakipler 6 ayda dönüştü, Kotter çok yavaş, bazı adımları atlayalım' diyor.",q:'Bu yaklaşım doğru mu?',opts:['Evet; acil durumda model atlanır.','Hayır; adımlar atlanamaz ama paralel yürütülerek hız artırılabilir.','Evet; en az 3 adım atlanabilir.','Hayır; her adım en az 3 ay sürmeli.'],correct:1,ok:'Adımlar birbirinin önkoşuludur; atlamak değil paralel çalıştırmak hız üretir.',no:'Kotter adımları zorunlu önkoşullardur. Atlamak kısa vade hız, uzun vade başarısızlık üretir.',theory:'Kotter Hızlandırılmış Uygulama: Adımlar iç içe yürütülebilir; atlamak değil, paralel çalıştırmak doğru.',comp:'Değişim Yönetimi',xp:80},
{ch:1,sc:'LogiGroup — Lewin Changing',sit:'Lojistik firması Unfreezing aşamasını başarıyla tamamladı. Şimdi Changing aşamasındalar.',q:"Lewin'in Changing aşamasında en kritik unsur nedir?",opts:['Hız; değişimi mümkün olduğunca hızlı tamamla.','Sürekli iletişim ve destek; belirsizlik en yüksek bu dönemde.','Tüm değişimi tek seferde uygula.','Direnci cezayla bastır.'],correct:1,ok:'Changing aşamasında belirsizlik ve direnç en yüksektir; sürekli iletişim ve destek şarttır.',no:'Hız tek başına yeterli değil; çalışanların belirsizliği yönetebilmesi için destek zorunlu.',theory:"Lewin — Değiştirme: Geçiş döneminde yoğun iletişim, koçluk ve hata yapma özgürlüğü gerekir.",comp:'İletişim',xp:80},
{ch:2,sc:'EduTech — İyileştirme',sit:'E-öğrenme platformu kullanımda. Bazı modüllerde düşüş var.',q:'Sürekli iyileştirme kültürü için ne yapılmalı?',opts:['Düşen modülleri kaldır.','Geri bildirim ve veriyi düzenli incele; iyileştirme döngüsü kur.','Platforma yatırımı durdur.','Düşüşü normal kabul et.'],correct:1,ok:"Kotter Adım 8: Geri bildirim döngüsü örgütü öğrenen yapıya dönüştürür.",no:"Sorunları görmezden gelmek değişimi kültüre işlemez.",theory:"Kotter Adım 8: Değişim 'tamamlanmaz', kültüre 'işlenir'. Sürekli öğrenme döngüsü bu adımı destekler.",comp:'Sürdürülebilirlik',xp:80},
{ch:1,sc:'RetailChain — Kısa Kazanım',sit:'Proje 8. ayında beklenenden iyi gidişat var. Ekiple paylaşmak mantıklı mı?',q:'Bu ilerlemeyi paylaşmanın değişim yönetimi açısından faydası nedir?',opts:['Çalışanlar detaylarla ilgilenmez.','Görünür kazanımlar şüphecileri ikna eder ve koalisyonu güçlendirir.','Erken paylaşım beklenti yönetimini zorlaştırır.','Sadece yönetim kuruluna bildirilmeli.'],correct:1,ok:'Kotter Adım 6: Kazanımları görünür kılmak değişimin mümkün olduğunu kanıtlar ve momentum sağlar.',no:'Şeffaf ilerleme paylaşımı çalışan bağlılığını artırır ve şüphecileri ikna eder.',theory:'Kotter Adım 6: Kısa vadeli kazanımlar gerçek ilerlemenin kanıtıdır; saklamak değil, duyurmak gerekir.',comp:'Liderlik',xp:80},
{ch:1,sc:'MediGroup — ADKAR Tanı',sit:"Hemşireler 'Bize ne faydası var?' diyor. Doktorlar 'Vakit kaybı' diyor. Yönetim 'Eğitim verdik' diyor.",q:"ADKAR'da en kritik başlangıç noktası hangisidir?",opts:['Knowledge — Eğitimler yetersiz.','Awareness — Fayda yeterince aktarılmamış.','Ability — Beceri eksikliği.','Reinforcement — Ödül yok.'],correct:1,ok:"'Bize ne faydası var?' sorusu Awareness sorunudur; bu çözülmeden üst basamaklar anlamsızdır.",no:'ADKAR doğrusal; Awareness çözülmeden istek oluşmaz.',theory:'ADKAR Kırılma Noktası: En alt eksik basamaktan başlanır; Awareness çözülmeden üst basamaklar işlemez.',comp:'Analiz',xp:80}
,{ch:2,sc:'TelecomX — Kutlama Kültürü',sit:'Çağrı merkezi pilotu başarıyla tamamladı. Yönetim "Zaten yapacaktık" diyerek kutlamak istemiyor.',q:'Kısa vadeli kazanımların kutlanması neden önemli?',opts:['Kutlamalar zaman kaybıdır.','Kutlamalar koalisyonu pekiştirir; değişime inananların haklı çıktığını somut kanıtlar.','Kutlama yalnızca tam başarıda yapılır.','Çalışanlar motivasyon için kutlamaya ihtiyaç duymaz.'],correct:1,ok:'Kotter Adım 6: Kazanımlar değişimin mümkün olduğunun kanıtıdır; şüphecileri ikna eden en güçlü araçtır.',no:'Kutlamalar moral değil stratejik araçtır; şüphecileri somut kanıtla ikna eder.',theory:'Kotter Adım 6: Kısa vadeli kazanım planlı, görünür ve değişimle açıkça ilişkili olmalı.',comp:'Liderlik',xp:80}
,{ch:1,sc:'AutoGroup — Yönetici Modeli',sit:'Otomotiv firmasında yöneticiler değişimi destekliyor ama kendileri eski davranışları sürdürüyor.',q:'Bu sorunu çözmek için ne yapılmalı?',opts:['Yöneticilere ek eğitim ver.','Yönetici davranışlarını performans değerlendirme kriterlerine dahil et; değişim liderliği ölçütü ekle.','Yöneticileri değiştir.','Çalışanlara yöneticileri görmezden gelmelerini söyle.'],correct:1,ok:'Yönetici davranışları performans kriterlerine dahil edilmezse söylem-eylem açığı kapanmaz.',no:'Eğitim bilgi verir; sisteme entegrasyon davranışı değiştirir.',theory:'Kotter Adım 8: Yeni davranış performans değerlendirme ve terfi kriterlerine kazınmalıdır.',comp:'Liderlik',xp:80}
,{ch:0,sc:'BankTR — Kotter Sıralaması',sit:"Yeni banka yöneticisi değişim projesini başlatmak istiyor. Vizyon hazır, ekip seçildi. Ama çalışanlar değişimin neden gerekli olduğunu bilmiyor.",q:"Kotter'a göre önce hangi adım atlanmış?",opts:['Adım 3 — Vizyon Geliştir','Adım 5 — Harekete Geç','Adım 1 — Aciliyet Duygusu Yarat','Adım 7 — Kazanımları Pekiştir'],correct:2,ok:'Aciliyet duygusu olmadan vizyon ve ekip çalışmaz. Kotter Adım 1 temeldir.',no:"Vizyon ve ekip hazır olsa da çalışanlar 'neden' sorusuna cevap bulamazsa adım 1 atlanmış demektir.",theory:"Kotter Adım 1: 'Neden değişmeliyiz?' sorusu tüm örgütte yanıtlanmadan hiçbir şey işlemez.",comp:'Vizyon',xp:80}
,{ch:2,sc:'InsurPlus — Sistem Değişikliği',sit:'Sigorta şirketi yeni süreç uyguladı. Çalışanlar biliyor ve yapabiliyor ama eski alışkanlıklar zaman zaman geri dönüyor.',q:"ADKAR'da kalıcılığı sağlamak için ne yapılmalı?",opts:['Daha fazla eğitim ver.','Ödül sistemi ve KPI güncelle; yeni davranışı resmi olarak tanı ve ölç.','Ceza mekanizması kur.','Görmezden gel; zamanla düzelir.'],correct:1,ok:'Reinforcement mekanizmaları yeni davranışı pekiştirir; ödül ve tanıma sistemleri güncellenmeli.',no:'Eğitim tekrar bilgi verir; kalıcılık için yapısal pekiştirme gerekir.',theory:'ADKAR-R: Ödüller, tanıma ve hesap verebilirlik mekanizmaları olmadan eski davranışlar geri döner.',comp:'Sürdürülebilirlik',xp:80}

];
const POOL_S=[
{ch:0,sc:'GlobalBank — Çok Paydaşlı Koalisyon',sit:'Büyük bankada dijital dönüşüm başlıyor. CTO ve CFO karşı, orta yönetim sessiz, sadece CEO onaylıyor.',q:'Koalisyon oluşturmak için öncelikli strateji nedir?',opts:["CEO otoritesiyle CTO ve CFO'yu zorla.",'Her itirazın kökünü anla; CTO teknik CFO mali kaygı taşır. Ayrı ayrı yanıtla ve orta yönetimden kilit isimleri kazan.','Projeyi başlat; destek zamanla gelir.','Tüm yöneticileri aynı anda büyük toplantıda ikna et.'],correct:1,ok:'Her itirazın kökü farklıdır; ayrı ele alınmalı ve orta yönetim de dahil edilmeli.',no:'Zorla uyum sağlansa bile benimseme olmaz; itiraz nedenlerini anlamak koalisyon kurmanın ilk adımıdır.',theory:'Kotter Adım 2: Etkin koalisyon CxO düzeyinden orta yönetime kadar uzanan katmanlı destekle kurulur.',comp:'Paydaş Yönetimi',xp:120},
{ch:0,sc:'RetailChain — Değişim Yorgunluğu',sit:"Perakende zincirinde 2 yılda 5 büyük proje. Çalışanlar yeni duyuruya 'Yine mi?' tepkisi veriyor.",q:'Değişim yorgunluğu riskini yönetmek için ne yapılmalı?',opts:['Projeyi başlat; alışırlar.','Mevcut projelerin kapasitesini ve tamamlanma oranını ölç; değişim takvimini yeniden önceliklendir.','Tüm projeleri 1 yıl ertele.','Yeni projeyi gizlice başlat.'],correct:1,ok:'Örgütsel değişim kapasitesi sınırlıdır. Kapasite analizi yapılmadan yeni proje başlatmak tüm projeleri riske atar.',no:'Zorlama kapasite tükenmesini hızlandırır; önce kapasite analizi zorunlu.',theory:'Kotter Adım 7: Değişim hızı örgütün absorpsiyon kapasitesiyle sınırlıdır. Aşırı yükleme başarısızlık riskini artırır.',comp:'Değişim Yönetimi',xp:120},
{ch:0,sc:'InsurPro — Direnç Analizi',sit:"Sigorta şirketinde yeni risk modeli uygulanacak. Aktüerler 'Model hatalı' diyor. Satış ekibi 'Müşteri ilişkileri bozulur' diyor.",q:'Bu iki grubu nasıl farklı ele alırsınız?',opts:['Her iki gruba aynı eğitimi ver.','Aktüerlerin teknik itirazlarını veri ve kanıtla yanıtla; satış ekibinin kaygısını birebir görüşme ve senaryolarla gider.','Her iki grubu da görmezden gel.','Sadece satış ekibiyle çalış.'],correct:1,ok:'İtiraz kökü farklı: teknik vs. ilişkisel. Her biri kendi mantığıyla ele alınmalı.',no:'Aynı müdahale farklı dirençleri çözmez; itiraz tipini anlamak doğru müdahale seçmek için şart.',theory:'ADKAR — Desire: Bireysel kaygılar kişiseldir. Teknik kanıtla, ilişkisel kaygılar empatiyle çözülür.',comp:'Direnç Yönetimi',xp:120},
{ch:0,sc:'AgroNet — Strateji Boşluğu',sit:'Şirketin vizyonu var ama hangi adımların ne zaman atılacağı belirsiz. Ekipler nereye koşacağını bilmiyor.',q:'Bu boşluk nasıl kapatılır?',opts:['Vizyonu daha sık tekrarla.','Vizyon altında SMART kriterlerine göre yol haritası ve kilometre taşları tanımla.','Tüm kaynakları en büyük projeye yoğunlaştır.','Danışmana devret.'],correct:1,ok:"Vizyon 'nereye' sorusunu yanıtlar; strateji 'nasıl' sorusunu. SMART hedefler köprüyü kurar.",no:'Tekrar yüzeysel; her çalışanın günlük kararıyla bağlantı kurabileceği somut adımlar gerekli.',theory:'Kotter Adım 3: Vizyon geliştirme aşaması aynı zamanda strateji ve yol haritasını içerir.',comp:'Vizyon',xp:120},
{ch:0,sc:'EduChain — Sendika',sit:'Özel okul zinciri yeni öğretmen değerlendirme sistemi kuruyor. Sendika sert muhalefet başlattı.',q:'Sendika direncini yönetmek için en etkili strateji?',opts:['Yasal zorunluluk olarak dayat.','Erken aşamada sendika liderlerini sürecin tasarımına ortak et; kaygılarını sistemin şekillenmesine yansıt.','Değişimi kademeli uygula, sendikaya söyleme.','Sendikayı görmezden gel.'],correct:1,ok:'Paydaşları erken dahil etmek direnci sahiplenmeye dönüştürür.',no:'Dayatma kısa dönem uyum, uzun dönem sabotaj üretir.',theory:'Kotter Adım 5: Engelleri kaldırmak kimi zaman direnci ortağa dönüştürmekle başlar.',comp:'Paydaş Yönetimi',xp:120},
{ch:1,sc:'ManuTech — Kültürel Direnç',sit:"Otomotiv firmasında 'Biz bunu hep böyle yaptık' kültürü var. Orta yönetim yeni KPI sistemini sabote ediyor.",q:'Kültürel direnç ile nasıl başa çıkılır?',opts:['Direnen yöneticileri disiplin cezasıyla uyar.','Başarı hikayelerini görünür kıl; kazanımları destekleyenlerin başarısı olarak sun ve ödüllendir.','Sistemi gizlice uygula.','Direnci görmezden gel.'],correct:1,ok:'Kotter Adım 6: Başarı hikayeleri somut kanıt sunar ve direnci yumuşatır.',no:'Ceza yüzeyi düzeltir kökü değil; görünür başarı hikayeleri kültürel direncin en güçlü ilacıdır.',theory:'Kotter Adım 6+8: Kısa vadeli kazanımlar kanıt üretir; Adım 8 kültüre entegrasyonu sağlar.',comp:'Değişim Yönetimi',xp:120},
{ch:1,sc:'BankPro — Değişim Yorgunluğu',sit:'18 ayda 4 büyük proje. Çalışanlar yeni duyuruya tepki vermiyor.',q:'Değişim yorgunluğunu nasıl yönetirsiniz?',opts:['5. projeyi başlat; alışırlar.','Önce kapasite değerlendir; değişim takvimini önceliklendir.','Tüm projeleri 6 ay ertele.','Bonus vererek motivasyonu artır.'],correct:1,ok:'Değişim kapasitesi sınırlıdır; önceliklendirme ve kapasite analizi sürdürülebilir ritim için şart.',no:'Zorlama kapasite tükenmesini hızlandırır ve tüm projeleri başarısızlığa sürükler.',theory:'Kotter Adım 7: Değişim hızı örgütün absorpsiyon kapasitesiyle sınırlıdır.',comp:'Değişim Yönetimi',xp:120},
{ch:1,sc:'HealthSystem — Peer Learning',sit:"Hastanede sistem değişiyor. Doktorlar 'Vakit kaybı' diyor. Hemşireler doktorlara bakıyor.",q:'Teknik direnci aşmak için en etkili yöntem?',opts:['Eski sisteme erişimi kes.','Klinik iş akışını bilen doktorları süper kullanıcı yap; akran öğretimi kur.','Yönetim kararıyla zorunlu kullanım şartı getir.','Sistemi iki versiyon sun.'],correct:1,ok:"Akran öğretimi döngüsel direnci kırar; doktorların 'sahibi' haline geldiği sistem dirençten çıkar.",no:'Zorlama uyum üretir benimseme değil; akranlar arası güven tabanlı öğrenme çok daha kalıcıdır.',theory:'ADKAR Ability + Desire: Akran öğretimi hem beceri hem motivasyon sağlar.',comp:'Direnç Yönetimi',xp:120},
{ch:1,sc:'GlobalManu — Vizyon Kopukluğu',sit:'Enerji şirketinde 5 yıllık dönüşüm vizyonu var ama saha ekibi günlük operasyonla bağlantı kuramıyor.',q:'Bu köprüyü nasıl kurarsınız?',opts:['Vizyonu daha sık e-posta ile paylaş.','Her departman için vizyon-rol bağlantısını OKR veya kaskad hedeflerle somutlaştır.','Vizyonu 1 cümleye indir.','Saha ekiplerini vizyon toplantılarına davet et.'],correct:1,ok:'OKR veya kaskad hedefleme bireysel rolü vizyona bağlar; bireysel anlam üretir.',no:'Tekrar veya davet yüzeysel. Vizyon-rol bağlantısı her çalışan için bireysel anlam üretmeli.',theory:'Kotter Adım 3+4: Vizyon her katmanda anlam üretmeli; kaskad hedefleme bu köprüyü kurar.',comp:'Vizyon',xp:120},
{ch:2,sc:'EduTech — ADKAR Gruplar',sit:'E-öğrenme platformu zorunlu kılındı. Bazı öğretmenler kullanıyor, bazıları kullanmıyor, bazıları yanlış kullanıyor.',q:"Bu 3 farklı durumda ADKAR'ın hangi basamakları sorunlu?",opts:['Hepsi aynı basamakta sorunlu.','Kullanmayanlar: Desire. Yanlış kullananlar: Knowledge/Ability. Performans kriteri olmayanlar: Reinforcement.','Hepsi Knowledge sorununa sahip.','Hepsi Awareness sorununa sahip.'],correct:1,ok:'Her grup farklı ADKAR basamağında takılı; müdahalelerin farklılaştırılması gerekir.',no:'Tek tip müdahale farklı kırılma noktalarını çözmez; grup bazlı tanı zorunlu.',theory:'ADKAR Diagnostics: Her grup için ayrı kırılma noktası tespiti ve müdahale planı oluşturulur.',comp:'Analiz',xp:120},
{ch:2,sc:'TechCorp — Refreezing Planı',sit:'Büyük yazılım firmasında agile dönüşüm tamamlandı. Yönetim projeyi kapattı ve ekibi dağıttı.',q:'Bu karar neden risklidir?',opts:['Proje tamamlandıysa ekibin dağıtılması normaldir.','Refreezing aşaması henüz tamamlanmadı; yeni davranışlar sisteme entegre edilmeden eski pratikler geri döner.','Agile dönüşüm teknik bir süreçtir; kültürel değil.','Risk yok; yazılım şirketleri çevik zaten.'],correct:1,ok:'Proje kapanması Refreezing bitişi değildir; kültüre entegrasyon süreci devam etmeli.',no:"'Proje bitti' düşüncesi Lewin'in en sık gözlenen ihmallerinden biridir.",theory:"Lewin — Refreezing: Değişim 'tamamlanmaz', kültüre 'işlenir'. Sistem entegrasyonu bitiş kriteridir.",comp:'Sürdürülebilirlik',xp:120},
{ch:2,sc:'LogiTech — Ability Eksikliği',sit:'Lojistik firmasında sürücüler rota optimizasyon sistemini kullanıyor ama verimlilik artmıyor.',q:"ADKAR'ın hangi basamağı eksik olabilir?",opts:['Awareness','Desire','Knowledge','Ability'],correct:3,ok:'Sürücüler kullanıyor ama verimlilik artmıyorsa sistem yetkinlikle kullanılamıyor; Ability eksik.',no:'Awareness Desire ve Knowledge var. Verimlilik artmaması Ability basamağındaki pratik beceri eksikliğine işaret eder.',theory:'ADKAR-A: Bilgi ile yetenek aynı şey değildir. Koçluk, mentörlük ve uygulama pratiği yeteneği geliştirir.',comp:'Analiz',xp:120},
{ch:3,sc:'AutoGroup — Kültürel Atalet',sit:"150 yıllık otomotiv firmasında derin 'Her zaman böyle yaptık' kültürü. Değişim projeleri tekrar başarısız.",q:'Kültürel atalet için uzun vadeli strateji nedir?',opts:['Direnen tüm yöneticileri değiştir.','Kısa vadeli kazanımları görünür kıl; destekleyenleri ödüllendir; işe alım ve terfi kriterlerini değişim yanlısı tutuma göre güncelle.','Tüm çalışanlara zorunlu eğitim ver.','Danışmanlığa devret.'],correct:1,ok:'Kültürel değişim 3 mekanizmayla kalıcı: görünür kazanımlar, destekleyenlerin ödüllendirilmesi ve sistem kriterleri.',no:'Eğitim veya değiştirme kısa vadeli. Kültür sistemler ödüller ve sembolik davranışlarla değişir.',theory:'Kotter Adım 6+8: Kısa vadeli kazanımlar kanıt üretir; Adım 8 kültüre entegrasyonu sağlar.',comp:'Değişim Yönetimi',xp:120},
{ch:3,sc:'GlobalMed — Mesaj Çelişkisi',sit:"Sağlık grubunun CEO'su çalışanlara 'Birlikte dönüşeceğiz' derken yönetim kuruluna 'Maliyetleri %30 düşüreceğiz' diyor.",q:'Bu paradoks hangi Kotter adımını çöküşe uğratıyor?',opts:['Adım 1 — Aciliyet','Adım 4 — Vizyonu İlet','Adım 2 — Koalisyon','Adım 6 — Kazanım'],correct:1,ok:"Çelişen mesajlar Adım 4'ü doğrudan çöküşe uğratır; her paydaş grubuna dürüst tutarlı çerçeve sunulmalı.",no:'İletişim tutarsızlığı değişim liderliğinin en öldürücü hatasıdır.',theory:'Kotter Adım 4 — Mesaj Bütünlüğü: Farklı paydaşlara verilen mesajlar çeliştiğinde güven çöker.',comp:'İletişim',xp:120},
{ch:3,sc:'RetailMega — Çoklu Direnç',sit:'Büyük perakende zincirinde yeni satış sistemi için IT teknik risk, müdürler beceri eksikliği, satış temsilcileri hedef kaygısı taşıyor.',q:'Üç farklı direnci nasıl yönetirsiniz?',opts:['Üçüne de aynı teknik sunum yap.','IT için pilot ve risk azaltma; müdürler için rol bazlı eğitim; temsilciler için geçiş dönemi hedef uyarlaması.','En güçlü dirençten başla.','Üst yönetimle bastır.'],correct:1,ok:'Her direnç tipi farklı müdahale gerektirir; rol bazlı farklılaştırma hem pratik hem güven inşa eder.',no:'Tek tip müdahale farklı köklü dirençleri çözmez.',theory:'ADKAR Desire + Kotter Adım 5: Farklı gruplarda engel farklı yerlerdedir; doğru tanı doğru müdahaleyi gerektirir.',comp:'Direnç Yönetimi',xp:120},
{ch:3,sc:'DigiBank — Kalıcılık',sit:'Dijital banka başarılı CX dönüşümü tamamladı. Yönetim projeyi kapattı. 8 ay sonra eski davranışlar geri döndü.',q:'Kalıcılık mimarisi nasıl kurulmalıydı?',opts:['Proje kapanıyor çünkü başarı kanıtlandı.','Yeni davranışları işe alım, performans değerlendirme, ödül ve terfi kriterlerine entegre etmek; değişim şampiyonlarını resmi rolle güçlendirmek.','Tekrar eğitim yeter.','Yöneticileri değiştir.'],correct:1,ok:'Kalıcılık için yeni davranışlar yapısal mekanizmalara kazınmalıdır.',no:'Proje bitmesi kalıcılık değil. Sistemsel entegrasyon olmadan geri kayma kaçınılmaz.',theory:'Lewin Refreezing + Kotter Adım 8: Değişim kültüre işlenmeden tamamlanmış sayılamaz.',comp:'Sürdürülebilirlik',xp:120},
{ch:0,sc:'BuildPro — Kültürel Sabotaj',sit:"İnşaat firmasında yönetici toplantılarda değişimi destekliyor ama ekibine 'Bu da geçer' diyor.",q:'Bu çelişki hangi Kotter adımını zedeliyor?',opts:['Adım 1','Adım 4 — Vizyonu İlet','Adım 2','Adım 6'],correct:1,ok:'Adım 4: Yönetici davranışları söyleminden güçlü mesaj taşır; çelişki güveni yıkıyor.',no:'İletişim yalnızca sözel değil; yönetici davranışları en güçlü mesaj taşıyıcısıdır.',theory:'Kotter Adım 4: Söylem-eylem çelişkisi değişim iletişimini geçersiz kılar.',comp:'İletişim',xp:120},
{ch:2,sc:'HealthGroup — Vizyon Testi',sit:"Hastane grubunun değişim vizyonu net. Yönetim 'Çalışanlar anlıyor mu?' diye merak ediyor.",q:'Vizyonun anlaşıldığını test etmenin en iyi yolu nedir?',opts:['Anket yap.','Çalışanları vizyonu kendi sözcükleriyle anlatmaları için rastgele gruplarla görüş.','CEO toplantısı düzenle.',"İntranet'te vizyon sayfası aç."],correct:1,ok:'Vizyonu kendi sözleriyle anlatabilen çalışan anlamış demektir; bu en güvenilir testtir.',no:'Anket yüzeysel; aktif geri bildirim daha güçlü anlama kanıtı sunar.',theory:'Kotter Adım 3: Vizyon anlaşılmadıysa iletilemez. Anlama testi yapılmadan ilerleme olmaz.',comp:'Vizyon',xp:120},
{ch:1,sc:'FinGroup — Strateji',sit:'Finans grubunun vizyonu net ama çalışanlar hangi adımların önce atılacağını bilmiyor.',q:'Bu durumda ne yapılmalı?',opts:['Vizyonu tekrar tekrar duyur.','SMART hedefler ve yol haritasıyla stratejiyi operasyonalize et.','En büyük projeye tüm kaynağı yoğunlaştır.','Danışmana bırak.'],correct:1,ok:"Vizyon 'nereye' sorusunu yanıtlar; strateji 'nasıl' sorusunu. SMART hedefler köprüdür.",no:'Tekrar yüzeysel; somut adımlar olmadan vizyon hayata geçemez.',theory:'Kotter Adım 3: Vizyon geliştirme strateji ve yol haritasını da kapsar.',comp:'Vizyon',xp:120},
{ch:3,sc:'ManuGroup — Değişim Kapasitesi',sit:'Üretim grubunda 3 aktif değişim projesi var. 4. proje zorunlu geliyor.',q:'Bu durumu yönetmek için ne yapılmalı?',opts:['4. projeyi de ekle; ekipler alışır.','Mevcut projelerin kapasite ve tamamlanma durumunu değerlendir; önceliklendirme yaparak 4. projenin zamanlamasına karar ver.','4. projeyi tamamen iptal et.','4. projeyi ayrı bütçeyle başlat.'],correct:1,ok:'Örgütsel değişim kapasitesi sınırlıdır; kapasite analizi yapılmadan yeni proje başlatmak tüm projeleri riske atar.',no:"'Ekle; alışır' yaklaşımı tüm projeleri başarısızlığa sürükler.",theory:'Kotter Adım 7: Değişim hızı örgütün absorpsiyon kapasitesiyle sınırlıdır; önceliklendirme kritik.',comp:'Değişim Yönetimi',xp:120},
{ch:2,sc:'ManufGroup — Kısa Vade',sit:'Üretim grubunda 3 yıllık büyük dönüşüm var. Yöneticiler 3. yıla kadar başarı görmek istemiyor.',q:'Bu yaklaşımın riski ve alternatifi nedir?',opts:['Risk yok; büyük dönüşümler uzun sürer.','Kısa vadeli kazanımların planlanmaması şüphecileri artırır ve koalisyonu zayıflatır; 6-18 aylık görünür başarılar planlanmalı.','3 yıl makul; beklemek gerekir.','Çalışanlara 3. yılda ödül vaat et.'],correct:1,ok:'Kotter Adım 6: Şüpheciler kısa vadeli somut kanıt olmadan sabırsızlanır ve direnç güçlenir.',no:'3 yıl boyunca görünür kazanım olmaması koalisyonu zayıflatır ve direnci güçlendirir.',theory:'Kotter Adım 6: Kısa vadeli kazanımlar 6-18 ay içinde planlanmalı; uzun vade tek başına yeterli değil.',comp:'Liderlik',xp:120},
{ch:0,sc:'TechGroup — Kazanım Paylaşımı',sit:'IT dönüşümü 6. ayında başarılı sonuçlar var. Yönetim "Vakit yok, kutlamaya gerek yok" diyor.',q:"Bu tutumun Kotter modeline göre riski nedir?",opts:['Risk yok; kutlama zaman kaybıdır.','Kısa vadeli kazanımların kutlanmaması değişime inananların motivasyonunu düşürür ve şüphecileri ikna fırsatını kaçırır.','Kutlama yalnızca tamamlanmış projelerde yapılır.','Küçük kazanımları kutlamak güvenilirliği zayıflatır.'],correct:1,ok:'Kotter Adım 6: Kazanımlar değişimin mümkün olduğunun kanıtı; kutlanmadan geçilmesi momentum kaybettirir.',no:'Kutlamalar stratejik araçtır; şüphecileri somut kanıtla ikna eden en güçlü mekanizmadır.',theory:'Kotter Adım 6: Planlı görünür ve değişimle açıkça ilişkili kazanımlar seçilip duyurulmalı.',comp:'Liderlik',xp:120},
,{ch:0,sc:'TelcoGroup — Vizyon Paylaşımı',sit:'Büyük telekom şirketinde dönüşüm vizyonu var ama farklı departmanlar vizyonu farklı anlıyor.',q:'Bu tutarsızlığı gidermek için ne yapılmalı?',opts:['Her departmana farklı vizyon sun.','Tüm departmanlarla ortak bir vizyon çalışması yap; her birimin vizyon yorumunu hizala.','Tek bir slayt yapıp dağıt.','Departman müdürlerine bırak.'],correct:1,ok:'Vizyon hizalama çalışması tutarsız yorumları ortadan kaldırır; her birim kendi bağlamında anlam üretmeli.',no:'Dağıtım yüzeyseldir; aktif hizalama çalışması ortak anlayış üretir.',theory:'Kotter Adım 4: Vizyon iletişimi tek yönlü değil, çift yönlü anlayış üretme sürecidir.',comp:'Vizyon',xp:120}
,{ch:2,sc:'HealthNet — ADKAR Katman',sit:'Sağlık ağında sistem değişikliği. Yöneticiler destekliyor, orta kademe kararsız, klinisyenler direniyor.',q:'Bu üç farklı ADKAR profilini nasıl ele alırsınız?',opts:['Hepsine aynı eğitimi ver.','Yöneticiler: Reinforcement yeterli. Orta kademe: Desire odaklı çalışma. Klinisyenler: Awareness ve Desire birlikte ele al.','Sadece klinisyenlerle çalış.','Orta kademeden başla.'],correct:1,ok:'Her katmanın ADKAR profili farklıdır; müdahale katman bazlı tasarlanmalı.',no:'Tek tip müdahale farklı ADKAR durumlarını çözmez.',theory:'ADKAR Diagnostics: Her grup için ayrı kırılma noktası tespiti ve müdahale planı şart.',comp:'Analiz',xp:120}
,{ch:1,sc:'ManuPro — Koalisyon Yetki',sit:'Üretim firmasında değişim koalisyonu kuruldu ama kararlar hâlâ eski hiyerarşiyle alınıyor.',q:'Koalisyon neden işlevsiz?',opts:['Koalisyon üyeleri yanlış seçildi.','Koalisyona karar alma yetkisi verilmedi; değişimi yürüten güç merkezi olmalı.','Koalisyon çok büyük.','Toplantı sıklığı yetersiz.'],correct:1,ok:'Yetkisiz koalisyon dekoratif kalır; karar alma gücü verilmeden değişim yürütülemez.',no:'Üyelik önemli ama yetki daha kritik.',theory:'Kotter Adım 2: Koalisyon değişimi somut adımlarla ilerletme yetkisine sahip olmalı.',comp:'Liderlik',xp:120}
,{ch:3,sc:'EduNet — Vizyon ve Eylem',sit:'Okul ağında güçlü bir vizyon var. Müdürler "Harika vizyon, peki ilk somut adımımız ne?" diye soruyor.',q:'Bu soruya en iyi yanıt nedir?',opts:['Vizyonu önce daha geniş kitlelere yay.','90 günlük somut eylem planı hazırla; her müdürün kendi okulunda ilk hafta yapacaklarını belirle.','Danışmanın gelmesini bekle.','Yıllık plan yapılınca başlanır.'],correct:1,ok:"Vizyon'dan eyleme geçiş 90 günlük spesifik planlarla başlar.",no:'Vizyonu yaymak önemli ama somut eylem planı olmadan vizyon havada kalır.',theory:'Kotter Adım 3+5: Vizyon somut strateji ve ilk eylemlerle desteklenmeli.',comp:'Vizyon',xp:120}
,{ch:3,sc:'LogiCorp — Refreezing Mimarisi',sit:'Lojistik firması büyük bir süreç dönüşümünü başarıyla tamamladı. Yönetim artık "Bitti" diyor.',q:"Bu tutumun Lewin modeli açısından riski nedir?",opts:["'Bitti' demek normaldir; proje kapatılmalı.",'Refreezing henüz tamamlanmamış; yeni davranışlar KPI ve kültüre kazınmadan geri kayma kaçınılmaz.','Lewin modeli yalnızca uygulama aşamasını kapsar.','Proje kapanması Refreezing anlamına gelir.'],correct:1,ok:'Refreezing proje kapanmasıyla değil, sistem entegrasyonuyla tamamlanır.',no:"'Proje bitti = değişim kalıcı' yanılgısı Lewin'in en sık gözlenen ihlalidir.",theory:'Lewin — Refreezing: Değişim kültüre işlenmeden bitmez. Sistem, kriter ve kültür güncellemesi zorunlu.',comp:'Sürdürülebilirlik',xp:120}
,{ch:0,sc:'PharmaTR — ADKAR Diagnostik',sit:'İlaç firmasında yeni kalite sistemi uygulandı. Çalışanlar eğitimi tamamladı. Ancak denetimlerde uyumsuzluk var.',q:"ADKAR'da asıl sorun hangi basamakta?",opts:['Awareness — Değişimin nedeni açıklanmadı.','Desire — Çalışanlar değişmek istemiyordur.','Ability — Bilgiyi uygulamaya dökemiyorlar olabilir.','Reinforcement — Denetim mekanizması eksik.'],correct:2,ok:'Eğitim aldılar (Knowledge var) ama uygulamada zorluk yaşıyorlar; bu Ability sorunudur.',no:'Knowledge basamağı tamamlandı. Uygulamada hata Ability eksikliğine işaret eder.',theory:'ADKAR-A (Ability): Bilgiyi pratiğe dökmek için koçluk, gözlem ve geri bildirim döngüsü gerekir.',comp:'Analiz',xp:120}
,{ch:2,sc:'RetailPro — Kültürel Değişim',sit:'Perakende şirketinde müşteri odaklı kültür değişimi başlatıldı. Eğitimler yapıldı ama müşteri şikayetleri azalmıyor.',q:'Eğitim sonrası kültürel değişimi kalıcı kılmak için ne yapılmalı?',opts:['Daha fazla eğitim ver.','Müşteri memnuniyetini performans kriterlerine dahil et; olumlu davranışı tanı ve ödüllendir.','Müşteri şikayetlerini raporla.','Yöneticileri bilgilendir.'],correct:1,ok:'Kültür eğitimle değil sistemlerle değişir; KPI ve ödül sistemi güncellenmeden davranış değişmez.',no:'Eğitim bilgi verir; sisteme entegrasyon davranışı kalıcı kılar.',theory:'Kotter Adım 8 + ADKAR-R: Yeni davranış hem kültüre hem ödül sistemine entegre edilmeli.',comp:'Değişim Yönetimi',xp:120}
,{ch:1,sc:'EnergyTR — Değişim Hızı',sit:'Enerji şirketinde CEO "2 yıllık dönüşümü 9 ayda tamamlayacağız" dedi. Proje yöneticisi kapasite yetersizliğinden endişeli.',q:'Bu durumda proje yöneticisi ne yapmalı?',opts:['CEO kararını kabul et; hız öncelik.','Mevcut kapasite ve kaynak durumunu analiz ederek CEO ile riskleri net biçimde paylaş; önceliklendirme ve kaynak takviyesi seçenekleri sun.','Sessiz kal; sonuçta görülür.','Ekibi fazla mesaiye zorla.'],correct:1,ok:'Lider riskleri zamanında ve açıkça paylaşır; kapasite sorunu konuşulmazsa proje çöker.',no:'Sessiz kalmak sorunu büyütür; proaktif risk paylaşımı liderlik görevidir.',theory:'Kotter Adım 7: Değişim hızı örgütün absorpsiyon kapasitesiyle sınırlıdır; önceliklendirme kritik.',comp:'Liderlik',xp:120}
,{ch:3,sc:'FinTech — Sürdürülebilir Değişim',sit:'Fintech şirketi agile dönüşümü başarıyla tamamladı. Yönetim değişimi "Bitti, artık iş oldu" olarak kapatmak istiyor.',q:'Bu yaklaşım doğru mu?',opts:["Evet; dönüşüm tamamlandı, artık operasyona odaklan.",'Hayır; değişim sürekli bir döngüdür. Retrospektif, ölçüm ve iyileştirme mekanizmaları aktif tutulmalı.','Belki; 6 ay daha izle, sonra kapat.','Evet; agile zaten sürekli değişim demek.'],correct:1,ok:"Kotter Adım 8: Değişim 'tamamlanmaz', kültüre işlenir. Öğrenme döngüleri aktif kalmalı.",no:"'Bitti' düşüncesi geri kaymanın en güçlü tetikleyicisidir.",theory:'Kotter Adım 8 + Lewin Refreezing: Değişim projesi kapanabilir ama değişim kültürünün yaşatılması sürekliliktir.',comp:'Sürdürülebilirlik',xp:120}
,{ch:0,sc:'HospitalTR — Direnç Yönetimi',sit:'Devlet hastanesinde yeni hasta kayıt sistemi zorunlu kılındı. Hemşireler "Bu bizi yoruyor, işimize yaramıyor" diyor.',q:'Bu direnci yönetmek için önce ne yapılmalı?',opts:['Kullanımı zorunlu kıl ve denetimleri artır.','Hemşirelerin iş yükü ve süreç deneyimini dinle; şikayetleri sistem iyileştirmesine yansıt.','Sistemi kaldır.','İK ile disiplin sürecini başlat.'],correct:1,ok:'Kullanıcı geri bildirimini sisteme yansıtmak sahiplenmeyi artırır ve teknik direnci azaltır.',no:'Zorlama uyum getirir, benimseme değil. Geri bildirim odaklı yaklaşım kalıcı çözümdür.',theory:'ADKAR-D + Kotter Adım 5: Kullanıcıları sürecin iyileştirilmesine ortak etmek direnci sahiplenmeye dönüştürür.',comp:'Direnç Yönetimi',xp:120}
,{ch:1,sc:'AutoTech — Vizyon Testi',sit:"Otomotiv şirketinin değişim vizyonu 'Dünya standartlarında üretim' olarak belirlendi. Çalışanlar vizyona ilgisiz.",q:'Vizyonun neden işe yaramadığını nasıl anlarsınız?',opts:['İlgisizlik normaldir; zaman içinde geçer.','Çalışanlara vizyonu kendi sözcükleriyle anlatmalarını iste; anlayamıyorlarsa vizyon somutlaştırılmamıştır.','Vizyonu daha büyük pankartlara bas.','Yöneticilere vizyonu ezberlet.'],correct:1,ok:'Vizyon ancak çalışan onu kendi sözleriyle ifade edebildiğinde anlaşılmış demektir.',no:"İlgisizlik genellikle 'vizyon bireysel anlam üretmiyor' sinyalidir.",theory:'Kotter Adım 3+4: Vizyon 5 dakikada anlatılabilmeli ve dinleyende kişisel anlam üretmeli.',comp:'Vizyon',xp:120}

];
const POOL_X=[
{ch:0,sc:'GlobalCorp — Üçlü Kriz',sit:'Uluslararası üretim şirketinde aynı anda: dijitalleşme baskısı, sendika grevi tehdidi ve rakip satın alması söylentisi var.',q:'Bu senaryoda hangi model öncelikli ve neden?',opts:['ADKAR — Bireysel değişimi yönet.','Kotter Adım 1-2: Tüm paydaşlar için farklı aciliyet mesajları oluştur ve her cephe için ayrı koalisyon kur.','Lewin — Önce dondur sonra değiştir.','Üç sorunu ayrı proje olarak ele al.'],correct:1,ok:'Çok cepheli krizlerde her paydaş grubu farklı aciliyet mesajı gerektirir; her cephe için koalisyon ayrı kurulmalıdır.',no:'Tek model veya proje ayrımı bu ölçekte yetersizdir.',theory:'Kotter Adım 1-2: Çok paydaşlı ortamda her grup kendi perspektifinden aciliyet hissetmeli; koalisyon bağlam odaklı olmalı.',comp:'Analiz',xp:160},
{ch:0,sc:'MegaBank — Model Sentezi',sit:"2000 çalışanlı bankada: üst yönetim koalisyonu var (Kotter), departman uygulaması başladı (Lewin Changing), ancak çalışan başarı oranı %40'ta takılı.",q:'Hangi modelin hangi boyutuna odaklanmalısınız?',opts:['Kotter — Koalisyonu güçlendir.','ADKAR — %40 başarı oranı bireysel kırılma noktasını gösterir; Awareness-Desire tanısı yap.','Lewin — Uygulama aşamasını hızlandır.','Tüm modeller aynı anda uygulanamaz.'],correct:1,ok:'%40 oranı bireysel ADKAR kırılması olduğunu gösterir; toplu tanı yapılmalı.',no:'Kotter ve Lewin kurumsal düzeyde çalışıyor; bireysel başarı oranı düşükse ADKAR diagnostiği gerekir.',theory:'Model Entegrasyonu: Kotter kurumsal yol haritası, Lewin geçiş yönetimi, ADKAR bireysel değişim tanısıdır.',comp:'Analiz',xp:160},
{ch:0,sc:'DigitalBank — Hız Paradoksu',sit:'Dijital banka kurmak için 18 ay var. Rakipler 12 ayda kuruyor. CEO "Kotter çok yavaş, adımları atlayalım" diyor.',q:'Bu yaklaşım doğru mu?',opts:['Evet; acil durumda model atlanır.','Hayır; adımlar atlanamaz ama paralel yürütülerek hız artırılabilir.','Evet; en az 3 adım atlanabilir.','Hayır; her adım en az 3 ay sürmeli.'],correct:1,ok:'Adımlar birbirinin önkoşuludur; atlamak değil paralel çalıştırmak hız üretir.',no:'Kotter adımları zorunlu önkoşullardur; atlamak kısa vade hız, uzun vade başarısızlık üretir.',theory:'Kotter Hızlandırılmış Uygulama: Adımlar iç içe geçmiş yürütülebilir; atlamak değil, paralel çalıştırmak doğru.',comp:'Değişim Yönetimi',xp:160},
{ch:0,sc:'PharmaCo — Küresel ADKAR',sit:"12 ülkede ERP değişikliği. Almanya'da Awareness yok, Türkiye'de Desire eksik, Hindistan'da Knowledge problemi.",q:'Bu senaryoda ne yapılmalı?',opts:['Herkese aynı global eğitim paketini ver.','Her ülke için ADKAR tanısına göre farklı müdahale planı; küresel çerçeve koru yerel taktik farklılaştır.','En kolay ülkeden başla, sırayla git.','Pilot ülke seç.'],correct:1,ok:'Kırılma noktası ülkeden ülkeye farklı olabilir; müdahale yerelleştirilmeli.',no:'Tek tip müdahale farklı kırılma noktalarını çözmez.',theory:'ADKAR Diagnostics: Her birim veya coğrafya için ayrı ADKAR değerlendirmesi yapılır.',comp:'Analiz',xp:160},
{ch:0,sc:'AutoGroup — Kültürel Atalet',sit:'150 yıllık otomotiv firmasında değişim projeleri tekrar başarısız. Kültürel atalet derinlere işlemiş.',q:'Kültürel atalet için uzun vadeli entegre strateji nedir?',opts:['Direnen tüm yöneticileri değiştir.','Görünür kazanımlar üret; kazanımları destekleyenlerin başarısı olarak sun; işe alım, terfi ve performans kriterlerini değişim yanlısı davranışa göre güncelle.','Tüm çalışanlara zorunlu değişim eğitimi ver.','Dışarıdan danışman getir.'],correct:1,ok:'Kültürel değişim 3 mekanizma ile kalıcı: görünür kazanımlar, destekleyenlerin ödüllendirilmesi ve sistem kriterleri.',no:'Değiştirme veya eğitim kısa vadeli. Kültür sistemler, ödüller ve sembolik davranışlarla değişir.',theory:'Kotter Adım 6+8: Kısa vadeli kazanımlar kanıt üretir; Adım 8 kültüre entegrasyonu sağlar.',comp:'Değişim Yönetimi',xp:160},
{ch:0,sc:'EnergyGiant — Vizyon Kopukluğu',sit:'Enerji şirketinde 5 yıllık vizyon var. Saha ekipleri vizyon ile günlük operasyon arasında bağlantı kuramıyor.',q:'Bu köprüyü nasıl kurarsınız?',opts:['Vizyonu daha sık e-posta ile paylaş.','Vizyon-Strateji-Taktik hiyerarşisi kur; her departman OKR ile vizyona bağlansın.','Vizyonu 1 cümleye indir.','Saha ekiplerini vizyon toplantısına davet et.'],correct:1,ok:'OKR veya kaskad hedefleme bireysel rolü vizyona bağlar; bireysel anlam üretir.',no:'Tekrar veya davet yüzeysel. Vizyon-rol bağlantısı her çalışan için bireysel anlam üretmeli.',theory:'Kotter Adım 3+4: Vizyon her katmanda anlam üretmeli; kaskad hedefleme bu köprüyü kurar.',comp:'Vizyon',xp:160},
{ch:0,sc:'StartUp2Scale — Paradoksal Kültür',sit:"50 kişiden 500 kişiye büyüyen startup. Eski çalışanlar 'Ruhumuzu kaybettik' diyor. Yeni gelenler 'Kaotik, sistem yok' diyor.",q:'Bu paradoksal değişimi nasıl yönetirsiniz?',opts:['Eski kültürü tamamen bırak.',"Kurucularla 'neyi koruyacağız' diyalogu aç; yeni gelenlerle 'nasıl sistematikleştireceğiz' çalışması yap; köprü vizyon her iki gruba hitap etmeli.",'Yeni gelenlerin fikirlerini uygula.','Sadece eski çalışanlara öncelik ver.'],correct:1,ok:'Paradoksal değişimde her grubun meşru kaygısı var; köprü vizyon her iki gerçeği kucaklamalı.',no:'Tek grup odağı diğerini dışlar; paradoks yönetimi her iki gerçeği aynı anda adresler.',theory:"Lewin Unfreezing — Diyalog: Çözme aşaması 'neyi taşıyacağız, neyi bırakacağız?' sorusunu birlikte yanıtlamaktır.",comp:'Liderlik',xp:160},
{ch:0,sc:'GlobalMed — Mesaj Tutarsızlığı',sit:"CEO çalışanlara 'Birlikte dönüşeceğiz' derken yönetim kuruluna 'Maliyetleri %30 düşüreceğiz' diyor.",q:'Bu paradoks hangi Kotter adımını çöküşe uğratıyor?',opts:['Adım 1 — Aciliyet','Adım 4 — Vizyonu İlet','Adım 2 — Koalisyon','Adım 6 — Kazanım'],correct:1,ok:"Çelişen mesajlar Adım 4'ü çöküşe uğratır; her paydaş grubuna dürüst tutarlı çerçeve sunulmalı.",no:'İletişim tutarsızlığı değişim liderliğinin en öldürücü hatasıdır.',theory:'Kotter Adım 4: Farklı paydaşlara verilen mesajlar çeliştiğinde güven çöker; tutarlılık liderlik güvenilirliğinin temelidir.',comp:'İletişim',xp:160},
{ch:0,sc:'ManuNet — ADKAR vs Kotter',sit:'Üretim şirketinde Kotter adımları doğru uygulandı; koalisyon güçlü, vizyon net. Ancak bireysel kabul oranı %50.',q:'Sorunun kaynağı nerede?',opts:['Kotter modeli yetersiz.','ADKAR bireysel düzeyde tanı gerektirir; kurumsal başarı bireysel başarıyı garantilemez.','Kazanımlar yeterince kutlanmadı.','Vizyon yeterince net değil.'],correct:1,ok:'Kotter kurumsal düzeyde çalışır; bireysel kabul için ADKAR ayrıca uygulanmalıdır.',no:'Kotter adımları doğru uygulandı; sorun bireysel basamaklarda, kurumsal değil.',theory:'Model Entegrasyonu: Kotter ve ADKAR farklı seviyelerde çalışır; birlikte kullanıldığında en güçlü sonuç alınır.',comp:'Analiz',xp:160},
{ch:1,sc:'TechUni — Kalıcılık İhmal',sit:'Üniversite dijital dönüşümü tamamladı. Rektör projeyi kapadı ve ekibi dağıttı. 1 yıl sonra eski pratikler geri döndü.',q:'Hangi Lewin + Kotter ikilisi atlandı?',opts:['Lewin Unfreezing + Kotter Adım 1','Lewin Refreezing + Kotter Adım 8','Lewin Changing + Kotter Adım 5','Hiçbirinde sorun yok.'],correct:1,ok:"'Bitirdik' tutumu Refreezing ve Adım 8'in atlandığını gösterir.",no:'Başarılı uygulama sonrası geri dönüş klasik kalıcılık mimarisi ihmalinin sonucudur.',theory:"Lewin Refreezing + Kotter Adım 8: Değişim 'tamamlanmaz', kültüre 'işlenir'.",comp:'Sürdürülebilirlik',xp:160},
{ch:1,sc:'NationalTelecom — Katmanlı İletişim',sit:'15.000 çalışanlı telekom şirketinde tek iletişim planı. Yöneticiler bilgili, orta kademe kararsız, saha tamamen bilgisiz.',q:'Bu yaklaşım neden yetersiz?',opts:['Tek plan yeterli; herkes aynı mesajı almalı.','Her katman kendi ADKAR durumundadır; yönetici orta kademe ve saha için ayrı içerik ve kanallar şart.','Yalnızca saha çalışanlarına odaklan.','Yöneticileri eğit, gerisi akar.'],correct:1,ok:'15.000 kişilik farklılaşmış ADKAR profili tek planla yönetilemez; katman bazlı iletişim zorunlu.',no:'Tek mesaj tek ihtiyacı karşılar; farklı ADKAR düzeyindeki gruplar farklı içerik ve kanal gerektirir.',theory:'ADKAR + Kotter Adım 4: İletişim planı hedef kitlenin ADKAR durumuna göre tasarlanır.',comp:'İletişim',xp:160},
{ch:1,sc:'ConsumeCo — Geri Kayma Analizi',sit:"Tüketici ürünleri şirketinde yalın üretim dönüşümü 2 yıl önce tamamlandı. Denetimde %60'ı eski süreçlere döndüğü görüldü.",q:'ADKAR ve Lewin perspektifinden kökeni nedir?',opts:['Awareness eksikliği.','ADKAR Reinforcement eksikliği + Lewin Refreezing ihmali; ödüller, KPI ve kültür normları güncellenmedi.','Knowledge eksikliği.','Changing yanlış uygulandı.'],correct:1,ok:'İki model aynı noktaya işaret eder: pekiştirme mekanizmaları kurulmadan değişim kalıcı olmaz.',no:'Uygulama başarılıydı. Sorun sistemlere ve kültüre entegrasyonda.',theory:'Model Entegrasyonu: ADKAR-R ve Lewin Refreezing birbirini tamamlar; ikisi birlikte ele alınmadan kalıcılık sağlanamaz.',comp:'Sürdürülebilirlik',xp:160},
{ch:1,sc:'RetailMega — Çoklu Direnç',sit:'Büyük perakende zincirinde yeni satış sistemi için IT teknik risk, müdürler beceri eksikliği, satış temsilcileri hedef kaygısı taşıyor.',q:'Üç direnci nasıl yönetirsiniz?',opts:['Üçüne de aynı teknik sunum yap.','IT için pilot ve risk azaltma; müdürler için rol bazlı eğitim; temsilciler için geçiş dönemi hedef uyarlaması.','En güçlü dirençten başla.','Üst yönetimle bastır.'],correct:1,ok:'Her direnç tipi farklı müdahale gerektirir; rol bazlı farklılaştırma hem pratik hem güven inşa eder.',no:'Tek tip müdahale farklı köklü dirençleri çözmez.',theory:'ADKAR Desire + Kotter Adım 5: Farklı gruplarda engel farklı yerlerdedir; doğru tanı doğru müdahaleyi gerektirir.',comp:'Direnç Yönetimi',xp:160},
{ch:1,sc:'EnergyGroup — Koalisyon Sürekliliği',sit:'Enerji firmasında değişim koalisyonunun kilit üyelerinin yarısı 2 yılda ayrıldı.',q:'Koalisyon sürekliliğini nasıl sağlarsınız?',opts:['Koalisyonu yeniden kur; bitti.','Koalisyonu kurumsal role bağla kişiye değil; rol değişince üyelik güncellenir ve yedek üyeler belirlenir.','Yeni üyeler eski üyeleri arasın.','Koalisyonu küçült.'],correct:1,ok:'Koalisyon kişiye bağlı olunca ayrılma ile çöker; kurumsal role bağlamak sürekliliği sağlar.',no:'Yeniden kurmak zaman ve güven kaybettirir; önceden yapısal süreklilik planlanmalı.',theory:'Kotter Adım 2: Koalisyon yalnızca bireyler değil kurumsal mekanizmadır; rotasyon ve yedek planı şart.',comp:'Liderlik',xp:160},
{ch:2,sc:'GlobalCorp — Sentez Karar',sit:'Danışman olarak şirkete girdiniz. Hem Kotter hem ADKAR hem Lewin uygulanmış ama değişim başarısız.',q:'Değişim başarısızlığının kök nedenini bulmak için ilk adım nedir?',opts:['Vizyonu değiştir.','Her modelin hangi basamağında kırılma olduğunu diagnostik sorularla belirle: Bireysel mi kurumsal mı?','Tüm modelleri yeniden uygula.','Dışarıdan yeni danışman getir.'],correct:1,ok:'Başarısızlığın kök nedeni bireysel ya da kurumsal kırılma noktasında gizlidir; diagnostik analiz ilk adımdır.',no:'Modeli değiştirmek veya yeniden uygulamak tanı yapılmadan işe yaramaz.',theory:'Model Entegrasyonu: Başarısızlık analizi için Kotter, ADKAR ve Lewin çerçevelerinin her birinde kırılma noktası tespiti yapılır.',comp:'Analiz',xp:160},
{ch:2,sc:'HealthNet — 3 Model Entegrasyonu',sit:"Ulusal sağlık ağında büyük sistem değişikliği. Kurumsal düzey (Kotter) çalışıyor ama bireysel benimsetme (%45) ve kültürel kalıcılık sorunlu.",q:'3 modeli nasıl entegre edersiniz?',opts:['Kotter yeterli; diğerlerine gerek yok.','Kotter = kurumsal yol haritası; ADKAR = bireysel kırılma tanısı; Lewin = kültürel geçiş ve kalıcılık; üçünü eş zamanlı uygula.','ADKAR\'ı terk et; Lewin yeterli.','Önce birini tamamla sonra diğerine geç.'],correct:1,ok:'Her model farklı düzeyde çalışır; birlikte kullanıldığında en güçlü sonuç alınır.',no:'Modelleri sıralı uygulamak değişim hızını yavaşlatır; eş zamanlı entegrasyon gerekir.',theory:'Model Entegrasyonu: Kotter kurumsal yol haritası; ADKAR bireysel tanı; Lewin kültürel geçiş. Birlikte en güçlü çerçeveyi oluşturur.',comp:'Analiz',xp:160},
{ch:2,sc:'TechGroup — Kazanım Seçimi',sit:"Büyük teknoloji firmasında 3 yıllık dönüşüm var. Yönetim 'Kutlama kültürü oluşturalım' diyor ama hangi kazanımları kutlayacaklarını bilmiyorlar.",q:'Kutlanacak kazanım nasıl seçilmeli?',opts:['Her başarıyı kutla.','Görünür özgün değişimle açıkça ilişkili ve bölünmüş olmayan kazanımları seç; itiraz etmesi zor olacak şekilde tasarla.','Yalnızca büyük dönüm noktalarını kutla.','Kutlamaları rastgele planla.'],correct:1,ok:"Kotter Adım 6: Kazanımlar görünür, özgün ve değişimle açıkça ilişkili olmalı; şüphecilerin itiraz edemeyeceği şekilde tasarlanmalı.",no:'Her başarıyı kutlamak etkiyi sulandırır; seçici olmak kritik.',theory:'Kotter Adım 6: İyi bir kısa vadeli kazanım; görünür, belirsizliği olmayan ve değişimle açıkça ilişkilendirilebilen bir başarıdır.',comp:'Liderlik',xp:160},
{ch:2,sc:'BankGroup — Liderlik Paradoksu',sit:'Değişim liderinin hem ivediyet hem de güven mesajı vermesi gerekiyor. Bu ikisi çelişiyor gibi görünüyor.',q:'Bu paradoksu nasıl yönetirsiniz?',opts:["İkisinden birini seç; ikisi birlikte verilemez.",'İvediyet "neden şimdi" sorusunu yanıtlar; güven "nasıl yöneteceğiz" sorusunu. İkisi farklı mesajlarda eş zamanlı verilebilir.','Önce güveni ver, sonra ivediyet.','Önce ivediyet ver, sonra güven.'],correct:1,ok:"İvediyet ve güven farklı mesajlardır; 'neden şimdi' ve 'nasıl yöneteceğiz' soruları eş zamanlı yanıtlanabilir.",no:'İkisini sıralı vermek değerli zaman kaybettirir; eş zamanlı mesaj verilebilir.',theory:'Kotter Adım 1+4: Aciliyet ve güven çelişmez; birlikte verilir.',comp:'Liderlik',xp:160},
{ch:3,sc:'ConsumeCo — Sistem Entegrasyonu',sit:'Tüketici ürünleri firması başarılı dönüşüm sonrası sistemi kapattı. 1 yılda eski davranışlar döndü.',q:"Kalıcılık için gereken 'sistem değişiklikleri' nelerdir?",opts:['Sadece eğitimi tekrarla.','İşe alım kriterleri, onboarding, performans değerlendirme, terfi kararları ve bütçe tahsisi — bunların tümü yeni davranışı desteklemeli.','CEO sürekli konuşsa yeter.','Yeni çalışanlar eski kültürü taşımaz; zamanla çözülür.'],correct:1,ok:'Kalıcılık için tüm İK ve kaynak sistemleri yeni davranışı desteklemeli; yalnızca birine odaklanmak yetersiz.',no:'Tek mekanizma yeterli değil; birden fazla sistem değişikliği birlikte kalıcılık üretir.',theory:'Kotter Adım 8 + Lewin Refreezing: Kalıcılık için sistemsel çok katmanlı entegrasyon zorunludur.',comp:'Sürdürülebilirlik',xp:160},
{ch:3,sc:'GlobalBank — Post-Merger Kültür',sit:"İki bankanın birleşmesinden sonra iki farklı kültür çarpışıyor. Her iki taraf da 'Biz haklıyız' diyor.",q:'Kültür entegrasyonunu nasıl başlatırsınız?',opts:["Büyük bankanın kültürünü egemen kıl.",'Her iki kültürden en güçlü unsurları haritalandır; ortak köprü vizyon oluştur; her iki taraftan koalisyon üyeleri dahil et.',"Küçük bankanın kültürünü koruma altına al.",'Kültürü zaman içinde organik şekilde çözülmeye bırak.'],correct:1,ok:'Kültür entegrasyonu dayatma değil ortak keşif sürecidir; köprü vizyon ve karma koalisyon kritiktir.',no:'Tek kültürü egemen kılmak ya da organik bırakmak uzun vadeli çatışma ve direnç üretir.',theory:'Lewin Unfreezing + Kotter Adım 1-2: Kültür çarpışmasında önce ortak zemin bulunur; sonra karma koalisyon ile köprü vizyon kurulur.',comp:'Değişim Yönetimi',xp:160},
{ch:3,sc:'MegaRetail — Kapasite Planı',sit:'Büyük perakende şirketinde aynı anda 7 değişim projesi var. Proje yöneticileri çökmekte.',q:'Değişim portföyünü nasıl önceliklendirirsiniz?',opts:['CEO hangi projeye öncelik verirse o.','Stratejik etki × uygulama hazırlığı matrisi ile değerlendir; yüksek etki düşük hazırlık olanlara önce kapasite oluştur; düşük etki düşük hazırlık olanları ertele veya iptal et.','Başlanan projelerin hiçbirini durdurma.','En eski projeyi tamamla sonra diğerlerine geç.'],correct:1,ok:'2x2 matris değerlendirmesi kaynak dağılımını ve önceliklendirmeyi nesnel hale getirir.',no:'CEO kararı subjektif olabilir; matris analizi şeffaf ve savunulabilir karar verir.',theory:'Kotter Adım 7 + Değişim Kapasitesi: Önceliklendirme analitik bir süreçtir; stratejik etki ve hazırlık birlikte değerlendirilmeli.',comp:'Değişim Yönetimi',xp:160},
{ch:3,sc:'AutoCorp — Değişim Kültürü',sit:"Üretim firması 5 yıllık dönüşümü tamamladı. Artık değişimi 'projelerle' değil 'kültürel yetkinlikle' yönetmek istiyor.",q:'Değişim kültürü nasıl inşa edilir?',opts:['Her yıl büyük bir değişim projesi başlat.','İçsel değişim liderliği kapasitesi geliştir; değişim yönetimi yetkinliğini liderlik gelişim programlarına entegre et; çalışanları değişim şampiyonu olarak yetiştir.','Değişimi danışmanlara bırak.','Kotter adımlarını her projede tekrarla.'],correct:1,ok:'Değişim kültürü içsel kapasite geliştirmeyle inşa edilir; dışa bağımlılık azaltılmalıdır.',no:'Her projeyi sıfırdan başlatmak öğrenmeyi biriktiremez; içsel kapasite sürdürülebilir değişimi mümkün kılar.',theory:'Kotter Adım 8 + Kurumsal Öğrenme: Değişim kültürü içsel liderlik kapasitesi ve kurumsal öğrenme döngüleriyle inşa edilir.',comp:'Liderlik',xp:160},
,{ch:1,sc:'TechUni — Kalıcılık İhmal',sit:'Üniversite dijital dönüşümü tamamladı. Rektör projeyi kapadı ve ekibi dağıttı. 1 yıl sonra eski pratikler geri döndü.',q:'Hangi Lewin + Kotter ikilisi atlandı?',opts:['Lewin Unfreezing + Kotter Adım 1','Lewin Refreezing + Kotter Adım 8','Lewin Changing + Kotter Adım 5','Hiçbirinde sorun yok.'],correct:1,ok:"'Bitirdik' tutumu Refreezing ve Adım 8'in atlandığını gösterir; değişim bitmez, kültüre entegre edilir.",no:'Başarılı uygulama sonrası geri dönüş klasik kalıcılık mimarisi ihmalinin sonucudur.',theory:"Lewin Refreezing + Kotter Adım 8: Değişim 'tamamlanmaz', kültüre 'işlenir'.",comp:'Sürdürülebilirlik',xp:160}
,{ch:1,sc:'NationalTelecom — Katmanlı İletişim',sit:'15.000 çalışanlı telekom şirketinde tek iletişim planı. Yöneticiler bilgili, orta kademe kararsız, saha tamamen bilgisiz.',q:'Bu yaklaşım neden yetersiz?',opts:['Tek plan yeterli; herkes aynı mesajı almalı.','Her katman kendi ADKAR durumundadır; yönetici orta kademe ve saha için ayrı içerik ve kanallar şart.','Yalnızca saha çalışanlarına odaklan.','Yöneticileri eğit, gerisi akar.'],correct:1,ok:'15.000 kişilik farklılaşmış ADKAR profili tek planla yönetilemez; katman bazlı iletişim zorunlu.',no:'Tek mesaj tek ihtiyacı karşılar; farklı ADKAR düzeyindeki gruplar farklı içerik ve kanal gerektirir.',theory:'ADKAR + Kotter Adım 4: İletişim planı hedef kitlenin ADKAR durumuna göre tasarlanır.',comp:'İletişim',xp:160}
,{ch:1,sc:'ConsumeCo — Geri Kayma Analizi',sit:"Tüketici ürünleri şirketinde yalın üretim dönüşümü 2 yıl önce tamamlandı. Denetimde %60'ı eski süreçlere döndüğü görüldü.",q:'ADKAR ve Lewin perspektifinden kökeni nedir?',opts:['Awareness eksikliği.','ADKAR Reinforcement eksikliği + Lewin Refreezing ihmali; ödüller KPI ve kültür normları güncellenmedi.','Knowledge eksikliği.','Changing yanlış uygulandı.'],correct:1,ok:'İki model aynı noktaya işaret eder: pekiştirme mekanizmaları kurulmadan değişim kalıcı olmaz.',no:'Uygulama başarılıydı. Sorun sistemlere ve kültüre entegrasyonda.',theory:'Model Entegrasyonu: ADKAR-R ve Lewin Refreezing birbirini tamamlar; ikisi birlikte ele alınmadan kalıcılık sağlanamaz.',comp:'Sürdürülebilirlik',xp:160}
,{ch:1,sc:'RetailMega — Çoklu Direnç',sit:'Büyük perakende zincirinde yeni satış sistemi için IT teknik risk, müdürler beceri eksikliği, satış temsilcileri hedef kaygısı taşıyor.',q:'Üç direnci nasıl yönetirsiniz?',opts:['Üçüne de aynı teknik sunum yap.','IT için pilot ve risk azaltma; müdürler için rol bazlı eğitim; temsilciler için geçiş dönemi hedef uyarlaması.','En güçlü dirençten başla.','Üst yönetimle bastır.'],correct:1,ok:'Her direnç tipi farklı müdahale gerektirir; rol bazlı farklılaştırma hem pratik hem güven inşa eder.',no:'Tek tip müdahale farklı köklü dirençleri çözmez.',theory:'ADKAR Desire + Kotter Adım 5: Farklı gruplarda engel farklı yerlerdedir; doğru tanı doğru müdahaleyi gerektirir.',comp:'Direnç Yönetimi',xp:160}
,{ch:2,sc:'GlobalCorp — Sentez Karar',sit:'Danışman olarak şirkete girdiniz. Hem Kotter hem ADKAR hem Lewin uygulanmış ama değişim başarısız.',q:'Değişim başarısızlığının kök nedenini bulmak için ilk adım nedir?',opts:['Vizyonu değiştir.','Her modelin hangi basamağında kırılma olduğunu diagnostik sorularla belirle: Bireysel mi kurumsal mı?','Tüm modelleri yeniden uygula.','Dışarıdan yeni danışman getir.'],correct:1,ok:'Başarısızlığın kök nedeni bireysel ya da kurumsal kırılma noktasında gizlidir; diagnostik analiz ilk adımdır.',no:'Modeli değiştirmek veya yeniden uygulamak tanı yapılmadan işe yaramaz.',theory:'Model Entegrasyonu: Başarısızlık analizi için Kotter ADKAR ve Lewin çerçevelerinin her birinde kırılma noktası tespiti yapılır.',comp:'Analiz',xp:160}
,{ch:2,sc:'HealthNet — 3 Model Entegrasyonu',sit:"Ulusal sağlık ağında büyük sistem değişikliği. Kurumsal düzey (Kotter) çalışıyor ama bireysel benimsetme (%45) ve kültürel kalıcılık sorunlu.",q:'3 modeli nasıl entegre edersiniz?',opts:['Kotter yeterli; diğerlerine gerek yok.','Kotter = kurumsal yol haritası; ADKAR = bireysel kırılma tanısı; Lewin = kültürel geçiş ve kalıcılık; üçünü eş zamanlı uygula.','ADKAR terk et; Lewin yeterli.','Önce birini tamamla sonra diğerine geç.'],correct:1,ok:'Her model farklı düzeyde çalışır; birlikte kullanıldığında en güçlü sonuç alınır.',no:'Modelleri sıralı uygulamak değişim hızını yavaşlatır; eş zamanlı entegrasyon gerekir.',theory:'Model Entegrasyonu: Kotter kurumsal yol haritası; ADKAR bireysel tanı; Lewin kültürel geçiş. Birlikte en güçlü çerçeveyi oluşturur.',comp:'Analiz',xp:160}
,{ch:2,sc:'TechGroup — Kazanım Seçimi',sit:"Büyük teknoloji firmasında 3 yıllık dönüşüm var. Yönetim 'Kutlama kültürü oluşturalım' diyor ama hangi kazanımları kutlayacaklarını bilmiyorlar.",q:'Kutlanacak kazanım nasıl seçilmeli?',opts:['Her başarıyı kutla.','Görünür özgün değişimle açıkça ilişkili ve tartışmasız kazanımları seç; itiraz etmesi zor olacak şekilde tasarla.','Yalnızca büyük dönüm noktalarını kutla.','Kutlamaları rastgele planla.'],correct:1,ok:'Kotter Adım 6: Kazanımlar görünür, özgün ve değişimle açıkça ilişkili olmalı; şüphecilerin itiraz edemeyeceği şekilde tasarlanmalı.',no:'Her başarıyı kutlamak etkiyi sulandırır; seçici olmak kritik.',theory:'Kotter Adım 6: İyi bir kısa vadeli kazanım; görünür, belirsizliği olmayan ve değişimle açıkça ilişkilendirilebilen bir başarıdır.',comp:'Liderlik',xp:160}
,{ch:2,sc:'BankGroup — Liderlik Paradoksu',sit:'Değişim liderinin hem ivediyet hem de güven mesajı vermesi gerekiyor. Bu ikisi çelişiyor gibi görünüyor.',q:'Bu paradoksu nasıl yönetirsiniz?',opts:["İkisinden birini seç; ikisi birlikte verilemez.",'İvediyet "neden şimdi" sorusunu yanıtlar; güven "nasıl yöneteceğiz" sorusunu. İkisi farklı mesajlarda eş zamanlı verilebilir.','Önce güveni ver sonra ivediyet.','Önce ivediyet ver sonra güven.'],correct:1,ok:"İvediyet ve güven farklı mesajlardır; 'neden şimdi' ve 'nasıl yöneteceğiz' soruları eş zamanlı yanıtlanabilir.",no:'İkisini sıralı vermek değerli zaman kaybettirir; eş zamanlı mesaj verilebilir.',theory:'Kotter Adım 1+4: Aciliyet ve güven çelişmez; birlikte verilir.',comp:'Liderlik',xp:160}
,{ch:3,sc:'ConsumeCo — Sistem Entegrasyonu',sit:'Tüketici ürünleri firması başarılı dönüşüm sonrası sistemi kapattı. 1 yılda eski davranışlar döndü.',q:"Kalıcılık için gereken 'sistem değişiklikleri' nelerdir?",opts:['Sadece eğitimi tekrarla.','İşe alım kriterleri, onboarding, performans değerlendirme, terfi kararları ve bütçe tahsisi — bunların tümü yeni davranışı desteklemeli.','CEO sürekli konuşsa yeter.','Yeni çalışanlar eski kültürü taşımaz; zamanla çözülür.'],correct:1,ok:'Kalıcılık için tüm İK ve kaynak sistemleri yeni davranışı desteklemeli; yalnızca birine odaklanmak yetersiz.',no:'Tek mekanizma yeterli değil; birden fazla sistem değişikliği birlikte kalıcılık üretir.',theory:'Kotter Adım 8 + Lewin Refreezing: Kalıcılık için sistemsel çok katmanlı entegrasyon zorunludur.',comp:'Sürdürülebilirlik',xp:160}
,{ch:3,sc:'GlobalBank — Post-Merger Kültür',sit:"İki bankanın birleşmesinden sonra iki farklı kültür çarpışıyor. Her iki taraf da 'Biz haklıyız' diyor.",q:'Kültür entegrasyonunu nasıl başlatırsınız?',opts:["Büyük bankanın kültürünü egemen kıl.",'Her iki kültürden en güçlü unsurları haritalandır; ortak köprü vizyon oluştur; her iki taraftan koalisyon üyeleri dahil et.',"Küçük bankanın kültürünü koruma altına al.",'Kültürü zaman içinde organik şekilde çözülmeye bırak.'],correct:1,ok:'Kültür entegrasyonu dayatma değil ortak keşif sürecidir; köprü vizyon ve karma koalisyon kritiktir.',no:'Tek kültürü egemen kılmak ya da organik bırakmak uzun vadeli çatışma ve direnç üretir.',theory:'Lewin Unfreezing + Kotter Adım 1-2: Kültür çarpışmasında önce ortak zemin bulunur; sonra karma koalisyon ile köprü vizyon kurulur.',comp:'Değişim Yönetimi',xp:160}
,{ch:3,sc:'AutoCorp — Değişim Kültürü',sit:"Üretim firması 5 yıllık dönüşümü tamamladı. Artık değişimi 'projelerle' değil 'kültürel yetkinlikle' yönetmek istiyor.",q:'Değişim kültürü nasıl inşa edilir?',opts:['Her yıl büyük bir değişim projesi başlat.','İçsel değişim liderliği kapasitesi geliştir; değişim yönetimi yetkinliğini liderlik gelişim programlarına entegre et; çalışanları değişim şampiyonu olarak yetiştir.','Değişimi danışmanlara bırak.','Kotter adımlarını her projede tekrarla.'],correct:1,ok:'Değişim kültürü içsel kapasite geliştirmeyle inşa edilir; dışa bağımlılık azaltılmalıdır.',no:'Her projeyi sıfırdan başlatmak öğrenmeyi biriktiremez; içsel kapasite sürdürülebilir değişimi mümkün kılar.',theory:'Kotter Adım 8 + Kurumsal Öğrenme: Değişim kültürü içsel liderlik kapasitesi ve kurumsal öğrenme döngüleriyle inşa edilir.',comp:'Liderlik',xp:160}

];

</script>
<script>
// ═══════════════════════════════════════════
//  SERVICE WORKER
// ═══════════════════════════════════════════
if('serviceWorker' in navigator){
  window.addEventListener('load',()=>{
    navigator.serviceWorker.register('./sw.js').catch(()=>{});
  });
}
let deferredPrompt=null;
window.addEventListener('beforeinstallprompt',e=>{
  e.preventDefault(); deferredPrompt=e;
  document.getElementById('installBanner').classList.add('show');
});
window.addEventListener('appinstalled',()=>{
  document.getElementById('installBanner').classList.remove('show');
  deferredPrompt=null;
});
function installPWA(){
  if(!deferredPrompt) return;
  deferredPrompt.prompt();
  deferredPrompt.userChoice.then(()=>{deferredPrompt=null;});
}

// ═══════════════════════════════════════════
//  EXTRA QUESTIONS (appended to pools)
// ═══════════════════════════════════════════
const EXTRA_G=[
{ch:2,sc:'TelecomX — Kutlama Kültürü',sit:'Çağrı merkezi pilotu başarıyla tamamladı. Yönetim "Zaten yapacaktık" diyerek kutlamak istemiyor.',q:'Kısa vadeli kazanımların kutlanması neden önemli?',opts:['Kutlamalar zaman kaybıdır.','Kutlamalar koalisyonu pekiştirir; değişime inananların haklı çıktığını kanıtlar.','Kutlama yalnızca tam başarıda yapılır.','Çalışanlar motivasyon için kutlamaya ihtiyaç duymaz.'],correct:1,ok:'Kotter Adım 6: Kazanımlar değişimin mümkün olduğunun kanıtıdır; kutlanmak zorundadır.',no:'Kutlamalar moral değil stratejik araçtır; şüphecileri somut kanıtla ikna eder.',theory:'Kotter Adım 6: Kısa vadeli kazanım planlı, görünür ve değişimle açıkça ilişkili olmalı.',comp:'Liderlik',xp:80},
{ch:1,sc:'AutoGroup — Yönetici Modeli',sit:'Otomotiv firmasında yöneticiler değişimi destekliyor ama kendileri eski davranışları sürdürüyor.',q:'Bu sorunu çözmek için ne yapılmalı?',opts:['Yöneticilere ek eğitim ver.','Yönetici davranışlarını performans değerlendirme kriterlerine dahil et; değişim liderliği ölçütü ekle.','Yöneticileri değiştir.','Çalışanlara yöneticileri görmezden gelmelerini söyle.'],correct:1,ok:'Yönetici davranışları performans kriterlerine dahil edilmezse söylem-eylem açığı kapanmaz.',no:'Eğitim bilgi verir; sisteme entegrasyon davranışı değiştirir.',theory:'Kotter Adım 8: Yeni davranış performans değerlendirme ve terfi kriterlerine kazınmalıdır.',comp:'Liderlik',xp:80},
{ch:0,sc:'BankTR — Kotter Sıralaması',sit:'Yeni banka yöneticisi değişim projesini başlatmak istiyor. Vizyon hazır, ekip seçildi. Ama çalışanlar değişimin neden gerekli olduğunu bilmiyor.',q:"Kotter'a göre önce hangi adım atlanmış?",opts:['Adım 3 — Vizyon Geliştir','Adım 5 — Harekete Geç','Adım 1 — Aciliyet Duygusu Yarat','Adım 7 — Kazanımları Pekiştir'],correct:2,ok:"Aciliyet duygusu olmadan vizyon ve ekip çalışmaz. Kotter Adım 1 temeldir.",no:"Vizyon ve ekip hazır olsa da çalışanlar 'neden' sorusuna cevap bulamazsa adım 1 atlanmış demektir.",theory:"Kotter Adım 1: 'Neden değişmeliyiz?' sorusu tüm örgütte yanıtlanmadan hiçbir şey işlemez.",comp:'Vizyon',xp:80},
{ch:2,sc:'InsurPlus — Sistem Değişikliği',sit:'Sigorta şirketi yeni süreç uyguladı. Çalışanlar biliyor ve yapabiliyor ama eski alışkanlıklar zaman zaman geri dönüyor.',q:"ADKAR'da kalıcılığı sağlamak için ne yapılmalı?",opts:['Daha fazla eğitim ver.','Ödül sistemi ve KPI güncelle; yeni davranışı resmi olarak tanı ve ölç.','Ceza mekanizması kur.','Görmezden gel; zamanla düzelir.'],correct:1,ok:'Reinforcement mekanizmaları yeni davranışı pekiştirir; ödül ve tanıma sistemleri güncellenmeli.',no:"Eğitim tekrar bilgi verir; kalıcılık için yapısal pekiştirme gerekir.",theory:'ADKAR-R: Ödüller, tanıma ve hesap verebilirlik mekanizmaları olmadan eski davranışlar geri döner.',comp:'Sürdürülebilirlik',xp:80}
];

const EXTRA_S=[
{ch:0,sc:'TelcoGroup — Vizyon Paylaşımı',sit:'Büyük telekom şirketinde dönüşüm vizyonu var ama farklı departmanlar vizyonu farklı anlıyor.',q:'Bu tutarsızlığı gidermek için ne yapılmalı?',opts:['Her departmana farklı vizyon sun.','Tüm departmanlarla ortak bir vizyon çalışması yap; her birimin vizyon yorumunu hizala.','Tek bir slayt yapıp dağıt.','Departman müdürlerine bırak.'],correct:1,ok:'Vizyon hizalama çalışması tutarsız yorumları ortadan kaldırır; her birim kendi bağlamında anlam üretmeli.',no:'Dağıtım yüzeyseldir; aktif hizalama çalışması ortak anlayış üretir.',theory:'Kotter Adım 4: Vizyon iletişimi tek yönlü değil, çift yönlü anlayış üretme sürecidir.',comp:'Vizyon',xp:120},
{ch:2,sc:'HealthNet — ADKAR Katman',sit:'Sağlık ağında sistem değişikliği. Yöneticiler destekliyor, orta kademe kararsız, klinisyenler direniyor.',q:"Bu üç farklı ADKAR profilini nasıl ele alırsınız?",opts:['Hepsine aynı eğitimi ver.','Yöneticiler: Reinforcement yeterli. Orta kademe: Desire odaklı çalışma. Klinisyenler: Awareness ve Desire birlikte ele al.','Sadece klinisyenlerle çalış.','Orta kademeden başla.'],correct:1,ok:'Her katmanın ADKAR profili farklıdır; müdahale katman bazlı tasarlanmalı.',no:"Tek tip müdahale farklı ADKAR durumlarını çözmez.",theory:'ADKAR Diagnostics: Her grup için ayrı kırılma noktası tespiti ve müdahale planı şart.',comp:'Analiz',xp:120},
{ch:1,sc:'ManuPro — Koalisyon Yetki',sit:'Üretim firmasında değişim koalisyonu kuruldu ama kararlar hâlâ eski hiyerarşiyle alınıyor.',q:'Koalisyon neden işlevsiz?',opts:['Koalisyon üyeleri yanlış seçildi.','Koalisyona karar alma yetkisi verilmedi; değişimi yürüten güç merkezi olmalı.','Koalisyon çok büyük.','Toplantı sıklığı yetersiz.'],correct:1,ok:'Yetkisiz koalisyon dekoratif kalır; karar alma gücü verilmeden değişim yürütülemez.',no:'Üyelik önemli ama yetki daha kritik.',theory:'Kotter Adım 2: Koalisyon değişimi somut adımlarla ilerletme yetkisine sahip olmalı.',comp:'Liderlik',xp:120},
{ch:3,sc:'EduNet — Vizyon ve Eylem',sit:'Okul ağında güçlü bir vizyon var. Müdürler "Harika vizyon, peki ilk somut adımımız ne?" diye soruyor.',q:'Bu soruya en iyi yanıt nedir?',opts:['Vizyonu önce daha geniş kitlelere yay.','90 günlük somut eylem planı hazırla; her müdürün kendi okulunda ilk hafta yapacaklarını belirle.','Danışmanın gelmesini bekle.','Yıllık plan yapılınca başlanır.'],correct:1,ok:"Vizyon'dan eyleme geçiş 90 günlük spesifik planlarla başlar.",no:'Vizyonu yaymak önemli ama somut eylem planı olmadan vizyon havada kalır.',theory:'Kotter Adım 3+5: Vizyon somut strateji ve ilk eylemlerle desteklenmeli.',comp:'Vizyon',xp:120},
{ch:3,sc:'LogiCorp — Refreezing Mimarisi',sit:'Lojistik firması büyük bir süreç dönüşümünü başarıyla tamamladı. Yönetim artık "Bitti" diyor.',q:"Bu tutumun Lewin modeli açısından riski nedir?",opts:["'Bitti' demek normaldir; proje kapatılmalı.",'Refreezing henüz tamamlanmamış; yeni davranışlar KPI ve kültüre kazınmadan sistem bırakılırsa geri kayma kaçınılmaz.','Lewin modeli yalnızca uygulama aşamasını kapsar.','Proje kapanması Refreezing anlamına gelir.'],correct:1,ok:"Refreezing proje kapanmasıyla değil, sistem entegrasyonuyla tamamlanır.",no:"'Proje bitti = değişim kalıcı' yanılgısı Lewin'in en sık gözlenen ihlalidir.",theory:'Lewin — Refreezing: Değişim kültüre işlenmeden bitmez. Sistem, kriter ve kültür güncellemesi zorunlu.',comp:'Sürdürülebilirlik',xp:120}
];

// Append extra questions to pools
POOL_G.push(...EXTRA_G);
POOL_S.push(...EXTRA_S);

console.log('Total questions — G:',POOL_G.length,' S:',POOL_S.length,' X:',POOL_X.length,' Total:',POOL_G.length+POOL_S.length+POOL_X.length);

// ═══════════════════════════════════════════
//  CONFIG
// ═══════════════════════════════════════════
const CHAPTERS={
  g:[{i:'🌱',n:'Temel Kavramlar',s:'Kotter & ADKAR'},{i:'📋',n:'Model Uygulama',s:'Adım Analizi'},{i:'🎯',n:'Bireysel Değişim',s:'ADKAR Odak'}],
  s:[{i:'🏢',n:'Kurumsal Analiz',s:'Senaryo Kararları'},{i:'👥',n:'Paydaş & Direnç',s:'Koalisyon'},{i:'🗺️',n:'Vizyon & Strateji',s:'Yol Haritası'},{i:'🔒',n:'Kalıcılık',s:'Refreezing'}],
  x:[{i:'🔥',n:'Kriz Liderliği',s:'Çok Katmanlı'},{i:'🧩',n:'Model Sentezi',s:'Entegre Analiz'},{i:'🚀',n:'Stratejik Dönüşüm',s:'Ustalık'},{i:'👑',n:'Kalıcı Değişim',s:'Sistem Mimarisi'}]
};
const LEV={
  g:{n:'Giriş',i:'🌱',bc:'bg-g',pc:'pi-g',hc:'hg',cnt:10,pool:POOL_G},
  s:{n:'Orta', i:'⚡',bc:'bg-s',pc:'pi-s',hc:'hs',cnt:10,pool:POOL_S},
  x:{n:'Ustalık',i:'🔥',bc:'bg-x',pc:'pi-x',hc:'hx',cnt:10,pool:POOL_X}
};
const NL={g:'s',s:'x',x:null};
const RANKS=[{m:0,n:'Başlangıç'},{m:250,n:'Temsilci'},{m:500,n:'Lider'},{m:800,n:'Mimar'},{m:1200,n:'Usta'}];
const TIPS={
  g:["Kotter'ın 8 adımı sıralı uygulanır; atlama yapılamaz.","ADKAR'da kırılma noktasını bul; orada müdahale et.","Lewin'in en önemli adımı 'dondurma' — kültüre entegrasyon.","Farkındalık olmadan istek oluşmaz."],
  s:["Koalisyona orta yönetim mutlaka dahil edilmeli.","Kısa vadeli kazanımlar şüphecileri somut kanıtla ikna eder.","Vizyon 5 dakikalık 'asansör konuşması' testini geçmeli.","Değişim kapasitesi sınırlıdır; önceliklendirme kritiktir."],
  x:["Modelleri sentezle: Kotter kurumsal + ADKAR bireysel + Lewin kültürel.","Her paydaş grubunun ADKAR durumu farklı olabilir.","Kültürel değişim en uzun süren süreçtir.","Stratejik lider ivediyet ve güveni eş zamanlı yönetir."]
};

// ═══════════════════════════════════════════
//  STATE
// ═══════════════════════════════════════════
let S, curLev='g', prevPg='pg-land';

function mkState(lev){
  const cfg=LEV[lev];
  const qs=[...cfg.pool].sort(()=>Math.random()-.5).slice(0,cfg.cnt);
  return {lev,qs,qi:0,sel:null,ans:false,score:0,xp:0,streak:0,chOk:[0,0,0,0],results:[]};
}

// ═══════════════════════════════════════════
//  NAVIGATION
// ═══════════════════════════════════════════
function showPg(id){
  document.querySelectorAll('.pg').forEach(p=>p.classList.remove('on'));
  document.getElementById(id).classList.add('on');
  // scroll reset
  const sc=document.querySelector('#'+id+' .scrollable, #'+id+' .gscroll');
  if(sc) sc.scrollTop=0;
}
function goHome(){prevPg='pg-land';showPg('pg-land');}
function goModels(){prevPg=document.querySelector('.pg.on')?.id||'pg-land';showPg('pg-models');}
function goBack(){showPg(prevPg);}
function startLevel(lev){
  curLev=lev; S=mkState(lev); prevPg='pg-game';
  const cfg=LEV[lev];
  const b=document.getElementById('hudBadge');
  b.textContent=cfg.i+' '+cfg.n; b.className='hud-badge '+cfg.bc;
  const p=document.getElementById('progBar');
  p.className='prog-in '+cfg.pc; p.style.width='0%';
  showPg('pg-game'); renderAll();
}
function replaySame(){startLevel(curLev);}

// ═══════════════════════════════════════════
//  HELPERS
// ═══════════════════════════════════════════
function rank(xp){for(let i=RANKS.length-1;i>=0;i--) if(xp>=RANKS[i].m) return RANKS[i].n; return RANKS[0].n;}
function popup(msg){const e=document.getElementById('xppop');e.textContent=msg;e.classList.add('show');setTimeout(()=>e.classList.remove('show'),2200);}

// ═══════════════════════════════════════════
//  GAME ACTIONS
// ═══════════════════════════════════════════
function selectOpt(i){
  if(S.ans) return;
  S.sel=i;
  document.querySelectorAll('.opt').forEach((el,idx)=>{
    el.className='opt'+(idx===i?' osel':'');
  });
  document.getElementById('btnSub').disabled=false;
}
function submitAnswer(){
  if(S.sel===null||S.ans) return;
  S.ans=true;
  const q=S.qs[S.qi];
  const ok=S.sel===q.correct;
  S.results.push({qi:S.qi,sel:S.sel,correct:q.correct,ok,q});
  if(ok){
    S.score+=100; S.xp+=q.xp; S.streak++;
    if(q.ch<S.chOk.length) S.chOk[q.ch]++;
    popup('+'+q.xp+' XP 🎉');
  } else { S.streak=0; }
  document.getElementById('hScore').textContent=S.score;
  document.getElementById('hXP').textContent=S.xp;
  renderCenter();
}
function nextQ(){
  S.qi++; S.sel=null; S.ans=false;
  if(S.qi>=S.qs.length){showResults();return;}
  document.getElementById('gscroll').scrollTop=0;
  renderCenter(); renderHUD();
}

// ═══════════════════════════════════════════
//  RENDER
// ═══════════════════════════════════════════
function renderAll(){renderHUD();renderCenter();}
function renderHUD(){
  document.getElementById('hScore').textContent=S.score;
  document.getElementById('hXP').textContent=S.xp;
  document.getElementById('hPhase').textContent=(S.qi+1)+'/'+S.qs.length;
  document.getElementById('progBar').style.width=(S.qi/S.qs.length*100)+'%';
}
function renderCenter(){
  if(S.qi>=S.qs.length){showResults();return;}
  const q=S.qs[S.qi], cfg=LEV[S.lev], L=['A','B','C','D'];
  const ok=S.ans&&S.sel===q.correct, isLast=S.qi===S.qs.length-1;
  const tip=TIPS[S.lev][S.qi%TIPS[S.lev].length];

  const opts=q.opts.map((t,i)=>{
    let c='opt';
    if(S.ans){c+=' od';if(i===q.correct)c+=' ook';else if(i===S.sel)c+=' ono';else c+=' odim';}
    else if(i===S.sel) c+=' osel';
    const cl=S.ans?'':` onclick="selectOpt(${i})"`;
    return `<div class="${c}"${cl}><div class="oltr">${L[i]}</div><div class="otxt">${t}</div></div>`;
  }).join('');

  let fb='';
  if(S.ans){
    if(ok){
      fb=`<div class="fb fbok"><div class="fbh">✅ Harika karar!</div><div class="fbb">${q.ok}</div>
<div class="fb-th"><div class="fb-th-l">📚 Model Referansı</div><div class="fb-th-t">${q.theory}</div></div></div>`;
    } else {
      fb=`<div class="fb fbno"><div class="fbh">❌ Bu sefer olmadı!</div><div class="fbb">${q.no}</div>
<div class="fb-rev"><div class="fb-rev-l">✅ Doğru Yanıt — ${L[q.correct]}</div><div class="fb-rev-t">${q.opts[q.correct]}</div></div>
<div class="fb-th"><div class="fb-th-l">📚 Model Açıklaması</div><div class="fb-th-t">${q.theory}</div></div></div>`;
    }
  }

  document.getElementById('gscrollD').innerHTML=`
<div class="sc-hdr ${cfg.hc}">
  <div class="sc-tag">Soru ${S.qi+1}/${S.qs.length} · ${cfg.i} ${cfg.n}</div>
  <h2 class="sc-ttl">${q.sc}</h2>
  <p class="sc-sub">Durumu dikkatlice oku ve en doğru kararı ver.</p>
</div>
<div class="sit-box">
  <div class="sit-lbl">📋 Durum</div>
  <p class="sit-txt">${q.sit}</p>
</div>
<div class="q-txt">❓ ${q.q}</div>
<div class="opts">${opts}</div>
${fb}
<div class="tip"><span class="tip-t">💡 İpucu</span>${tip}</div>`;

  document.getElementById('gameBar').innerHTML=S.ans
    ?`<button class="btn-ref" onclick="goModels()">📖</button>
      <button class="btn-nxt" onclick="nextQ()">${isLast?'🏆 Sonuçları Gör':'Devam Et →'}</button>`
    :`<button class="btn-ref" onclick="goModels()">📖</button>
      <button class="btn-sub" id="btnSub" onclick="submitAnswer()" ${S.sel===null?'disabled':''}>Cevabı Gönder ✓</button>`;
}

// ═══════════════════════════════════════════
//  RESULTS
// ═══════════════════════════════════════════
function showResults(){
  const cfg=LEV[S.lev], tot=S.qs.length, cor=S.results.filter(r=>r.ok).length;
  const acc=Math.round(cor/tot*100), lv=rank(S.xp), nl=NL[S.lev];
  const chs=CHAPTERS[S.lev];
  const L=['A','B','C','D'];
  const bCls={g:'rb-g',s:'rb-s',x:'rb-x'}[S.lev];
  const nlCls={s:'nl-s',x:'nl-x'};

  const chHtml=chs.map((ch,i)=>{
    const cqs=S.qs.filter(q=>q.ch===i).length; if(!cqs) return '';
    const ok=S.chOk[i], pct=Math.round(ok/cqs*100);
    const col=pct===100?'#00D4AA':pct>=67?'#7B61FF':pct>=33?'#FF6B35':'#FF5050';
    return `<div class="ch-row"><span class="chi">${ch.i}</span><span class="chn">${ch.n}</span>
<div class="chb"><div class="chf" style="width:${pct}%;background:${col}"></div></div>
<span class="chs" style="color:${col}">${ok}/${cqs}</span></div>`;
  }).join('');

  const revHtml=S.results.map((r,idx)=>{
    const q=r.q, ok=r.ok;
    const opts=q.opts.map((t,oi)=>{
      let c='ro ';
      if(oi===q.correct)c+='ro-ok'; else if(oi===r.sel&&!ok)c+='ro-no'; else c+='ro-dim';
      return `<div class="${c}"><span class="rl">${L[oi]}.</span><span>${t}</span></div>`;
    }).join('');
    const ex=!ok
      ?`<div class="rev-ex"><strong style="color:var(--ac)">❌ Neden yanlış?</strong> ${q.no}<br><br><strong style="color:var(--ac3)">📚 Model:</strong> ${q.theory}</div>`
      :`<div class="rev-ex" style="border-color:rgba(0,212,170,.15)"><strong style="color:var(--ac2)">✅ Neden doğru?</strong> ${q.ok}</div>`;
    return `<div class="rev-c ${ok?'rev-ok':'rev-no'}">
<div class="rev-hd"><span class="rev-sc">${idx+1}. ${q.sc}</span><span class="rev-bg ${ok?'rbok':'rbno'}">${ok?'✓':'✗'}</span></div>
<div class="rev-q">${q.q}</div><div class="rev-opts">${opts}</div>${ex}</div>`;
  }).join('');

  let nlHtml='';
  if(nl&&acc>=60){
    const nlCfg=LEV[nl];
    nlHtml=`<div class="nlev ${nlCls[nl]}">
<div class="nl-t">${nlCfg.i} ${nlCfg.n} Seviyesine Geç!</div>
<div class="nl-s2">Başarın bir sonraki zorluğu hak ettiğini gösteriyor.</div>
<button class="btn-nlev" onclick="startLevel('${nl}')">Başla →</button></div>`;
  }

  document.getElementById('resInner').innerHTML=`
<div class="res-hero">
  <span class="res-trophy">${acc>=80?'🏆':acc>=60?'🥈':'🥉'}</span>
  <h2 class="res-title">${acc>=80?'🏆 Efsane!':acc>=60?'👏 İyi İş!':'💪 Gelişme Var!'}</h2>
  <p class="res-sub">${cfg.i} ${cfg.n} Seviyesi · ${lv}</p>
</div>
<div class="res-banner ${bCls}">
  <div class="rb-ico">${cfg.i}</div>
  <div class="rb-txt"><strong>${cfg.n} Seviyesi</strong> — Başarı: <strong style="color:var(--ac)">${acc}%</strong><br>XP: <strong>${S.xp}</strong> · Seviye: <strong>${lv}</strong></div>
</div>
<div class="res-stats">
  <div class="rs"><div class="rs-n" style="color:var(--gold)">${S.score}</div><div class="rs-l">Puan</div></div>
  <div class="rs"><div class="rs-n" style="color:var(--ac2)">${S.xp}</div><div class="rs-l">XP</div></div>
  <div class="rs"><div class="rs-n" style="color:var(--ac3)">${acc}%</div><div class="rs-l">Başarı</div></div>
  <div class="rs"><div class="rs-n" style="color:var(--ac)">${cor}/${tot}</div><div class="rs-l">Doğru</div></div>
</div>
<div class="res-cert"><strong>🎓 Tamamlama Belgesi</strong><br>Bu seviyeyi tamamlayarak Kotter, ADKAR ve Lewin modellerini uygulamalı olarak deneyimledin.</div>
<div class="res-sec"><div class="res-sec-t">📊 Bölüm Performansı</div>${chHtml}</div>
<div class="rot-note">🔄 <strong>Senaryo Rotasyonu:</strong> Tekrar oynadığında ${cfg.pool?cfg.pool.length:'100'} soruluk havuzdan farklı ${cfg.cnt} soru gelir.</div>
${nlHtml}
<div class="res-sec"><div class="res-sec-t">🔍 Tüm Sorular — Cevap İncelemesi</div>${revHtml}</div>`;

  prevPg='pg-res'; showPg('pg-res');
}
</script>
</body>
</html>
