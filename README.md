<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v11.0 | Dashboard</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surface: #0d1117;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --up: #10b981;
            --border: #30363d;
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

        /* Header Dinâmico */
        header { flex-shrink: 0; border-bottom: 1px solid var(--border); padding: 6px 0; }
        h1 { font-family: 'Orbitron', sans-serif; font-size: 0.75rem; text-align: center; color: var(--primary); }

        .ticker { overflow: hidden; white-space: nowrap; background: #000; padding: 4px 0; font-size: 0.6rem; border-top: 1px solid #111; }
        .track { display: inline-block; animation: scroll 15s linear infinite; }
        .asset { padding: 0 12px; border-right: 1px solid var(--border); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        /* Area de Visualização */
        main { flex-grow: 1; position: relative; overflow: hidden; width: 100%; }
        .tab-content { 
            display: none; height: 100%; width: 100%; 
            padding: 8px; flex-direction: column; gap: 6px;
        }
        .tab-content.active { display: flex; }

        .card { 
            flex: 1; background: var(--surface); 
            border: 1px solid var(--border); 
            border-radius: 6px; overflow: hidden; 
        }

        /* Painel Institucional (BitcoinTreasuries Data) */
        .inst-panel {
            display: grid; grid-template-columns: 1fr 1fr;
            gap: 5px; flex-shrink: 0;
        }
        .inst-box {
            background: #161b22; border: 1px solid var(--border);
            padding: 10px; border-radius: 6px; border-left: 3px solid var(--crypto);
        }
        .inst-box label { font-size: 0.5rem; color: #8b949e; display: block; margin-bottom: 2px; }
        .inst-box span { font-size: 0.7rem; font-weight: bold; color: #fff; display: block; }
        .inst-box small { font-size: 0.5rem; color: var(--up); font-weight: bold; }

        /* Navegação Fixa na Base */
        nav {
            display: flex; height: 60px; background: #010409;
            border-top: 1px solid var(--border); padding-bottom: env(safe-area-inset-bottom);
        }
        .nav-item {
            flex: 1; border: none; background: none; color: #484f58;
            font-family: 'Orbitron', sans-serif; font-size: 0.6rem;
            display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 4px;
        }
        .nav-item.active { color: var(--primary); background: #0d1117; }
        .nav-item.crypto-active.active { color: var(--crypto); }
        .indicator { width: 15px; height: 2px; background: currentColor; border-radius: 1px; }

    </style>
</head>
<body>

<header>
    <h1>NELS1-RADAR v11.0</h1>
    <div class="ticker">
        <div class="track">
            <span class="asset">BTC/USD $80,340 ▲</span>
            <span class="asset">BBAS3 R$ 26.45 ▼</span>
            <span class="asset">SBSP3 R$ 82.10 ▲</span>
            <span class="asset">SOL/USD $174.50 ▲</span>
            <span class="asset">BTC/USD $80,340 ▲</span>
            <span class="asset">BBAS3 R$ 26.45 ▼</span>
            <span class="asset">SBSP3 R$ 82.10 ▲</span>
            <span class="asset">SOL/USD $174.50 ▲</span>
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
        <div class="card" style="border-color: var(--crypto); flex: 0.7;">
            <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="100%" frameborder="0"></iframe>
        </div>
        
        <div class="inst-panel">
            <div class="inst-box">
                <label>🇺🇸 STRATEGY INC (MSTR)</label>
                <span>818,869 BTC</span>
                <small>+9.4% YIELD</small>
            </div>
            <div class="inst-box">
                <label>🇯🇵 METAPLANET</label>
                <span>40,177 BTC</span>
                <small>ASIA LEADER</small>
            </div>
            <div class="inst-box" style="border-left-color: #2196f3;">
                <label>🌐 21 CAPITAL</label>
                <span>43,514 BTC</span>
                <small>ETF FLOW</small>
            </div>
            <div class="inst-box" style="border-left-color: #fff;">
                <label>⛏️ MARA HOLDINGS</label>
                <span>35,303 BTC</span>
                <small>HODL MINER</small>
            </div>
        </div>
    </div>
</main>

<nav>
    <button class="nav-item active" onclick="tabs(event, 'b3')">
        <div class="indicator"></div> B3 RADAR
    </button>
    <button class="nav-item crypto-active" onclick="tabs(event, 'crypto')">
        <div class="indicator"></div> BITCOIN TREASURIES
    </button>
</nav>

<script>
    function tabs(e, id) {
        document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.nav-item').forEach(b => b.classList.remove('active'));
        document.getElementById(id).classList.add('active');
        e.currentTarget.classList.add('active');
        if (window.navigator.vibrate) window.navigator.vibrate(10);
    }
</script>

</body>
</html>
