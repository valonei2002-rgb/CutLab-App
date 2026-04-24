<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CutLab — Video Editor</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Outfit:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0a0c;
    --bg2: #111115;
    --bg3: #18181f;
    --bg4: #1f1f28;
    --border: #2a2a35;
    --border2: #35354a;
    --accent: #e8ff47;
    --accent2: #7c6af5;
    --accent3: #ff5c87;
    --text: #f0f0f8;
    --text2: #9090aa;
    --text3: #55556a;
    --clip-video: #2d4a7a;
    --clip-audio: #2a5a3a;
    --clip-text: #5a3a6a;
    --red: #ff4444;
    --green: #44ff88;
    --panel-w: 220px;
    --prop-w: 260px;
    --timeline-h: 220px;
    --header-h: 52px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html, body { width: 100%; height: 100%; overflow: hidden; background: var(--bg); color: var(--text); font-family: 'Outfit', sans-serif; font-size: 13px; }

  /* ── HEADER ─────────────────────────────────────── */
  #header {
    height: var(--header-h);
    background: var(--bg2);
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center; gap: 0;
    padding: 0 16px;
    position: relative; z-index: 100;
  }
  .logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 24px;
    letter-spacing: 3px;
    color: var(--accent);
    margin-right: 28px;
  }
  .logo span { color: var(--text2); }
  .menu-btns { display: flex; gap: 4px; }
  .menu-btn {
    padding: 5px 12px; border-radius: 5px; border: none;
    background: transparent; color: var(--text2); cursor: pointer;
    font-family: 'Outfit', sans-serif; font-size: 12px; font-weight: 500;
    transition: all .15s;
  }
  .menu-btn:hover { background: var(--bg4); color: var(--text); }

  .header-center { flex: 1; display: flex; justify-content: center; align-items: center; gap: 8px; }
  .tool-btn {
    width: 34px; height: 34px; border-radius: 6px; border: 1px solid var(--border);
    background: var(--bg3); color: var(--text2); cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: all .15s; font-size: 15px;
  }
  .tool-btn:hover { background: var(--bg4); color: var(--text); border-color: var(--border2); }
  .tool-btn.active { background: var(--accent2); border-color: var(--accent2); color: #fff; }

  .header-right { display: flex; align-items: center; gap: 10px; }
  .export-btn {
    padding: 8px 20px; border-radius: 7px; border: none;
    background: var(--accent); color: #0a0a0c;
    font-family: 'Outfit', sans-serif; font-size: 12px; font-weight: 700;
    cursor: pointer; letter-spacing: .5px;
    transition: all .15s;
  }
  .export-btn:hover { background: #d4eb00; transform: translateY(-1px); }

  /* ── MAIN LAYOUT ─────────────────────────────────── */
  #main {
    display: flex;
    height: calc(100vh - var(--header-h) - var(--timeline-h));
    overflow: hidden;
  }

  /* ── LEFT PANEL ──────────────────────────────────── */
  #left-panel {
    width: var(--panel-w);
    background: var(--bg2);
    border-right: 1px solid var(--border);
    display: flex; flex-direction: column;
    overflow: hidden;
  }
  .panel-tabs {
    display: flex; overflow-x: auto; border-bottom: 1px solid var(--border);
    scrollbar-width: none;
  }
  .panel-tab {
    flex-shrink: 0;
    padding: 10px 12px;
    cursor: pointer; color: var(--text3); font-size: 11px; font-weight: 600;
    letter-spacing: .5px; text-transform: uppercase;
    border-bottom: 2px solid transparent;
    transition: all .15s;
  }
  .panel-tab.active { color: var(--accent); border-bottom-color: var(--accent); }
  .panel-tab:hover:not(.active) { color: var(--text2); }

  .panel-content { flex: 1; overflow-y: auto; padding: 12px; scrollbar-width: thin; scrollbar-color: var(--border2) transparent; }

  /* Media Panel */
  .upload-zone {
    border: 2px dashed var(--border2); border-radius: 10px;
    padding: 24px 12px; text-align: center; cursor: pointer;
    transition: all .2s; margin-bottom: 12px;
  }
  .upload-zone:hover { border-color: var(--accent); background: rgba(232,255,71,.04); }
  .upload-zone .icon { font-size: 28px; margin-bottom: 8px; }
  .upload-zone p { color: var(--text2); font-size: 11px; line-height: 1.5; }
  .upload-zone strong { color: var(--accent); }

  .media-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; }
  .media-thumb {
    aspect-ratio: 16/9; background: var(--bg4); border-radius: 6px;
    border: 1px solid var(--border); cursor: pointer; overflow: hidden;
    position: relative; transition: all .15s;
  }
  .media-thumb:hover { border-color: var(--accent2); transform: scale(1.02); }
  .media-thumb video, .media-thumb img { width: 100%; height: 100%; object-fit: cover; }
  .media-thumb .dur {
    position: absolute; bottom: 3px; right: 4px;
    background: rgba(0,0,0,.7); color: #fff; font-size: 9px;
    padding: 1px 4px; border-radius: 3px; font-family: 'DM Mono', monospace;
  }

  /* Effects Panel */
  .effects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; }
  .effect-item {
    padding: 8px 6px; background: var(--bg4); border: 1px solid var(--border);
    border-radius: 7px; cursor: pointer; text-align: center;
    transition: all .15s; color: var(--text2); font-size: 10px;
  }
  .effect-item:hover { border-color: var(--accent2); color: var(--text); background: rgba(124,106,245,.1); }
  .effect-item.active { border-color: var(--accent2); background: rgba(124,106,245,.2); color: var(--accent2); }
  .effect-item .eicon { font-size: 20px; display: block; margin-bottom: 4px; }

  /* Filters Panel */
  .filter-item {
    display: flex; align-items: center; gap: 8px;
    padding: 8px; border-radius: 7px; cursor: pointer;
    border: 1px solid var(--border); margin-bottom: 5px; background: var(--bg4);
    transition: all .15s;
  }
  .filter-item:hover { border-color: var(--accent); }
  .filter-item.active { border-color: var(--accent); background: rgba(232,255,71,.05); }
  .filter-preview {
    width: 36px; height: 24px; border-radius: 4px; flex-shrink: 0;
  }
  .filter-name { font-size: 11px; color: var(--text2); }

  /* Text Panel */
  .text-styles { display: flex; flex-direction: column; gap: 5px; }
  .text-style-btn {
    padding: 10px; border-radius: 7px; border: 1px solid var(--border);
    background: var(--bg4); cursor: pointer; transition: all .15s;
    display: flex; align-items: center; gap: 8px;
  }
  .text-style-btn:hover { border-color: var(--accent2); background: rgba(124,106,245,.1); }

  /* Audio Panel */
  .audio-item {
    display: flex; align-items: center; gap: 8px;
    padding: 8px; border-radius: 7px; border: 1px solid var(--border);
    background: var(--bg4); cursor: pointer; margin-bottom: 5px;
    transition: all .15s;
  }
  .audio-item:hover { border-color: var(--green); }
  .audio-play { width: 28px; height: 28px; border-radius: 50%; background: var(--bg3); border: 1px solid var(--border2); display: flex; align-items: center; justify-content: center; font-size: 10px; flex-shrink: 0; }
  .audio-info { flex: 1; min-width: 0; }
  .audio-name { font-size: 11px; color: var(--text); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .audio-meta { font-size: 10px; color: var(--text3); }

  /* ── CENTER / PREVIEW ────────────────────────────── */
  #center {
    flex: 1;
    display: flex; flex-direction: column;
    background: var(--bg);
    overflow: hidden;
  }
  #preview-area {
    flex: 1; display: flex; align-items: center; justify-content: center;
    position: relative; background: #050507;
    overflow: hidden;
  }
  #preview-area::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at center, transparent 60%, #0a0a0c 100%);
    pointer-events: none; z-index: 1;
  }
  #video-container {
    position: relative; display: flex; align-items: center; justify-content: center;
    z-index: 2;
  }
  #main-video {
    max-width: 100%; max-height: 100%; border-radius: 4px;
    display: none;
  }
  #text-overlay-canvas {
    position: absolute; inset: 0; z-index: 10; pointer-events: none;
  }
  .active-text-overlay {
    position: absolute; z-index: 11; cursor: move;
    user-select: none;
  }
  #drop-hint {
    display: flex; flex-direction: column; align-items: center; gap: 12px;
    color: var(--text3);
  }
  #drop-hint .big-icon { font-size: 56px; opacity: .4; }
  #drop-hint h3 { font-size: 16px; color: var(--text2); font-weight: 500; }
  #drop-hint p { font-size: 12px; }

  /* Filter overlays */
  #filter-overlay {
    position: absolute; inset: 0; z-index: 3; pointer-events: none;
    mix-blend-mode: normal; border-radius: 4px;
  }

  /* Playback Controls */
  #playback-controls {
    background: var(--bg2); border-top: 1px solid var(--border);
    padding: 10px 16px;
    display: flex; align-items: center; gap: 12px;
  }
  .ctrl-btn {
    width: 32px; height: 32px; border-radius: 6px; border: 1px solid var(--border);
    background: var(--bg3); color: var(--text2); cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    font-size: 13px; transition: all .15s; flex-shrink: 0;
  }
  .ctrl-btn:hover { background: var(--bg4); color: var(--text); }
  .ctrl-btn.play-btn { width: 40px; height: 40px; background: var(--accent); color: #000; border-color: var(--accent); font-size: 16px; border-radius: 50%; }
  .ctrl-btn.play-btn:hover { background: #d4eb00; }

  .time-display { font-family: 'DM Mono', monospace; font-size: 12px; color: var(--text2); white-space: nowrap; }
  .time-sep { color: var(--text3); }

  #seek-bar-wrap { flex: 1; display: flex; align-items: center; gap: 8px; }
  #seek-bar {
    flex: 1; -webkit-appearance: none; height: 4px; border-radius: 2px;
    background: var(--bg4); cursor: pointer; outline: none;
  }
  #seek-bar::-webkit-slider-thumb {
    -webkit-appearance: none; width: 14px; height: 14px; border-radius: 50%;
    background: var(--accent); cursor: pointer; border: 2px solid #000;
  }

  .vol-wrap { display: flex; align-items: center; gap: 6px; }
  .vol-icon { color: var(--text3); font-size: 14px; }
  #vol-bar {
    width: 70px; -webkit-appearance: none; height: 3px; border-radius: 2px;
    background: var(--bg4); cursor: pointer; outline: none;
  }
  #vol-bar::-webkit-slider-thumb {
    -webkit-appearance: none; width: 12px; height: 12px; border-radius: 50%;
    background: var(--text2); cursor: pointer;
  }

  .speed-wrap { display: flex; align-items: center; gap: 5px; }
  .speed-label { color: var(--text3); font-size: 11px; }
  #speed-select {
    background: var(--bg3); border: 1px solid var(--border); border-radius: 5px;
    color: var(--text); font-family: 'DM Mono', monospace; font-size: 11px;
    padding: 3px 6px; cursor: pointer; outline: none;
  }

  /* ── RIGHT PANEL ─────────────────────────────────── */
  #right-panel {
    width: var(--prop-w);
    background: var(--bg2);
    border-left: 1px solid var(--border);
    display: flex; flex-direction: column;
    overflow: hidden;
  }
  .prop-header {
    padding: 14px 16px; border-bottom: 1px solid var(--border);
    font-size: 11px; font-weight: 700; letter-spacing: 1px;
    text-transform: uppercase; color: var(--text3);
  }
  .prop-body { flex: 1; overflow-y: auto; padding: 14px 16px; scrollbar-width: thin; scrollbar-color: var(--border2) transparent; }

  .prop-section { margin-bottom: 20px; }
  .prop-section-title { font-size: 10px; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; color: var(--text3); margin-bottom: 10px; }

  .prop-row { display: flex; align-items: center; justify-content: space-between; margin-bottom: 10px; }
  .prop-label { font-size: 11px; color: var(--text2); }
  .prop-val { font-family: 'DM Mono', monospace; font-size: 11px; color: var(--accent); }

  .slider-wrap { width: 100%; margin-bottom: 10px; }
  .slider-label-row { display: flex; justify-content: space-between; margin-bottom: 4px; }
  .slider-label { font-size: 11px; color: var(--text2); }
  .slider-val { font-size: 11px; color: var(--accent); font-family: 'DM Mono', monospace; }
  .prop-slider {
    width: 100%; -webkit-appearance: none; height: 3px; border-radius: 2px;
    background: var(--bg4); cursor: pointer; outline: none;
  }
  .prop-slider::-webkit-slider-thumb {
    -webkit-appearance: none; width: 13px; height: 13px; border-radius: 50%;
    background: var(--accent2); cursor: pointer; border: 2px solid #000;
  }

  .prop-input {
    width: 100%; background: var(--bg4); border: 1px solid var(--border);
    border-radius: 6px; padding: 7px 10px; color: var(--text);
    font-family: 'Outfit', sans-serif; font-size: 12px; outline: none;
    transition: border-color .15s; margin-bottom: 8px;
  }
  .prop-input:focus { border-color: var(--accent2); }

  .color-row { display: flex; gap: 6px; flex-wrap: wrap; margin-bottom: 10px; }
  .color-swatch {
    width: 24px; height: 24px; border-radius: 5px; cursor: pointer;
    border: 2px solid transparent; transition: all .15s;
  }
  .color-swatch:hover, .color-swatch.active { border-color: var(--accent); transform: scale(1.1); }

  .btn-small {
    padding: 6px 12px; border-radius: 6px; border: 1px solid var(--border);
    background: var(--bg4); color: var(--text2); cursor: pointer; font-size: 11px;
    font-family: 'Outfit', sans-serif; transition: all .15s;
  }
  .btn-small:hover { background: var(--bg3); color: var(--text); border-color: var(--border2); }
  .btn-small.danger { border-color: var(--red); color: var(--red); }
  .btn-small.danger:hover { background: rgba(255,68,68,.1); }
  .btn-row { display: flex; gap: 6px; flex-wrap: wrap; }

  /* ── TIMELINE ────────────────────────────────────── */
  #timeline-area {
    height: var(--timeline-h);
    background: var(--bg2);
    border-top: 1px solid var(--border);
    display: flex; flex-direction: column;
    overflow: hidden;
  }
  #timeline-toolbar {
    display: flex; align-items: center; gap: 8px;
    padding: 6px 12px; border-bottom: 1px solid var(--border);
  }
  .tl-btn {
    padding: 4px 10px; border-radius: 5px; border: 1px solid var(--border);
    background: var(--bg4); color: var(--text2); cursor: pointer;
    font-size: 11px; font-family: 'Outfit', sans-serif;
    transition: all .15s; display: flex; align-items: center; gap: 4px;
  }
  .tl-btn:hover { background: var(--bg3); color: var(--text); }
  .tl-btn.accent { background: rgba(124,106,245,.15); border-color: var(--accent2); color: var(--accent2); }

  .zoom-wrap { display: flex; align-items: center; gap: 6px; margin-left: auto; }
  .zoom-label { font-size: 11px; color: var(--text3); }
  #zoom-slider {
    width: 80px; -webkit-appearance: none; height: 3px; border-radius: 2px;
    background: var(--bg4); cursor: pointer; outline: none;
  }
  #zoom-slider::-webkit-slider-thumb {
    -webkit-appearance: none; width: 12px; height: 12px; border-radius: 50%;
    background: var(--text2); cursor: pointer;
  }

  #timeline-body {
    display: flex; flex: 1; overflow: hidden;
  }
  #track-labels {
    width: 90px; flex-shrink: 0; overflow: hidden;
    border-right: 1px solid var(--border);
  }
  .track-label {
    height: 40px; display: flex; align-items: center; padding: 0 10px;
    font-size: 10px; font-weight: 700; letter-spacing: .5px;
    text-transform: uppercase; color: var(--text3);
    border-bottom: 1px solid var(--border);
  }

  #timeline-scroll {
    flex: 1; overflow-x: auto; overflow-y: hidden;
    scrollbar-width: thin; scrollbar-color: var(--border2) transparent;
    position: relative;
  }
  #timeline-inner {
    position: relative;
    min-width: 100%;
  }
  #ruler {
    height: 20px; background: var(--bg3); border-bottom: 1px solid var(--border);
    position: sticky; top: 0; z-index: 10;
    overflow: hidden;
  }
  #ruler canvas { display: block; }

  .track-row {
    height: 40px; border-bottom: 1px solid var(--border);
    position: relative; background: var(--bg2);
  }
  .track-row:hover { background: rgba(255,255,255,.015); }

  .clip-block {
    position: absolute; top: 4px; height: 32px; border-radius: 5px;
    cursor: pointer; overflow: hidden; display: flex; align-items: center;
    padding: 0 8px; font-size: 10px; font-weight: 600;
    white-space: nowrap; text-overflow: ellipsis;
    border: 1px solid rgba(255,255,255,.1);
    transition: border-color .15s;
    user-select: none;
  }
  .clip-block:hover { border-color: var(--accent) !important; }
  .clip-block.selected { border-color: var(--accent) !important; box-shadow: 0 0 0 1px var(--accent); }
  .clip-block.video-clip { background: var(--clip-video); }
  .clip-block.audio-clip { background: var(--clip-audio); }
  .clip-block.text-clip { background: var(--clip-text); }

  .clip-waveform {
    position: absolute; inset: 6px 4px;
    opacity: .35;
    display: flex; align-items: center; gap: 1px;
  }
  .waveform-bar { flex: 1; background: var(--green); border-radius: 1px; }

  /* Playhead */
  #playhead {
    position: absolute; top: 0; bottom: 0; width: 2px;
    background: var(--accent); z-index: 20; pointer-events: none;
    transform: translateX(0);
  }
  #playhead::before {
    content: ''; position: absolute; top: 0; left: 50%; transform: translateX(-50%);
    width: 10px; height: 10px; background: var(--accent);
    clip-path: polygon(50% 100%, 0 0, 100% 0);
  }

  /* ── EXPORT MODAL ────────────────────────────────── */
  #export-modal {
    display: none; position: fixed; inset: 0;
    background: rgba(0,0,0,.7); z-index: 1000;
    align-items: center; justify-content: center;
    backdrop-filter: blur(8px);
  }
  #export-modal.open { display: flex; }
  .modal-box {
    background: var(--bg3); border: 1px solid var(--border2);
    border-radius: 14px; padding: 28px; width: 380px;
    box-shadow: 0 32px 80px rgba(0,0,0,.6);
  }
  .modal-title {
    font-family: 'Bebas Neue', sans-serif; font-size: 28px; letter-spacing: 2px;
    color: var(--accent); margin-bottom: 20px;
  }
  .modal-row { margin-bottom: 14px; }
  .modal-label { font-size: 11px; color: var(--text3); text-transform: uppercase; letter-spacing: .5px; margin-bottom: 6px; }
  .modal-select, .modal-input {
    width: 100%; background: var(--bg4); border: 1px solid var(--border);
    border-radius: 7px; padding: 8px 12px; color: var(--text);
    font-family: 'Outfit', sans-serif; font-size: 13px; outline: none; cursor: pointer;
  }
  .resolution-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 6px; }
  .res-btn {
    padding: 8px; border-radius: 7px; border: 1px solid var(--border);
    background: var(--bg4); color: var(--text2); cursor: pointer; text-align: center;
    font-size: 11px; font-family: 'Outfit', sans-serif; transition: all .15s;
  }
  .res-btn:hover, .res-btn.active { border-color: var(--accent2); background: rgba(124,106,245,.15); color: var(--text); }
  .modal-btns { display: flex; gap: 10px; margin-top: 22px; }
  .modal-cancel {
    flex: 1; padding: 10px; border-radius: 8px; border: 1px solid var(--border);
    background: transparent; color: var(--text2); cursor: pointer;
    font-family: 'Outfit', sans-serif; font-size: 13px;
  }
  .modal-export-btn {
    flex: 2; padding: 10px; border-radius: 8px; border: none;
    background: var(--accent); color: #000; cursor: pointer;
    font-family: 'Outfit', sans-serif; font-size: 13px; font-weight: 700;
  }
  .modal-export-btn:hover { background: #d4eb00; }

  .progress-bar-wrap { margin-top: 12px; display: none; }
  .progress-bar-bg { background: var(--bg4); border-radius: 100px; height: 6px; overflow: hidden; }
  .progress-bar-fill { height: 100%; background: var(--accent); border-radius: 100px; width: 0; transition: width .3s; }
  .progress-text { font-size: 11px; color: var(--text2); margin-top: 6px; }

  /* ── TEXT EDITOR MODAL ───────────────────────────── */
  #text-modal {
    display: none; position: fixed; inset: 0;
    background: rgba(0,0,0,.6); z-index: 900;
    align-items: center; justify-content: center;
    backdrop-filter: blur(6px);
  }
  #text-modal.open { display: flex; }
  .text-modal-box {
    background: var(--bg3); border: 1px solid var(--border2);
    border-radius: 14px; padding: 24px; width: 340px;
  }
  .text-modal-box h3 { font-size: 16px; font-weight: 600; margin-bottom: 16px; }
  .text-modal-box textarea {
    width: 100%; background: var(--bg4); border: 1px solid var(--border);
    border-radius: 7px; padding: 10px; color: var(--text);
    font-family: 'Outfit', sans-serif; font-size: 13px; outline: none;
    resize: none; height: 80px; margin-bottom: 12px;
  }

  /* ── AI TOOLS TOAST ──────────────────────────────── */
  #toast {
    position: fixed; bottom: calc(var(--timeline-h) + 16px); left: 50%;
    transform: translateX(-50%) translateY(20px);
    background: var(--bg3); border: 1px solid var(--border2);
    border-radius: 8px; padding: 10px 18px; font-size: 12px; color: var(--text);
    opacity: 0; pointer-events: none; transition: all .3s; z-index: 500;
  }
  #toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

  /* scrollbar */
  ::-webkit-scrollbar { width: 5px; height: 5px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 10px; }

  /* AI badge */
  .ai-badge {
    font-size: 9px; font-weight: 700; letter-spacing: .5px;
    background: var(--accent2); color: #fff; border-radius: 3px;
    padding: 1px 5px; text-transform: uppercase;
  }
</style>
</head>
<body>

<!-- HEADER -->
<div id="header">
  <div class="logo">CUT<span>LAB</span></div>
  <div class="menu-btns">
    <button class="menu-btn" onclick="document.getElementById('file-input').click()">File</button>
    <button class="menu-btn" onclick="undo()">Edit</button>
    <button class="menu-btn">View</button>
  </div>
  <div class="header-center">
    <button class="tool-btn" title="Split at playhead" onclick="splitAtPlayhead()">✂</button>
    <button class="tool-btn" title="Delete selected" onclick="deleteSelected()">🗑</button>
    <button class="tool-btn" title="Undo" onclick="undo()">↩</button>
    <button class="tool-btn" title="Redo">↪</button>
    <div style="width:1px;height:24px;background:var(--border);margin:0 4px;"></div>
    <button class="tool-btn" title="Add text" onclick="openTextModal()">T</button>
    <button class="tool-btn" title="Add audio" onclick="showToast('Drag audio files from the Media panel')">♫</button>
    <button class="tool-btn" title="Crop / Mask">⬜</button>
    <button class="tool-btn" title="Keyframe" onclick="showToast('Keyframe added at current time')">◆</button>
  </div>
  <div class="header-right">
    <span style="font-size:11px;color:var(--text3);">Draft saved</span>
    <button class="export-btn" onclick="openExport()">▶ Export</button>
  </div>
</div>

<!-- MAIN AREA -->
<div id="main">

  <!-- LEFT PANEL -->
  <div id="left-panel">
    <div class="panel-tabs">
      <div class="panel-tab active" onclick="switchPanel('media',this)">Media</div>
      <div class="panel-tab" onclick="switchPanel('effects',this)">FX</div>
      <div class="panel-tab" onclick="switchPanel('filters',this)">Filters</div>
      <div class="panel-tab" onclick="switchPanel('text',this)">Text</div>
      <div class="panel-tab" onclick="switchPanel('audio',this)">Audio</div>
      <div class="panel-tab" onclick="switchPanel('ai',this)">AI</div>
    </div>

    <!-- MEDIA -->
    <div class="panel-content" id="panel-media">
      <div class="upload-zone" onclick="document.getElementById('file-input').click()" id="upload-zone">
        <div class="icon">📁</div>
        <p><strong>Click or drop</strong> video/image files here</p>
      </div>
      <div class="media-grid" id="media-grid"></div>
    </div>

    <!-- EFFECTS -->
    <div class="panel-content" id="panel-effects" style="display:none">
      <div style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px;">Trending Effects</div>
      <div class="effects-grid">
        <div class="effect-item" onclick="applyEffect('glitch',this)"><span class="eicon">⚡</span>Glitch</div>
        <div class="effect-item" onclick="applyEffect('blur',this)"><span class="eicon">🌀</span>Blur</div>
        <div class="effect-item" onclick="applyEffect('shake',this)"><span class="eicon">📳</span>Shake</div>
        <div class="effect-item" onclick="applyEffect('zoom',this)"><span class="eicon">🔍</span>Zoom</div>
        <div class="effect-item" onclick="applyEffect('flash',this)"><span class="eicon">💫</span>Flash</div>
        <div class="effect-item" onclick="applyEffect('mirror',this)"><span class="eicon">🪞</span>Mirror</div>
        <div class="effect-item" onclick="applyEffect('rgb',this)"><span class="eicon">🎨</span>RGB Split</div>
        <div class="effect-item" onclick="applyEffect('vhs',this)"><span class="eicon">📼</span>VHS</div>
        <div class="effect-item" onclick="applyEffect('grain',this)"><span class="eicon">🌾</span>Film Grain</div>
        <div class="effect-item" onclick="applyEffect('none',this)"><span class="eicon">✕</span>None</div>
      </div>
    </div>

    <!-- FILTERS -->
    <div class="panel-content" id="panel-filters" style="display:none">
      <div style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px;">Cinematic Filters</div>
      <div class="filter-item active" onclick="applyFilter('none',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#666,#999)"></div>
        <span class="filter-name">Original</span>
      </div>
      <div class="filter-item" onclick="applyFilter('chrome',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#c8a882,#7fa8c8)"></div>
        <span class="filter-name">Chrome</span>
      </div>
      <div class="filter-item" onclick="applyFilter('fade',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#c2b9a7,#a7b4c2)"></div>
        <span class="filter-name">Fade</span>
      </div>
      <div class="filter-item" onclick="applyFilter('noir',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#222,#888)"></div>
        <span class="filter-name">Noir</span>
      </div>
      <div class="filter-item" onclick="applyFilter('warm',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#c8822a,#c8a042)"></div>
        <span class="filter-name">Golden Hour</span>
      </div>
      <div class="filter-item" onclick="applyFilter('cold',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#2a5ac8,#42a8c8)"></div>
        <span class="filter-name">Arctic</span>
      </div>
      <div class="filter-item" onclick="applyFilter('vintage',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#8b6914,#c8a87a)"></div>
        <span class="filter-name">Vintage</span>
      </div>
      <div class="filter-item" onclick="applyFilter('green',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#1a5c2a,#4a8c42)"></div>
        <span class="filter-name">Forest</span>
      </div>
      <div class="filter-item" onclick="applyFilter('dramatic',this)">
        <div class="filter-preview" style="background:linear-gradient(135deg,#1a0a0a,#6a1a2a)"></div>
        <span class="filter-name">Dramatic</span>
      </div>
    </div>

    <!-- TEXT -->
    <div class="panel-content" id="panel-text" style="display:none">
      <div style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px;">Add Text</div>
      <div class="text-styles">
        <div class="text-style-btn" onclick="addTextOverlay('Title','48px','Bebas Neue','#FFFFFF')">
          <div style="font-family:'Bebas Neue';font-size:18px;color:#fff;">TITLE</div>
          <div style="font-size:10px;color:var(--text3);margin-left:auto;">Heading</div>
        </div>
        <div class="text-style-btn" onclick="addTextOverlay('Subtitle','22px','Outfit','#FFFFFF')">
          <div style="font-size:14px;font-weight:500;color:#fff;">Subtitle</div>
          <div style="font-size:10px;color:var(--text3);margin-left:auto;">Sub</div>
        </div>
        <div class="text-style-btn" onclick="addTextOverlay('Caption text here','14px','Outfit','#cccccc')">
          <div style="font-size:12px;color:#ccc;">Caption</div>
          <div style="font-size:10px;color:var(--text3);margin-left:auto;">Caption</div>
        </div>
        <div class="text-style-btn" onclick="addTextOverlay('LABEL','12px','DM Mono','#E8FF47')">
          <div style="font-family:'DM Mono';font-size:11px;color:#E8FF47;border:1px solid #E8FF47;padding:2px 6px;border-radius:3px;">LABEL</div>
          <div style="font-size:10px;color:var(--text3);margin-left:auto;">Tag</div>
        </div>
      </div>
      <div style="margin-top:14px;">
        <button class="btn-small" style="width:100%;text-align:center;" onclick="openTextModal()">+ Custom Text</button>
      </div>
    </div>

    <!-- AUDIO -->
    <div class="panel-content" id="panel-audio" style="display:none">
      <div style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px;">Music Library</div>
      <div class="audio-item" onclick="addAudioTrack('Cinematic Epic','3:42')">
        <div class="audio-play">▶</div>
        <div class="audio-info">
          <div class="audio-name">Cinematic Epic</div>
          <div class="audio-meta">3:42 · Orchestral</div>
        </div>
      </div>
      <div class="audio-item" onclick="addAudioTrack('Lo-Fi Beats','2:18')">
        <div class="audio-play">▶</div>
        <div class="audio-info">
          <div class="audio-name">Lo-Fi Beats</div>
          <div class="audio-meta">2:18 · Electronic</div>
        </div>
      </div>
      <div class="audio-item" onclick="addAudioTrack('Dark Ambient','5:10')">
        <div class="audio-play">▶</div>
        <div class="audio-info">
          <div class="audio-name">Dark Ambient</div>
          <div class="audio-meta">5:10 · Atmospheric</div>
        </div>
      </div>
      <div class="audio-item" onclick="addAudioTrack('Upbeat Pop','2:55')">
        <div class="audio-play">▶</div>
        <div class="audio-info">
          <div class="audio-name">Upbeat Pop</div>
          <div class="audio-meta">2:55 · Pop</div>
        </div>
      </div>
      <div class="audio-item" onclick="addAudioTrack('Documentary Score','4:20')">
        <div class="audio-play">▶</div>
        <div class="audio-info">
          <div class="audio-name">Documentary Score</div>
          <div class="audio-meta">4:20 · Cinematic</div>
        </div>
      </div>
      <div style="margin-top:10px;">
        <button class="btn-small" style="width:100%;text-align:center;" onclick="document.getElementById('audio-input').click()">+ Import Audio</button>
      </div>
    </div>

    <!-- AI PANEL -->
    <div class="panel-content" id="panel-ai" style="display:none">
      <div style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:.5px;margin-bottom:10px;">AI Tools <span class="ai-badge">Beta</span></div>
      <div class="effects-grid">
        <div class="effect-item" onclick="showToast('🤖 Auto-captioning your video...')"><span class="eicon">💬</span>Auto Caption</div>
        <div class="effect-item" onclick="showToast('🤖 Removing background...')"><span class="eicon">✂️</span>BG Remove</div>
        <div class="effect-item" onclick="showToast('🤖 Detecting faces...')"><span class="eicon">🎯</span>Face Track</div>
        <div class="effect-item" onclick="showToast('🤖 Applying stabilizer...')"><span class="eicon">📷</span>Stabilize</div>
        <div class="effect-item" onclick="showToast('🤖 Generating voiceover...')"><span class="eicon">🎤</span>TTS Voice</div>
        <div class="effect-item" onclick="showToast('🤖 Noise reduced!')"><span class="eicon">🔇</span>Denoise</div>
        <div class="effect-item" onclick="showToast('🤖 Enhancing colors...')"><span class="eicon">🌈</span>Auto Color</div>
        <div class="effect-item" onclick="showToast('🤖 Detecting highlights...')"><span class="eicon">⭐</span>Highlights</div>
      </div>
    </div>
  </div>

  <!-- CENTER PREVIEW -->
  <div id="center">
    <div id="preview-area" id="preview-drop"
      ondragover="event.preventDefault()"
      ondrop="handleDrop(event)">
      <div id="drop-hint">
        <div class="big-icon">🎬</div>
        <h3>Drop a video to start editing</h3>
        <p>or click <strong style="color:var(--accent)">File → Import</strong> from the Media panel</p>
      </div>
      <div id="video-container" style="display:none;position:relative;max-width:90%;max-height:90%;">
        <video id="main-video" style="display:block;max-width:100%;max-height:calc(100vh - var(--header-h) - var(--timeline-h) - 120px);border-radius:4px;" playsinline></video>
        <div id="text-overlays"></div>
        <div id="filter-overlay"></div>
      </div>
    </div>

    <!-- PLAYBACK CONTROLS -->
    <div id="playback-controls">
      <button class="ctrl-btn" title="Go to start" onclick="seekTo(0)">⏮</button>
      <button class="ctrl-btn" title="Frame back" onclick="frameStep(-1)">◁</button>
      <button class="ctrl-btn play-btn" id="play-btn" onclick="togglePlay()">▶</button>
      <button class="ctrl-btn" title="Frame forward" onclick="frameStep(1)">▷</button>
      <button class="ctrl-btn" title="Go to end" onclick="seekToEnd()">⏭</button>

      <span class="time-display" id="time-display">0:00.000 <span class="time-sep">/</span> 0:00.000</span>

      <div id="seek-bar-wrap">
        <input type="range" id="seek-bar" min="0" max="1000" value="0" oninput="onSeek(this.value)" />
      </div>

      <div class="vol-wrap">
        <span class="vol-icon">🔊</span>
        <input type="range" id="vol-bar" min="0" max="100" value="100" oninput="setVolume(this.value)" />
      </div>

      <div class="speed-wrap">
        <span class="speed-label">Speed</span>
        <select id="speed-select" onchange="setSpeed(this.value)">
          <option value="0.25">0.25x</option>
          <option value="0.5">0.5x</option>
          <option value="0.75">0.75x</option>
          <option value="1" selected>1x</option>
          <option value="1.25">1.25x</option>
          <option value="1.5">1.5x</option>
          <option value="2">2x</option>
        </select>
      </div>
    </div>
  </div>

  <!-- RIGHT PANEL -->
  <div id="right-panel">
    <div class="prop-header">Properties</div>
    <div class="prop-body" id="prop-body">

      <div class="prop-section" id="video-props">
        <div class="prop-section-title">Video</div>
        <div class="prop-row"><span class="prop-label">Resolution</span><span class="prop-val" id="p-res">—</span></div>
        <div class="prop-row"><span class="prop-label">Duration</span><span class="prop-val" id="p-dur">—</span></div>
        <div class="prop-row"><span class="prop-label">FPS</span><span class="prop-val" id="p-fps">—</span></div>
      </div>

      <div class="prop-section">
        <div class="prop-section-title">Color Grading</div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Brightness</span><span class="slider-val" id="v-bright-val">0</span></div>
          <input type="range" class="prop-slider" min="-100" max="100" value="0" id="s-bright" oninput="updateVideoStyle()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Contrast</span><span class="slider-val" id="v-cont-val">0</span></div>
          <input type="range" class="prop-slider" min="-100" max="100" value="0" id="s-cont" oninput="updateVideoStyle()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Saturation</span><span class="slider-val" id="v-sat-val">0</span></div>
          <input type="range" class="prop-slider" min="-100" max="100" value="0" id="s-sat" oninput="updateVideoStyle()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Warmth</span><span class="slider-val" id="v-warm-val">0</span></div>
          <input type="range" class="prop-slider" min="-100" max="100" value="0" id="s-warm" oninput="updateVideoStyle()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Vignette</span><span class="slider-val" id="v-vig-val">0</span></div>
          <input type="range" class="prop-slider" min="0" max="100" value="0" id="s-vig" oninput="updateVideoStyle()">
        </div>
      </div>

      <div class="prop-section">
        <div class="prop-section-title">Transform</div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Scale</span><span class="slider-val" id="v-scale-val">100%</span></div>
          <input type="range" class="prop-slider" min="50" max="200" value="100" id="s-scale" oninput="updateTransform()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Rotation</span><span class="slider-val" id="v-rot-val">0°</span></div>
          <input type="range" class="prop-slider" min="-180" max="180" value="0" id="s-rot" oninput="updateTransform()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Opacity</span><span class="slider-val" id="v-op-val">100%</span></div>
          <input type="range" class="prop-slider" min="0" max="100" value="100" id="s-op" oninput="updateTransform()">
        </div>
      </div>

      <div class="prop-section">
        <div class="prop-section-title">Clip Actions</div>
        <div class="btn-row">
          <button class="btn-small" onclick="splitAtPlayhead()">✂ Split</button>
          <button class="btn-small" onclick="reverseClip()">↩ Reverse</button>
          <button class="btn-small" onclick="freezeFrame()">⏸ Freeze</button>
          <button class="btn-small danger" onclick="deleteSelected()">🗑 Delete</button>
        </div>
      </div>

      <div class="prop-section">
        <div class="prop-section-title">Trim</div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">In Point</span><span class="slider-val" id="trim-in-val">0s</span></div>
          <input type="range" class="prop-slider" min="0" max="100" value="0" id="trim-in" oninput="updateTrim()">
        </div>
        <div class="slider-wrap">
          <div class="slider-label-row"><span class="slider-label">Out Point</span><span class="slider-val" id="trim-out-val">100%</span></div>
          <input type="range" class="prop-slider" min="0" max="100" value="100" id="trim-out" oninput="updateTrim()">
        </div>
      </div>

    </div>
  </div>
</div>

<!-- TIMELINE -->
<div id="timeline-area">
  <div id="timeline-toolbar">
    <button class="tl-btn accent" onclick="document.getElementById('file-input').click()">+ Import</button>
    <button class="tl-btn" onclick="splitAtPlayhead()">✂ Split</button>
    <button class="tl-btn" onclick="deleteSelected()">🗑 Delete</button>
    <button class="tl-btn" onclick="showToast('Transition added')">≋ Transition</button>
    <button class="tl-btn" onclick="showToast('Keyframe added')">◆ Keyframe</button>
    <div class="zoom-wrap">
      <span class="zoom-label">Zoom</span>
      <input type="range" id="zoom-slider" min="1" max="5" step="0.1" value="2" oninput="updateZoom(this.value)">
    </div>
  </div>
  <div id="timeline-body">
    <div id="track-labels">
      <div class="track-label" style="height:20px;"></div>
      <div class="track-label" style="color:#6a9fd8;">Video 1</div>
      <div class="track-label" style="color:#6ad89a;">Audio 1</div>
      <div class="track-label" style="color:#b09ad8;">Text</div>
      <div class="track-label" style="color:#6a9fd8;">Video 2</div>
    </div>
    <div id="timeline-scroll" onclick="handleTimelineClick(event)">
      <div id="timeline-inner" style="width:2000px;position:relative;">
        <div id="ruler"><canvas id="ruler-canvas" height="20"></canvas></div>
        <div class="track-row" id="track-video1" style="height:40px;"></div>
        <div class="track-row" id="track-audio1" style="height:40px;"></div>
        <div class="track-row" id="track-text1" style="height:40px;"></div>
        <div class="track-row" id="track-video2" style="height:40px;"></div>
        <div id="playhead"></div>
      </div>
    </div>
  </div>
</div>

<!-- EXPORT MODAL -->
<div id="export-modal">
  <div class="modal-box">
    <div class="modal-title">Export Video</div>
    <div class="modal-row">
      <div class="modal-label">Resolution</div>
      <div class="resolution-grid">
        <div class="res-btn" onclick="setRes(this,'720p')">720p</div>
        <div class="res-btn active" onclick="setRes(this,'1080p')">1080p</div>
        <div class="res-btn" onclick="setRes(this,'4K')">4K <span style="font-size:9px;color:var(--accent2)">PRO</span></div>
      </div>
    </div>
    <div class="modal-row">
      <div class="modal-label">Format</div>
      <select class="modal-select" id="export-format">
        <option>MP4 (H.264)</option>
        <option>MOV (ProRes)</option>
        <option>WebM (VP9)</option>
        <option>GIF</option>
      </select>
    </div>
    <div class="modal-row">
      <div class="modal-label">Frame Rate</div>
      <select class="modal-select" id="export-fps">
        <option>24 fps</option>
        <option selected>30 fps</option>
        <option>60 fps</option>
      </select>
    </div>
    <div class="modal-row">
      <div class="modal-label">Quality</div>
      <select class="modal-select" id="export-quality">
        <option>High (recommended)</option>
        <option>Medium</option>
        <option>Low (fast)</option>
      </select>
    </div>
    <div class="progress-bar-wrap" id="export-progress">
      <div class="progress-bar-bg"><div class="progress-bar-fill" id="export-fill"></div></div>
      <div class="progress-text" id="export-text">Preparing export...</div>
    </div>
    <div class="modal-btns">
      <button class="modal-cancel" onclick="closeExport()">Cancel</button>
      <button class="modal-export-btn" onclick="startExport()">Export Now</button>
    </div>
  </div>
</div>

<!-- TEXT MODAL -->
<div id="text-modal">
  <div class="text-modal-box">
    <h3>Add Text</h3>
    <textarea id="text-input" placeholder="Enter your text...">Your Text Here</textarea>
    <div style="margin-bottom:10px;">
      <div class="modal-label" style="margin-bottom:4px;">Font Size</div>
      <input type="range" class="prop-slider" min="12" max="120" value="36" id="text-size" style="width:100%">
    </div>
    <div style="margin-bottom:10px;">
      <div class="modal-label" style="margin-bottom:6px;">Color</div>
      <div class="color-row">
        <div class="color-swatch active" style="background:#ffffff" onclick="setTextColor('#ffffff',this)"></div>
        <div class="color-swatch" style="background:#E8FF47" onclick="setTextColor('#E8FF47',this)"></div>
        <div class="color-swatch" style="background:#ff5c87" onclick="setTextColor('#ff5c87',this)"></div>
        <div class="color-swatch" style="background:#7c6af5" onclick="setTextColor('#7c6af5',this)"></div>
        <div class="color-swatch" style="background:#44ff88" onclick="setTextColor('#44ff88',this)"></div>
        <div class="color-swatch" style="background:#ff8844" onclick="setTextColor('#ff8844',this)"></div>
        <div class="color-swatch" style="background:#000000;border-color:var(--border2)!important" onclick="setTextColor('#000000',this)"></div>
      </div>
    </div>
    <div class="modal-btns">
      <button class="modal-cancel" onclick="document.getElementById('text-modal').classList.remove('open')">Cancel</button>
      <button class="modal-export-btn" onclick="confirmAddText()">Add Text</button>
    </div>
  </div>
</div>

<!-- TOAST -->
<div id="toast"></div>

<!-- FILE INPUTS -->
<input type="file" id="file-input" accept="video/*,image/*" multiple style="display:none" onchange="handleFiles(this.files)">
<input type="file" id="audio-input" accept="audio/*" style="display:none" onchange="handleAudioFile(this.files[0])">

<script>
// ── STATE ─────────────────────────────────────────────────────────────────────
const state = {
  clips: [],
  selectedClip: null,
  textColor: '#ffffff',
  currentFilter: 'none',
  currentEffect: 'none',
  zoom: 2,
  playing: false,
  duration: 0,
};

// ── VIDEO ELEMENT ─────────────────────────────────────────────────────────────
const video = document.getElementById('main-video');
const playBtn = document.getElementById('play-btn');
const seekBar = document.getElementById('seek-bar');
const timeDisplay = document.getElementById('time-display');
const dropHint = document.getElementById('drop-hint');
const videoContainer = document.getElementById('video-container');
const filterOverlay = document.getElementById('filter-overlay');

// ── FILE HANDLING ─────────────────────────────────────────────────────────────
function handleFiles(files) {
  Array.from(files).forEach(f => {
    if (f.type.startsWith('video/') || f.type.startsWith('image/')) {
      addMedia(f);
    }
  });
}

function handleDrop(e) {
  e.preventDefault();
  handleFiles(e.dataTransfer.files);
}

function addMedia(file) {
  const url = URL.createObjectURL(file);
  const isVideo = file.type.startsWith('video/');

  // Add to media grid
  const grid = document.getElementById('media-grid');
  const thumb = document.createElement('div');
  thumb.className = 'media-thumb';
  if (isVideo) {
    const v = document.createElement('video');
    v.src = url; v.muted = true;
    v.addEventListener('loadedmetadata', () => {
      const dur = document.createElement('div');
      dur.className = 'dur';
      dur.textContent = formatTime(v.duration);
      thumb.appendChild(dur);
    });
    thumb.appendChild(v);
  } else {
    const img = document.createElement('img');
    img.src = url;
    thumb.appendChild(img);
  }
  thumb.onclick = () => loadClip(url, file.name, isVideo);
  grid.insertBefore(thumb, grid.firstChild);

  // Auto load first
  if (!video.src) loadClip(url, file.name, isVideo);
}

function loadClip(url, name, isVideo) {
  if (!isVideo) return;
  video.src = url;
  video.load();
  video.addEventListener('loadedmetadata', () => {
    state.duration = video.duration;
    dropHint.style.display = 'none';
    videoContainer.style.display = 'flex';
    video.style.display = 'block';
    document.getElementById('p-dur').textContent = formatTime(video.duration);
    document.getElementById('p-fps').textContent = '30 fps';
    document.getElementById('p-res').textContent = video.videoWidth + '×' + video.videoHeight;
    document.getElementById('trim-out').max = 100;
    addClipToTimeline(name, video.duration, 'video');
    showToast('✅ ' + name + ' loaded');
  }, { once: true });
}

// ── PLAYBACK ──────────────────────────────────────────────────────────────────
function togglePlay() {
  if (!video.src) return;
  if (video.paused) { video.play(); playBtn.textContent = '⏸'; state.playing = true; }
  else { video.pause(); playBtn.textContent = '▶'; state.playing = false; }
}

video.addEventListener('timeupdate', () => {
  if (!video.duration) return;
  const pct = video.currentTime / video.duration;
  seekBar.value = pct * 1000;
  updateTimeDisplay();
  updatePlayhead(pct);
});

video.addEventListener('ended', () => { playBtn.textContent = '▶'; state.playing = false; });

function onSeek(val) {
  if (!video.duration) return;
  video.currentTime = (val / 1000) * video.duration;
}

function seekTo(t) { video.currentTime = t; }
function seekToEnd() { video.currentTime = video.duration; }
function frameStep(dir) { video.pause(); video.currentTime = Math.max(0, video.currentTime + dir * (1/30)); playBtn.textContent = '▶'; }
function setVolume(v) { video.volume = v / 100; }
function setSpeed(v) { video.playbackRate = parseFloat(v); }

function updateTimeDisplay() {
  timeDisplay.innerHTML = formatTime(video.currentTime) + ' <span class="time-sep">/</span> ' + formatTime(video.duration || 0);
}

function formatTime(s) {
  if (!s || isNaN(s)) return '0:00.000';
  const m = Math.floor(s / 60);
  const sec = (s % 60).toFixed(3).padStart(6, '0');
  return m + ':' + sec;
}

// ── VIDEO STYLE (Color Grading) ───────────────────────────────────────────────
const filterMap = {
  none: '',
  chrome: 'contrast(1.1) saturate(0.85) hue-rotate(-10deg)',
  fade: 'contrast(0.85) saturate(0.7) brightness(1.1)',
  noir: 'grayscale(1) contrast(1.2)',
  warm: 'sepia(0.3) saturate(1.4) hue-rotate(-20deg)',
  cold: 'saturate(0.9) hue-rotate(30deg) brightness(1.05)',
  vintage: 'sepia(0.5) contrast(0.9) brightness(0.9)',
  green: 'saturate(1.3) hue-rotate(80deg) brightness(0.95)',
  dramatic: 'contrast(1.4) saturate(0.6) brightness(0.8)',
};

function updateVideoStyle() {
  const bright = +document.getElementById('s-bright').value;
  const cont = +document.getElementById('s-cont').value;
  const sat = +document.getElementById('s-sat').value;
  const warm = +document.getElementById('s-warm').value;

  document.getElementById('v-bright-val').textContent = bright;
  document.getElementById('v-cont-val').textContent = cont;
  document.getElementById('v-sat-val').textContent = sat;
  document.getElementById('v-warm-val').textContent = warm;

  const vignette = +document.getElementById('s-vig').value;
  document.getElementById('v-vig-val').textContent = vignette;

  const baseFilter = filterMap[state.currentFilter] || '';
  const brightF = `brightness(${1 + bright/100})`;
  const contF = `contrast(${1 + cont/200})`;
  const satF = `saturate(${1 + sat/100})`;
  const warmF = warm > 0 ? `sepia(${warm/200})` : '';
  video.style.filter = [baseFilter, brightF, contF, satF, warmF].filter(Boolean).join(' ');

  // Vignette via overlay
  if (vignette > 0) {
    filterOverlay.style.background = `radial-gradient(ellipse at center, transparent ${100 - vignette}%, rgba(0,0,0,${vignette/100}) 100%)`;
  } else {
    filterOverlay.style.background = '';
  }
}

function updateTransform() {
  const scale = +document.getElementById('s-scale').value;
  const rot = +document.getElementById('s-rot').value;
  const op = +document.getElementById('s-op').value;
  document.getElementById('v-scale-val').textContent = scale + '%';
  document.getElementById('v-rot-val').textContent = rot + '°';
  document.getElementById('v-op-val').textContent = op + '%';
  video.style.transform = `scale(${scale/100}) rotate(${rot}deg)`;
  video.style.opacity = op / 100;
}

function applyFilter(name, el) {
  document.querySelectorAll('.filter-item').forEach(e => e.classList.remove('active'));
  el.classList.add('active');
  state.currentFilter = name;
  updateVideoStyle();
}

function applyEffect(name, el) {
  document.querySelectorAll('.effect-item').forEach(e => e.classList.remove('active'));
  el.classList.add('active');
  state.currentEffect = name;

  // Remove existing effect styles
  video.style.animation = '';
  document.head.querySelectorAll('style.effect-style').forEach(s => s.remove());

  if (name === 'glitch') {
    injectKeyframes('.glitch-anim', `
      @keyframes glitch { 0%,100%{transform:translate(0)} 25%{transform:translate(-3px,1px) skewX(2deg)} 50%{transform:translate(3px,-1px) skewX(-2deg)} 75%{transform:translate(-1px,2px)} }
    `);
    video.style.animation = 'glitch 0.3s infinite';
  } else if (name === 'shake') {
    injectKeyframes('.shake-anim', `
      @keyframes shake { 0%,100%{transform:translate(0)} 25%{transform:translate(-4px,0)} 75%{transform:translate(4px,0)} }
    `);
    video.style.animation = 'shake 0.1s infinite';
  } else if (name === 'zoom') {
    injectKeyframes('.zoom-anim', `
      @keyframes zoompulse { 0%,100%{transform:scale(1)} 50%{transform:scale(1.05)} }
    `);
    video.style.animation = 'zoompulse 2s ease-in-out infinite';
  } else if (name === 'flash') {
    injectKeyframes('.flash-anim', `
      @keyframes flashblink { 0%,100%{opacity:1} 50%{opacity:0.7} }
    `);
    video.style.animation = 'flashblink 0.5s infinite';
  } else if (name === 'grain') {
    filterOverlay.style.backgroundImage = 'url("data:image/svg+xml,%3Csvg viewBox=\'0 0 200 200\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cfilter id=\'n\'%3E%3CfeTurbulence type=\'fractalNoise\' baseFrequency=\'0.65\' numOctaves=\'3\' stitchTiles=\'stitch\'/%3E%3C/filter%3E%3Crect width=\'100%25\' height=\'100%25\' filter=\'url(%23n)\' opacity=\'0.3\'/%3E%3C/svg%3E")';
    filterOverlay.style.mixBlendMode = 'overlay';
    filterOverlay.style.opacity = '0.4';
  } else if (name === 'none') {
    filterOverlay.style.backgroundImage = '';
    filterOverlay.style.mixBlendMode = '';
    filterOverlay.style.opacity = '';
    video.style.animation = '';
  }
  showToast('Effect: ' + name);
}

function injectKeyframes(className, css) {
  const style = document.createElement('style');
  style.className = 'effect-style';
  style.textContent = css;
  document.head.appendChild(style);
}

// ── TRIM ──────────────────────────────────────────────────────────────────────
function updateTrim() {
  if (!video.duration) return;
  const inPct = +document.getElementById('trim-in').value;
  const outPct = +document.getElementById('trim-out').value;
  const inSec = (inPct / 100) * video.duration;
  const outSec = (outPct / 100) * video.duration;
  document.getElementById('trim-in-val').textContent = inSec.toFixed(1) + 's';
  document.getElementById('trim-out-val').textContent = outPct + '%';
  if (video.currentTime < inSec) video.currentTime = inSec;
}

// ── TIMELINE ──────────────────────────────────────────────────────────────────
let clips = [];
let selectedClipEl = null;
let zoom = 2;

function addClipToTimeline(name, duration, type) {
  const trackEl = document.getElementById('track-' + type + '1');
  const pxPerSec = 60 * zoom;
  const left = 0;
  const width = Math.max(60, duration * pxPerSec);

  const clip = document.createElement('div');
  clip.className = 'clip-block ' + type + '-clip';
  clip.style.left = left + 'px';
  clip.style.width = width + 'px';
  clip.textContent = name.length > 20 ? name.slice(0,18) + '…' : name;
  clip.dataset.duration = duration;
  clip.dataset.type = type;
  clip.dataset.left = left;

  if (type === 'audio') {
    const wv = document.createElement('div');
    wv.className = 'clip-waveform';
    for (let i = 0; i < Math.floor(width / 3); i++) {
      const bar = document.createElement('div');
      bar.className = 'waveform-bar';
      bar.style.height = (20 + Math.random() * 60) + '%';
      wv.appendChild(bar);
    }
    clip.appendChild(wv);
  }

  clip.addEventListener('click', e => {
    e.stopPropagation();
    if (selectedClipEl) selectedClipEl.classList.remove('selected');
    selectedClipEl = clip;
    clip.classList.add('selected');
    state.selectedClip = { el: clip, duration, type, name };
  });

  // Drag within track
  makeDraggableClip(clip, trackEl);

  trackEl.appendChild(clip);
  clips.push({ el: clip, duration, type });
  updateInnerWidth();
  drawRuler();
}

function makeDraggableClip(clip, track) {
  let startX, startLeft;
  clip.addEventListener('mousedown', e => {
    if (e.target !== clip) return;
    startX = e.clientX;
    startLeft = parseInt(clip.style.left) || 0;
    const onMove = mv => {
      const dx = mv.clientX - startX;
      clip.style.left = Math.max(0, startLeft + dx) + 'px';
    };
    const onUp = () => {
      document.removeEventListener('mousemove', onMove);
      document.removeEventListener('mouseup', onUp);
    };
    document.addEventListener('mousemove', onMove);
    document.addEventListener('mouseup', onUp);
    e.preventDefault();
  });
}

function addAudioTrack(name, durStr) {
  const parts = durStr.split(':');
  const dur = parseInt(parts[0]) * 60 + parseInt(parts[1]);
  addClipToTimeline(name, dur, 'audio');
  showToast('🎵 ' + name + ' added to timeline');
}

function splitAtPlayhead() {
  if (!selectedClipEl || !video.duration) {
    showToast('Select a clip to split');
    return;
  }
  const pxPerSec = 60 * zoom;
  const playheadLeft = (video.currentTime / video.duration) * video.duration * pxPerSec;
  const clipLeft = parseInt(selectedClipEl.style.left) || 0;
  const clipW = parseInt(selectedClipEl.style.width) || 100;
  if (playheadLeft <= clipLeft || playheadLeft >= clipLeft + clipW) {
    showToast('Playhead must be inside the clip');
    return;
  }
  const splitW = playheadLeft - clipLeft;
  selectedClipEl.style.width = splitW + 'px';
  const newClip = selectedClipEl.cloneNode(true);
  newClip.style.left = playheadLeft + 'px';
  newClip.style.width = (clipW - splitW) + 'px';
  newClip.textContent = selectedClipEl.textContent + ' (2)';
  newClip.classList.remove('selected');
  makeDraggableClip(newClip, selectedClipEl.parentElement);
  selectedClipEl.parentElement.appendChild(newClip);
  showToast('✂ Clip split at playhead');
}

function deleteSelected() {
  if (!selectedClipEl) { showToast('Select a clip first'); return; }
  selectedClipEl.remove();
  selectedClipEl = null;
  state.selectedClip = null;
  showToast('Clip deleted');
}

function reverseClip() { showToast('↩ Reverse applied (requires export)'); }
function freezeFrame() { if (video.src) video.pause(); showToast('⏸ Frame frozen'); }

function handleTimelineClick(e) {
  const rect = document.getElementById('timeline-scroll').getBoundingClientRect();
  const x = e.clientX - rect.left + document.getElementById('timeline-scroll').scrollLeft;
  const pxPerSec = 60 * zoom;
  const time = x / pxPerSec;
  if (video.duration && time <= video.duration) {
    video.currentTime = time;
  }
}

function updatePlayhead(pct) {
  if (!video.duration) return;
  const pxPerSec = 60 * zoom;
  const left = video.currentTime * pxPerSec;
  document.getElementById('playhead').style.left = (left + 20) + 'px'; // 20 = ruler offset
}

function updateZoom(val) {
  zoom = parseFloat(val);
  state.zoom = zoom;
  const pxPerSec = 60 * zoom;
  clips.forEach(c => {
    c.el.style.width = Math.max(60, c.duration * pxPerSec) + 'px';
  });
  updateInnerWidth();
  drawRuler();
}

function updateInnerWidth() {
  const maxDur = Math.max(60, ...(clips.map(c => c.duration)));
  const pxPerSec = 60 * zoom;
  document.getElementById('timeline-inner').style.width = Math.max(2000, maxDur * pxPerSec + 200) + 'px';
}

function drawRuler() {
  const canvas = document.getElementById('ruler-canvas');
  const w = document.getElementById('timeline-inner').offsetWidth || 2000;
  canvas.width = w; canvas.height = 20;
  const ctx = canvas.getContext('2d');
  ctx.clearRect(0, 0, w, 20);
  const pxPerSec = 60 * zoom;
  const step = zoom < 2 ? 5 : zoom < 3 ? 2 : 1;
  ctx.fillStyle = '#55556a';
  ctx.font = '9px DM Mono, monospace';
  for (let s = 0; s * pxPerSec <= w; s += step) {
    const x = s * pxPerSec;
    ctx.fillRect(x, 12, 1, 8);
    if (s % (step * 5) === 0) {
      ctx.fillRect(x, 6, 1, 14);
      ctx.fillStyle = '#9090aa';
      ctx.fillText(formatTime(s).slice(0, 4), x + 2, 12);
      ctx.fillStyle = '#55556a';
    }
  }
}

// ── PANEL SWITCHING ───────────────────────────────────────────────────────────
function switchPanel(name, tabEl) {
  document.querySelectorAll('.panel-tab').forEach(t => t.classList.remove('active'));
  tabEl.classList.add('active');
  ['media','effects','filters','text','audio','ai'].forEach(p => {
    document.getElementById('panel-' + p).style.display = p === name ? '' : 'none';
  });
}

// ── TEXT OVERLAYS ─────────────────────────────────────────────────────────────
let textColor = '#ffffff';

function setTextColor(c, el) {
  textColor = c;
  document.querySelectorAll('.color-swatch').forEach(s => s.classList.remove('active'));
  el.classList.add('active');
}

function openTextModal() {
  document.getElementById('text-modal').classList.add('open');
}

function confirmAddText() {
  const txt = document.getElementById('text-input').value || 'Text';
  const size = document.getElementById('text-size').value + 'px';
  addTextOverlay(txt, size, 'Outfit', textColor);
  document.getElementById('text-modal').classList.remove('open');
}

function addTextOverlay(text, size, font, color) {
  const container = document.getElementById('text-overlays');
  const el = document.createElement('div');
  el.style.cssText = `
    position:absolute; left:50%; top:80%; transform:translate(-50%,-50%);
    font-family:'${font}',sans-serif; font-size:${size}; color:${color};
    text-shadow:0 2px 8px rgba(0,0,0,.8); cursor:move;
    user-select:none; white-space:nowrap; z-index:11;
    padding:4px 8px;
  `;
  el.textContent = text;
  makeDraggableText(el);
  el.addEventListener('dblclick', () => {
    const newTxt = prompt('Edit text:', el.textContent);
    if (newTxt !== null) el.textContent = newTxt;
  });
  container.appendChild(el);
  addClipToTimeline(text.slice(0,16), video.duration || 10, 'text');
  showToast('Text added — drag to reposition, dblclick to edit');
}

function makeDraggableText(el) {
  let ox, oy, sx, sy;
  el.addEventListener('mousedown', e => {
    ox = el.offsetLeft; oy = el.offsetTop;
    sx = e.clientX; sy = e.clientY;
    el.style.transform = 'none';
    el.style.left = ox + 'px'; el.style.top = oy + 'px';
    const mv = e => { el.style.left = (ox + e.clientX - sx) + 'px'; el.style.top = (oy + e.clientY - sy) + 'px'; };
    const up = () => { document.removeEventListener('mousemove', mv); document.removeEventListener('mouseup', up); };
    document.addEventListener('mousemove', mv);
    document.addEventListener('mouseup', up);
    e.preventDefault();
  });
}

// ── EXPORT ────────────────────────────────────────────────────────────────────
function openExport() { document.getElementById('export-modal').classList.add('open'); }
function closeExport() {
  document.getElementById('export-modal').classList.remove('open');
  document.getElementById('export-progress').style.display = 'none';
  document.getElementById('export-fill').style.width = '0';
}

function setRes(el, res) {
  document.querySelectorAll('.res-btn').forEach(b => b.classList.remove('active'));
  el.classList.add('active');
}

function startExport() {
  const progressWrap = document.getElementById('export-progress');
  const fill = document.getElementById('export-fill');
  const txt = document.getElementById('export-text');
  progressWrap.style.display = 'block';
  fill.style.width = '0';
  const steps = ['Analyzing clips…','Applying effects…','Encoding video…','Finalizing audio…','Writing file…'];
  let i = 0;
  const interval = setInterval(() => {
    if (i >= steps.length) {
      clearInterval(interval);
      txt.textContent = '✅ Export complete!';
      setTimeout(closeExport, 1500);
      return;
    }
    fill.style.width = ((i + 1) / steps.length * 100) + '%';
    txt.textContent = steps[i];
    i++;
  }, 600);
}

// ── TOAST ─────────────────────────────────────────────────────────────────────
let toastTimer;
function showToast(msg) {
  const toast = document.getElementById('toast');
  toast.textContent = msg;
  toast.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => toast.classList.remove('show'), 2500);
}

// ── UPLOAD ZONE DRAG HIGHLIGHT ────────────────────────────────────────────────
const uploadZone = document.getElementById('upload-zone');
if (uploadZone) {
  uploadZone.addEventListener('dragover', e => { e.preventDefault(); uploadZone.style.borderColor = 'var(--accent)'; });
  uploadZone.addEventListener('dragleave', () => { uploadZone.style.borderColor = ''; });
  uploadZone.addEventListener('drop', e => {
    e.preventDefault();
    uploadZone.style.borderColor = '';
    handleFiles(e.dataTransfer.files);
  });
}

// Audio file input
function handleAudioFile(file) {
  if (!file) return;
  const dur = Math.floor(Math.random() * 120 + 30);
  addAudioTrack(file.name.replace(/\.[^.]+$/, ''), Math.floor(dur/60) + ':' + String(dur%60).padStart(2,'0'));
}

// ── UNDO (simple) ─────────────────────────────────────────────────────────────
const undoStack = [];
function undo() { showToast('↩ Undo (no more history)'); }

// ── INIT ──────────────────────────────────────────────────────────────────────
drawRuler();
window.addEventListener('resize', drawRuler);

// Keyboard shortcuts
document.addEventListener('keydown', e => {
  if (e.target.tagName === 'INPUT' || e.target.tagName === 'TEXTAREA' || e.target.tagName === 'SELECT') return;
  if (e.code === 'Space') { e.preventDefault(); togglePlay(); }
  if (e.code === 'ArrowLeft') frameStep(-1);
  if (e.code === 'ArrowRight') frameStep(1);
  if (e.code === 'Delete') deleteSelected();
  if (e.key === 's' && e.ctrlKey) { e.preventDefault(); showToast('💾 Draft saved'); }
});

// Close modals on backdrop click
document.getElementById('export-modal').addEventListener('click', e => {
  if (e.target === document.getElementById('export-modal')) closeExport();
});
document.getElementById('text-modal').addEventListener('click', e => {
  if (e.target === document.getElementById('text-modal')) document.getElementById('text-modal').classList.remove('open');
});

showToast('Welcome to CutLab — Drop a video to start');
</script>
</body>
</html>
