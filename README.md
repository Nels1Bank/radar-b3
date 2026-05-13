
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v7.0</title>
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
        }

        /* Reset para ocupar 100% da tela sem scroll */
        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        html, body { 
            height: 100%; width: 100%; margin: 0; padding: 0; 
            overflow: hidden; background: var(--bg); color: #f8fafc;
            font-family: 'JetBrains Mono', monospace;
        }

        body { display: flex; flex-direction: column; }

        /* Header Fixo */
        header {
            flex-shrink: 0;
            background: #000;
            border-bottom: 1px solid var(--border);
            padding: 8px 0;
        }

        h1 { 
            font-family: 'Orbitron', sans-serif; color: var(--primary); 
            font-size: 0.85rem; text-align: center; margin: 0; letter-spacing: 2px;
        }

        .ticker-stream { 
            background: #000; overflow: hidden; white-space: nowrap; padding: 5px 0;
            border-bottom: 1px solid var(--border);
        }

        .track { display: inline-block; animation: scroll 20s linear infinite; }
        .asset { padding: 0 15px; font-size: 0.7rem; border-right: 1px solid var(--border); }
        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        /* Área de Conteúdo Adaptável ao Monitor */
        main {
            flex-grow: 1;
            position: relative;
            width: 100%;
            overflow: hidden;
        }

        .tab-content { 
            position: absolute; width: 100%; height: 100%;
            display: none; padding: 10px;
        }
        .tab-content.active { display: flex; flex-direction: column; gap: 10px; }

        .card { 
            flex-grow: 1; background: var(--surface); 
            border-radius: 12px; border: 1px solid var(--border); 
            overflow: hidden; position: relative;
        }

        .crypto-border { border: 2px solid var(--crypto); }

        /* Grade Institucional - Compacta para o Monitor */
        .inst-grid { 
            flex-shrink: 0; display: grid; grid-template-columns: 1fr 1fr; 
            gap: 1px; background: var(--crypto); border: 1px solid var(--crypto);
            border-radius: 8px; overflow: hidden;
        }
        .inst-item { background: #000; padding: 8px 12px; }
        .inst-item label { font-size: 0.5rem; color: #64748b; display: block; }
        .inst-item value { font-size: 0.75rem; font-weight: bold; color: #fff; display: block; }
        .inst-item status { font-size: 0.55rem; color: var(--up); font-weight: bold; }

        /* Navegação Inferior */
        nav {
            flex-shrink: 0; display: flex; justify-content: space-around;
            background: #0f172a; border-top: 1px solid var(--border);
            padding: 10px 0; padding-bottom: max(10px, env(safe-area-inset-bottom));
        }

        .nav-btn {
            background: none; border: none; color: #64748b;
            font-family: 'Orbitron', sans-serif; font-size: 0.6rem;
            display: flex; flex-direction: column; align-items: center; gap: 4px;
        }

        .nav-btn.active { color: var(--primary); }
        .nav-btn.crypto-btn.active { color: var(--crypto); }
        .nav-line { width: 20px; height: 2px; background: currentColor; border-radius: 1px; }

    </style>
</head>
<body>

<header>
    <h1>NELS1-RADAR v7.0</h1>
    <div class="ticker-stream">
        <div class="track">
            <span class="asset"><b>BTC</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>SBSP3</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>BBAS3</b> <span style="color:var(--down)">▼</span></span>
            <span class="asset"><b>SOL</b> <span style="color:var(--up)">▲</span></span>
            <!-- Loop -->
            <span class="asset"><b>BTC</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>SBSP3</b> <span style="color:var(--up)">▲</span></span>
            <span class="asset"><b>BBAS3</b> <span style="color:var(--down)">▼</span></span>
            <span class="asset"><b>SOL</b> <span style="color:var(--up)">▲</span></span>
        </div>
    </div>
</header>

<main>
    <!-- ABA B3: Auto-ajuste de altura -->
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

    <!-- ABA CRYPTO: Dados Oficiais Maio 2026 -->
    <div id="crypto" class="tab-content">
        <div class="card crypto-border">
            <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="100%" frameborder="0" style="border:0;"></iframe>
        </div>
        
        <div class="inst-grid">
            <div class="inst-item">
                <label>🇺🇸 MICROSTRATEGY</label>
                <value>226,331 BTC</value>
                <status>SAYLOR</status>
            </div>
            <div class="inst-item">
                <label>🇯🇵 METAPLANET</label>
                <value>141.07 BTC</value>
                <status>YEN HEDGE</status>
            </div>
            <div class="inst-item">
                <label>🇧🇷 HASH11 (B3)</label>
                <value>LÍDER NACIONAL</value>
                <status>LOCAL HUB</status>
            </div>
            <div class="inst-item">
                <label>🇨🇳 HARVEST (HK)</label>
                <value>SPOT ETF</value>
                <status>CHINA PROXY</status>
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
