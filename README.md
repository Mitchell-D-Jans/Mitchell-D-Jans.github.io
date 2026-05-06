<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Mitchell D. Jans</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,600;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #f5f2eb;
      --surface: #fff;
      --ink: #1c1c1c;
      --muted: #6b6455;
      --accent: #2a5c8a;
      --accent-light: #dde8f2;
      --rule: #d5cfc5;
      --tab-h: 48px;
    }
 
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
    body {
      font-family: 'EB Garamond', Georgia, serif;
      background: var(--bg);
      color: var(--ink);
      min-height: 100vh;
      font-size: 17px;
      line-height: 1.7;
    }
 
    /* ── Header ── */
    header {
      background: var(--surface);
      border-bottom: 1px solid var(--rule);
      padding: 3rem 2rem 0;
      text-align: center;
    }
 
    .avatar-wrap {
      width: 130px;
      height: 130px;
      border-radius: 50%;
      overflow: hidden;
      margin: 0 auto 1.25rem;
      border: 3px solid var(--accent);
      box-shadow: 0 4px 20px rgba(42,92,138,.15);
    }
 
    .avatar-wrap img {
      width: 100%; height: 100%; object-fit: cover;
    }
 
    h1 {
      font-size: 2rem;
      font-weight: 600;
      letter-spacing: .01em;
    }
 
    .subtitle {
      font-style: italic;
      color: var(--muted);
      margin-top: .25rem;
      font-size: 1rem;
    }
 
    .bio {
      max-width: 620px;
      margin: 1rem auto 0;
      color: var(--muted);
      font-size: .95rem;
    }
 
    /* ── Tab nav ── */
    .tab-nav {
      display: flex;
      justify-content: center;
      gap: 0;
      margin-top: 2rem;
      border-top: 1px solid var(--rule);
    }
 
    .tab-btn {
      font-family: 'DM Mono', monospace;
      font-size: .78rem;
      letter-spacing: .08em;
      text-transform: uppercase;
      padding: 0 2rem;
      height: var(--tab-h);
      border: none;
      background: transparent;
      color: var(--muted);
      cursor: pointer;
      position: relative;
      transition: color .2s;
    }
 
    .tab-btn::after {
      content: '';
      position: absolute;
      bottom: 0; left: 20%; right: 20%;
      height: 2px;
      background: var(--accent);
      transform: scaleX(0);
      transition: transform .2s;
    }
 
    .tab-btn:hover { color: var(--ink); }
    .tab-btn.active { color: var(--accent); }
    .tab-btn.active::after { transform: scaleX(1); }
 
    /* ── Tab content ── */
    .tab-panel {
      display: none;
      max-width: 820px;
      margin: 0 auto;
      padding: 3rem 1.5rem 5rem;
      animation: fadeUp .3s ease;
    }
 
    .tab-panel.active { display: block; }
 
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(8px); }
      to   { opacity: 1; transform: translateY(0); }
    }
 
    /* ── Section headings ── */
    h2 {
      font-size: 1.5rem;
      font-weight: 600;
      margin-bottom: .4rem;
      color: var(--ink);
    }
 
    h3 {
      font-size: 1.1rem;
      font-weight: 600;
      margin: 2rem 0 .5rem;
      color: var(--accent);
      font-style: italic;
    }
 
    .section-rule {
      border: none;
      border-top: 1px solid var(--rule);
      margin: 2.5rem 0;
    }
 
    p { margin-bottom: 1rem; }
 
    /* ── Research blocks ── */
    .research-block {
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 8px;
      padding: 1.75rem;
      margin-bottom: 2rem;
    }
 
    .research-block h3 { margin-top: 0; }
 
    video, img.fig {
      display: block;
      width: 100%;
      max-width: 680px;
      margin: 1.25rem auto;
      border-radius: 6px;
      border: 1px solid var(--rule);
    }
 
    figcaption {
      text-align: center;
      font-style: italic;
      font-size: .88rem;
      color: var(--muted);
      margin-top: .4rem;
      margin-bottom: 1rem;
    }
 
    /* ── References ── */
    .ref-list {
      list-style: none;
      padding: 0;
    }
 
    .ref-list li {
      padding: .75rem 0;
      border-bottom: 1px solid var(--rule);
      font-size: .95rem;
    }
 
    .ref-list li:last-child { border-bottom: none; }
 
    /* ── Links panel ── */
    .link-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
      margin-top: 1.5rem;
    }
 
    .link-card {
      display: flex;
      align-items: center;
      gap: 1rem;
      padding: 1.2rem 1.5rem;
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 8px;
      text-decoration: none;
      color: var(--ink);
      transition: border-color .2s, box-shadow .2s;
    }
 
    .link-card:hover {
      border-color: var(--accent);
      box-shadow: 0 4px 16px rgba(42,92,138,.1);
    }
 
    .link-card .icon {
      font-size: 1.4rem;
      flex-shrink: 0;
    }
 
    .link-card .label { font-size: .92rem; color: var(--muted); }
    .link-card .name  { font-weight: 600; }
 
    a { color: var(--accent); }
    a:hover { text-decoration: underline; }
  </style>
</head>
<body>
 
<header>
  <div class="avatar-wrap">
    <img src="/Self.jpg" alt="Mitchell D. Jans">
  </div>
  <h1>Mitchell D. Jans</h1>
  <p class="subtitle">PhD Candidate · Interfacial Water Group · Princeton University</p>
  <p class="bio">
    Advised by Professor Ian Bourg in the Civil and Environmental Engineering Department.
    B.S. Civil Engineering, University of Minnesota Duluth (2022).<br>
    M.A. Civil &amp; Environmental Engineering, Princeton University (2024).
  </p>
 
  <nav class="tab-nav" role="tablist">
    <button class="tab-btn active" onclick="switchTab('research', this)" role="tab">Research: Sediment Transport</button>
    <button class="tab-btn" onclick="switchTab('water', this)" role="tab">Research: Water Quality</button>
    <button class="tab-btn" onclick="switchTab('engineering', this)" role="tab">Research:Engineering Applications</button>
    <button class="tab-btn" onclick="switchTab('publications', this)" role="tab">Publications and Presentations</button>
    <button class="tab-btn" onclick="switchTab('connect', this)" role="tab">Connect</button>
  </nav>
</header>
 
<!-- ═══ RESEARCH ═══ -->
<section id="research" class="tab-panel active" role="tabpanel">
  <h2>Mineralogical Insights in Soft Geophysical Flows &amp; Sediment Transport</h2>
 
  <div class="research-block">
    <h3>Impact of Clay Minerals on Sediment Gravity Flows</h3>
    <p>
      Cohesive sediment gravity flows are important geophysical flows that transport large volumes
      of sediment in marine and lacustrine environments. Despite their significance as a sediment
      transport mechanism, the physical processes governing these flows remain poorly understood
      due to complex mechanical and chemical interactions within clay-rich flows.
    </p>
    <p>
      This research develops a computational fluid dynamics model to simulate cohesive sediment
      gravity flows and investigate how sediment properties control flow behavior. The model
      captures multiple flow regimes and can accurately predict key characteristics such as flow
      morphology and propagation speed.
    </p>
    <video autoplay loop muted playsinline controls>
      <source src="SGFExample.mp4" type="video/mp4">
    </video>
  </div>
 
  <div class="research-block">
    <h3>Impact of Clay Content on Sediment Bed Erodibility</h3>
    <p>
      The erosion of clay-rich sediment beds remains difficult to predict compared to granular
      sediment beds, which can often be described using the
      <a href="https://en.wikipedia.org/wiki/Shields_formula" target="_blank">Shields curve and formula</a>.
      Even small amounts of clay can significantly alter erosion thresholds, causing sediment beds
      to behave very differently from purely granular systems.
    </p>
    <p>
      In this work, we collaborate with
      <a href="https://yang.cege.umn.edu" target="_blank">experimental researchers</a>
      at the University of Minnesota to develop and validate a computational fluid dynamics model
      capable of predicting incipient erosion in clay-rich sediment beds. The model is tested
      across a range of geophysically relevant conditions, including variations in salinity,
      consolidation state, and sediment permeability.
    </p>
    <video autoplay loop muted playsinline controls>
      <source src="ErosionEvent1.mp4" type="video/mp4">
    </video>
    <video autoplay loop muted playsinline controls>
      <source src="ErosionEvent2.mp4" type="video/mp4">
    </video>
  </div>
</section>
 
<!-- ═══ WATER QUALITY ═══ -->
<section id="water" class="tab-panel" role="tabpanel">
  <h2>Water Quality Impacts in Temperate Lakes and Rivers</h2>
 
  <div class="research-block">
    <h3>Historic Water Quality</h3>
    <figure>
      <img class="fig" src="/St_Louis_River_WaterQualityHistory.png" alt="St. Louis River historical water quality data">
      <figcaption>Adapted from Jans (2020).</figcaption>
    </figure>
  </div>
 
  <div class="research-block">
    <h3>Monitoring Surface Water Quality and Temperature</h3>
    <p>Ongoing work monitoring surface water quality and temperature dynamics in temperate lake and river systems.</p>
  </div>
</section>
 
<!-- ═══ ENGINEERING ═══ -->
<section id="engineering" class="tab-panel" role="tabpanel">
  <h2>Improving Engineering Insights to Reduce Anthropogenic Impact</h2>
 
  <div class="research-block">
    <h3>Biochar Application to Reduce Methyl Mercury Bioaccumulation</h3>
    <p>
      Investigating the use of biochar (activated carbon) as a sediment amendment to reduce
      methyl mercury bioaccumulation from moderately contaminated sediments.
    </p>
    <figure>
      <img class="fig" src="/MeHg_Conc_Jans_HonorsThesis.png" alt="MeHg concentration data from honors thesis">
      <figcaption>Adapted from Jans (2022).</figcaption>
    </figure>
  </div>
 
  <div class="research-block">
    <h3>Biopolymer Application to Reduce Sediment Erodibility</h3>
    <figure>
      <img class="fig" src="/JansViscosityBiopolymerAddition.png" alt="Viscosity measurements with biopolymer addition">
    </figure>
  </div>
</section>
 
<!-- ═══ PUBLICATIONS ═══ -->
<section id="publications" class="tab-panel" role="tabpanel">
  <h2>References &amp; Publications</h2>
  <ul class="ref-list">
    <li>
      Jans, M. D. (2022). <em>Exploring Activated Carbon's Impact on Mercury Geochemistry and Eutrophication</em>.
      Undergraduate Honors Thesis, University of Minnesota Duluth.
    </li>
    <li>
      Jans, M. D. (2020). <em>Analysis and Digitization of Historical Water Quality in Western Lake Superior</em>.
      University of Minnesota Virtual Undergraduate Research Symposium.
    </li>
  </ul>
</section>
 
<!-- ═══ CONNECT ═══ -->
<section id="connect" class="tab-panel" role="tabpanel">
  <h2>Connect</h2>
  <p>Feel free to reach out through any of the following platforms.</p>
  <div class="link-grid">
    <a class="link-card" href="https://www.linkedin.com/in/mitchelljans/" target="_blank">
      <span class="icon">💼</span>
      <div>
        <div class="name">LinkedIn</div>
        <div class="label">mitchelljans</div>
      </div>
    </a>
    <a class="link-card" href="https://scholar.google.com/citations?user=iKfFNVEAAAAJ&hl=en&oi=ao" target="_blank">
      <span class="icon">🎓</span>
      <div>
        <div class="name">Google Scholar</div>
        <div class="label">View publications</div>
      </div>
    </a>
  </div>
</section>
 
<script>
  function switchTab(id, btn) {
    document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    btn.classList.add('active');
  }
</script>
 
</body>
</html>
 
