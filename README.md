
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar | Terminal</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Rajdhani:wght@500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #030712;
            --primary: #0ea5e9;
            --secondary: #22c55e;
            --glass: rgba(15, 23, 42, 0.7);
            --neon-glow: 0 0 15px rgba(14, 165, 233, 0.4);
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

        body { 
            font-family: 'Rajdhani', sans-serif; 
            background: radial-gradient(circle at top, #1e1b4b 0%, #030712 100%);
            background-attachment: fixed;
            color: #e2e8f0; 
            margin: 0; padding: 15px;
            min-height: 100vh;
            display: flex; justify-content: center;
        }

        .container { 
            width: 100%; max-width: 500px;
            background: var(--glass);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px; padding: 25px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.6);
        }

        header { text-align: center; margin-bottom: 30px; }

        h1 { 
            font-family: 'Orbitron', sans-serif;
            color: var(--primary); font-size: 1.3rem;
            text-transform: uppercase; letter-spacing: 3px;
            margin: 0; text-shadow: var(--neon-glow);
        }

        .status-indicator {
            font-size: 0.6rem; color: var(--secondary);
            text-transform: uppercase; margin-top: 5px;
            display: flex; align-items: center; justify-content: center; gap: 5px;
        }

        .status-dot { 
            width: 6px; height: 6px; background: var(--secondary); 
            border-radius: 50%; animation: blink 1.5s infinite;
        }

        /* Ticker Futurista */
        .ticker-panel {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 16px; padding: 15px 0;
            margin-bottom: 25px; overflow: hidden;
            box-shadow: inset 0 0 20px rgba(0,0,0,0.5);
        }

        .ticker-track {
            display: inline-block; white-space: nowrap;
            animation: ticker-scroll 25s linear infinite;
        }

        .ticker-item {
            display: inline-block; padding: 0 30px;
            font-weight: 700; font-size: 1rem;
        }

        .ticker-item span { color: var(--secondary); font-family: 'Orbitron', sans-serif; }
        .ticker-item small { 
            color: #64748b; font-size: 0.7rem; 
            display: block; text-transform: uppercase; margin-top: 2px;
        }

        @keyframes ticker-scroll {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        @keyframes blink {
            0%, 100% { opacity: 1; } 50% { opacity: 0.3; }
        }

        /* Widget Área */
        .market-view {
            border-radius: 18px; overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.08);
            height: 520px; box-shadow: 0 10px 30px rgba(0,0,0,0.4);
        }

        footer {
            margin-top: 25px; text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            padding-top: 15px;
        }

        .disclaimer {
            color: var(--secondary); font-size: 8px;
            opacity: 0.8; letter-spacing: 0.5px;
            line-height: 1.4;
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>Nels1Radar</h1>
        <div class="status-indicator">
            <div class="status-dot"></div> Sistema Operacional v3.0
        </div>
    </header>
    
    <div class="ticker-panel">
        <div class="ticker-track">
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo Luxo</small></div>
            <div class="ticker-item"><span>SBSP3</span><small>Saneamento</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Banking</small></div>
            <div class="ticker-item"><span>GUAR3</span><small>Varejo</small></div>
            <!-- Loop -->
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo Luxo</small></div>
            <div class="ticker-item"><span>SBSP3</span><small>Saneamento</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Banking</small></div>
            <div class="ticker-item"><span>GUAR3</span><small>Varejo</small></div>
        </div>
    </div>

    <div class="market-view">
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
        <p class="disclaimer">Atenção: Este ambiente é estritamente para monitoramento técnico de ativos de mercado. Nenhuma informação aqui contida constitui indicação de compra ou venda.</p>
    </footer>
</div>

</body>
</html>
