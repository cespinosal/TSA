<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<title>TSA — Tower Structural Analysis</title>
<style>
/* ── Reset ─────────────────────────────────────────────────── */
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
html, body { width: 100%; height: 100%; overflow: hidden; }

:root {
  --bg-deep:    #0A1628;   /* fondo principal        */
  --bg-bar:     #060F1C;   /* barras toolbar/tabs     */
  --bg-panel:   #0D1E35;   /* superficie2 (panel)     */
  --bg-input:   #152340;   /* superficie (inputs)     */
  --bg-row:     #111D33;   /* tabla_alterno            */
  --border:     #1E3A5F;   /* borde normal             */
  --accent:     #00D4FF;   /* cyan — acento principal  */
  --btn-pri:    #185FA5;   /* primario — botón Run     */
  --btn-hov:    #1E6FBE;   /* primario_hover           */
  --txt-pri:    #E2E8F0;   /* texto principal          */
  --txt-sec:    #94A3B8;   /* texto_tenue              */
  --txt-dim:    #1E3A5F;   /* texto muy tenue (borde)  */
  --cyan:       #00D4FF;
  --menta:      #5EEAD4;
  --azul-claro: #85B7EB;
  --error:      #F87171;
  --warn:       #FBBF24;
}

body {
  display: flex;
  flex-direction: column;
  background: var(--bg-deep);
  color: var(--txt-pri);
  font-family: 'Segoe UI', Arial, sans-serif;
  font-size: 12px;
  user-select: none;
}

/* ── Toolbar ────────────────────────────────────────────────── */
.toolbar {
  display: flex;
  align-items: center;
  gap: 5px;
  height: 46px;
  padding: 0 10px;
  background: var(--bg-bar);
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
}

.logo {
  display: flex;
  flex-direction: column;
  line-height: 1.15;
  color: var(--txt-pri);
  white-space: nowrap;
  margin-right: 2px;
}
.logo-main {
  font-size: 15px;
  font-weight: 700;
  letter-spacing: 1px;
}
.logo-sub {
  font-size: 9px;
  font-weight: 400;
  letter-spacing: 1.2px;
  color: var(--txt-sec);
}

.tower-name {
  background: #121d2b;
  border: 1px solid var(--border);
  border-radius: 5px;
  padding: 3px 10px;
  color: var(--txt-sec);
  font-size: 12px;
  cursor: pointer;
  white-space: nowrap;
}

.btn {
  background: transparent;
  border: 1px solid transparent;
  border-radius: 4px;
  color: var(--txt-sec);
  padding: 0 10px;
  height: 28px;
  cursor: pointer;
  font-size: 11px;
  font-family: inherit;
  white-space: nowrap;
  transition: color .15s, background .15s;
}
.btn:hover { color: var(--txt-pri); background: #141e2c; }

.btn-accent {
  background: var(--btn-pri);
  color: #fff;
  border: none;
  border-radius: 5px;
  padding: 0 14px;
  height: 32px;
  font-weight: 600;
  font-size: 12px;
  cursor: pointer;
  font-family: inherit;
  white-space: nowrap;
  transition: background .15s;
}
.btn-accent:hover { background: var(--btn-hov); }

.btn-toggle {
  border: 1px solid var(--border);
  border-radius: 4px;
  width: 36px;
  padding: 0;
  height: 28px;
}
.btn-toggle.active {
  background: #0D2040;
  color: var(--cyan);
  border-color: var(--cyan);
}

.tb-sep { width: 1px; height: 20px; background: var(--border); margin: 0 3px; flex-shrink:0; }
.spacer { flex: 1; }

/* ── Tab bar ────────────────────────────────────────────────── */
.tabbar {
  display: flex;
  align-items: stretch;
  height: 36px;
  background: #0b1219;
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
  padding-left: 52px;  /* align with sidebar width */
}

.tab {
  background: transparent;
  border: none;
  border-bottom: 2px solid transparent;
  color: var(--txt-sec);
  padding: 0 14px;
  height: 100%;
  cursor: pointer;
  font-size: 12px;
  font-family: inherit;
  white-space: nowrap;
  transition: color .15s, background .15s;
}
.tab:hover { color: var(--txt-pri); background: #0b1520; }
.tab.active {
  color: var(--cyan);
  border-bottom-color: var(--cyan);
  background: #0D1E35;
}

.tabbar-end {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 1px;
  padding-right: 8px;
  position: relative;
}

/* ── Vista dropdown ─────────────────────────────────────────── */
#vista-menu {
  display: none;
  position: absolute;
  top: 100%;
  right: 0;
  width: 150px;
  background: #0D1E35;
  border: 1px solid var(--border);
  border-radius: 0 0 6px 6px;
  box-shadow: 0 8px 24px rgba(0,0,0,.55);
  z-index: 100;
  overflow: hidden;
}
#vista-menu.open { display: block; }
#vista-menu button {
  width: 100%;
  background: transparent;
  border: none;
  color: var(--txt-pri);
  font: 12px 'Segoe UI', sans-serif;
  padding: 9px 14px;
  text-align: left;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 10px;
  transition: background .15s;
}
#vista-menu button:hover { background: #152340; }
#vista-menu button.active { color: var(--cyan); }
.icon-btn.active { color: var(--cyan); background: #0D2040; }
.icon-btn {
  background: transparent;
  border: none;
  color: var(--txt-sec);
  width: 30px;
  height: 30px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: color .15s, background .15s;
}
.icon-btn:hover { color: var(--txt-pri); background: #141e2c; }

/* ── Main content ───────────────────────────────────────────── */
.main { display: flex; flex: 1; overflow: hidden; min-height: 0; }

/* ── Sidebar ────────────────────────────────────────────────── */
.sidebar {
  width: 52px;
  background: var(--bg-bar);
  border-right: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 8px 4px;
  gap: 3px;
  flex-shrink: 0;
  position: relative;
  z-index: 5;
}
.side-btn {
  width: 42px; height: 42px;
  border-radius: 7px;
  background: transparent;
  border: none;
  color: var(--txt-sec);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: color .15s, background .15s;
}
.side-btn svg { width: 22px; height: 22px; }
.side-btn:hover { color: var(--txt-pri); background: #141e2c; }
.side-btn.active { background: #0D2040; color: var(--cyan); }
.side-spacer { flex: 1; }

/* ── Home menu ───────────────────────────────────────────────── */
.home-menu {
  display: none;
  position: absolute;
  left: 52px;
  top: 8px;
  width: 200px;
  max-height: calc(100vh - 16px);
  overflow-y: auto;
  background: #0D1E35;
  border: 1px solid var(--border);
  border-radius: 8px;
  box-shadow: 0 8px 24px rgba(0,0,0,.55);
  z-index: 50;
}
.home-menu.open { display: block; }
.home-menu::-webkit-scrollbar { width: 4px; }
.home-menu::-webkit-scrollbar-track { background: transparent; }
.home-menu::-webkit-scrollbar-thumb { background: #263545; border-radius: 2px; }
.home-menu-title {
  padding: 8px 14px 6px;
  font-size: 10px;
  font-weight: 600;
  letter-spacing: .5px;
  color: var(--txt-sec);
  border-bottom: 1px solid var(--border);
  background: #060F1C;
}
.home-menu button {
  width: 100%;
  background: transparent;
  border: none;
  color: var(--txt-pri);
  font: 12px 'Segoe UI', sans-serif;
  padding: 9px 14px;
  text-align: left;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 10px;
  transition: background .15s;
}
.home-menu button:hover { background: #152340; }
.home-menu button svg { width: 15px; height: 15px; color: var(--txt-sec); flex-shrink: 0; }

/* ── Viewer ─────────────────────────────────────────────────── */
#viewer-wrap {
  flex: 1;
  position: relative;
  overflow: hidden;
  background: #0A1628;
  min-width: 0;
}
#viewer-wrap canvas { display: block; }

#v-overlay {
  position: absolute;
  bottom: 10px; right: 14px;
  color: rgba(0, 212, 255, 0.35);
  font: 11px monospace;
  pointer-events: none;
}


/* ── Right panel ────────────────────────────────────────────── */
.rpanel {
  width: 272px;
  flex-shrink: 0;
  display: none;          /* oculto hasta activar Torre */
  flex-direction: column;
  background: var(--bg-panel);
  border-left: 1px solid var(--border);
}
.rpanel.visible { display: flex; }

/* ── Info panel (único view del rpanel ahora) ────────────────── */
#rpanel-info { display: none; flex-direction: column; flex: 1; min-height: 0; }
#rpanel-info.visible { display: flex; }

/* ── Torre flyout (desplegable junto al botón Torre) ─────────── */
.torre-flyout {
  position: absolute;
  left: 52px;        /* pegado al borde derecho del sidebar */
  top: 53px;         /* alineado con el botón Torre */
  bottom: 12px;      /* altura exacta hasta el borde inferior de la ventana, nunca se desborda */
  width: 268px;
  background: #0D1E35;
  border: 1px solid var(--border);
  border-radius: 0 8px 8px 0;
  box-shadow: 6px 0 24px rgba(0,0,0,.5);
  z-index: 50;
  display: none;
  flex-direction: column;
}
.torre-flyout.open { display: flex; }
.tf-scroll { overflow-y: auto; min-height: 0; flex: 1; }
.tf-scroll::-webkit-scrollbar { width: 6px; }
.tf-scroll::-webkit-scrollbar-track { background: transparent; }
.tf-scroll::-webkit-scrollbar-thumb { background: #3a5a7a; border-radius: 3px; }

.tf-header {
  display: flex; align-items: center; justify-content: space-between;
  padding: 10px 14px;
  background: #060F1C;
  border-bottom: 1px solid var(--border);
  font: 600 12px 'Segoe UI', sans-serif;
  color: var(--cyan);
  flex-shrink: 0;
}
.tf-header button {
  background: transparent; border: none;
  color: var(--txt-sec); cursor: pointer; font-size: 14px; line-height: 1;
}
.tf-header button:hover { color: var(--txt-pri); }

.tf-sect  { font: 600 10px 'Segoe UI', sans-serif; color: var(--txt-sec);
            letter-spacing: .5px; padding: 10px 14px 4px; }
.tf-body  { display: flex; flex-direction: column; gap: 9px; padding: 4px 14px 10px; }
.tf-row   { display: flex; flex-direction: column; gap: 3px; }
.tf-lbl   { font-size: 10px; font-weight: 600; color: var(--txt-sec); letter-spacing: .3px; }
.tf-input {
  width: 100%; background: var(--bg-input); border: 1px solid var(--border);
  border-radius: 4px; color: var(--txt-pri); font-size: 12px;
  font-family: inherit; padding: 5px 8px; box-sizing: border-box;
  transition: border-color .15s;
}
.tf-input:focus { outline: none; border-color: var(--accent); }
.tf-sep { height: 1px; background: var(--border); margin: 4px 14px; }

/* Generar Torre button */
.gen-btn-wrap { padding: 12px 14px 16px; flex-shrink: 0; }
.gen-btn {
  width: 100%; background: var(--btn-pri); border: none; border-radius: 6px;
  color: #fff; font: 600 13px 'Segoe UI', sans-serif;
  padding: 10px 0; cursor: pointer;
  display: flex; align-items: center; justify-content: center; gap: 8px;
  transition: background .15s;
}
.gen-btn:hover { background: var(--btn-hov); }
.gen-btn svg { width: 14px; height: 14px; }

.rpanel-header {
  padding: 10px 14px;
  font-size: 13px;
  font-weight: 600;
  color: var(--cyan);
  background: #060F1C;
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
}

.rpanel-scroll {
  flex: 1;
  overflow-y: auto;
  overflow-x: hidden;
}
.rpanel-scroll::-webkit-scrollbar { width: 5px; }
.rpanel-scroll::-webkit-scrollbar-track { background: #0c1520; }
.rpanel-scroll::-webkit-scrollbar-thumb { background: #263545; border-radius: 2px; }

/* Section block */
.sect-title {
  padding: 7px 14px 5px;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: .5px;
  color: var(--txt-pri);
  background: var(--bg-row);
  border-bottom: 1px solid var(--border);
}
.sect-body {
  padding: 10px 14px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

/* Dimension grid: label col + 3 equal input cols */
.dim-grid {
  display: grid;
  grid-template-columns: 1fr 62px 62px 62px;
  column-gap: 4px;
  row-gap: 5px;
  align-items: center;
}
.dim-hdr { font-size: 10px; color: #94a3b8; text-align: center; }
.dim-lbl { font-size: 11px; color: var(--txt-sec); }

/* Generic form row: label left, control right */
.frow {
  display: flex;
  align-items: center;
  gap: 6px;
}
.frow .flbl { font-size: 11px; color: var(--txt-sec); flex: 1; }
.frow .fval { font-size: 11px; color: var(--txt-pri); font-weight: 500; }

/* Inputs */
input[type=number], input[type=text], select {
  background: var(--bg-input);
  border: 1px solid var(--border);
  border-radius: 4px;
  color: var(--txt-pri);
  font-size: 11px;
  font-family: inherit;
  padding: 3px 5px;
  min-width: 0;
  transition: border-color .15s;
}
input[type=number]:focus, input[type=text]:focus, select:focus {
  outline: none;
  border-color: var(--accent);
}
.dim-input  { width: 62px; text-align: right; }
.ctrl-input { width: 110px; }

/* Separator */
.sep {
  height: 1px;
  background: var(--border);
}

/* Guyed params block */
#guyed-params { display: none; flex-direction: column; gap: 10px; }
#guyed-params.show { display: flex; }

/* Tramos rectos toggle */
.rp-toggle { position: relative; display: inline-block; width: 34px; height: 18px; flex-shrink: 0; }
.rp-toggle input { opacity: 0; width: 0; height: 0; }
.rp-slider {
  position: absolute; inset: 0;
  background: var(--border); border-radius: 18px; cursor: pointer;
  transition: background .2s;
}
.rp-slider::before {
  content: ''; position: absolute;
  width: 12px; height: 12px; left: 3px; top: 3px;
  background: var(--txt-sec); border-radius: 50%;
  transition: transform .2s, background .2s;
}
.rp-toggle input:checked + .rp-slider { background: #185FA5; }
.rp-toggle input:checked + .rp-slider::before { transform: translateX(16px); background: var(--accent); }

/* Per-section detail cards */
.sec-card {
  padding: 10px 14px 12px;
  border-bottom: 1px solid #111c28;
}
.sec-card-hdr {
  display: flex; align-items: center; gap: 4px; margin-bottom: 8px;
  flex-wrap: nowrap; overflow: hidden;
}
.sec-card-title {
  font-size: 11px; font-weight: 700; color: #94a3b8; margin-right: 2px;
  white-space: nowrap; flex-shrink: 0;
}
.sec-tag {
  font-size: 9px; padding: 1px 5px; border-radius: 3px;
  color: #94a3b8; background: #0c1828; border: 1px solid #1b3150;
  letter-spacing: .3px;
}
.sec-tag.tipo-inc { color: #60a5fa; background: #091e36; }
.sec-tag.tipo-rec { color: #4ade80; background: #091e14; }
.sec-row-detail {
  display: flex; justify-content: space-between; align-items: baseline;
  padding: 2px 0; line-height: 1.5;
}
.sec-row-code {
  font-size: 10px; color: #94a3b8; min-width: 36px; flex-shrink: 0;
}
.sec-row-val {
  font-size: 10px; color: #7a9ab8; font-family: 'Courier New', monospace;
  text-align: right;
}
.sec-edit-btn {
  margin-left: auto; background: none; border: 1px solid #1b3150;
  color: #94a3b8; border-radius: 4px; padding: 1px 6px;
  font-size: 9px; cursor: pointer; line-height: 1.6;
}
.sec-edit-btn:hover { border-color: var(--cyan); color: var(--cyan); }

/* Secciones modal */
.sec-modal-overlay {
  display: none; position: fixed; inset: 0;
  background: rgba(5,12,25,.78); z-index: 200;
  align-items: center; justify-content: center;
}
.sec-modal-overlay.open { display: flex; }
.sec-modal {
  background: #0D1E35; border: 1px solid #1E3A5F;
  border-radius: 10px; box-shadow: 0 16px 48px rgba(0,0,0,.7);
  width: 640px; max-height: 82vh; display: flex; flex-direction: column;
}
.sec-modal-hdr {
  display: flex; align-items: center; justify-content: space-between;
  padding: 12px 16px; border-bottom: 1px solid #1E3A5F; flex-shrink: 0;
}
.sec-modal-hdr span { font-size: 12px; font-weight: 700; color: var(--txt); letter-spacing: .5px; }
.sec-modal-hdr button { background: none; border: none; color: var(--txt-dim); font-size: 16px; cursor: pointer; }
.sec-modal-body { overflow-y: auto; flex: 1; padding: 0; }
.sec-modal-body::-webkit-scrollbar { width: 4px; }
.sec-modal-body::-webkit-scrollbar-thumb { background: #263545; border-radius: 2px; }

/* Modal: cards por sección */
.sm-card { padding: 10px 16px 12px; border-bottom: 1px solid #111c28; }
.sm-card-hdr { display: flex; align-items: center; gap: 6px; margin-bottom: 8px; }
.sm-card-title { font-size: 11px; font-weight: 700; color: var(--txt); }
.sm-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 6px 12px;
}
.sm-field { display: flex; flex-direction: column; gap: 2px; }
.sm-lbl { font-size: 9px; color: #b8c8d8; letter-spacing: .4px; }
.sm-chk-row { display:flex; align-items:center; gap:6px; cursor:pointer; padding: 4px 0 2px; }
.sm-chk-row input[type=checkbox] { accent-color:#22C55E; cursor:pointer; flex-shrink:0; }
.sm-chk-lbl { font-size:9px; color:#c8d9e8; letter-spacing:.3px; user-select:none; }
.sm-preview-panel { flex:0 0 220px; display:flex; flex-direction:column; align-items:center; gap:4px; padding-top:28px; }
.sm-preview-title { font-size:8px; color:#6b85a0; letter-spacing:.5px; }
.sm-preview-box { background:#071120; border:1px solid #1b3150; border-radius:4px; padding:6px 4px; display:flex; justify-content:center; min-height:140px; }
.sm-inp {
  background: #0b1828; border: 1px solid #1E3A5F;
  color: var(--txt); border-radius: 4px; padding: 4px 6px; font-size: 10px;
  font-family: 'Courier New', monospace; width: 100%; box-sizing: border-box;
}
.sm-inp:focus { outline: none; border-color: var(--cyan); }
.sm-sel {
  background: #0b1828; border: 1px solid #1E3A5F;
  color: var(--txt); border-radius: 4px; padding: 4px 4px; font-size: 10px; width: 100%;
}
.sm-sel:focus { outline: none; border-color: var(--cyan); }
.diag-icon-grid { display: flex; flex-wrap: wrap; gap: 4px; margin-top: 4px; }
.diag-icon-btn {
  display: flex; flex-direction: column; align-items: center; gap: 2px;
  width: 52px; padding: 4px 2px; background: #0b1828; border: 1px solid #1E3A5F;
  border-radius: 4px; cursor: pointer;
}
.diag-icon-btn:hover { border-color: #3B82F6; }
.diag-icon-btn.selected { border-color: var(--cyan); background: #0e2236; }
.diag-icon-btn svg { display: block; }
.diag-icon-btn span { font-size: 9px; color: var(--txt-sec); text-align: center; line-height: 1.2; word-break: break-word; }
.diag-icon-btn.selected span { color: var(--txt-pri); }

.sec-modal-ftr {
  display: flex; gap: 8px; justify-content: flex-end;
  padding: 10px 16px; border-top: 1px solid #1E3A5F; flex-shrink: 0;
}
.sec-modal-ftr button {
  padding: 6px 18px; border-radius: 5px; font-size: 11px;
  font-weight: 600; cursor: pointer; border: 1px solid;
}
.btn-cancel { background: transparent; border-color: #1E3A5F; color: var(--txt-dim); }
.btn-apply  { background: var(--btn); border-color: var(--btn); color: #fff; }
.btn-apply:hover { background: #1e70c0; }
/* ── Export dropdown ────────────────────────────────────── */
.export-dd { position: relative; display: inline-block; }
.export-menu {
  display: none; position: absolute; top: calc(100% + 5px); right: 0;
  background: #0d1e35; border: 1px solid #1E3A5F; border-radius: 6px;
  min-width: 170px; padding: 4px 0; z-index: 300;
  box-shadow: 0 6px 18px rgba(0,0,0,.6);
}
.export-menu.open { display: block; }
.export-menu-item {
  display: block; width: 100%; background: transparent; border: none;
  color: var(--txt-sec); font-size: 11px; font-family: inherit;
  padding: 7px 14px; text-align: left; cursor: pointer; white-space: nowrap;
}
.export-menu-item:hover:not(:disabled) { background: #142030; color: var(--txt-pri); }
.export-menu-item:disabled { opacity: 0.38; cursor: not-allowed; }
.export-menu-sep { height: 1px; background: #1a2d42; margin: 3px 0; }
/* ── Toast notificación ─────────────────────────────────── */
#tsa-toast {
  position: fixed; top: 80px; left: 50%; transform: translateX(-50%);
  background: #1a2d42; border: 1px solid #2a4a6a;
  color: #e2e8f0; font-size: 12px; font-family: inherit;
  padding: 10px 20px; border-radius: 6px;
  box-shadow: 0 4px 16px rgba(0,0,0,.6);
  pointer-events: none; opacity: 0;
  transition: opacity .25s ease;
  z-index: 9999; white-space: nowrap;
}
#tsa-toast.warn  { border-color: #c47a1a; color: #fbbf24; }
#tsa-toast.show  { opacity: 1; }
/* ── Member info panel ──────────────────────────────── */
#mi-panel {
  position: fixed; z-index: 900;
  background: #0d1e35; border: 1px solid #1a4060;
  border-radius: 8px; width: max-content; max-width: 280px;
  box-shadow: 0 4px 20px rgba(0,0,0,.55);
  display: none;
}
.mi-hdr {
  display: flex; align-items: center; justify-content: space-between;
  background: #0a1628; border-bottom: 1px solid #1a4060;
  padding: 6px 10px; border-radius: 8px 8px 0 0;
}
.mi-title { font-size:11px; font-weight:700; letter-spacing:.8px; color:#00D4FF; text-transform:uppercase; }
.mi-close-btn { background:none; border:none; color:#94A3B8; cursor:pointer; font-size:14px; line-height:1; padding:0 2px; }
.mi-close-btn:hover { color:#e2e8f0; }
.mi-body { padding:8px 10px; display:grid; grid-template-columns:auto 1fr; gap:3px 10px; }
.mi-lbl { font-size:10px; color:#5a7fa8; text-transform:uppercase; letter-spacing:.5px; white-space:nowrap; }
.mi-val { font-size:11px; color:#e2e8f0; font-family:monospace; word-break:break-all; }

/* ── Grid floating panel ────────────────────────────────── */
#grid-panel {
  display: none;
  position: fixed;
  top: 84px;          /* just below tabbar */
  right: 282px;       /* left of right panel */
  width: 220px;
  background: #0D1E35;
  border: 1px solid #1E3A5F;
  border-radius: 8px;
  box-shadow: 0 8px 24px rgba(0,0,0,.5);
  z-index: 100;
  overflow: hidden;
}
#grid-panel.open { display: block; }

.gp-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 12px;
  background: #060F1C;
  border-bottom: 1px solid #1E3A5F;
  font-size: 11px;
  font-weight: 600;
  color: var(--cyan);
}
.gp-header button {
  background: transparent;
  border: none;
  color: var(--txt-sec);
  cursor: pointer;
  font-size: 13px;
  line-height: 1;
}
.gp-header button:hover { color: var(--txt-pri); }

.gp-sub {
  font-size: 10px;
  font-weight: 600;
  color: var(--azul-claro);
  letter-spacing: .4px;
  padding: 8px 12px 4px;
}

.gp-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4px 12px;
  gap: 8px;
}
.gp-row span {
  font-size: 11px;
  color: var(--txt-sec);
  flex: 1;
}
.gp-row input {
  width: 70px;
  background: var(--bg-input);
  border: 1px solid var(--border);
  border-radius: 4px;
  color: var(--txt-pri);
  font-size: 11px;
  padding: 3px 6px;
  text-align: right;
}
.gp-row input[type=number]:focus { outline: none; border-color: var(--cyan); }

.gp-sep {
  height: 1px;
  background: var(--border);
  margin: 8px 12px;
}

/* Toggle switch */
.gp-toggle { position: relative; display: inline-block; width: 36px; height: 20px; }
.gp-toggle input { opacity: 0; width: 0; height: 0; }
.gp-slider {
  position: absolute; inset: 0;
  background: #1E3A5F;
  border-radius: 20px;
  cursor: pointer;
  transition: background .2s;
}
.gp-slider::before {
  content: '';
  position: absolute;
  width: 14px; height: 14px;
  left: 3px; top: 3px;
  background: var(--txt-sec);
  border-radius: 50%;
  transition: transform .2s, background .2s;
}
.gp-toggle input:checked + .gp-slider { background: #185FA5; }
.gp-toggle input:checked + .gp-slider::before {
  transform: translateX(16px);
  background: var(--cyan);
}

/* ── Tooltip ─────────────────────────────────────────────────── */
[title] { position: relative; }
[title]:hover::after {
  content: attr(title);
  position: absolute;
  bottom: calc(100% + 6px);
  left: 50%;
  transform: translateX(-50%);
  background: #0D1E35;
  color: var(--txt-pri);
  border: 1px solid var(--border);
  border-radius: 5px;
  padding: 4px 10px;
  font-size: 11px;
  white-space: nowrap;
  pointer-events: none;
  z-index: 100;
  box-shadow: 0 4px 12px rgba(0,0,0,.5);
}

/* ── Status bar ─────────────────────────────────────────────── */
.statusbar {
  height: 26px;
  padding: 0 10px;
  display: flex;
  align-items: center;
  gap: 6px;
  background: var(--bg-bar);
  border-top: 1px solid var(--border);
  color: var(--txt-sec);
  font-size: 11px;
  flex-shrink: 0;
}
.sb-arrow { color: var(--cyan); }
</style>
</head>
<body>

<!-- ══════════════ TOOLBAR ══════════════════════════════════════ -->
<div class="toolbar">
  <span class="logo">
    <span class="logo-main">🏗 TSA</span>
    <span class="logo-sub">TOWER STRUCTURAL ANALYSIS</span>
  </span>
  <span class="tower-name">Tower 30 &nbsp;▾</span>
  <button class="btn" title="Deshacer" style="width:28px;padding:0">←</button>
  <button class="btn" title="Rehacer"  style="width:28px;padding:0">→</button>
  <button class="btn-accent">▶ &nbsp;Ejecutar Análisis</button>
  <span class="spacer"></span>
  <button class="btn btn-toggle active" id="mks-btn" onclick="setUnit(this,'MKS')" title="MKS — Metro, Kilogramo-fuerza, Segundo">MKS</button>
  <button class="btn btn-toggle"        id="imp-btn" onclick="setUnit(this,'IMP')" title="IMP — Pies, Kips, Segundo (Imperial)">IMP</button>
  <div class="tb-sep"></div>
  <button class="btn">Mostrar Resultados</button>
  <div class="export-dd">
    <button class="btn" onclick="toggleExportDD(event)">Exportar ▾</button>
    <div class="export-menu" id="export-menu">
      <button class="export-menu-item" onclick="exportSTAAD()">STAAD.Pro &nbsp;(.std)</button>
      <div class="export-menu-sep"></div>
      <button class="export-menu-item" disabled title="Próximamente">DXF &nbsp;(.dxf)</button>
    </div>
  </div>
  <button class="btn">Compartir</button>
  <button class="btn">Ayuda</button>
</div>

<!-- ══════════════ TAB BAR ══════════════════════════════════════ -->
<div class="tabbar">
  <button class="tab active">⬡ &nbsp;FEM</button>
  <button class="tab">⬡ &nbsp;Códigos</button>
  <button class="tab">&nbsp;&nbsp;Cargas Viento</button>
  <button class="tab">⬡ &nbsp;Antenas</button>
  <button class="tab">⬡ &nbsp;Escaleras</button>
  <button class="tab">⬡ &nbsp;Plataformas</button>
  <div class="tabbar-end">
    <button class="icon-btn" title="Etiquetas">🏷</button>
    <button class="icon-btn" title="Gráficas">📈</button>
    <button class="icon-btn" title="Tabla">⊞</button>
    <button class="icon-btn" id="vista-btn" title="Vista" onclick="toggleVistaMenu(event)">⊙</button>
    <button class="icon-btn" id="grid-cfg-btn" title="Configuración de malla" onclick="toggleGridPanel(event)">⚙</button>
    <div id="vista-menu">
      <button onclick="setCamFrente()">&#9633; Frente</button>
      <button id="vbtn-orbit" onclick="toggleAutoOrbit()">&#8635; Orbitar</button>
    </div>
  </div>
</div>

<!-- ══════════════ MAIN ═════════════════════════════════════════ -->
<div class="main">

  <!-- Sidebar -->
  <div class="sidebar">

    <!-- Home -->
    <button class="side-btn" id="home-btn" title="Inicio" onclick="toggleHomeMenu(event)">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
        <path d="M3 10L11 3L19 10V19H14V14H8V19H3V10Z"/>
      </svg>
    </button>

    <!-- Torre -->
    <button class="side-btn" id="torre-btn" title="Torre" onclick="switchToTorre()">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
        <!-- mástil -->
        <line x1="11" y1="4" x2="11" y2="18"/>
        <!-- patas base -->
        <line x1="11" y1="18" x2="5"  y2="22"/>
        <line x1="11" y1="18" x2="17" y2="22"/>
        <line x1="7"  y1="21" x2="15" y2="21"/>
        <!-- ondas de señal -->
        <path d="M13.5 9.5 A3.5 3.5 0 0 0 13.5 4.5"/>
        <path d="M15.5 11 A6   6   0 0 0 15.5 3"/>
      </svg>
    </button>

    <!-- Análisis -->
    <button class="side-btn" title="Análisis">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="3,16 7,10 11,13 15,6 19,9"/>
        <line x1="3" y1="19" x2="19" y2="19"/>
      </svg>
    </button>

    <!-- Optimización -->
    <button class="side-btn" title="Optimización">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
        <circle cx="11" cy="11" r="8"/>
        <circle cx="11" cy="11" r="3"/>
        <line x1="11" y1="1" x2="11" y2="4"/>
        <line x1="11" y1="18" x2="11" y2="21"/>
        <line x1="1" y1="11" x2="4" y2="11"/>
        <line x1="18" y1="11" x2="21" y2="11"/>
      </svg>
    </button>

    <div class="side-spacer"></div>

    <!-- Reporte -->
    <button class="side-btn" title="Reporte">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
        <rect x="4" y="2" width="14" height="18" rx="2"/>
        <line x1="7" y1="8"  x2="15" y2="8"/>
        <line x1="7" y1="12" x2="15" y2="12"/>
        <line x1="7" y1="16" x2="11" y2="16"/>
      </svg>
    </button>

    <!-- Ubicación -->
    <button class="side-btn" title="Ubicación">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
        <path d="M11 2C8.2 2 6 4.2 6 7C6 11 11 19 11 19C11 19 16 11 16 7C16 4.2 13.8 2 11 2Z"/>
        <circle cx="11" cy="7" r="2"/>
      </svg>
    </button>

    <!-- Config rápida -->
    <button class="side-btn" title="Configuración">
      <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
        <circle cx="11" cy="11" r="3"/>
        <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/>
      </svg>
    </button>

    <!-- Torre flyout -->
    <div class="torre-flyout" id="torre-flyout">
      <div class="tf-header">
        <span>Nueva Torre</span>
        <button onclick="closeTorreFlyout()">✕</button>
      </div>

      <div class="tf-scroll">
      <div class="tf-sect">PROYECTO</div>
      <div class="tf-body">
        <div class="tf-row"><span class="tf-lbl">ASSET NAME</span>
          <input class="tf-input" type="text" id="s-asset" placeholder="ID del activo"></div>
        <div class="tf-row"><span class="tf-lbl">SITE NAME</span>
          <input class="tf-input" type="text" id="s-site" placeholder="Nombre del sitio"></div>
        <div class="tf-row"><span class="tf-lbl">PAÍS</span>
          <input class="tf-input" type="text" id="s-pais" placeholder="México"></div>
        <div class="tf-row"><span class="tf-lbl">INGENIERO RESPONSABLE</span>
          <input class="tf-input" type="text" id="s-ing" placeholder="Nombre del ingeniero"></div>
        <div class="tf-row"><span class="tf-lbl">FECHA DE CREACIÓN</span>
          <input class="tf-input" type="date" id="s-fecha"></div>
      </div>

      <div class="tf-sep"></div>
      <div class="tf-sect">ESTRUCTURA</div>
      <div class="tf-body">
        <div class="tf-row"><span class="tf-lbl">TIPO DE ESTRUCTURA</span>
          <select class="tf-input" id="s-tipo" onchange="onSetupTipoChange()">
            <option value="triangular">Autosoportada 3 piernas</option>
            <option value="square">Autosoportada 4 piernas</option>
            <option value="guyed">Arriostrada</option>
            <option value="monopole">Monopolo</option>
          </select></div>
        <div class="tf-row"><span class="tf-lbl">ALTURA (m)</span>
          <input class="tf-input" type="number" id="s-height" value="30" min="1" max="999" step="1"></div>
        <div class="tf-row" id="s-row-base"><span class="tf-lbl">APERTURA INICIAL (m)</span>
          <input class="tf-input" type="number" id="s-baseW" value="4" min="0.5" max="99" step="0.5"></div>
        <div class="tf-row" id="s-row-top"><span class="tf-lbl">APERTURA FINAL (m)</span>
          <input class="tf-input" type="number" id="s-topW" value="2" min="0.5" max="99" step="0.5"></div>
        <div class="tf-row" id="s-row-ninc"><span class="tf-lbl">TRAMOS INCLINADOS</span>
          <input class="tf-input" type="number" id="s-nInc" value="6" min="0" max="40" step="1"></div>
        <div class="tf-row" id="s-row-nstr"><span class="tf-lbl" id="s-nstr-lbl">TRAMOS RECTOS</span>
          <input class="tf-input" type="number" id="s-nStr" value="2" min="0" max="40" step="1"></div>
        <div class="tf-row" id="s-row-guyApertura"><span class="tf-lbl">APERTURA (m) — constante</span>
          <input class="tf-input" type="number" id="s-shaftW" value="1" min="0.3" max="10" step="0.1"></div>
        <div class="tf-row" id="s-row-guyLevels"><span class="tf-lbl">NIVELES DE RETENIDAS</span>
          <input class="tf-input" type="number" id="s-guyLevels" value="3" min="1" max="10" step="1" oninput="buildGuyHeightsList()"></div>
        <div class="tf-row" id="s-row-guyHeights"><span class="tf-lbl">ALTURA DE CADA RETENIDA (m)</span>
          <div id="s-guyHeights-list" style="display:flex;flex-direction:column;gap:4px;"></div></div>
        <div class="tf-row" id="s-row-guyPivot">
          <label style="display:flex;align-items:center;gap:6px;cursor:pointer;">
            <input type="checkbox" id="s-guyPivot">
            <span class="tf-lbl" style="margin:0">TORRE CON PIVOTE</span>
          </label>
        </div>
      </div>
      </div>

      <div class="gen-btn-wrap">
        <button class="gen-btn" onclick="generateTowerFromSetup()">
          <svg viewBox="0 0 22 22" fill="currentColor"><polygon points="4,3 18,11 4,19"/></svg>
          Generar Torre
        </button>
      </div>
    </div>

    <!-- Home dropdown menu -->
    <div class="home-menu" id="home-menu">
      <div class="home-menu-title">ARCHIVO</div>
      <button onclick="nuevoProyecto()">
        <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="3" width="16" height="16" rx="2"/>
          <line x1="11" y1="7" x2="11" y2="15"/>
          <line x1="7" y1="11" x2="15" y2="11"/>
        </svg>
        Nuevo proyecto
      </button>
      <div style="height:1px;background:var(--border);margin:2px 0;"></div>
      <button onclick="openProject()">
        <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
          <path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z"/>
        </svg>
        Abrir proyecto…
      </button>
      <button onclick="saveProjectAs()">
        <svg viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
          <path d="M19 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11l5 5v11a2 2 0 0 1-2 2z"/>
          <polyline points="17 21 17 13 7 13 7 21"/>
          <polyline points="7 3 7 8 15 8"/>
          <line x1="16" y1="5" x2="19" y2="5" stroke-width="1.8"/>
          <line x1="17.5" y1="3.5" x2="17.5" y2="6.5" stroke-width="1.8"/>
        </svg>
        Guardar como…
      </button>
    </div>

  </div>

  <!-- File input oculto para Abrir proyecto -->
  <input type="file" id="file-input" accept=".TSA,.tsa,.json" style="display:none" onchange="loadProject(this)">

  <!-- 3-D Viewer -->
  <div id="viewer-wrap">
  </div>

  <!-- Right Panel -->
  <div class="rpanel" id="rpanel">

    <!-- ═══ INFO VIEW ═══════════════════════════════════════════ -->
    <div id="rpanel-info">
      <div class="rpanel-header">Panel de Información</div>
      <div class="rpanel-scroll">

        <!-- PROYECTO -->
        <div class="sect-title">PROYECTO</div>
        <div class="sect-body" style="gap:8px;">
          <div class="frow">
            <span class="flbl">Asset Name:</span>
            <input class="ctrl-input" type="text" id="assetName" style="width:120px;" placeholder="—">
          </div>
          <div class="frow">
            <span class="flbl">Site Name:</span>
            <input class="ctrl-input" type="text" id="siteName" style="width:120px;" placeholder="—">
          </div>
          <div class="frow">
            <span class="flbl">País:</span>
            <input class="ctrl-input" type="text" id="pais" style="width:120px;" placeholder="—">
          </div>
          <div class="frow">
            <span class="flbl">Ing. Responsable:</span>
            <input class="ctrl-input" type="text" id="ingResponsable" style="width:120px;" placeholder="—">
          </div>
          <div class="frow">
            <span class="flbl">Fecha de creación:</span>
            <input class="ctrl-input" type="date" id="fechaCreacion" style="width:120px;">
          </div>
        </div>

        <div class="sep"></div>

        <!-- GEOMETRÍA -->
        <div class="sect-title">GEOMETRÍA DE LA TORRE</div>
        <div class="sect-body">

          <div class="dim-grid">
            <span class="dim-hdr"></span>
            <span class="dim-hdr">Inicial</span>
            <span class="dim-hdr">Final</span>
            <span class="dim-hdr">Altura</span>
            <span class="dim-lbl">Valor</span>
            <input class="dim-input" type="number" id="baseW"  value="4"  min="0.5" max="99"  step="0.5" oninput="refresh()">
            <input class="dim-input" type="number" id="topW"   value="2"  min="0.5" max="99"  step="0.5" oninput="refresh()">
            <input class="dim-input" type="number" id="height" value="30" min="1"   max="999" step="1"   oninput="refresh()">
          </div>

          <div class="sep"></div>

          <div class="frow">
            <span class="flbl">Tipo:</span>
            <select class="ctrl-input" id="ttype" onchange="onTypeChange()">
              <option value="triangular">Autosoportada 3P</option>
              <option value="square">Autosoportada 4P</option>
              <option value="guyed">Arriostrada</option>
              <option value="monopole">Monopolo</option>
            </select>
          </div>

          <div class="frow">
            <span class="flbl">Tramos inclinados:</span>
            <input class="ctrl-input" type="number" id="nInc" value="6" min="0" max="40" step="1" oninput="onSecChange()">
          </div>
          <div class="frow">
            <span class="flbl">Tramos rectos:</span>
            <input class="ctrl-input" type="number" id="nStr" value="2" min="0" max="40" step="1" oninput="onSecChange()">
          </div>

          <div id="guyed-params">
            <div class="sep"></div>
            <div class="frow">
              <span class="flbl">Ancho fuste:</span>
              <input class="ctrl-input" type="number" id="shaftW" value="1" min="0.3" max="10" step="0.1" oninput="refresh()">
            </div>
            <div class="frow">
              <span class="flbl">Niveles vientos:</span>
              <input class="ctrl-input" type="number" id="guyLevels" value="3" min="1" max="10" step="1" oninput="refresh()">
            </div>
            <div class="frow">
              <span class="flbl">Radio anclaje:</span>
              <input class="ctrl-input" type="number" id="anchorR" value="15" min="5" max="200" step="1" oninput="refresh()">
            </div>
            <div class="frow">
              <span class="flbl">Perfil cable:</span>
              <input class="ctrl-input" type="text" id="guyProfile" placeholder="ej. Cable 1/2&quot; EHS" oninput="refresh()">
            </div>
          </div>

          <div class="frow">
            <span class="flbl">Peso total:</span>
            <span class="fval">0 kg</span>
          </div>

        </div><!-- /sect-body geom -->

        <div class="sep"></div>
        <div class="sect-title">DETALLE POR SECCIÓN</div>
        <div id="sec-container"></div>

      </div><!-- /rpanel-scroll info -->
    </div><!-- /rpanel-info -->

  </div><!-- /rpanel -->

</div><!-- /main -->

<!-- ══════════════ STATUS BAR ═══════════════════════════════════ -->
<div class="statusbar">
  <span class="sb-arrow">›</span>
  <span id="status">Iniciando TSA…</span>
  <span style="margin-left:auto; color:var(--txt-sec); font-size:10px; letter-spacing:.3px;">
    Created by: Ing Juan Christian Espinosa López
  </span>
</div>

<!-- ── Grid config floating panel ──────────────────────────── -->
<div id="grid-panel">
  <div class="gp-header">
    <span>⚙&nbsp; Configuración de Malla</span>
    <button onclick="toggleGridPanel()">✕</button>
  </div>

  <div class="gp-sub">Malla principal</div>
  <div class="gp-row">
    <span>Tamaño (m)</span>
    <input type="number" id="grid-size"  value="200" min="50"  max="2000" step="50"  oninput="refreshGrid()">
  </div>
  <div class="gp-row">
    <span>Divisiones</span>
    <input type="number" id="grid-divs"  value="10"  min="2"   max="50"   step="1"   oninput="refreshGrid()">
  </div>
  <div class="gp-row">
    <span>Grosor (px)</span>
    <input type="number" id="grid-thick" value="1.5" min="0.5" max="8"    step="0.5" oninput="refreshGrid()">
  </div>

  <div class="gp-sub" style="margin-top:10px;">Malla secundaria</div>
  <div class="gp-row">
    <span>Subdivisiones</span>
    <input type="number" id="grid-subs"  value="5"   min="2"   max="20"   step="1"   oninput="refreshGrid()">
  </div>

  <div class="gp-sep"></div>

  <div class="gp-sub">Fade circular</div>
  <div class="gp-row">
    <span>Activar</span>
    <label class="gp-toggle">
      <input type="checkbox" id="fade-on" checked onchange="refreshGrid()">
      <span class="gp-slider"></span>
    </label>
  </div>
  <div class="gp-row">
    <span>Inicio (%)</span>
    <input type="number" id="fade-start" value="45" min="0" max="95" step="5" oninput="refreshGrid()">
  </div>
  <div class="gp-row" style="padding-bottom:12px;">
    <span>Intensidad</span>
    <input type="range"  id="fade-exp"   value="2"  min="1" max="5"  step="0.5" oninput="refreshGrid()" style="width:70px;accent-color:var(--cyan);">
  </div>
</div>

<!-- ── Modal editor de secciones ─────────────────────────────── -->
<div class="sec-modal-overlay" id="sec-modal-overlay" onclick="closeSecModal(event)">
  <div class="sec-modal" onclick="event.stopPropagation()">
    <div class="sec-modal-hdr">
      <span id="sec-modal-title">EDITOR DE SECCIÓN</span>
      <button onclick="closeSecModal()">✕</button>
    </div>
    <div class="sec-modal-body" id="sec-modal-body"></div>
    <div class="sec-modal-ftr">
      <button class="btn-cancel" onclick="closeSecModal()">Cancelar</button>
      <button class="btn-apply"  onclick="applySecModal()">Aplicar</button>
    </div>
  </div>
</div>

<!-- ── Three.js ──────────────────────────────────────────────── -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/lines/LineSegmentsGeometry.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/lines/LineMaterial.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/lines/LineSegments2.js"></script>
<script>
// ══════════════════════════════════════════════════════════════════
//  TOWER GENERATOR
// ══════════════════════════════════════════════════════════════════
function generateTower(cfg) {
  return cfg.type === 'square'   ? genSquare(cfg)
       : cfg.type === 'guyed'    ? genGuyed(cfg)
       : cfg.type === 'monopole' ? genMonopole(cfg)
       :                           genTriangular(cfg);
}

// Monopolo: tubo cilíndrico (12 líneas verticales + anillos)
function genMonopole(cfg) {
  const SEGS = 12;
  const ANG  = Array.from({length: SEGS}, (_, i) => i * 2 * Math.PI / SEGS);
  const {nodes, members, lnodes} = initBuffers();
  const nTot = (cfg.nInc + cfg.nStr) || 8;
  for (let lv = 0; lv <= nTot; lv++) {
    const t = lv / nTot;
    const r = (cfg.baseW + (cfg.topW - cfg.baseW) * t) / 2;
    lnodes.push(ANG.map(a => addNode(nodes, r*Math.cos(a), r*Math.sin(a), cfg.height*t)));
  }
  // Líneas verticales
  for (let lv = 0; lv < nTot; lv++)
    for (let j = 0; j < SEGS; j++)
      members.push({ni: lnodes[lv][j], nj: lnodes[lv+1][j], type: 'leg', sec: lv});
  // Anillos horizontales en cada nivel
  for (let lv = 0; lv <= nTot; lv++)
    for (let j = 0; j < SEGS; j++)
      members.push({ni: lnodes[lv][j], nj: lnodes[lv][(j+1)%SEGS], type: 'horizontal', sec: lv});
  return {nodes, members};
}

// Generador unificado: nInc tramos cónicos + nStr tramos rectos, con bahías.
function genMixed(cfg, ANG, radiusFn) {
  const {nodes, members, lnodes} = initBuffers();
  const nLegs = ANG.length;
  const nTot  = cfg.nInc + cfg.nStr;
  if (nTot === 0) return {nodes, members};

  const hSec = cfg.height / nTot;
  const zInc = cfg.nInc > 0 ? cfg.height * cfg.nInc / nTot : 0;

  const levelAt = z => {
    const t = zInc > 0 ? Math.min(z / zInc, 1) : 1;
    const R = radiusFn(t);
    return ANG.map(a => addNode(nodes, R*Math.cos(a), R*Math.sin(a), z));
  };

  lnodes.push(levelAt(0));
  const secForLevel = [];
  let z = 0;
  for (let sec = 0; sec < nTot; sec++) {
    const bays = Math.max(1, secData[sec]?.bays || 1);
    const hBay = hSec / bays;
    for (let b = 0; b < bays; b++) {
      z += hBay;
      lnodes.push(levelAt(z));
      secForLevel.push(sec);
    }
  }

  const patterns = secData.map(s => s?.diag || 'X');
  const structNodes = nodes.length;   // nodos estructurales antes del bracing
  addMembersWithSecs(nodes, members, lnodes, nLegs, secForLevel, patterns);
  return {nodes, members, structNodes};
}

function genTriangular(cfg) {
  const ANG = [90,210,330].map(d => d*Math.PI/180);
  return genMixed(cfg, ANG, t => (cfg.baseW+(cfg.topW-cfg.baseW)*t)/Math.sqrt(3));
}

function genSquare(cfg) {
  const ANG = [45,135,225,315].map(d => d*Math.PI/180);
  return genMixed(cfg, ANG, t => (cfg.baseW+(cfg.topW-cfg.baseW)*t)*Math.SQRT2/2);
}

function genGuyed(cfg) {
  const ANG = [90,210,330].map(d => d*Math.PI/180);
  const {nodes, members, lnodes} = initBuffers();
  const R0 = cfg.shaftW/Math.sqrt(3);
  for (let lv = 0; lv <= cfg.nsec; lv++)
    lnodes.push(ANG.map(a => addNode(nodes, R0*Math.cos(a), R0*Math.sin(a), cfg.height*lv/cfg.nsec)));
  const secForLv = Array.from({length:cfg.nsec}, (_,i) => i);
  const patterns = secData.map(s => s?.diag || 'X');
  addMembersWithSecs(nodes, members, lnodes, 3, secForLv, patterns);
  const ancIds = ANG.map(a => addNode(nodes, cfg.anchorR*Math.cos(a), cfg.anchorR*Math.sin(a), 0));
  for (let g=1; g<=cfg.guyLevels; g++) {
    const gLv = Math.round(g*cfg.nsec/(cfg.guyLevels+1));
    // Cada pierna k conecta a su propio anclaje k (misma dirección angular) — no las 3 a la pierna 0
    ancIds.forEach((aid, k) => members.push({ni:lnodes[gLv][k], nj:aid, type:'guy', guyLevel:g}));
  }
  return {nodes, members};
}

function initBuffers() { return {nodes:[], members:[], lnodes:[]}; }
function addNode(nodes, x, y, z) { nodes.push({x:-x, y:-y, z}); return nodes.length-1; }
function addRawNode(nodes, x, y, z) { nodes.push({x, y, z}); return nodes.length-1; }
function _midNode(nodes, a, b) {
  const na = nodes[a], nb = nodes[b];
  return addRawNode(nodes, (na.x+nb.x)/2, (na.y+nb.y)/2, (na.z+nb.z)/2);
}

// Plan bracing (diafragma en planta): conecta los puntos medios de los lados del polígono
// formado por "corners" (Diaphragm 1) y, en el patrón A-A, agrega el triángulo medial de
// cada triángulo de esquina sobrante (Diaphragm 2). Reemplaza el horizontal perimetral
// completo de cada lado por 2 segmentos partidos en su punto medio.
function addPlanBracing(nodes, members, sec, pattern, corners, isTop) {
  if (!pattern || pattern === 'none') return;
  const n = corners.length;
  const mids = corners.map((c, i) => {
    const nb = corners[(i+1)%n];
    const idx = members.findIndex(m => m.type==='horizontal' && m.sec===sec &&
      ((m.ni===c && m.nj===nb) || (m.ni===nb && m.nj===c)));
    const mid = _midNode(nodes, c, nb);
    if (idx !== -1) {
      members.splice(idx, 1,
        {ni:c, nj:mid, type:'horizontal', sec, principal:true},
        {ni:mid, nj:nb, type:'horizontal', sec, principal:true});
    }
    return mid;
  });
  const pb = (a,b,isCorner=false) => members.push({ni:a, nj:b, type:'planbrace', sec, isTop, isCorner});
  for (let i = 0; i < n; i++) pb(mids[i], mids[(i+1)%n]);   // Diaphragm 1
  if (pattern === 'A-A') {
    for (let i = 0; i < n; i++) {                            // Diaphragm 2 — esquinas
      const corner = corners[i], mPrev = mids[(i-1+n)%n], mNext = mids[i];
      const mA = _midNode(nodes, corner, mPrev);
      const mB = _midNode(nodes, mPrev, mNext);
      const mC = _midNode(nodes, mNext, corner);
      pb(mA,mB,true); pb(mB,mC,true); pb(mC,mA,true);
    }
  }
}

function addMembersWithSecs(nodes, members, lnodes, nLegs, secForLevel, patterns) {
  const nSpans = secForLevel.length;
  for (let lv = 0; lv < nSpans; lv++) {
    const sec = secForLevel[lv];
    const pat = patterns[sec] || 'X';
    // isTopBay: última bahía de la sección (comparte nodo con el tramo siguiente)
    const isTopBay = (lv === nSpans - 1) || (secForLevel[lv + 1] !== sec);
    // Bracing por cara — retorna nodos de corte de pierna
    const legCuts = {};
    const hipPtsByFace = {};
    for (let f = 0; f < nLegs; f++) {
      const {legL, legR, hipPts} = addFaceBracing(nodes, members, sec, pat,
        lnodes[lv][f], lnodes[lv][(f+1)%nLegs],
        lnodes[lv+1][f], lnodes[lv+1][(f+1)%nLegs], lv, isTopBay);
      legL.forEach(n => (legCuts[f] = legCuts[f]||[]).push(n));
      legR.forEach(n => (legCuts[(f+1)%nLegs] = legCuts[(f+1)%nLegs]||[]).push(n));
      hipPtsByFace[f] = hipPts;
    }
    // Piernas divididas en los puntos de corte
    for (let j = 0; j < nLegs; j++) {
      const cuts = (legCuts[j]||[]).sort((a,b) => nodes[a].z - nodes[b].z);
      let prev = lnodes[lv][j];
      for (const c of cuts) { members.push({ni:prev, nj:c, type:'leg', sec}); prev = c; }
      members.push({ni:prev, nj:lnodes[lv+1][j], type:'leg', sec});
    }
    // Plan bracing — solo en bahías con horizontal de tope activo
    if (isTopBay && secData[sec]?.topH !== false) {
      addPlanBracing(nodes, members, sec, secData[sec]?.planTop, lnodes[lv+1], true);
    } else if (!isTopBay && secData[sec]?.bayTopH) {
      addPlanBracing(nodes, members, sec, secData[sec]?.planBay, lnodes[lv+1], false);
    }
    // Hip bracing — conecta caras adyacentes a través de cada hip (solo X-25Pct)
    addHipBracing(nodes, members, sec, secData[sec]?.hip, hipPtsByFace, nLegs);
  }
}

function addHipBracing(nodes, members, sec, option, hipPtsByFace, nLegs) {
  if (!option || option === 'none') return;
  const hb = (a, b, isDiag=false, isDiaphragm=false) => members.push({ni:a, nj:b, type:'hipbrace', sec, isDiag, isDiaphragm});
  for (let i = 0; i < nLegs; i++) {
    const L = hipPtsByFace[i], R = hipPtsByFace[(i+1)%nLegs];
    if (!L || !R || L.kind !== R.kind) continue;   // la cara no tiene puntos compatibles para hip bracing

    if (L.kind === 'x25') {
      hb(L.D1H, R.D2H);
      hb(L.D2L, R.D1L);
      if (option === '1') continue;
      hb(L.IX, R.IX, false, true);   // a media altura, NO redundante con plan bracing (que opera en el tope)
      if (option === '2') continue;
      if (option === '3') {
        hb(L.IX, R.D2H, true);
        hb(L.D2L, R.IX, true);
      } else if (option === '4') {
        hb(L.IX, R.D2H, true);
        hb(R.D1L, L.IX, true);
      }
    } else if (L.kind === 'k25') {
      if (option === '1') {
        hb(L.P2R, R.P2L);
        hb(L.P2R, R.TC, true);
      } else if (option === '2' || option === '3') {
        hb(L.P1R, R.P1L);
        hb(L.P2R, R.P2L);
        hb(L.P3R, R.P3L);
        if (option === '3') {
          hb(R.P1L, L.P2R, true);
          hb(R.P2L, L.P3R, true);
          hb(R.P3L, L.TC, true);
        }
      }
    } else if (L.kind === 'k33') {
      hb(L.P1R, R.P1L);
      hb(L.P2R, R.P2L);
      if (option === '2') {
        hb(R.P1L, L.P2R, true);
        hb(R.P2L, L.TC, true);
      }
    } else if (L.kind === 'k50') {
      hb(L.PR, R.PL);
      if (option === '2') {
        hb(R.PL, L.TC, true);
      }
    }
  }
}

function addFaceBracing(nodes, members, sec, pat, BL, BR, TL, TR, bayIdx, isTopBay=true) {
  // principal=true por defecto; se marca false para elementos secundarios (bracing auxiliar)
  const d = (a,b,principal=true) => members.push({ni:a, nj:b, type:'diagonal',   sec, principal});
  const h = (a,b,principal=true) => members.push({ni:a, nj:b, type:'horizontal', sec, principal});
  const lerp = (a,b,t) => {
    const na=nodes[a], nb=nodes[b];
    return addRawNode(nodes, na.x+(nb.x-na.x)*t, na.y+(nb.y-na.y)*t, na.z+(nb.z-na.z)*t);
  };
  const mid = (a,b) => lerp(a,b,0.5);
  // Conecta ML→[pts ordenados por proyección]→MR como segmentos horizontales
  const sortH = (ML, MR, ...pts) => {
    const nML=nodes[ML], nMR=nodes[MR];
    const dx=nMR.x-nML.x, dy=nMR.y-nML.y, dz=nMR.z-nML.z;
    const proj = id => { const n=nodes[id]; return (n.x-nML.x)*dx+(n.y-nML.y)*dy+(n.z-nML.z)*dz; };
    const sorted = pts.slice().sort((a,b)=>proj(a)-proj(b));
    let prev=ML; sorted.forEach(p=>{ h(prev,p); prev=p; }); h(prev,MR);
  };
  // Parámetro t de la intersección real de las dos diagonales (BL→TR y BR→TL).
  // Como ambas abarcan el mismo rango z, t=s. Se resuelve en x o y.
  const xInt = () => {
    const nBL=nodes[BL], nBR=nodes[BR], nTL=nodes[TL], nTR=nodes[TR];
    const dX=(nTR.x-nTL.x)+(nBR.x-nBL.x);
    const dY=(nTR.y-nTL.y)+(nBR.y-nBL.y);
    let t = Math.abs(dX)>1e-9 ? (nBR.x-nBL.x)/dX
           : Math.abs(dY)>1e-9 ? (nBR.y-nBL.y)/dY : 0.5;
    return Math.max(0.05, Math.min(0.95, t));
  };

  let legL=[], legR=[];   // nodos de corte de pierna izq. y der.
  let hipPts = null;      // puntos IX/D1H/D2L/D1L/D2H — solo X-25Pct (usados por Hip Bracing)

  switch(pat) {

    case 'X':
      d(BL,TR); d(BR,TL);
      break;

    case 'X-50Pct': {
      const t = xInt();
      const IX = lerp(BL,TR,t);          // único nodo: intersección real de diagonales
      const ML = lerp(BL,TL,t);          // corte pierna izq. a la misma altura
      const MR = lerp(BR,TR,t);          // corte pierna der. a la misma altura
      h(ML,IX,false); h(IX,MR,false);    // horizontal desde IX hacia ambas piernas — secundario
      d(BL,IX); d(IX,TR);                // diagonal 1 dividida en IX
      d(BR,IX); d(IX,TL);                // diagonal 2 dividida en IX
      legL=[ML]; legR=[MR];
      break;
    }

    case 'X-25Pct': {
      // 1. Misma base que X-50Pct: IX real + cortes ML/MR en piernas
      const t  = xInt();
      const IX = lerp(BL,TR,t);
      const ML = lerp(BL,TL,t);
      const MR = lerp(BR,TR,t);
      // 2. Las mitades de pierna son el nuevo 100%: cortar al 50%
      const tL = t/2,  tH = (1+t)/2;
      const ML_L = lerp(BL,TL,tL),  MR_L = lerp(BR,TR,tL);
      const ML_U = lerp(BL,TL,tH),  MR_U = lerp(BR,TR,tH);
      // 3. Puntos donde cada diagonal cruza esos niveles de altura
      const D1L = lerp(BL,TR,tL),  D2L = lerp(BR,TL,tL);   // nivel bajo
      const D1H = lerp(BL,TR,tH),  D2H = lerp(BR,TL,tH);   // nivel alto
      // 4. Media-horizontal desde cada pierna hasta su diagonal más cercana
      //    Bajo IX: D1 queda del lado izq. (viene de BL), D2 del der.
      //    Sobre IX: D2 pasó al lado izq., D1 al der.
      h(ML_L, D1L,false);  h(MR_L, D2L,false);   // nivel bajo — secundario
      h(ML,IX,false); h(IX,MR,false);             // nivel medio (intersección) — secundario
      h(ML_U, D2H,false);  h(MR_U, D1H,false);   // nivel alto (diagonales invertidas) — secundario
      // 5. Diagonales principales divididas en 4 nodos cada una
      d(BL,D1L); d(D1L,IX); d(IX,D1H); d(D1H,TR);
      d(BR,D2L); d(D2L,IX); d(IX,D2H); d(D2H,TL);
      // Member 2: D1L→ML (izq) y espejo D2L→MR (der) — celosía secundaria
      d(D1L, ML,false);  d(D2L, MR,false);
      // Member 4: ML→D2H (izq) y espejo MR→D1H (der) — celosía secundaria
      d(ML, D2H,false);  d(MR, D1H,false);
      // 6. Cortes en piernas (4 sub-segmentos cada una)
      legL=[ML_L,ML,ML_U];  legR=[MR_L,MR,MR_U];
      hipPts = {kind:'x25', IX, D1H, D2L, D1L, D2H};
      break;
    }

    case 'K': {
      const TC = mid(TL,TR);
      d(BL,TC); d(BR,TC);
      break;
    }

    case 'K-Rev': {
      const BC = mid(BL,BR);
      d(TL,BC); d(TR,BC);
      break;
    }

    case 'K-50Pct': {
      const TC = mid(TL,TR);           // vértice K en el top center
      const ML = lerp(BL,TL,.5);      // corte pierna izq a 50%
      const MR = lerp(BR,TR,.5);      // corte pierna der a 50%
      const PL = lerp(BL,TC,.5);      // diagonal K izq a la misma altura que ML
      const PR = lerp(BR,TC,.5);      // diagonal K der a la misma altura que MR
      d(BL,PL); d(PL,TC);            // diagonal K izq dividida en PL — PRINCIPAL
      d(BR,PR); d(PR,TC);            // diagonal K der dividida en PR — PRINCIPAL
      h(ML,PL,false);                 // horizontal: pierna izq → intersección K — secundario
      h(MR,PR,false);                 // horizontal: pierna der → intersección K — secundario
      d(PL,TL,false);                 // Member 2: PL → TL — secundario
      d(PR,TR,false);                 // Member 2 espejo: PR → TR — secundario
      legL=[ML]; legR=[MR];
      hipPts = {kind:'k50', PL, PR, TC};
      break;
    }

    case 'K-50Pct-Rev': {
      const BC = mid(BL,BR);           // vértice K-Rev en el bottom center
      const ML = lerp(BL,TL,.5);      // corte pierna izq a 50%
      const MR = lerp(BR,TR,.5);      // corte pierna der a 50%
      const PL = lerp(TL,BC,.5);      // diagonal K-Rev izq a la misma altura que ML
      const PR = lerp(TR,BC,.5);      // diagonal K-Rev der a la misma altura que MR
      d(TL,PL); d(PL,BC);            // diagonal K-Rev izq dividida en PL — PRINCIPAL
      d(TR,PR); d(PR,BC);            // diagonal K-Rev der dividida en PR — PRINCIPAL
      h(ML,PL,false);                 // horizontal: pierna izq → intersección K-Rev — secundario
      h(MR,PR,false);                 // horizontal: pierna der → intersección K-Rev — secundario
      d(PL,BL,false);                 // Member 2: PL → BL — secundario
      d(PR,BR,false);                 // Member 2 espejo: PR → BR — secundario
      legL=[ML]; legR=[MR];
      hipPts = {kind:'k50', PL, PR, TC: BC};
      break;
    }

    case 'K-33Pct': {
      const TC  = mid(TL,TR);
      const L1  = lerp(BL,TL,1/3), R1  = lerp(BR,TR,1/3);
      const L2  = lerp(BL,TL,2/3), R2  = lerp(BR,TR,2/3);
      const P1L = lerp(BL,TC,1/3), P1R = lerp(BR,TC,1/3);
      const P2L = lerp(BL,TC,2/3), P2R = lerp(BR,TC,2/3);
      d(BL,P1L); d(P1L,P2L); d(P2L,TC);   // cadena K — PRINCIPAL
      d(BR,P1R); d(P1R,P2R); d(P2R,TC);   // cadena K — PRINCIPAL
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,TL,false); d(P2R,TR,false);
      legL=[L1,L2]; legR=[R1,R2];
      hipPts = {kind:'k33', P1L,P2L,P1R,P2R,TC};
      break;
    }

    case 'K-33Pct-Rev': {
      const BC  = mid(BL,BR);
      const LA  = lerp(BL,TL,1/3), RA  = lerp(BR,TR,1/3);
      const LB  = lerp(BL,TL,2/3), RB  = lerp(BR,TR,2/3);
      const P1L = lerp(TL,BC,1/3), P1R = lerp(TR,BC,1/3);
      const P2L = lerp(TL,BC,2/3), P2R = lerp(TR,BC,2/3);
      d(TL,P1L); d(P1L,P2L); d(P2L,BC);   // cadena K — PRINCIPAL
      d(TR,P1R); d(P1R,P2R); d(P2R,BC);   // cadena K — PRINCIPAL
      h(LB,P1L,false); h(RB,P1R,false);
      h(LA,P2L,false); h(RA,P2R,false);
      d(P1L,LA,false); d(P1R,RA,false);
      d(P2L,BL,false); d(P2R,BR,false);
      legL=[LA,LB]; legR=[RA,RB];
      hipPts = {kind:'k33', P1L,P2L,P1R,P2R, TC: BC};
      break;
    }

    case 'K-25Pct': {
      const TC  = mid(TL,TR);
      const L1  = lerp(BL,TL,1/4), R1  = lerp(BR,TR,1/4);
      const L2  = lerp(BL,TL,2/4), R2  = lerp(BR,TR,2/4);
      const L3  = lerp(BL,TL,3/4), R3  = lerp(BR,TR,3/4);
      const P1L = lerp(BL,TC,1/4), P1R = lerp(BR,TC,1/4);
      const P2L = lerp(BL,TC,2/4), P2R = lerp(BR,TC,2/4);
      const P3L = lerp(BL,TC,3/4), P3R = lerp(BR,TC,3/4);
      d(BL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,TC);   // cadena K — PRINCIPAL
      d(BR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,TC);   // cadena K — PRINCIPAL
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      h(L3,P3L,false); h(R3,P3R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,L3,false); d(P2R,R3,false);
      d(P3L,TL,false); d(P3R,TR,false);
      legL=[L1,L2,L3]; legR=[R1,R2,R3];
      hipPts = {kind:'k25', P1L,P2L,P3L,P1R,P2R,P3R,TC};
      break;
    }

    case 'K-25Pct-Rev': {
      const BC  = mid(BL,BR);
      const LA  = lerp(BL,TL,1/4), RA  = lerp(BR,TR,1/4);
      const LB  = lerp(BL,TL,2/4), RB  = lerp(BR,TR,2/4);
      const LC  = lerp(BL,TL,3/4), RC  = lerp(BR,TR,3/4);
      const P1L = lerp(TL,BC,1/4), P1R = lerp(TR,BC,1/4);
      const P2L = lerp(TL,BC,2/4), P2R = lerp(TR,BC,2/4);
      const P3L = lerp(TL,BC,3/4), P3R = lerp(TR,BC,3/4);
      d(TL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,BC);   // cadena K — PRINCIPAL
      d(TR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,BC);   // cadena K — PRINCIPAL
      h(LC,P1L,false); h(RC,P1R,false);
      h(LB,P2L,false); h(RB,P2R,false);
      h(LA,P3L,false); h(RA,P3R,false);
      d(P1L,LB,false); d(P1R,RB,false);
      d(P2L,LA,false); d(P2R,RA,false);
      d(P3L,BL,false); d(P3R,BR,false);
      legL=[LA,LB,LC]; legR=[RA,RB,RC];
      hipPts = {kind:'k25', P1L,P2L,P3L,P1R,P2R,P3R, TC: BC};
      break;
    }

    case 'K-25Pct2': {
      const TC  = mid(TL,TR);
      const TLC = mid(TL,TC), TRC = mid(TR,TC);
      const L1  = lerp(BL,TL,1/4), R1  = lerp(BR,TR,1/4);
      const L2  = lerp(BL,TL,2/4), R2  = lerp(BR,TR,2/4);
      const L3  = lerp(BL,TL,3/4), R3  = lerp(BR,TR,3/4);
      const P1L = lerp(BL,TC,1/4), P1R = lerp(BR,TC,1/4);
      const P2L = lerp(BL,TC,2/4), P2R = lerp(BR,TC,2/4);
      const P3L = lerp(BL,TC,3/4), P3R = lerp(BR,TC,3/4);
      if ((isTopBay && secData[sec]?.topH !== false) || (!isTopBay && secData[sec]?.bayTopH)) { h(TL,TLC); h(TLC,TRC); h(TRC,TR); }   // horizontal de tope — PRINCIPAL
      d(BL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,TC);   // cadena K — PRINCIPAL
      d(BR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,TC);   // cadena K — PRINCIPAL
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      h(L3,P3L,false); h(R3,P3R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,L3,false); d(P2R,R3,false);
      d(L3,TLC,false); d(R3,TRC,false);
      d(P3L,TLC,false); d(P3R,TRC,false);
      legL=[L1,L2,L3]; legR=[R1,R2,R3];
      hipPts = {kind:'k25', P1L,P2L,P3L,P1R,P2R,P3R,TC};
      break;
    }

    case 'K-25Pct2-Rev': {
      const BC  = mid(BL,BR);
      const BLC = mid(BL,BC), BRC = mid(BR,BC);
      const LA  = lerp(BL,TL,1/4), RA  = lerp(BR,TR,1/4);
      const LB  = lerp(BL,TL,2/4), RB  = lerp(BR,TR,2/4);
      const LC  = lerp(BL,TL,3/4), RC  = lerp(BR,TR,3/4);
      const P1L = lerp(TL,BC,1/4), P1R = lerp(TR,BC,1/4);
      const P2L = lerp(TL,BC,2/4), P2R = lerp(TR,BC,2/4);
      const P3L = lerp(TL,BC,3/4), P3R = lerp(TR,BC,3/4);
      d(TL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,BC);   // cadena K — PRINCIPAL
      d(TR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,BC);   // cadena K — PRINCIPAL
      h(LC,P1L,false); h(RC,P1R,false);
      h(LB,P2L,false); h(RB,P2R,false);
      h(LA,P3L,false); h(RA,P3R,false);
      d(P1L,LB,false); d(P1R,RB,false);
      d(P2L,LA,false); d(P2R,RA,false);
      d(LA,BLC,false); d(RA,BRC,false);
      d(P3L,BLC,false); d(P3R,BRC,false);
      legL=[LA,LB,LC]; legR=[RA,RB,RC];
      break;
    }

    case 'Staggered': {
      const flip = !!secData[sec]?.staggerFlip;
      if ((bayIdx%2===0) !== flip) d(BL,TR); else d(BR,TL);
      break;
    }

    case 'Staggered-50Pct': {
      const flip = !!secData[sec]?.staggerFlip;
      const ML=lerp(BL,TL,.5), MR=lerp(BR,TR,.5);
      h(ML,MR);
      if ((bayIdx%2===0) !== flip) d(BL,TR); else d(BR,TL);
      legL=[ML]; legR=[MR];
      break;
    }

    default:
      d(BL,TR); d(BR,TL);
  }
  if (pat !== 'K-25Pct2') {
    if (isTopBay && secData[sec]?.topH !== false) h(TL,TR);
    else if (!isTopBay && secData[sec]?.bayTopH) h(TL,TR);
  }
  return {legL, legR, hipPts};
}
function addMembers(nodes, members, lnodes, nLegs, nsec, patterns) {
  for (let lv=0; lv<nsec; lv++) {
    for (let j=0; j<nLegs; j++)
      members.push({ni:lnodes[lv][j], nj:lnodes[lv+1][j], type:'leg', sec:lv});

    const pat = patterns ? (patterns[lv] || 'X') : 'X';
    for (let f=0; f<nLegs; f++) {
      const a=f, b=(f+1)%nLegs;
      if (pat === 'Z') {
        // Diagonal simple alternando dirección por tramo
        if (lv % 2 === 0)
          members.push({ni:lnodes[lv][a],   nj:lnodes[lv+1][b], type:'diagonal', sec:lv});
        else
          members.push({ni:lnodes[lv+1][a], nj:lnodes[lv][b],   type:'diagonal', sec:lv});
      } else if (pat === 'K') {
        // K-brace: diagonales hacia punto medio del horizontal superior
        const nA = nodes[lnodes[lv+1][a]], nB = nodes[lnodes[lv+1][b]];
        const midId = addNode(nodes, (nA.x+nB.x)/2, (nA.y+nB.y)/2, (nA.z+nB.z)/2);
        members.push({ni:lnodes[lv][a], nj:midId, type:'diagonal', sec:lv});
        members.push({ni:lnodes[lv][b], nj:midId, type:'diagonal', sec:lv});
        members.push({ni:midId, nj:lnodes[lv+1][a], type:'diagonal', sec:lv});
        members.push({ni:midId, nj:lnodes[lv+1][b], type:'diagonal', sec:lv});
      } else {
        // X-brace (default)
        members.push({ni:lnodes[lv][a],   nj:lnodes[lv+1][b], type:'diagonal', sec:lv});
        members.push({ni:lnodes[lv+1][a], nj:lnodes[lv][b],   type:'diagonal', sec:lv});
      }
    }
    for (let f=0; f<nLegs; f++)
      members.push({ni:lnodes[lv+1][f], nj:lnodes[lv+1][(f+1)%nLegs], type:'horizontal', sec:lv});
  }
  for (let f=0; f<nLegs; f++)
    members.push({ni:lnodes[0][f], nj:lnodes[0][(f+1)%nLegs], type:'horizontal', sec:0});
}

// ══════════════════════════════════════════════════════════════════
//  THREE.JS
// ══════════════════════════════════════════════════════════════════
const wrap = document.getElementById('viewer-wrap');
const scene = new THREE.Scene();
scene.background = new THREE.Color(0x0A1628);
scene.fog = new THREE.FogExp2(0x0A1628, 0.004);

const camera = new THREE.PerspectiveCamera(45, 1, 0.1, 2000);
camera.up.set(0, 0, 1);   // Z-up: la altura de la torre va en el eje Z
camera.position.set(50, 50, 25);

const renderer = new THREE.WebGLRenderer({antialias:true});
renderer.setPixelRatio(devicePixelRatio);
renderer.autoClear = false;
wrap.appendChild(renderer.domElement);

// Grids — rebuilt by buildGrid()
let primaryGrid = null;
let secondaryGrid = null;
let _towerData = null;   // datos del último renderTower (nodes, members)
let _hlMesh    = null;   // LineSegments del elemento seleccionado
scene.add(new THREE.AmbientLight(0xffffff, 0.6));
const sun = new THREE.DirectionalLight(0xffffff, 0.5);
sun.position.set(40,40,80);
scene.add(sun);

const controls = new THREE.OrbitControls(camera, renderer.domElement);
controls.enableDamping = true;
controls.dampingFactor = 0.07;
controls.target.set(0,0,15);
controls.update();

controls.saveState();

// ── Member click selection ─────────────────────────────────────────────────
const _raycaster = new THREE.Raycaster();
_raycaster.params.Line.threshold = 0.02;
let _mouseDownPos = {x:0, y:0};
// OrbitControls (three r128) usa Pointer Events y hace preventDefault en pointerdown,
// lo que suprime los mousedown/mouseup sintéticos sobre el canvas — por eso se usan pointer events aquí.
renderer.domElement.addEventListener('pointerdown', e => { _mouseDownPos = {x:e.clientX, y:e.clientY}; });
renderer.domElement.addEventListener('pointerup',   e => {
  if (!_towerData) { showToast('Genere la torre antes de seleccionar elementos.'); return; }
  if (Math.abs(e.clientX - _mouseDownPos.x) > 5 || Math.abs(e.clientY - _mouseDownPos.y) > 5) return;
  try { _pickMember(e); } catch (err) { showToast('Error selección: ' + err.message); }
});

function toggleVistaMenu(e) {
  e.stopPropagation();
  const menu = document.getElementById('vista-menu');
  const btn  = document.getElementById('vista-btn');
  const open = menu.classList.toggle('open');
  btn.classList.toggle('active', open);
}
document.addEventListener('click', () => {
  document.getElementById('vista-menu').classList.remove('open');
  document.getElementById('vista-btn').classList.remove('active');
});

function towerBounds() {
  const box = new THREE.Box3().setFromObject(towerGroup);
  if (box.isEmpty()) return null;
  return { center: box.getCenter(new THREE.Vector3()), size: box.getSize(new THREE.Vector3()) };
}

function setCamFrente() {
  controls.autoRotate = false;
  document.getElementById('vbtn-orbit').classList.remove('active');
  const b = towerBounds();
  if (!b) return;
  const dist = Math.max(b.size.x, b.size.z) * 1.5 + 10;
  camera.position.set(b.center.x, b.center.y + dist, b.center.z);
  controls.target.copy(b.center);
  controls.update();
}
function toggleAutoOrbit() {
  controls.autoRotate = !controls.autoRotate;
  controls.autoRotateSpeed = 2.0;
  document.getElementById('vbtn-orbit').classList.toggle('active', controls.autoRotate);
}


let _lastMid = 0;
document.addEventListener('auxclick', e => {
  if (e.button !== 1) return;
  const now = Date.now();
  if (now - _lastMid < 300) { controls.reset(); _lastMid = 0; }
  else { _lastMid = now; }
});

// ── Axis indicator — renderer dedicado ────────────────────────
const axisCanvas = document.createElement('canvas');
const AX_S = 110;
axisCanvas.width  = AX_S * devicePixelRatio;
axisCanvas.height = AX_S * devicePixelRatio;
axisCanvas.style.cssText = `position:absolute;bottom:10px;right:10px;width:${AX_S}px;height:${AX_S}px;pointer-events:none;z-index:5;`;
wrap.appendChild(axisCanvas);

const axisRenderer = new THREE.WebGLRenderer({canvas: axisCanvas, alpha: true, antialias: true});
axisRenderer.setPixelRatio(devicePixelRatio);
axisRenderer.setSize(AX_S, AX_S);

const axisScene = new THREE.Scene();
axisScene.add(new THREE.AxesHelper(1.2));

const axisLabelWrap = document.createElement('div');
axisLabelWrap.style.cssText = `position:absolute;bottom:10px;right:10px;width:${AX_S}px;height:${AX_S}px;pointer-events:none;z-index:6;`;
wrap.appendChild(axisLabelWrap);

function makeAxisLabelEl(txt, color) {
  const el = document.createElement('div');
  el.textContent = txt;
  el.style.cssText = `position:absolute;transform:translate(-50%,-50%);color:${color};font:bold 13px Arial,sans-serif;text-shadow:0 0 3px #000,0 0 3px #000;`;
  axisLabelWrap.appendChild(el);
  return el;
}
const axisLabelEls = {
  x: { el: makeAxisLabelEl('X', '#ff5555'), pos: new THREE.Vector3(1.45, 0, 0) },
  y: { el: makeAxisLabelEl('Y', '#55dd55'), pos: new THREE.Vector3(0, 1.45, 0) },
  z: { el: makeAxisLabelEl('Z', '#5599ff'), pos: new THREE.Vector3(0, 0, 1.45) },
};

const axisCamera = new THREE.PerspectiveCamera(50, 1, 0.01, 10);
axisCamera.position.set(0, 0, 3.2);
const _axisDir = new THREE.Vector3();
const _axisProj = new THREE.Vector3();

function updateAxisLabels() {
  for (const key in axisLabelEls) {
    const { el, pos } = axisLabelEls[key];
    _axisProj.copy(pos).project(axisCamera);
    el.style.left = ((_axisProj.x * 0.5 + 0.5) * AX_S) + 'px';
    el.style.top  = ((1 - (_axisProj.y * 0.5 + 0.5)) * AX_S) + 'px';
  }
}

const towerGroup = new THREE.Group();
scene.add(towerGroup);

const C_LEG       = 0xFF2233;  // rojo fosforescente
const C_RING      = 0xCCEEFF;  // blanco frío fosforescente
const C_GUY       = 0xFFCC00;  // ámbar brillante
const C_SECONDARY = 0x5A7A95;  // azul grisáceo — diagonales/horizontales secundarias (bracing auxiliar)
const C_PLANBRACE = 0xB85FD6;  // magenta — plan bracing (diafragma en planta)
const C_HIPBRACE_H = 0xFF66FF; // magenta brillante — hip bracing horizontal
const C_HIPBRACE_D = 0xFFA500; // naranja — hip bracing diagonal

function renderTower(data) {
  towerGroup.children.slice().forEach(c => {
    c.geometry && c.geometry.dispose();
    c.material && c.material.dispose();
    towerGroup.remove(c);
  });
  if (_hlMesh) { _hlMesh.geometry.dispose(); _hlMesh.material.dispose(); scene.remove(_hlMesh); _hlMesh = null; }
  closeMemberInfo();

  // Agrupa piernas/diagonales por (tipo, paridad de tramo); horizontales y guys por tipo
  // Diagonales/horizontales secundarias (bracing auxiliar de los patrones K) van en su propio batch para colorearlas distinto
  const batches = {};
  data.members.forEach((m, i) => {
    m._idx = i;
    const alternate = (m.type==='leg' || m.type==='diagonal' || m.type==='horizontal') && m.sec!=null;
    const isSecondary = (m.type==='diagonal' || m.type==='horizontal') && m.principal===false;
    const key = alternate ? `${m.type}_${m.sec%2}${isSecondary?'_s':''}`
      : (m.type==='hipbrace' ? `hipbrace_${m.isDiag?'d':'h'}` : m.type);
    (batches[key] = batches[key]||[]).push(m);
  });

  Object.entries(batches).forEach(([key, list]) => {
    const parts = key.split('_');
    const type = parts[0];
    const parity = key.includes('_') ? +parts[1] : null;
    const isSecondary = key.endsWith('_s');
    const pts = [];
    list.forEach(m => {
      const ni=data.nodes[m.ni], nj=data.nodes[m.nj];
      pts.push(ni.x, ni.y, ni.z,  nj.x, nj.y, nj.z);
    });
    const geo = new THREE.BufferGeometry();
    geo.setAttribute('position', new THREE.Float32BufferAttribute(pts, 3));

    let color, opacity=1, transparent=false;
    if (isSecondary) {
      color = C_SECONDARY; opacity = 0.55; transparent = true;
    } else if (type==='leg') {
      color = parity===0 ? C_LEG : C_RING;
    } else if (type==='diagonal') {
      color = parity===0 ? C_LEG : C_RING; opacity=0.85; transparent=true;
    } else if (type==='horizontal') {
      color = parity===0 ? C_LEG : C_RING;
    } else if (type==='guy') {
      color=C_GUY; opacity=0.6; transparent=true;
    } else if (type==='planbrace') {
      color=C_PLANBRACE; opacity=0.85; transparent=true;
    } else if (type==='hipbrace') {
      color = key.endsWith('_d') ? C_HIPBRACE_D : C_HIPBRACE_H; opacity=0.85; transparent=true;
    } else {
      color=0xaaaaaa;
    }

    const ls = new THREE.LineSegments(geo, new THREE.LineBasicMaterial({color, opacity, transparent}));
    ls.userData.members = list;
    towerGroup.add(ls);
  });

  // Nodos de intersección (puntos auxiliares de los patrones de celosía)
  const sn = data.structNodes ?? data.nodes.length;
  const ptInt = [];
  data.nodes.forEach((n, i) => { if (i >= sn) ptInt.push(n.x, n.y, n.z); });
  if (ptInt.length) {
    const g = new THREE.BufferGeometry();
    g.setAttribute('position', new THREE.Float32BufferAttribute(ptInt, 3));
    towerGroup.add(new THREE.Points(g, new THREE.PointsMaterial({color:0x445566, size:0.10, sizeAttenuation:true})));
  }

  const maxH = Math.max(...data.nodes.map(n=>n.z));
  controls.target.set(0, 0, maxH/2);
  document.getElementById('status').textContent =
    `Torre generada  |  Nodos: ${data.nodes.length}  |  Elementos: ${data.members.length}  |  Altura: ${maxH.toFixed(1)} m`;
  _towerData = data;
}

// ── Dual grid ─────────────────────────────────────────────────────────
function buildGrid(totalSize, primaryDivs, thickness, subDivs) {
  // Remove old grids
  [primaryGrid, secondaryGrid].forEach(g => {
    if (!g) return;
    g.geometry && g.geometry.dispose();
    if (g.material) { if (Array.isArray(g.material)) g.material.forEach(m=>m.dispose()); else g.material.dispose(); }
    scene.remove(g);
  });

  // Secondary grid — thin, subdivided (regular GridHelper for performance)
  const totalDivs = primaryDivs * subDivs;
  secondaryGrid = new THREE.GridHelper(totalSize, totalDivs, 0x1E3A5F, 0x1E3A5F);
  secondaryGrid.rotation.x = -Math.PI / 2;   // Z-up: plano XY en vez de XZ
  secondaryGrid.material.opacity = 0.45;
  secondaryGrid.material.transparent = true;
  scene.add(secondaryGrid);

  // Primary grid — thick lines via LineSegments2
  const half = totalSize / 2;
  const step = totalSize / primaryDivs;
  const positions = [];
  for (let i = 0; i <= primaryDivs; i++) {
    const v = -half + i * step;
    positions.push(-half, v, 0,  half, v, 0);   // lines along X
    positions.push(v, -half, 0,  v, half, 0);    // lines along Y
  }
  const geo = new THREE.LineSegmentsGeometry();
  geo.setPositions(positions);
  const mat = new THREE.LineMaterial({
    color: 0x1E6FBE,
    linewidth: thickness,
    opacity: 0.9,
    transparent: true,
    resolution: new THREE.Vector2(wrap.clientWidth || 800, wrap.clientHeight || 600),
  });
  primaryGrid = new THREE.LineSegments2(geo, mat);
  scene.add(primaryGrid);
}

function resizeRenderer() {
  const w=wrap.clientWidth, h=wrap.clientHeight;
  camera.aspect = w/h;
  camera.updateProjectionMatrix();
  renderer.setSize(w, h, false);
  if (primaryGrid) primaryGrid.material.resolution.set(w, h);
}

(function animate() {
  requestAnimationFrame(animate);
  controls.update();
  const w=wrap.clientWidth, h=wrap.clientHeight;
  renderer.setViewport(0,0,w,h);
  renderer.render(scene,camera);
  camera.getWorldDirection(_axisDir);
  axisCamera.position.copy(_axisDir).multiplyScalar(-3.2);
  axisCamera.up.copy(camera.up);
  axisCamera.lookAt(0,0,0);
  axisRenderer.render(axisScene, axisCamera);
  updateAxisLabels();
})();

new ResizeObserver(resizeRenderer).observe(wrap);
resizeRenderer();

// ══════════════════════════════════════════════════════════════════
//  UI LOGIC
// ══════════════════════════════════════════════════════════════════
// ── Estado del proyecto ────────────────────────────────────────
let projectGenerated = false;
let secData = [];  // [{h, diag, perfil}] — una entrada por tramo
let guyHeights = [];  // altura (m) de cada nivel de retenidas — solo Arriostrada
let currentFileHandle = null;  // FileSystemFileHandle activo (File System Access API)

function getConfig() {
  const nInc = Math.max(0, +document.getElementById('nInc').value || 0);
  const nStr = Math.max(0, +document.getElementById('nStr').value || 0);
  return {
    type:      document.getElementById('ttype').value,
    baseW:     +document.getElementById('baseW').value  || 4,
    topW:      +document.getElementById('topW').value   || 2,
    height:    +document.getElementById('height').value || 30,
    nInc, nStr,
    nsec:      nInc + nStr || 1,
    shaftW:    +document.getElementById('shaftW').value || 1,
    guyLevels: +document.getElementById('guyLevels').value || 3,
    anchorR:   +document.getElementById('anchorR').value   || 15,
    guyProfile:     document.getElementById('guyProfile').value,
    assetName:      document.getElementById('assetName').value,
    siteName:       document.getElementById('siteName').value,
    pais:           document.getElementById('pais').value,
    ingResponsable: document.getElementById('ingResponsable').value,
    fechaCreacion:  document.getElementById('fechaCreacion').value,
    secData:        secData.slice(),
  };
}

function refresh() {
  if (projectGenerated) renderTower(generateTower(getConfig()));
}

function onTypeChange() {
  const v = document.getElementById('ttype').value;
  document.getElementById('guyed-params').classList.toggle('show', v === 'guyed');
  refresh();
}

function onSecChange() {
  const n = (+document.getElementById('nInc').value || 0)
           + (+document.getElementById('nStr').value || 0);
  buildSectionRows(n);
  refresh();
}

// ── Setup panel: cambio de tipo ────────────────────────────────
function onSetupTipoChange() {
  const v = document.getElementById('s-tipo').value;
  const hide = (id, on) => document.getElementById(id).style.display = on ? '' : 'none';
  hide('s-row-base',  v !== 'guyed');
  hide('s-row-top',   v !== 'guyed' && v !== 'monopole' ? true : v === 'monopole');
  hide('s-row-ninc',  v !== 'monopole' && v !== 'guyed');
  hide('s-row-guyApertura', v === 'guyed');
  hide('s-row-guyLevels',   v === 'guyed');
  hide('s-row-guyHeights',  v === 'guyed');
  hide('s-row-guyPivot',    v === 'guyed');
  document.getElementById('s-nstr-lbl').textContent = v === 'guyed' ? 'NÚMERO DE TRAMOS' : 'TRAMOS RECTOS';
  if (v === 'guyed') buildGuyHeightsList();
}

// ── Lista dinámica de alturas de retenidas (flyout Nueva Torre) ────
function buildGuyHeightsList() {
  const n = Math.max(1, +document.getElementById('s-guyLevels')?.value || 3);
  const h = +document.getElementById('s-height')?.value || 30;
  const prev = guyHeights.slice();
  guyHeights = Array.from({length:n}, (_,i) => prev[i] ?? +(h*(i+1)/(n+1)).toFixed(1));
  const list = document.getElementById('s-guyHeights-list');
  if (!list) return;
  list.innerHTML = guyHeights.map((val,i) => `
    <div style="display:flex;align-items:center;gap:6px;">
      <span class="tf-lbl" style="width:62px;flex-shrink:0;">Nivel ${i+1}</span>
      <input class="tf-input" type="number" min="0" max="${h}" step="0.5" value="${val}"
        oninput="guyHeights[${i}] = +this.value || 0">
    </div>`).join('');
}

// ── Generar Torre desde el setup ───────────────────────────────
function generateTowerFromSetup() {
  // Mapear tipo de estructura a ttype
  const tipoMap = {
    triangular: 'triangular', square: 'square',
    guyed: 'guyed', monopole: 'monopole'
  };
  const tipo = document.getElementById('s-tipo').value;

  // Sincronizar valores al panel de información
  const syncVal = (dst, src) => {
    const d = document.getElementById(dst), s = document.getElementById(src);
    if (d && s) d.value = s.value;
  };
  document.getElementById('ttype').value = tipo;
  syncVal('height', 's-height');
  syncVal('baseW',  's-baseW');
  syncVal('topW',   's-topW');
  syncVal('nInc',   's-nInc');
  syncVal('nStr',   's-nStr');
  document.getElementById('assetName').value      = document.getElementById('s-asset').value;
  document.getElementById('siteName').value       = document.getElementById('s-site').value;
  document.getElementById('pais').value           = document.getElementById('s-pais').value;
  document.getElementById('ingResponsable').value = document.getElementById('s-ing').value;
  document.getElementById('fechaCreacion').value  = document.getElementById('s-fecha').value;

  onTypeChange();
  onSecChange();

  // Cerrar flyout, mostrar info panel
  projectGenerated = true;
  closeTorreFlyout();
  document.getElementById('rpanel').classList.add('visible');
  document.getElementById('rpanel-info').classList.add('visible');

  renderTower(generateTower(getConfig()));
  document.getElementById('status').textContent =
    `Torre generada · ${document.getElementById('s-asset').value || '—'} · ${document.getElementById('s-site').value || '—'}`;
}

// ── Flyout Torre ───────────────────────────────────────────────
function closeTorreFlyout() {
  document.getElementById('torre-flyout').classList.remove('open');
}

function switchToTorre() {
  document.querySelectorAll('.side-btn').forEach(x => x.classList.remove('active'));
  document.getElementById('torre-btn').classList.add('active');
  if (projectGenerated) {
    // Ya hay torre — mostrar info panel, cerrar flyout
    closeTorreFlyout();
    document.getElementById('rpanel').classList.add('visible');
  } else {
    // Sin torre — abrir flyout, ocultar rpanel
    document.getElementById('rpanel').classList.remove('visible');
    const fly = document.getElementById('torre-flyout');
    fly.classList.toggle('open');
  }
}

// ── Nuevo Proyecto ─────────────────────────────────────────────
function nuevoProyecto() {
  document.getElementById('home-menu').classList.remove('open');
  ['s-asset','s-site','s-pais','s-ing'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('s-fecha').value = new Date().toISOString().slice(0,10);
  document.getElementById('s-tipo').value   = 'triangular';
  document.getElementById('s-height').value = '30';
  document.getElementById('s-baseW').value  = '4';
  document.getElementById('s-topW').value   = '2';
  document.getElementById('s-nInc').value   = '6';
  document.getElementById('s-nStr').value   = '2';
  onSetupTipoChange();
  towerGroup.children.slice().forEach(c => {
    c.geometry && c.geometry.dispose();
    c.material && c.material.dispose();
    towerGroup.remove(c);
  });
  projectGenerated = false;
  document.getElementById('rpanel').classList.remove('visible');
  document.getElementById('rpanel-info').classList.remove('visible');
  document.querySelectorAll('.side-btn').forEach(x => x.classList.remove('active'));
  document.getElementById('torre-btn').classList.add('active');
  document.getElementById('torre-flyout').classList.add('open');
}

// Tab click
document.querySelectorAll('.tab').forEach(t =>
  t.addEventListener('click', () => {
    document.querySelectorAll('.tab').forEach(x => x.classList.remove('active'));
    t.classList.add('active');
  })
);

// Sidebar: todos excepto Home y Torre (Torre tiene su propia función)
document.querySelectorAll('.side-btn:not(#home-btn):not(#torre-btn)').forEach(b =>
  b.addEventListener('click', () => {
    document.querySelectorAll('.side-btn').forEach(x => x.classList.remove('active'));
    b.classList.add('active');
    // Ocultar panel si no es Torre
    document.getElementById('rpanel').classList.remove('visible');
  })
);

// ── Home menu ──────────────────────────────────────────────────
function toggleHomeMenu(e) {
  if (e) e.stopPropagation();
  document.getElementById('home-menu').classList.toggle('open');
}
document.addEventListener('click', () => {
  document.getElementById('home-menu').classList.remove('open');
  document.getElementById('torre-flyout').classList.remove('open');
  document.getElementById('export-menu')?.classList.remove('open');
});
document.getElementById('home-menu').addEventListener('click', e => e.stopPropagation());
document.getElementById('torre-flyout').addEventListener('click', e => e.stopPropagation());

function toggleExportDD(e) {
  e.stopPropagation();
  document.getElementById('export-menu').classList.toggle('open');
}

// ── Exportar STAAD.Pro ─────────────────────────────────────────
// Punto más cercano entre dos segmentos 3D (Ericson, "Real-Time Collision Detection")
function _closestPtSegSeg(p1, p2, p3, p4) {
  const d1 = {x:p2.x-p1.x, y:p2.y-p1.y, z:p2.z-p1.z};
  const d2 = {x:p4.x-p3.x, y:p4.y-p3.y, z:p4.z-p3.z};
  const r  = {x:p1.x-p3.x, y:p1.y-p3.y, z:p1.z-p3.z};
  const dot = (a,b) => a.x*b.x + a.y*b.y + a.z*b.z;
  const EPS = 1e-12;
  const a = dot(d1,d1), e = dot(d2,d2), f = dot(d2,r);
  let tA, tB;
  if (a <= EPS && e <= EPS) { tA = 0; tB = 0; }
  else if (a <= EPS) { tA = 0; tB = Math.min(1, Math.max(0, f/e)); }
  else {
    const c = dot(d1,r);
    if (e <= EPS) { tB = 0; tA = Math.min(1, Math.max(0, -c/a)); }
    else {
      const b = dot(d1,d2);
      const denom = a*e - b*b;
      tA = denom !== 0 ? Math.min(1, Math.max(0, (b*f - c*e)/denom)) : 0;
      tB = (b*tA + f) / e;
      if (tB < 0) { tB = 0; tA = Math.min(1, Math.max(0, -c/a)); }
      else if (tB > 1) { tB = 1; tA = Math.min(1, Math.max(0, (b-c)/a)); }
    }
  }
  const c1 = {x:p1.x+d1.x*tA, y:p1.y+d1.y*tA, z:p1.z+d1.z*tA};
  const c2 = {x:p3.x+d2.x*tB, y:p3.y+d2.y*tB, z:p3.z+d2.z*tB};
  const dd = {x:c1.x-c2.x, y:c1.y-c2.y, z:c1.z-c2.z};
  return {tA, tB, c1, c2, distSq: dot(dd,dd)};
}

// Detecta diagonales que se cruzan dentro de la misma sección (ej. patrón X) y las
// divide en 4 segmentos agregando el nodo de intersección — solo para el archivo STAAD.
function _splitCrossingDiagonals(nodes, members) {
  const outNodes   = nodes.map(n => ({...n}));
  const outMembers = [];
  const removed    = new Set();
  const diagIdxs    = [];
  members.forEach((m, i) => { if (m.type === 'diagonal') diagIdxs.push(i); });
  const TOL_SQ   = 1e-6;   // ~1mm
  const EDGE_EPS = 1e-4;
  for (let a = 0; a < diagIdxs.length; a++) {
    const ia = diagIdxs[a];
    if (removed.has(ia)) continue;
    const ma = members[ia];
    for (let b = a+1; b < diagIdxs.length; b++) {
      const ib = diagIdxs[b];
      if (removed.has(ib)) continue;
      const mb = members[ib];
      if (ma.sec !== mb.sec) continue;
      if (ma.ni===mb.ni || ma.ni===mb.nj || ma.nj===mb.ni || ma.nj===mb.nj) continue;
      const r = _closestPtSegSeg(outNodes[ma.ni], outNodes[ma.nj], outNodes[mb.ni], outNodes[mb.nj]);
      if (r.distSq > TOL_SQ) continue;
      if (r.tA < EDGE_EPS || r.tA > 1-EDGE_EPS || r.tB < EDGE_EPS || r.tB > 1-EDGE_EPS) continue;
      const ip = {x:(r.c1.x+r.c2.x)/2, y:(r.c1.y+r.c2.y)/2, z:(r.c1.z+r.c2.z)/2};
      const newIdx = outNodes.length;
      outNodes.push(ip);
      outMembers.push({ni:ma.ni, nj:newIdx, type:'diagonal', sec:ma.sec});
      outMembers.push({ni:newIdx, nj:ma.nj, type:'diagonal', sec:ma.sec});
      outMembers.push({ni:mb.ni, nj:newIdx, type:'diagonal', sec:mb.sec});
      outMembers.push({ni:newIdx, nj:mb.nj, type:'diagonal', sec:mb.sec});
      removed.add(ia); removed.add(ib);
      break;
    }
  }
  members.forEach((m, i) => { if (!removed.has(i)) outMembers.push(m); });
  return { nodes: outNodes, members: outMembers };
}

// Elimina nodos con coordenadas repetidas — conserva el de ID (índice) menor, reasigna
// las barras que apuntaban al duplicado, y renumera todo de forma consecutiva (1..n).
function _dedupeNodes(nodes, members) {
  const TOL = 1e-4; // ~0.1mm — tolerancia para considerar dos nodos coincidentes
  const key = n => `${Math.round(n.x/TOL)}_${Math.round(n.y/TOL)}_${Math.round(n.z/TOL)}`;
  const firstIdxByKey = new Map();
  const remap = new Array(nodes.length);
  nodes.forEach((n, i) => {
    const k = key(n);
    if (!firstIdxByKey.has(k)) { firstIdxByKey.set(k, i); }
    remap[i] = firstIdxByKey.get(k);   // índice canónico (el menor) para esta coordenada
  });
  const keepIdxs = [...new Set(remap)].sort((a,b) => a-b);
  const oldToNew = new Map(keepIdxs.map((oldIdx, newIdx) => [oldIdx, newIdx]));
  const outNodes = keepIdxs.map(i => nodes[i]);
  const outMembers = members
    .map(m => ({...m, ni: oldToNew.get(remap[m.ni]), nj: oldToNew.get(remap[m.nj])}))
    .filter(m => m.ni !== m.nj);   // descarta barras que quedaron degeneradas (longitud 0)
  return { nodes: outNodes, members: outMembers };
}

// Convierte una fecha ISO (yyyy-mm-dd, del <input type="date">) al formato que exige
// STAAD.Pro en START JOB INFORMATION: DD-Mon-YY (ej. 17-Jun-26).
function _staadDate(iso) {
  if (!iso) return '';
  const months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
  const [y, m, d] = iso.split('-');
  if (!y || !m || !d) return iso;
  return `${d}-${months[+m - 1]}-${y.slice(-2)}`;
}

function exportSTAAD() {
  document.getElementById('export-menu').classList.remove('open');
  if (!projectGenerated) {
    const msg = '⚠  Genere una torre antes de exportar.';
    const s = document.getElementById('status');
    if (s) s.textContent = msg;
    showToast(msg);
    return;
  }

  const cfg  = getConfig();
  const tower = generateTower(cfg);
  const split = _splitCrossingDiagonals(tower.nodes, tower.members);
  const {nodes, members} = _dedupeNodes(split.nodes, split.members);
  const title = (cfg.assetName || cfg.siteName || 'TORRE').replace(/\s+/g,'_');

  // Unidades activas en TSA
  const isIMP = document.getElementById('imp-btn')?.classList.contains('active');
  // TSA almacena geometría siempre en metros; IMP solo cambia presentación en UI
  // → exportamos en metros con unidad de fuerza según selección
  const staadUnit = isIMP ? 'UNIT METER KIP' : 'UNIT METER KG';
  // Propiedades del acero según unidad de fuerza
  // MKS (kgf): E = 2.039e10 kgf/m², densidad = 7850 kgf/m³
  // IMP (kip):  E = 4.176e6 kip/ft² → en metros: 4.494e7 kip/m², densidad = 0.490 kip/ft³ → 17.29 kip/m³
  const steelE    = isIMP ? '4.494E+07' : '2.039E+10';
  const steelDens = isIMP ? '1.729E+01' : '7.850E+03';

  // Coordinate mapping
  // TSA addNode stores {x:-x_phys, y:-y_phys, z:z_phys}
  // STAAD: X horizontal, Y vertical (altura), Z horizontal
  // → STAAD_X = -node.x  (= x_phys)
  //   STAAD_Y =  node.z  (= z_phys = altura)
  //   STAAD_Z =  node.y  (= -y_phys, invertido por solicitud del usuario)
  const sx = i => (-nodes[i].x).toFixed(4);
  const sy = i =>  nodes[i].z .toFixed(4);
  const sz = i =>  nodes[i].y .toFixed(4);


  let out = '';
  out += `STAAD SPACE ${cfg.assetName||''}-${cfg.siteName||''}\n`;
  out += `START JOB INFORMATION\n`;
  out += `ENGINEER DATE ${_staadDate(cfg.fechaCreacion)}\n`;
  out += `ENGINEER NAME ${cfg.ingResponsable||''}\n`;
  out += `END JOB INFORMATION\n`;
  out += `INPUT WIDTH 79\n`;
  out += `${staadUnit}\n`;

  out += `JOINT COORDINATES\n`;
  nodes.forEach((_, i) => { out += `${i+1} ${sx(i)} ${sy(i)} ${sz(i)}\n`; });

  out += `MEMBER INCIDENCES\n`;
  members.forEach((m, i) => { out += `${i+1} ${m.ni+1} ${m.nj+1}\n`; });

  out += `FINISH\n`;

  const blob = new Blob([out], { type: 'text/plain' });
  const url  = URL.createObjectURL(blob);
  const a    = document.createElement('a');
  a.href = url; a.download = `${title}.std`; a.click();
  URL.revokeObjectURL(url);
}

// ── Guardar proyecto ───────────────────────────────────────────
// ── Guardar proyecto ───────────────────────────────────────────
async function saveProject() {
  document.getElementById('home-menu').classList.remove('open');
  if (currentFileHandle) {
    try {
      await _writeHandle(currentFileHandle);
      document.getElementById('status').textContent = `Guardado: ${currentFileHandle.name}`;
      return;
    } catch { /* handle revocado — pedir ruta nueva */ }
  }
  await saveProjectAs();
}

async function saveProjectAs() {
  document.getElementById('home-menu').classList.remove('open');
  if (window.showSaveFilePicker) {
    try {
      const handle = await window.showSaveFilePicker({
        suggestedName: currentFileHandle ? currentFileHandle.name : 'proyecto_tsa.TSA',
        types: [{ description: 'TSA Project', accept: { 'application/json': ['.TSA', '.tsa'] } }]
      });
      await _writeHandle(handle);
      currentFileHandle = handle;
      document.getElementById('status').textContent = `Guardado: ${handle.name}`;
    } catch (e) {
      if (e.name !== 'AbortError')
        document.getElementById('status').textContent = 'Error al guardar.';
    }
  } else {
    // Fallback navegadores sin File System Access API
    const blob = new Blob([_projectJSON()], {type: 'application/json'});
    const url  = URL.createObjectURL(blob);
    const a    = document.createElement('a');
    a.href = url; a.download = 'proyecto_tsa.TSA'; a.click();
    URL.revokeObjectURL(url);
    document.getElementById('status').textContent = 'Proyecto guardado.';
  }
}

function _projectJSON() { return JSON.stringify(getConfig(), null, 2); }

async function _writeHandle(handle) {
  const writable = await handle.createWritable();
  await writable.write(_projectJSON());
  await writable.close();
}

// ── Abrir proyecto ─────────────────────────────────────────────
async function openProject() {
  document.getElementById('home-menu').classList.remove('open');
  if (window.showOpenFilePicker) {
    try {
      const [handle] = await window.showOpenFilePicker({
        types: [{ description: 'TSA Project', accept: { 'application/json': ['.TSA', '.tsa', '.json'] } }]
      });
      const file = await handle.getFile();
      loadProjectData(JSON.parse(await file.text()), file.name);
      currentFileHandle = handle;
    } catch (e) {
      if (e.name !== 'AbortError')
        document.getElementById('status').textContent = 'Error al abrir.';
    }
  } else {
    document.getElementById('file-input').value = '';
    document.getElementById('file-input').click();
  }
}

function loadProject(input) {
  const file = input.files[0];
  if (!file) return;
  const reader = new FileReader();
  reader.onload = e => {
    try {
      loadProjectData(JSON.parse(e.target.result), file.name);
      currentFileHandle = null;
    } catch {
      document.getElementById('status').textContent = 'Error al leer el archivo.';
    }
  };
  reader.readAsText(file);
}

function loadProjectData(cfg, filename) {
  try {
    const set = (id, val) => { const el = document.getElementById(id); if (el && val !== undefined) el.value = val; };
    set('ttype',         cfg.type);
    set('baseW',         cfg.baseW);
    set('topW',          cfg.topW);
    set('height',        cfg.height);
    set('nInc',          cfg.nInc);
    set('nStr',          cfg.nStr);
    set('shaftW',        cfg.shaftW);
    set('guyLevels',     cfg.guyLevels);
    set('anchorR',       cfg.anchorR);
    set('guyProfile',    cfg.guyProfile);
    set('assetName',      cfg.assetName);
    set('siteName',       cfg.siteName);
    set('pais',           cfg.pais);
    set('ingResponsable', cfg.ingResponsable);
    set('fechaCreacion',  cfg.fechaCreacion);
    projectGenerated = true;
    const rsetup = document.getElementById('rpanel-setup');
    if (rsetup) rsetup.style.display = 'none';
    document.getElementById('rpanel-info').classList.add('visible');
    document.getElementById('rpanel').classList.add('visible');
    document.querySelectorAll('.side-btn').forEach(x => x.classList.remove('active'));
    document.getElementById('torre-btn').classList.add('active');
    onTypeChange();
    onSecChange();
    if (Array.isArray(cfg.secData)) {
      cfg.secData.forEach((s, i) => { if (s) secData[i] = s; });
      buildSectionRows(cfg.nInc + cfg.nStr);
      refresh();
    }
    document.getElementById('status').textContent = `Proyecto cargado: ${filename}`;
  } catch {
    document.getElementById('status').textContent = 'Error al leer el archivo.';
  }
}

// MKS/IMP toggle
function setUnit(btn, unit) {
  ['mks-btn','imp-btn'].forEach(id => document.getElementById(id).classList.remove('active'));
  btn.classList.add('active');
}

// ── Sección read-only + modal ──────────────────────────────────

let modalTemp = {};
let modalIdx  = -1;

function buildSectionRows(n) {
  if (n <= 0) { document.getElementById('sec-container').innerHTML = ''; return; }

  const cfg  = getConfig();
  const nInc = cfg.nInc;
  const h    = +(cfg.height / n).toFixed(2);

  const prev = secData.slice();
  secData = Array.from({length: n}, (_, i) => ({
    diag:    prev[i]?.diag    ?? 'X',
    bays:    prev[i]?.bays    ?? 1,
    M:       prev[i]?.M       ?? '-',
    D:       prev[i]?.D       ?? '-',
    topH:    prev[i]?.topH    ?? true,
    Htop:    prev[i]?.Htop    ?? '-',
    bayTopH: prev[i]?.bayTopH ?? false,
    Hbay:    prev[i]?.Hbay    ?? '-',
    Ds:      prev[i]?.Ds      ?? '-',   // perfil diagonales secundarias (patrones K)
    Hs:      prev[i]?.Hs      ?? '-',   // perfil horizontales secundarias (patrones K)
    planTop: prev[i]?.planTop ?? 'none',  // patrón de plan bracing — top del tramo
    PbTop:   prev[i]?.PbTop   ?? '-',
    PbTop2:  prev[i]?.PbTop2  ?? '-',      // perfil triángulos de esquina (Diaphragm 2) — solo patrón Compuesto
    planBay: prev[i]?.planBay ?? 'none',  // patrón de plan bracing — top de cada bahía
    PbBay:   prev[i]?.PbBay   ?? '-',
    PbBay2:  prev[i]?.PbBay2  ?? '-',
    hip:     prev[i]?.hip     ?? 'none',  // patrón de hip bracing — solo X-25Pct
    HhipH:   prev[i]?.HhipH   ?? '-',      // perfil horizontales del hip bracing
    HhipD:   prev[i]?.HhipD   ?? '-',      // perfil diagonales del hip bracing (opciones 3 y 4)
    HhipDia: prev[i]?.HhipDia ?? '-',      // perfil horizontal del diafragma (opciones 2 a 4)
    staggerFlip: prev[i]?.staggerFlip ?? false,   // invierte orientación de la diagonal — solo Staggered/Staggered-50Pct
  }));

  const c = document.getElementById('sec-container');
  c.innerHTML = '';
  secData.forEach((s, i) => {
    const tipo    = i < nInc ? 'INC' : 'REC';
    const tipoLbl = i < nInc ? 'Inclinado' : 'Recto';
    const card = document.createElement('div');
    card.className = 'sec-card';
    card.innerHTML = `
      <div class="sec-card-hdr">
        <span class="sec-card-title">Section ${i+1}</span>
        <span class="sec-tag" style="flex-shrink:0">${s.diag}</span>
        <span class="sec-tag" style="flex-shrink:0">x${s.bays}</span>
        <span class="sec-tag" style="flex-shrink:0">${h} m</span>
        <button class="sec-edit-btn" style="flex-shrink:0" onclick="openSecModal(${i})">✎ editar</button>
      </div>
      <div class="sec-row-detail"><span class="sec-row-code">M:</span><span class="sec-row-val">${s.M}</span></div>
      <div class="sec-row-detail"><span class="sec-row-code">D:</span><span class="sec-row-val">${s.D}</span></div>
      ${isKPattern(s.diag) ? `<div class="sec-row-detail"><span class="sec-row-code">Ds:</span><span class="sec-row-val">${s.Ds}</span></div>` : ''}
      ${isKPattern(s.diag) ? `<div class="sec-row-detail"><span class="sec-row-code">Hs:</span><span class="sec-row-val">${s.Hs}</span></div>` : ''}
      <div class="sec-row-detail"><span class="sec-row-code">Wt:</span><span class="sec-row-val">-</span></div>
      <div class="sec-row-detail"><span class="sec-row-code">H:</span><span class="sec-row-val" style="color:${(s.topH||s.bayTopH)?'#22C55E':'#3a5070'}">${[s.topH&&'TOP',s.bayTopH&&'BAH'].filter(Boolean).join('+') || '—'}</span></div>`;
    c.appendChild(card);
  });
}

const DIAG_PATTERNS = ['X','X-50Pct','X-25Pct','K','K-Rev',
  'K-50Pct','K-50Pct-Rev','K-33Pct','K-33Pct-Rev',
  'K-25Pct','K-25Pct-Rev','K-25Pct2','K-25Pct2-Rev',
  'Staggered','Staggered-50Pct'];
// true para patrones que generan celosía secundaria (K-* y X-25Pct/X-50Pct)
const isKPattern = pat => !!pat && (pat.startsWith('K') || pat==='X-25Pct' || pat==='X-50Pct');

// Réplica 2D de addFaceBracing — solo para dibujar el ícono de cada patrón.
function diagIconLines(pat, staggerUp=true) {
  const BL=[6,42], BR=[30,42], TL=[6,6], TR=[30,6];
  const lerp=(a,b,t)=>[a[0]+(b[0]-a[0])*t, a[1]+(b[1]-a[1])*t];
  const mid=(a,b)=>lerp(a,b,.5);
  const L=[];
  const h=(a,b,principal=true)=>L.push({a,b,type:'h',principal});
  const d=(a,b,principal=true)=>L.push({a,b,type:'d',principal});
  const t=0.5; // intersección aproximada (solo para el ícono)

  switch(pat) {
    case 'X':
      d(BL,TR); d(BR,TL);
      break;

    case 'X-50Pct': {
      const IX=lerp(BL,TR,t), ML=lerp(BL,TL,t), MR=lerp(BR,TR,t);
      h(ML,IX,false); h(IX,MR,false);
      d(BL,IX); d(IX,TR); d(BR,IX); d(IX,TL);
      break;
    }

    case 'X-25Pct': {
      const IX=lerp(BL,TR,t), ML=lerp(BL,TL,t), MR=lerp(BR,TR,t);
      const tL=t/2, tH=(1+t)/2;
      const ML_L=lerp(BL,TL,tL), MR_L=lerp(BR,TR,tL);
      const ML_U=lerp(BL,TL,tH), MR_U=lerp(BR,TR,tH);
      const D1L=lerp(BL,TR,tL), D2L=lerp(BR,TL,tL);
      const D1H=lerp(BL,TR,tH), D2H=lerp(BR,TL,tH);
      h(ML_L,D1L,false); h(MR_L,D2L,false);
      h(ML,IX,false); h(IX,MR,false);
      h(ML_U,D2H,false); h(MR_U,D1H,false);
      d(BL,D1L); d(D1L,IX); d(IX,D1H); d(D1H,TR);
      d(BR,D2L); d(D2L,IX); d(IX,D2H); d(D2H,TL);
      d(D1L,ML,false); d(D2L,MR,false);
      d(ML,D2H,false); d(MR,D1H,false);
      break;
    }

    case 'K': {
      const TC=mid(TL,TR);
      d(BL,TC); d(BR,TC);
      break;
    }

    case 'K-Rev': {
      const BC=mid(BL,BR);
      d(TL,BC); d(TR,BC);
      break;
    }

    case 'K-50Pct': {
      const TC=mid(TL,TR);
      const ML=lerp(BL,TL,.5), MR=lerp(BR,TR,.5);
      const PL=lerp(BL,TC,.5), PR=lerp(BR,TC,.5);
      d(BL,PL); d(PL,TC); d(BR,PR); d(PR,TC);
      h(ML,PL,false); h(MR,PR,false);
      d(PL,TL,false); d(PR,TR,false);
      break;
    }

    case 'K-50Pct-Rev': {
      const BC=mid(BL,BR);
      const ML=lerp(BL,TL,.5), MR=lerp(BR,TR,.5);
      const PL=lerp(TL,BC,.5), PR=lerp(TR,BC,.5);
      d(TL,PL); d(PL,BC); d(TR,PR); d(PR,BC);
      h(ML,PL,false); h(MR,PR,false);
      d(PL,BL,false); d(PR,BR,false);
      break;
    }

    case 'K-33Pct': {
      const TC=mid(TL,TR);
      const L1=lerp(BL,TL,1/3), R1=lerp(BR,TR,1/3);
      const L2=lerp(BL,TL,2/3), R2=lerp(BR,TR,2/3);
      const P1L=lerp(BL,TC,1/3), P1R=lerp(BR,TC,1/3);
      const P2L=lerp(BL,TC,2/3), P2R=lerp(BR,TC,2/3);
      d(BL,P1L); d(P1L,P2L); d(P2L,TC);
      d(BR,P1R); d(P1R,P2R); d(P2R,TC);
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,TL,false); d(P2R,TR,false);
      break;
    }

    case 'K-33Pct-Rev': {
      const BC=mid(BL,BR);
      const LA=lerp(BL,TL,1/3), RA=lerp(BR,TR,1/3);
      const LB=lerp(BL,TL,2/3), RB=lerp(BR,TR,2/3);
      const P1L=lerp(TL,BC,1/3), P1R=lerp(TR,BC,1/3);
      const P2L=lerp(TL,BC,2/3), P2R=lerp(TR,BC,2/3);
      d(TL,P1L); d(P1L,P2L); d(P2L,BC);
      d(TR,P1R); d(P1R,P2R); d(P2R,BC);
      h(LB,P1L,false); h(RB,P1R,false);
      h(LA,P2L,false); h(RA,P2R,false);
      d(P1L,LA,false); d(P1R,RA,false);
      d(P2L,BL,false); d(P2R,BR,false);
      break;
    }

    case 'K-25Pct': {
      const TC=mid(TL,TR);
      const L1=lerp(BL,TL,1/4), R1=lerp(BR,TR,1/4);
      const L2=lerp(BL,TL,2/4), R2=lerp(BR,TR,2/4);
      const L3=lerp(BL,TL,3/4), R3=lerp(BR,TR,3/4);
      const P1L=lerp(BL,TC,1/4), P1R=lerp(BR,TC,1/4);
      const P2L=lerp(BL,TC,2/4), P2R=lerp(BR,TC,2/4);
      const P3L=lerp(BL,TC,3/4), P3R=lerp(BR,TC,3/4);
      d(BL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,TC);
      d(BR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,TC);
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      h(L3,P3L,false); h(R3,P3R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,L3,false); d(P2R,R3,false);
      d(P3L,TL,false); d(P3R,TR,false);
      break;
    }

    case 'K-25Pct-Rev': {
      const BC=mid(BL,BR);
      const LA=lerp(BL,TL,1/4), RA=lerp(BR,TR,1/4);
      const LB=lerp(BL,TL,2/4), RB=lerp(BR,TR,2/4);
      const LC=lerp(BL,TL,3/4), RC=lerp(BR,TR,3/4);
      const P1L=lerp(TL,BC,1/4), P1R=lerp(TR,BC,1/4);
      const P2L=lerp(TL,BC,2/4), P2R=lerp(TR,BC,2/4);
      const P3L=lerp(TL,BC,3/4), P3R=lerp(TR,BC,3/4);
      d(TL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,BC);
      d(TR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,BC);
      h(LC,P1L,false); h(RC,P1R,false);
      h(LB,P2L,false); h(RB,P2R,false);
      h(LA,P3L,false); h(RA,P3R,false);
      d(P1L,LB,false); d(P1R,RB,false);
      d(P2L,LA,false); d(P2R,RA,false);
      d(P3L,BL,false); d(P3R,BR,false);
      break;
    }

    case 'K-25Pct2': {
      const TC=mid(TL,TR);
      const TLC=mid(TL,TC), TRC=mid(TR,TC);
      const L1=lerp(BL,TL,1/4), R1=lerp(BR,TR,1/4);
      const L2=lerp(BL,TL,2/4), R2=lerp(BR,TR,2/4);
      const L3=lerp(BL,TL,3/4), R3=lerp(BR,TR,3/4);
      const P1L=lerp(BL,TC,1/4), P1R=lerp(BR,TC,1/4);
      const P2L=lerp(BL,TC,2/4), P2R=lerp(BR,TC,2/4);
      const P3L=lerp(BL,TC,3/4), P3R=lerp(BR,TC,3/4);
      d(BL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,TC);
      d(BR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,TC);
      h(L1,P1L,false); h(R1,P1R,false);
      h(L2,P2L,false); h(R2,P2R,false);
      h(L3,P3L,false); h(R3,P3R,false);
      d(P1L,L2,false); d(P1R,R2,false);
      d(P2L,L3,false); d(P2R,R3,false);
      d(L3,TLC,false); d(R3,TRC,false);
      d(P3L,TLC,false); d(P3R,TRC,false);
      break;
    }

    case 'K-25Pct2-Rev': {
      const BC=mid(BL,BR);
      const BLC=mid(BL,BC), BRC=mid(BR,BC);
      const LA=lerp(BL,TL,1/4), RA=lerp(BR,TR,1/4);
      const LB=lerp(BL,TL,2/4), RB=lerp(BR,TR,2/4);
      const LC=lerp(BL,TL,3/4), RC=lerp(BR,TR,3/4);
      const P1L=lerp(TL,BC,1/4), P1R=lerp(TR,BC,1/4);
      const P2L=lerp(TL,BC,2/4), P2R=lerp(TR,BC,2/4);
      const P3L=lerp(TL,BC,3/4), P3R=lerp(TR,BC,3/4);
      d(TL,P1L); d(P1L,P2L); d(P2L,P3L); d(P3L,BC);
      d(TR,P1R); d(P1R,P2R); d(P2R,P3R); d(P3R,BC);
      h(LC,P1L,false); h(RC,P1R,false);
      h(LB,P2L,false); h(RB,P2R,false);
      h(LA,P3L,false); h(RA,P3R,false);
      d(P1L,LB,false); d(P1R,RB,false);
      d(P2L,LA,false); d(P2R,RA,false);
      d(LA,BLC,false); d(RA,BRC,false);
      d(P3L,BLC,false); d(P3R,BRC,false);
      break;
    }

    case 'Staggered':
      if (staggerUp) d(BL,TR); else d(BR,TL);
      break;

    case 'Staggered-50Pct': {
      const ML=lerp(BL,TL,.5), MR=lerp(BR,TR,.5);
      h(ML,MR);
      if (staggerUp) d(BL,TR); else d(BR,TL);
      break;
    }

    default:
      d(BL,TR); d(BR,TL);
  }
  return L;
}

function diagIconSVG(pat) {
  const COL = {h:'#22C55E', d:'#EF4444'};
  const legSvg = `<line x1="6" y1="42" x2="6" y2="6" stroke="#3B82F6" stroke-width="1.4"/>
    <line x1="30" y1="42" x2="30" y2="6" stroke="#3B82F6" stroke-width="1.4"/>`;
  const lineSvg = diagIconLines(pat).map(({a,b,type}) =>
    `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${COL[type]}" stroke-width="1.2"/>`
  ).join('');
  return `<svg viewBox="0 0 36 48" width="30" height="40">${legSvg}${lineSvg}</svg>`;
}

function buildDiagIconGrid(selected) {
  const grid = document.getElementById('diag-icon-grid');
  if (!grid) return;
  grid.innerHTML = DIAG_PATTERNS.map(p => `
    <div class="diag-icon-btn${p===selected?' selected':''}" data-pat="${p}" title="${p}">
      ${diagIconSVG(p)}
      <span>${p}</span>
    </div>`).join('');
  grid.querySelectorAll('.diag-icon-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      grid.querySelectorAll('.diag-icon-btn').forEach(b => b.classList.remove('selected'));
      btn.classList.add('selected');
      document.getElementById('mt-diag').value = btn.dataset.pat;
      const showSec = isKPattern(btn.dataset.pat);
      const wrapD = document.getElementById('mt-secProf-wrap');
      const wrapH = document.getElementById('mt-secProfH-wrap');
      if (wrapD) wrapD.style.display = showSec ? '' : 'none';
      if (wrapH) wrapH.style.display = showSec ? '' : 'none';
      const newPat = btn.dataset.pat;
      const wrapStagger = document.getElementById('mt-staggerFlip-wrap');
      if (wrapStagger) wrapStagger.style.display = (newPat==='Staggered'||newPat==='Staggered-50Pct') ? '' : 'none';
      const wrapHip = document.getElementById('mt-hip-wrap');
      const def = HIP_BRACING_DEFS[newPat];
      if (wrapHip) wrapHip.style.display = def ? '' : 'none';
      if (def) {
        // Si el caso seleccionado no existe para el nuevo patrón, se reinicia a NONE
        const currentHip = document.getElementById('mt-hip').value;
        const hipSel = def.options.includes(currentHip) ? currentHip : 'none';
        document.getElementById('mt-hip').value = hipSel;
        buildHipBracingGrid('hip-icon-grid', 'mt-hip', 'mt-hipH-wrap', 'mt-hipDia-wrap', 'mt-hipD-wrap', hipSel, newPat);
        document.getElementById('mt-hipH-wrap').style.display = hipSel==='none' ? 'none' : '';
        document.getElementById('mt-hipDia-wrap').style.display = def.hasDiaphragm(hipSel) ? '' : 'none';
        document.getElementById('mt-hipD-wrap').style.display = def.hasDiagonal(hipSel) ? '' : 'none';
      }
      buildSecModalPreview();
    });
  });
}

// ── Plan bracing (diafragma en planta) ──────────────────────────
const PLAN_BRACING_PATTERNS = ['none', 'B-B', 'A-A'];
const PLAN_BRACING_LABELS   = {none:'NONE', 'B-B':'Simple', 'A-A':'Compuesto'};

function planBracingIconSVG(pattern, nLegs) {
  const cx = 17, cy = 16, R = 13;
  const ang  = i => -Math.PI/2 + i*2*Math.PI/nLegs;
  const pt   = i => [cx + R*Math.cos(ang(i)), cy + R*Math.sin(ang(i))];
  const mid  = (a,b) => [(a[0]+b[0])/2, (a[1]+b[1])/2];
  const corners = Array.from({length:nLegs}, (_,i) => pt(i));
  const mids    = corners.map((c,i) => mid(c, corners[(i+1)%nLegs]));
  const line = (a,b,color,w) => `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${color}" stroke-width="${w}"/>`;
  let svg = '';
  for (let i = 0; i < nLegs; i++) svg += line(corners[i], corners[(i+1)%nLegs], '#3B82F6', 1.2);
  if (pattern === 'B-B' || pattern === 'A-A') {
    for (let i = 0; i < nLegs; i++) svg += line(mids[i], mids[(i+1)%nLegs], '#22C55E', 1.1);
  }
  if (pattern === 'A-A') {
    for (let i = 0; i < nLegs; i++) {
      const corner = corners[i], mPrev = mids[(i-1+nLegs)%nLegs], mNext = mids[i];
      const mA = mid(corner,mPrev), mB = mid(mPrev,mNext), mC = mid(mNext,corner);
      svg += line(mA,mB,'#B85FD6',1) + line(mB,mC,'#B85FD6',1) + line(mC,mA,'#B85FD6',1);
    }
  }
  return `<svg viewBox="0 0 34 32" width="30" height="30">${svg}</svg>`;
}

function buildPlanBracingGrid(gridId, hiddenId, profWrapId, corner2WrapId, selected, nLegs) {
  const grid = document.getElementById(gridId);
  if (!grid) return;
  grid.innerHTML = PLAN_BRACING_PATTERNS.map(p => `
    <div class="diag-icon-btn${p===selected?' selected':''}" data-pat="${p}" title="${PLAN_BRACING_LABELS[p]}">
      ${planBracingIconSVG(p, nLegs)}
      <span>${PLAN_BRACING_LABELS[p]}</span>
    </div>`).join('');
  grid.querySelectorAll('.diag-icon-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      grid.querySelectorAll('.diag-icon-btn').forEach(b => b.classList.remove('selected'));
      btn.classList.add('selected');
      const pat = btn.dataset.pat;
      document.getElementById(hiddenId).value = pat;
      const profWrap   = document.getElementById(profWrapId);
      const corner2Wrap = document.getElementById(corner2WrapId);
      if (profWrap)    profWrap.style.display    = pat==='none' ? 'none' : '';
      if (corner2Wrap) corner2Wrap.style.display  = pat==='A-A'  ? '' : 'none';
    });
  });
}

// ── Hip bracing (solo X-25Pct) ──────────────────────────────────
const HIP_BRACING_LABELS  = {none:'NONE', '1':'Caso 1', '2':'Caso 2', '3':'Caso 3', '4':'Caso 4'};
// Patrones que admiten hip bracing, sus opciones disponibles y cuándo mostrar cada campo de perfil
const HIP_BRACING_DEFS = {
  'X-25Pct': {
    options: ['none','1','2','3','4'],
    hasDiaphragm: opt => opt==='2'||opt==='3'||opt==='4',
    hasDiagonal:  opt => opt==='3'||opt==='4',
  },
  'K-25Pct': {
    options: ['none','1','2','3'],
    hasDiaphragm: () => false,   // TC-TC ya lo cubre Plan Bracing — no aplica aquí
    hasDiagonal:  opt => opt==='1'||opt==='3',
  },
  'K-25Pct2': {
    options: ['none','1','2','3'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='1'||opt==='3',
  },
  'K-33Pct': {
    options: ['none','1','2'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='2',
  },
  'K-50Pct': {
    options: ['none','1','2'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='2',
  },
  'K-50Pct-Rev': {
    options: ['none','1','2'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='2',
  },
  'K-33Pct-Rev': {
    options: ['none','1','2'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='2',
  },
  'K-25Pct-Rev': {
    options: ['none','1','2','3'],
    hasDiaphragm: () => false,
    hasDiagonal:  opt => opt==='1'||opt==='3',
  },
};

// K-25Pct: un solo vértice abajo (BL=BR, el hip) del que parten 2 líneas hacia
// TC de cada cara — P1R/P2R/P3R sobre la línea izquierda (cara L), P1L/P2L/P3L
// sobre la línea derecha (cara R), igual que el diagrama de referencia.
function hipBracingIconSVG_K25(opt) {
  const bottom = [18, 37], TCL = [6, 4], TCR = [30, 4];
  const lerp = (p,q,t) => [p[0]+(q[0]-p[0])*t, p[1]+(q[1]-p[1])*t];
  const P1R=lerp(bottom,TCL,.25), P2R=lerp(bottom,TCL,.50), P3R=lerp(bottom,TCL,.75);
  const P1L=lerp(bottom,TCR,.25), P2L=lerp(bottom,TCR,.50), P3L=lerp(bottom,TCR,.75);
  const line = (a,b,color,w=1.4) => `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${color}" stroke-width="${w}"/>`;
  const dot  = (p,color) => `<circle cx="${p[0]}" cy="${p[1]}" r="1.8" fill="${color}"/>`;
  let svg = '';
  svg += line(bottom, TCL, '#94A3B8', 1.2) + line(bottom, TCR, '#94A3B8', 1.2);
  if (opt === 'none') return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;

  if (opt === '1') {
    svg += line(P2R, P2L, '#3B82F6');
    svg += line(P2R, TCR, '#FFA500');
    svg += dot(TCR, '#00D4FF');
    return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
  }

  svg += line(P1R, P1L, '#3B82F6');
  svg += line(P2R, P2L, '#3B82F6');
  svg += line(P3R, P3L, '#3B82F6');
  if (opt === '3') {
    svg += line(P1L, P2R, '#FFA500') + line(P2L, P3R, '#FFA500') + line(P3L, TCL, '#FFA500');
    svg += dot(TCL, '#00D4FF');
  }
  return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
}

// K-33Pct: misma idea que K-25Pct pero con solo 2 niveles (1/3, 2/3).
function hipBracingIconSVG_K33(opt) {
  const bottom = [18, 37], TCL = [6, 4], TCR = [30, 4];
  const lerp = (p,q,t) => [p[0]+(q[0]-p[0])*t, p[1]+(q[1]-p[1])*t];
  const P1R=lerp(bottom,TCL,1/3), P2R=lerp(bottom,TCL,2/3);
  const P1L=lerp(bottom,TCR,1/3), P2L=lerp(bottom,TCR,2/3);
  const line = (a,b,color,w=1.4) => `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${color}" stroke-width="${w}"/>`;
  const dot  = (p,color) => `<circle cx="${p[0]}" cy="${p[1]}" r="1.8" fill="${color}"/>`;
  let svg = '';
  svg += line(bottom, TCL, '#94A3B8', 1.2) + line(bottom, TCR, '#94A3B8', 1.2);
  if (opt === 'none') return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;

  svg += line(P1R, P1L, '#3B82F6');
  svg += line(P2R, P2L, '#3B82F6');
  if (opt === '2') {
    svg += line(P1L, P2R, '#FFA500') + line(P2L, TCL, '#FFA500');
    svg += dot(TCL, '#00D4FF');
  }
  return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
}

// K-50Pct: un solo nivel (50%).
function hipBracingIconSVG_K50(opt) {
  const bottom = [18, 37], TCL = [6, 4], TCR = [30, 4];
  const lerp = (p,q,t) => [p[0]+(q[0]-p[0])*t, p[1]+(q[1]-p[1])*t];
  const PR=lerp(bottom,TCL,.5), PL=lerp(bottom,TCR,.5);
  const line = (a,b,color,w=1.4) => `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${color}" stroke-width="${w}"/>`;
  const dot  = (p,color) => `<circle cx="${p[0]}" cy="${p[1]}" r="1.8" fill="${color}"/>`;
  let svg = '';
  svg += line(bottom, TCL, '#94A3B8', 1.2) + line(bottom, TCR, '#94A3B8', 1.2);
  if (opt === 'none') return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;

  svg += line(PR, PL, '#3B82F6');
  if (opt === '2') {
    svg += line(PL, TCL, '#FFA500');
    svg += dot(TCL, '#00D4FF');
  }
  return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
}

function hipBracingIconSVG(opt, pattern) {
  if (pattern === 'K-25Pct' || pattern === 'K-25Pct2' || pattern === 'K-25Pct-Rev') return hipBracingIconSVG_K25(opt);
  if (pattern === 'K-33Pct' || pattern === 'K-33Pct-Rev') return hipBracingIconSVG_K33(opt);
  if (pattern === 'K-50Pct' || pattern === 'K-50Pct-Rev') return hipBracingIconSVG_K50(opt);

  const top=[18,3], bot=[18,37], left=[6,20], right=[30,20];
  const wAt = y => 12 * (1 - Math.abs(y-20)/17);   // ancho del rombo a la altura y
  const yLow=12, yMid=20, yHigh=28;
  const line = (a,b,color,w=1.2) => `<line x1="${a[0].toFixed(1)}" y1="${a[1].toFixed(1)}" x2="${b[0].toFixed(1)}" y2="${b[1].toFixed(1)}" stroke="${color}" stroke-width="${w}"/>`;
  let svg = '';
  svg += line(top,left,'#94A3B8') + line(top,right,'#94A3B8') + line(bot,left,'#94A3B8') + line(bot,right,'#94A3B8');
  if (opt === 'none') return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
  const wL = wAt(yLow);

  svg += line([18-wL,yLow],[18+wL,yLow], '#3B82F6');
  if (opt !== '1') svg += line([18-12,yMid],[18+12,yMid], '#EF4444');
  svg += line([18-wL,yHigh],[18+wL,yHigh], '#3B82F6');
  if (opt === '3') {
    svg += line([18-wL,yLow],[18+12,yMid],'#FFA500') + line([18-12,yMid],[18+wL,yHigh],'#FFA500');
  } else if (opt === '4') {
    svg += line([18+wL,yLow],[18-12,yMid],'#FFA500') + line([18-12,yMid],[18+wL,yHigh],'#FFA500');
  }
  return `<svg viewBox="0 0 36 40" width="30" height="32">${svg}</svg>`;
}

function buildHipBracingGrid(gridId, hiddenId, profHWrapId, profDiaWrapId, profDWrapId, selected, pattern) {
  const grid = document.getElementById(gridId);
  if (!grid) return;
  const def = HIP_BRACING_DEFS[pattern];
  if (!def) { grid.innerHTML = ''; return; }
  const options = ['none', ...def.options.filter(o => o!=='none')];
  grid.innerHTML = options.map(o => `
    <div class="diag-icon-btn${o===selected?' selected':''}" data-opt="${o}" title="${HIP_BRACING_LABELS[o]}">
      ${hipBracingIconSVG(o, pattern)}
      <span>${HIP_BRACING_LABELS[o]}</span>
    </div>`).join('');
  grid.querySelectorAll('.diag-icon-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      grid.querySelectorAll('.diag-icon-btn').forEach(b => b.classList.remove('selected'));
      btn.classList.add('selected');
      const opt = btn.dataset.opt;
      document.getElementById(hiddenId).value = opt;
      const profHWrap   = document.getElementById(profHWrapId);
      const profDiaWrap = document.getElementById(profDiaWrapId);
      const profDWrap   = document.getElementById(profDWrapId);
      if (profHWrap)   profHWrap.style.display   = opt==='none' ? 'none' : '';
      if (profDiaWrap)  profDiaWrap.style.display = def.hasDiaphragm(opt) ? '' : 'none';
      if (profDWrap)    profDWrap.style.display   = def.hasDiagonal(opt) ? '' : 'none';
    });
  });
}

function openSecModal(idx) {
  const cfg  = getConfig();
  const n    = secData.length;
  const nInc = cfg.nInc;
  const h    = +(cfg.height / n).toFixed(2);

  modalIdx  = idx;
  modalTemp = {...secData[idx]};

  const s       = modalTemp;
  const tipo    = idx < nInc ? 'INC' : 'REC';
  const tipoLbl = idx < nInc ? 'Inclinado' : 'Recto';

  document.getElementById('sec-modal-body').innerHTML = `
    <div class="sm-card">
      <div class="sm-card-hdr">
        <span class="sm-card-title">Section ${idx+1}</span>
        <span class="sec-tag">${h} m</span>
      </div>
      <div style="display:flex;gap:8px;align-items:flex-start">
        <div class="sm-grid" style="flex:1;min-width:0">
          <div class="sm-field" style="grid-column: 1 / -1">
            <label class="sm-lbl">CONFIGURACIÓN</label>
            <select class="sm-sel" id="mt-diag" style="display:none">
              ${DIAG_PATTERNS.map(p=>`<option value="${p}"${s.diag===p?' selected':''}>${p}</option>`).join('')}
            </select>
            <div class="diag-icon-grid" id="diag-icon-grid"></div>
          </div>
          <div class="sm-field" id="mt-staggerFlip-wrap" style="grid-column: 1 / -1; ${(s.diag==='Staggered'||s.diag==='Staggered-50Pct')?'':'display:none'}">
            <label class="sm-chk-row">
              <input type="checkbox" id="mt-staggerFlip" ${s.staggerFlip?'checked':''} onchange="buildSecModalPreview()">
              <span class="sm-chk-lbl">INVERTIR ORIENTACIÓN DE LA DIAGONAL</span>
            </label>
          </div>
          <div class="sm-field" id="mt-hip-wrap" style="grid-column: 1 / -1; ${HIP_BRACING_DEFS[s.diag]?'':'display:none'}">
            <label class="sm-lbl">HIP BRACING</label>
            <select class="sm-sel" id="mt-hip" style="display:none">
              ${['none','1','2','3','4'].map(o=>`<option value="${o}"${s.hip===o?' selected':''}>${o}</option>`).join('')}
            </select>
            <div class="diag-icon-grid" id="hip-icon-grid"></div>
            <div id="mt-hipH-wrap" style="${s.hip==='none'?'display:none':''};margin-top:4px">
              <label class="sm-lbl" style="display:block">PERFIL HORIZONTALES (HIP)</label>
              <input class="sm-inp" id="mt-HhipH" type="text" placeholder="ej. L2x2x3/16"
                value="${s.HhipH==='-'?'':s.HhipH??''}">
            </div>
            <div id="mt-hipDia-wrap" style="${HIP_BRACING_DEFS[s.diag]?.hasDiaphragm(s.hip)?'':'display:none'};margin-top:4px">
              <label class="sm-lbl" style="display:block">PERFIL HORIZONTAL (DIAFRAGMA)</label>
              <input class="sm-inp" id="mt-HhipDia" type="text" placeholder="ej. L2x2x3/16"
                value="${s.HhipDia==='-'?'':s.HhipDia??''}">
            </div>
            <div id="mt-hipD-wrap" style="${HIP_BRACING_DEFS[s.diag]?.hasDiagonal(s.hip)?'':'display:none'};margin-top:4px">
              <label class="sm-lbl" style="display:block">PERFIL DIAGONALES (HIP)</label>
              <input class="sm-inp" id="mt-HhipD" type="text" placeholder="ej. L2x2x3/16"
                value="${s.HhipD==='-'?'':s.HhipD??''}">
            </div>
          </div>
          <div class="sm-field" style="border-top:1px solid var(--border); padding-top:8px; margin-top:4px;">
            <label class="sm-lbl">BAHÍAS (repeticiones)</label>
            <input class="sm-inp" id="mt-bays" type="number" min="1" max="20" step="1"
              value="${s.bays ?? 1}" oninput="buildSecModalPreview()">
          </div>
          <div class="sm-field" style="border-top:1px solid var(--border); padding-top:8px; margin-top:4px;">
            <label class="sm-lbl">M — MONTANTES (piernas)</label>
            <input class="sm-inp" id="mt-M" type="text" placeholder="ej. L4x4x1/4"
              value="${s.M==='-'?'':s.M}">
          </div>
          <div class="sm-field">
            <label class="sm-lbl">D — DIAGONALES</label>
            <input class="sm-inp" id="mt-D" type="text" placeholder="ej. L3x3x3/16"
              value="${s.D==='-'?'':s.D}">
          </div>
          <div class="sm-field" id="mt-secProf-wrap" style="${isKPattern(s.diag)?'':'display:none'}">
            <label class="sm-lbl">Ds — DIAGONAL SECUNDARIA</label>
            <input class="sm-inp" id="mt-Ds" type="text" placeholder="ej. L2x2x3/16"
              value="${s.Ds==='-'?'':s.Ds}">
          </div>
          <div class="sm-field" id="mt-secProfH-wrap" style="${isKPattern(s.diag)?'':'display:none'}">
            <label class="sm-lbl">Hs — HORIZONTAL SECUNDARIA</label>
            <input class="sm-inp" id="mt-Hs" type="text" placeholder="ej. L2x2x3/16"
              value="${s.Hs==='-'?'':s.Hs}">
          </div>
          <div class="sm-field" style="grid-column: 1 / -1; border-top:1px solid var(--border); padding-top:8px; margin-top:4px;">
            <label class="sm-chk-row">
              <input type="checkbox" id="mt-topH" ${s.topH?'checked':''}
                onchange="document.getElementById('mt-topH-prof').style.display=this.checked?'':'none';buildSecModalPreview()">
              <span class="sm-chk-lbl">HORIZONTAL EN TOP DEL TRAMO</span>
            </label>
            <div id="mt-topH-prof" style="${s.topH?'':'display:none'};margin-top:3px">
              <input class="sm-inp" id="mt-Htop" type="text" placeholder="ej. L2x2x3/16"
                value="${s.Htop==='-'?'':s.Htop??''}">
              <label class="sm-lbl" style="margin-top:6px;display:block">PLAN BRACING</label>
              <select class="sm-sel" id="mt-planTop" style="display:none">
                ${PLAN_BRACING_PATTERNS.map(p=>`<option value="${p}"${s.planTop===p?' selected':''}>${p}</option>`).join('')}
              </select>
              <div class="diag-icon-grid" id="planTop-icon-grid"></div>
              <div id="mt-PbTop-wrap" style="${s.planTop==='none'?'display:none':''};margin-top:4px">
                <input class="sm-inp" id="mt-PbTop" type="text" placeholder="ej. L2x2x3/16"
                  value="${s.PbTop==='-'?'':s.PbTop??''}">
              </div>
              <div id="mt-PbTop2-wrap" style="${s.planTop==='A-A'?'':'display:none'};margin-top:4px">
                <label class="sm-lbl" style="display:block">PERFIL ESQUINAS (Diaphragm 2)</label>
                <input class="sm-inp" id="mt-PbTop2" type="text" placeholder="ej. L2x2x3/16"
                  value="${s.PbTop2==='-'?'':s.PbTop2??''}">
              </div>
            </div>
          </div>
          <div class="sm-field" style="grid-column: 1 / -1; border-top:1px solid var(--border); padding-top:8px; margin-top:4px;">
            <label class="sm-chk-row">
              <input type="checkbox" id="mt-bayTopH" ${s.bayTopH?'checked':''}
                onchange="document.getElementById('mt-bayH-prof').style.display=this.checked?'':'none';buildSecModalPreview()">
              <span class="sm-chk-lbl">HORIZONTAL EN TOP DE CADA BAHÍA</span>
            </label>
            <div id="mt-bayH-prof" style="${s.bayTopH?'':'display:none'};margin-top:3px">
              <input class="sm-inp" id="mt-Hbay" type="text" placeholder="ej. L2x2x3/16"
                value="${s.Hbay==='-'?'':s.Hbay??''}">
              <label class="sm-lbl" style="margin-top:6px;display:block">PLAN BRACING</label>
              <select class="sm-sel" id="mt-planBay" style="display:none">
                ${PLAN_BRACING_PATTERNS.map(p=>`<option value="${p}"${s.planBay===p?' selected':''}>${p}</option>`).join('')}
              </select>
              <div class="diag-icon-grid" id="planBay-icon-grid"></div>
              <div id="mt-PbBay-wrap" style="${s.planBay==='none'?'display:none':''};margin-top:4px">
                <input class="sm-inp" id="mt-PbBay" type="text" placeholder="ej. L2x2x3/16"
                  value="${s.PbBay==='-'?'':s.PbBay??''}">
              </div>
              <div id="mt-PbBay2-wrap" style="${s.planBay==='A-A'?'':'display:none'};margin-top:4px">
                <label class="sm-lbl" style="display:block">PERFIL ESQUINAS (Diaphragm 2)</label>
                <input class="sm-inp" id="mt-PbBay2" type="text" placeholder="ej. L2x2x3/16"
                  value="${s.PbBay2==='-'?'':s.PbBay2??''}">
              </div>
            </div>
          </div>
        </div>
        <div class="sm-preview-panel">
          <div class="sm-preview-title">VISTA</div>
          <div class="sm-preview-box" id="sec-modal-preview"></div>
        </div>
      </div>
    </div>`;

  buildDiagIconGrid(s.diag);
  const nLegs = cfg.type === 'square' ? 4 : 3;
  buildPlanBracingGrid('planTop-icon-grid', 'mt-planTop', 'mt-PbTop-wrap', 'mt-PbTop2-wrap', s.planTop, nLegs);
  buildPlanBracingGrid('planBay-icon-grid', 'mt-planBay', 'mt-PbBay-wrap', 'mt-PbBay2-wrap', s.planBay, nLegs);
  buildHipBracingGrid('hip-icon-grid', 'mt-hip', 'mt-hipH-wrap', 'mt-hipDia-wrap', 'mt-hipD-wrap', s.hip, s.diag);
  document.getElementById('sec-modal-title').textContent = `SECTION ${idx+1}`;
  document.getElementById('sec-modal-overlay').classList.add('open');
  buildSecModalPreview();
}

function closeSecModal(e) {
  if (e && e.target !== document.getElementById('sec-modal-overlay')) return;
  document.getElementById('sec-modal-overlay').classList.remove('open');
}

function buildSecModalPreview() {
  const el = document.getElementById('sec-modal-preview');
  if (!el) return;
  const bays   = Math.max(1, +document.getElementById('mt-bays')?.value || 1);
  const diag   = document.getElementById('mt-diag')?.value || 'X';
  const topH   = document.getElementById('mt-topH')?.checked ?? true;
  const bayTopH= document.getElementById('mt-bayTopH')?.checked ?? false;
  const staggerFlip = document.getElementById('mt-staggerFlip')?.checked ?? false;

  const LBL_W = 46;   // columna reservada para etiquetas de perfil (M, D, Ds, H, Hs)
  const BW = 72, BH = 52, x0 = LBL_W + 10, x1 = x0 + BW;
  const totalH = bays * BH;
  const SEC_COLOR = '#5A7A95';   // mismo color que la celosía secundaria en el visor 3D
  const toXY = (p, bayTop) => [x0 + (p[0]-6)*BW/24, bayTop + (p[1]-6)*BH/36];

  let svg = '';
  // Piernas (perfil M)
  svg += `<line x1="${x0}" y1="0" x2="${x0}" y2="${totalH}" stroke="#3B82F6" stroke-width="1.6"/>`;
  svg += `<line x1="${x1}" y1="0" x2="${x1}" y2="${totalH}" stroke="#3B82F6" stroke-width="1.6"/>`;

  for (let b = 0; b < bays; b++) {
    const isTop = b === bays - 1;
    const bayTop = (bays - 1 - b) * BH;
    const staggerUp = (b%2===0) !== staggerFlip;   // misma alternancia que el modelo real
    const rawLines = diagIconLines(diag, staggerUp);
    rawLines.forEach(({a, b: pb, type, principal}) => {
      const [ax,ay] = toXY(a, bayTop), [bx,by] = toXY(pb, bayTop);
      const color = principal===false ? SEC_COLOR : (type==='d'?'#EF4444':'#22C55E');
      svg += `<line x1="${ax.toFixed(1)}" y1="${ay.toFixed(1)}" x2="${bx.toFixed(1)}" y2="${by.toFixed(1)}" stroke="${color}" stroke-width="1.3"/>`;
    });
    // Top horizontal de esta bahía (perfil H)
    const showH = (isTop && topH) || (!isTop && bayTopH);
    const hCol  = showH ? '#22C55E' : '#1a2d42';
    const dash  = showH ? '' : ' stroke-dasharray="2,1.5"';
    svg += `<line x1="${x0}" y1="${bayTop}" x2="${x1}" y2="${bayTop}" stroke="${hCol}" stroke-width="${showH?1.8:0.6}"${dash}/>`;
  }

  // ── Etiquetas de perfil (identifican el color de cada línea: M/D/Ds/H/Hs) ──
  const labelLines = diagIconLines(diag, true);   // dirección no afecta qué tipos de línea existen
  const hasPrincipalD = labelLines.some(l => l.type==='d' && l.principal!==false);
  const hasSecD       = labelLines.some(l => l.type==='d' && l.principal===false);
  const hasSecH       = labelLines.some(l => l.type==='h' && l.principal===false);

  const labelDefs = [['M', '#3B82F6']];
  if (hasPrincipalD) labelDefs.push(['D', '#EF4444']);
  if (hasSecD)       labelDefs.push(['Ds', SEC_COLOR]);
  labelDefs.push(['H', '#22C55E']);
  if (hasSecH)       labelDefs.push(['Hs', SEC_COLOR]);

  labelDefs.forEach(([text, color], i) => {
    const ly = 8 + i*14;
    svg += `<text x="2" y="${ly+3}" font-size="10" fill="${color}" font-family="monospace">${text}</text>`;
  });

  const dispW = x1 + 10;
  const dispH = Math.min(340, Math.max(140, totalH * (bays > 6 ? 1.5 : bays > 3 ? 1.9 : 2.3)));
  el.innerHTML = `<svg viewBox="0 0 ${dispW} ${totalH}" width="${Math.round(dispW*1.5)}" height="${dispH}" style="display:block">${svg}</svg>`;
}

function applySecModal() {
  const val = id => document.getElementById(id)?.value.trim() || '-';
  secData[modalIdx] = {
    diag:    document.getElementById('mt-diag').value,
    bays:    Math.max(1, +document.getElementById('mt-bays').value || 1),
    M:       val('mt-M'),
    D:       val('mt-D'),
    topH:    document.getElementById('mt-topH').checked,
    Htop:    val('mt-Htop'),
    bayTopH: document.getElementById('mt-bayTopH').checked,
    Hbay:    val('mt-Hbay'),
    Ds:      val('mt-Ds'),
    Hs:      val('mt-Hs'),
    planTop: document.getElementById('mt-planTop').value,
    PbTop:   val('mt-PbTop'),
    PbTop2:  val('mt-PbTop2'),
    planBay: document.getElementById('mt-planBay').value,
    PbBay:   val('mt-PbBay'),
    PbBay2:  val('mt-PbBay2'),
    hip:     document.getElementById('mt-hip').value,
    HhipH:   val('mt-HhipH'),
    HhipD:   val('mt-HhipD'),
    HhipDia: val('mt-HhipDia'),
    staggerFlip: document.getElementById('mt-staggerFlip').checked,
  };
  document.getElementById('sec-modal-overlay').classList.remove('open');
  buildSectionRows(secData.length);
  refresh();
}


// ── Circular fade mask ─────────────────────────────────────────────────
let fadeMesh = null;

function buildFadeMask(totalSize, fadeStartPct, exponent, enabled) {
  if (fadeMesh) {
    fadeMesh.geometry.dispose();
    fadeMesh.material.map && fadeMesh.material.map.dispose();
    fadeMesh.material.dispose();
    scene.remove(fadeMesh);
    fadeMesh = null;
  }
  if (!enabled) return;

  // Canvas radial gradient — bg color = #0A1628 = rgba(10,22,40)
  const RES = 512;
  const canvas = document.createElement('canvas');
  canvas.width = canvas.height = RES;
  const ctx = canvas.getContext('2d');
  const cx = RES / 2;

  const grad = ctx.createRadialGradient(cx, cx, 0, cx, cx, cx);
  const t0 = Math.min(fadeStartPct / 100, 0.97);

  // Build gradient with configurable exponent (controls softness)
  const steps = 20;
  for (let i = 0; i <= steps; i++) {
    const t = i / steps;            // 0 → 1 (normalized radius)
    if (t <= t0) {
      grad.addColorStop(t, 'rgba(10,22,40,0)');
    } else {
      const progress = (t - t0) / (1 - t0);      // 0 → 1 in fade zone
      const alpha = Math.pow(progress, 1 / exponent);
      grad.addColorStop(t, `rgba(10,22,40,${alpha.toFixed(3)})`);
    }
  }

  ctx.fillStyle = grad;
  ctx.fillRect(0, 0, RES, RES);

  const tex = new THREE.CanvasTexture(canvas);

  // Circle radius = half-diagonal of the grid square so corners quedan cubiertos
  // grid side = totalSize*2, half-diagonal = totalSize * sqrt(2)
  const geo = new THREE.CircleGeometry(totalSize * Math.SQRT2, 128);
  const mat = new THREE.MeshBasicMaterial({
    map: tex,
    transparent: true,
    depthWrite: false,
    polygonOffset: true,
    polygonOffsetFactor: -1,
    polygonOffsetUnits: -1,
  });
  fadeMesh = new THREE.Mesh(geo, mat);
  fadeMesh.position.z = 0.02;
  fadeMesh.renderOrder = 2;
  scene.add(fadeMesh);
}

function toggleGridPanel(e) {
  if (e) e.stopPropagation();
  const panel = document.getElementById('grid-panel');
  const btn   = document.getElementById('grid-cfg-btn');
  panel.classList.toggle('open');
  btn.style.background = panel.classList.contains('open') ? '#0D2040' : '';
  btn.style.color      = panel.classList.contains('open') ? 'var(--cyan)' : '';
}

// Close panel when clicking outside
document.addEventListener('click', e => {
  const panel = document.getElementById('grid-panel');
  const btn   = document.getElementById('grid-cfg-btn');
  if (!panel.contains(e.target) && !btn.contains(e.target)) {
    panel.classList.remove('open');
    btn.style.background = '';
    btn.style.color = '';
  }
});

function refreshGrid() {
  const size  = +document.getElementById('grid-size').value  || 200;
  const divs  = +document.getElementById('grid-divs').value  || 10;
  const thick = +document.getElementById('grid-thick').value || 1.5;
  const subs  = +document.getElementById('grid-subs').value  || 5;
  buildGrid(size, divs, thick, subs);

  const enabled = document.getElementById('fade-on').checked;
  const start   = +document.getElementById('fade-start').value || 45;
  const exp     = +document.getElementById('fade-exp').value   || 2;
  buildFadeMask(size / 2, start, exp, enabled);
}

// Boot — inicia limpio sin torre
document.getElementById('s-fecha').value = new Date().toISOString().slice(0,10);
buildSectionRows(8);
refreshGrid();

// ── Member pick / highlight / info ────────────────────────────────────────────
function _pickMember(e) {
  const rect = renderer.domElement.getBoundingClientRect();
  const ndc  = new THREE.Vector2(
    ((e.clientX - rect.left) / rect.width)  *  2 - 1,
   -((e.clientY - rect.top)  / rect.height) *  2 + 1
  );
  _raycaster.setFromCamera(ndc, camera);
  const targets = towerGroup.children.filter(c =>
    c instanceof THREE.LineSegments && c.userData.members && c.userData.members.length
  );
  const hits = _raycaster.intersectObjects(targets, false);
  if (!hits.length) { closeMemberInfo(); return; }
  const hit    = hits[0];
  const segIdx = Math.floor(hit.index / 2);
  const member = hit.object.userData.members[segIdx];
  if (!member) { closeMemberInfo(); return; }
  _highlightMember(member);
  showMemberInfo(member, e.clientX, e.clientY);
}

function _highlightMember(m) {
  if (_hlMesh) { _hlMesh.geometry.dispose(); _hlMesh.material.dispose(); scene.remove(_hlMesh); }
  const ni = _towerData.nodes[m.ni], nj = _towerData.nodes[m.nj];
  const hlGeo = new THREE.BufferGeometry();
  hlGeo.setAttribute('position', new THREE.Float32BufferAttribute(
    [ni.x, ni.y, ni.z, nj.x, nj.y, nj.z], 3));
  _hlMesh = new THREE.LineSegments(hlGeo, new THREE.LineBasicMaterial({color:0x00D4FF, linewidth:2}));
  scene.add(_hlMesh);
}

function showMemberInfo(m, cx, cy) {
  const panel = document.getElementById('mi-panel');
  if (!panel || !_towerData) return;
  const ni = _towerData.nodes[m.ni], nj = _towerData.nodes[m.nj];
  const dx = nj.x-ni.x, dy = nj.y-ni.y, dz = nj.z-ni.z;
  const len = Math.sqrt(dx*dx+dy*dy+dz*dz).toFixed(3);
  const typeNames = {leg:'PIERNA', diagonal:'DIAGONAL', horizontal:'HORIZONTAL', guy:'GUY WIRE', planbrace:'PLAN BRACING', hipbrace:'HIP BRACING'};
  document.getElementById('mi-type').textContent = typeNames[m.type] || m.type.toUpperCase();
  const sec = m.sec ?? null;
  const sd  = (sec != null && typeof secData !== 'undefined') ? secData[sec] : null;
  const isPrincipal = m.principal !== false;
  let profile = '—';
  if (sd) {
    if (m.type==='leg') profile = (sd.M && sd.M!=='-') ? sd.M : '—';
    else if (m.type==='diagonal') profile = isPrincipal
      ? ((sd.D  && sd.D!=='-')  ? sd.D  : '—')
      : ((sd.Ds && sd.Ds!=='-') ? sd.Ds : '—');
    else if (m.type==='horizontal') profile = isPrincipal
      ? ((sd.Htop && sd.Htop!=='-') ? sd.Htop : (sd.Hbay && sd.Hbay!=='-') ? sd.Hbay : '—')
      : ((sd.Hs   && sd.Hs!=='-')   ? sd.Hs   : '—');
    else if (m.type==='planbrace') {
      const pTop = m.isCorner ? sd.PbTop2 : sd.PbTop;
      const pBay = m.isCorner ? sd.PbBay2 : sd.PbBay;
      profile = m.isTop
        ? ((pTop && pTop!=='-') ? pTop : '—')
        : ((pBay && pBay!=='-') ? pBay : '—');
    }
    else if (m.type==='hipbrace') {
      const p = m.isDiag ? sd.HhipD : (m.isDiaphragm ? sd.HhipDia : sd.HhipH);
      profile = (p && p!=='-') ? p : '—';
    }
  }
  const rows = [
    ['Tramo',     sec != null ? `${sec+1}` : '—'],
    ['Categoría', isPrincipal ? 'Principal' : 'Secundario'],
    ['Perfil',    profile],
    ['Longitud',  `${len} m`],
    ['ID perfil', _profileId(m)],
  ];
  document.getElementById('mi-body').innerHTML = rows.map(([l, v]) =>
    l==='Categoría'
      ? `<span class="mi-lbl">${l}</span><span class="mi-val" style="color:${isPrincipal?'#22C55E':'#7FA8C9'}">${v}</span>`
      : `<span class="mi-lbl">${l}</span><span class="mi-val">${v}</span>`
  ).join('');
  // Posicionar fuera de pantalla primero para medir el ancho/alto reales del contenido
  panel.style.left = '-9999px';
  panel.style.top  = '-9999px';
  panel.style.display = 'block';
  const pw = panel.offsetWidth, ph = panel.offsetHeight;
  const vw = window.innerWidth, vh = window.innerHeight;
  let x = cx + 14, y = cy - 10;
  if (x + pw > vw - 8) x = cx - pw - 8;
  if (y + ph > vh - 8) y = vh - ph - 8;
  if (y < 8) y = 8;
  panel.style.left = x + 'px';
  panel.style.top  = y + 'px';
}

function _profileId(m) {
  const typeLetter  = {leg:'M', diagonal:'D', horizontal:'H', guy:'G', planbrace:'PB', hipbrace:'HB'}[m.type] || 'X';
  const isSecondary = m.principal === false;
  // Numeración independiente: secundarios se cuentan aparte de los principales del mismo tipo+tramo
  const sameGroup = mm => mm.type === m.type && (m.sec != null ? mm.sec === m.sec : true)
    && (mm.principal === false) === isSecondary;
  const group = _towerData.members.filter(sameGroup);
  const idx = group.indexOf(m) + 1;
  const sMark = isSecondary ? 'S' : '';
  return (m.sec != null) ? `${typeLetter}${m.sec+1}${sMark}-${idx}` : `${typeLetter}${sMark}-${idx}`;
}

function closeMemberInfo() {
  const panel = document.getElementById('mi-panel');
  if (panel) panel.style.display = 'none';
  if (_hlMesh) { _hlMesh.geometry.dispose(); _hlMesh.material.dispose(); scene.remove(_hlMesh); _hlMesh = null; }
}

let _toastTimer = null;
function showToast(msg, type='warn', ms=3000) {
  let el = document.getElementById('tsa-toast');
  if (!el) {
    el = document.createElement('div');
    el.id = 'tsa-toast';
    document.body.appendChild(el);
  }
  el.textContent = msg;
  el.className = type + ' show';
  clearTimeout(_toastTimer);
  _toastTimer = setTimeout(() => el.classList.remove('show'), ms);
}
</script>
<div id="tsa-toast"></div>
<div id="mi-panel">
  <div class="mi-hdr">
    <span class="mi-title" id="mi-type">—</span>
    <button class="mi-close-btn" onclick="closeMemberInfo()">✕</button>
  </div>
  <div class="mi-body" id="mi-body"></div>
</div>
</body>
</html>
