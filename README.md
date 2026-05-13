
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar | Crypto Focus</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #020617;
            --primary: #f59e0b; /* Laranja Bitcoin */
            --up: #10b981;
            --down: #ef4444;
            --glass: rgba(15, 23, 42, 0.9);
        }

        body { 
            font-family: 'JetBrains Mono', monospace; 
            background: var(--bg); color: #f8fafc; 
            margin: 0; padding: 10px; display: flex; justify-content: center;
        }

        .terminal { 
            width: 100%; max-width: 480px; background: var(--glass);
            border: 1px solid #1e293b; border-radius: 16px; padding: 15px;
            box-shadow: 0 0 40px rgba(245, 158, 11, 0.1);
        }

        h1 { 
            font-family: 'Orbitron', sans-serif; color: var(--primary); 
            font-size: 1.1rem; text-align: center; letter-spacing: 2px;
            text-shadow: 0 0 10px rgba(245, 158, 11, 0.5);
        }

        .alert-box {
            background: rgba(245, 158, 11, 0.15); border: 1px solid var(--primary);
            border-radius: 8px; padding: 10px; margin: 15px 0;
            font-size: 0.7rem; color: var(--primary); text-align: center;
        }

        .ticker-stream {
            background: #000; border: 1px solid #334155;
            border-radius: 8px; padding: 12px 0; overflow: hidden;
        }

        .track { display: inline-block; white-space: nowrap; animation: scroll 20s linear infinite; }
        .asset { display: inline-block; padding: 0 25px; border-right: 1px solid #1e293b; }
        .asset b { font-size: 0.9rem; }
        .up { color: var(--up); } .down { color: var(--down); }

        @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

        footer { margin-top: 25px; text-align: center; border-top: 1px solid #1e293b; padding-top: 10px; }
        .legal { color: var(--up); font-size: 8px; text-transform: uppercase; }
    </style>
</head>
<body>

<div class="terminal">
    <h1>NELS1-RADAR: CRYPTO EDITION</h1>
    
    <div class="alert-box">
        ⚠️ [SINAL DETECTADO]: RECUPERAÇÃO DE 5 BTC VIA IA CONFIRMADA NO X.
    </div>

    <div class="ticker-stream">
        <div class="track">
            <div class="asset"><b>BTC</b><span class="up"> ▲</span></div>
            <div class="asset"><b>SOL</b><span class="up"> ▲</span></div>
            <div class="asset"><b>ETH</b><span class="up"> ▲</span></div>
            <div class="asset"><b>BBAS3</b><span class="down"> ▼</span></div>
            <div class="asset"><b>SBSP3</b><span class="up"> ▲</span></div>
            <!-- Loop -->
            <div class="asset"><b>BTC</b><span class="up"> ▲</span></div>
            <div class="asset"><b>SOL</b><span class="up"> ▲</span></div>
            <div class="asset"><b>ETH</b><span class="up"> ▲</span></div>
            <div class="asset"><b>BBAS3</b><span class="down"> ▼</span></div>
            <div class="asset"><b>SBSP3</b><span class="up"> ▲</span></div>
        </div>
    </div>

    <div style="margin-top:20px; height: 300px; border-radius: 8px; overflow:hidden;">
        <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=5&pref_coin_id=1505" width="100%" height="300px" frameborder="0" style="border:0;"></iframe>
    </div>

    <footer>
        <p class="legal">Atenção: Monitoramento técnico. Informações não constituem indicação de compra ou venda.</p>
    </footer>
</div>

</body>
</html>
