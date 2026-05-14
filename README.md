
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000000;
            --surf: #0a0a0a;
            --prim: #00e5ff;
            --up: #00ff88;
            --down: #ff3d3d;
            --brd: #1a1a1a;
            --txt: #ffffff;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            font-family: 'Inter', sans-serif; 
            background: var(--bg); 
            color: var(--txt); 
            height: 100vh; 
            display: flex; 
            flex-direction: column;
            overflow: hidden;
        }

        /* Título Principal */
        header { flex-shrink: 0; padding: 18px 0; border-bottom: 1px solid var(--brd); text-align: center; background: #000; }
        h1 { font-family: 'Orbitron', sans-serif; font-size: 1.4rem; color: var(--prim); letter-spacing: 4px; }

        /* Letreiro Digital (Ticker) */
        .ticker { background: #050505; padding: 12px 0; overflow: hidden; white-space: nowrap; border-bottom: 1px solid var(--brd); flex-shrink: 0; }
        .track { display: inline-block; animation: scroll 30s linear infinite; font-size: 0.9rem; color: var(--prim); font-weight: 700; }
        .asset { padding: 0 30px; border-right: 1px solid var(--brd); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }

        main { flex: 1; padding: 15px; display: flex; flex-direction: column; gap: 20px; overflow-y: auto; }

        /* Seção Criptos - Estilo Bubbles/Cards */
        .crypto-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; }
        .crypto-card { 
            background: var(--surf); border: 1px solid var(--brd); padding: 20px; border-radius: 18px; 
            text-align: center; transition: transform 0.2s;
        }
        .crypto-card label { display: block; font-family: 'Orbitron'; font-size: 0.7rem; color: #888; margin-bottom: 8px; }
        .crypto-card .val { font-size: 1.2rem; font-weight: 700; display: block; margin-bottom: 4px; }
        .crypto-card .pct { font-size: 0.75rem; font-weight: bold; }
        .up { color: var(--up); }
        .neutral { color: #aaa; }

        /* Seção B3 */
        .b3-container { flex: 1; min-height: 350px; border: 1px solid var(--brd); border-radius: 15px; overflow: hidden; }

        /* Rodapé Requisitado */
        footer { 
            flex-shrink: 0; padding: 20px; text-align: center; 
            font-size: 0.8rem; color: #555; border-top: 1px solid var(--brd); 
            background: #000; letter-spacing: 1px;
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
        <span class="asset">BPAC3: R$ 25,10 (SUPPORT ZONE) ▼</span>
        <span class="asset">IBOVESPA: 128.450 pts ▲</span>
        <span class="asset">21 CAPITAL: 43,514 BTC ▲</span>
        <span class="asset">STRATEGY INC: 818,869 BTC ▲</span>
    </div>
</div>

<main>
    <div class="crypto-grid">
        <div class="crypto-card">
            <label>BITCOIN</label>
            <span class="val">$80,340.50</span>
            <span class="pct up">+2.45%</span>
        </div>
        <div class="crypto-card">
            <label>ETHEREUM</label>
            <span class="val">$4,120.15</span>
            <span class="pct up">+1.12%</span>
        </div>
        <div class="crypto-card">
            <label>SOLANA</label>
            <span class="val">$174.45</span>
            <span class="pct up">+4.80%</span>
        </div>
        <div class="crypto-card">
            <label>USDC</label>
            <span class="val">$1.00</span>
            <span class="pct neutral">0.00%</span>
        </div>
    </div>

    <div class="b3-container">
        <iframe src="https://s.tradingview.com/widgetembed/?symbol=BMFBOVESPA%3ABPAC3&interval=D&hidesidetoolbar=1&theme=dark&style=1&timezone=America%2FSao_Paulo&locale=br" width="100%" height="100%" frameborder="0"></iframe>
    </div>
</main>

<footer>
    Nels1Radar by MaquinadoDigital - 2026 - [&lt;o&gt;]
</footer>

<script>
    // Impede o cache agressivo do navegador
    if (window.location.href.indexOf('?') === -1) {
        window.location.href = window.location.href + '?v=19.0';
    }
</script>

</body>
</html>
