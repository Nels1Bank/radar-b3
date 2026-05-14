
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000; --surf: #0a0a0a; --prim: #00e5ff; --cry: #f59e0b;
            --txt: #fff; --dim: #888; --brd: #1a1a1a;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { 
            font-family: 'Inter', sans-serif; background: var(--bg); color: var(--txt); 
            height: 100vh; display: flex; flex-direction: column; overflow: hidden;
        }
        header { padding: 15px 0; border-bottom: 1px solid var(--brd); text-align: center; flex-shrink: 0; }
        h1 { font-family: 'Orbitron'; font-size: 1.2rem; color: var(--prim); letter-spacing: 3px; }
        
        /* Letreiro Digital - Dados Oficiais Maio 2026 */
        .ticker { background: #050505; padding: 10px 0; overflow: hidden; white-space: nowrap; border-bottom: 1px solid var(--brd); }
        .track { display: inline-block; animation: scroll 25s linear infinite; font-size: 0.85rem; color: var(--prim); font-weight: 700; }
        .asset { padding: 0 25px; border-right: 1px solid var(--brd); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        main { flex-grow: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; gap: 15px; }
        .section-label { font-family: 'Orbitron'; font-size: 0.7rem; color: var(--dim); letter-spacing: 1px; margin-bottom: 5px; text-transform: uppercase; }

        /* Grid de Criptos */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .card { background: var(--surf); border: 1px solid var(--brd); padding: 15px; border-radius: 12px; }
        .card label { display: block; font-size: 0.65rem; color: var(--dim); margin-bottom: 6px; }
        .card span { font-size: 1.1rem; font-weight: 700; color: #fff; }
        .btc-highlight { border-left: 4px solid var(--cry); }

        /* Container Gráfico B3 */
        .b3-box { flex-grow: 1; min-height: 320px; border: 1px solid var(--brd); border-radius: 12px; overflow: hidden; position: relative; }

        footer { 
            padding: 15px; text-align: center; font-size: 0.75rem; color: var(--dim); 
            border-top: 1px solid var(--brd); background: #000; flex-shrink: 0;
        }
    </style>
</head>
<body>

<header><h1>Nels1Radar</h1></header>

<div class="ticker">
    <div class="track">
        <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
        <span class="asset">METAPLANET: 40,177 BTC ▲</span>
        <span class="asset">BPAC3: R$ 25,12 (TREND A) ▼</span>
        <span class="asset">IBOVESPA: 128.450 pts ▲</span>
        <span class="asset">21 CAPITAL: 43,514 BTC ▲</span>
        <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
        <span class="asset">METAPLANET: 40,177 BTC ▲</span>
    </div>
</div>

<main>
    <div>
        <div class="section-label">Criptos & Stablecoins</div>
        <div class="grid">
            <div class="card btc-highlight"><label>BITCOIN (BTC)</label><span>$80,340.50</span></div>
            <div class="card"><label>ETHEREUM (ETH)</label><span>$4,120.15</span></div>
            <div class="card"><label>SOLANA (SOL)</label><span>$174.45</span></div>
            <div class="card"><label>USDC (FIAT)</label><span>$1.0000</span></div>
        </div>
    </div>

    <div style="flex-grow: 1; display: flex; flex-direction: column;">
        <div class="section-label">B3 Radar - Performance</div>
        <div class="b3-box">
            <iframe src="https://s.tradingview.com/widgetembed/?symbol=BMFBOVESPA%3ABPAC3&interval=D&hidesidetoolbar=1&theme=dark&style=1&timezone=America%2FSao_Paulo&locale=br" width="100%" height="100%" frameborder="0"></iframe>
        </div>
    </div>
</main>

<footer>
    Nels1Radar by MaquinadoDigital - 2026 - [&lt;o&gt;]
</footer>

</body>
</html>
