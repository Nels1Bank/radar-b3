<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v9.0 | Official Treasuries</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surface: #0d1117;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --up: #10b981;
            --border: #30363d;
            --header-h: 65px;
            --nav-h: 60px;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            font-family: 'JetBrains Mono', monospace; 
            background: var(--bg); 
            color: #c9d1d9; 
            height: 100vh;
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }

        /* Header e Ticker Profissional */
        header { flex-shrink: 0; border-bottom: 1px solid var(--border); background: #000; padding: 5px 0; }
        h1 { font-family: 'Orbitron', sans-serif; font-size: 0.7rem; text-align: center; color: var(--primary); letter-spacing: 1px; }

        .ticker { overflow: hidden; white-space: nowrap; background: #000; padding: 4px 0; font-size: 0.6rem; }
        .track { display: inline-block; animation: scroll 20s linear infinite; }
        .asset { padding: 0 15px; border-right: 1px solid var(--border); font-weight: bold; }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        /* Container Principal */
        main { flex-grow: 1; position: relative; overflow: hidden; width: 100%; }
        .tab-content { 
            display: none; height: 100%; width: 100%; 
            padding: 8px; flex-direction: column; gap: 8px;
        }
        .tab-content.active { display: flex; }

        .card { 
            flex: 1; background: var(--surface); 
            border: 1px solid var(--border); 
            border-radius: 8px; overflow: hidden; 
        }

        /* Grid Institucional - Dados Atualizados Maio 2026 */
        .inst-panel {
            display: grid; grid-template-columns: 1fr 1fr;
            gap: 6px; flex-shrink: 0; padding-bottom: 5px;
        }
        .inst-box {
            background: #161b22; border: 1px solid var(--border);
            padding: 10px; border-radius: 6px; border-left: 4px solid var(--crypto);
        }
        .inst-box label { font-size: 0.55rem; color: #8b949e; display: block; margin-bottom: 3px; }
        .inst-box span { font-size: 0.75rem; font-weight: bold; color: #fff; display: block; }
        .inst-box small { font-size: 0.5rem; color: var(--up); font-weight: bold; }

        /* Navegação Mobile */
        nav {
            flex-shrink: 0; height: var(--nav-h); display: flex; 
            background: #010409; border-top: 1px solid var(--border);
            padding-bottom: env(safe-area-inset-bottom);
        }
        .nav-item {
            flex: 1; border: none; background: none; color: #484f58;
            font-family: 'Orbitron', sans-serif; font-size: 0.65rem;
            display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 5px;
        }
        .nav-item.active { color: var(--primary); }
        .nav-item.crypto-active.active { color: var(--crypto); }
        .indicator { width: 15px; height: 2px; background: currentColor; border-radius: 2px; }

    </style>
</head>
<body>

<header>
    <h1>NELS1-RADAR v9.0</h1>
    <div class="ticker">
        <div class="track">
            <span class="asset">BTC $80,340 <span style="color:var(--up)">▲</span></span>
            <span class="asset">BBAS3 R$ 26.45 <span style="color:red">▼</span></span>
            <span class="asset">SBSP3 R$ 82.10 <span style="color:var(--up)">▲</span></span>
            <span class="asset">SOL $174.50 <span style="color:var(--up)">▲</span></span>
            <!-- Duplicação para loop -->
            <span class="asset">BTC $80,340 <span style="color:var(--up)">▲</span></span>
            <span class="asset">BBAS3 R$ 26.45 <span style="color:red">▼</span></span>
            <span class="asset">SBSP3 R$ 82.10 <span style="color:var(--up)">▲</span></span>
            <span class="asset">SOL $174.50 <span style="color:var(--up)">▲</span></span>
        </div>
    </div>
</header>

<main>
    <div id="b3" class="tab-content active">
        <div class="card">
            <iframe src="https://br.tradingview.com/widgetembed/?symbol=BMFBOVESPA%3AIBOV&interval=D&theme=dark" width="100%" height="100%" frameborder="0"></iframe>
        </div>
    </div>

    <div id="crypto" class="tab-content">
        <div class="card" style="border-color: var(--crypto);">
            <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="100%" frameborder="0"></iframe>
        </div>
        
        <div class="inst-panel">
            <div class="inst-box">
                <label>🇺🇸 STRATEGY INC (MSTR)</label>
                <span>818,869 BTC</span>
                <small>+9.4% YTD YIELD</small>
            </div>
            <div class="inst-box">
                <label>🇯🇵 METAPLANET (3350)</label>
                <span>40,177 BTC</span>
                <small>JAPAN TREASURY</small>
            </div>
            <div class="inst-box" style="border-left-color: var(--primary);">
                <label>🇧🇷 HASH11 (B3)</label>
                <span>5,440 BTC</span>
                <small>NASDAQ INDEX</small>
            </div>
            <div class="inst-box" style="border-left-color: #fff;">
                <label>🇨🇳 CHINAAMC (HK)</label>
                <span>2,603 BTC</span>
                <small>SPOT ETF HK</small>
            </div>
        </div>
    </div>
</main>

<nav>
    <button class="nav-item active" onclick="tabs(event, 'b3')">
        <div class="indicator"></div> B3 RADAR
    </button>
    <button class="nav-item crypto-active" onclick="tabs(event, 'crypto')">
        <div class="indicator"></div> BTC TREASURIES
    </button>
</nav>

<script>
    function tabs(e, id) {
        document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.nav-item').forEach(b => b.classList.remove('active'));
        document.getElementById(id).classList.add('active');
        e.currentTarget.classList.add('active');
        // Feedback tátil para mobile
        if (window.navigator.vibrate) window.navigator.vibrate(12);
    }
</script>

</body>
</html>
