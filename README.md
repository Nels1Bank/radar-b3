<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Nels1Bank - Monitor de Mercado</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; background-color: #0d1117; color: #c9d1d9; padding: 20px; }
        .container { max-width: 1000px; margin: auto; border: 1px solid #30363d; border-radius: 8px; padding: 25px; background-color: #161b22; }
        h1 { color: #58a6ff; text-align: center; border-bottom: 1px solid #30363d; padding-bottom: 15px; }
        .asset-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 10px; margin-bottom: 30px; }
        .asset-card { background: #21262d; border: 1px solid #30363d; padding: 12px; border-radius: 6px; text-align: center; }
        .ticker { color: #aff5b4; font-weight: bold; }
    </style>
</head>
<body>

<div class="container">
    <h1>Painel de Ativos Financeiros</h1>
    
    <!-- Lista Expandida de Ativos -->
    <div class="asset-grid">
        <div class="asset-card"><span class="ticker">ECOR3</span><br><small>Logística</small></div>
        <div class="asset-card"><span class="ticker">MTRE3</span><br><small>Imobiliário</small></div>
        <div class="asset-card"><span class="ticker">AZZAS3</span><br><small>Varejo</small></div>
        <div class="asset-card"><span class="ticker">AURE3</span><br><small>Energia</small></div>
        <div class="asset-card"><span class="ticker">BBAS3</span><br><small>Bancário</small></div>
        <div class="asset-card"><span class="ticker">ITUB4</span><br><small>Bancário</small></div>
        <div class="asset-card"><span class="ticker">PETR4</span><br><small>Energia</small></div>
        <div class="asset-card"><span class="ticker">BTC</span><br><small>Digital Asset</small></div>
    </div>

    <!-- Widget de Variações de Mercado (Automático) -->
    <div class="tradingview-widget-container">
        <div class="tradingview-widget-container__widget"></div>
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-screener.js" async>
        {
        "width": "100%",
        "height": 450,
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

    <footer style="margin-top: 30px; padding-top: 15px; border-top: 1px solid #30363d; font-size: 0.75em; color: #8b949e; text-align: center;">
        <p>Dados de mercado para fins de monitoramento. Este ambiente não constitui oferta ou recomendação de ativos.</p>
    </footer>
</div>

</body>
</html>
