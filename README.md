
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v7.1</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surface: #0a0f1e;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --up: #10b981;
            --down: #ef4444;
            --border: #1e293b;
            --header-h: 75px;
            --nav-h: 65px;
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        
        html, body { 
            height: 100vh; width: 100vw; margin: 0; padding: 0; 
            overflow: hidden; background: var(--bg); color: #f8fafc;
            font-family: 'JetBrains Mono', monospace;
        }

        body { display: flex; flex-direction: column; }

        /* Header fixo com altura definida */
        header {
            height: var(--header-h);
            background: #000;
            border-bottom: 1px solid var(--border);
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        h1 { 
            font-family: 'Orbitron', sans-serif; color: var(--primary); 
            font-size: 0.8rem; text-align: center; margin: 0; letter-spacing: 2px;
        }

        .ticker-stream { 
            background: #000; overflow: hidden; white-space: nowrap; padding: 4px 0;
            border-top: 1px solid #111;
        }

        .track { display: inline-block; animation: scroll 20s linear infinite; }
        .asset { padding: 0 15px; font-size: 0.65rem; border-right: 1px solid var(--border); }
        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        /* Main ajustado dinamicamente para o monitor */
        main {
            height: calc(100vh - var(--header-h) - var(--nav-h));
            width: 100%;
            position: relative;
        }

        .tab-content { 
            position: absolute; inset: 0;
            display: none; padding: 10px;
            flex-direction: column;
        }
        .tab-content.active { display: flex; }

        .card { 
            flex: 1; background: var(--surface); 
            border-radius: 8px; border: 1px solid var(--border); 
            overflow: hidden; margin-bottom: 8px;
        }

        .crypto-border { border: 1px solid var(--crypto); box-shadow: inset 0 0 10px rgba(245, 158, 11, 0.1); }

        /* Grade Institucional Compacta */
        .inst-grid { 
            height: 100px; display: grid; grid-template-columns: 1fr 1fr; 
            gap: 1px; background: var(--crypto); border: 1px solid var(--crypto);
            border-radius: 6px; overflow: hidden; flex-shrink: 0;
        }
        .inst-item { background: #000; padding: 6px 10px; display: flex; flex-direction: column; justify-content: center; }
        .inst-item label { font-size: 0.5rem; color: #64748b; text-transform: uppercase; }
        .inst-item value { font-size: 0.7rem; font-weight: bold; color: #fff; margin: 2px 0; }
        .inst-item status { font-size: 0.55rem; color: var(--up); }

        /* Navegação Inferior */
        nav {
            height: var(--nav-h);
            display: flex; justify-content: space-around; align-items: center;
            background: #050505; border-top: 1px solid var(--border);
            padding-bottom: env(safe-area-inset-bottom);
        }

        .nav-btn {
            background: none; border: none; color: #475569;
            font-family: 'Orbitron', sans-serif; font-size: 0.6rem;
            display: flex; flex-direction: column; align-items: center; gap: 4px; transition: 0.2s;
        }

        .nav-btn.active { color: var(--primary); }
        .nav-btn.crypto-btn.active { color: var(--crypto); }
        .nav-line { width: 18px; height: 2px; background: currentColor; border-radius: 1px; }

    </style>
</head>
<body>

<header>
    <h1>NELS1-RADAR v7.1</h1>
    <div class="ticker-stream">
        <div class="track">
            <span class="asset"><b>BTC</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>SBSP3</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>BBAS3</b> <span style="color:var(--down)">▼</span></span>
            <span class="asset"><b>SOL</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>ETH</b> <span style="color:var(--up)">▲</span></span>
            <!-- Loop -->
            <span class="asset"><b>BTC</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>SBSP3</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>BBAS3</b> <span style="color:var(--down)">▼</span></span>
            <span class="asset"><b>SOL</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>ETH</b> <span style="color:var(--up)">▲</span></span>
        </div>
    </div>
</header>

<main>
    <div id="b3" class="tab-content active">
        <div class="card">
            <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
            {
              "width": "100%", "height": "100%", "defaultColumn": "overview",
              "defaultScreen": "top_losers", "market": "brazil",
              "showToolbar": false, "colorTheme": "dark", "locale": "br"
            }
            </script>
        </div>
    </div>

    <div id="crypto" class="tab-content">
        <div class="card crypto-border">
            <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=6&pref_coin_id=1505" width="100%" height="100%" frameborder="0" style="border:0;"></iframe>
        </div>
        
        <div class="inst-grid">
            <div class="inst-item">
                <label>🇺🇸 MicroStrategy</label>
                <value>226,331 BTC</value>
                <status>[OFFICIAL MAY-26]</status>
            </div>
            <div class="inst-item">
                <label>🇯🇵 Metaplanet</label>
                <value>141.07 BTC</value>
                <status>[ASIA PROXY]</status>
            </div>
            <div class="inst-item">
                <label>🇧🇷 HASH11 (B3)</label>
                <value>ETF Leader</value>
                <status>[LOCAL HUB]</status>
            </div>
            <div class="inst-item">
                <label>🇨🇳 Harvest (HK)</label>
                <value>Spot ETF</value>
                <status>[CHINA FLOW]</status>
            </div>
        </div>
    </div>
</main>

<nav>
    <button class="nav-btn active" onclick="switchTab(event, 'b3')">
        <div class="nav-line"></div> B3 STOCKS
    </button>
    <button class="nav-btn crypto-btn" onclick="switchTab(event, 'crypto')">
        <div class="nav-line"></div> CRYPTO INST
    </button>
</nav>

<script>
    function switchTab(evt, tabId) {
        document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
        document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
        document.getElementById(tabId).classList.add('active');
        evt.currentTarget.classList.add('active');
        if (window.navigator.vibrate) window.navigator.vibrate(10);
    }
</script>

</body>
</html>
