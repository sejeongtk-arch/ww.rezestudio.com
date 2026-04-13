<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>𝓡𝓮𝔃𝓮 𝓢𝓽𝓾𝓭𝓲𝓸</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Rajdhani:wght@300;400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
:root {
  --purple: #7c3aed;
  --purple-light: #a855f7;
  --purple-dark: #4c1d95;
  --green: #10b981;
  --green-light: #34d399;
  --green-dark: #064e3b;
  --bg: #05020f;
  --surface: rgba(124, 58, 237, 0.07);
  --border: rgba(168, 85, 247, 0.2);
  --text: #f0e6ff;
  --muted: #9d8ec0;
  --gold: #fbbf24;
  --anime-outline: 2px solid #1a0a2e;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

/* CUSTOM CURSOR */
* { cursor: none !important; }
#custom-cursor {
  position: fixed;
  width: 38px;
  height: 38px;
  pointer-events: none;
  z-index: 99999;
  transform: translate(-50%, -50%);
  transition: transform 0.05s linear;
  image-rendering: pixelated;
}
#custom-cursor svg {
  width: 100%;
  height: 100%;
  filter: drop-shadow(0 0 6px rgba(168,85,247,0.8));
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Rajdhani', sans-serif;
  overflow-x: hidden;
}

/* ANIME OUTLINE EFFECT */
.anime-card {
  outline: var(--anime-outline);
  box-shadow: 3px 3px 0 #1a0a2e, 6px 6px 0 rgba(124,58,237,0.3);
}

/* BACKGROUND */
.bg-layer {
  position: fixed; inset: 0; z-index: 0;
  background:
    radial-gradient(ellipse 60% 40% at 20% 30%, rgba(124,58,237,0.18) 0%, transparent 70%),
    radial-gradient(ellipse 50% 50% at 80% 70%, rgba(16,185,129,0.12) 0%, transparent 70%);
  animation: bgPulse 8s ease-in-out infinite alternate;
}
@keyframes bgPulse { 0% { opacity:0.8; } 100% { opacity:1.2; } }

.grid-bg {
  position: fixed; inset: 0; z-index: 0;
  background-image:
    linear-gradient(rgba(124,58,237,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(124,58,237,0.04) 1px, transparent 1px);
  background-size: 60px 60px;
  pointer-events: none;
}

.particles { position: fixed; inset: 0; z-index: 0; pointer-events: none; overflow: hidden; }
.particle {
  position: absolute; border-radius: 50%;
  animation: floatUp linear infinite; opacity: 0;
}
@keyframes floatUp {
  0% { transform: translateY(100vh) scale(0); opacity: 0; }
  10% { opacity: 1; }
  90% { opacity: 0.6; }
  100% { transform: translateY(-10vh) scale(1); opacity: 0; }
}

/* NAVBAR */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  padding: 14px 40px;
  display: flex; align-items: center; justify-content: space-between;
  background: rgba(5,2,15,0.85);
  backdrop-filter: blur(20px);
  border-bottom: 2px solid var(--border);
  outline: 1px solid #1a0a2e;
}
.nav-logo {
  font-family: 'Cinzel Decorative', serif;
  font-size: 1.1rem; font-weight: 700;
  background: linear-gradient(135deg, var(--purple-light), var(--green-light));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  letter-spacing: 2px; text-decoration: none;
  text-shadow: none;
  filter: drop-shadow(0 0 8px rgba(168,85,247,0.5));
}
.nav-links { display: flex; gap: 4px; list-style: none; }
.nav-links a {
  color: var(--muted); text-decoration: none;
  font-size: 0.9rem; font-weight: 700; letter-spacing: 2px; text-transform: uppercase;
  padding: 8px 16px; border-radius: 4px;
  transition: all 0.2s;
  border: 1px solid transparent;
  outline: 1px solid transparent;
}
.nav-links a:hover, .nav-links a.active {
  color: var(--text);
  border-color: var(--border);
  outline-color: #1a0a2e;
  background: rgba(124,58,237,0.1);
  box-shadow: 2px 2px 0 #1a0a2e;
}

/* LANG SWITCHER */
.lang-switcher {
  display: flex; align-items: center; gap: 6px;
  background: rgba(124,58,237,0.1);
  border: 2px solid var(--border);
  outline: 1px solid #1a0a2e;
  border-radius: 20px;
  padding: 4px 6px;
  box-shadow: 2px 2px 0 #1a0a2e;
}
.lang-btn {
  background: transparent; border: none;
  color: var(--muted); font-family: 'Rajdhani', sans-serif;
  font-size: 0.75rem; font-weight: 700; letter-spacing: 1px;
  padding: 4px 10px; border-radius: 14px;
  transition: all 0.2s;
}
.lang-btn.active {
  background: linear-gradient(135deg, var(--purple), var(--purple-dark));
  color: white;
  box-shadow: 1px 1px 0 #1a0a2e;
}
.lang-btn:hover:not(.active) { color: var(--text); }

/* NAV RIGHT GROUP */
.nav-right { display: flex; align-items: center; gap: 12px; }

/* SECRET SEARCH */
.secret-search-wrap {
  position: relative; display: flex; align-items: center;
}
.secret-input {
  background: rgba(124,58,237,0.1); border: 2px solid var(--border);
  outline: 1px solid #1a0a2e; border-radius: 30px;
  padding: 8px 44px 8px 20px; color: var(--text);
  font-family: 'Rajdhani', sans-serif; font-size: 0.9rem; font-weight: 600;
  letter-spacing: 1px; width: 180px; transition: all 0.3s;
}
.secret-input:focus {
  outline: 1px solid #1a0a2e; border-color: var(--purple-light);
  box-shadow: 0 0 20px rgba(168,85,247,0.3), 3px 3px 0 #1a0a2e; width: 220px;
}
.secret-icon { position: absolute; right: 14px; color: var(--purple-light); font-size: 1rem; pointer-events: none; }

/* PAGE */
.page { position: relative; z-index: 10; }
section { display: none; min-height: 100vh; padding-top: 80px; }
section.active { display: block; }

/* HOME */
.hero {
  min-height: 100vh;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column; text-align: center;
  padding: 120px 24px 60px; position: relative;
}
.hero-badge {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(124,58,237,0.15);
  border: 2px solid rgba(168,85,247,0.4);
  outline: var(--anime-outline);
  border-radius: 30px; padding: 6px 20px;
  font-size: 0.8rem; letter-spacing: 3px; text-transform: uppercase;
  color: var(--purple-light); margin-bottom: 32px;
  animation: fadeSlideDown 0.8s ease forwards;
  box-shadow: 3px 3px 0 #1a0a2e;
}
.badge-dot {
  width: 6px; height: 6px; background: var(--green-light);
  border-radius: 50%; animation: pulse 2s infinite;
  outline: 1px solid #1a0a2e;
}
@keyframes pulse {
  0%,100% { box-shadow: 0 0 0 0 rgba(52,211,153,0.4); }
  50% { box-shadow: 0 0 0 8px rgba(52,211,153,0); }
}
.hero-title {
  font-family: 'Cinzel Decorative', serif;
  font-size: clamp(2.5rem, 6vw, 5.5rem);
  font-weight: 900; line-height: 1.1; margin-bottom: 20px;
  animation: fadeSlideDown 0.9s 0.1s ease both;
  -webkit-text-stroke: 1px #1a0a2e;
}
.hero-title .line1 {
  background: linear-gradient(135deg, #c084fc 0%, #a855f7 40%, #34d399 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  -webkit-text-stroke: 0;
  filter: drop-shadow(0 0 15px rgba(168,85,247,0.5));
  display: block;
}
.hero-sub {
  font-size: 1.1rem; color: var(--muted); letter-spacing: 3px;
  text-transform: uppercase; margin-bottom: 48px; font-weight: 600;
  animation: fadeSlideDown 1s 0.2s ease both;
  -webkit-text-stroke: 0.5px #1a0a2e;
}
.hero-ctas {
  display: flex; gap: 16px; flex-wrap: wrap; justify-content: center;
  animation: fadeSlideDown 1.1s 0.3s ease both;
}
.btn-primary {
  background: linear-gradient(135deg, var(--purple), #6d28d9);
  border: 2px solid var(--purple-light);
  outline: var(--anime-outline);
  color: white; padding: 14px 36px; border-radius: 6px;
  font-family: 'Rajdhani', sans-serif; font-size: 1rem; font-weight: 700;
  letter-spacing: 2px; text-transform: uppercase;
  text-decoration: none; position: relative; overflow: hidden;
  transition: all 0.2s;
  box-shadow: 4px 4px 0 #1a0a2e;
}
.btn-primary:hover { transform: translate(-2px,-2px); box-shadow: 6px 6px 0 #1a0a2e; }
.btn-outline {
  background: transparent; border: 2px solid var(--border);
  outline: var(--anime-outline);
  color: var(--text); padding: 14px 36px; border-radius: 6px;
  font-family: 'Rajdhani', sans-serif; font-size: 1rem; font-weight: 700;
  letter-spacing: 2px; text-transform: uppercase;
  text-decoration: none; transition: all 0.2s;
  box-shadow: 4px 4px 0 #1a0a2e;
}
.btn-outline:hover { border-color: var(--purple-light); transform: translate(-2px,-2px); box-shadow: 6px 6px 0 #1a0a2e; }

.orb { position: absolute; border-radius: 50%; filter: blur(60px); pointer-events: none; animation: orbFloat 6s ease-in-out infinite alternate; }
.orb-1 { width:300px;height:300px;background:rgba(124,58,237,0.15);top:15%;left:5%; }
.orb-2 { width:200px;height:200px;background:rgba(16,185,129,0.12);top:60%;right:8%;animation-delay:-3s; }
.orb-3 { width:150px;height:150px;background:rgba(168,85,247,0.1);bottom:20%;left:20%;animation-delay:-1.5s; }
@keyframes orbFloat { 0%{transform:translateY(0) scale(1);} 100%{transform:translateY(-30px) scale(1.1);} }
@keyframes fadeSlideDown { from{opacity:0;transform:translateY(-20px);} to{opacity:1;transform:translateY(0);} }

/* SECTION HEADERS */
.section-header { text-align: center; padding: 50px 24px 30px; }
.section-label { font-size:0.75rem;letter-spacing:4px;text-transform:uppercase;color:var(--green-light);margin-bottom:12px; }
.section-title {
  font-family: 'Cinzel Decorative', serif;
  font-size: clamp(1.6rem, 3.5vw, 2.5rem);
  background: linear-gradient(135deg, var(--purple-light), var(--green-light));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  margin-bottom: 12px; -webkit-text-stroke: 0;
  filter: drop-shadow(0 0 8px rgba(168,85,247,0.4));
}
.section-sub { color: var(--muted); font-size:1rem;letter-spacing:1px;max-width:500px;margin:0 auto; }
.divider { width:80px;height:3px;margin:16px auto 0;background:linear-gradient(90deg,var(--purple),var(--green));outline:1px solid #1a0a2e; }

/* ADMIN PANEL */
.admin-panel-overlay {
  display: none; position: fixed; inset: 0; z-index: 500;
  background: rgba(0,0,0,0.7); backdrop-filter: blur(10px);
  align-items: center; justify-content: center;
}
.admin-panel-overlay.open { display: flex; }
.admin-panel {
  background: linear-gradient(145deg, #0a0418, #040d08);
  border: 2px solid var(--border);
  outline: var(--anime-outline);
  border-radius: 16px; padding: 40px;
  width: 90%; max-width: 600px;
  box-shadow: 8px 8px 0 #1a0a2e, 0 0 60px rgba(124,58,237,0.2);
  max-height: 90vh; overflow-y: auto;
  position: relative;
}
.admin-panel h2 {
  font-family: 'Cinzel Decorative', serif;
  font-size: 1.3rem;
  background: linear-gradient(135deg, var(--purple-light), var(--green-light));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  margin-bottom: 24px; text-align: center;
}
.form-group { margin-bottom: 20px; }
.form-label {
  display: block; color: var(--green-light);
  font-size: 0.8rem; letter-spacing: 2px; text-transform: uppercase;
  margin-bottom: 8px; font-weight: 700;
}
.form-input, .form-select {
  width: 100%; background: rgba(124,58,237,0.1);
  border: 2px solid var(--border); outline: 1px solid #1a0a2e;
  border-radius: 8px; padding: 12px 16px;
  color: var(--text); font-family: 'Rajdhani', sans-serif;
  font-size: 1rem; font-weight: 600; letter-spacing: 1px;
  transition: all 0.2s;
}
.form-input:focus, .form-select:focus {
  outline: 1px solid #1a0a2e;
  border-color: var(--purple-light);
  box-shadow: 0 0 15px rgba(168,85,247,0.3), 3px 3px 0 #1a0a2e;
  background: rgba(124,58,237,0.15);
}
.form-select option { background: #0a0418; }
.type-selector { display: flex; gap: 12px; margin-bottom: 20px; }
.type-btn {
  flex: 1; padding: 12px; border: 2px solid var(--border);
  outline: var(--anime-outline);
  border-radius: 8px; background: transparent;
  color: var(--muted); font-family: 'Rajdhani', sans-serif;
  font-size: 0.9rem; font-weight: 700; letter-spacing: 2px;
  text-transform: uppercase; transition: all 0.2s;
  box-shadow: 3px 3px 0 #1a0a2e;
}
.type-btn.active {
  border-color: var(--purple-light); color: var(--text);
  background: rgba(124,58,237,0.2);
  box-shadow: 3px 3px 0 #1a0a2e;
}
.type-btn:hover { border-color: var(--purple-light); color: var(--text); transform: translate(-1px,-1px); box-shadow: 4px 4px 0 #1a0a2e; }
.shop-fields { display: none; }
.shop-fields.show { display: block; }
.btn-submit {
  width: 100%; background: linear-gradient(135deg, var(--purple), var(--green-dark));
  border: 2px solid var(--purple-light); outline: var(--anime-outline);
  color: white; padding: 14px; border-radius: 8px;
  font-family: 'Rajdhani', sans-serif; font-size: 1rem; font-weight: 700;
  letter-spacing: 2px; text-transform: uppercase;
  transition: all 0.2s; margin-top: 8px;
  box-shadow: 4px 4px 0 #1a0a2e;
}
.btn-submit:hover { transform: translate(-2px,-2px); box-shadow: 6px 6px 0 #1a0a2e; }
.btn-close-panel {
  position: absolute; top: 16px; right: 16px;
  background: rgba(168,85,247,0.1); border: 2px solid var(--border);
  outline: 1px solid #1a0a2e; color: var(--muted);
  width: 36px; height: 36px; border-radius: 50%;
  font-size: 1.2rem; display: flex; align-items: center; justify-content: center;
  box-shadow: 2px 2px 0 #1a0a2e;
}
.btn-close-panel:hover { color: var(--text); border-color: var(--purple-light); }

/* FILE UPLOAD ZONE */
.file-upload-zone {
  width: 100%;
  border: 2px dashed rgba(168,85,247,0.4);
  outline: 1px solid #1a0a2e;
  border-radius: 12px;
  padding: 32px 20px;
  text-align: center;
  background: rgba(124,58,237,0.05);
  transition: all 0.3s;
  position: relative;
  overflow: hidden;
}
.file-upload-zone:hover, .file-upload-zone.dragover {
  border-color: var(--purple-light);
  background: rgba(124,58,237,0.12);
  box-shadow: 0 0 20px rgba(168,85,247,0.2);
}
.file-upload-zone input[type="file"] {
  position: absolute; inset: 0; opacity: 0; width: 100%; height: 100%;
}
.upload-icon { font-size: 2.5rem; margin-bottom: 12px; display: block; }
.upload-label-main {
  color: var(--purple-light); font-weight: 700;
  font-size: 1rem; letter-spacing: 1px; display: block; margin-bottom: 6px;
}
.upload-label-sub {
  color: var(--muted); font-size: 0.8rem; letter-spacing: 1px;
}
.upload-formats {
  margin-top: 10px;
  display: flex; gap: 8px; justify-content: center; flex-wrap: wrap;
}
.upload-format-tag {
  background: rgba(124,58,237,0.15);
  border: 1px solid var(--border);
  border-radius: 20px; padding: 3px 10px;
  font-size: 0.7rem; letter-spacing: 1px; color: var(--muted);
  font-family: 'Space Mono', monospace;
}

/* VIDEO PREVIEW IN FORM */
.video-preview-wrap {
  display: none;
  margin-top: 12px;
  position: relative;
  border-radius: 10px;
  overflow: hidden;
  border: 2px solid var(--border);
  outline: 1px solid #1a0a2e;
  box-shadow: 3px 3px 0 #1a0a2e;
  background: #000;
}
.video-preview-wrap.show { display: block; }
.video-preview-wrap video {
  width: 100%;
  max-height: 200px;
  object-fit: cover;
  display: block;
}
.video-preview-info {
  padding: 10px 14px;
  background: rgba(5,2,15,0.9);
  display: flex; align-items: center; justify-content: space-between;
}
.video-preview-name {
  font-size: 0.8rem; color: var(--green-light);
  letter-spacing: 1px; font-weight: 700;
  white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
  max-width: 200px;
}
.video-preview-size {
  font-size: 0.75rem; color: var(--muted);
  font-family: 'Space Mono', monospace;
}
.btn-remove-video {
  background: rgba(220,38,38,0.7); border: 1px solid #dc2626;
  color: white; border-radius: 50%; width: 24px; height: 24px;
  font-size: 0.7rem; display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}
.btn-remove-video:hover { background: #dc2626; }

/* UPLOAD PROGRESS */
.upload-progress-wrap {
  display: none; margin-top: 10px;
}
.upload-progress-wrap.show { display: block; }
.upload-progress-bar-bg {
  background: rgba(124,58,237,0.1);
  border: 1px solid var(--border);
  border-radius: 20px; height: 8px; overflow: hidden;
}
.upload-progress-bar {
  height: 100%; background: linear-gradient(90deg, var(--purple), var(--green));
  border-radius: 20px; transition: width 0.3s; width: 0%;
}
.upload-progress-text {
  text-align: center; font-size: 0.75rem; color: var(--green-light);
  margin-top: 6px; letter-spacing: 1px; font-family: 'Space Mono', monospace;
}

/* SHOWCASE GRID */
.showcase-grid {
  display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 24px; padding: 20px 40px 80px; max-width: 1200px; margin: 0 auto;
}
.showcase-card {
  background: var(--surface); border: 2px solid var(--border);
  border-radius: 12px; overflow: hidden; transition: all 0.3s;
  outline: var(--anime-outline);
  box-shadow: 4px 4px 0 #1a0a2e;
  position: relative;
}
.showcase-card:hover { transform: translate(-3px,-3px); box-shadow: 7px 7px 0 #1a0a2e, 0 0 30px rgba(124,58,237,0.15); border-color: rgba(168,85,247,0.5); }

.video-wrapper {
  position: relative; width: 100%; padding-top: 56.25%;
  background: #000; overflow: hidden;
}
.video-wrapper video {
  position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  object-fit: cover; border: none;
}
.video-wrapper iframe {
  position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  border: none;
}
.video-placeholder {
  position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  background: linear-gradient(135deg, rgba(76,29,149,0.6), rgba(6,78,59,0.6));
  display: flex; align-items: center; justify-content: center;
  font-size: 2.5rem;
}
.video-tag {
  position: absolute; bottom: 8px; left: 10px; z-index: 2;
  font-size: 0.65rem; letter-spacing: 2px; text-transform: uppercase;
  color: var(--green-light); background: rgba(0,0,0,0.7);
  padding: 3px 10px; border-radius: 20px;
  outline: 1px solid #1a0a2e; border: 1px solid var(--green-dark);
}
.card-body { padding: 16px 20px; }
.card-title { font-family: 'Cinzel Decorative', serif; font-size: 0.85rem; font-weight: 700; margin-bottom: 6px; -webkit-text-stroke: 0.3px #1a0a2e; }
.empty-state {
  text-align: center; padding: 80px 40px; color: var(--muted);
  display: flex; flex-direction: column; align-items: center; gap: 16px;
}
.empty-state .empty-icon { font-size: 4rem; filter: grayscale(0.5); }
.empty-state p { font-size: 1rem; letter-spacing: 1px; }

/* SHOP GRID */
.shop-grid {
  display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 24px; padding: 20px 40px 80px; max-width: 1200px; margin: 0 auto;
}
.shop-card {
  background: linear-gradient(145deg, rgba(12,5,30,0.9), rgba(4,20,15,0.9));
  border: 2px solid var(--border); border-radius: 16px; padding: 0;
  outline: var(--anime-outline); box-shadow: 5px 5px 0 #1a0a2e;
  overflow: hidden; transition: all 0.3s; position: relative;
}
.shop-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
  background: linear-gradient(90deg, var(--purple), var(--green));
  outline: none;
}
.shop-card:hover { transform: translate(-3px,-3px); box-shadow: 8px 8px 0 #1a0a2e; border-color: rgba(168,85,247,0.5); }
.shop-card .video-wrapper { border-bottom: 2px solid var(--border); }
.shop-card-body { padding: 20px; }
.shop-card-title {
  font-family: 'Cinzel Decorative', serif; font-size: 0.9rem; font-weight: 700;
  margin-bottom: 8px;
  background: linear-gradient(135deg, white, var(--purple-light));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  -webkit-text-stroke: 0;
}
.shop-card-desc { color: var(--muted); font-size: 0.85rem; line-height: 1.6; margin-bottom: 16px; }
.price-row { display: flex; align-items: center; justify-content: space-between; margin-bottom: 12px; }
.price { font-family: 'Space Mono', monospace; font-size: 1.6rem; font-weight: 700; color: var(--gold); -webkit-text-stroke: 1px #1a0a2e; }
.price-from { font-size: 0.7rem; color: var(--muted); letter-spacing: 1px; }
.btn-buy {
  display: block; width: 100%;
  background: linear-gradient(135deg, var(--purple-dark), var(--purple));
  border: 2px solid rgba(168,85,247,0.5); outline: var(--anime-outline);
  color: white; padding: 12px; border-radius: 8px;
  font-family: 'Rajdhani', sans-serif; font-size: 0.9rem; font-weight: 700;
  letter-spacing: 1.5px; text-transform: uppercase;
  text-decoration: none; text-align: center;
  transition: all 0.2s; box-shadow: 3px 3px 0 #1a0a2e;
}
.btn-buy:hover { transform: translate(-2px,-2px); box-shadow: 5px 5px 0 #1a0a2e; }
.buy-note { text-align:center;margin-top:8px;font-size:0.7rem;letter-spacing:1px;color:var(--muted);text-transform:uppercase; }
.buy-note strong { color: var(--purple-light); }

/* POST DETAIL MODAL */
.post-detail-overlay {
  display: none; position: fixed; inset: 0; z-index: 400;
  background: rgba(0,0,0,0.85); backdrop-filter: blur(12px);
  align-items: center; justify-content: center; padding: 20px;
}
.post-detail-overlay.open { display: flex; }
.post-detail {
  background: linear-gradient(145deg, #0a0418, #040d08);
  border: 2px solid var(--border); outline: var(--anime-outline);
  border-radius: 20px; width: 100%; max-width: 780px;
  box-shadow: 8px 8px 0 #1a0a2e; overflow: hidden;
  max-height: 90vh; display: flex; flex-direction: column;
  position: relative;
}
.post-detail-video { position: relative; width: 100%; padding-top: 56.25%; flex-shrink: 0; }
.post-detail-video video {
  position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; object-fit: contain; background: #000;
}
.post-detail-video .video-placeholder { position:absolute;top:0;left:0;width:100%;height:100%;font-size:5rem; }
.post-detail-info { padding: 28px; overflow-y: auto; }
.post-detail-title { font-family:'Cinzel Decorative',serif;font-size:1.2rem;margin-bottom:12px; -webkit-text-stroke:0.5px #1a0a2e; }
.post-detail-desc { color:var(--muted);font-size:0.95rem;line-height:1.7;margin-bottom:20px; }
.post-detail-price {
  font-family:'Space Mono',monospace;font-size:2rem;font-weight:700;
  color:var(--gold);margin-bottom:20px; -webkit-text-stroke:1px #1a0a2e;
  display:flex;align-items:center;gap:12px;
}
.post-detail-price span { font-family:'Rajdhani',sans-serif;font-size:0.8rem;color:var(--muted);font-weight:400;-webkit-text-stroke:0; }
.post-detail-close {
  position:absolute;top:16px;right:16px;
  background:rgba(0,0,0,0.5);border:2px solid var(--border);outline:1px solid #1a0a2e;
  color:var(--text);width:38px;height:38px;border-radius:50%;
  font-size:1.2rem;display:flex;align-items:center;justify-content:center;
  z-index:10;box-shadow:2px 2px 0 #1a0a2e;
}

/* CONTACT PAGE */
.contact-wrap { max-width:700px;margin:0 auto;padding:20px 24px 80px;display:flex;flex-direction:column;gap:20px; }
.contact-card {
  background:var(--surface);border:2px solid var(--border);border-radius:16px;
  padding:28px;display:flex;align-items:flex-start;gap:20px;
  transition:all 0.3s;outline:var(--anime-outline);box-shadow:4px 4px 0 #1a0a2e;
}
.contact-card:hover { border-color:rgba(168,85,247,0.4);transform:translate(-2px,-2px);box-shadow:6px 6px 0 #1a0a2e; }
.contact-icon {
  width:52px;height:52px;border-radius:12px;
  background:linear-gradient(135deg,var(--purple-dark),var(--green-dark));
  display:flex;align-items:center;justify-content:center;
  font-size:1.5rem;flex-shrink:0;
  border:2px solid var(--border);outline:1px solid #1a0a2e;
  box-shadow:3px 3px 0 #1a0a2e;
}
.contact-info h3 { font-family:'Cinzel Decorative',serif;font-size:0.85rem;margin-bottom:6px; -webkit-text-stroke:0.3px #1a0a2e; }
.contact-info p { color:var(--muted);font-size:0.85rem;line-height:1.6;margin-bottom:14px; }
.btn-discord {
  display:inline-flex;align-items:center;gap:8px;
  background:#5865f2;color:white;text-decoration:none;
  padding:10px 20px;border-radius:6px;
  font-family:'Rajdhani',sans-serif;font-size:0.9rem;font-weight:700;letter-spacing:1px;
  transition:all 0.2s;border:2px solid #4752c4;outline:1px solid #1a0a2e;
  box-shadow:3px 3px 0 #1a0a2e;
}
.btn-discord:hover { background:#4752c4;transform:translate(-2px,-2px);box-shadow:5px 5px 0 #1a0a2e; }
.how-it-works {
  background:var(--surface);border:2px solid var(--border);border-radius:16px;padding:28px;
  outline:var(--anime-outline);box-shadow:4px 4px 0 #1a0a2e;
}
.how-it-works h3 { font-family:'Cinzel Decorative',serif;font-size:0.85rem;margin-bottom:20px;color:var(--green-light); -webkit-text-stroke:0.3px #1a0a2e; }
.steps { display:flex;flex-direction:column;gap:14px; }
.step { display:flex;gap:14px;align-items:flex-start; }
.step-num {
  width:28px;height:28px;border-radius:50%;flex-shrink:0;
  background:linear-gradient(135deg,var(--purple),var(--green-dark));
  display:flex;align-items:center;justify-content:center;
  font-size:0.75rem;font-weight:700;font-family:'Space Mono',monospace;
  border:2px solid var(--border);outline:1px solid #1a0a2e;
  box-shadow:2px 2px 0 #1a0a2e;
}
.step-text { color:var(--muted);font-size:0.85rem;line-height:1.6; }
.step-text strong { color:var(--text); }

/* ADMIN FAB — hidden by default, shown after secret code */
.admin-fab {
  position: fixed; bottom: 30px; right: 30px; z-index: 200;
  width: 56px; height: 56px; border-radius: 50%;
  background: linear-gradient(135deg, var(--purple), var(--green-dark));
  border: 2px solid var(--purple-light); outline: var(--anime-outline);
  color: white; font-size: 1.4rem;
  display: none; align-items: center; justify-content: center;
  transition: all 0.2s;
  box-shadow: 4px 4px 0 #1a0a2e, 0 0 20px rgba(124,58,237,0.4);
}
.admin-fab.visible { display: flex; }
.admin-fab:hover { transform: translate(-2px,-2px) rotate(15deg); box-shadow: 6px 6px 0 #1a0a2e; }

/* FOOTER */
footer {
  text-align:center;padding:28px;
  border-top:2px solid var(--border);
  color:var(--muted);font-size:0.8rem;letter-spacing:2px;
  position:relative;z-index:10;
}
footer span { color:var(--purple-light); }

/* NOTIFICATION */
.notif {
  position: fixed; top: 90px; right: 20px; z-index: 300;
  background: linear-gradient(135deg, #0a0418, #040d08);
  border: 2px solid var(--green-light); outline: var(--anime-outline);
  border-radius: 12px; padding: 16px 20px;
  box-shadow: 4px 4px 0 #1a0a2e;
  font-size: 0.9rem; font-weight: 700; letter-spacing: 1px;
  color: var(--green-light);
  transform: translateX(200%); transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
  max-width: 280px;
}
.notif.show { transform: translateX(0); }
.notif.error { border-color: #ef4444; color: #ef4444; }

/* DELETE BTN */
.delete-btn {
  position: absolute; top: 8px; right: 8px; z-index: 5;
  background: rgba(220,38,38,0.8); border: 2px solid #dc2626; outline: 1px solid #1a0a2e;
  color: white; width: 28px; height: 28px; border-radius: 50%;
  font-size: 0.8rem; display: flex; align-items: center; justify-content: center;
  opacity: 0; transition: opacity 0.2s; box-shadow: 2px 2px 0 #1a0a2e;
}
.showcase-card:hover .delete-btn, .shop-card:hover .delete-btn { opacity: 1; }

/* VIDEO SIZE BADGE */
.video-size-badge {
  position: absolute; bottom: 8px; right: 10px; z-index: 2;
  font-size: 0.6rem; letter-spacing: 1px;
  color: var(--muted); background: rgba(0,0,0,0.7);
  padding: 2px 8px; border-radius: 20px;
  font-family: 'Space Mono', monospace;
  border: 1px solid var(--border);
}

/* STORAGE INFO */
.storage-info {
  background: rgba(124,58,237,0.08);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 10px 14px;
  font-size: 0.75rem;
  color: var(--muted);
  letter-spacing: 1px;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.storage-dot {
  width: 8px; height: 8px; border-radius: 50%;
  background: var(--green-light);
  animation: pulse 2s infinite;
  flex-shrink: 0;
}

@media(max-width:768px) {
  nav { padding: 14px 16px; }
  .nav-links a { padding: 6px 10px; font-size: 0.75rem; }
  .showcase-grid, .shop-grid { padding: 20px 16px 60px; grid-template-columns: 1fr; }
  .contact-wrap { padding: 20px 16px 60px; }
  .admin-panel { padding: 24px; }
  .secret-input { width: 120px; }
  .secret-input:focus { width: 150px; }
  .lang-switcher { display: none; }
}
</style>
</head>
<body>

<!-- CUSTOM CURSOR -->
<div id="custom-cursor">
  <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
    <g transform="rotate(-30, 20, 20)">
      <polygon points="20,2 22,30 20,34 18,30" fill="#c084fc" stroke="#1a0a2e" stroke-width="1.5"/>
      <polygon points="20,2 21,20 20,22 19,20" fill="#e9d5ff" stroke="#1a0a2e" stroke-width="0.5"/>
      <rect x="13" y="28" width="14" height="4" rx="1" fill="#7c3aed" stroke="#1a0a2e" stroke-width="1.5"/>
      <rect x="17" y="32" width="6" height="7" rx="1" fill="#4c1d95" stroke="#1a0a2e" stroke-width="1.5"/>
      <line x1="19.5" y1="4" x2="19" y2="18" stroke="white" stroke-width="0.8" opacity="0.5"/>
      <circle cx="20" cy="4" r="1.5" fill="#34d399" stroke="#1a0a2e" stroke-width="0.8"/>
    </g>
  </svg>
</div>

<div class="bg-layer"></div>
<div class="grid-bg"></div>
<div class="particles" id="particles"></div>

<!-- NOTIFICATION -->
<div class="notif" id="notif">✨ Done!</div>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo" onclick="showPage('home');return false;">𓆩 𝓡𝓮𝔃𝓮 𝓢𝓽𝓾𝓭𝓲𝓸 𓆪</a>
  <ul class="nav-links">
    <li><a href="#" id="nav-home" class="active" onclick="showPage('home');return false;" data-ar="الرئيسية" data-en="Home">Home</a></li>
    <li><a href="#" id="nav-showcase" onclick="showPage('showcase');return false;" data-ar="الأعمال" data-en="Showcase">Showcase</a></li>
    <li><a href="#" id="nav-shop" onclick="showPage('shop');return false;" data-ar="المتجر" data-en="Shop">Shop</a></li>
    <li><a href="#" id="nav-contact" onclick="showPage('contact');return false;" data-ar="تواصل" data-en="Contact">Contact</a></li>
  </ul>
  <div class="nav-right">
    <div class="lang-switcher">
      <button class="lang-btn" id="langAR" onclick="setLang('ar')">AR</button>
      <button class="lang-btn active" id="langEN" onclick="setLang('en')">EN</button>
    </div>
    <div class="secret-search-wrap">
      <input class="secret-input" type="password" placeholder="🔐" id="secretInput" autocomplete="off">
      <span class="secret-icon">⌕</span>
    </div>
  </div>
</nav>

<!-- ADMIN FAB — hidden until secret code entered -->
<button class="admin-fab" id="adminFab" onclick="openAdmin()" title="Add Post">＋</button>

<!-- ADMIN PANEL OVERLAY -->
<div class="admin-panel-overlay" id="adminOverlay" onclick="closeAdminIfOutside(event)">
  <div class="admin-panel">
    <button class="btn-close-panel" onclick="closeAdmin()">✕</button>
    <h2>⚡ <span data-ar="نشر محتوى جديد" data-en="Publish New Content">Publish New Content</span></h2>

    <div class="type-selector">
      <button class="type-btn active" id="typeShowcase" onclick="setType('showcase')">🎬 Showcase</button>
      <button class="type-btn" id="typeShop" onclick="setType('shop')">🛒 Shop</button>
    </div>

    <!-- FILE UPLOAD ZONE -->
    <div class="form-group">
      <label class="form-label">🎥 <span data-ar="رفع فيديو من الجهاز" data-en="Upload Video from Device">Upload Video from Device</span></label>

      <div class="storage-info">
        <div class="storage-dot"></div>
        <span data-ar="الفيديوهات تُخزَّن في المتصفح — جودة كاملة بدون ضغط" data-en="Videos stored in browser — full quality, no compression">Videos stored in browser — full quality, no compression</span>
      </div>

      <div class="file-upload-zone" id="uploadZone">
        <input type="file" id="videoFileInput" accept="video/mp4,video/webm,video/ogg,video/mov,video/avi,video/mkv,video/*" onchange="handleFileSelect(event)">
        <span class="upload-icon">📁</span>
        <span class="upload-label-main" data-ar="اختار فيديو من جهازك" data-en="Choose a video from your device">Choose a video from your device</span>
        <span class="upload-label-sub" data-ar="أو اسحب وأفلت هنا" data-en="or drag & drop here">or drag & drop here</span>
        <div class="upload-formats">
          <span class="upload-format-tag">MP4</span>
          <span class="upload-format-tag">WebM</span>
          <span class="upload-format-tag">MOV</span>
          <span class="upload-format-tag">MKV</span>
          <span class="upload-format-tag">AVI</span>
        </div>
      </div>

      <div class="upload-progress-wrap" id="uploadProgress">
        <div class="upload-progress-bar-bg">
          <div class="upload-progress-bar" id="uploadProgressBar"></div>
        </div>
        <div class="upload-progress-text" id="uploadProgressText">Loading...</div>
      </div>

      <div class="video-preview-wrap" id="videoPreviewWrap">
        <video id="videoPreview" controls preload="metadata"></video>
        <div class="video-preview-info">
          <span class="video-preview-name" id="videoPreviewName">video.mp4</span>
          <span class="video-preview-size" id="videoPreviewSize">0 MB</span>
          <button class="btn-remove-video" onclick="removeVideo()">✕</button>
        </div>
      </div>
    </div>

    <div class="form-group">
      <label class="form-label">📝 <span data-ar="اسم المنشور" data-en="Post Title">Post Title</span></label>
      <input class="form-input" type="text" id="inputTitle" placeholder="e.g. Reze VFX - Edit #1">
    </div>

    <div class="form-group">
      <label class="form-label">📄 <span data-ar="الوصف" data-en="Description">Description</span></label>
      <input class="form-input" type="text" id="inputDesc" placeholder="Short description...">
    </div>

    <div class="shop-fields" id="shopFields">
      <div class="form-group">
        <label class="form-label">💰 <span data-ar="السعر" data-en="Price">Price</span></label>
        <input class="form-input" type="text" id="inputPrice" placeholder="e.g. 10€ or 500 Robux">
      </div>
    </div>

    <button class="btn-submit" onclick="publishPost()">✨ <span data-ar="نشر الآن" data-en="Publish Now">Publish Now</span></button>
  </div>
</div>

<!-- POST DETAIL OVERLAY -->
<div class="post-detail-overlay" id="postDetailOverlay" onclick="closeDetailIfOutside(event)">
  <div class="post-detail" id="postDetailContent">
    <button class="post-detail-close" onclick="closeDetail()">✕</button>
    <div class="post-detail-video" id="detailVideo"></div>
    <div class="post-detail-info">
      <div class="post-detail-title" id="detailTitle"></div>
      <div class="post-detail-desc" id="detailDesc"></div>
      <div class="post-detail-price" id="detailPrice" style="display:none"></div>
      <a id="detailBuyBtn" href="https://discord.gg/3gqEsUSU" target="_blank" class="btn-buy" style="display:none">
        🛒 <span data-ar="اشتري الآن ✧ → Discord" data-en="Buy Now ✧ → Discord">Buy Now ✧ → Discord</span>
      </a>
      <div id="detailBuyNote" class="buy-note" style="display:none">
        <span data-ar="الدفع عبر → " data-en="Payment via → ">Payment via → </span><strong>Discord Server</strong>
      </div>
    </div>
  </div>
</div>

<div class="page">

  <!-- HOME -->
  <section id="home" class="active">
    <div class="hero">
      <div class="orb orb-1"></div>
      <div class="orb orb-2"></div>
      <div class="orb orb-3"></div>
      <div class="hero-badge"><span class="badge-dot"></span>VFX &bull; Animation &bull; Motion</div>
      <h1 class="hero-title">
        <span class="ornament" style="-webkit-text-stroke:0;color:rgba(168,85,247,0.5);font-size:0.6em;">𓆩</span>
        <span class="line1">𝓡𝓮𝔃𝓮 𝓢𝓽𝓾𝓭𝓲𝓸</span>
        <span class="ornament" style="-webkit-text-stroke:0;color:rgba(168,85,247,0.5);font-size:0.6em;">𓆪</span>
      </h1>
      <p class="hero-sub">Premium VFX &amp; Animation Studio</p>
      <div class="hero-ctas">
        <a href="#" class="btn-primary" onclick="showPage('showcase');return false;" data-ar="⬡ شوف الأعمال" data-en="⬡ View Work">⬡ View Work</a>
        <a href="#" class="btn-outline" onclick="showPage('shop');return false;">🛒 Shop</a>
      </div>
    </div>
  </section>

  <!-- SHOWCASE -->
  <section id="showcase">
    <div class="section-header">
      <div class="section-label">⬡ <span data-ar="أعمالنا" data-en="Our Work">Our Work</span></div>
      <h2 class="section-title">Showcase</h2>
      <p class="section-sub" data-ar="مجموعة من أفضل أعمال VFX والـ Animation" data-en="A collection of our best VFX & Animation work">A collection of our best VFX &amp; Animation work</p>
      <div class="divider"></div>
    </div>
    <div class="showcase-grid" id="showcaseGrid">
      <div class="empty-state" style="grid-column:1/-1;">
        <div class="empty-icon">🎬</div>
        <p data-ar="لا يوجد محتوى بعد" data-en="No content yet — enter the secret code to add videos">No content yet — enter the secret code to add videos</p>
      </div>
    </div>
  </section>

  <!-- SHOP -->
  <section id="shop">
    <div class="section-header">
      <div class="section-label">⬡ <span data-ar="الخدمات" data-en="Services">Services</span></div>
      <h2 class="section-title">Shop</h2>
      <p class="section-sub" data-ar="اشتري عبر Discord — جودة عالية وتسليم سريع" data-en="Order via Discord — high quality, fast delivery">Order via Discord — high quality, fast delivery</p>
      <div class="divider"></div>
    </div>
    <div class="shop-grid" id="shopGrid">
      <div class="empty-state" style="grid-column:1/-1;">
        <div class="empty-icon">🛒</div>
        <p data-ar="لا يوجد منتجات بعد" data-en="No products yet — enter the secret code to add services">No products yet — enter the secret code to add services</p>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="section-header">
      <div class="section-label">⬡ <span data-ar="تواصل معنا" data-en="Get in Touch">Get in Touch</span></div>
      <h2 class="section-title">Contact</h2>
      <p class="section-sub" data-ar="جميع الطلبات والدعم عبر Discord" data-en="All orders and support via Discord">All orders and support via Discord</p>
      <div class="divider"></div>
    </div>
    <div class="contact-wrap">
      <div class="contact-card">
        <div class="contact-icon">💬</div>
        <div class="contact-info">
          <h3>Discord Server</h3>
          <p data-ar="انضم لـ Discord عشان تطلب أو تتواصل مع Reze Studio مباشرة. كل المشتريات تتم داخل السيرفر." data-en="Join our Discord to place orders or contact Reze Studio directly. All purchases are made inside the server.">Join our Discord to place orders or contact Reze Studio directly. All purchases are made inside the server.</p>
          <a href="https://discord.gg/3gqEsUSU" target="_blank" class="btn-discord">🔗 <span data-ar="انضم للـ Discord" data-en="Join Discord">Join Discord</span></a>
        </div>
      </div>
      <div class="contact-card">
        <div class="contact-icon">🛒</div>
        <div class="contact-info">
          <h3 data-ar="اطلب خدمة" data-en="Order a Service">Order a Service</h3>
          <p data-ar="تصفح الـ Shop، اختار الخدمة، اضغط 'اشتري الآن' وراح ينقلك للـ Discord عشان تكمل طلبك." data-en="Browse the Shop, pick a service, click 'Buy Now' and you'll be redirected to Discord to complete your order.">Browse the Shop, pick a service, click 'Buy Now' and you'll be redirected to Discord to complete your order.</p>
          <a href="#" onclick="showPage('shop');return false;" class="btn-discord" style="background:linear-gradient(135deg,var(--purple-dark),var(--green-dark));border-color:var(--border);">🛒 <span data-ar="روح للـ Shop" data-en="Go to Shop">Go to Shop</span></a>
        </div>
      </div>
      <div class="contact-card">
        <div class="contact-icon">🎥</div>
        <div class="contact-info">
          <h3 data-ar="شوف أعمالنا" data-en="View Our Work">View Our Work</h3>
          <p data-ar="شوف جميع الأعمال والفيديوهات في Showcase قبل ما تطلب." data-en="Browse all work and videos in the Showcase before placing an order.">Browse all work and videos in the Showcase before placing an order.</p>
          <a href="#" onclick="showPage('showcase');return false;" class="btn-discord" style="background:linear-gradient(135deg,#1a1a2e,#16213e);border-color:var(--border);">🎬 <span data-ar="شوف الأعمال" data-en="View Showcase">View Showcase</span></a>
        </div>
      </div>
      <div class="how-it-works">
        <h3>⬡ <span data-ar="كيف تشتري؟" data-en="How to Order?">How to Order?</span></h3>
        <div class="steps">
          <div class="step"><div class="step-num">1</div><div class="step-text"><strong data-ar="تصفح" data-en="Browse">Browse</strong> <span data-ar="الـ Shop واختار الخدمة اللي تبيها." data-en="the Shop and pick the service you want.">the Shop and pick the service you want.</span></div></div>
          <div class="step"><div class="step-num">2</div><div class="step-text"><strong data-ar='اضغط "اشتري الآن"' data-en='"Buy Now"'>Buy Now</strong> <span data-ar="وراح ينقلك لـ Discord تلقائي." data-en="— you'll be redirected to Discord automatically.">— you'll be redirected to Discord automatically.</span></div></div>
          <div class="step"><div class="step-num">3</div><div class="step-text"><strong data-ar="افتح تذكرة" data-en="Open a ticket">Open a ticket</strong> <span data-ar="داخل Discord وشرح تفاصيل مشروعك." data-en="inside Discord and describe your project details.">inside Discord and describe your project details.</span></div></div>
          <div class="step"><div class="step-num">4</div><div class="step-text"><strong data-ar="ادفع" data-en="Pay">Pay</strong> <span data-ar="داخل السيرفر بأي طريقة دفع تناسبك." data-en="inside the server using any payment method that suits you.">inside the server using any payment method that suits you.</span></div></div>
          <div class="step"><div class="step-num">5</div><div class="step-text"><strong data-ar="استلم مشروعك" data-en="Receive your project">Receive your project</strong> <span data-ar="في الوقت المتفق عليه. ✓" data-en="within the agreed timeframe. ✓">within the agreed timeframe. ✓</span></div></div>
        </div>
      </div>
    </div>
  </section>

</div>

<footer>
  <span>𓆩 𝓡𝓮𝔃𝓮 𝓢𝓽𝓾𝓭𝓲𝓸 𓆪</span> &nbsp;·&nbsp; Premium VFX &amp; Animation &nbsp;·&nbsp; All rights reserved
</footer>

<script>
// ─── CUSTOM CURSOR ───────────────────────────────────
const cur = document.getElementById('custom-cursor');
document.addEventListener('mousemove', e => {
  cur.style.left = e.clientX + 'px';
  cur.style.top = e.clientY + 'px';
});

// ─── PARTICLES ───────────────────────────────────────
(function() {
  const c = document.getElementById('particles');
  const colors = ['rgba(168,85,247,0.6)','rgba(52,211,153,0.5)','rgba(124,58,237,0.4)','rgba(16,185,129,0.3)'];
  for (let i = 0; i < 20; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random()*4+1;
    p.style.cssText = `width:${size}px;height:${size}px;left:${Math.random()*100}%;background:${colors[Math.floor(Math.random()*colors.length)]};animation-duration:${Math.random()*15+10}s;animation-delay:${Math.random()*-20}s;outline:1px solid #1a0a2e;`;
    c.appendChild(p);
  }
})();

// ─── LANGUAGE SYSTEM ─────────────────────────────────
let currentLang = localStorage.getItem('rezeLang') || 'en';

function setLang(lang) {
  currentLang = lang;
  localStorage.setItem('rezeLang', lang);

  // Update lang btn states
  document.getElementById('langAR').classList.toggle('active', lang === 'ar');
  document.getElementById('langEN').classList.toggle('active', lang === 'en');

  // Update html dir
  document.documentElement.lang = lang;
  document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr';

  // Update all data-ar / data-en elements
  document.querySelectorAll('[data-ar],[data-en]').forEach(el => {
    const val = el.getAttribute('data-' + lang);
    if (val !== null) {
      if (el.tagName === 'INPUT' && el.hasAttribute('placeholder')) {
        // skip — keep placeholders as-is or you can add data-placeholder-ar etc.
      } else {
        el.textContent = val;
      }
    }
  });
}

// Init lang
setLang(currentLang);

// ─── PAGE NAV ────────────────────────────────────────
function showPage(id) {
  document.querySelectorAll('.page section').forEach(s => s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  const navEl = document.getElementById('nav-'+id);
  if(navEl) navEl.classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
}

// ─── SECRET CODE ─────────────────────────────────────
const secretInput = document.getElementById('secretInput');
let secretBuffer = '';

secretInput.addEventListener('input', e => {
  secretBuffer = e.target.value;
});

secretInput.addEventListener('keydown', e => {
  if(e.key === 'Enter') {
    if(secretBuffer === '121212') {
      document.getElementById('adminFab').classList.add('visible');
      openAdmin();
      secretInput.value = '';
      secretBuffer = '';
      showNotif('🔓 ' + (currentLang === 'ar' ? 'تم فتح لوحة الإدارة' : 'Admin panel unlocked'));
    } else {
      showNotif('❌ ' + (currentLang === 'ar' ? 'كود خاطئ' : 'Wrong code'), true);
      secretInput.value = '';
      secretBuffer = '';
    }
  }
});

// ─── DATA STORE ──────────────────────────────────────
// Videos stored as IndexedDB for large files + metadata in localStorage
let posts = JSON.parse(localStorage.getItem('rezePosts') || '[]');

function savePosts() {
  // Save metadata only (no blob data) to localStorage
  const meta = posts.map(p => ({ id: p.id, type: p.type, title: p.title, desc: p.desc, price: p.price, fileName: p.fileName, fileSize: p.fileSize }));
  localStorage.setItem('rezePosts', JSON.stringify(meta));
}

// ─── INDEXEDDB FOR VIDEO STORAGE ─────────────────────
const DB_NAME = 'RezeStudioDB';
const DB_VERSION = 1;
const STORE_NAME = 'videos';
let db = null;

function openDB() {
  return new Promise((resolve, reject) => {
    const req = indexedDB.open(DB_NAME, DB_VERSION);
    req.onupgradeneeded = e => {
      const d = e.target.result;
      if (!d.objectStoreNames.contains(STORE_NAME)) {
        d.createObjectStore(STORE_NAME, { keyPath: 'id' });
      }
    };
    req.onsuccess = e => { db = e.target.result; resolve(db); };
    req.onerror = e => reject(e);
  });
}

function saveVideo(id, blob) {
  return new Promise((resolve, reject) => {
    const tx = db.transaction(STORE_NAME, 'readwrite');
    const store = tx.objectStore(STORE_NAME);
    store.put({ id, blob });
    tx.oncomplete = () => resolve();
    tx.onerror = e => reject(e);
  });
}

function getVideo(id) {
  return new Promise((resolve, reject) => {
    const tx = db.transaction(STORE_NAME, 'readonly');
    const store = tx.objectStore(STORE_NAME);
    const req = store.get(id);
    req.onsuccess = e => resolve(e.target.result ? e.target.result.blob : null);
    req.onerror = e => reject(e);
  });
}

function deleteVideo(id) {
  return new Promise((resolve, reject) => {
    const tx = db.transaction(STORE_NAME, 'readwrite');
    const store = tx.objectStore(STORE_NAME);
    store.delete(id);
    tx.oncomplete = () => resolve();
    tx.onerror = e => reject(e);
  });
}

// ─── ADMIN PANEL ─────────────────────────────────────
let currentType = 'showcase';
let currentVideoBlob = null;
let currentVideoFile = null;

function openAdmin() {
  document.getElementById('adminOverlay').classList.add('open');
}
function closeAdmin() {
  document.getElementById('adminOverlay').classList.remove('open');
  resetForm();
}
function closeAdminIfOutside(e) {
  if(e.target === document.getElementById('adminOverlay')) closeAdmin();
}

function setType(t) {
  currentType = t;
  document.getElementById('typeShowcase').classList.toggle('active', t==='showcase');
  document.getElementById('typeShop').classList.toggle('active', t==='shop');
  document.getElementById('shopFields').classList.toggle('show', t==='shop');
}

function resetForm() {
  document.getElementById('inputTitle').value = '';
  document.getElementById('inputDesc').value = '';
  document.getElementById('inputPrice').value = '';
  removeVideo();
  setType('showcase');
}

function showNotif(msg, isError) {
  const n = document.getElementById('notif');
  n.textContent = msg;
  n.classList.toggle('error', !!isError);
  n.classList.add('show');
  setTimeout(()=>n.classList.remove('show'), 3000);
}

// ─── FILE UPLOAD ─────────────────────────────────────
function handleFileSelect(e) {
  const file = e.target.files[0];
  if (!file) return;
  loadVideoFile(file);
}

// Drag & Drop
const uploadZone = document.getElementById('uploadZone');
uploadZone.addEventListener('dragover', e => {
  e.preventDefault();
  uploadZone.classList.add('dragover');
});
uploadZone.addEventListener('dragleave', () => uploadZone.classList.remove('dragover'));
uploadZone.addEventListener('drop', e => {
  e.preventDefault();
  uploadZone.classList.remove('dragover');
  const file = e.dataTransfer.files[0];
  if (file && file.type.startsWith('video/')) {
    loadVideoFile(file);
  } else {
    showNotif('❌ ' + (currentLang === 'ar' ? 'ملف غير صالح — فقط فيديو' : 'Invalid file — video only'), true);
  }
});

function loadVideoFile(file) {
  currentVideoFile = file;

  // Show progress
  const progressWrap = document.getElementById('uploadProgress');
  const progressBar = document.getElementById('uploadProgressBar');
  const progressText = document.getElementById('uploadProgressText');
  progressWrap.classList.add('show');

  // Simulate reading progress
  const reader = new FileReader();
  reader.onprogress = e => {
    if (e.lengthComputable) {
      const pct = Math.round((e.loaded / e.total) * 100);
      progressBar.style.width = pct + '%';
      progressText.textContent = pct + '%';
    }
  };
  reader.onload = e => {
    progressBar.style.width = '100%';
    progressText.textContent = '100%';
    setTimeout(() => {
      progressWrap.classList.remove('show');
      progressBar.style.width = '0%';
    }, 600);

    // Create blob URL for preview
    currentVideoBlob = new Blob([e.target.result], { type: file.type });
    const blobUrl = URL.createObjectURL(currentVideoBlob);

    // Show preview
    const previewWrap = document.getElementById('videoPreviewWrap');
    const previewVideo = document.getElementById('videoPreview');
    const previewName = document.getElementById('videoPreviewName');
    const previewSize = document.getElementById('videoPreviewSize');

    previewVideo.src = blobUrl;
    previewName.textContent = file.name;
    previewSize.textContent = formatBytes(file.size);
    previewWrap.classList.add('show');

    showNotif('✅ ' + (currentLang === 'ar' ? 'تم تحميل الفيديو!' : 'Video loaded!'));
  };
  reader.onerror = () => {
    showNotif('❌ ' + (currentLang === 'ar' ? 'فشل تحميل الملف' : 'Failed to load file'), true);
    progressWrap.classList.remove('show');
  };
  reader.readAsArrayBuffer(file);
}

function removeVideo() {
  currentVideoBlob = null;
  currentVideoFile = null;
  document.getElementById('videoPreviewWrap').classList.remove('show');
  const previewVideo = document.getElementById('videoPreview');
  if (previewVideo.src) {
    URL.revokeObjectURL(previewVideo.src);
    previewVideo.src = '';
  }
  document.getElementById('videoFileInput').value = '';
}

function formatBytes(bytes) {
  if (bytes < 1024*1024) return (bytes/1024).toFixed(1) + ' KB';
  if (bytes < 1024*1024*1024) return (bytes/(1024*1024)).toFixed(1) + ' MB';
  return (bytes/(1024*1024*1024)).toFixed(2) + ' GB';
}

// ─── PUBLISH ─────────────────────────────────────────
async function publishPost() {
  const title = document.getElementById('inputTitle').value.trim();
  const desc = document.getElementById('inputDesc').value.trim();
  const price = document.getElementById('inputPrice').value.trim();

  if(!currentVideoBlob) {
    showNotif('❌ ' + (currentLang === 'ar' ? 'رفع فيديو أول!' : 'Upload a video first!'), true);
    return;
  }
  if(!title) {
    showNotif('❌ ' + (currentLang === 'ar' ? 'حط اسم للمنشور!' : 'Enter a post title!'), true);
    return;
  }
  if(currentType==='shop' && !price) {
    showNotif('❌ ' + (currentLang === 'ar' ? 'حط السعر!' : 'Enter a price!'), true);
    return;
  }

  const id = Date.now();
  const fileName = currentVideoFile ? currentVideoFile.name : 'video.mp4';
  const fileSize = currentVideoFile ? currentVideoFile.size : 0;
  const fileType = currentVideoFile ? currentVideoFile.type : 'video/mp4';

  // Save blob to IndexedDB
  try {
    const blobToSave = new Blob([await currentVideoBlob.arrayBuffer()], { type: fileType });
    await saveVideo(id, blobToSave);
  } catch(err) {
    console.warn('IndexedDB save failed, using object URL fallback:', err);
  }

  const post = { id, type: currentType, title, desc, price, fileName, fileSize };
  posts.unshift(post);
  savePosts();
  renderAll();
  closeAdmin();
  showNotif('✨ ' + (currentLang === 'ar' ? 'تم النشر بنجاح!' : 'Published successfully!'));
}

// ─── RENDER ──────────────────────────────────────────
function renderAll() {
  renderShowcase();
  renderShop();
}

async function renderShowcase() {
  const grid = document.getElementById('showcaseGrid');
  const items = posts.filter(p => p.type === 'showcase');
  if(!items.length) {
    const msg = currentLang === 'ar' ? 'لا يوجد محتوى بعد' : 'No content yet — enter the secret code to add videos';
    grid.innerHTML = `<div class="empty-state" style="grid-column:1/-1;"><div class="empty-icon">🎬</div><p>${msg}</p></div>`;
    return;
  }

  // Build cards with async video URLs
  grid.innerHTML = '';
  for (const p of items) {
    const card = document.createElement('div');
    card.className = 'showcase-card';
    card.onclick = () => openDetail(p.id);
    card.innerHTML = `
      <button class="delete-btn" onclick="event.stopPropagation();deletePost(${p.id})">✕</button>
      <div class="video-wrapper" id="vw-${p.id}"><div class="video-placeholder">🎬</div></div>
      <div class="card-body">
        <div class="card-title">${escHtml(p.title)}</div>
        ${p.desc ? `<div style="color:var(--muted);font-size:0.8rem;margin-top:4px;">${escHtml(p.desc)}</div>` : ''}
        <div class="video-size-badge">${formatBytes(p.fileSize || 0)}</div>
      </div>
    `;
    grid.appendChild(card);
    loadVideoIntoWrapper(p.id, `vw-${p.id}`);
  }
}

async function renderShop() {
  const grid = document.getElementById('shopGrid');
  const items = posts.filter(p => p.type === 'shop');
  if(!items.length) {
    const msg = currentLang === 'ar' ? 'لا يوجد منتجات بعد' : 'No products yet — enter the secret code to add services';
    grid.innerHTML = `<div class="empty-state" style="grid-column:1/-1;"><div class="empty-icon">🛒</div><p>${msg}</p></div>`;
    return;
  }

  grid.innerHTML = '';
  for (const p of items) {
    const card = document.createElement('div');
    card.className = 'shop-card';
    card.onclick = () => openDetail(p.id);
    const priceLabel = currentLang === 'ar' ? 'السعر' : 'Price';
    card.innerHTML = `
      <button class="delete-btn" onclick="event.stopPropagation();deletePost(${p.id})">✕</button>
      <div class="video-wrapper" id="vw-${p.id}"><div class="video-placeholder">🛒</div></div>
      <div class="shop-card-body">
        <div class="shop-card-title">${escHtml(p.title)}</div>
        ${p.desc ? `<div class="shop-card-desc">${escHtml(p.desc)}</div>` : ''}
        <div class="price-row">
          <div>
            <div class="price-from">${priceLabel}</div>
            <div class="price">${escHtml(p.price)}</div>
          </div>
          <div class="video-size-badge" style="position:static">${formatBytes(p.fileSize || 0)}</div>
        </div>
      </div>
    `;
    grid.appendChild(card);
    loadVideoIntoWrapper(p.id, `vw-${p.id}`);
  }
}

async function loadVideoIntoWrapper(postId, wrapperId) {
  try {
    const blob = await getVideo(postId);
    if (!blob) return;
    const url = URL.createObjectURL(blob);
    const wrapper = document.getElementById(wrapperId);
    if (!wrapper) return;
    wrapper.innerHTML = `<video src="${url}" muted loop playsinline preload="metadata" style="position:absolute;top:0;left:0;width:100%;height:100%;object-fit:cover;"></video>`;
    const vid = wrapper.querySelector('video');
    // Hover play
    wrapper.closest('.showcase-card, .shop-card')?.addEventListener('mouseenter', () => vid.play().catch(()=>{}));
    wrapper.closest('.showcase-card, .shop-card')?.addEventListener('mouseleave', () => { vid.pause(); vid.currentTime = 0; });
  } catch(e) {
    console.warn('Could not load video for post', postId, e);
  }
}

// ─── DETAIL MODAL ────────────────────────────────────
async function openDetail(id) {
  const p = posts.find(x => x.id === id);
  if(!p) return;

  document.getElementById('detailTitle').textContent = p.title;
  document.getElementById('detailDesc').textContent = p.desc || '';

  // Load video
  const detailVideoEl = document.getElementById('detailVideo');
  detailVideoEl.innerHTML = '<div class="video-placeholder">⏳</div>';

  try {
    const blob = await getVideo(id);
    if (blob) {
      const url = URL.createObjectURL(blob);
      detailVideoEl.innerHTML = `<video src="${url}" controls autoplay playsinline style="position:absolute;top:0;left:0;width:100%;height:100%;border:none;object-fit:contain;background:#000;"></video>`;
    } else {
      detailVideoEl.innerHTML = '<div class="video-placeholder">🎬</div>';
    }
  } catch(e) {
    detailVideoEl.innerHTML = '<div class="video-placeholder">❌</div>';
  }

  const priceEl = document.getElementById('detailPrice');
  const buyBtn = document.getElementById('detailBuyBtn');
  const buyNote = document.getElementById('detailBuyNote');
  const priceLabel = currentLang === 'ar' ? 'السعر' : 'Price';

  if(p.type === 'shop' && p.price) {
    priceEl.style.display = 'flex';
    priceEl.innerHTML = `${escHtml(p.price)} <span>${priceLabel}</span>`;
    buyBtn.style.display = 'block';
    buyNote.style.display = 'block';
  } else {
    priceEl.style.display = 'none';
    buyBtn.style.display = 'none';
    buyNote.style.display = 'none';
  }

  document.getElementById('postDetailOverlay').classList.add('open');
}

function closeDetail() {
  document.getElementById('postDetailOverlay').classList.remove('open');
  const v = document.getElementById('detailVideo');
  const video = v.querySelector('video');
  if(video) {
    video.pause();
    URL.revokeObjectURL(video.src);
    video.src = '';
  }
  v.innerHTML = '';
}

function closeDetailIfOutside(e) {
  if(e.target === document.getElementById('postDetailOverlay')) closeDetail();
}

// ─── DELETE ──────────────────────────────────────────
async function deletePost(id) {
  const confirmMsg = currentLang === 'ar' ? 'مسح هذا المنشور؟' : 'Delete this post?';
  if(!confirm(confirmMsg)) return;
  posts = posts.filter(p => p.id !== id);
  savePosts();
  await deleteVideo(id);
  renderAll();
  showNotif('🗑️ ' + (currentLang === 'ar' ? 'تم المسح!' : 'Deleted!'));
}

// ─── UTILS ───────────────────────────────────────────
function escHtml(s) {
  return String(s)
    .replace(/&/g,'&amp;')
    .replace(/</g,'&lt;')
    .replace(/>/g,'&gt;')
    .replace(/"/g,'&quot;');
}

// ─── INIT ────────────────────────────────────────────
openDB().then(() => {
  renderAll();
}).catch(err => {
  console.error('IndexedDB failed to open:', err);
  renderAll();
});

// Re-apply lang after render
setTimeout(() => setLang(currentLang), 100);
</script>
</body>
</html>
