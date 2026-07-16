[KOBI_Donusum_Akademisiindex.html.html](https://github.com/user-attachments/files/30090986/KOBI_Donusum_Akademisiindex.html.html)
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>KOBİ Dönüşüm Akademisi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.30.0/tabler-icons.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap">
<style>
:root{
  --navy:#0B1628; --navy-2:#0E1D35; --navy-light:#112240; --navy-card:#162A4A; --navy-card-2:#1B3257;
  --navy-border: rgba(255,255,255,0.08); --navy-border-2: rgba(255,255,255,0.14);
  --orange:#F97316; --orange-soft: rgba(249,115,22,0.15); --orange-glow: rgba(249,115,22,0.35); --orange-dark:#C2570B;
  --blue:#3B82F6; --blue-soft: rgba(59,130,246,0.13);
  --text-1:#F1F5F9; --text-2:#9FB0C5; --text-3:#64748B;
  --green:#10B981; --green-soft: rgba(16,185,129,0.13);
  --red:#EF4444; --red-soft: rgba(239,68,68,0.13);
  --purple:#8B5CF6; --purple-soft: rgba(139,92,246,0.13);
  --teal:#14B8A6; --teal-soft: rgba(20,184,166,0.13);
  --amber:#F59E0B; --amber-soft: rgba(245,158,11,0.13);
  --radius-sm:6px; --radius-md:10px; --radius-lg:14px;
}
*{box-sizing:border-box; margin:0; padding:0;}
html,body{height:100%;}
body{
  font-family:'Inter', system-ui, sans-serif;
  background: var(--navy);
  color: var(--text-1);
  min-height:100vh;
  -webkit-font-smoothing: antialiased;
}
button, input, textarea, select { font-family: inherit; }
::-webkit-scrollbar{width:5px; height:5px;}
::-webkit-scrollbar-track{background:transparent;}
::-webkit-scrollbar-thumb{background: rgba(255,255,255,0.12); border-radius:3px;}
a { color: var(--orange); text-decoration: none; }

.hidden { display: none !important; }
.pulse { animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1;} 50%{opacity:0.55;} }
.spin { animation: spin 0.8s linear infinite; display:inline-block; }
@keyframes spin { from{transform:rotate(0deg);} to{transform:rotate(360deg);} }
@keyframes fadeUp { from{opacity:0; transform:translateY(8px);} to{opacity:1; transform:translateY(0);} }
.fade-up { animation: fadeUp 0.35s ease both; }
.loading-dots::after{ content:''; animation: dots 1.2s steps(3,end) infinite; }
@keyframes dots{ 0%{content:'';} 33%{content:'.';} 66%{content:'..';} 100%{content:'...';} }
.toast-pop { animation: toastPop 0.3s cubic-bezier(.34,1.56,.64,1) both; }
@keyframes toastPop { from{opacity:0; transform: translateY(10px) scale(0.95);} to{opacity:1; transform: translateY(0) scale(1);} }

/* ============ AUTH SCREENS ============ */
#auth-root{
  min-height:100vh; display:flex; align-items:center; justify-content:center;
  background:
    radial-gradient(circle at 15% 15%, rgba(249,115,22,0.10), transparent 45%),
    radial-gradient(circle at 85% 80%, rgba(59,130,246,0.08), transparent 45%),
    var(--navy);
  padding: 24px;
}
.auth-card{
  width:100%; max-width:420px;
  background: var(--navy-light);
  border:0.5px solid var(--navy-border);
  border-radius: var(--radius-lg);
  padding: 36px 32px;
}
.auth-logo{ display:flex; align-items:center; gap:12px; margin-bottom:28px; }
.auth-logo-icon{
  width:46px; height:46px; border-radius:12px; background: var(--orange);
  display:flex; align-items:center; justify-content:center; font-size:22px; flex-shrink:0;
}
.auth-logo-text{ font-size:16px; font-weight:600; color:var(--text-1); line-height:1.3; }
.auth-logo-sub{ font-size:11px; color:var(--text-3); margin-top:1px; }
.auth-title{ font-size:20px; font-weight:600; color:var(--text-1); margin-bottom:6px; }
.auth-subtitle{ font-size:13px; color:var(--text-2); margin-bottom:24px; line-height:1.5; }
.field-group{ margin-bottom:14px; }
.field-label{ font-size:12px; color:var(--text-2); margin-bottom:6px; display:block; }
.field-input, .field-select{
  width:100%; padding:11px 14px; background: var(--navy-card);
  border:0.5px solid var(--navy-border); border-radius: var(--radius-sm);
  color: var(--text-1); font-size:13px; outline:none; transition: border-color 0.15s;
}
.field-input:focus, .field-select:focus{ border-color: var(--orange-glow); }
.field-input::placeholder{ color: var(--text-3); }
.role-pick-grid{ display:grid; grid-template-columns: 1fr 1fr 1fr; gap:8px; margin-bottom:18px; }
.role-pick{
  border:0.5px solid var(--navy-border); border-radius: var(--radius-sm); padding:12px 8px;
  text-align:center; cursor:pointer; background: var(--navy-card); transition: all 0.15s;
}
.role-pick.active{ border-color: var(--orange-glow); background: var(--orange-soft); }
.role-pick-icon{ font-size:20px; margin-bottom:4px; }
.role-pick-label{ font-size:11px; color: var(--text-2); }
.role-pick.active .role-pick-label{ color: var(--orange); }
.btn-primary{
  width:100%; padding:12px; background: var(--orange); border:none; border-radius: var(--radius-sm);
  color:white; font-size:14px; font-weight:600; cursor:pointer; transition: opacity 0.15s;
  display:flex; align-items:center; justify-content:center; gap:8px;
}
.btn-primary:hover{ opacity:0.9; }
.btn-primary:disabled{ opacity:0.5; cursor:not-allowed; }
.btn-secondary{
  width:100%; padding:11px; background:transparent; border:0.5px solid var(--navy-border-2); border-radius: var(--radius-sm);
  color: var(--text-2); font-size:13px; font-weight:500; cursor:pointer; transition: all 0.15s; margin-top:8px;
}
.btn-secondary:hover{ background: var(--navy-card); color: var(--text-1); }
.auth-switch{ text-align:center; font-size:12px; color: var(--text-3); margin-top:18px; }
.auth-switch span{ color: var(--orange); cursor:pointer; font-weight:500; }
.auth-note{
  margin-top:16px; padding:10px 12px; background: var(--blue-soft); border-radius: var(--radius-sm);
  font-size:11px; color: var(--text-2); line-height:1.5; display:flex; gap:8px;
}
.auth-note i{ color: var(--blue); font-size:14px; flex-shrink:0; margin-top:1px; }
.pending-badge{
  display:inline-flex; align-items:center; gap:6px; padding:8px 12px; border-radius: var(--radius-sm);
  background: var(--amber-soft); color: var(--amber); font-size:12px; margin-bottom:16px;
}
.field-error{ font-size:11px; color: var(--red); margin-top:4px; min-height:14px; }

/* ============ APP SHELL ============ */
.app{ display:flex; height:100vh; }
.sidebar{ width:230px; background: var(--navy-light); border-right:0.5px solid var(--navy-border); display:flex; flex-direction:column; flex-shrink:0; }
.logo-area{ padding:18px 16px 14px; border-bottom:0.5px solid var(--navy-border); }
.logo-badge{ display:flex; align-items:center; gap:10px; }
.logo-icon{ width:34px; height:34px; background: var(--orange); border-radius:9px; display:flex; align-items:center; justify-content:center; font-size:16px; flex-shrink:0; }
.logo-text{ font-size:12.5px; font-weight:600; line-height:1.3; color: var(--text-1); }
.logo-sub{ font-size:10px; color: var(--text-3); margin-top:1px; }
.user-pill{ margin:12px 16px 0; background: var(--navy-card); border-radius:8px; padding:8px 10px; display:flex; align-items:center; gap:8px; cursor:pointer; transition: border-color 0.15s; border:0.5px solid transparent; }
.user-pill:hover{ border-color: var(--navy-border-2); }
.avatar{ width:28px; height:28px; border-radius:50%; background: var(--orange-soft); border:1px solid var(--orange-glow); display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:600; color: var(--orange); flex-shrink:0; }
.user-info{ flex:1; min-width:0; }
.user-name{ font-size:12px; font-weight:500; color: var(--text-1); white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.user-role{ font-size:10px; color: var(--text-3); }
nav{ flex:1; padding:8px 12px; overflow-y:auto; }
.nav-section-label{ font-size:9px; font-weight:600; color: var(--text-3); text-transform:uppercase; letter-spacing:0.08em; padding:12px 4px 4px; }
.nav-item{ display:flex; align-items:center; gap:8px; padding:7px 8px; border-radius:7px; cursor:pointer; transition: all 0.15s; color: var(--text-2); font-size:12px; margin-bottom:1px; }
.nav-item:hover{ background: var(--navy-card); color: var(--text-1); }
.nav-item.active{ background: var(--orange-soft); color: var(--orange); }
.nav-item i{ font-size:15px; flex-shrink:0; width:16px; text-align:center; }
.nav-badge{ margin-left:auto; font-size:9px; background: var(--orange); color:white; border-radius:10px; padding:1px 6px; }
.sidebar-footer{ padding:12px 16px; border-top:0.5px solid var(--navy-border); }
.xp-bar-wrap{ margin-bottom:8px; }
.xp-label{ display:flex; justify-content:space-between; font-size:10px; color: var(--text-3); margin-bottom:4px; }
.xp-track{ height:4px; background: rgba(255,255,255,0.08); border-radius:2px; overflow:hidden; }
.xp-fill{ height:100%; background: var(--orange); border-radius:2px; transition: width 0.5s; }
.level-badge{ display:inline-flex; align-items:center; gap:4px; font-size:10px; color: var(--orange); background: var(--orange-soft); padding:3px 8px; border-radius:20px; }
.logout-link{ display:flex; align-items:center; gap:6px; font-size:11px; color: var(--text-3); margin-top:10px; cursor:pointer; transition: color 0.15s; }
.logout-link:hover{ color: var(--red); }

.main{ flex:1; display:flex; flex-direction:column; overflow:hidden; height:100vh; }
.topbar{ height:52px; border-bottom:0.5px solid var(--navy-border); display:flex; align-items:center; padding:0 20px; gap:12px; flex-shrink:0; }
.page-title{ font-size:15px; font-weight:600; color: var(--text-1); flex:1; }
.topbar-actions{ display:flex; align-items:center; gap:8px; }
.icon-btn{ width:32px; height:32px; border-radius:7px; border:0.5px solid var(--navy-border); background:transparent; display:flex; align-items:center; justify-content:center; cursor:pointer; color: var(--text-2); font-size:15px; transition: all 0.15s; position:relative; }
.icon-btn:hover{ background: var(--navy-card); color: var(--text-1); }
.ai-chat-btn{ display:flex; align-items:center; gap:6px; padding:6px 12px; border-radius:7px; background: var(--orange); border:none; color:white; font-size:12px; font-weight:600; cursor:pointer; transition: opacity 0.15s; }
.ai-chat-btn:hover{ opacity:0.9; }
.content{ flex:1; overflow-y:auto; padding:20px; }
.screen{ display:none; }
.screen.active{ display:block; }

/* generic */
.stats-row{ display:grid; grid-template-columns:repeat(4,1fr); gap:12px; margin-bottom:20px; }
.stat-card{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; padding:14px 16px; }
.stat-label{ font-size:11px; color: var(--text-3); margin-bottom:6px; display:flex; align-items:center; gap:5px; }
.stat-value{ font-size:22px; font-weight:600; color: var(--text-1); }
.stat-sub{ font-size:11px; color: var(--green); margin-top:2px; }
.dash-grid{ display:grid; grid-template-columns:1fr 1fr; gap:16px; margin-bottom:16px; }
.dash-col{ display:flex; flex-direction:column; gap:16px; }
.panel{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; padding:16px; }
.panel-header{ display:flex; align-items:center; justify-content:space-between; margin-bottom:14px; }
.panel-title{ font-size:13px; font-weight:600; color: var(--text-1); display:flex; align-items:center; gap:6px; }
.panel-title i{ font-size:15px; color: var(--orange); }
.panel-action{ font-size:11px; color: var(--blue); cursor:pointer; }
.task-item{ display:flex; align-items:center; gap:10px; padding:8px 0; border-bottom:0.5px solid var(--navy-border); cursor:pointer; }
.task-item:last-child{ border-bottom:none; }
.task-check{ width:18px; height:18px; border-radius:5px; border:1.5px solid var(--navy-border-2); display:flex; align-items:center; justify-content:center; font-size:10px; flex-shrink:0; transition: all 0.15s; }
.task-check.done{ background: var(--green); border-color: var(--green); color:white; }
.task-info{ flex:1; min-width:0; }
.task-name{ font-size:12px; color: var(--text-1); }
.task-name.done-text{ text-decoration: line-through; color: var(--text-3); }
.task-sub{ font-size:10px; color: var(--text-3); margin-top:1px; }
.task-xp{ font-size:10px; color: var(--orange); font-weight:600; flex-shrink:0; }
.progress-item{ margin-bottom:12px; }
.progress-item:last-child{ margin-bottom:0; }
.progress-label{ display:flex; justify-content:space-between; font-size:12px; color: var(--text-2); margin-bottom:5px; }
.progress-track{ height:6px; background: rgba(255,255,255,0.06); border-radius:3px; overflow:hidden; }
.progress-fill{ height:100%; border-radius:3px; transition: width 0.6s; }
.badge-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:8px; }
.badge-item{ background: var(--navy); border:0.5px solid var(--navy-border); border-radius:8px; padding:10px 8px; text-align:center; cursor:pointer; transition: transform 0.15s; }
.badge-item:hover{ transform: translateY(-2px); }
.badge-icon{ font-size:22px; margin-bottom:4px; }
.badge-name{ font-size:10px; color: var(--text-2); line-height:1.2; }
.badge-item.earned{ border-color: var(--orange-glow); background: var(--orange-soft); }
.badge-item.earned .badge-name{ color: var(--orange); }

.btn-ai{ width:100%; padding:11px; background: var(--orange); border:none; border-radius:8px; color:white; font-size:13px; font-weight:600; cursor:pointer; display:flex; align-items:center; justify-content:center; gap:6px; margin-top:4px; transition: opacity 0.15s; }
.btn-ai:hover{ opacity:0.88; }
.btn-ai:disabled{ opacity:0.5; cursor:not-allowed; }
.text-input, .text-area, .select-input{ width:100%; background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:7px; color: var(--text-1); padding:9px 12px; font-size:12px; outline:none; transition: border-color 0.15s; }
.text-input:focus, .text-area:focus, .select-input:focus{ border-color: var(--orange-glow); }
.text-area{ resize:vertical; min-height:70px; line-height:1.5; }
.text-input::placeholder, .text-area::placeholder{ color: var(--text-3); }

/* AI chat */
.ai-panel-screen{ display:flex; flex-direction:column; }
.ai-header{ background: linear-gradient(135deg, #112240, #1B3257); border-radius:10px; padding:16px; margin-bottom:14px; display:flex; align-items:center; gap:12px; }
.ai-avatar{ width:44px; height:44px; border-radius:12px; background: var(--orange); display:flex; align-items:center; justify-content:center; font-size:20px; flex-shrink:0; }
.ai-info h3{ font-size:15px; font-weight:600; color: var(--text-1); }
.ai-info p{ font-size:11px; color: var(--text-2); margin-top:2px; }
.chat-area{ overflow-y:auto; background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; padding:14px; margin-bottom:12px; min-height:300px; max-height:420px; }
.msg{ margin-bottom:12px; }
.msg-user{ text-align:right; }
.msg-bubble{ display:inline-block; max-width:88%; padding:9px 13px; border-radius:10px; font-size:12.5px; line-height:1.6; text-align:left; white-space:pre-wrap; }
.msg-user .msg-bubble{ background: var(--orange); color:white; border-radius:10px 10px 2px 10px; }
.msg-ai .msg-bubble{ background: var(--navy); color: var(--text-1); border:0.5px solid var(--navy-border); border-radius:10px 10px 10px 2px; }
.msg-sender{ font-size:10px; color: var(--text-3); margin-bottom:3px; }
.msg-user .msg-sender{ text-align:right; }
.quick-prompts{ display:flex; gap:6px; flex-wrap:wrap; margin-bottom:10px; }
.quick-prompt-btn{ font-size:11px; padding:5px 10px; border-radius:20px; border:0.5px solid var(--navy-border); background: var(--navy-card); color: var(--text-2); cursor:pointer; transition: all 0.15s; white-space:nowrap; }
.quick-prompt-btn:hover{ border-color: var(--orange-glow); color: var(--orange); }
.quick-prompt-btn.active{ background: var(--orange-soft); border-color: var(--orange-glow); color: var(--orange); }
.chat-input-row{ display:flex; gap:8px; }
.chat-input{ flex:1; padding:9px 12px; background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:8px; color: var(--text-1); font-size:12px; outline:none; transition: border-color 0.15s; }
.chat-input:focus{ border-color: var(--orange-glow); }
.send-btn{ padding:9px 14px; border-radius:8px; background: var(--orange); border:none; color:white; cursor:pointer; font-size:13px; transition: opacity 0.15s; }
.send-btn:hover{ opacity:0.85; }
.send-btn:disabled{ opacity:0.5; cursor:not-allowed; }

/* SWOT */
.swot-grid{ display:grid; grid-template-columns:1fr 1fr; gap:12px; margin-bottom:16px; }
.swot-card{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; padding:14px; }
.swot-card.s-strength{ border-top:2px solid var(--green); }
.swot-card.s-weakness{ border-top:2px solid var(--red); }
.swot-card.s-opportunity{ border-top:2px solid var(--blue); }
.swot-card.s-threat{ border-top:2px solid var(--purple); }
.swot-title{ font-size:12px; font-weight:600; margin-bottom:8px; display:flex; align-items:center; gap:5px; }
.swot-card.s-strength .swot-title{ color: var(--green); }
.swot-card.s-weakness .swot-title{ color: var(--red); }
.swot-card.s-opportunity .swot-title{ color: var(--blue); }
.swot-card.s-threat .swot-title{ color: var(--purple); }

.ai-result-box{ margin-top:16px; padding:16px; background: var(--navy-card); border:0.5px solid var(--orange-glow); border-radius:10px; }
.ai-result-label{ font-size:12px; font-weight:600; color: var(--orange); margin-bottom:10px; display:flex; align-items:center; gap:6px; justify-content:space-between; }
.ai-result-text{ font-size:12.5px; color: var(--text-2); line-height:1.75; white-space:pre-wrap; }
.copy-mini-btn{ font-size:10px; padding:4px 9px; border-radius:6px; border:0.5px solid var(--navy-border-2); background:transparent; color: var(--text-2); cursor:pointer; }
.copy-mini-btn:hover{ color: var(--orange); border-color: var(--orange-glow); }

/* Digital test */
.test-question{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; padding:18px; margin-bottom:12px; }
.test-q-text{ font-size:14px; color: var(--text-1); margin-bottom:14px; line-height:1.5; font-weight:500; }
.test-options{ display:flex; flex-direction:column; gap:7px; }
.test-option{ padding:10px 14px; border-radius:8px; border:0.5px solid var(--navy-border); background: var(--navy); color: var(--text-2); font-size:12.5px; cursor:pointer; transition: all 0.15s; text-align:left; }
.test-option:hover{ border-color: var(--orange-glow); color: var(--orange); }
.test-option.selected{ background: var(--orange-soft); border-color: var(--orange-glow); color: var(--orange); }
.q-dots{ display:flex; gap:5px; }
.q-dot{ width:8px; height:8px; border-radius:50%; background: rgba(255,255,255,0.1); transition: background 0.2s; }

/* Quiz */
.quiz-result-item{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:8px; padding:14px 16px; margin-bottom:8px; }

/* Leaderboard */
.lb-item{ display:flex; align-items:center; gap:12px; padding:10px 14px; border-radius:8px; background: var(--navy-card); border:0.5px solid var(--navy-border); margin-bottom:6px; }
.lb-rank{ width:24px; font-size:12px; font-weight:600; color: var(--text-3); text-align:center; flex-shrink:0; }
.lb-rank.gold{ color:#F59E0B; } .lb-rank.silver{ color:#94A3B8; } .lb-rank.bronze{ color:#B45309; }
.lb-avatar{ width:32px; height:32px; border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:12px; font-weight:600; flex-shrink:0; }
.lb-name{ flex:1; font-size:13px; color: var(--text-1); }
.lb-level-tag{ font-size:10px; color: var(--text-3); margin-right:8px; }
.lb-xp{ font-size:12px; font-weight:600; color: var(--orange); flex-shrink:0; }

/* Courses */
.courses-grid{ display:grid; grid-template-columns:1fr 1fr 1fr; gap:12px; }
.course-card{ background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:10px; overflow:hidden; cursor:pointer; transition: border-color 0.15s; }
.course-card:hover{ border-color: var(--orange-glow); }
.course-thumb{ height:84px; display:flex; align-items:center; justify-content:center; font-size:34px; }
.course-body{ padding:12px; }
.course-title{ font-size:12.5px; font-weight:600; color: var(--text-1); margin-bottom:4px; }
.course-meta{ font-size:10px; color: var(--text-3); margin-bottom:8px; }
.course-progress-bar{ height:3px; background: rgba(255,255,255,0.06); border-radius:2px; overflow:hidden; }
.course-progress-fill{ height:100%; background: var(--orange); border-radius:2px; }
.course-progress-label{ font-size:10px; color: var(--text-3); margin-top:4px; }
.filter-chip-row{ display:flex; gap:8px; margin-bottom:16px; flex-wrap:wrap; }

/* Modal */
.modal-overlay{ position:fixed; inset:0; background: rgba(0,0,0,0.55); display:flex; align-items:center; justify-content:center; z-index:1000; padding:20px; }
.modal-box{ background: var(--navy-light); border:0.5px solid var(--navy-border-2); border-radius:12px; max-width:560px; width:100%; max-height:85vh; overflow-y:auto; padding:24px; }
.modal-header{ display:flex; align-items:center; justify-content:space-between; margin-bottom:16px; }
.modal-title{ font-size:16px; font-weight:600; color: var(--text-1); }
.modal-close{ width:28px; height:28px; border-radius:6px; border:none; background: var(--navy-card); color: var(--text-2); cursor:pointer; font-size:16px; display:flex; align-items:center; justify-content:center; }
.modal-close:hover{ color: var(--text-1); }

/* certificate */
.cert-card{ background: linear-gradient(135deg, var(--navy-card), var(--navy-card-2)); border:1px solid var(--orange-glow); border-radius:14px; padding:28px; text-align:center; position:relative; }
.cert-seal{ font-size:38px; margin-bottom:10px; }
.cert-title-text{ font-size:11px; color: var(--text-3); letter-spacing:0.1em; text-transform:uppercase; margin-bottom:8px; }
.cert-name{ font-size:22px; font-weight:600; color: var(--text-1); margin-bottom:6px; font-family: var(--font-serif, serif); }
.cert-course{ font-size:14px; color: var(--orange); margin-bottom:14px; }
.cert-meta-row{ display:flex; justify-content:center; gap:24px; font-size:11px; color: var(--text-3); margin-top:14px; padding-top:14px; border-top:0.5px dashed var(--navy-border-2); }

/* admin */
.admin-pin-pad{ display:grid; grid-template-columns:repeat(3,1fr); gap:8px; max-width:220px; margin: 16px auto; }
.pin-key{ padding:14px; background: var(--navy-card); border:0.5px solid var(--navy-border); border-radius:8px; font-size:16px; color: var(--text-1); cursor:pointer; text-align:center; }
.pin-key:hover{ border-color: var(--orange-glow); }
.pin-dots{ display:flex; justify-content:center; gap:10px; margin:16px 0; }
.pin-dot{ width:12px; height:12px; border-radius:50%; border:1.5px solid var(--navy-border-2); }
.pin-dot.filled{ background: var(--orange); border-color: var(--orange); }
.admin-row{ display:flex; align-items:center; gap:12px; padding:10px 0; border-bottom:0.5px solid var(--navy-border); }
.admin-row:last-child{ border-bottom:none; }
.admin-approve-btn{ padding:6px 12px; background: var(--green); border:none; border-radius:6px; color:white; font-size:11px; cursor:pointer; }
.admin-reject-btn{ padding:6px 12px; background: transparent; border:0.5px solid var(--red); border-radius:6px; color: var(--red); font-size:11px; cursor:pointer; margin-left:6px; }

/* toast */
.toast{ background: var(--navy-light); border:0.5px solid var(--navy-border-2); border-radius:10px; padding:12px 16px; font-size:12px; color: var(--text-1); display:flex; align-items:center; gap:8px; box-shadow: 0 4px 16px rgba(0,0,0,0.3); min-width:200px; }
.toast i{ color: var(--orange); font-size:16px; }
.toast.success i{ color: var(--green); }
.toast.error i{ color: var(--red); }

.empty-state{ text-align:center; padding:40px 20px; color: var(--text-3); }
.empty-state i{ font-size:32px; margin-bottom:10px; display:block; opacity:0.5; }
.empty-state-text{ font-size:12px; }

/* ============ MOBİL: hamburger / drawer / bottom-nav ============ */
.hamburger-btn{ display:none; }
.sidebar-overlay{ display:none; }
.mobile-bottom-nav{ display:none; }
.drawer-close-btn{ display:none; }

@media (max-width: 980px){
  .dash-grid{ grid-template-columns:1fr; }
  .courses-grid{ grid-template-columns:1fr 1fr; }
  .swot-grid{ grid-template-columns:1fr; }
}

@media (max-width: 760px){
  body{ overflow-x:hidden; }

  /* --- Auth ekranı mobil --- */
  .auth-card{ padding:26px 20px; border-radius:12px; }
  .role-pick-grid{ grid-template-columns: 1fr 1fr 1fr; gap:6px; }
  .role-pick{ padding:10px 4px; }
  .role-pick-icon{ font-size:17px; }
  .role-pick-label{ font-size:10px; }

  /* --- App shell mobil --- */
  .app{ position:relative; height:100vh; overflow:hidden; }

  .hamburger-btn{
    display:flex; align-items:center; justify-content:center;
    width:34px; height:34px; border-radius:8px; border:0.5px solid var(--navy-border);
    background:transparent; color: var(--text-1); font-size:18px; cursor:pointer; flex-shrink:0;
  }

  .sidebar{
    position:fixed; top:0; left:0; height:100vh; width:78vw; max-width:300px;
    z-index:200; transform: translateX(-100%); transition: transform 0.25s ease;
    box-shadow: 8px 0 24px rgba(0,0,0,0.4);
  }
  .sidebar.drawer-open{ transform: translateX(0); }

  .drawer-close-btn{
    display:flex; align-items:center; justify-content:center;
    width:28px; height:28px; border-radius:7px; background: var(--navy-card);
    border:none; color: var(--text-2); font-size:15px; cursor:pointer; margin-left:auto;
  }

  .sidebar-overlay{
    display:none; position:fixed; inset:0; background: rgba(0,0,0,0.55);
    z-index:150; opacity:0; transition: opacity 0.25s ease;
  }
  .sidebar-overlay.visible{ display:block; opacity:1; }

  .main{ width:100%; }

  .topbar{ padding:0 12px; gap:8px; height:50px; }
  .page-title{ font-size:13.5px; }
  .ai-chat-btn span.ai-chat-label{ display:none; }
  .ai-chat-btn{ padding:7px 10px; }
  .icon-btn{ width:30px; height:30px; }

  .content{ padding:14px 14px 78px 14px; } /* alt boşluk bottom-nav için */

  /* bottom nav (hızlı erişim) */
  .mobile-bottom-nav{
    display:flex; position:fixed; bottom:0; left:0; right:0; z-index:120;
    background: var(--navy-light); border-top:0.5px solid var(--navy-border);
    padding: 6px 4px calc(6px + env(safe-area-inset-bottom)) 4px;
  }
  .mobile-bottom-nav-item{
    flex:1; display:flex; flex-direction:column; align-items:center; gap:2px;
    padding:6px 2px; color: var(--text-3); font-size:9.5px; cursor:pointer; border-radius:8px;
    transition: color 0.15s;
  }
  .mobile-bottom-nav-item i{ font-size:18px; }
  .mobile-bottom-nav-item.active{ color: var(--orange); }

  /* --- grids tek kolon --- */
  .stats-row{ grid-template-columns: 1fr 1fr; gap:8px; }
  .stat-card{ padding:11px 12px; }
  .stat-value{ font-size:18px; }
  .dash-grid{ grid-template-columns:1fr; gap:12px; }
  .courses-grid{ grid-template-columns: 1fr 1fr; gap:8px; }
  .swot-grid{ grid-template-columns:1fr; gap:10px; }
  .badge-grid{ grid-template-columns: repeat(3,1fr); }
  .filter-chip-row{ overflow-x:auto; flex-wrap:nowrap; padding-bottom:4px; -webkit-overflow-scrolling:touch; }
  .filter-chip-row::-webkit-scrollbar{ display:none; }
  .quick-prompts{ overflow-x:auto; flex-wrap:nowrap; padding-bottom:2px; -webkit-overflow-scrolling:touch; }
  .quick-prompts::-webkit-scrollbar{ display:none; }

  /* strategic/plan/swot inner grids -> 1 column */
  div[style*="grid-template-columns:1fr 1fr"]{ grid-template-columns:1fr !important; }
  div[style*="grid-template-columns: 1fr 1fr"]{ grid-template-columns:1fr !important; }
  div[style*="grid-template-columns:2fr 1fr 1fr"]{ grid-template-columns:1fr !important; }
  div[style*="grid-template-columns:1fr 1fr 1fr"]{ grid-template-columns:1fr !important; }

  .chat-area{ min-height:300px; max-height:50vh; }
  .ai-panel-screen{ display:flex; flex-direction:column; }
  .ai-header{ padding:12px; }
  .ai-info p{ font-size:10.5px; }

  .modal-box{ padding:18px; max-height:80vh; }
  .modal-title{ font-size:14px; }

  .cert-card{ padding:20px 16px; }
  .cert-name{ font-size:18px; }

  .admin-pin-pad{ max-width:260px; }
  .pin-key{ padding:16px; }

  .lb-item{ padding:9px 10px; gap:8px; }
  .lb-name{ font-size:12px; }
  .lb-level-tag{ display:none; }

  .test-question{ padding:14px; }
  .test-q-text{ font-size:13px; }

  /* user-pill içinde rol seçimi yoksa sorun yok */
  .user-pill{ margin:10px 14px 0; }
  .logo-area{ padding:14px 14px 12px; display:flex; align-items:center; justify-content:space-between; }
}

@media (max-width: 420px){
  .stats-row{ grid-template-columns: 1fr 1fr; }
  .courses-grid{ grid-template-columns: 1fr; }
  .badge-grid{ grid-template-columns: repeat(3,1fr); }
  .mobile-bottom-nav-item span{ font-size:9px; }
}
</style>
</head>
<body>

<!-- ============ AUTH ROOT ============ -->
<div id="auth-root">
  <div class="auth-card fade-up" id="auth-card">
    <div class="auth-logo">
      <div class="auth-logo-icon">🏛️</div>
      <div>
        <div class="auth-logo-text">KOBİ Dönüşüm Akademisi</div>
        <div class="auth-logo-sub">AI Eğitmen Asistanı</div>
      </div>
    </div>

    <!-- LOGIN FORM -->
    <div id="form-login">
      <div class="auth-title">Tekrar hoş geldiniz</div>
      <div class="auth-subtitle">Hesabınıza giriş yapın ve dönüşüm yolculuğunuza devam edin.</div>
      <div class="field-group">
        <label class="field-label">E-posta</label>
        <input type="email" class="field-input" id="login-email" placeholder="ornek@sirket.com">
      </div>
      <div class="field-group">
        <label class="field-label">Şifre</label>
        <input type="password" class="field-input" id="login-password" placeholder="••••••••">
        <div class="field-error" id="login-error"></div>
      </div>
      <button class="btn-primary" onclick="handleLogin()" id="login-btn">
        <i class="ti ti-login-2"></i> Giriş Yap
      </button>
      <div class="auth-switch">Hesabınız yok mu? <span onclick="switchAuth('register')">Kayıt Ol</span></div>
      <div class="auth-note"><i class="ti ti-info-circle"></i> Demo: herhangi bir e-posta + en az 4 karakter şifre ile giriş yapabilirsiniz. Veya hızlı demo hesaplarını kullanın.</div>
      <div style="display:flex; gap:6px; margin-top:10px;">
        <button class="btn-secondary" style="margin-top:0" onclick="quickDemo('yonetici')">Yönetici demo</button>
        <button class="btn-secondary" style="margin-top:0" onclick="quickDemo('egitmen')">Eğitmen demo</button>
        <button class="btn-secondary" style="margin-top:0" onclick="quickDemo('ogrenci')">Öğrenci demo</button>
      </div>
    </div>

    <!-- REGISTER FORM -->
    <div id="form-register" class="hidden">
      <div class="auth-title">Hesap oluştur</div>
      <div class="auth-subtitle">Birkaç adımda Akademi'ye katılın. Eğitmen ve yönetici hesapları admin onayı gerektirir.</div>
      <div class="field-group">
        <label class="field-label">Ad Soyad</label>
        <input type="text" class="field-input" id="reg-name" placeholder="Adınız Soyadınız">
      </div>
      <div class="field-group">
        <label class="field-label">Şirket / Kurum</label>
        <input type="text" class="field-input" id="reg-company" placeholder="Şirket adı (opsiyonel)">
      </div>
      <div class="field-group">
        <label class="field-label">E-posta</label>
        <input type="email" class="field-input" id="reg-email" placeholder="ornek@sirket.com">
      </div>
      <div class="field-group">
        <label class="field-label">Şifre</label>
        <input type="password" class="field-input" id="reg-password" placeholder="En az 4 karakter">
        <div class="field-error" id="reg-error"></div>
      </div>
      <label class="field-label">Kullanıcı tipi</label>
      <div class="role-pick-grid">
        <div class="role-pick active" data-role="ogrenci" onclick="pickRole(this,'ogrenci')">
          <div class="role-pick-icon">🎓</div><div class="role-pick-label">Öğrenci</div>
        </div>
        <div class="role-pick" data-role="egitmen" onclick="pickRole(this,'egitmen')">
          <div class="role-pick-icon">👨‍🏫</div><div class="role-pick-label">Eğitmen</div>
        </div>
        <div class="role-pick" data-role="yonetici" onclick="pickRole(this,'yonetici')">
          <div class="role-pick-icon">💼</div><div class="role-pick-label">KOBİ Yöneticisi</div>
        </div>
      </div>
      <button class="btn-primary" onclick="handleRegister()" id="register-btn">
        <i class="ti ti-user-plus"></i> Kayıt Ol
      </button>
      <div class="auth-switch">Zaten hesabınız var mı? <span onclick="switchAuth('login')">Giriş Yap</span></div>
    </div>

    <!-- PENDING APPROVAL -->
    <div id="form-pending" class="hidden" style="text-align:center;">
      <div style="font-size:40px; margin-bottom:12px;">⏳</div>
      <div class="auth-title">Onay bekleniyor</div>
      <div class="auth-subtitle" id="pending-text">Hesabınız oluşturuldu. Eğitmen/Yönetici hesapları için admin onayı gerekiyor.</div>
      <button class="btn-secondary" onclick="switchAuth('login')">Giriş ekranına dön</button>
      <div class="auth-note"><i class="ti ti-bulb"></i> Demo amaçlı: admin panelinden (PIN: 1234) bu hesabı onaylayabilir ya da doğrudan demo hesaplarıyla giriş yapabilirsiniz.</div>
    </div>
  </div>
</div>

<!-- ============ MAIN APP ROOT ============ -->
<div id="app-root" class="hidden"></div>

<!-- ============ TOAST CONTAINER ============ -->
<div id="toast-container" style="position:fixed; bottom:20px; right:20px; z-index:9999; display:flex; flex-direction:column; gap:8px; align-items:flex-end;"></div>

<script>
/* ===================================================================
   KOBİ DÖNÜŞÜM AKADEMİSİ — Tek Dosya Uygulama Mantığı
   Veri katmanı: localStorage (gerçek Firebase yerine demo persistans)
   AI katmanı: Anthropic Messages API (kullanıcının kendi API anahtarı ile)
=================================================================== */

const DB_KEY = 'kobi_akademi_db_v1';
const SESSION_KEY = 'kobi_akademi_session_v1';

/* ---------- Varsayılan veritabanı (Firebase koleksiyonlarının yerel karşılığı) ---------- */
function defaultDB(){
  return {
    users: [
      { id:'u_admin', name:'Sistem Admin', email:'admin@akademi.com', password:'admin', role:'admin', status:'approved', xp:0, level:'Usta', streak:0, badges:[], createdAt: Date.now() },
      { id:'u_demo_yonetici', name:'Ayşe Yılmaz', email:'yonetici@demo.com', password:'demo', role:'yonetici', status:'approved', company:'Yılmaz Tekstil A.Ş.', xp:1280, level:'Uzman', streak:12, badges:['girisimci','ai-uzmani','donusum-lideri'], createdAt: Date.now() },
      { id:'u_demo_egitmen', name:'Mehmet Kaya', email:'egitmen@demo.com', password:'demo', role:'egitmen', status:'approved', xp:3450, level:'Usta', streak:30, badges:['girisimci','ai-uzmani','donusum-lideri','egitmen-ustasi'], createdAt: Date.now() },
      { id:'u_demo_ogrenci', name:'Zeynep Kurt', email:'ogrenci@demo.com', password:'demo', role:'ogrenci', status:'approved', xp:980, level:'Kaşif', streak:5, badges:['girisimci'], createdAt: Date.now() },
      { id:'u_demo2', name:'Fatma Demir', email:'fatma@demo.com', password:'demo', role:'yonetici', status:'approved', xp:2980, level:'Lider', streak:21, badges:['girisimci','ai-uzmani'], createdAt: Date.now() },
      { id:'u_demo3', name:'Ali Çelik', email:'ali@demo.com', password:'demo', role:'yonetici', status:'approved', xp:2100, level:'Uzman', streak:8, badges:['girisimci'], createdAt: Date.now() }
    ],
    companies: [],
    swotAnalyses: [],
    digitalAssessments: [],
    strategicPlans: [],
    aiChats: [],
    courses: [
      { id:'c1', title:'Girişimcilik Temelleri', category:'Girişimcilik', icon:'🚀', color:'orange', lessons:12, hours:6, level:'Başlangıç' },
      { id:'c2', title:'Yapay Zekâ Yönetimi', category:'Yapay Zekâ', icon:'🤖', color:'blue', lessons:8, hours:4, level:'Orta' },
      { id:'c3', title:'Stratejik Planlama', category:'Strateji', icon:'🎯', color:'purple', lessons:10, hours:5, level:'Orta' },
      { id:'c4', title:'Dijital Dönüşüm', category:'Dijital Dönüşüm', icon:'🔄', color:'teal', lessons:15, hours:8, level:'İleri' },
      { id:'c5', title:'Takım Liderliği', category:'Liderlik', icon:'👥', color:'green', lessons:9, hours:4.5, level:'Başlangıç' },
      { id:'c6', title:'KPI & Performans Yönetimi', category:'Strateji', icon:'📊', color:'amber', lessons:6, hours:3, level:'Başlangıç' }
    ],
    courseProgress: {
      'u_demo_yonetici': { c1:100, c2:45, c3:32, c4:78, c5:60, c6:0 },
      'u_demo_egitmen': { c1:100, c2:100, c3:90, c4:100, c5:100, c6:80 },
      'u_demo_ogrenci': { c1:60, c2:20, c3:0, c4:10, c5:0, c6:0 }
    },
    tasks: {
      'u_demo_yonetici': [
        { id:'t1', name:'SWOT analizini tamamla', sub:'KOBİ Merkezi', xp:50, done:true },
        { id:'t2', name:'Dijital olgunluk testini çöz', sub:'Değerlendirme', xp:80, done:false },
        { id:'t3', name:'Hadi AI ile 1 soru sor', sub:'AI Danışman', xp:20, done:false },
        { id:'t4', name:'Stratejik Plan modülü aç', sub:'Planlama', xp:30, done:false }
      ]
    },
    badgesCatalog: [
      { id:'girisimci', name:'Girişimci', icon:'🚀', desc:'İlk eğitimini tamamladın' },
      { id:'ai-uzmani', name:'AI Uzmanı', icon:'🤖', desc:'10 kez Hadi AI kullandın' },
      { id:'donusum-lideri', name:'Dönüşüm Lideri', icon:'🔄', desc:'Dijital dönüşüm modülünü tamamladın' },
      { id:'egitmen-ustasi', name:'Eğitmen Ustası', icon:'🏆', desc:'5 eğitim tasarladın' },
      { id:'strateji-master', name:'Strateji Master', icon:'⭐', desc:'3 stratejik plan oluşturdun' },
      { id:'analiz-uzmani', name:'Analiz Uzmanı', icon:'🧠', desc:'5 SWOT analizi yaptın' }
    ],
    quizzes: [],
    cases: [],
    gamificationDesigns: [],
    lessonPlans: [],
    certificates: [
      { id:'cert1', userId:'u_demo_yonetici', courseTitle:'Girişimcilik Temelleri', date:'12 Mayıs 2026', certNo:'KDA-2026-0142' }
    ],
    settings: { adminPin: '1234' }
  };
}

function loadDB(){
  try{
    const raw = localStorage.getItem(DB_KEY);
    if(!raw) { const db = defaultDB(); saveDB(db); return db; }
    return JSON.parse(raw);
  }catch(e){
    const db = defaultDB(); saveDB(db); return db;
  }
}
function saveDB(db){ localStorage.setItem(DB_KEY, JSON.stringify(db)); }

let DB = loadDB();
let SESSION = JSON.parse(localStorage.getItem(SESSION_KEY) || 'null');

function currentUser(){
  if(!SESSION) return null;
  return DB.users.find(u => u.id === SESSION.userId) || null;
}

function uid(prefix){ return prefix + '_' + Math.random().toString(36).slice(2,10); }

/* ---------- Toast ---------- */
function toast(msg, type){
  type = type || 'default';
  const c = document.getElementById('toast-container');
  const el = document.createElement('div');
  el.className = 'toast toast-pop ' + type;
  const icon = type === 'success' ? 'ti-check' : (type === 'error' ? 'ti-alert-circle' : 'ti-info-circle');
  el.innerHTML = `<i class="ti ${icon}"></i><span>${escapeHtml(msg)}</span>`;
  c.appendChild(el);
  setTimeout(() => { el.style.transition = 'opacity 0.3s'; el.style.opacity = '0'; setTimeout(()=>el.remove(), 300); }, 2800);
}

function escapeHtml(str){
  const d = document.createElement('div');
  d.textContent = str;
  return d.innerHTML;
}

/* ---------- AUTH ---------- */
function switchAuth(which){
  document.getElementById('form-login').classList.toggle('hidden', which !== 'login');
  document.getElementById('form-register').classList.toggle('hidden', which !== 'register');
  document.getElementById('form-pending').classList.toggle('hidden', which !== 'pending');
  const errL = document.getElementById('login-error'); if(errL) errL.textContent='';
  const errR = document.getElementById('reg-error'); if(errR) errR.textContent='';
}

let pickedRole = 'ogrenci';
function pickRole(el, role){
  document.querySelectorAll('.role-pick').forEach(r => r.classList.remove('active'));
  el.classList.add('active');
  pickedRole = role;
}

function handleLogin(){
  const email = document.getElementById('login-email').value.trim().toLowerCase();
  const pass = document.getElementById('login-password').value;
  const errEl = document.getElementById('login-error');
  if(!email || !pass){ errEl.textContent = 'E-posta ve şifre gerekli.'; return; }
  const user = DB.users.find(u => u.email.toLowerCase() === email);
  if(!user){ errEl.textContent = 'Bu e-posta ile kayıtlı kullanıcı bulunamadı.'; return; }
  if(user.password !== pass){ errEl.textContent = 'Şifre yanlış.'; return; }
  if(user.status === 'pending'){
    document.getElementById('pending-text').textContent = 'Hesabınız ' + roleLabel(user.role) + ' olarak kayıtlı ve admin onayı bekliyor.';
    switchAuth('pending');
    return;
  }
  if(user.status === 'rejected'){ errEl.textContent = 'Hesap başvurunuz onaylanmadı. Lütfen yönetici ile iletişime geçin.'; return; }
  errEl.textContent = '';
  loginAs(user.id);
}

function quickDemo(role){
  const map = { yonetici:'yonetici@demo.com', egitmen:'egitmen@demo.com', ogrenci:'ogrenci@demo.com' };
  const user = DB.users.find(u => u.email === map[role]);
  if(user) loginAs(user.id);
}

function handleRegister(){
  const name = document.getElementById('reg-name').value.trim();
  const company = document.getElementById('reg-company').value.trim();
  const email = document.getElementById('reg-email').value.trim().toLowerCase();
  const pass = document.getElementById('reg-password').value;
  const errEl = document.getElementById('reg-error');
  if(!name || !email || pass.length < 4){ errEl.textContent = 'Ad, e-posta ve en az 4 karakterli şifre gerekli.'; return; }
  if(DB.users.some(u => u.email.toLowerCase() === email)){ errEl.textContent = 'Bu e-posta zaten kayıtlı.'; return; }
  errEl.textContent = '';

  const needsApproval = pickedRole === 'egitmen' || pickedRole === 'yonetici';
  const newUser = {
    id: uid('u'), name, email, password: pass, role: pickedRole,
    status: needsApproval ? 'pending' : 'approved',
    company: company || null,
    xp: 0, level: 'Başlangıç', streak: 0, badges: [], createdAt: Date.now()
  };
  DB.users.push(newUser);
  saveDB(DB);

  if(needsApproval){
    document.getElementById('pending-text').textContent = roleLabel(pickedRole) + ' hesabınız oluşturuldu ve admin onayına gönderildi.';
    switchAuth('pending');
    toast('Kayıt başvurunuz alındı, onay bekleniyor.', 'success');
  } else {
    loginAs(newUser.id);
    toast('Hesabınız oluşturuldu, hoş geldiniz!', 'success');
  }
}

function roleLabel(role){
  return { yonetici:'KOBİ Yöneticisi', egitmen:'Eğitmen', ogrenci:'Öğrenci/Katılımcı', admin:'Admin' }[role] || role;
}

function loginAs(userId){
  SESSION = { userId };
  localStorage.setItem(SESSION_KEY, JSON.stringify(SESSION));
  document.getElementById('auth-root').classList.add('hidden');
  document.getElementById('app-root').classList.remove('hidden');
  renderApp();
}

function logout(){
  SESSION = null;
  localStorage.removeItem(SESSION_KEY);
  document.getElementById('app-root').classList.add('hidden');
  document.getElementById('auth-root').classList.remove('hidden');
  switchAuth('login');
}

/* ---------- Boot ---------- */
document.addEventListener('DOMContentLoaded', () => {
  if(SESSION && currentUser()){
    document.getElementById('auth-root').classList.add('hidden');
    document.getElementById('app-root').classList.remove('hidden');
    renderApp();
  }
});

/* ===================================================================
   AI KATMANI — Anthropic Messages API çağrıları
   NOT: Bu uygulama Claude.ai Artifact ortamında çalıştığı için
   api.anthropic.com isteği proxy üzerinden geçer ve API anahtarı
   GEREKMEZ. Kullanıcıdan hiçbir anahtar istenmez.
=================================================================== */

const AI_SYSTEM_PROMPT = `Sen "Hadi AI" adında, KOBİ Dönüşüm Akademisi'nin yapay zekâ danışmanısın. Aşağıdaki uzmanlık alanlarında hizmet veriyorsun:
- SWOT Analiz Uzmanı: Güçlü/zayıf yön, fırsat/tehdit analizleri yapar, stratejik öneriler sunarsın.
- Stratejik Plan Uzmanı: Misyon, vizyon, hedef ve KPI önerileri sunarsın.
- Eğitim Tasarım Uzmanı: Eğitim akışı, öğrenme hedefleri, aktivite önerileri üretirsin.
- Oyunlaştırma Uzmanı: Rozet, görev, puan sistemi ve takım yarışması tasarımları üretirsin.
- Quiz Uzmanı: Çoktan seçmeli, doğru/yanlış ve vaka sorularını cevap anahtarıyla üretirsin.
- KOBİ Danışmanı: Verimlilik, satış, dijitalleşme gibi konularda pratik öneriler sunarsın.

Kurallar:
- Her zaman Türkçe yanıt ver.
- Kısa, aksiyon odaklı, madde işaretli ve uygulanabilir cevaplar ver.
- Kurumsal ama samimi bir ton kullan.
- Gerektiğinde başlıklar kullan ama gereksiz uzatma.
- Sayısal öneriler (KPI, hedef gibi) verirken gerçekçi ve ölçülebilir ol.`;

async function callClaudeAPI(userPrompt, opts){
  opts = opts || {};

  const res = await fetch('https://api.anthropic.com/v1/messages', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      model: 'claude-sonnet-4-6',
      max_tokens: opts.maxTokens || 1200,
      system: opts.system || AI_SYSTEM_PROMPT,
      messages: [{ role: 'user', content: userPrompt }]
    })
  });

  if(!res.ok){
    const errText = await res.text().catch(()=> '');
    throw new Error('AI servisi hata döndü (' + res.status + '): ' + errText.slice(0,200));
  }
  const data = await res.json();
  const textBlock = (data.content || []).find(b => b.type === 'text');
  return textBlock ? textBlock.text : 'Yanıt alınamadı.';
}

/* Network/servis hatası durumunda kullanıcıya net mesaj döndüren sarmalayıcı */
async function safeAICall(prompt, opts){
  try{
    return await callClaudeAPI(prompt, opts);
  }catch(e){
    console.error(e);
    return '⚠️ AI servisine bağlanırken bir hata oluştu. Lütfen tekrar deneyin. (' + (e.message || '') + ')';
  }
}

/* ===================================================================
   UYGULAMA KABUĞU (SHELL) — sidebar + topbar + içerik alanı
=================================================================== */

const NAV_ITEMS = {
  yonetici: [
    { section:'Ana', items:[ {id:'dashboard', icon:'ti-layout-dashboard', label:'Dashboard'} ] },
    { section:'KOBİ Dönüşüm Merkezi', items:[
      {id:'swot', icon:'ti-chart-radar', label:'SWOT Analizi'},
      {id:'digital-test', icon:'ti-device-analytics', label:'Dijital Olgunluk'},
      {id:'strategic', icon:'ti-target', label:'Stratejik Plan'},
    ]},
    { section:'AI Danışman', items:[ {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'} ] },
    { section:'Akademi', items:[
      {id:'courses', icon:'ti-school', label:'Eğitimler'},
      {id:'certificates', icon:'ti-certificate', label:'Sertifikalarım'},
      {id:'leaderboard', icon:'ti-trophy', label:'Liderboard'},
      {id:'reports', icon:'ti-report', label:'Raporlama'},
    ]}
  ],
  egitmen: [
    { section:'Ana', items:[ {id:'dashboard', icon:'ti-layout-dashboard', label:'Dashboard'} ] },
    { section:'AI Eğitmen Asistanı', items:[
      {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'},
      {id:'lesson-designer', icon:'ti-bulb', label:'Eğitim Tasarımcısı'},
      {id:'gamify-designer', icon:'ti-puzzle', label:'Oyunlaştırma Tasarımcısı'},
      {id:'quiz-maker', icon:'ti-question-mark', label:'Quiz Oluşturucu'},
      {id:'case-generator', icon:'ti-briefcase', label:'Vaka Analizi Üretici'},
    ]},
    { section:'Akademi', items:[
      {id:'courses', icon:'ti-school', label:'Eğitimler'},
      {id:'participants', icon:'ti-users', label:'Katılımcılar'},
      {id:'leaderboard', icon:'ti-trophy', label:'Liderboard'},
      {id:'reports', icon:'ti-report', label:'Raporlama'},
    ]}
  ],
  ogrenci: [
    { section:'Ana', items:[ {id:'dashboard', icon:'ti-layout-dashboard', label:'Dashboard'} ] },
    { section:'Akademi', items:[
      {id:'courses', icon:'ti-school', label:'Eğitimler'},
      {id:'quiz-maker', icon:'ti-question-mark', label:'Quiz Çöz'},
      {id:'certificates', icon:'ti-certificate', label:'Sertifikalarım'},
      {id:'leaderboard', icon:'ti-trophy', label:'Liderboard'},
    ]},
    { section:'AI Danışman', items:[ {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'} ] }
  ],
  admin: [
    { section:'Ana', items:[ {id:'dashboard', icon:'ti-layout-dashboard', label:'Dashboard'} ] },
    { section:'Yönetim', items:[
      {id:'admin-panel', icon:'ti-shield-lock', label:'Admin Panel'},
      {id:'participants', icon:'ti-users', label:'Tüm Kullanıcılar'},
      {id:'reports', icon:'ti-report', label:'Raporlama'},
    ]},
    { section:'AI Danışman', items:[ {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'} ] }
  ]
};

const PAGE_TITLES = {
  'dashboard':'Dashboard', 'ai-chat':'Hadi AI — İş & Eğitim Danışmanı', 'swot':'SWOT Analizi',
  'digital-test':'Dijital Olgunluk Testi', 'strategic':'Stratejik Plan Oluşturucu',
  'lesson-designer':'Eğitim Tasarımcısı', 'gamify-designer':'Oyunlaştırma Tasarımcısı',
  'quiz-maker':'Quiz Oluşturucu', 'case-generator':'Vaka Analizi Üretici',
  'courses':'Eğitim Akademisi', 'certificates':'Sertifikalarım', 'leaderboard':'Liderboard',
  'reports':'Raporlama', 'participants':'Katılımcı Yönetimi', 'admin-panel':'Admin Panel'
};

let currentScreen = 'dashboard';

function initials(name){
  return name.split(' ').map(p=>p[0]).slice(0,2).join('').toUpperCase();
}

function xpToLevel(xp){
  if(xp < 200) return {level:'Başlangıç', next:200, floor:0};
  if(xp < 600) return {level:'Kaşif', next:600, floor:200};
  if(xp < 1500) return {level:'Uzman', next:1500, floor:600};
  if(xp < 3000) return {level:'Lider', next:3000, floor:1500};
  return {level:'Usta', next: xp + 1000, floor:3000};
}

function addXP(amount, badgeCheck){
  const user = currentUser();
  if(!user) return;
  user.xp = (user.xp || 0) + amount;
  const lv = xpToLevel(user.xp);
  user.level = lv.level;
  saveDB(DB);
  renderSidebarFooter();
  if(badgeCheck) checkBadges(user);
}

function awardBadge(badgeId){
  const user = currentUser();
  if(!user) return;
  if(!user.badges) user.badges = [];
  if(!user.badges.includes(badgeId)){
    user.badges.push(badgeId);
    saveDB(DB);
    const badge = DB.badgesCatalog.find(b=>b.id===badgeId);
    if(badge) toast('Yeni rozet kazandın: ' + badge.name + ' ' + badge.icon, 'success');
  }
}

function checkBadges(user){
  // basit demo kuralları
  const swotCount = DB.swotAnalyses.filter(s=>s.userId===user.id).length;
  if(swotCount >= 1) awardBadge('girisimci');
  if(swotCount >= 5) awardBadge('analiz-uzmani');
  const chatCount = DB.aiChats.filter(c=>c.userId===user.id).length;
  if(chatCount >= 10) awardBadge('ai-uzmani');
  const plansCount = DB.strategicPlans.filter(p=>p.userId===user.id).length;
  if(plansCount >= 3) awardBadge('strateji-master');
  const lessonsCount = DB.lessonPlans.filter(l=>l.userId===user.id).length;
  if(lessonsCount >= 5) awardBadge('egitmen-ustasi');
}

function renderApp(){
  const user = currentUser();
  if(!user) return logout();
  const root = document.getElementById('app-root');
  root.innerHTML = `
    <div class="app">
      <div class="sidebar-overlay" id="sidebar-overlay" onclick="closeDrawer()"></div>
      <aside class="sidebar" id="sidebar">
        <div class="logo-area">
          <div class="logo-badge">
            <div class="logo-icon">🏛️</div>
            <div>
              <div class="logo-text">KOBİ Dönüşüm</div>
              <div class="logo-sub">Akademisi</div>
            </div>
          </div>
          <button class="drawer-close-btn" onclick="closeDrawer()"><i class="ti ti-x"></i></button>
        </div>
        <div class="user-pill" onclick="openProfileModal()">
          <div class="avatar">${initials(user.name)}</div>
          <div class="user-info">
            <div class="user-name">${escapeHtml(user.name)}</div>
            <div class="user-role">${roleLabel(user.role)}</div>
          </div>
          <i class="ti ti-chevron-right" style="color:var(--text-3); font-size:13px;"></i>
        </div>
        <nav id="nav-container"></nav>
        <div class="sidebar-footer" id="sidebar-footer"></div>
      </aside>
      <main class="main">
        <div class="topbar">
          <button class="hamburger-btn" onclick="openDrawer()"><i class="ti ti-menu-2"></i></button>
          <div class="page-title" id="page-title">Dashboard</div>
          <div class="topbar-actions">
            <button class="icon-btn" title="Bildirimler"><i class="ti ti-bell"></i></button>
            <button class="ai-chat-btn" onclick="navigateTo('ai-chat')"><i class="ti ti-sparkles"></i> <span class="ai-chat-label">Hadi AI</span></button>
          </div>
        </div>
        <div class="content" id="content-area"></div>
        <div class="mobile-bottom-nav" id="mobile-bottom-nav"></div>
      </main>
    </div>
  `;
  renderNav(user.role);
  renderSidebarFooter();
  renderMobileBottomNav(user.role);
  navigateTo('dashboard');
}

const MOBILE_NAV_MAP = {
  yonetici: [
    {id:'dashboard', icon:'ti-layout-dashboard', label:'Ana Sayfa'},
    {id:'swot', icon:'ti-chart-radar', label:'SWOT'},
    {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'},
    {id:'courses', icon:'ti-school', label:'Eğitim'},
    {id:'leaderboard', icon:'ti-trophy', label:'Lider'}
  ],
  egitmen: [
    {id:'dashboard', icon:'ti-layout-dashboard', label:'Ana Sayfa'},
    {id:'lesson-designer', icon:'ti-bulb', label:'Tasarım'},
    {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'},
    {id:'quiz-maker', icon:'ti-question-mark', label:'Quiz'},
    {id:'participants', icon:'ti-users', label:'Katılımcı'}
  ],
  ogrenci: [
    {id:'dashboard', icon:'ti-layout-dashboard', label:'Ana Sayfa'},
    {id:'courses', icon:'ti-school', label:'Eğitim'},
    {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'},
    {id:'certificates', icon:'ti-certificate', label:'Sertifika'},
    {id:'leaderboard', icon:'ti-trophy', label:'Lider'}
  ],
  admin: [
    {id:'dashboard', icon:'ti-layout-dashboard', label:'Ana Sayfa'},
    {id:'admin-panel', icon:'ti-shield-lock', label:'Admin'},
    {id:'ai-chat', icon:'ti-robot', label:'Hadi AI'},
    {id:'participants', icon:'ti-users', label:'Kullanıcı'},
    {id:'reports', icon:'ti-report', label:'Rapor'}
  ]
};

function renderMobileBottomNav(role){
  const items = MOBILE_NAV_MAP[role] || MOBILE_NAV_MAP.ogrenci;
  const nav = document.getElementById('mobile-bottom-nav');
  if(!nav) return;
  nav.innerHTML = items.map(it => `
    <div class="mobile-bottom-nav-item" data-bottom-screen="${it.id}" onclick="navigateTo('${it.id}')">
      <i class="ti ${it.icon}"></i><span>${it.label}</span>
    </div>
  `).join('');
}

function openDrawer(){
  document.getElementById('sidebar').classList.add('drawer-open');
  document.getElementById('sidebar-overlay').classList.add('visible');
}
function closeDrawer(){
  document.getElementById('sidebar').classList.remove('drawer-open');
  document.getElementById('sidebar-overlay').classList.remove('visible');
}

function renderNav(role){
  const sections = NAV_ITEMS[role] || NAV_ITEMS.ogrenci;
  const nav = document.getElementById('nav-container');
  nav.innerHTML = sections.map(sec => `
    <div class="nav-section-label">${sec.section}</div>
    ${sec.items.map(it => `
      <div class="nav-item" data-screen="${it.id}" onclick="navigateTo('${it.id}')">
        <i class="ti ${it.icon}"></i> ${it.label}
      </div>
    `).join('')}
  `).join('');
}

function renderSidebarFooter(){
  const user = currentUser();
  if(!user) return;
  const lv = xpToLevel(user.xp || 0);
  const pct = Math.min(100, Math.round(((user.xp - lv.floor) / (lv.next - lv.floor)) * 100));
  const footer = document.getElementById('sidebar-footer');
  if(!footer) return;
  footer.innerHTML = `
    <div class="xp-bar-wrap">
      <div class="xp-label"><span>${lv.level}</span><span>${(user.xp||0).toLocaleString('tr-TR')} XP</span></div>
      <div class="xp-track"><div class="xp-fill" style="width:${pct}%"></div></div>
    </div>
    <div class="level-badge"><i class="ti ti-star" style="font-size:11px"></i> ${lv.level} Seviyesi</div>
    <div class="logout-link" onclick="logout()"><i class="ti ti-logout"></i> Çıkış yap</div>
  `;
}

function navigateTo(screenId){
  currentScreen = screenId;
  document.querySelectorAll('.nav-item').forEach(n => n.classList.toggle('active', n.dataset.screen === screenId));
  document.querySelectorAll('.mobile-bottom-nav-item').forEach(n => n.classList.toggle('active', n.dataset.bottomScreen === screenId));
  document.getElementById('page-title').textContent = PAGE_TITLES[screenId] || screenId;
  const content = document.getElementById('content-area');
  content.innerHTML = '<div class="fade-up">' + renderScreen(screenId) + '</div>';
  afterScreenRender(screenId);
  closeDrawer();
  content.scrollTop = 0;
}

function renderScreen(id){
  const user = currentUser();
  switch(id){
    case 'dashboard': return renderDashboard(user);
    case 'ai-chat': return renderAIChat();
    case 'swot': return renderSwot();
    case 'digital-test': return renderDigitalTest();
    case 'strategic': return renderStrategic();
    case 'lesson-designer': return renderLessonDesigner();
    case 'gamify-designer': return renderGamifyDesigner();
    case 'quiz-maker': return renderQuizMaker();
    case 'case-generator': return renderCaseGenerator();
    case 'courses': return renderCourses(user);
    case 'certificates': return renderCertificates(user);
    case 'leaderboard': return renderLeaderboard(user);
    case 'reports': return renderReports(user);
    case 'participants': return renderParticipants();
    case 'admin-panel': return renderAdminPanelEntry();
    default: return '<div class="empty-state"><i class="ti ti-mood-empty"></i><div class="empty-state-text">Bu ekran henüz yok.</div></div>';
  }
}

function afterScreenRender(id){
  if(id === 'digital-test') initDigitalTest();
  if(id === 'ai-chat') initAIChatScroll();
}

/* ===================================================================
   DASHBOARD
=================================================================== */

function renderDashboard(user){
  const tasks = (DB.tasks[user.id] || defaultTasksFor(user)).slice();
  const doneCount = tasks.filter(t=>t.done).length;
  const progress = DB.courseProgress[user.id] || {};
  const courseRows = DB.courses.map(c => ({...c, pct: progress[c.id] || 0}))
    .sort((a,b)=> b.pct - a.pct).slice(0,5);
  const earnedBadges = user.badges || [];
  const allBadges = DB.badgesCatalog;

  return `
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-label"><i class="ti ti-flame" style="color:var(--orange);font-size:13px"></i> Günlük Seri</div>
        <div class="stat-value">${user.streak || 0}</div>
        <div class="stat-sub">gün üst üste</div>
      </div>
      <div class="stat-card">
        <div class="stat-label"><i class="ti ti-certificate" style="color:var(--teal);font-size:13px"></i> Sertifika</div>
        <div class="stat-value">${DB.certificates.filter(c=>c.userId===user.id).length}</div>
        <div class="stat-sub">kazanılan</div>
      </div>
      <div class="stat-card">
        <div class="stat-label"><i class="ti ti-checklist" style="color:var(--blue);font-size:13px"></i> Görevler</div>
        <div class="stat-value">${doneCount}/${tasks.length}</div>
        <div class="stat-sub">bugün tamamlandı</div>
      </div>
      <div class="stat-card">
        <div class="stat-label"><i class="ti ti-coin" style="color:var(--amber);font-size:13px"></i> XP Puanı</div>
        <div class="stat-value">${(user.xp||0).toLocaleString('tr-TR')}</div>
        <div class="stat-sub">${xpToLevel(user.xp||0).level} seviyesi</div>
      </div>
    </div>

    <div class="dash-grid">
      <div class="dash-col">
        <div class="panel">
          <div class="panel-header">
            <div class="panel-title"><i class="ti ti-checklist"></i> Günlük Görevler</div>
            <div class="panel-action" onclick="navigateTo('courses')">Tümü</div>
          </div>
          <div id="task-list">
            ${tasks.map(t => `
              <div class="task-item" onclick="toggleTask('${t.id}', this)">
                <div class="task-check ${t.done?'done':''}">${t.done?'<i class="ti ti-check"></i>':''}</div>
                <div class="task-info">
                  <div class="task-name ${t.done?'done-text':''}">${escapeHtml(t.name)}</div>
                  <div class="task-sub">${escapeHtml(t.sub)}</div>
                </div>
                <div class="task-xp">+${t.xp} XP</div>
              </div>
            `).join('')}
          </div>
        </div>

        <div class="panel">
          <div class="panel-header"><div class="panel-title"><i class="ti ti-medal"></i> Rozetlerim</div></div>
          <div class="badge-grid">
            ${allBadges.map(b => `
              <div class="badge-item ${earnedBadges.includes(b.id)?'earned':''}" title="${escapeHtml(b.desc)}">
                <div class="badge-icon" style="${earnedBadges.includes(b.id)?'':'opacity:0.3'}">${b.icon}</div>
                <div class="badge-name">${b.name}</div>
              </div>
            `).join('')}
          </div>
        </div>
      </div>

      <div class="dash-col">
        <div class="panel">
          <div class="panel-header"><div class="panel-title"><i class="ti ti-trending-up"></i> Eğitim İlerlemesi</div></div>
          ${courseRows.length ? courseRows.map((c,i) => {
            const colors = ['var(--orange)','var(--green)','var(--blue)','var(--purple)','var(--teal)'];
            return `
            <div class="progress-item">
              <div class="progress-label"><span>${escapeHtml(c.title)}</span><span style="color:${colors[i%5]}">${c.pct}%</span></div>
              <div class="progress-track"><div class="progress-fill" style="width:${c.pct}%;background:${colors[i%5]}"></div></div>
            </div>`;
          }).join('') : '<div class="empty-state" style="padding:16px"><div class="empty-state-text">Henüz bir eğitime başlamadın.</div></div>'}
        </div>

        <div class="panel">
          <div class="panel-header"><div class="panel-title"><i class="ti ti-sparkles"></i> Hadi AI'dan Hızlı Yardım</div></div>
          <div style="font-size:12px; color:var(--text-2); margin-bottom:12px; line-height:1.6;">Bugün ne yapmak istersin? Hadi AI sana anında yardımcı olabilir.</div>
          <div class="quick-prompts">
            <button class="quick-prompt-btn" onclick="navigateTo('ai-chat'); setTimeout(()=>sendQuick('Bugün için 3 öncelikli iş önerisi ver'),100)">💼 Bugünün öncelikleri</button>
            <button class="quick-prompt-btn" onclick="navigateTo('swot')">📊 SWOT yap</button>
            <button class="quick-prompt-btn" onclick="navigateTo('digital-test')">🧪 Dijital test çöz</button>
          </div>
        </div>
      </div>
    </div>
  `;
}

function defaultTasksFor(user){
  const tasks = [
    { id:uid('t'), name:'SWOT analizini tamamla', sub:'KOBİ Merkezi', xp:50, done:false },
    { id:uid('t'), name:'Dijital olgunluk testini çöz', sub:'Değerlendirme', xp:80, done:false },
    { id:uid('t'), name:'Hadi AI ile 1 soru sor', sub:'AI Danışman', xp:20, done:false },
    { id:uid('t'), name:'Bir eğitim dersini tamamla', sub:'Akademi', xp:30, done:false }
  ];
  DB.tasks[user.id] = tasks;
  saveDB(DB);
  return tasks;
}

function toggleTask(taskId, el){
  const user = currentUser();
  const tasks = DB.tasks[user.id];
  const t = tasks.find(x=>x.id===taskId);
  if(!t) return;
  t.done = !t.done;
  saveDB(DB);
  const check = el.querySelector('.task-check');
  const nameEl = el.querySelector('.task-name');
  check.classList.toggle('done', t.done);
  check.innerHTML = t.done ? '<i class="ti ti-check"></i>' : '';
  nameEl.classList.toggle('done-text', t.done);
  if(t.done) addXP(t.xp, true);
}

/* ===================================================================
   HADI AI — Genel sohbet
=================================================================== */

function renderAIChat(){
  const user = currentUser();
  const history = DB.aiChats.filter(c => c.userId === user.id).slice(-20);
  return `
    <div class="ai-panel-screen">
      <div class="ai-header">
        <div class="ai-avatar">🤖</div>
        <div class="ai-info">
          <h3>Hadi AI — İş & Eğitim Danışmanın</h3>
          <p>SWOT, stratejik plan, eğitim tasarımı, quiz, vaka analizi, oyunlaştırma ve KOBİ danışmanlığı için buradayım.</p>
        </div>
        <div style="margin-left:auto; display:flex; align-items:center; gap:5px; font-size:11px; color:var(--green); flex-shrink:0;">
          <div style="width:6px;height:6px;border-radius:50%;background:var(--green)" class="pulse"></div> Aktif
        </div>
      </div>

      <div class="chat-area" id="chat-area">
        ${history.length ? history.map(renderChatMsgPair).join('') : `
          <div class="msg msg-ai">
            <div class="msg-sender">Hadi AI</div>
            <div class="msg-bubble">Merhaba ${escapeHtml(user.name.split(' ')[0])}! Ben Hadi AI. SWOT analizi, stratejik plan, KPI önerisi, eğitim tasarımı, oyunlaştırma veya quiz oluşturma konularında yardımcı olabilirim. Ne yapmak istersin?</div>
          </div>
        `}
      </div>

      <div class="quick-prompts">
        <button class="quick-prompt-btn" onclick="sendQuick('Şirketimde verimlilik nasıl artırılır, 5 madde halinde pratik öneri ver')">⚡ Verimlilik önerileri</button>
        <button class="quick-prompt-btn" onclick="sendQuick('Satışları artırmak için somut öneriler ver')">💰 Satış önerileri</button>
        <button class="quick-prompt-btn" onclick="sendQuick('İş süreçlerimi nasıl dijitalleştirebilirim, adım adım anlat')">🔄 Dijitalleşme yol haritası</button>
        <button class="quick-prompt-btn" onclick="sendQuick('Yeni bir iş fikri geliştirmem için bana 3 fikir öner ve değerlendir')">💡 İş fikri geliştir</button>
        <button class="quick-prompt-btn" onclick="sendQuick('Satış departmanı için 3 ölçülebilir KPI öner')">🎯 KPI öner</button>
      </div>

      <div class="chat-input-row">
        <input class="chat-input" id="chat-input" placeholder="Bir soru sor veya görev ver..." onkeydown="if(event.key==='Enter')sendMessage()">
        <button class="send-btn" id="send-btn" onclick="sendMessage()"><i class="ti ti-send"></i></button>
      </div>
    </div>
  `;
}

function renderChatMsgPair(c){
  return `
    <div class="msg msg-user">
      <div class="msg-sender">Siz</div>
      <div class="msg-bubble">${escapeHtml(c.prompt)}</div>
    </div>
    <div class="msg msg-ai">
      <div class="msg-sender">Hadi AI</div>
      <div class="msg-bubble">${escapeHtml(c.reply)}</div>
    </div>
  `;
}

function initAIChatScroll(){
  const area = document.getElementById('chat-area');
  if(area) area.scrollTop = area.scrollHeight;
}

let msgCounter = 0;
function addLiveMsg(text, role){
  const id = 'livemsg-' + (++msgCounter);
  const area = document.getElementById('chat-area');
  if(!area) return id;
  const div = document.createElement('div');
  div.className = 'msg msg-' + role + ' fade-up';
  div.id = id;
  div.innerHTML = `<div class="msg-sender">${role==='user'?'Siz':'Hadi AI'}</div><div class="msg-bubble">${text}</div>`;
  area.appendChild(div);
  area.scrollTop = area.scrollHeight;
  return id;
}
function updateLiveMsg(id, text, isHtml){
  const el = document.getElementById(id);
  if(!el) return;
  const bubble = el.querySelector('.msg-bubble');
  if(isHtml) bubble.innerHTML = text; else bubble.textContent = text;
}

async function sendMessage(){
  const input = document.getElementById('chat-input');
  const text = input.value.trim();
  if(!text) return;
  input.value = '';
  const sendBtn = document.getElementById('send-btn');
  sendBtn.disabled = true;
  addLiveMsg(escapeHtml(text), 'user');
  const loadingId = addLiveMsg('Düşünüyor<span class="loading-dots"></span>', 'ai');
  const reply = await safeAICall(text);
  updateLiveMsg(loadingId, escapeHtml(reply));
  const user = currentUser();
  DB.aiChats.push({ id: uid('chat'), userId: user.id, prompt: text, reply, createdAt: Date.now() });
  saveDB(DB);
  checkBadges(user);
  sendBtn.disabled = false;
}

function sendQuick(prompt){
  const input = document.getElementById('chat-input');
  if(input){ input.value = prompt; sendMessage(); }
}

/* ===================================================================
   SWOT ANALİZİ
=================================================================== */

function renderSwot(){
  const user = currentUser();
  const past = DB.swotAnalyses.filter(s=>s.userId===user.id);
  return `
    <div style="margin-bottom:16px">
      <div style="font-size:13px; color:var(--text-2); margin-bottom:12px;">Şirketinizin güçlü/zayıf yönleri ile fırsat/tehditlerini girin. Hadi AI detaylı analiz ve stratejik öneriler üretecek.</div>
      <div style="display:flex; gap:8px; margin-bottom:12px;">
        <input class="text-input" id="swot-company" placeholder="Şirket adı veya sektör" style="flex:1" value="${user.company ? escapeHtml(user.company) : ''}">
        <select class="select-input" id="swot-sector" style="width:160px">
          <option>Üretim</option><option>Perakende</option><option>Hizmet</option><option>Teknoloji</option><option>İnşaat</option><option>Tarım</option>
        </select>
      </div>
    </div>

    <div class="swot-grid">
      <div class="swot-card s-strength">
        <div class="swot-title"><i class="ti ti-thumb-up"></i> Güçlü Yönler</div>
        <textarea class="text-area" id="swot-s" placeholder="- Deneyimli ekip&#10;- Güçlü müşteri tabanı"></textarea>
      </div>
      <div class="swot-card s-weakness">
        <div class="swot-title"><i class="ti ti-thumb-down"></i> Zayıf Yönler</div>
        <textarea class="text-area" id="swot-w" placeholder="- Dijitalleşme eksikliği&#10;- Bütçe kısıtları"></textarea>
      </div>
      <div class="swot-card s-opportunity">
        <div class="swot-title"><i class="ti ti-trending-up"></i> Fırsatlar</div>
        <textarea class="text-area" id="swot-o" placeholder="- Yeni pazar segmentleri&#10;- Dijital kanallar"></textarea>
      </div>
      <div class="swot-card s-threat">
        <div class="swot-title"><i class="ti ti-alert-triangle"></i> Tehditler</div>
        <textarea class="text-area" id="swot-t" placeholder="- Artan rekabet&#10;- Ekonomik belirsizlik"></textarea>
      </div>
    </div>

    <button class="btn-ai" id="swot-btn" onclick="analyzeSwot()"><i class="ti ti-sparkles"></i> Hadi AI ile Analiz Et</button>

    <div id="swot-result-wrap"></div>

    ${past.length ? `
      <div class="panel" style="margin-top:20px">
        <div class="panel-header"><div class="panel-title"><i class="ti ti-history"></i> Geçmiş Analizler</div></div>
        ${past.slice(-3).reverse().map(p => `
          <div class="task-item" style="cursor:default">
            <div class="task-info">
              <div class="task-name">${escapeHtml(p.company || 'İsimsiz analiz')}</div>
              <div class="task-sub">${new Date(p.createdAt).toLocaleDateString('tr-TR')}</div>
            </div>
          </div>
        `).join('')}
      </div>
    ` : ''}
  `;
}

async function analyzeSwot(){
  const s = document.getElementById('swot-s').value.trim();
  const w = document.getElementById('swot-w').value.trim();
  const o = document.getElementById('swot-o').value.trim();
  const t = document.getElementById('swot-t').value.trim();
  const company = document.getElementById('swot-company').value.trim();
  const sector = document.getElementById('swot-sector').value;

  if(!s && !w && !o && !t){ toast('Lütfen en az bir alanı doldurun.', 'error'); return; }

  const btn = document.getElementById('swot-btn');
  btn.disabled = true;
  btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Analiz ediliyor...';

  const wrap = document.getElementById('swot-result-wrap');
  wrap.innerHTML = `<div class="ai-result-box fade-up"><div class="ai-result-label">Hadi AI Analizi</div><div class="ai-result-text">Analiz ediliyor<span class="loading-dots"></span></div></div>`;

  const prompt = `Sen bir SWOT Analiz Uzmanısın. ${company ? company + ' isimli ' : ''}${sector} sektöründeki bir KOBİ için aşağıdaki SWOT girdilerini değerlendir ve detaylı analiz yap:

Güçlü Yönler: ${s || 'belirtilmedi'}
Zayıf Yönler: ${w || 'belirtilmedi'}
Fırsatlar: ${o || 'belirtilmedi'}
Tehditler: ${t || 'belirtilmedi'}

Şunları yap:
1. Her bir alanı kısaca değerlendir (1-2 cümle)
2. Güçlü yönler ile fırsatları nasıl birleştirebileceğine dair 2 strateji öner
3. Zayıf yönler ve tehditlere karşı 2 önlem öner
4. Sonuç olarak 3 maddelik aksiyon planı ver

Kısa, madde işaretli, uygulanabilir yaz.`;

  const reply = await safeAICall(prompt);

  wrap.innerHTML = `
    <div class="ai-result-box fade-up">
      <div class="ai-result-label">
        <span><i class="ti ti-robot"></i> Hadi AI Analizi</span>
        <button class="copy-mini-btn" onclick="copyText(this, swotLastResult)"><i class="ti ti-copy"></i> Kopyala</button>
      </div>
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
  `;
  window.swotLastResult = reply;

  const user = currentUser();
  DB.swotAnalyses.push({ id: uid('swot'), userId: user.id, company, sector, s, w, o, t, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(50, true);

  btn.disabled = false;
  btn.innerHTML = '<i class="ti ti-sparkles"></i> Hadi AI ile Analiz Et';
}

function copyText(btnEl, text){
  navigator.clipboard.writeText(text || '').then(()=>{
    toast('Panoya kopyalandı.', 'success');
  }).catch(()=>{ toast('Kopyalama başarısız.', 'error'); });
}

/* ===================================================================
   DİJİTAL OLGUNLUK TESTİ
=================================================================== */

const DIGITAL_TEST_QUESTIONS = [
  { q:'İşletmenizde satış ve müşteri verilerini hangi düzeyde dijital olarak yönetiyorsunuz?', opts:['Hiç yok, kağıt kullanıyoruz','Temel Excel/tablolar','CRM veya özel yazılım','Entegre dijital ekosistem'] },
  { q:'Çalışanlarınız için dijital araç eğitimleri düzenliyor musunuz?', opts:['Hayır, düzenlemiyoruz','Nadiren, talep üzerine','Yılda 1-2 kez','Sürekli ve düzenli programlar'] },
  { q:'E-ticaret veya dijital satış kanallarınız var mı?', opts:['Yok','Planlamaktayız','Küçük ölçekli var','Ana satış kanalımız'] },
  { q:'Yapay zekâ veya otomasyon araçlarından faydalanıyor musunuz?', opts:['Hayır, hiç kullanmıyoruz','Araştırma aşamasındayız','Bazı süreçlerde kullanıyoruz','Entegre şekilde kullanıyoruz'] },
  { q:'Dijital pazarlama stratejinizi nasıl değerlendirirsiniz?', opts:['Dijital pazarlama yapmıyoruz','Sosyal medyada paylaşım yapıyoruz','İçerik ve reklam yönetimi yapıyoruz','Veri odaklı, optimize kampanyalar'] },
  { q:'İç süreçleriniz (stok, muhasebe, İK) ne kadar dijitalleşmiş durumda?', opts:['Tamamen manuel/kağıt','Bazı bölümler dijital','Çoğu süreç yazılımla yönetiliyor','Tüm süreçler entegre ERP ile yönetiliyor'] }
];

let testState = { idx:0, answers:[] };

function renderDigitalTest(){
  testState = { idx:0, answers:[] };
  return `
    <div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:16px;">
      <div>
        <div style="font-size:13px; color:var(--text-2);">Dijital Olgunluk Testi — Soru <span id="q-num">1</span>/${DIGITAL_TEST_QUESTIONS.length}</div>
        <div style="font-size:11px; color:var(--text-3); margin-top:2px;">Her soruyu dürüstçe yanıtlayın, sonunda Hadi AI yorumunu alacaksınız.</div>
      </div>
      <div class="q-dots" id="q-dots"></div>
    </div>
    <div id="test-container"></div>
    <button id="next-q-btn" class="btn-ai hidden" style="max-width:200px" onclick="nextQuestion()">Sonraki Soru <i class="ti ti-arrow-right"></i></button>
    <div id="test-result" class="hidden"></div>
  `;
}

function initDigitalTest(){
  renderQDots();
  renderQuestion(0);
}

function renderQDots(){
  const dots = document.getElementById('q-dots');
  if(!dots) return;
  dots.innerHTML = DIGITAL_TEST_QUESTIONS.map((_,i) => `<div class="q-dot" id="q-dot-${i}"></div>`).join('');
}

function renderQuestion(idx){
  const q = DIGITAL_TEST_QUESTIONS[idx];
  document.getElementById('q-num').textContent = idx + 1;
  for(let i=0;i<DIGITAL_TEST_QUESTIONS.length;i++){
    const dot = document.getElementById('q-dot-'+i);
    if(!dot) continue;
    dot.style.background = i < idx ? 'var(--green)' : (i === idx ? 'var(--orange)' : 'rgba(255,255,255,0.1)');
  }
  document.getElementById('test-container').innerHTML = `
    <div class="test-question fade-up">
      <div class="test-q-text">${escapeHtml(q.q)}</div>
      <div class="test-options">
        ${q.opts.map((o,i) => `<button class="test-option" onclick="selectOption(this,${i})">${escapeHtml(o)}</button>`).join('')}
      </div>
    </div>
  `;
  document.getElementById('next-q-btn').classList.add('hidden');
}

function selectOption(el, idx){
  el.parentElement.querySelectorAll('.test-option').forEach(o=>o.classList.remove('selected'));
  el.classList.add('selected');
  testState.answers[testState.idx] = idx;
  document.getElementById('next-q-btn').classList.remove('hidden');
}

async function nextQuestion(){
  testState.idx++;
  if(testState.idx < DIGITAL_TEST_QUESTIONS.length){
    renderQuestion(testState.idx);
  } else {
    document.getElementById('test-container').style.display = 'none';
    document.getElementById('next-q-btn').classList.add('hidden');
    const resultEl = document.getElementById('test-result');
    resultEl.classList.remove('hidden');
    resultEl.innerHTML = `
      <div class="ai-result-box fade-up" style="text-align:center">
        <div style="font-size:36px; margin-bottom:8px;">🏆</div>
        <div style="font-size:12px; color:var(--text-2);">Sonuç hesaplanıyor<span class="loading-dots"></span></div>
      </div>
    `;
    const total = testState.answers.reduce((a,b)=>a+b,0);
    const max = DIGITAL_TEST_QUESTIONS.length * 3;
    const pct = total / max;
    let level;
    if(pct < 0.25) level = 'Başlangıç';
    else if(pct < 0.5) level = 'Gelişmekte';
    else if(pct < 0.75) level = 'İleri';
    else level = 'Lider';

    const answersSummary = DIGITAL_TEST_QUESTIONS.map((q,i) => `${q.q} → ${q.opts[testState.answers[i]]}`).join('\n');
    const prompt = `Bir KOBİ'nin dijital olgunluk testi sonuçlarını değerlendiriyorsun. Test sonucu seviyesi: "${level}" (${Math.round(pct*100)}% puan).

Cevaplar:
${answersSummary}

Bu seviyeye özel, 4-5 madde halinde kısa ve uygulanabilir gelişim önerileri ver. Cesaretlendirici ama gerçekçi bir ton kullan.`;

    const reply = await safeAICall(prompt);

    resultEl.innerHTML = `
      <div class="ai-result-box fade-up" style="text-align:center">
        <div style="font-size:36px; margin-bottom:8px;">🏆</div>
        <div style="font-size:16px; font-weight:600; color:var(--text-1); margin-bottom:4px;">Dijital Olgunluk Seviyeniz</div>
        <div style="font-size:24px; font-weight:700; color:var(--orange); margin-bottom:16px;">${level}</div>
        <div class="ai-result-text" style="text-align:left">${escapeHtml(reply)}</div>
      </div>
    `;

    const user = currentUser();
    DB.digitalAssessments.push({ id: uid('da'), userId:user.id, level, pct: Math.round(pct*100), answers: testState.answers, result: reply, createdAt: Date.now() });
    saveDB(DB);
    addXP(80, true);
  }
}

/* ===================================================================
   STRATEJİK PLAN OLUŞTURUCU
=================================================================== */

function renderStrategic(){
  return `
    <div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin-bottom:16px;">
      <div class="panel">
        <div class="panel-header"><div class="panel-title"><i class="ti ti-eye"></i> Vizyon</div></div>
        <textarea class="text-area" id="plan-vizyon" placeholder="Şirketinizin 5 yıllık vizyonunu yazın..."></textarea>
      </div>
      <div class="panel">
        <div class="panel-header"><div class="panel-title"><i class="ti ti-heart"></i> Misyon</div></div>
        <textarea class="text-area" id="plan-misyon" placeholder="Şirketinizin misyonunu yazın..."></textarea>
      </div>
    </div>

    <div class="panel" style="margin-bottom:12px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-target"></i> Stratejik Hedefler</div></div>
      <div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:8px;">
        <input class="text-input" id="plan-hedef1" placeholder="Hedef 1 — örn: Satışları %20 artır">
        <input class="text-input" id="plan-hedef2" placeholder="Hedef 2 — örn: Dijitalleşme oranı">
        <input class="text-input" id="plan-hedef3" placeholder="Hedef 3 — örn: Müşteri memnuniyeti">
      </div>
    </div>

    <div class="panel" style="margin-bottom:12px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-building"></i> Sektör & Bağlam</div></div>
      <div style="display:flex; gap:8px;">
        <select class="select-input" id="plan-sektor" style="flex:1">
          <option>Üretim</option><option>Perakende</option><option>Hizmet</option><option>Teknoloji</option><option>İnşaat</option><option>Tarım</option>
        </select>
        <select class="select-input" id="plan-buyukluk" style="flex:1">
          <option>1-10 çalışan (Mikro)</option><option>11-50 çalışan (Küçük)</option><option>51-250 çalışan (Orta)</option>
        </select>
      </div>
    </div>

    <button class="btn-ai" id="plan-btn" onclick="generatePlan()"><i class="ti ti-sparkles"></i> Hadi AI ile Stratejik Plan Oluştur</button>

    <div id="plan-result-wrap"></div>
  `;
}

async function generatePlan(){
  const vizyon = document.getElementById('plan-vizyon').value.trim();
  const misyon = document.getElementById('plan-misyon').value.trim();
  const h1 = document.getElementById('plan-hedef1').value.trim();
  const h2 = document.getElementById('plan-hedef2').value.trim();
  const h3 = document.getElementById('plan-hedef3').value.trim();
  const sektor = document.getElementById('plan-sektor').value;
  const buyukluk = document.getElementById('plan-buyukluk').value;

  const btn = document.getElementById('plan-btn');
  btn.disabled = true;
  btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Plan oluşturuluyor...';

  const wrap = document.getElementById('plan-result-wrap');
  wrap.innerHTML = `<div class="ai-result-box fade-up"><div class="ai-result-label">AI Stratejik Plan</div><div class="ai-result-text">Hazırlanıyor<span class="loading-dots"></span></div></div>`;

  const prompt = `Sen bir Stratejik Plan Uzmanısın. ${sektor} sektöründe, ${buyukluk} büyüklüğünde bir KOBİ için kapsamlı bir stratejik plan hazırla.

Girdi bilgileri:
Vizyon: ${vizyon || 'belirtilmedi, sen öner'}
Misyon: ${misyon || 'belirtilmedi, sen öner'}
Hedefler: ${[h1,h2,h3].filter(Boolean).join(', ') || 'belirtilmedi, sen öner'}

Şu formatta hazırla:
1. Vizyon/Misyon önerisi (girilmemişse)
2. 1 yıllık 3 stratejik hedef
3. Her hedef için 1-2 ölçülebilir KPI
4. İlk 90 gün için öncelikli 3 aksiyon

Kısa, net ve uygulanabilir yaz.`;

  const reply = await safeAICall(prompt);

  wrap.innerHTML = `
    <div class="ai-result-box fade-up">
      <div class="ai-result-label">
        <span><i class="ti ti-robot"></i> AI Stratejik Plan</span>
        <button class="copy-mini-btn" onclick="copyText(this, planLastResult)"><i class="ti ti-copy"></i> Kopyala</button>
      </div>
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
  `;
  window.planLastResult = reply;

  const user = currentUser();
  DB.strategicPlans.push({ id: uid('plan'), userId:user.id, vizyon, misyon, hedefler:[h1,h2,h3], sektor, buyukluk, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(60, true);

  btn.disabled = false;
  btn.innerHTML = '<i class="ti ti-sparkles"></i> Hadi AI ile Stratejik Plan Oluştur';
}

/* ===================================================================
   EĞİTİM TASARIMCISI (Eğitmen modülü)
=================================================================== */

function renderLessonDesigner(){
  return `
    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-bulb"></i> Eğitim Tasarım Girdileri</div></div>
      <div class="field-group" style="margin-bottom:10px">
        <label class="field-label">Eğitim konusu</label>
        <input class="text-input" id="ld-topic" placeholder="örn: Dijital Pazarlamaya Giriş">
      </div>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-bottom:10px;">
        <div>
          <label class="field-label">Süre</label>
          <select class="select-input" id="ld-duration">
            <option>45 dakika</option><option>1.5 saat</option><option>Yarım gün (3 saat)</option><option>Tam gün (6 saat)</option>
          </select>
        </div>
        <div>
          <label class="field-label">Hedef kitle</label>
          <select class="select-input" id="ld-audience">
            <option>KOBİ Yöneticileri</option><option>Yeni girişimciler</option><option>Çalışanlar / Operasyon ekibi</option><option>Üst düzey yöneticiler</option>
          </select>
        </div>
      </div>
      <button class="btn-ai" id="ld-btn" onclick="generateLessonPlan()"><i class="ti ti-sparkles"></i> Eğitim Akışı Oluştur</button>
    </div>
    <div id="ld-result-wrap"></div>
  `;
}

async function generateLessonPlan(){
  const topic = document.getElementById('ld-topic').value.trim();
  if(!topic){ toast('Lütfen bir eğitim konusu girin.', 'error'); return; }
  const duration = document.getElementById('ld-duration').value;
  const audience = document.getElementById('ld-audience').value;

  const btn = document.getElementById('ld-btn');
  btn.disabled = true; btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Tasarlanıyor...';
  const wrap = document.getElementById('ld-result-wrap');
  wrap.innerHTML = `<div class="ai-result-box fade-up"><div class="ai-result-label">AI Eğitim Tasarımı</div><div class="ai-result-text">Hazırlanıyor<span class="loading-dots"></span></div></div>`;

  const prompt = `Sen bir Eğitim Tasarım Uzmanısın. "${topic}" konusunda, ${duration} süreli, hedef kitlesi "${audience}" olan bir eğitim tasarla.

Şu formatta ver:
1. Öğrenme hedefleri (3-4 madde, "katılımcı ... yapabilecektir" formatında)
2. Eğitim akışı (zaman dilimlerine bölünmüş bölümler)
3. Önerilen aktiviteler (en az 2 interaktif aktivite — örnek, grup çalışması, rol oyunu vb.)
4. Değerlendirme yöntemi önerisi

Kısa, pratik ve uygulanabilir yaz.`;

  const reply = await safeAICall(prompt);
  wrap.innerHTML = `
    <div class="ai-result-box fade-up">
      <div class="ai-result-label"><span><i class="ti ti-robot"></i> Eğitim Akışı: ${escapeHtml(topic)}</span><button class="copy-mini-btn" onclick="copyText(this, ldLastResult)"><i class="ti ti-copy"></i> Kopyala</button></div>
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
  `;
  window.ldLastResult = reply;
  const user = currentUser();
  DB.lessonPlans.push({ id: uid('lp'), userId:user.id, topic, duration, audience, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(50, true);
  btn.disabled = false; btn.innerHTML = '<i class="ti ti-sparkles"></i> Eğitim Akışı Oluştur';
}

/* ===================================================================
   OYUNLAŞTIRMA TASARIMCISI
=================================================================== */

function renderGamifyDesigner(){
  return `
    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-puzzle"></i> Oyunlaştırma Tasarım Girdileri</div></div>
      <div class="field-group" style="margin-bottom:10px">
        <label class="field-label">Eğitim / program adı</label>
        <input class="text-input" id="gd-program" placeholder="örn: Dijital Dönüşüm Sertifika Programı">
      </div>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-bottom:10px;">
        <div>
          <label class="field-label">Katılımcı sayısı</label>
          <select class="select-input" id="gd-size">
            <option>5-15 kişi (küçük grup)</option><option>15-40 kişi (sınıf)</option><option>40+ kişi (büyük kohort)</option>
          </select>
        </div>
        <div>
          <label class="field-label">Odak</label>
          <select class="select-input" id="gd-focus">
            <option>Bireysel ilerleme</option><option>Takım yarışması</option><option>Karma (bireysel + takım)</option>
          </select>
        </div>
      </div>
      <button class="btn-ai" id="gd-btn" onclick="generateGamification()"><i class="ti ti-sparkles"></i> Oyunlaştırma Sistemi Oluştur</button>
    </div>
    <div id="gd-result-wrap"></div>
  `;
}

async function generateGamification(){
  const program = document.getElementById('gd-program').value.trim();
  if(!program){ toast('Lütfen bir program adı girin.', 'error'); return; }
  const size = document.getElementById('gd-size').value;
  const focus = document.getElementById('gd-focus').value;

  const btn = document.getElementById('gd-btn');
  btn.disabled = true; btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Tasarlanıyor...';
  const wrap = document.getElementById('gd-result-wrap');
  wrap.innerHTML = `<div class="ai-result-box fade-up"><div class="ai-result-label">AI Oyunlaştırma Tasarımı</div><div class="ai-result-text">Hazırlanıyor<span class="loading-dots"></span></div></div>`;

  const prompt = `Sen bir Oyunlaştırma Uzmanısın. "${program}" isimli eğitim programı için, ${size} katılımcı ve "${focus}" odağıyla bir oyunlaştırma sistemi tasarla.

Şunları üret:
1. Puan sistemi (hangi aktivite kaç puan kazandırır — en az 5 aktivite)
2. 4-5 rozet önerisi (isim + kazanma koşulu)
3. Seviye sistemi (en az 4 seviye, isim + gereken puan)
4. Eğer takım odaklıysa: 1 takım yarışması formatı önerisi

Kısa, somut ve uygulanabilir yaz, tablo formatından kaçın, madde işaretleri kullan.`;

  const reply = await safeAICall(prompt);
  wrap.innerHTML = `
    <div class="ai-result-box fade-up">
      <div class="ai-result-label"><span><i class="ti ti-robot"></i> Oyunlaştırma: ${escapeHtml(program)}</span><button class="copy-mini-btn" onclick="copyText(this, gdLastResult)"><i class="ti ti-copy"></i> Kopyala</button></div>
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
  `;
  window.gdLastResult = reply;
  const user = currentUser();
  DB.gamificationDesigns.push({ id: uid('gd'), userId:user.id, program, size, focus, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(50, true);
  btn.disabled = false; btn.innerHTML = '<i class="ti ti-sparkles"></i> Oyunlaştırma Sistemi Oluştur';
}

/* ===================================================================
   QUIZ OLUŞTURUCU
=================================================================== */

function renderQuizMaker(){
  return `
    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-wand"></i> AI Quiz Oluşturucu</div></div>
      <div style="display:grid; grid-template-columns:2fr 1fr 1fr; gap:8px; margin-bottom:12px;">
        <input id="quiz-topic" class="text-input" placeholder="Eğitim konusu (örn: Dijital Dönüşüm)">
        <select id="quiz-type" class="select-input">
          <option value="coktan">Çoktan seçmeli</option>
          <option value="dogru">Doğru/Yanlış</option>
          <option value="vaka">Vaka sorusu</option>
        </select>
        <select id="quiz-count" class="select-input">
          <option value="3">3 soru</option><option value="5">5 soru</option><option value="10">10 soru</option>
        </select>
      </div>
      <button class="btn-ai" id="quiz-btn" onclick="generateQuiz()"><i class="ti ti-sparkles"></i> Quiz Oluştur</button>
    </div>
    <div id="quiz-output"></div>
  `;
}

async function generateQuiz(){
  const topic = document.getElementById('quiz-topic').value.trim() || 'Dijital Dönüşüm';
  const type = document.getElementById('quiz-type').value;
  const count = document.getElementById('quiz-count').value;
  const typeMap = { coktan:'çoktan seçmeli (4 şık, A-B-C-D)', dogru:'doğru/yanlış', vaka:'vaka analizi sorusu (kısa senaryo + soru)' };

  const btn = document.getElementById('quiz-btn');
  btn.disabled = true; btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Oluşturuluyor...';
  const output = document.getElementById('quiz-output');
  output.innerHTML = `<div style="text-align:center; padding:24px; color:var(--text-3);">Quiz oluşturuluyor<span class="loading-dots"></span></div>`;

  const prompt = `"${topic}" konusunda ${count} adet ${typeMap[type]} soru oluştur. Her soruyu numaralandır, şıkları ver, sonunda ayrı bir "Cevap Anahtarı" bölümü ekle. Düz metin formatında yaz, markdown tablosu kullanma.`;

  const reply = await safeAICall(prompt);
  output.innerHTML = `
    <div class="quiz-result-item fade-up">
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
    <div style="display:flex; gap:8px;">
      <button class="copy-mini-btn" onclick="copyText(this, quizLastResult)"><i class="ti ti-copy"></i> Kopyala</button>
      <button class="copy-mini-btn" onclick="navigateTo('quiz-maker')"><i class="ti ti-refresh"></i> Yeni quiz</button>
    </div>
  `;
  window.quizLastResult = reply;
  const user = currentUser();
  DB.quizzes.push({ id: uid('quiz'), userId:user.id, topic, type, count, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(40, true);
  btn.disabled = false; btn.innerHTML = '<i class="ti ti-sparkles"></i> Quiz Oluştur';
}

/* ===================================================================
   VAKA ANALİZİ ÜRETİCİ
=================================================================== */

function renderCaseGenerator(){
  return `
    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-briefcase"></i> Vaka Analizi Üretici</div></div>
      <div class="field-group" style="margin-bottom:10px">
        <label class="field-label">Vaka konusu</label>
        <input class="text-input" id="case-topic" placeholder="örn: Dijital dönüşüm yaşayan bir KOBİ vakası oluştur">
      </div>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-bottom:10px;">
        <select class="select-input" id="case-sector">
          <option>Üretim</option><option>Perakende</option><option>Hizmet</option><option>Teknoloji</option><option>İnşaat</option><option>Tarım</option>
        </select>
        <select class="select-input" id="case-length">
          <option>Kısa (1 sayfa)</option><option>Orta (detaylı senaryo)</option><option>Uzun (çok boyutlu vaka)</option>
        </select>
      </div>
      <button class="btn-ai" id="case-btn" onclick="generateCase()"><i class="ti ti-sparkles"></i> Vaka Oluştur</button>
    </div>
    <div id="case-result-wrap"></div>
  `;
}

async function generateCase(){
  const topic = document.getElementById('case-topic').value.trim() || 'Dijital dönüşüm yaşayan bir KOBİ vakası';
  const sector = document.getElementById('case-sector').value;
  const length = document.getElementById('case-length').value;

  const btn = document.getElementById('case-btn');
  btn.disabled = true; btn.innerHTML = '<i class="ti ti-loader-2 spin"></i> Hazırlanıyor...';
  const wrap = document.getElementById('case-result-wrap');
  wrap.innerHTML = `<div class="ai-result-box fade-up"><div class="ai-result-label">AI Vaka Analizi</div><div class="ai-result-text">Hazırlanıyor<span class="loading-dots"></span></div></div>`;

  const prompt = `Sen bir Vaka Analizi Üreticisisin. "${topic}" konusunda, ${sector} sektöründe geçen, ${length} uzunluğunda tam bir vaka çalışması hazırla.

Vaka şunları içermeli:
1. Şirket profili (kurgusal isim, sektör, büyüklük)
2. Karşılaşılan durum / problem
3. Alınan kararlar ve uygulanan adımlar
4. Sonuç ve öğrenilen dersler
5. Tartışma için 3 soru (eğitimde katılımcılara sorulacak)

Gerçekçi, somut detaylarla (sayılar, zaman çizelgesi) yaz.`;

  const reply = await safeAICall(prompt);
  wrap.innerHTML = `
    <div class="ai-result-box fade-up">
      <div class="ai-result-label"><span><i class="ti ti-robot"></i> Vaka Analizi</span><button class="copy-mini-btn" onclick="copyText(this, caseLastResult)"><i class="ti ti-copy"></i> Kopyala</button></div>
      <div class="ai-result-text">${escapeHtml(reply)}</div>
    </div>
  `;
  window.caseLastResult = reply;
  const user = currentUser();
  DB.cases.push({ id: uid('case'), userId:user.id, topic, sector, length, result: reply, createdAt: Date.now() });
  saveDB(DB);
  addXP(50, true);
  btn.disabled = false; btn.innerHTML = '<i class="ti ti-sparkles"></i> Vaka Oluştur';
}

/* ===================================================================
   EĞİTİM AKADEMİSİ (Courses)
=================================================================== */

const COURSE_COLOR_BG = {
  orange:'rgba(249,115,22,0.08)', blue:'rgba(59,130,246,0.08)', purple:'rgba(139,92,246,0.08)',
  teal:'rgba(20,184,166,0.08)', green:'rgba(16,185,129,0.08)', amber:'rgba(245,158,11,0.08)'
};

function renderCourses(user){
  const progress = DB.courseProgress[user.id] || {};
  const categories = ['Tümü', ...new Set(DB.courses.map(c=>c.category))];
  return `
    <div class="filter-chip-row" id="course-filter-row">
      ${categories.map((cat,i) => `<button class="quick-prompt-btn ${i===0?'active':''}" onclick="filterCourses('${cat}', this)">${cat}</button>`).join('')}
    </div>
    <div class="courses-grid" id="courses-grid">
      ${DB.courses.map(c => renderCourseCard(c, progress[c.id] || 0)).join('')}
    </div>
  `;
}

function renderCourseCard(c, pct){
  return `
    <div class="course-card" data-category="${c.category}" onclick="openCourseModal('${c.id}')">
      <div class="course-thumb" style="background:${COURSE_COLOR_BG[c.color]||COURSE_COLOR_BG.orange}">${c.icon}</div>
      <div class="course-body">
        <div class="course-title">${escapeHtml(c.title)}</div>
        <div class="course-meta">${c.lessons} ders · ${c.hours} saat · ${c.level}</div>
        <div class="course-progress-bar"><div class="course-progress-fill" style="width:${pct}%"></div></div>
        <div class="course-progress-label" style="${pct===100?'color:var(--green)':''}">${pct===100?'✓ Tamamlandı':(pct===0?'Başlamadı':'%'+pct+' tamamlandı')}</div>
      </div>
    </div>
  `;
}

function filterCourses(cat, btn){
  document.querySelectorAll('#course-filter-row .quick-prompt-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('#courses-grid .course-card').forEach(card => {
    card.style.display = (cat === 'Tümü' || card.dataset.category === cat) ? '' : 'none';
  });
}

function openCourseModal(courseId){
  const course = DB.courses.find(c=>c.id===courseId);
  const user = currentUser();
  const pct = (DB.courseProgress[user.id] || {})[courseId] || 0;
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'course-modal-overlay';
  overlay.onclick = (e) => { if(e.target === overlay) closeModal('course-modal-overlay'); };
  overlay.innerHTML = `
    <div class="modal-box fade-up">
      <div class="modal-header">
        <div class="modal-title">${course.icon} ${escapeHtml(course.title)}</div>
        <button class="modal-close" onclick="closeModal('course-modal-overlay')"><i class="ti ti-x"></i></button>
      </div>
      <div style="font-size:12px; color:var(--text-3); margin-bottom:16px;">${course.lessons} ders · ${course.hours} saat · ${course.level} seviye · ${course.category}</div>
      <div class="progress-track" style="margin-bottom:16px"><div class="progress-fill" style="width:${pct}%; background:var(--orange)"></div></div>
      <div style="font-size:12px; color:var(--text-2); line-height:1.7; margin-bottom:20px;">
        Bu eğitim, ${course.category.toLowerCase()} alanında pratik beceriler kazandırmayı hedefler. İçerik; video dersler, interaktif quizler ve gerçek KOBİ vaka çalışmalarından oluşur. Tamamladığınızda XP kazanır ve sertifika alma hakkı elde edersiniz.
      </div>
      <button class="btn-ai" onclick="advanceCourse('${courseId}')"><i class="ti ti-player-play"></i> ${pct===0?'Eğitime Başla':(pct===100?'Tekrar Gözden Geçir':'Devam Et')}</button>
    </div>
  `;
  document.body.appendChild(overlay);
}

function closeModal(id){
  const el = document.getElementById(id);
  if(el) el.remove();
}

function advanceCourse(courseId){
  const user = currentUser();
  if(!DB.courseProgress[user.id]) DB.courseProgress[user.id] = {};
  const cur = DB.courseProgress[user.id][courseId] || 0;
  const next = Math.min(100, cur + 25);
  DB.courseProgress[user.id][courseId] = next;
  saveDB(DB);
  closeModal('course-modal-overlay');
  if(next === 100 && cur !== 100){
    const course = DB.courses.find(c=>c.id===courseId);
    issueCertificate(course);
    addXP(100, true);
    toast('Tebrikler! "' + course.title + '" eğitimini tamamladınız 🎉', 'success');
  } else {
    addXP(15, true);
    toast('İlerleme kaydedildi: %' + next, 'success');
  }
  if(currentScreen === 'courses') navigateTo('courses');
  if(currentScreen === 'dashboard') navigateTo('dashboard');
}

function issueCertificate(course){
  const user = currentUser();
  const exists = DB.certificates.find(c=>c.userId===user.id && c.courseTitle===course.title);
  if(exists) return;
  DB.certificates.push({
    id: uid('cert'), userId: user.id, courseTitle: course.title,
    date: new Date().toLocaleDateString('tr-TR', {day:'numeric', month:'long', year:'numeric'}),
    certNo: 'KDA-' + new Date().getFullYear() + '-' + Math.floor(1000+Math.random()*9000)
  });
  saveDB(DB);
}

/* ===================================================================
   SERTİFİKALAR
=================================================================== */

function renderCertificates(user){
  const certs = DB.certificates.filter(c=>c.userId===user.id);
  if(!certs.length){
    return `<div class="empty-state"><i class="ti ti-certificate"></i><div class="empty-state-text">Henüz bir sertifika kazanmadınız. Bir eğitimi %100 tamamlayarak sertifika kazanabilirsiniz.</div></div>`;
  }
  return `
    <div style="display:grid; grid-template-columns:1fr 1fr; gap:16px;">
      ${certs.map(c => `
        <div class="cert-card fade-up">
          <div class="cert-seal">🏅</div>
          <div class="cert-title-text">Başarı Sertifikası</div>
          <div class="cert-name">${escapeHtml(user.name)}</div>
          <div class="cert-course">${escapeHtml(c.courseTitle)} eğitimini başarıyla tamamladı</div>
          <div class="cert-meta-row">
            <span>${c.date}</span>
            <span>No: ${c.certNo}</span>
          </div>
          <button class="copy-mini-btn" style="margin-top:14px" onclick="downloadCertText('${c.id}')"><i class="ti ti-download"></i> İndir (metin)</button>
        </div>
      `).join('')}
    </div>
  `;
}

function downloadCertText(certId){
  const c = DB.certificates.find(x=>x.id===certId);
  const user = currentUser();
  const text = `KOBİ DÖNÜŞÜM AKADEMİSİ - BAŞARI SERTİFİKASI\n\n${user.name}\n\n"${c.courseTitle}" eğitimini başarıyla tamamlamıştır.\n\nTarih: ${c.date}\nSertifika No: ${c.certNo}`;
  const blob = new Blob([text], {type:'text/plain'});
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  a.download = 'sertifika_' + c.certNo + '.txt';
  a.click();
}

/* ===================================================================
   LİDERBOARD
=================================================================== */

function renderLeaderboard(user){
  const ranked = DB.users.filter(u=>u.role!=='admin').slice().sort((a,b)=>(b.xp||0)-(a.xp||0));
  const myRank = ranked.findIndex(u=>u.id===user.id) + 1;
  const top = ranked[0];
  const colorPool = ['var(--amber)','var(--blue)','var(--purple)','var(--teal)','var(--green)','var(--red)','var(--orange)'];

  return `
    ${top ? `
    <div class="panel" style="margin-bottom:16px; background:linear-gradient(135deg, rgba(249,115,22,0.15), rgba(249,115,22,0.04));">
      <div style="display:flex; align-items:center; gap:12px;">
        <div style="font-size:40px;">🥇</div>
        <div>
          <div style="font-size:12px; color:var(--text-3);">Genel Lider</div>
          <div style="font-size:16px; font-weight:600; color:var(--text-1);">${escapeHtml(top.name)}</div>
          <div style="font-size:12px; color:var(--orange);">${(top.xp||0).toLocaleString('tr-TR')} XP · ${xpToLevel(top.xp||0).level}</div>
        </div>
        <div style="margin-left:auto; font-size:12px; color:var(--text-3);">Senin sıran: <span style="color:var(--orange); font-weight:600;">#${myRank}</span></div>
      </div>
    </div>` : ''}

    <div id="lb-list">
      ${ranked.map((u,i) => {
        const rankClass = i===0?'gold':(i===1?'silver':(i===2?'bronze':''));
        const isMe = u.id === user.id;
        const color = colorPool[i % colorPool.length];
        return `
          <div class="lb-item" style="${isMe?'border-color:var(--orange-glow); background:var(--orange-soft);':''}">
            <div class="lb-rank ${rankClass}" style="${isMe&&!rankClass?'color:var(--orange)':''}">${i+1}</div>
            <div class="lb-avatar" style="background:${color}22; color:${color}">${initials(u.name)}</div>
            <div class="lb-name" style="${isMe?'color:var(--orange)':''}">${escapeHtml(u.name)}${isMe?' (Siz)':''}</div>
            <div class="lb-level-tag" style="${isMe?'color:var(--orange); opacity:0.7':''}">${xpToLevel(u.xp||0).level}</div>
            <div class="lb-xp">${(u.xp||0).toLocaleString('tr-TR')} XP</div>
          </div>
        `;
      }).join('')}
    </div>
  `;
}

/* ===================================================================
   RAPORLAMA
=================================================================== */

function renderReports(user){
  const isAdminLike = user.role === 'egitmen' || user.role === 'admin';
  const pool = isAdminLike ? DB.users.filter(u=>u.role!=='admin') : [user];
  const totalSwot = DB.swotAnalyses.filter(s => pool.some(p=>p.id===s.userId)).length;
  const totalPlans = DB.strategicPlans.filter(s => pool.some(p=>p.id===s.userId)).length;
  const totalAssessments = DB.digitalAssessments.filter(s => pool.some(p=>p.id===s.userId)).length;
  const avgXP = Math.round(pool.reduce((a,u)=>a+(u.xp||0),0) / pool.length) || 0;
  const completedCourses = pool.reduce((acc,u) => {
    const prog = DB.courseProgress[u.id] || {};
    return acc + Object.values(prog).filter(p=>p===100).length;
  }, 0);

  return `
    <div class="stats-row">
      <div class="stat-card"><div class="stat-label"><i class="ti ti-chart-radar" style="color:var(--purple);font-size:13px"></i> SWOT Analizleri</div><div class="stat-value">${totalSwot}</div></div>
      <div class="stat-card"><div class="stat-label"><i class="ti ti-target" style="color:var(--blue);font-size:13px"></i> Stratejik Planlar</div><div class="stat-value">${totalPlans}</div></div>
      <div class="stat-card"><div class="stat-label"><i class="ti ti-device-analytics" style="color:var(--teal);font-size:13px"></i> Dijital Testler</div><div class="stat-value">${totalAssessments}</div></div>
      <div class="stat-card"><div class="stat-label"><i class="ti ti-school" style="color:var(--green);font-size:13px"></i> Tamamlanan Eğitim</div><div class="stat-value">${completedCourses}</div></div>
    </div>

    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header">
        <div class="panel-title"><i class="ti ti-file-text"></i> ${isAdminLike ? 'Genel Katılım Raporu' : 'Kişisel Performans Raporu'}</div>
        <button class="copy-mini-btn" onclick="exportReportPDF()"><i class="ti ti-download"></i> PDF olarak dışa aktar</button>
      </div>
      <div style="font-size:12px; color:var(--text-2); line-height:1.7;">
        Ortalama XP: <strong style="color:var(--text-1)">${avgXP.toLocaleString('tr-TR')}</strong><br>
        Değerlendirilen kullanıcı sayısı: <strong style="color:var(--text-1)">${pool.length}</strong><br>
        Toplam AI etkileşimi: <strong style="color:var(--text-1)">${DB.aiChats.filter(c=>pool.some(p=>p.id===c.userId)).length}</strong>
      </div>
    </div>

    <div class="panel">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-users"></i> ${isAdminLike?'Kullanıcı Bazlı Özet':'Eğitim İlerlemem'}</div></div>
      ${pool.map(u => {
        const prog = DB.courseProgress[u.id] || {};
        const avgProg = Math.round(Object.values(prog).reduce((a,b)=>a+b,0) / (DB.courses.length)) || 0;
        return `
          <div class="task-item" style="cursor:default">
            <div class="avatar" style="margin-right:0">${initials(u.name)}</div>
            <div class="task-info">
              <div class="task-name">${escapeHtml(u.name)}</div>
              <div class="task-sub">${(u.xp||0).toLocaleString('tr-TR')} XP · ${xpToLevel(u.xp||0).level}</div>
            </div>
            <div class="task-xp" style="color:var(--blue)">%${avgProg} ilerleme</div>
          </div>
        `;
      }).join('')}
    </div>
  `;
}

function exportReportPDF(){
  // Basit demo: yazdırma diyaloğu üzerinden PDF'e aktarım
  toast('Yazdırma penceresi açılıyor, "PDF olarak kaydet" seçeneğini kullanabilirsiniz.', 'success');
  setTimeout(() => window.print(), 400);
}

/* ===================================================================
   KATILIMCI YÖNETİMİ (Eğitmen/Admin)
=================================================================== */

function renderParticipants(){
  const users = DB.users.filter(u=>u.role==='ogrenci' || u.role==='yonetici');
  return `
    <div class="panel">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-users"></i> Katılımcılar (${users.length})</div></div>
      ${users.map(u => {
        const prog = DB.courseProgress[u.id] || {};
        const avgProg = Math.round(Object.values(prog).reduce((a,b)=>a+b,0) / (DB.courses.length || 1)) || 0;
        return `
          <div class="task-item" style="cursor:default">
            <div class="avatar" style="margin-right:0">${initials(u.name)}</div>
            <div class="task-info">
              <div class="task-name">${escapeHtml(u.name)} <span style="color:var(--text-3); font-weight:400;">— ${roleLabel(u.role)}</span></div>
              <div class="task-sub">${escapeHtml(u.email)} · ${(u.xp||0).toLocaleString('tr-TR')} XP</div>
            </div>
            <div class="task-xp" style="color:var(--blue)">%${avgProg} ilerleme</div>
          </div>
        `;
      }).join('')}
    </div>
  `;
}

/* ===================================================================
   ADMIN PANEL (PIN korumalı)
=================================================================== */

let adminPinBuffer = '';
let adminUnlocked = false;

function renderAdminPanelEntry(){
  if(adminUnlocked) return renderAdminPanelContent();
  return `
    <div style="max-width:320px; margin:40px auto; text-align:center;">
      <i class="ti ti-shield-lock" style="font-size:32px; color:var(--orange);"></i>
      <div style="font-size:15px; font-weight:600; margin:12px 0 4px; color:var(--text-1);">Admin Panel</div>
      <div style="font-size:12px; color:var(--text-3); margin-bottom:8px;">Devam etmek için 4 haneli PIN girin (demo: 1234)</div>
      <div class="pin-dots" id="pin-dots">
        ${[0,1,2,3].map(i=>`<div class="pin-dot" id="pin-dot-${i}"></div>`).join('')}
      </div>
      <div class="admin-pin-pad">
        ${[1,2,3,4,5,6,7,8,9].map(n=>`<div class="pin-key" onclick="pinPress('${n}')">${n}</div>`).join('')}
        <div class="pin-key" onclick="pinClear()"><i class="ti ti-x"></i></div>
        <div class="pin-key" onclick="pinPress('0')">0</div>
        <div class="pin-key" onclick="pinBackspace()"><i class="ti ti-backspace"></i></div>
      </div>
    </div>
  `;
}

function pinPress(digit){
  if(adminPinBuffer.length >= 4) return;
  adminPinBuffer += digit;
  renderPinDots();
  if(adminPinBuffer.length === 4){
    setTimeout(() => {
      if(adminPinBuffer === DB.settings.adminPin){
        adminUnlocked = true;
        toast('Admin paneline giriş yapıldı.', 'success');
        navigateTo('admin-panel');
      } else {
        toast('Hatalı PIN.', 'error');
        adminPinBuffer = '';
        renderPinDots();
      }
    }, 200);
  }
}
function pinClear(){ adminPinBuffer=''; renderPinDots(); }
function pinBackspace(){ adminPinBuffer = adminPinBuffer.slice(0,-1); renderPinDots(); }
function renderPinDots(){
  for(let i=0;i<4;i++){
    const dot = document.getElementById('pin-dot-'+i);
    if(dot) dot.classList.toggle('filled', i < adminPinBuffer.length);
  }
}

function renderAdminPanelContent(){
  const pending = DB.users.filter(u=>u.status==='pending');
  const approved = DB.users.filter(u=>u.status==='approved' && u.role!=='admin');
  return `
    <div class="panel" style="margin-bottom:16px">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-user-check"></i> Onay Bekleyen Hesaplar (${pending.length})</div></div>
      ${pending.length ? pending.map(u => `
        <div class="admin-row">
          <div class="avatar">${initials(u.name)}</div>
          <div class="task-info">
            <div class="task-name">${escapeHtml(u.name)} <span style="color:var(--text-3); font-weight:400;">— ${roleLabel(u.role)}</span></div>
            <div class="task-sub">${escapeHtml(u.email)}${u.company ? ' · '+escapeHtml(u.company) : ''}</div>
          </div>
          <button class="admin-approve-btn" onclick="approveUser('${u.id}')">Onayla</button>
          <button class="admin-reject-btn" onclick="rejectUser('${u.id}')">Reddet</button>
        </div>
      `).join('') : '<div class="empty-state" style="padding:16px"><div class="empty-state-text">Onay bekleyen hesap yok.</div></div>'}
    </div>

    <div class="panel">
      <div class="panel-header"><div class="panel-title"><i class="ti ti-users"></i> Tüm Kullanıcılar (${approved.length})</div></div>
      ${approved.map(u => `
        <div class="task-item" style="cursor:default">
          <div class="avatar" style="margin-right:0">${initials(u.name)}</div>
          <div class="task-info">
            <div class="task-name">${escapeHtml(u.name)} <span style="color:var(--text-3); font-weight:400;">— ${roleLabel(u.role)}</span></div>
            <div class="task-sub">${escapeHtml(u.email)} · ${(u.xp||0).toLocaleString('tr-TR')} XP</div>
          </div>
        </div>
      `).join('')}
    </div>
  `;
}

function approveUser(userId){
  const u = DB.users.find(x=>x.id===userId);
  if(u){ u.status = 'approved'; saveDB(DB); toast(u.name + ' onaylandı.', 'success'); navigateTo('admin-panel'); }
}
function rejectUser(userId){
  const u = DB.users.find(x=>x.id===userId);
  if(u){ u.status = 'rejected'; saveDB(DB); toast(u.name + ' reddedildi.', 'default'); navigateTo('admin-panel'); }
}

/* ===================================================================
   PROFİL MODALI
=================================================================== */

function openProfileModal(){
  const user = currentUser();
  const lv = xpToLevel(user.xp||0);
  const overlay = document.createElement('div');
  overlay.className = 'modal-overlay';
  overlay.id = 'profile-modal-overlay';
  overlay.onclick = (e) => { if(e.target===overlay) closeModal('profile-modal-overlay'); };
  overlay.innerHTML = `
    <div class="modal-box fade-up">
      <div class="modal-header">
        <div class="modal-title">Profil</div>
        <button class="modal-close" onclick="closeModal('profile-modal-overlay')"><i class="ti ti-x"></i></button>
      </div>
      <div style="display:flex; align-items:center; gap:14px; margin-bottom:20px;">
        <div class="avatar" style="width:52px; height:52px; font-size:16px;">${initials(user.name)}</div>
        <div>
          <div style="font-size:15px; font-weight:600; color:var(--text-1);">${escapeHtml(user.name)}</div>
          <div style="font-size:12px; color:var(--text-3);">${escapeHtml(user.email)} · ${roleLabel(user.role)}</div>
        </div>
      </div>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-bottom:16px;">
        <div class="stat-card"><div class="stat-label">Seviye</div><div class="stat-value" style="font-size:16px">${lv.level}</div></div>
        <div class="stat-card"><div class="stat-label">Toplam XP</div><div class="stat-value" style="font-size:16px">${(user.xp||0).toLocaleString('tr-TR')}</div></div>
      </div>
      <button class="btn-secondary" style="border-color:var(--red); color:var(--red);" onclick="logout()"><i class="ti ti-logout"></i> Çıkış yap</button>
    </div>
  `;
  document.body.appendChild(overlay);
}

</script>
</body>
</html>
