</Nels1Radar/>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            --neon-blue: #38bdf8;
            --neon-green: #4ade80;
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        body { 
            font-family: 'Inter', sans-serif; 
            background: var(--bg-gradient); 
            background-attachment: fixed;
            color: #f1f5f9; 
            margin: 0; padding: 15px;
            min-height: 100vh;
        }

        .container { 
            width: 100%;
            background: rgba(15, 23, 42, 0.6); 
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 20px; 
            padding: 20px;
            box-sizing: border-box;
        }

        h1 { 
            font-family: 'Orbitron', sans-serif;
            color: var(--neon-blue); text-align: center; 
            font-size: 1.1rem; margin-bottom: 25px;
            text-transform: uppercase; letter-spacing: 2px;
        }

        .ticker-wrap {
            background: rgba(255, 255, 255, 0.03); 
            border: 1px solid var(--glass-border);
            border-radius: 12px; 
            padding: 12px 0;
            overflow: hidden; 
            margin-bottom: 25px;
        }

        .ticker-move {
            display: inline-block; white-space: nowrap;
            animation: move-left 30s linear infinite;
        }

        .ticker-item {
            display: inline-block; padding: 0 25px;
            font-weight: 700; font-size: 0.9rem;
        }

        .ticker-item span { color: var(--neon-green); margin-right: 5px; }
        .ticker-item small { color: #94a3b8; font-size: 0.7rem; font-weight: 400; }

        @keyframes move-left {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .widget-box {
            border-radius: 15px; overflow: hidden;
            border: 1px solid var(--glass-border);
            height: 500px;
        }

        footer {
            margin-top: 25px; text-align: center;
            padding-top: 15px; border-top: 1px solid var(--glass-border);
        }

        .disclaimer {
            color: var(--neon-green);
            font-size: 8px;
            font-weight: 400;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>📈 Nels1Radar: Monitoramento de Ativos</h1>
    
    <div class="ticker-wrap">
        <div class="ticker-move">
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo Luxo</small></div>
            <div class="ticker-item"><span>GUAR3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>LREN3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="ticker-item"><span>SBSP3</span><small>Saneamento</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
            <!-- Loop -->
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo Luxo</small></div>
            <div class="ticker-item"><span>GUAR3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>LREN3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="ticker-item"><span>SBSP3</span><small>Saneamento</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
        </div>
    </div>

    <div class="widget-box">
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
