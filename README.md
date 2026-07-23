<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="1180" height="610">
  <defs>
    <!-- Dark theme gradients -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#030712"/>
      <stop offset="100%" stop-color="#0F172A"/>
    </linearGradient>

    <radialGradient id="glow1" cx="20%" cy="30%" r="60%">
      <stop offset="0%" stop-color="rgba(124,58,237,0.15)"/>
      <stop offset="100%" stop-color="rgba(124,58,237,0)"/>
    </radialGradient>

    <radialGradient id="glow2" cx="80%" cy="70%" r="50%">
      <stop offset="0%" stop-color="rgba(34,211,238,0.12)"/>
      <stop offset="100%" stop-color="rgba(34,211,238,0)"/>
    </radialGradient>

    <radialGradient id="glow3" cx="50%" cy="50%" r="40%">
      <stop offset="0%" stop-color="rgba(16,185,129,0.08)"/>
      <stop offset="100%" stop-color="rgba(16,185,129,0)"/>
    </radialGradient>

    <!-- ASCII Gradient -->
    <linearGradient id="asciiGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7C3AED">
        <animate attributeName="stop-color" values="#7C3AED;#22D3EE;#10B981;#7C3AED" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" stop-color="#22D3EE">
        <animate attributeName="stop-color" values="#22D3EE;#10B981;#7C3AED;#22D3EE" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#10B981">
        <animate attributeName="stop-color" values="#10B981;#7C3AED;#22D3EE;#10B981" dur="8s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <!-- Accent Gradient -->
    <linearGradient id="accentGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7C3AED"/>
      <stop offset="50%" stop-color="#22D3EE"/>
      <stop offset="100%" stop-color="#10B981"/>
    </linearGradient>

    <!-- Glassmorphism filter -->
    <filter id="glass" x="-5%" y="-5%" width="110%" height="110%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="1" result="blur"/>
      <feFlood flood-color="rgba(255,255,255,0.03)" result="color"/>
      <feComposite in="color" in2="blur" operator="in" result="shadow"/>
      <feMerge>
        <feMergeNode in="shadow"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="glowFilter" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Scanline pattern -->
    <pattern id="scanlines" width="4" height="4" patternUnits="userSpaceOnUse">
      <line x1="0" y1="0" x2="4" y2="0" stroke="rgba(0,0,0,0.03)" stroke-width="1"/>
    </pattern>

    <!-- Noise texture -->
    <filter id="noise">
      <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="4" stitchTiles="stitch"/>
      <feColorMatrix type="matrix" values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 0.03 0"/>
    </filter>

    <!-- Border shimmer -->
    <linearGradient id="borderShimmer" x1="-100%" y1="-100%" x2="200%" y2="200%">
      <stop offset="0%" stop-color="rgba(255,255,255,0)">
        <animate attributeName="offset" values="0;1" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="30%" stop-color="rgba(255,255,255,0.08)">
        <animate attributeName="offset" values="0.3;1.3" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="60%" stop-color="rgba(255,255,255,0.15)">
        <animate attributeName="offset" values="0.6;1.6" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="rgba(255,255,255,0)">
        <animate attributeName="offset" values="1;2" dur="4s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <!-- Cursor blink -->
    <style>
      @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
      @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-6px)} }
      @keyframes pulse { 0%,100%{opacity:0.6} 50%{opacity:1} }
      .cursor{animation:blink 1s step-end infinite}
      .float{animation:float 4s ease-in-out infinite}
      .pulse{animation:pulse 3s ease-in-out infinite}
    </style>
  </defs>

  <!-- Background -->
  <rect width="1180" height="610" rx="16" fill="url(#bgGrad)"/>
  <rect width="1180" height="610" rx="16" fill="url(#glow1)"/>
  <rect width="1180" height="610" rx="16" fill="url(#glow2)"/>
  <rect width="1180" height="610" rx="16" fill="url(#glow3)"/>

  <!-- Noise overlay -->
  <rect width="1180" height="610" rx="16" filter="url(#noise)" opacity="0.4"/>

  <!-- Border glow -->
  <rect x="0.5" y="0.5" width="1179" height="609" rx="15.5" fill="none" stroke="rgba(124,58,237,0.2)" stroke-width="1">
    <animate attributeName="stroke" values="rgba(124,58,237,0.2);rgba(34,211,238,0.2);rgba(16,185,129,0.2);rgba(124,58,237,0.2)" dur="6s" repeatCount="indefinite"/>
  </rect>

  <!-- Shimmer border -->
  <rect x="0.5" y="0.5" width="1179" height="609" rx="15.5" fill="none" stroke="url(#borderShimmer)" stroke-width="1.5"/>

  <!-- ==================== LEFT SECTION - ASCII ==================== -->
  <g transform="translate(0,0)">
    <!-- Glass panel background -->
    <rect x="20" y="20" width="430" height="570" rx="12" fill="rgba(15,23,42,0.6)" filter="url(#glass)"/>
    <rect x="20" y="20" width="430" height="570" rx="12" fill="none" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

    <!-- ASCII Art with typing animation -->
    <g class="float" filter="url(#glowFilter)">
      <!-- ASCII lines with sequential reveal -->
      <g font-family="monospace" font-size="11" fill="url(#asciiGrad)" letter-spacing="0.5">
        <!-- Line 1 -->
        <text x="40" y="65" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="0.2s" dur="0.1s" fill="freeze"/>
          <tspan>     ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄</tspan>
        </text>

        <!-- Line 2 -->
        <text x="40" y="80" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="0.6s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌</tspan>
        </text>

        <!-- Line 3 -->
        <text x="40" y="95" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="1.0s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░█▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀█░▌</tspan>
        </text>

        <!-- Line 4 -->
        <text x="40" y="110" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="1.4s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░▌       ▐░▌</tspan>
        </text>

        <!-- Line 5 -->
        <text x="40" y="125" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="1.8s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░█▄▄▄▄▄▄▄█░▌</tspan>
        </text>

        <!-- Line 6 -->
        <text x="40" y="140" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="2.2s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░░░░░░░░░░░▌</tspan>
        </text>

        <!-- Line 7 -->
        <text x="40" y="155" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="2.6s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░█▀▀▀▀▀▀▀█░▌</tspan>
        </text>

        <!-- Line 8 -->
        <text x="40" y="170" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="3.0s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░▌       ▐░▌</tspan>
        </text>

        <!-- Line 9 -->
        <text x="40" y="185" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="3.4s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░█▄▄▄▄▄▄▄█░▌▐░█▄▄▄▄▄▄▄█░▌▐░▌       ▐░▌</tspan>
        </text>

        <!-- Line 10 -->
        <text x="40" y="200" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="3.8s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌▐░▌       ▐░▌</tspan>
        </text>

        <!-- Line 11 -->
        <text x="40" y="215" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="4.2s" dur="0.1s" fill="freeze"/>
          <tspan>     ▀▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀▀  ▀         ▀</tspan>
        </text>

        <!-- Line 12 -->
        <text x="40" y="240" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="4.6s" dur="0.1s" fill="freeze"/>
          <tspan>     ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄</tspan>
        </text>

        <!-- Line 13 -->
        <text x="40" y="255" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="5.0s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌</tspan>
        </text>

        <!-- Line 14 -->
        <text x="40" y="270" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="5.4s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░█▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀▀▀</tspan>
        </text>

        <!-- Line 15 -->
        <text x="40" y="285" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="5.8s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░▌</tspan>
        </text>

        <!-- Line 16 -->
        <text x="40" y="300" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="6.2s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░█▄▄▄▄▄▄▄▄▄</tspan>
        </text>

        <!-- Line 17 -->
        <text x="40" y="315" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="6.6s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░▌       ▐░▌▐░▌       ▐░▌▐░░░░░░░░░░░▌</tspan>
        </text>

        <!-- Line 18 -->
        <text x="40" y="330" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="7.0s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░█▄▄▄▄▄▄▄█░▌▐░█▄▄▄▄▄▄▄█░▌ ▀▀▀▀▀▀▀▀▀█░▌</tspan>
        </text>

        <!-- Line 19 -->
        <text x="40" y="345" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="7.4s" dur="0.1s" fill="freeze"/>
          <tspan>    ▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌          ▐░▌</tspan>
        </text>

        <!-- Line 20 -->
        <text x="40" y="360" opacity="0">
          <animate attributeName="opacity" values="0;1" begin="7.8s" dur="0.1s" fill="freeze"/>
          <tspan>     ▀▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀▀           ▀</tspan>
        </text>
      </g>

      <!-- Cursor -->
      <text x="40" y="380" font-family="monospace" font-size="14" fill="url(#asciiGrad)">
        <tspan class="cursor">█</tspan>
        <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>
      </text>
    </g>

    <!-- Scanline overlay on ASCII -->
    <rect x="20" y="20" width="430" height="570" rx="12" fill="url(#scanlines)" opacity="0.15">
      <animate attributeName="y" values="0;570" dur="8s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- ==================== RIGHT SECTION - TERMINAL ==================== -->
  <g transform="translate(470,20)">
    <!-- Glass panel background -->
    <rect x="0" y="0" width="690" height="570" rx="12" fill="rgba(15,23,42,0.6)" filter="url(#glass)"/>
    <rect x="0" y="0" width="690" height="570" rx="12" fill="none" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

    <!-- Terminal header -->
    <rect x="0" y="0" width="690" height="36" rx="12" fill="rgba(255,255,255,0.03)"/>
    <rect x="0" y="20" width="690" height="16" fill="rgba(15,23,42,0.6)"/>
    <circle cx="16" cy="18" r="5" fill="#EF4444" opacity="0.8"/>
    <circle cx="32" cy="18" r="5" fill="#F59E0B" opacity="0.8"/>
    <circle cx="48" cy="18" r="5" fill="#10B981" opacity="0.8"/>
    <text x="310" y="22" font-family="monospace" font-size="11" fill="#94A3B8">developer@portfolio — zsh</text>

    <!-- === GREETING === -->
    <text x="28" y="70" font-family="monospace" font-size="13" fill="#94A3B8">
      <tspan>┌──</tspan>
      <animate attributeName="opacity" values="0;1" begin="0.5s" dur="0.3s" fill="freeze"/>
    </text>

    <text x="28" y="95" font-family="monospace" font-size="15" fill="#F8FAFC" font-weight="bold" opacity="0">
      <animate attributeName="opacity" values="0;1" begin="1.0s" dur="0.5s" fill="freeze"/>
      <tspan fill="url(#accentGrad)">❯</tspan>
      <tspan> Hello, I'm </tspan>
      <tspan fill="url(#accentGrad)">John Doe</tspan>
    </text>

    <!-- === TYPING TITLE === -->
    <text x="28" y="130" font-family="monospace" font-size="20" fill="#F8FAFC" font-weight="bold" opacity="0">
      <animate attributeName="opacity" values="0;1" begin="2.0s" dur="0.3s" fill="freeze"/>
      <tspan fill="url(#accentGrad)">❯</tspan>
      <tspan> </tspan>
      <tspan>
        <animate attributeName="fill" values="#7C3AED;#22D3EE;#10B981;#7C3AED" dur="6s" repeatCount="indefinite"/>
        Frontend Engineer
      </tspan>
      <animate attributeName="opacity" values="0;1" begin="2.0s" dur="0.3s" fill="freeze"/>
    </text>

    <!-- Typing cursor for title -->
    <text x="250" y="130" font-family="monospace" font-size="20" fill="#7C3AED" opacity="0">
      <animate attributeName="opacity" values="0;1" begin="2.3s" dur="0.1s" fill="freeze"/>
      <tspan class="cursor">|</tspan>
    </text>

    <!-- === INFO ITEMS === -->
    <g opacity="0">
      <animate attributeName="opacity" values="0;1" begin="3.5s" dur="0.5s" fill="freeze"/>

      <!-- Location -->
      <text x="28" y="170" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>├── </tspan>
        <tspan fill="#64748B">📍</tspan>
        <tspan> Location: </tspan>
        <tspan fill="#F8FAFC"> Bengaluru </tspan>
      </text>

      <!-- Education -->
      <text x="28" y="195" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>├── </tspan>
        <tspan fill="#64748B">🎓</tspan>
        <tspan> Education: </tspan>
        <tspan fill="#F8FAFC"> B.E in Computer Science </tspan>
      </text>

      <!-- Current Focus -->
      <text x="28" y="220" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>├── </tspan>
        <tspan fill="#64748B">⚡</tspan>
        <tspan> Focus: </tspan>
        <tspan fill="#22D3EE">Building scalable web apps</tspan>
      </text>

      <!-- Portfolio -->
      <text x="28" y="245" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>├── </tspan>
        <tspan fill="#64748B">🌐</tspan>
        <tspan> Portfolio: </tspan>
        <tspan fill="#7C3AED">john.dev</tspan>
      </text>

      <!-- Email -->
      <text x="28" y="270" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>└── </tspan>
        <tspan fill="#64748B">✉</tspan>
        <tspan> Email: </tspan>
        <tspan fill="#10B981">john@example.com</tspan>
      </text>
    </g>

    <!-- === SKILLS SECTION === -->
    <text x="28" y="315" font-family="monospace" font-size="13" fill="#94A3B8" opacity="0">
      <animate attributeName="opacity" values="0;1" begin="4.5s" dur="0.3s" fill="freeze"/>
      <tspan>┌── Skills ──</tspan>
    </text>

    <!-- Skill pills -->
    <g opacity="0">
      <animate attributeName="opacity" values="0;1" begin="5.0s" dur="0.5s" fill="freeze"/>

      <!-- Row 1 -->
      <g transform="translate(28,340)">
        <rect x="0" y="0" width="80" height="30" rx="15" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
          <animate attributeName="width" values="80;85;80" dur="3s" repeatCount="indefinite"/>
        </rect>
        <text x="40" y="20" font-family="monospace" font-size="12" fill="#C084FC" text-anchor="middle">React</text>
      </g>

      <g transform="translate(118,340)">
        <rect x="0" y="0" width="80" height="30" rx="15" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
          <animate attributeName="width" values="80;85;80" dur="3.2s" repeatCount="indefinite"/>
        </rect>
        <text x="40" y="20" font-family="monospace" font-size="12" fill="#67E8F9" text-anchor="middle">Next.js</text>
      </g>

      <g transform="translate(208,340)">
        <rect x="0" y="0" width="90" height="30" rx="15" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
          <animate attributeName="width" values="90;95;90" dur="2.8s" repeatCount="indefinite"/>
        </rect>
        <text x="45" y="20" font-family="monospace" font-size="12" fill="#6EE7B7" text-anchor="middle">TypeScript</text>
      </g>

      <g transform="translate(308,340)">
        <rect x="0" y="0" width="80" height="30" rx="15" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
          <animate attributeName="width" values="80;85;80" dur="3.5s" repeatCount="indefinite"/>
        </rect>
        <text x="40" y="20" font-family="monospace" font-size="12" fill="#C084FC" text-anchor="middle">Tailwind</text>
      </g>

      <g transform="translate(398,340)">
        <rect x="0" y="0" width="70" height="30" rx="15" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
          <animate attributeName="width" values="70;75;70" dur="3.1s" repeatCount="indefinite"/>
        </rect>
        <text x="35" y="20" font-family="monospace" font-size="12" fill="#67E8F9" text-anchor="middle">Python</text>
      </g>

      <!-- Row 2 -->
      <g transform="translate(28,380)">
        <rect x="0" y="0" width="80" height="30" rx="15" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
          <animate attributeName="width" values="80;85;80" dur="2.9s" repeatCount="indefinite"/>
        </rect>
        <text x="40" y="20" font-family="monospace" font-size="12" fill="#6EE7B7" text-anchor="middle">Docker</text>
      </g>

      <g transform="translate(118,380)">
        <rect x="0" y="0" width="90" height="30" rx="15" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
          <animate attributeName="width" values="90;95;90" dur="3.3s" repeatCount="indefinite"/>
        </rect>
        <text x="45" y="20" font-family="monospace" font-size="12" fill="#C084FC" text-anchor="middle">Postgres</text>
      </g>

      <g transform="translate(218,380)">
        <rect x="0" y="0" width="60" height="30" rx="15" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
          <animate attributeName="width" values="60;65;60" dur="3.6s" repeatCount="indefinite"/>
        </rect>
        <text x="30" y="20" font-family="monospace" font-size="12" fill="#67E8F9" text-anchor="middle">AWS</text>
      </g>

      <g transform="translate(288,380)">
        <rect x="0" y="0" width="55" height="30" rx="15" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
          <animate attributeName="width" values="55;60;55" dur="2.7s" repeatCount="indefinite"/>
        </rect>
        <text x="27" y="20" font-family="monospace" font-size="12" fill="#6EE7B7" text-anchor="middle">Git</text>
      </g>

      <g transform="translate(353,380)">
        <rect x="0" y="0" width="70" height="30" rx="15" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
          <animate attributeName="width" values="70;75;70" dur="3.4s" repeatCount="indefinite"/>
        </rect>
        <text x="35" y="20" font-family="monospace" font-size="12" fill="#C084FC" text-anchor="middle">Figma</text>
      </g>
    </g>

    <!-- === SOCIAL ICONS === -->
    <g opacity="0">
      <animate attributeName="opacity" values="0;1" begin="6.0s" dur="0.5s" fill="freeze"/>

      <text x="28" y="450" font-family="monospace" font-size="13" fill="#94A3B8">
        <tspan>└── Connect ──</tspan>
      </text>

      <!-- Social icons row -->
      <g transform="translate(28,470)">
        <!-- GitHub -->
        <g transform="translate(0,0)">
          <circle cx="18" cy="18" r="18" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1">
            <animate attributeName="r" values="18;20;18" dur="2s" repeatCount="indefinite"/>
          </circle>
          <text x="18" y="23" font-family="monospace" font-size="16" fill="#94A3B8" text-anchor="middle">🐙</text>
        </g>

        <!-- LinkedIn -->
        <g transform="translate(60,0)">
          <circle cx="18" cy="18" r="18" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1">
            <animate attributeName="r" values="18;20;18" dur="2.2s" repeatCount="indefinite"/>
          </circle>
          <text x="18" y="23" font-family="monospace" font-size="16" fill="#94A3B8" text-anchor="middle">🔗</text>
        </g>

        <!-- Twitter -->
        <g transform="translate(120,0)">
          <circle cx="18" cy="18" r="18" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1">
            <animate attributeName="r" values="18;20;18" dur="1.8s" repeatCount="indefinite"/>
          </circle>
          <text x="18" y="23" font-family="monospace" font-size="16" fill="#94A3B8" text-anchor="middle">🐦</text>
        </g>

        <!-- Portfolio -->
        <g transform="translate(180,0)">
          <circle cx="18" cy="18" r="18" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1">
            <animate attributeName="r" values="18;20;18" dur="2.4s" repeatCount="indefinite"/>
          </circle>
          <text x="18" y="23
