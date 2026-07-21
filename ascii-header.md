<svg width="1200" height="320" viewBox="0 0 1200 320" xmlns="http://www.w3.org/2000/svg"
     font-family="'Cascadia Code','Consolas',Menlo,Monaco,monospace">

  <defs>
    <!-- Hintergrundgradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#04070d"/>
      <stop offset="100%" stop-color="#0b111c"/>
    </linearGradient>

    <!-- Titelgradient -->
    <linearGradient id="titleGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00ffd0"/>
      <stop offset="50%" stop-color="#ffd700"/>
      <stop offset="100%" stop-color="#00ffd0"/>
    </linearGradient>

    <!-- Glow Layer -->
    <radialGradient id="glow" cx="50%" cy="35%" r="70%">
      <stop offset="0%" stop-color="#ffd700" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#ffd700" stop-opacity="0"/>
    </radialGradient>

    <!-- Grid -->
    <pattern id="grid" width="28" height="28" patternUnits="userSpaceOnUse">
      <path d="M 28 0 L 0 0 0 28" fill="none" stroke="#0d1a28" stroke-width="0.8"/>
    </pattern>

    <!-- Soft Glow Filter -->
    <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="3.2" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <style>
    /* Glow Pulsing Overlay */
    .hero-overlay {
      animation: glowPulse 6s ease-in-out infinite;
    }
    @keyframes glowPulse {
      0% { opacity: 0.25; }
      50% { opacity: 0.6; }
      100% { opacity: 0.25; }
    }

    /* Titel Glow */
    .hero-title {
      animation: titleGlow 4s ease-in-out infinite;
    }
    @keyframes titleGlow {
      0% { filter: drop-shadow(0 0 10px rgba(255,215,0,0.25)); }
      50% { filter: drop-shadow(0 0 22px rgba(255,215,0,0.45)); }
      100% { filter: drop-shadow(0 0 10px rgba(255,215,0,0.25)); }
    }

    /* Ticker */
    .ticker {
      animation: tickerSlide 18s linear infinite;
    }
    @keyframes tickerSlide {
      from { transform: translateX(0%); }
      to { transform: translateX(-100%); }
    }

    /* Code Rain */
    .code-column {
      animation: rain 6s linear infinite;
    }
    .code-column:nth-child(2) { animation-duration: 7s; animation-delay: 1s; }
    .code-column:nth-child(3) { animation-duration: 5.5s; animation-delay: 2s; }
    .code-column:nth-child(4) { animation-duration: 6.5s; animation-delay: 0.5s; }
    .code-column:nth-child(5) { animation-duration: 7.5s; animation-delay: 1.5s; }
    .code-column:nth-child(6) { animation-duration: 5.8s; animation-delay: 2.3s; }
    .code-column:nth-child(7) { animation-duration: 6.2s; animation-delay: 0.8s; }
    .code-column:nth-child(8) { animation-duration: 7.2s; animation-delay: 1.8s; }

    @keyframes rain {
      0%   { transform: translateY(-320px); opacity: 0; }
      10%  { opacity: 1; }
      90%  { opacity: 1; }
      100% { transform: translateY(320px); opacity: 0; }
    }
  </style>

  <!-- Background -->
  <rect width="1200" height="320" rx="18" fill="url(#bgGrad)"/>
  <rect width="1200" height="320" rx="18" fill="url(#grid)" opacity="0.35"/>
  <rect class="hero-overlay" width="1200" height="320" rx="18" fill="url(#glow)" opacity="0.9"/>

  <!-- Border -->
  <rect x="5" y="5" width="1190" height="310" rx="16"
        fill="none" stroke="url(#titleGrad)" stroke-width="1.4" opacity="0.55"/>

  <!-- Matrix Code Rain -->
  <g fill="#00ff9a" font-size="14" opacity="0.75">
    <g class="code-column" transform="translate(120, -320)">
      <text x="0" y="40">01</text>
      <text x="0" y="70">0xA</text>
      <text x="0" y="100">11</text>
      <text x="0" y="130">0xF</text>
      <text x="0" y="160">10</text>
      <text x="0" y="190">0x3</text>
      <text x="0" y="220">01</text>
      <text x="0" y="250">0xC</text>
      <text x="0" y="280">11</text>
    </g>

    <g class="code-column" transform="translate(220, -320)">
      <text x="0" y="40">0x9</text>
      <text x="0" y="70">10</text>
      <text x="0" y="100">0xB</text>
      <text x="0" y="130">01</text>
      <text x="0" y="160">0xD</text>
      <text x="0" y="190">11</text>
      <text x="0" y="220">0x2</text>
      <text x="0" y="250">10</text>
      <text x="0" y="280">0xE</text>
    </g>

    <g class="code-column" transform="translate(320, -320)">
      <text x="0" y="40">11</text>
      <text x="0" y="70">0x7</text>
      <text x="0" y="100">01</text>
      <text x="0" y="130">0xA</text>
      <text x="0" y="160">10</text>
      <text x="0" y="190">0x1</text>
      <text x="0" y="220">11</text>
      <text x="0" y="250">0xC</text>
      <text x="0" y="280">01</text>
    </g>

    <g class="code-column" transform="translate(420, -320)">
      <text x="0" y="40">0xF</text>
      <text x="0" y="70">10</text>
      <text x="0" y="100">0x4</text>
      <text x="0" y="130">11</text>
      <text x="0" y="160">0x8</text>
      <text x="0" y="190">01</text>
      <text x="0" y="220">0xB</text>
      <text x="0" y="250">10</text>
      <text x="0" y="280">0x2</text>
    </g>

    <g class="code-column" transform="translate(520, -320)">
      <text x="0" y="40">01</text>
      <text x="0" y="70">0x6</text>
      <text x="0" y="100">11</text>
      <text x="0" y="130">0x9</text>
      <text x="0" y="160">10</text>
      <text x="0" y="190">0x3</text>
      <text x="0" y="220">01</text>
      <text x="0" y="250">0xD</text>
      <text x="0" y="280">11</text>
    </g>

    <g class="code-column" transform="translate(620, -320)">
      <text x="0" y="40">0xA</text>
      <text x="0" y="70">10</text>
      <text x="0" y="100">0x5</text>
      <text x="0" y="130">01</text>
      <text x="0" y="160">0xC</text>
      <text x="0" y="190">11</text>
      <text x="0" y="220">0x1</text>
      <text x="0" y="250">10</text>
      <text x="0" y="280">0xE</text>
    </g>

    <g class="code-column" transform="translate(720, -320)">
      <text x="0" y="40">11</text>
      <text x="0" y="70">0x7</text>
      <text x="0" y="100">01</text>
      <text x="0" y="130">0xB</text>
      <text x="0" y="160">10</text>
      <text x="0" y="190">0x2</text>
      <text x="0" y="220">11</text>
      <text x="0" y="250">0xC</text>
      <text x="0" y="280">01</text>
    </g>

    <g class="code-column" transform="translate(820, -320)">
      <text x="0" y="40">0xF</text>
      <text x="0" y="70">10</text>
      <text x="0" y="100">0x4</text>
      <text x="0" y="130">11</text>
      <text x="0" y="160">0x8</text>
      <text x="0" y="190">01</text>
      <text x="0" y="220">0x9</text>
      <text x="0" y="250">10</text>
      <text x="0" y="280">0x3</text>
    </g>
  </g>

  <!-- Titel -->
  <text x="50%" y="34%" text-anchor="middle" font-size="52" font-weight="700"
        class="hero-title"
        fill="url(#titleGrad)" filter="url(#softGlow)" letter-spacing="1.5">
    &gt;_ MF-swiss
  </text>

  <!-- Subtitle -->
  <text x="50%" y="48%" text-anchor="middle" font-size="18"
        fill="#9fe8d4" letter-spacing="0.7">
    Full‑Stack Engineering · Java Backend · React Frontend · Cloud & Containerization
  </text>

  <!-- Ticker -->
  <g transform="translate(80, 220)">
    <clipPath id="tickerClip">
      <rect x="0" y="-18" width="1040" height="40" rx="8"/>
    </clipPath>

    <rect x="0" y="-18" width="1040" height="40" rx="8"
          fill="#050a12" opacity="0.85" stroke="#0f1b2a" stroke-width="1"/>

    <g clip-path="url(#tickerClip)">
      <text class="ticker" x="0" y="8" font-size="16" fill="#6c8a9b">
        Java · Spring Boot · REST‑APIs · React · Vite · PostgreSQL · Docker · Git · UI/UX‑Design ·
        Software‑Architektur · Containerisierung · Debugging · API‑Integration ·
        Java · Spring Boot · REST‑APIs · React · Vite · PostgreSQL · Docker · Git · UI/UX‑Design ·
        Software‑Architektur · Containerisierung · Debugging · API‑Integration ·
      </text>
    </g>
  </g>

</svg>
