---
layout: single
title: ""
author_profile: false
permalink: /
classes: wide
---

<div class="landing-canvas">
  <div class="center-stroke" aria-hidden="true"></div>

  <!-- LEFT PANE -->
  <section class="pane left" aria-label="Work: ML, AI, Blockchain">
    <h2 class="landing-title">Lost in the Forest. Random or Isolation</h2>

    <div class="pane-content">
      <!-- Add left-side content here as you grow (posts, links, etc.) -->
      <div class="tag-list">
        <a href="https://github.com/sivacluster?tab=repositories&q=ml" target="_blank" rel="noopener">ml</a>
        <a href="https://github.com/sivacluster?tab=repositories&q=ai" target="_blank" rel="noopener">ai</a>
        <a href="https://github.com/sivacluster?tab=repositories&q=blockchain" target="_blank" rel="noopener">blockchain</a>
        <a href="/year-archive/">all posts</a>
      </div>
    </div>
  </section>

  <!-- RIGHT PANE -->
  <section class="pane right" aria-label="Markets: Stocks and Crypto">
    <h2 class="landing-title">Being an Analyst</h2>

    <div class="pane-content">
      <!-- Bitcoin Live -->
      <h3 class="widget-title">Bitcoin Live</h3>
      <div class="widget-box">
        <!-- TradingView mini chart -->
        <div class="tradingview-widget-container" style="height: 280px;">
          <div class="tradingview-widget-container__widget"></div>
          <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js" async>
          {
            "symbol": "BITSTAMP:BTCUSD",
            "locale": "en",
            "width": "100%",
            "height": "280",
            "dateRange": "12M",
            "colorTheme": "light",
            "trendLineColor": "#268bd2",
            "underLineColor": "rgba(38,139,210,0.15)",
            "isTransparent": true
          }
          </script>
        </div>
      </div>

      <!-- Fear & Greed index Live -->
      <h3 class="widget-title">People Greed index live</h3>
      <div class="widget-box">
        <!-- Simple live image (cache-busted) -->
        <img
          src="https://alternative.me/crypto/fear-and-greed-index.png?t={{ site.time | date: '%s' }}"
          alt="Crypto Fear & Greed Index"
          style="max-width:100%; height:auto;"
        />
      </div>
    </div>
  </section>

  <!-- BOTTOM-LEFT FOOTER -->
  <footer class="landing-footer">
    <div>
      © {{ site.time | date: "%Y" }} Siva Cluster
      <span class="sep">·</span>
      <a href="https://www.linkedin.com/sivav/" target="_blank" rel="noopener">LinkedIn</a>
      <span class="sep">·</span>
      <a href="https://www.reddit.com/user/chasingMillion" target="_blank" rel="noopener">Reddit</a>
      <span class="sep">·</span>
      <a href="https://discord.com/users/unbrokenideas" target="_blank" rel="noopener">Discord (@unbrokenideas)</a>
    </div>
  </footer>
</div>