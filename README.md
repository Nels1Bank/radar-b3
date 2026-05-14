
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>Nels1Radar</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { background: #000; color: #fff; font-family: sans-serif; display: flex; flex-direction: column; align-items: center; padding: 20px; }
        
        .header { text-align: center; margin-bottom: 30px; width: 100%; border-bottom: 1px solid #1a1a1a; padding-bottom: 15px; }
        .header h1 { font-size: 1.2rem; color: #00e5ff; letter-spacing: 2px; }

        /* Grid Blindado */
        .grid { 
            display: grid; 
            grid-template-columns: repeat(2, 1fr); 
            gap: 15px; 
            width: 100%; 
            max-width: 500px; 
        }

        .card { 
            background: #0a0a0a; 
            border: 1px solid #222; 
            border-radius: 8px; 
            padding: 20px; 
            text-align: center; 
        }

        /* Regra: Nada ao lado */
        .ticker { 
            display: block; 
            font-weight: bold; 
            font-size: 1.1rem; 
            color: #fff;
            margin-bottom: 5px;
        }

        .price { color: #00ff88; font-size: 0.9rem; display: block; }
        
        footer { margin-top: 40px; font-size: 0.7rem; color: #444; }
    </style>
</head>
<body>

    <div class="header"><h1>Nels1Bank Radar</h1></div>

    <div class="grid">
        <div class="card"><span class="ticker">BBAS3</span><span class="price">R$ 27,45</span></div>
        <div class="card"><span class="ticker">ITUB4</span><span class="price">R$ 32,10</span></div>
        <div class="card"><span class="ticker">PETR4</span><span class="price">R$ 41,20</span></div>
        <div class="card"><span class="ticker">AURE3</span><span class="price">R$ 11,85</span></div>
        <div class="card"><span class="ticker">BPAC3</span><span class="price">R$ 14,90</span></div>
        <div class="card"><span class="ticker">CSNA3</span><span class="price">R$ 6,55</span></div>
        <div class="card" style="grid-column: span 2; border-color: #f59e0b;">
            <span class="ticker">SOLANA (SOL)</span>
            <span class="price" style="color: #f59e0b;">R$ 457,83</span>
        </div>
    </div>

    <footer>Sincronizado com fechamento de 13/05/2026</footer>

</body>
</html>
