<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Animated AI Banner - Mariam Yasir</title>
  <style>
    html,body{height:100%;margin:0;background:#0b1020;display:flex;align-items:center;justify-content:center}
    .frame{width:980px;height:240px;}
  </style>
</head>
<body>
  <div class="frame">
    <!-- SVG banner: modern, animated, AI-themed -->
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 980 240" width="980" height="240" preserveAspectRatio="xMidYMid slice">
      <defs>
        <linearGradient id="g1" x1="0" x2="1">
          <stop offset="0%" stop-color="#00d2ff"/>
          <stop offset="50%" stop-color="#6a00ff"/>
          <stop offset="100%" stop-color="#ff007a"/>
        </linearGradient><filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- subtle noise texture -->
    <pattern id="dots" width="8" height="8" patternUnits="userSpaceOnUse" patternTransform="rotate(20)">
      <rect width="8" height="8" fill="rgba(255,255,255,0.01)"/>
      <circle cx="1.5" cy="1.5" r="0.6" fill="rgba(255,255,255,0.02)"/>
    </pattern>

    <!-- animated circuit path for tech feeling -->
    <linearGradient id="pathGrad" x1="0" x2="1">
      <stop offset="0%" stop-color="#00fff0"/>
      <stop offset="100%" stop-color="#9b59ff"/>
    </linearGradient>

  </defs>

  <!-- background rectangle -->
  <rect width="100%" height="100%" fill="#071127"/>

  <!-- moving gradient band -->
  <g filter="url(#glow)">
    <rect x="-300" y="20" width="1600" height="80" rx="40" fill="url(#g1)">
      <animate attributeName="x" from="-300" to="-900" dur="8s" repeatCount="indefinite"/>
    </rect>
    <rect x="-800" y="120" width="1600" height="30" rx="20" fill="url(#g1)" opacity="0.6">
      <animate attributeName="x" from="-800" to="-1600" dur="10s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- matrix of subtle nodes -->
  <g id="nodes" opacity="0.9">
    <!-- generate several animated circles to resemble a neural-net -->
    <g transform="translate(80,40)">
      <circle cx="0" cy="0" r="3" fill="#00fff0">
        <animate attributeName="r" values="2;4;2" dur="4s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.3;1;0.3" dur="3.6s" repeatCount="indefinite"/>
      </circle>
      <circle cx="120" cy="20" r="2.5" fill="#9b59ff">
        <animate attributeName="cx" values="120;130;120" dur="5s" repeatCount="indefinite"/>
      </circle>
      <circle cx="240" cy="10" r="3" fill="#ff007a">
        <animate attributeName="cy" values="10;18;10" dur="6s" repeatCount="indefinite"/>
      </circle>
      <circle cx="360" cy="30" r="2.5" fill="#00d2ff">
        <animate attributeName="r" values="2;4;2" dur="3.8s" repeatCount="indefinite"/>
      </circle>
    </g>
  </g>

  <!-- abstract circuit lines -->
  <g stroke-width="2" stroke-linecap="round" stroke-linejoin="round" fill="none" stroke="url(#pathGrad)">
    <path d="M 60 180 C 200 120, 320 40, 460 80 S 740 200, 920 160" stroke-opacity="0.15"/>
    <path d="M 40 150 C 180 100, 340 60, 500 110 S 780 220, 940 180" stroke-opacity="0.08"/>
  </g>

  <!-- animated AI hexagon + nodes cluster (left) -->
  <g transform="translate(40,40)">
    <g id="hex" transform="scale(1)">
      <polygon points="0,48 28,12 84,12 112,48 84,84 28,84" transform="translate(40,20)" fill="none" stroke="url(#g1)" stroke-width="3" stroke-linejoin="round">
        <animateTransform attributeName="transform" attributeType="XML" type="rotate" from="0 84 48" to="360 84 48" dur="18s" repeatCount="indefinite"/>
      </polygon>
      <!-- inner nodes -->
      <circle cx="84" cy="48" r="6" fill="#fff" opacity="0.95"/>
      <circle cx="60" cy="30" r="3" fill="#00fff0">
        <animate attributeName="r" values="2;5;2" dur="3s" repeatCount="indefinite"/>
      </circle>
      <circle cx="108" cy="30" r="3" fill="#9b59ff">
        <animate attributeName="r" values="2;5;2" dur="3.6s" repeatCount="indefinite"/>
      </circle>
    </g>
  </g>

  <!-- Name text (center) -->
  <g transform="translate(220,120)">
    <text id="name" x="0" y="0" font-family="Inter, Helvetica, Arial, sans-serif" font-size="36" font-weight="700" fill="url(#g1)">
      Mariam Yasir
    </text>
    <text x="0" y="36" font-family="Inter, Helvetica, Arial, sans-serif" font-size="16" fill="#b8c6d9" opacity="0.9">
      AI Engineer • Computer Vision • Embedded AI
    </text>
  </g>

  <!-- code-like floating tokens on the right -->
  <g transform="translate(640,40)" opacity="0.9">
    <rect x="0" y="0" width="240" height="160" rx="8" fill="rgba(255,255,255,0.02)" stroke="rgba(255,255,255,0.03)"/>
    <g font-family="monospace" font-size="12" fill="#cde9ff">
      <text x="16" y="28">&lt;model&gt; ResNet50</text>
      <text x="16" y="48">&lt;framework&gt; PyTorch</text>
      <text x="16" y="68">&lt;device&gt; Raspberry Pi 4</text>
      <text x="16" y="88">&lt;task&gt; FaceRec • Detection</text>
      <text x="16" y="108">&lt;status&gt; Deploying…</text>
    </g>
    <!-- small moving cursor line -->
    <rect x="16" y="112" width="8" height="2" fill="#00fff0">
      <animate attributeName="x" values="16;24;16" dur="0.8s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- subtle overlay texture -->
  <rect width="100%" height="100%" fill="url(#dots)" opacity="0.6"/>

  <!-- small floating particles (to add life) -->
  <g>
    <circle cx="780" cy="30" r="2" fill="#00fff0" opacity="0.9">
      <animate attributeName="cy" values="30;18;30" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="860" cy="60" r="2.5" fill="#ff007a" opacity="0.9">
      <animate attributeName="cy" values="60;72;60" dur="5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="720" cy="110" r="2" fill="#6a00ff" opacity="0.8">
      <animate attributeName="cy" values="110;98;110" dur="6s" repeatCount="indefinite"/>
    </circle>
  </g>

</svg>

  </div>
</body>
</html>

<!---
mariamyasir74/mariamyasir74 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
