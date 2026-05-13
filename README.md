
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar | OS</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #050505;
            --primary: #00e5ff;
            --up: #00ff41;
            --down: #ff0055;
            --glass: rgba(20, 20, 20, 0.95);
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

        body { 
            font-family: 'JetBrains Mono', monospace; 
            background: var(--bg);
            color: #d1d5db; 
            margin: 0; padding: 12px;
            display: flex; justify-content: center;
        }

        .terminal-container { 
            width: 100%; max-width: 480px;
            background: var(--glass);
            border: 1px solid #333;
            border-radius: 12px; padding: 15px;
            box-shadow: 0 0 30px rgba(0,0,0,0.8);
        }

        h1 { 
            font-family: 'Orbitron', sans-serif;
            color: var(--primary); font-size: 1rem;
            text-align: center; letter-spacing: 4px;
            margin: 10px 0;
        }

        .ticker-stream {
            background: #000;
            border: 1px solid #222;
            border-radius: 6px; padding: 12px 0;
            margin: 15px 0; overflow: hidden;
        }

        .track {
            display: inline-block; white-space: nowrap;
            animation: scroll 22s linear infinite;
        }

        .asset {
            display: inline-block; padding: 0 25px;
            border-right: 1px solid #222;
        }

        .asset b { color: #fff; font-size: 0.9rem; }
        .up { color: var(--up); }
        .down { color: var(--down); }
        .asset span { font-size: 0.65rem; color: #666; display: block; text-transform: uppercase; margin-top: 2px; }

        @keyframes scroll {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .market-engine {
            border-radius: 8px; overflow: hidden;
            border: 1px solid #222; height: 450px;
        }

        footer { margin-top: 20px; text-align: center; border-top: 1px dotted #444; padding-top: 10px; }

        .legal {
            color: var(--up); font-size: 8px;
            text-transform: uppercase; opacity: 0.7;
        }
    </style>
</head>
<body>

<div class="terminal-container">
    <h1>NELS1-RADAR v5.4</h1>
    
    <div class="ticker-stream">
        <div class="track">
            <div class="asset"><b>SBSP3</b><span class="up">▲</span><span>Saneamento</span></div>
            <div class="asset"><b>BBAS3</b><span class="down">▼</span><span>Banking</span></div>
            <div class="asset"><b>BTC</b><span class="up">▲</span><span>Digital Asset</span></div>
            <div class="asset"><b>AZZAS3</b><span class="down">▼</span><span>Retail High</span></div>
            <div class="asset"><b>GUAR3</b><span class="up">▲</span><span>Retail</span></div>
            <div class="asset"><b>SOL</b><span class="up">▲</span><span>Solana Network</span></div>
            <!-- Loop -->
            <div class="asset"><b>SBSP3</b><span class="up">▲</span><span>Saneamento</span></div>
            <div class="asset"><b>BBAS3</b><span class="down">▼</span><span>Banking</span></div>
            <div class="asset"><b>BTC</b><span class="up">▲</span><span>Digital Asset</span></div>
            <div class="asset"><b>AZZAS3</b><span class="down">▼</span><span>Retail High</span></div>
            <div class="asset"><b>GUAR3</b><span class="up">▲</span><span>Retail</span></div>
            <div class="asset"><b>SOL</b><span class="up">▲</span><span>Solana Network</span></div>
        </div>
    </div>

    <div class="market-engine">
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
        {
          "width": "100%",
          "height": "100%",
          "defaultColumn": "overview",
          "defaultScreen": "top_losers",
          "market": "brazil",
          "showToolbar": false,
          "colorTheme": "dark",
          "locale": "br"
        }
        </script>
    </div>

    <footer>
        <p class="legal">Atenção: Sistema de monitoramento técnico. Informações não constituem indicação de compra ou venda.</p>
    </footer>
</div>

</body>
</html>
