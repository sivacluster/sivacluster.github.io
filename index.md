      <!-- Bitcoin Live -->
      <h3 class="widget-title">Bitcoin Live</h3>
      <div class="live-row">
        <span class="live-label">BTC/USD</span>
        <span id="btc-price" class="live-value">$—</span>
        <span id="btc-change" class="live-delta"></span>
      </div>
       <div class="widget-box">
         <!-- TradingView mini chart -->
         <div class="tradingview-widget-container" style="height: 280px;">
    <!-- Fear & Greed index Live -->
    <h3 class="widget-title">People Greed index live</h3>
    <div class="live-row">
      <span class="live-label">Fear &amp; Greed (US)</span>
      <span id="fng-value" class="live-value">—</span>
    </div>
    <div class="widget-box">
      <!-- Simple live image (cache-busted) -->
      <img
        src="https://alternative.me/crypto/fear-and-greed-index.png?t={{ site.time | date: '%s' }}"
        alt="Crypto Fear & Greed Index"
        style="max-width:100%; height:auto;"
      />
  </footer>
</div>

<script>
  async function fetchBTC() {
    try {
      const r = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd&include_24hr_change=true');
      const j = await r.json();
      const p = j?.bitcoin?.usd;
      const ch = j?.bitcoin?.usd_24h_change;
      const priceEl = document.getElementById('btc-price');
      const changeEl = document.getElementById('btc-change');
      if (priceEl && typeof p === 'number') {
        priceEl.textContent = p.toLocaleString('en-US', { style: 'currency', currency: 'USD' });
      }
      if (changeEl && typeof ch === 'number') {
        changeEl.textContent = (ch >= 0 ? '+' : '') + ch.toFixed(2) + '%';
        changeEl.style.color = ch >= 0 ? '#2aa198' : '#cb4b16';
      }
    } catch (e) { console.error('BTC fetch failed', e); }
  }

  async function fetchFNG() {
    try {
      const r = await fetch('https://api.alternative.me/fng/?limit=1');
      const j = await r.json();
      const entry = (j && j.data && j.data[0]) || null;
      const v = entry ? entry.value : null; // 0-100
      const cls = entry ? entry.value_classification : '';
      const el = document.getElementById('fng-value');
      if (el && v !== null) el.textContent = `${v} / 100 (${cls})`;
    } catch (e) { console.error('FNG fetch failed', e); }
  }

  function refresh() { fetchBTC(); fetchFNG(); }
  refresh();
  setInterval(refresh, 60000);
</script>