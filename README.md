
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v6.2 | Terminal Profissional</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surface: #0f172a;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --up: #10b981;
            --down: #ef4444;
            --text-dim: #94a3b8;
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        
        body { 
            font-family: 'JetBrains Mono', monospace; 
            background: var(--bg); 
            color: #f8fafc; 
            margin: 0; 
            padding: 0;
            overflow-x: hidden;
            display: flex;
            flex-direction: column;
            height: 100vh;
        }

        /* Header e Ticker Fixo */
        header {
            background: rgba(0, 0, 0, 0.9);
            padding: 10px 0;
            border-bottom: 1px solid #1e293b;
            z-index: 100;
        }

        h1 { 
            font-family: 'Orbitron', sans-serif; 
            color: var(--primary); 
            font-size: 0.9rem; 
            text-align: center; 
            margin: 5px 0;
            letter-spacing: 3px;
        }

        .ticker-stream { 
            background: #000; 
            overflow: hidden; 
            white-space: nowrap; 
            padding: 8px 0;
            border-bottom: 1px solid #1e293b;
        }

        .track { display: inline-block; animation: scroll 20s linear infinite; }
        .asset { padding: 0 20px; font-size: 0.75rem; border-right: 1px solid #1e293b; }
        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        /* Conteúdo Principal */
        main {
            flex: 1;
            overflow-y: auto;
            padding: 15px;
            padding-bottom: 90px;
        }

        .tab-content { display: none; }
        .tab-content.active { display: block; animation: slideUp 0.3s ease-out; }

        @keyframes slideUp { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        .card { 
            background: var(--surface); 
            border-radius: 12px; 
            border: 1px solid #1e293b; 
            overflow: hidden; 
            margin-bottom: 15px;
        }

        .crypto-accent { border: 2px solid var(--crypto); }

        /* Painel Institucional */
        .inst-grid { 
            display: grid; 
            grid-template-columns: 1fr 1fr; 
            gap: 1px; 
            background: var(--crypto); 
        }
        .inst-item { background: #000; padding: 12px; }
        .inst-item label { font-size: 0.55rem; color: var(--text-dim); display: block; margin-bottom: 4px; }
        .inst-item value { font-size: 0.8rem; font-weight: bold; display: block; }
        .inst-item status { font-size: 0.6rem; color: var(--up); font-weight: bold; }

        /* Navegação Inferior (UX Pro) */
        nav {
            position: fixed;
            bottom: 0;
            width: 100%;
            background: rgba(15, 23, 42, 0.98);
            backdrop-filter: blur(15px);
            display: flex;
            justify-content: space-around;
            padding: 15px 0;
            border-top: 1px solid #1e293b;
            z-index: 1000;
        }

        .nav-btn {
            background: none;
            border: none;
            color: var(--text-dim);
            font-family: 'Orbitron', sans-serif;
            font-size: 0.65rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 6px;
            cursor: pointer;
            transition: 0.2s;
        }

        .nav-btn.active { color: var(--primary); }
        .nav-btn.crypto-btn.active { color: var(--crypto); }
        .nav-btn .icon-bar { width: 24px; height: 3px; background: currentColor; border-radius: 2px; }

    </style>
</head>
<body>

<header>
    <h1>NELS1-RADAR v6.2</h1>
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
    <!-- Aba B3: Foco em Ações -->
    <div id="b3" class="tab-content active">
        <div class="card" style="height: 520px;">
            <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
            {
              "width": "100%", "height": "100%", "defaultColumn": "overview",
              "defaultScreen": "top_losers", "market": "brazil",
              "showToolbar": false, "colorTheme": "dark", "locale": "br"
            }
            </script>
        </div>
    </div>

    <!-- Aba Crypto: Preços e Institucionais (DADOS ATUALIZADOS MAIO/26) -->
    <div id="crypto" class="tab-content">
        <div class="card crypto-accent">
            <div style="height: 340px;">
                <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="340px" frameborder="0" style="border:0;"></iframe>
            </div>
            <div class="inst-grid">
                <div class="inst-item">
                    <label>🇺🇸 MICROSTRATEGY</label>
                    <value>226,331 BTC</value>
                    <status>HODL RESERVE</status>
                </div>
                <div class="inst-item">
                    <label>🇯🇵 METAPLANET</label>
                    <value>141.07 BTC</value>
                    <status>YEN HEDGE</status>
                </div>
                <div class="inst-item">
                    <label>🇧🇷 HASH11 (B3)</label>
                    <value>LÍDER ETF</value>
                    <status>LOCAL HUB</status>
                </div>
                <div class="inst-item">
                    <label>🇨🇳 HARVEST (HK)</label>
                    <value>SPOT ETF</value>
                    <status>CHINA PROXY</status>
                </div>
            </div>
        </div>
        <div style="font-size: 0.6rem; color: var(--text-dim); text-align: center; padding: 10px; border: 1px dashed #334155; border-radius: 8px;">
            DADOS INSTITUCIONAIS ATUALIZADOS: MAIO 2026
        </div>
    </div>
</main>

<nav>
    <button class="nav-btn active" onclick="switchTab(event, 'b3')">
        <div class="icon-bar"></div>
        B3 STOCKS
    </button>
    <button class="nav-btn crypto-btn" onclick="switchTab(event, 'crypto')">
        <div class="icon-bar"></div>
        CRYPTO INST
    </button>
</nav>

<script>
    function switchTab(evt, tabId) {
        const contents = document.querySelectorAll('.tab-content');
        const buttons = document.querySelectorAll('.nav-btn');
        
        contents.forEach(c => c.classList.remove('active'));
        buttons.forEach(b => b.classList.remove('active'));
        
        document.getElementById(tabId).classList.add('active');
        evt.currentTarget.classList.add('active');
        
        if (window.navigator.vibrate) { window.navigator.vibrate(12); }
    }
</script>

</body>
</html>
