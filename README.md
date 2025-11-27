<!--
  README.md for github.com/gauravgupta364
  Single file — inline animated SVGs (hero + live card) — no extra folders
  Paste this entire file as README.md in your profile repo.
-->

<p align="center">
  <!-- Inline animated hero SVG (neon, float, glow) -->
  <svg xmlns="http://www.w3.org/2000/svg" width="100%" viewBox="0 0 1100 300" preserveAspectRatio="xMidYMid slice" role="img" aria-label="Gaurav Gupta - Frontend Developer">
    <defs>
      <linearGradient id="g" x1="0" x2="1">
        <stop offset="0" stop-color="#00E5FF"/>
        <stop offset="0.45" stop-color="#9B7BFF"/>
        <stop offset="1" stop-color="#FF4DFF"/>
      </linearGradient>

      <filter id="blur" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="6" result="b"/>
        <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
      </filter>

      <pattern id="grain" width="12" height="12" patternUnits="userSpaceOnUse">
        <rect width="12" height="12" fill="#000"/>
        <path d="M0 0 L12 12 M12 0 L0 12" stroke="#00000010" stroke-width="0.6"/>
      </pattern>

      <style><![CDATA[
        .bg { fill: #071028; }
        .panel { fill:#041225; stroke: rgba(255,255,255,0.02); rx:14; ry:14; }
        .title { font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; font-weight:800; font-size:46px; fill: url(#g); filter: url(#blur); letter-spacing: -1px; }
        .sub { font-family: Inter, system-ui; font-size:15px; fill:#bcdff6; opacity:0.95; }
        .meta { font-family: Inter, system-ui; font-size:12px; fill:#9fbfe8; opacity:0.95; }
        .dot { filter: url(#blur); }
        @keyframes floatA { 0% { transform: translateY(0);} 50% { transform: translateY(-8px);} 100% { transform: translateY(0);} }
        @keyframes floatB { 0% { transform: translateY(0);} 50% { transform: translateY(-5px);} 100% { transform: translateY(0);} }
      ]]></style>
    </defs>

    <!-- Background -->
    <rect class="bg" width="1100" height="300"/>
    <rect width="1100" height="300" fill="url(#grain)" opacity="0.02"/>

    <!-- Left floating info card -->
    <g transform="translate(40,36)" style="animation: floatA 5s ease-in-out infinite;">
      <rect class="panel" x="0" y="0" width="520" height="210" rx="14" ry="14"/>
      <rect x="8" y="8" width="504" height="194" rx="10" ry="10" fill="none" stroke="url(#g)" stroke-width="1.6" opacity="0.9"/>
      <g transform="translate(28,32)">
        <text class="title">Gaurav Gupta</text>
        <text y="62" class="sub">Frontend Engineer · React • TypeScript • Motion & 3D</text>
        <text y="96" class="meta">Building performant, delightful interfaces — GSAP • Three.js • Framer Motion</text>

        <!-- small skill badges (SVG text badges) -->
        <g transform="translate(0,120)">
          <rect x="0" y="0" rx="6" ry="6" width="110" height="28" fill="#07172a" stroke="rgba(255,255,255,0.02)"/>
          <text x="14" y="19" font-family="Inter, system-ui" font-size="12" fill="#d6f7ff">React</text>

          <rect x="128" y="0" rx="6" ry="6" width="140" height="28" fill="#07172a" stroke="rgba(255,255,255,0.02)"/>
          <text x="142" y="19" font-family="Inter, system-ui" font-size="12" fill="#d6f7ff">TypeScript • Tailwind</text>

          <rect x="280" y="0" rx="6" ry="6" width="120" height="28" fill="#07172a" stroke="rgba(255,255,255,0.02)"/>
          <text x="294" y="19" font-family="Inter, system-ui" font-size="12" fill="#d6f7ff">Three.js</text>
        </g>
      </g>
    </g>

    <!-- Right floating neon panels -->
    <g transform="translate(620,28)" style="animation: floatB 4.2s ease-in-out infinite;">
      <!-- panel 1 -->
      <g transform="translate(0,0)">
        <rect x="0" y="0" width="420" height="80" rx="12" ry="12" fill="#041225" stroke="rgba(255,255,255,0.02)"/>
        <rect x="6" y="6" width="408" height="68" rx="8" ry="8" fill="none" stroke="url(#g)" stroke-width="1.2" opacity="0.95"/>
        <g transform="translate(18,20)">
          <text font-family="Inter, system-ui" font-size="13" fill="#e8fbff" font-weight="700">Featured</text>
          <text x="0" y="24" font-family="Inter, system-ui" font-size="12" fill="#9fbfe8">gauravbits.in — neon portfolio · 3D hero · perf optimized</text>
        </g>
      </g>

      <!-- animated dots grid -->
      <g transform="translate(12,98)">
        <g>
          <circle class="dot" cx="52" cy="24" r="6" fill="#00E5FF" opacity="0.95">
            <animate attributeName="cy" dur="3.8s" values="24;10;24" repeatCount="indefinite" />
          </circle>
          <circle class="dot" cx="140" cy="20" r="5" fill="#FF4DFF" opacity="0.92">
            <animate attributeName="cy" dur="4.6s" values="20;2;20" repeatCount="indefinite" begin="0.6s" />
          </circle>
          <circle class="dot" cx="220" cy="26" r="4.2" fill="#9B7BFF" opacity="0.9">
            <animate attributeName="cy" dur="5.2s" values="26;12;26" repeatCount="indefinite" begin="0.9s" />
          </circle>
        </g>
      </g>
    </g>

    <!-- glowing underline animated -->
    <g transform="translate(40,260)">
      <rect x="0" y="0" width="1020" height="8" rx="6" ry="6" fill="url(#g)" opacity="0.07">
        <animate attributeName="opacity" values="0.05;0.12;0.05" dur="4s" repeatCount="indefinite"/>
      </rect>
    </g>

    <!-- corner emblem -->
    <g transform="translate(980,18)">
      <rect x="0" y="0" width="100" height="80" rx="12" ry="12" fill="#071028" stroke="url(#g)" stroke-width="1.2" opacity="0.95"/>
      <g transform="translate(14,10)">
        <path d="M10 36 L26 18 L46 36 L26 54 Z" fill="url(#g)" filter="url(#blur)"/>
      </g>
    </g>
  </svg>
</p>

<br/>

<h1 align="center" style="margin-top:6px">Gaurav Gupta — <span style="color:#00E5FF">Frontend Engineer</span></h1>
<p align="center">React · TypeScript · Tailwind · Motion & 3D · Creator</p>

---

<!-- Now-building inline animated SVG card -->
<p>
  <svg xmlns="http://www.w3.org/2000/svg" width="420" height="120" viewBox="0 0 420 120" preserveAspectRatio="xMidYMid meet" role="img" aria-label="Now building">
    <defs>
      <linearGradient id="cg" x1="0" x2="1">
        <stop offset="0" stop-color="#00E5FF"/>
        <stop offset="1" stop-color="#9B7BFF"/>
      </linearGradient>
      <filter id="s" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="4" result="bb"/>
        <feMerge><feMergeNode in="bb"/><feMergeNode in="SourceGraphic"/></feMerge>
      </filter>
      <style><![CDATA[
        .card-bg { fill:#051428; stroke: rgba(255,255,255,0.02); rx:12; ry:12; }
        .card-title { font-family: Inter, system-ui; font-size:13px; font-weight:700; fill:#e8fbff; }
        .card-sub { font-family: Inter, system-ui; font-size:12px; fill:#bcdff6; opacity:0.95; }
        .pulse { animation: pulse 1.6s ease-in-out infinite; transform-origin:center; }
        @keyframes pulse { 0% { transform: scale(1);} 50% { transform: scale(1.06);} 100% { transform: scale(1);} }
        .marq { animation: marq 9s linear infinite; white-space: nowrap; }
        @keyframes marq { 0% { transform: translateX(0%);} 100% { transform: translateX(-50%);} }
      ]]></style>
    </defs>

    <rect x="0" y="0" width="420" height="120" rx="14" fill="#051428"/>
    <rect x="8" y="8" width="404" height="104" rx="10" fill="none" stroke="rgba(255,255,255,0.02)"/>

    <g transform="translate(18,18)">
      <circle cx="18" cy="18" r="14" fill="url(#cg)" filter="url(#s)" class="pulse"/>
      <g transform="translate(48,4)">
        <text class="card-title">Now — Building</text>
        <text y="26" class="card-sub">Neon portfolio UI · GSAP · 3D WebGL experiments</text>
      </g>
    </g>

    <g transform="translate(18,72)">
      <rect x="0" y="0" width="384" height="30" rx="8" fill="#06102a" stroke="rgba(255,255,255,0.02)"/>
      <g transform="translate(12,6)">
        <foreignObject width="360" height="20">
          <div xmlns="http://www.w3.org/1999/xhtml" style="font-family:Inter, system-ui; font-size:12px; color:#bcdff6; overflow:hidden;">
            <div style="display:inline-block; padding-right:40px; white-space:nowrap; animation:marq 9s linear infinite;">
              Live: optimizing bundle + buttery motion • designing 3D hero • micro-interactions & perf
            </div>
            <div style="display:inline-block; padding-left:24px; white-space:nowrap; opacity:0.9;">
              Live: optimizing bundle + buttery motion • designing 3D hero • micro-interactions & perf
            </div>
          </div>
        </foreignObject>
      </g>
    </g>
  </svg>
</p>

---

## 🔭 About
I design and build high-fidelity frontend experiences — animation-first, performance-aware, and obsessively polished.  
Creator of tutorials & projects focused on real-world engineering: Java + DSA + modern frontend.

---

## 🛠 Tech snapshot
`React` · `Next.js` · `TypeScript` · `Tailwind CSS` · `GSAP` · `Framer Motion` · `Three.js` · `FastAPI`

---

## 📁 Featured projects
- **gauravbits.in** — neon portfolio, 3D hero, particle system, GSAP micro-interactions.  
- **gym-membership** — dashboard + payments + role-based UX.  
- **legal-doc-simplifier** — NLP summarizer for legal text.  
- **finance-tracker** — analytics-first personal finance app.

---

## 📫 Contact & socials
<p align="center">
  <a href="https://gauravbits.in" style="text-decoration:none">🔗 Portfolio</a> •
  <a href="https://www.instagram.com/gauravbits/" style="text-decoration:none">📷 Instagram</a> •
  <a href="https://x.com/gauravbuilds" style="text-decoration:none">🐦 X</a> •
  <a href="https://www.linkedin.com/in/gaurav-gupta-4179671b0/" style="text-decoration:none">💼 LinkedIn</a> •
  <a href="mailto:contactgaurav8@gmail.com" style="text-decoration:none">✉️ contactgaurav8@gmail.com</a> •
  <a href="https://github.com/gauravgupta364" style="text-decoration:none">💻 GitHub</a>
</p>

---

## 📈 GitHub stats
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=gauravgupta364&show_icons=true&theme=react&hide_border=true" height="140"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=gauravgupta364&theme=react&hide_border=true" height="140"/>
</p>

---

<p align="center" style="opacity:0.8; font-size:12px">
  Built for speed, crafted for delight • Made by <strong>Gaurav Gupta</strong>
</p>
