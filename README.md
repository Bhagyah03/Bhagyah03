## Hi there
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Resume</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --a: #6366f1;
    --a2: #818cf8;
    --a3: #c7d2fe;
    --bg: #0f0f1a;
    --bg2: #16162a;
    --bg3: #1e1e36;
    --card: #1a1a2e;
    --border: rgba(99,102,241,.2);
    --text: #e2e8f0;
    --muted: #94a3b8;
    --white: #ffffff;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    padding: 0;
    overflow-x: hidden;
  }

  .particles {
    position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden;
  }
  .particle {
    position: absolute;
    border-radius: 50%;
    background: var(--a);
    opacity: .08;
    animation: float linear infinite;
  }

  @keyframes float {
    0%   { transform: translateY(100vh) scale(0); opacity: 0; }
    10%  { opacity: .08; }
    90%  { opacity: .08; }
    100% { transform: translateY(-20vh) scale(1); opacity: 0; }
  }

  .resume {
    position: relative; z-index: 1;
    max-width: 900px;
    margin: 0 auto;
    padding: 0 0 60px;
  }

  .hd {
    background: linear-gradient(135deg, #1a1a3e 0%, #0f0f1a 60%);
    border-bottom: 1px solid var(--border);
    padding: 52px 56px 44px;
    position: relative;
    overflow: hidden;
    opacity: 0;
    animation: slideDown .7s cubic-bezier(.22,1,.36,1) .1s forwards;
  }

  .hd-grid {
    position: absolute; inset: 0; pointer-events: none;
    background-image:
      linear-gradient(rgba(99,102,241,.07) 1px, transparent 1px),
      linear-gradient(90deg, rgba(99,102,241,.07) 1px, transparent 1px);
    background-size: 40px 40px;
  }

  .hd-orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(60px);
    pointer-events: none;
  }
  .hd-orb1 { width:320px; height:320px; top:-100px; right:-80px; background:rgba(99,102,241,.15); }
  .hd-orb2 { width:200px; height:200px; bottom:-60px; left:20%; background:rgba(129,140,248,.1); }

  .hd-inner { position: relative; z-index: 1; }

  .hd-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--a2);
    background: rgba(99,102,241,.12);
    border: 1px solid rgba(99,102,241,.3);
    padding: 4px 14px;
    border-radius: 20px;
    margin-bottom: 18px;
  }
  .hd-badge::before { content:''; width:6px; height:6px; border-radius:50%; background:var(--a2); animation: pulse 2s infinite; }

  @keyframes pulse {
    0%,100% { opacity:1; transform:scale(1); }
    50%      { opacity:.4; transform:scale(1