<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nels1Radar - Monitor de Mercado</title>
    <style>
        :root {
            --bg: #0d1117;
            --card-bg: #161b22;
            --accent: #58a6ff;
            --text: #c9d1d9;
            --ticker-color: #aff5b4;
        }

        body { 
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif; 
            background-color: var(--bg); 
            color: var(--text); 
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        .container { 
            width: 100%;
            max-width: 1100px; 
            border: 1px solid #30363d; 
            border-radius: 12px; 
            padding: 30px; 
            background-color: var(--card-bg);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        h1 { 
            color: var(--accent); 
            text-align: center; 
            font-size: 1.8rem;
            margin-bottom: 25px;
            letter-spacing: 1px;
        }

        /* --- Estilo do Letreiro (Ticker) --- */
        .ticker-wrapper {
            overflow: hidden;
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 50px;
            padding: 12px 0;
            margin-bottom: 30px;
            white-space: nowrap;
        }

        .ticker-move {
            display: inline-block;
            animation: ticker-animation 30s linear infinite;
        }

        .asset-item {
            display: inline-block;
            padding: 0 30px;
            font-weight: bold;
        }

        .asset-item span {
            color: var(--ticker-color);
            margin-right: 5px;
        }

        .asset-item small {
            color: #8b949e;
            font-weight: normal;
            font-size: 0.8em;
        }

        @keyframes ticker-animation {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- Widget TradingView --- */
        .widget-area {
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #30363d;
        }

        footer {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #30363d;
            font-size: 0.8rem;
            color: #8b949e;
            text-align: center;
            line-height: 1.5;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>📈 Nels1Radar: Painel de Monitoramento</h1>
    
    <!-- Letreiro Dinâmico Lateral -->
    <div class="ticker-wrapper">
        <div class="ticker-move">
            <div class="asset-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="asset-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="asset-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="asset-item"><span>AURE3</span><small>Energia</small></div>
            <div class="asset-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="asset-item"><span>ITUB4</span><small>Bancário</small></div>
            <div class="asset-item"><span>PETR4</span><small>Energia</small></div>
            <div class="asset-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>SOL</span><small>Ativo Digital</small></div>
            <!-- Repetição para o efeito infinito suave -->
            <div class="asset-item"><span>ECOR3</span><small>Logística</small></div>
            <div class="asset-item"><span>MTRE3</span><small>Imobiliário</small></div>
            <div class="asset-item"><span>AZZAS3</span><small>Varejo</small></div>
            <div class="asset-item"><span>AURE3</span><small>Energia</small></div>
            <div class="asset-item"><span>BBAS3</span><small>Bancário</small></div>
            <div class="asset-item"><span>ITUB4</span><small>Bancário</small></div>
            <div class="asset-item"><span>PETR4</span><small>Energia</small></div>
            <div class="asset-item"><span>BTC</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>ETH</span><small>Ativo Digital</small></div>
            <div class="asset-item"><span>SOL</span><small>Ativo Digital</small></div>
        </div>
    </div>

    <!-- Widget de Mercado (Automático) -->
    <div class="widget-area">
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
        {
        "width": "100%",
        "height": 500,
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
        <p><strong>Aviso Legal:</strong> Este painel é uma ferramenta de visualização de dados públicos de mercado. Não constitui oferta ou recomendação de ativos. Dados processados para fins de acompanhamento técnico.</p>
    </footer>
</div>

</body>
</html>
