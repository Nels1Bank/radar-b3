<!-- ... (estilos anteriores mantidos) ... -->
<style>
    /* Novo estilo para a grade de institucionais */
    .inst-grid {
        display: grid; grid-template-columns: 1fr 1fr; gap: 10px;
        padding: 10px; background: #000; border: 1px solid var(--crypto-accent);
        border-top: none; border-radius: 0 0 12px 12px;
    }
    .inst-card {
        padding: 8px; border-left: 2px solid var(--crypto-accent);
        background: rgba(245, 158, 11, 0.05);
    }
    .inst-card h3 { font-size: 0.6rem; color: #64748b; margin: 0; text-transform: uppercase; }
    .inst-card p { font-size: 0.75rem; color: #fff; margin: 4px 0 0 0; font-weight: bold; }
    .inst-card span { font-size: 0.6rem; color: var(--up); }
</style>

<div class="terminal">
    <!-- ... (Letreiro e Widget B3 anteriores) ... -->

    <div class="section-tag" style="color: var(--crypto-accent);">Crypto Market & Institutional</div>
    <div class="widget-box crypto-border" style="height: 350px; border-bottom: none; border-radius: 12px 12px 0 0;">
        <iframe src="https://widget.coinlib.io/widget?type=full_v2&theme=dark&cnt=6&pref_coin_id=1505" width="100%" height="350px" frameborder="0" style="border:0;"></iframe>
    </div>
    
    <!-- Painel de Detentores Institucionais -->
    <div class="inst-grid">
        <div class="inst-card">
            <h3>🇺🇸 EUA (MicroStrategy)</h3>
            <p>214,400+ BTC</p>
            <span>Saylor's Bet</span>
        </div>
        <div class="inst-card">
            <h3>🇯🇵 Japão (Metaplanet)</h3>
            <p>117+ BTC</p>
            <span>"The Asia MSTR"</span>
        </div>
        <div class="inst-card">
            <h3>🇧🇷 Brasil (HASH11)</h3>
            <p>ETF Leader</p>
            <span>Hasdex Index</span>
        </div>
        <div class="inst-card">
            <h3>🇨🇳 China (Harvest/BOS)</h3>
            <p>HK ETFs</p>
            <span>Institutional Proxy</span>
        </div>
    </div>

    <footer>
        <p class="legal">Atenção: Monitoramento técnico. Informações não constituem indicação de compra ou venda.</p>
    </footer>
</div>
