<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Xinfeng Gu — Quant · Crypto-Quant · ZK</title>
  <meta name="description" content="Quant / Crypto-Quant / ZK & ML — reproducible research, tiny benchmarks, one-page briefs." />
  <meta name="theme-color" content="#0f172a" />
  <!-- 简洁 favicon（内联 SVG） -->
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 256 256'%3E%3Ccircle cx='128' cy='128' r='120' fill='%230f172a'/%3E%3Ctext x='50%' y='58%' dominant-baseline='middle' text-anchor='middle' font-family='Arial, Helvetica, sans-serif' font-size='120' fill='%23fff'%3EG%3C/text%3E%3C/svg%3E"/>
  <!-- Open Graph（先指向主页，等你上传 og-card.png 再改） -->
  <meta property="og:title" content="Xinfeng Gu — Quant · Crypto-Quant · ZK" />
  <meta property="og:description" content="Reproducible research, tiny benchmarks, one-page briefs." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://xinfeng-gu.github.io/" />
  <!-- <meta property="og:image" content="https://raw.githubusercontent.com/xinfeng-gu/xinfeng-gu.github.io/main/og-card.png" /> -->
  <meta name="twitter:card" content="summary_large_image" />
  <style>
    :root{
      --bg:#0b1020; --panel:#111827; --muted:#a7b0c0; --text:#e5e7eb; --brand:#22d3ee; --brand2:#a78bfa;
      --border: rgba(167,176,192,.26);
    }
    @media (prefers-color-scheme: light){
      :root{ --bg:#f8fafc; --panel:#ffffff; --muted:#475569; --text:#0f172a; --border: rgba(71,85,105,.26); }
    }
    *,*::before,*::after{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background:
        radial-gradient(1200px 600px at 80% -10%, rgba(34,211,238,.15), transparent 45%),
        radial-gradient(900px 400px at -10% 20%, rgba(167,139,250,.15), transparent 50%),
        var(--bg);
      color:var(--text); line-height:1.6; -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    }
    a{color:var(--brand); text-decoration:none}
    a:hover{text-decoration:underline}
    .container{max-width:1100px; margin:0 auto; padding:24px}
    header{
      position:sticky; top:0; backdrop-filter:saturate(180%) blur(12px);
      background: rgba(11,16,32,.75);
      border-bottom:1px solid var(--border); z-index:50;
    }
    .nav{display:flex; align-items:center; justify-content:space-between; gap:16px}
    .nav a.btn{padding:8px 14px; border:1px solid var(--border); border-radius:12px}
    .brand{display:flex; align-items:center; gap:12px; font-weight:700; letter-spacing:.2px}
    .dot{width:10px; height:10px; border-radius:50%; background:linear-gradient(135deg,var(--brand),var(--brand2)); box-shadow:0 0 18px rgba(34,211,238,.6)}
    .hero{display:grid; grid-template-columns:1.2fr .8fr; gap:24px; align-items:center; padding:48px 0 20px}
    .hero h1{font-size:clamp(28px,4vw,46px); line-height:1.15; margin:8px 0 10px}
    .tagline{font-size:clamp(14px,2.2vw,18px); color:var(--muted)}
    .cta{display:flex; gap:12px; flex-wrap:wrap; margin-top:20px}
    .btn{display:inline-flex; align-items:center; gap:8px; padding:10px 16px; border-radius:12px; border:1px solid var(--border); color:var(--text)}
    .btn.primary{background:linear-gradient(135deg,var(--brand),var(--brand2)); color:#0b1020; border:none; box-shadow:0 10px 24px -12px rgba(34,211,238,.4)}
    .btn:hover{transform:translateY(-1px); transition:.15s ease}
    .section{padding:34px 0}
    .section h2{font-size:clamp(20px,3vw,28px); margin:0 0 14px}
    .grid{display:grid; grid-template-columns:repeat(12,1fr); gap:16px}
    .card{grid-column:span 12; padding:18px; background:rgba(17,24,39,.88); border:1px solid var(--border); border-radius:16px; box-shadow:0 10px 30px -20px rgba(0,0,0,.35)}
    @media (prefers-color-scheme: light){ .card{background:#fff} }
    @media (min-width:860px){ .card.md6{grid-column:span 6} .card.md4{grid-column:span 4} }
    .card h3{margin:6px 0 8px; font-size:18px}
    .muted{color:var(--muted); font-size:14px}
    .badges{display:flex; flex-wrap:wrap; gap:8px; margin-top:10px}
    .badge{font-size:12px; padding:6px 10px; border-radius:999px; background:rgba(17,24,39,.6); border:1px solid var(--border)}
    @media (prefers-color-scheme: light){ .badge{background:#f1f5f9} }
    .footer{padding:36px 0 48px; color:var(--muted); font-size:14px; display:flex; justify-content:space-between; gap:16px; flex-wrap:wrap}
    .links{display:flex; gap:14px; flex-wrap:wrap}
    .kbd{font-family:ui-monospace, SFMono-Regular, Menlo, Consolas, monospace; font-size:12px; background:rgba(17,24,39,.7); padding:2px 6px; border-radius:6px; border:1px solid var(--border)}
    .visually-hidden{position:absolute; clip:rect(1px,1px,1px,1px); padding:0; border:0; height:1px; width:1px; overflow:hidden}
  </style>
</head>
<body>
  <header>
    <div class="container nav" role="navigation" aria-label="Primary">
      <div class="brand"><span class="dot" aria-hidden="true"></span> Xinfeng Gu</div>
      <nav class="links">
        <a class="btn" href="#projects">Projects</a>
        <a class="btn" href="#about">About</a>
        <a class="btn" href="#contact">Contact</a>
        <button class="btn" id="themeToggle" aria-label="Toggle theme">🌗 Theme</button>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero" id="home">
      <div>
        <div class="kbd">Quant · Crypto-Quant · ZK · LLM</div>
        <h1>Reproducible research & small, solid benchmarks.</h1>
        <p class="tagline">I turn unstructured signals (text, on-chain, microstructure) into tradable research with evidence: <em>metrics.json</em>, charts, and one-page briefs.</p>
        <div class="cta">
          <a class="btn primary" href="#projects">View projects</a>
          <a class="btn" href="mailto:martineuclid@gmail.com">Email me</a>
          <!-- 若没有 docs/CV.pdf 先注释掉下面这一行 -->
          <!-- <a class="btn" href="./docs/CV.pdf">Download CV</a> -->
        </div>
      </div>
      <div class="card">
        <h3>Now / 最近在做</h3>
        <ul class="muted" style="margin:8px 0 0 16px;">
          <li>Finance/Crypto <strong>Text → Signal → Backtest</strong> (IC/Sharpe)</li>
          <li>Uniswap v3 LP <strong>band</strong> rebalancing (fees vs IL)</li>
          <li>ZK: Groth16 vs PLONK on the <strong>same circuit</strong></li>
        </ul>
        <div class="badges">
          <span class="badge">Python</span><span class="badge">C++</span><span class="badge">Rust</span><span class="badge">Solidity</span><span class="badge">SQL</span>
        </div>
      </div>
    </section>

    <section class="section" id="projects">
      <h2>Featured Projects</h2>
      <div class="grid">
        <article class="card md6">
          <h3>text_signal_mvp — Text → Signal → IC → Backtest</h3>
          <p class="muted">Turn finance/crypto text into tradable signals; evaluate Rank IC & after-cost Sharpe; one-command reproducible.</p>
          <div class="badges"><span class="badge">IC</span><span class="badge">Sharpe</span><span class="badge">RAG-ready</span></div>
          <p style="margin-top:10px;">
            <a href="https://github.com/xinfeng-gu/text_signal_mvp" class="btn">Repo</a>
            <!-- <a href="https://xinfeng-gu.github.io/briefs/text_signal_mvp.pdf" class="btn">1-page brief</a> -->
          </p>
        </article>
        <article class="card md6">
          <h3>quant_backtest_min — Mid-freq with costs</h3>
          <p class="muted">Leakage-safe pipeline with transaction costs & slippage; equity charts and metrics.json out of the box.</p>
          <div class="badges"><span class="badge">Sharpe</span><span class="badge">IR</span><span class="badge">DD</span></div>
          <p style="margin-top:10px;">
            <a href="https://github.com/xinfeng-gu/quant_backtest_min" class="btn">Repo</a>
          </p>
        </article>
        <article class="card md6">
          <h3>univ3_lp_min — Uniswap v3 LP (toy)</h3>
          <p class="muted">Compare fee income vs impermanent loss across dynamic bands; simple, visual, and extendable to real pool data.</p>
          <div class="badges"><span class="badge">DeFi</span><span class="badge">LP</span><span class="badge">Sensitivity</span></div>
          <p style="margin-top:10px;">
            <a href="https://github.com/xinfeng-gu/univ3_lp_min" class="btn">Repo</a>
          </p>
        </article>
        <article class="card md6">
          <h3>zk_bench_min — Groth16 vs PLONK</h3>
          <p class="muted">Apple-to-apple benchmark on the same circuit: constraints, prover/verify time, memory, proof size.</p>
          <div class="badges"><span class="badge">ZK</span><span class="badge">MSM/FFT</span><span class="badge">Benchmark</span></div>
          <p style="margin-top:10px;">
            <a href="https://github.com/xinfeng-gu/zk_bench_min" class="btn">Repo</a>
          </p>
        </article>
      </div>
    </section>

    <section class="section" id="about">
      <h2>About</h2>
      <div class="card">
        <p>Hi! I’m <strong>Xinfeng</strong>. I work at the intersection of <em>Quant, Crypto-Quant, Zero-Knowledge systems, and LLMs</em>. I like small, reliable building blocks: code you can run, evidence you can verify, and brief documents that tell you what works and when it breaks.</p>
        <p class="muted">Keywords: mid-freq alpha, event studies, oracle reliability, Uniswap v3 LP, MSM/FFT, verifiable backtesting.</p>
      </div>
    </section>

    <section class="section" id="contact">
      <h2>Contact</h2>
      <div class="card">
        <p class="muted">I’m open to remote internships and research collaborations.</p>
        <p>
          <a class="btn" href="mailto:martineuclid@gmail.com">martineuclid@gmail.com</a>
          <a class="btn" href="https://github.com/xinfeng-gu">GitHub</a>
          <!-- 把 LINKEDIN_ID 换成你的 LinkedIn handle 再解开 -->
          <!-- <a class="btn" href="https://www.linkedin.com/in/LINKEDIN_ID/">LinkedIn</a> -->
        </p>
        <p class="muted">Last updated: <span id="lastUpdated">—</span></p>
      </div>
    </section>
  </main>

  <footer class="container footer">
    <span>© <span id="yr"></span> Xinfeng Gu. All rights reserved.</span>
    <div class="links">
      <a href="#home">Back to top ↑</a>
      <!-- 没有 sitemap.xml 就先别放 -->
      <!-- <a href="./sitemap.xml">Sitemap</a> -->
    </div>
  </footer>

  <script>
    // Theme toggle（避免可选链，兼容旧浏览器）
    var btn = document.getElementById('themeToggle');
    var mode = localStorage.getItem('theme');
    if (mode === 'light') document.body.classList.add('light');
    if (btn){
      btn.addEventListener('click', function(){
        document.body.classList.toggle('light');
        localStorage.setItem('theme', document.body.classList.contains('light') ? 'light' : 'dark');
      });
    }
    // Year & last updated
    document.getElementById('yr').textContent = new Date().getFullYear();
    document.getElementById('lastUpdated').textContent = new Date(document.lastModified).toLocaleDateString();
  </script>

  <!-- JSON-LD for SEO -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Person",
    "name": "Xinfeng Gu",
    "url": "https://xinfeng-gu.github.io/",
    "email": "mailto:martineuclid@gmail.com",
    "sameAs": [
      "https://github.com/xinfeng-gu"
    ],
    "jobTitle": "Quant / Crypto-Quant / ZK"
  }
  </script>
</body>
</html>
