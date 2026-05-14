
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nels1Radar | Terminal</title>
    <style>
        /* Reset e Base */
        * { box-sizing: border-box; margin: 0; padding: 0; }
        :root { 
            --bg: #050505; 
            --card-bg: #0f0f0f; 
            --accent: #00e5ff; 
            --border: #1a1a1a; 
            --text: #e0e0e0;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.5;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Header Estilizado */
        header {
            padding: 20px;
            text-align: center;
            border-bottom: 1px solid var(--border);
            background: linear-gradient(to bottom, #0a0a0a, var(--bg));
        }

        h1 {
            font-size: 1.4rem;
            letter-spacing: 4px;
            color: var(--accent);
            text-transform: uppercase;
        }

        /* Grid de Ativos - Ajuste Supremo de Layout */
        .dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
            padding: 15px;
            width: 100%;
            max-width: 1000px;
            align-self: center;
        }

        .ticker-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border);
            padding: 25px 10px;
            border-radius: 6px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }

        /* Ticker Isolado - Regra: Nada ao lado */
        .ticker-name {
            font-family: 'Courier New', Courier, monospace;
            font-weight: 700;
            font-size: 1.1rem;
            color: #fff;
            display: block;
            width: 100%;
        }

        /* Footer */
        footer {
            margin-top: auto;
            padding: 15px;
            text-align: center;
            font-size: 0.7rem;
            color: #444;
            border-top: 1px solid var(--border);
        }

        /* Ajuste para telas pequenas */
        @media (max-width: 480px) {
            .dashboard {
                grid-template-columns: 1fr 1fr; /* Força duas colunas no celular */
                padding: 10px;
            }
            h1 { font-size: 1.1rem; }
        }
    </style>
</head>
<body>

    <header>
        <h1>Nels1Bank Radar</h1>
    </header>

    <main class="dashboard">
        <div class="ticker-card"><span class="ticker-name">BBAS3</span></div>
        <div class="ticker-card"><span class="ticker-name">ITUB4</span></div>
        <div class="ticker-card"><span class="ticker-name">PETR4</span></div>
        <div class="ticker-card"><span class="ticker-name">AURE3</span></div>
        <div class="ticker-card"><span class="ticker-name">BPAC3</span></div>
        <div class="ticker-card"><span class="ticker-name">CSNA3</span></div>
    </main>

    <footer>
        SISTEMA DE MONITORAMENTO DE ATIVOS V26.0
    </footer>

</body>
</html>
