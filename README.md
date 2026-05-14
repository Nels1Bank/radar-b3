
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surface: #0a0a0a;
            --primary: #00e5ff;
            --crypto: #f59e0b;
            --text: #ffffff;
            --text-dim: #999;
            --border: #1a1a1a;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            font-family: 'Inter', sans-serif; 
            background: var(--bg); 
            color: var(--text); 
            height: 100vh; 
            display: flex; 
            flex-direction: column;
            overflow-x: hidden;
        }

        /* Titulo */
        header { flex-shrink: 0; padding: 15px 0; border-bottom: 1px solid var(--border); }
        h1 { font-family: 'Orbitron', sans-serif; font-size: 1.2rem; text-align: center; color: var(--primary); letter-spacing: 3px; }

        /* Letreiro Digital - Dados Oficiais Maio/2026 */
        .ticker { background: #050505; padding: 10px 0; overflow: hidden; white-space: nowrap; border-bottom: 1px solid var(--border); }
        .track { display: inline-block; animation: scroll 25s linear infinite; font-size: 0.85rem; color: var(--primary); font-weight: bold; }
        .asset { padding: 0 25px; border-right: 1px solid var(--border); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        /* Grid de Criptos */
        .market-section { padding: 15px; flex-shrink: 0; }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .card { background: var(--surface); border: 1px solid var(--border); padding: 15px; border-radius: 12px; }
        .card label { display: block; font-size: 0.65rem; color: var(--text-dim); margin-bottom: 5px; text-transform: uppercase; letter-spacing: 1px; }
        .card span { font-size: 1.1rem; font-weight: 700; color: #fff; }
        .btc-card { border-left: 4px solid var(--crypto); }

        /* B3 Section */
        .b3-section { flex-grow: 1; padding: 0 15px 15px 15px; display: flex; flex-direction: column; }
        .b3-frame { flex-grow: 1; border-radius: 12px; border: 1px solid var(--border); overflow: hidden; }

        /* Footer */
        footer { 
            flex-shrink: 0; 
            padding: 15px; 
            text-align: center; 
            font-size: 0.75rem; 
            color: var(--text-dim); 
            border-top: 1px solid var(--border);
            background: #000;
        }
    </style>
</head>
<body>

<header>
    <h1>Nels1Radar</h1>
</header>

<div class="ticker">
    <div class="track">
        <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
        <span class="asset">METAPLANET: 40,177 BTC ▲</span>
        <span class="asset">21 CAPITAL: 43,514 BTC ▲</span>
        <span class="asset">IBOVESPA: 128.450 pts ▲</span>
        <span class="asset">BBAS3: R$ 26,45 ▼</span>
        <!-- Loop para animação fluida -->
        <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
        <span class="asset">METAPLANET: 40,177 BTC ▲</span>
        <span class="asset">IBOVESPA: 128.450 pts ▲</span>
    </div>
</div>

<main class="market-section">
    <div class="grid">
        <div class="card btc-card"><label>Bitcoin (BTC)</label><span>$80,340.50</span></div>
        <div class="card"><label>Ethereum (ETH)</label><span>$4,120.15</span></div>
        <div class="card"><label>Solana (SOL)</label><span>$174.45</span></div>
        <div class="card"><label>USDC</label><span>$1.00</span></div>
    </div>
</main>

<section class="b3-section">
    <div style="margin-bottom: 8px; font-size: 0.7rem; color: var(--text-dim); font-family: 'Orbitron';">B3 Market Overview</div>
    <div class="b3-frame">
        <iframe src="https://s.tradingview.com/embed-widget/screener/?locale=br#%7B%22width%22%3A%22100%25%22%2C%22height%22%3A%22100%25%22%2C%22defaultColumn%22%3A%22overview%22%2C%22defaultScreen%22%3A%22most_capitalized%22%2C%22market%22%3A%22brazil%22%2C%22showToolbar%22%3Afalse%2C%22colorTheme%22%3A%22dark%22%2C%22isTransparent%22%3Afalse%7D" width="100%" height="100%" frameborder="0"></iframe>
    </div>
</section>

<footer>
    Nels1Radar by MaquinadoDigital - 2026 - [&lt;o&gt;]
</footer>

</body>
</html>
