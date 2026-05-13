
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #050505;
            --surface: #111111;
            --primary: #00e5ff;
            --crypto-alt: #f59e0b;
            --text: #ffffff;
            --text-dim: #a0a0a0;
            --border: #222222;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            font-family: 'Inter', sans-serif; 
            background: var(--bg); 
            color: var(--text); 
            height: 100vh; 
            display: flex; 
            flex-direction: column;
            overflow: hidden;
        }

        /* Título e Letreiro */
        header { flex-shrink: 0; border-bottom: 1px solid var(--border); padding: 12px 0; background: var(--bg); }
        h1 { font-family: 'Orbitron', sans-serif; font-size: 1rem; text-align: center; color: var(--primary); letter-spacing: 2px; }

        .ticker { background: #000; padding: 8px 0; overflow: hidden; white-space: nowrap; border-bottom: 1px solid var(--border); }
        .track { display: inline-block; animation: scroll 25s linear infinite; font-size: 0.8rem; font-weight: bold; }
        .asset { padding: 0 20px; border-right: 1px solid var(--border); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        /* Conteúdo Principal */
        main { flex-grow: 1; overflow-y: auto; padding: 15px; display: flex; flex-direction: column; gap: 15px; }

        .section-title { font-family: 'Orbitron'; font-size: 0.7rem; color: var(--text-dim); text-transform: uppercase; margin-bottom: 8px; }
        
        .card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; overflow: hidden; flex-shrink: 0; }

        /* Grid de Preços Legível */
        .market-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .price-box { background: var(--surface); border: 1px solid var(--border); padding: 15px; border-radius: 12px; }
        .price-box label { font-size: 0.65rem; color: var(--text-dim); display: block; margin-bottom: 5px; }
        .price-box span { font-size: 1rem; font-weight: 700; color: #fff; }

        /* Footer */
        footer { 
            flex-shrink: 0; 
            padding: 15px; 
            text-align: center; 
            font-size: 0.7rem; 
            color: var(--text-dim); 
            border-top: 1px solid var(--border);
            background: var(--bg);
        }

    </style>
</head>
<body>

<header>
    <h1>Nels1Radar</h1>
    <div class="ticker">
        <div class="track">
            <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
            <span class="asset">METAPLANET: 40,177 BTC ▲</span>
            <span class="asset">21 CAPITAL: 43,514 BTC ▲</span>
            <span class="asset">MARA HOLDINGS: 35,303 BTC ▲</span>
            <!-- Loop -->
            <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
            <span class="asset">METAPLANET: 40,177 BTC ▲</span>
        </div>
    </div>
</header>

<main>
    <!-- CRIPTOS ATUALIZADAS -->
    <div>
        <h2 class="section-title">Cripto Mercado (Real-Time)</h2>
        <div class="market-grid">
            <div class="price-box"><label>BITCOIN (BTC)</label><span>$80,340.50</span></div>
            <div class="price-box"><label>ETHEREUM (ETH)</label><span>$4,120.15</span></div>
            <div class="price-box"><label>SOLANA (SOL)</label><span>$174.45</span></div>
            <div class="price-box"><label>USDC</label><span>$1.00</span></div>
        </div>
    </div>

    <!-- B3 RADAR -->
    <div style="flex-grow: 1; min-height: 300px;">
        <h2 class="section-title">B3 Radar - Ações</h2>
        <div class="card" style="height: 100%;">
            <iframe src="https://br.tradingview.com/widgetembed/?symbol=BMFBOVESPA%3AIBOV&interval=D&theme=dark" width="100%" height="100%" frameborder="0"></iframe>
        </div>
    </div>
</main>

<footer>
    Nels1Radar by MaquinadoDigital - 2026 - [&lt;o&gt;]
</footer>

</body>
</html>
