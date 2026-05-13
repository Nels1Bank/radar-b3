<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Nels1Bank - Monitor de Ativos Reais</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; background-color: #0d1117; color: #c9d1d9; padding: 20px; }
        .container { max-width: 900px; margin: auto; border: 1px solid #30363d; border-radius: 8px; padding: 25px; background-color: #161b22; }
        h1 { color: #58a6ff; text-align: center; border-bottom: 1px solid #30363d; padding-bottom: 15px; }
        .status-bar { background: #21262d; padding: 12px; border-radius: 5px; margin-bottom: 20px; text-align: center; font-weight: bold; color: #58a6ff; border: 1px solid #388bfd; }
        .asset-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 15px; margin-bottom: 30px; }
        .asset-card { background: #0d1117; border: 1px solid #30363d; padding: 15px; border-radius: 6px; text-align: center; }
        .ticker { color: #aff5b4; font-weight: bold; font-size: 1.1em; }
    </style>
</head>
<body>

<div class="container">
    <h1>📈 Nels1Bank: Monitoramento de Ativos</h1>
    
    <div class="status-bar">
        Acompanhamento de Fluxo e Ativos de Infraestrutura / Valor
    </div>

    <!-- Lista de 5 Ativos do Radar -->
    <div class="asset-grid">
        <div class="asset-card">
            <span class="ticker">ECOR3</span><br>
            <small>Concessões</small>
        </div>
        <div class="asset-card">
            <span class="ticker">MTRE3</span><br>
            <small>Imobiliário</small>
        </div>
        <div class="asset-card">
            <span class="ticker">AZZAS3</span><br>
            <small>Varejo Luxo</small>
        </div>
        <div class="asset-card">
            <span class="ticker">AURE3</span><br>
            <small>Energia</small>
        </div>
        <div class="asset-card">
            <span class="ticker">BBAS3</span><br>
            <small>Bancário</small>
        </div>
    </div>

    <!-- Widget Automático de Quedas (Sem viés de recomendação) -->
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

    <p style="font-size: 0.8em; color: #8b949e; margin-top: 20px; text-align: center;">
        <em>Nota: Este painel destina-se apenas ao acompanhamento de métricas de mercado. Não constitui oferta ou recomendação de compra/venda.</em>
    </p>
</div>

</body>
</html>
