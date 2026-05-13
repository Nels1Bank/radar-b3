
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar v6.0 | Dashboard</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #020617;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --up: #10b981;
            --down: #ef4444;
            --glass: rgba(15, 23, 42, 0.95);
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { font-family: 'JetBrains Mono', monospace; background: var(--bg); color: #f8fafc; margin: 0; padding: 10px; }

        .terminal { width: 100%; max-width: 480px; margin: auto; background: var(--glass); border: 1px solid #1e293b; border-radius: 16px; padding: 12px; }
        
        h1 { font-family: 'Orbitron', sans-serif; color: var(--primary); font-size: 1rem; text-align: center; letter-spacing: 2px; margin: 10px 0; }

        /* Sistema de Navegação (Paginação por Abas) */
        .nav-tabs { display: flex; gap: 5px; margin-bottom: 15px; background: #000; padding: 5px; border-radius: 10px; border: 1px solid #1e293b; }
        .tab-btn { flex: 1; padding: 10px; border: none; background: transparent; color: #64748b; font-family: 'Orbitron', sans-serif; font-size: 0.65rem; cursor: pointer; border-radius: 6px; transition: 0.3s; }
        .tab-btn.active { background: var(--primary); color: #000; font-weight: bold; }
        .tab-btn.crypto-tab.active { background: var(--crypto); }

        .tab-content { display: none; }
        .tab-content.active { display: block; animation: fadeIn 0.4s ease; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(5px); } to { opacity: 1; transform: translateY(0); } }

        /* Ticker e Widgets */
        .ticker-stream { background: #000; border: 1px solid #1e293b; border-radius: 8px; padding: 10px 0; overflow: hidden; margin-bottom: 15px; }
        .track { display: inline-block; white-space: nowrap; animation: scroll 25s linear infinite; }
        .asset { display: inline-block; padding: 0 15px; border-right: 1px solid #1e293b; font-size: 0.75rem; }
        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        .widget-box { border-radius: 12px; overflow: hidden; border: 1px solid #1e293b; background: #000; }
        .crypto-border { border: 2px solid var(--crypto); box-shadow: 0 0 15px rgba(245, 158, 11, 0.1); }

        /* Grade Institucional */
        .inst-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--crypto); border-top: 1px solid var(--crypto); }
        .inst-card { padding: 10px; background: #000; }
        .inst-card h3 { font-size: 0.5rem; color: #64748b; margin: 0; }
        .inst-card p { font-size: 0.7rem; color: #fff; margin: 4px 0; font-weight: bold; }
        .inst-card span { font-size: 0.55rem; color: var(--up); }

        footer { margin-top: 20px; text-align: center; font-size: 8px; color: var(--up); opacity: 0.6; text-transform: uppercase; }
    </style>
</head>
<body>

<div class="terminal">
    <h1>NELS1-RADAR v6.0</h1>

    <!-- Letreiro Global -->
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

    <!-- Navegação por Abas -->
    <div class="nav-tabs">
        <button class="tab-btn active" onclick="openTab(event, 'b3-panel')">B3 STOCKS</button>
        <button class="tab-btn crypto-tab" onclick="openTab(event, 'crypto-panel')">CRYPTO / INST</button>
    </div>

    <!-- Painel B3 -->
    <div id="b3-panel" class="tab-content active">
        <div class="widget-box" style="height: 400px;">
            <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
            {
              "width": "100%", "height": "100%", "defaultColumn": "overview",
              "defaultScreen": "top_losers", "market": "brazil",
              "showToolbar": false, "colorTheme": "dark", "locale": "br"
            }
            </script>
        </div>
    </div>

    <!-- Painel Crypto -->
    <div id="crypto-panel" class="tab-content">
        <div class="crypto-border" style="border-radius: 12px; overflow: hidden;">
            <div style="height: 300px;">
                <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="300px" frameborder="0" style="border:0;"></iframe>
            </div>
            <div class="inst-grid">
                <div class="inst-card"><h3>🇺🇸 MSTR</h3><p>214k BTC</p><span>SAYLOR</span></div>
                <div class="inst-card"><h3>🇯🇵 METAPLANET</h3><p>117 BTC</p><span>ASIA</span></div>
                <div class="inst-card"><h3>🇧🇷 HASH11</h3><p>ETF LEADER</p><span>B3</span></div>
                <div class="inst-card"><h3>🇨🇳 HARVEST</h3><p>HK SPOT</p><span>CHINA</span></div>
            </div>
        </div>
    </div>

    <footer>Monitoramento Técnico | Nels1Bank Protocol</footer>
</div>

<script>
    function openTab(evt, tabName) {
        var i, tabcontent, tablinks;
        tabcontent = document.getElementsByClassName("tab-content");
        for (i = 0; i < tabcontent.length; i++) { tabcontent[i].className = tabcontent[i].className.replace(" active", ""); }
        tablinks = document.getElementsByClassName("tab-btn");
        for (i = 0; i < tablinks.length; i++) { tablinks[i].className = tablinks[i].className.replace(" active", ""); }
        document.getElementById(tabName).className += " active";
        evt.currentTarget.className += " active";
    }
</script>

</body>
</html>
