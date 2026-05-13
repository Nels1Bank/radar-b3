
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar v5.7 | Terminal Híbrido</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #020617;
            --primary: #00e5ff;
            --crypto-accent: #f59e0b; /* Laranja Bitcoin */
            --up: #10b981;
            --down: #ef4444;
            --glass: rgba(15, 23, 42, 0.9);
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

        body { 
            font-family: 'JetBrains Mono', monospace; 
            background: var(--bg); color: #f8fafc; 
            margin: 0; padding: 10px; display: flex; justify-content: center;
        }

        .terminal { 
            width: 100%; max-width: 480px; background: var(--glass);
            border: 1px solid #1e293b; border-radius: 16px; padding: 15px;
            box-shadow: 0 0 40px rgba(0, 229, 255, 0.05);
        }

        h1 { 
            font-family: 'Orbitron', sans-serif; color: var(--primary); 
            font-size: 1.1rem; text-align: center; letter-spacing: 2px;
            text-shadow: 0 0 10px rgba(0, 229, 255, 0.4);
            margin: 10px 0;
        }

        .section-tag {
            font-size: 0.6rem; color: #64748b; text-transform: uppercase;
            margin: 15px 0 5px 5px; border-left: 2px solid var(--primary); padding-left: 8px;
        }

        /* Letreiro Digital (Ticker) */
        .ticker-stream {
            background: #000; border: 1px solid #1e293b;
            border-radius: 8px; padding: 12px 0; overflow: hidden; margin-bottom: 15px;
        }

        .track { display: inline-block; white-space: nowrap; animation: scroll 25s linear infinite; }
        .asset { display: inline-block; padding: 0 20px; border-right: 1px solid #1e293b; }
        .asset b { font-size: 0.85rem; color: #fff; }
        .up { color: var(--up); } .down { color: var(--down); }
        .asset span { font-size: 0.6rem; color: #475569; display: block; text-transform: uppercase; }

        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        /* Estilo dos Containers de Dados */
        .widget-box {
            border-radius: 12px; overflow: hidden;
            border: 1px solid #1e293b; background: #000;
            margin-bottom: 0;
        }

        /* Destaque Laranja para Cripto */
        .crypto-container {
            border: 2px solid var(--crypto-accent);
            border-radius: 12px; overflow: hidden;
            box-shadow: 0 0 15px rgba(245, 158, 11, 0.15);
        }

        /* Grade de Detentores Institucionais */
        .inst-grid {
            display: grid; grid-template-columns: 1fr 1fr; gap: 1px;
            background: var(--crypto-accent); /* Linha de divisão */
            border-top: 1px solid var(--crypto-accent);
        }
        .inst-card {
            padding: 10px; background: #000;
        }
        .inst-card h3 { font-size: 0.55rem; color: #64748b; margin: 0; text-transform: uppercase; }
        .inst-card p { font-size: 0.75rem; color: #fff; margin: 4px 0 0 0; font-weight: bold; }
        .inst-card span { font-size: 0.55rem; color: var(--up); font-weight: bold; }

        footer { margin-top: 25px; text-align: center; border-top: 1px solid #1e293b; padding-top: 15px; }
        .legal { color: var(--up); font-size: 8px; text-transform: uppercase; opacity: 0.8; }
    </style>
</head>
<body>

<div class="terminal">
    <h1>NELS1-RADAR v5.7</h1>
    
    <div class="section-tag">Monitoramento Estratégico</div>
    <div class="ticker-stream">
        <div class="track">
            <div class="asset"><b>BTC</b><span class="up">▲</span><span>Digital Gold</span></div>
            <div class="asset"><b>SBSP3</b><span class="up">▲</span><span>Saneamento</span></div>
            <div class="asset"><b>SOL</b><span class="up">▲</span><span>Solana</span></div>
            <div class="asset"><b>BBAS3</b><span class="down">▼</span><span>Result 1T26</span></div>
            <div class="asset"><b>ETH</b><span class="up">▲</span><span>Ethereum</span></div>
            <div class="asset"><b>AZZAS3</b><span class="down">▼</span><span>Retail</span></div>
            <!-- Loop para animação infinita -->
            <div class="asset"><b>BTC</b><span class="up">▲</span><span>Digital Gold</span></div>
            <div class="asset"><b>SBSP3</b><span class="up">▲</span><span>Saneamento</span></div>
            <div class="asset"><b>SOL</b><span class="up">▲</span><span>Solana</span></div>
            <div class="asset"><b>BBAS3</b><span class="down">▼</span><span>Result 1T26</span></div>
            <div class="asset"><b>ETH</b><span class="up">▲</span><span>Ethereum</span></div>
            <div class="asset"><b>AZZAS3</b><span class="down">▼</span><span>Retail</span></div>
        </div>
    </div>

    <div class="section-tag">Market Screener (B3)</div>
    <div class="widget-box" style="height: 380px; margin-bottom: 15px;">
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
        {
          "width": "100%", "height": "100%", "defaultColumn": "overview",
          "defaultScreen": "top_losers", "market": "brazil",
          "showToolbar": false, "colorTheme": "dark", "locale": "br"
        }
        </script>
    </div>

    <div class="section-tag" style="color: var(--crypto-accent);">Crypto & Institutional Smart Money</div>
    <div class="crypto-container">
        <!-- Feed de Preços Cripto -->
        <div style="height: 320px; background: #000;">
            <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="320px" frameborder="0" style="border:0;"></iframe>
        </div>
        
        <!-- Painel de Detentores Institucionais -->
        <div class="inst-grid">
            <div class="inst-card">
                <h3>🇺🇸 EUA (MicroStrategy)</h3>
                <p>214,400 BTC</p>
                <span>HODL SUPREMO</span>
            </div>
            <div class="inst-card">
                <h3>🇯🇵 JAPÃO (Metaplanet)</h3>
                <p>117+ BTC</p>
                <span>ASIA PROXY</span>
            </div>
            <div class="inst-card">
                <h3>🇧🇷 BRASIL (HASH11)</h3>
                <p>LÍDER ETF</p>
                <span>NATIVE CRYPTO</span>
            </div>
            <div class="inst-card">
                <h3>🇨🇳 CHINA (Harvest/HK)</h3>
                <p>ETF SPOT HK</p>
                <span>INST. ACCESS</span>
            </div>
        </div>
    </div>

    <footer>
        <p class="legal">Atenção: Sistema de monitoramento técnico. Informações não constituem indicação de compra ou venda.</p>
    </footer>
</div>

</body>
</html>
