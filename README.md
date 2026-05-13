
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Nels1Radar v12.0</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #000; --surf: #0d1117; --prim: #00e5ff; --crypt: #f59e0b;
            --up: #10b981; --bord: #30363d;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body, html { 
            height: 100%; width: 100%; overflow: hidden; 
            background: var(--bg); color: #c9d1d9; font-family: 'JetBrains Mono', monospace;
            display: flex; flex-direction: column;
        }
        header { flex-shrink: 0; border-bottom: 1px solid var(--bord); padding: 5px 0; text-align: center; }
        h1 { font-family: 'Orbitron'; font-size: 0.7rem; color: var(--prim); letter-spacing: 1px; }
        .ticker { overflow: hidden; white-space: nowrap; font-size: 0.6rem; padding: 3px 0; background: #000; }
        .track { display: inline-block; animation: scroll 20s linear infinite; }
        .asset { padding: 0 10px; border-right: 1px solid var(--bord); }
        @keyframes scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }
        
        main { flex-grow: 1; position: relative; }
        .tab { display: none; height: 100%; width: 100%; padding: 5px; flex-direction: column; gap: 5px; }
        .tab.active { display: flex; }
        .card { flex: 1; background: var(--surf); border: 1px solid var(--bord); border-radius: 5px; overflow: hidden; }
        
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4px; flex-shrink: 0; }
        .box { background: #161b22; border: 1px solid var(--bord); padding: 8px; border-radius: 5px; border-left: 3px solid var(--crypt); }
        .box label { font-size: 0.45rem; color: #8b949e; display: block; }
        .box b { font-size: 0.7rem; color: #fff; display: block; margin: 2px 0; }
        .box span { font-size: 0.45rem; color: var(--up); font-weight: bold; }

        nav { flex-shrink: 0; height: 55px; display: flex; background: #010409; border-top: 1px solid var(--bord); padding-bottom: env(safe-area-inset-bottom); }
        .btn { flex: 1; border: none; background: none; color: #484f58; font-family: 'Orbitron'; font-size: 0.6rem; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 3px; }
        .btn.active { color: var(--prim); }
        .btn.cry.active { color: var(--crypt); }
        .ind { width: 12px; height: 2px; background: currentColor; }
    </style>
</head>
<body>
    <header>
        <h1>NELS1-RADAR v12.0</h1>
        <div class="ticker">
            <div class="track">
                <span class="asset">BTC $80,340 ▲</span><span class="asset">BBAS3 R$ 26.45 ▼</span>
                <span class="asset">SBSP3 R$ 82.10 ▲</span><span class="asset">SOL $174.50 ▲</span>
                <span class="asset">BTC $80,340 ▲</span><span class="asset">BBAS3 R$ 26.45 ▼</span>
            </div>
        </div>
    </header>
    <main>
        <div id="b3" class="tab active">
            <div class="card">
                <iframe src="https://br.tradingview.com/widgetembed/?symbol=BMFBOVESPA%3AIBOV&interval=D&theme=dark" width="100%" height="100%" frameborder="0"></iframe>
            </div>
        </div>
        <div id="cry" class="tab">
            <div class="card" style="flex: 0.65;">
                <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=4&pref_coin_id=1505" width="100%" height="100%" frameborder="0"></iframe>
            </div>
            <div class="grid">
                <div class="box"><label>STRATEGY INC</label><b>818,869 BTC</b><span>TREASURY #1</span></div>
                <div class="box"><label>METAPLANET</label><b>40,177 BTC</b><span>ASIA #1</span></div>
                <div class="box" style="border-left-color:var(--prim)"><label>21 CAPITAL</label><b>43,514 BTC</b><span>ETF FLOW</span></div>
                <div class="box" style="border-left-color:#fff"><label>MARA HOLDINGS</label><b>35,303 BTC</b><span>MINING</span></div>
            </div>
        </div>
    </main>
    <nav>
        <button class="btn active" onclick="sh('b3', event)"><div class="ind"></div>B3</button>
        <button class="btn cry" onclick="sh('cry', event)"><div class="ind"></div>BTC</button>
    </nav>
    <script>
        function sh(id, e) {
            document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
            document.querySelectorAll('.btn').forEach(b => b.classList.remove('active'));
            document.getElementById(id).classList.add('active');
            e.currentTarget.classList.add('active');
            if (window.navigator.vibrate) window.navigator.vibrate(8);
        }
    </script>
</body>
</html>
