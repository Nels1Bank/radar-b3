<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar</title>
    <!-- Fontes Modernas -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #020617;
            --card: #0f172a;
            --neon-blue: #38bdf8;
            --neon-green: #4ade80;
            --border: #1e293b;
        }

        body { 
            font-family: 'Inter', sans-serif; 
            background-color: var(--bg); 
            color: #f1f5f9; 
            margin: 0; padding: 10px;
            overflow-x: hidden;
        }

        .container { 
            width: 100%; box-sizing: border-box;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 16px; padding: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.4);
        }

        h1 { 
            font-family: 'Orbitron', sans-serif;
            color: var(--neon-blue); text-align: center; 
            font-size: 1.2rem; margin: 10px 0 20px 0;
            letter-spacing: 1px; text-transform: uppercase;
        }

        /* Letreiro Dinâmico Otimizado para Mobile */
        .ticker-wrap {
            background: #000; border: 1px solid var(--border);
            border-radius: 8px; padding: 10px 0;
            overflow: hidden; margin-bottom: 20px;
        }

        .ticker-move {
            display: inline-block; white-space: nowrap;
            animation: move-left 20s linear infinite;
        }

        .ticker-item {
            display: inline-block; padding: 0 25px;
            font-size: 0.9rem; font-weight: 700;
        }

        .ticker-item span { color: var(--neon-green); margin-right: 5px; }
        .ticker-item small { color: #94a3b8; font-size: 0.7rem; font-weight: 400; }

        @keyframes move-left {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .tradingview-widget-container {
            border-radius: 12px; overflow: hidden;
            border: 1px solid var(--border);
            height: 500px; /* Altura ideal para scroll no celular */
        }

        footer {
            margin-top: 20px; text-align: center;
            font-size: 0.7rem; color: #475569;
            padding: 10px; border-top: 1px solid var(--border);
        }
    </style>
</head>
<body>

<div class="container">
    <h1>📈 Nels1Radar: Monitoramento de Ativos</h1>
    
    <div class="ticker-wrap">
        <div class="ticker-move">
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>AURE3</span><small>Energia</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="ticker-item"><span>PETR4</span><small>Energia</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
            <!-- Loop -->
            <div class="ticker-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="ticker-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="ticker-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="ticker-item"><span>AURE3</span><small>Energia</small></div>
            <div class="ticker-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="ticker-item"><span>PETR4</span><small>Energia</small></div>
            <div class="ticker-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="ticker-item"><span>SOL</span><small>Ativo Digital</small></div>
        </div>
    </div>

    <div class="tradingview-widget-container">
        <div class="tradingview-widget-container__widget"></div>
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
        Monitoramento de ativos reais e digitais. Dados públicos B3 e Cripto.
    </footer>
</div>

</body>
</html>
