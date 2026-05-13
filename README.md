<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nels1Radar - Monitoramento</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            --card-bg: rgba(30, 41, 59, 0.7);
            --neon-blue: #00f2ff;
            --neon-green: #39ff14;
            --text-main: #f8fafc;
        }

        body { 
            font-family: 'Inter', sans-serif; 
            background: var(--bg-gradient); 
            background-attachment: fixed;
            color: var(--text-main); 
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        .container { 
            width: 100%;
            max-width: 1100px; 
            border: 2px solid var(--neon-blue); 
            border-radius: 20px; 
            padding: 40px; 
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            box-shadow: 0 0 20px rgba(0, 242, 255, 0.2);
        }

        h1 { 
            font-family: 'Orbitron', sans-serif;
            color: var(--neon-blue); 
            text-align: center; 
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 0 0 10px rgba(0, 242, 255, 0.5);
        }

        /* --- Letreiro Neon (Ticker) --- */
        .ticker-wrapper {
            overflow: hidden;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid var(--neon-green);
            border-radius: 10px;
            padding: 15px 0;
            margin-bottom: 40px;
            white-space: nowrap;
            box-shadow: inset 0 0 10px rgba(57, 255, 20, 0.2);
        }

        .ticker-move {
            display: inline-block;
            animation: ticker-animation 25s linear infinite;
        }

        .asset-item {
            display: inline-block;
            padding: 0 40px;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .asset-item span {
            color: var(--neon-green);
            margin-right: 8px;
        }

        .asset-item small {
            color: #94a3b8;
            font-size: 0.8em;
            text-transform: uppercase;
        }

        @keyframes ticker-animation {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- Widget TradingView --- */
        .widget-area {
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid #334155;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        footer {
            margin-top: 40px;
            padding: 20px;
            font-size: 0.85rem;
            color: #94a3b8;
            text-align: center;
            border-top: 1px dashed #334155;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>📈 Nels1Radar: Monitoramento de Ativos</h1>
    
    <div class="ticker-wrapper">
        <div class="ticker-move">
            <div class="asset-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="asset-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="asset-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="asset-item"><span>AURE3</span><small>Energia</small></div>
            <div class="asset-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="asset-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>SOL</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>PETR4</span><small>Energia</small></div>
            <!-- Clone para Loop -->
            <div class="asset-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="asset-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="asset-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="asset-item"><span>AURE3</span><small>Energia</small></div>
            <div class="asset-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="asset-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>SOL</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>PETR4</span><small>Energia</small></div>
        </div>
    </div>

    <div class="widget-area">
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
        {
        "width": "100%",
        "height": 550,
        "defaultColumn": "overview",
        "defaultScreen": "top_losers",
        "market": "brazil",
        "showToolbar": false,
        "colorTheme": "dark",
        "locale": "br",
        "symbolEdit": false
        }
        </script>
    </div>

    <footer>
        <p><strong>Compliance Nels1Radar:</strong> Visualização de dados públicos de mercado. Não constitui recomendação de ativos. Uso exclusivo para acompanhamento técnico.</p>
    </footer>
</div>

</body>
</html>
