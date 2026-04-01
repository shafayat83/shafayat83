<svg width="854" height="200" viewBox="0 0 854 200" fill="none" xmlns="http://www.w3.org/2000/svg">
<defs>
  <style>
    @keyframes twinkle {
      0%,100% { opacity:0.15; }
      50%      { opacity:1; }
    }
    @keyframes float {
      0%,100% { transform:translateY(0px); }
      50%      { transform:translateY(-7px); }
    }
    @keyframes pulse {
      0%,100% { opacity:1; }
      50%      { opacity:0.72; }
    }
    @keyframes blink {
      0%,49%  { opacity:1; }
      50%,100%{ opacity:0; }
    }
    @keyframes particle {
      0%,100%{ transform:translateY(0) rotate(0deg); opacity:0.45; }
      50%    { transform:translateY(-12px) rotate(8deg); opacity:0.9; }
    }
    @keyframes scanline {
      0%  { transform:translateY(0);   opacity:0.55; }
      100%{ transform:translateY(24px);opacity:0; }
    }
    @keyframes eyeglow {
      0%,100%{ opacity:1; }
      50%    { opacity:0.35; }
    }
    @keyframes linerun {
      0%  { stroke-dashoffset:400; }
      100%{ stroke-dashoffset:0; }
    }
    .t1{ animation:twinkle 2.1s ease-in-out infinite 0.0s; }
    .t2{ animation:twinkle 3.0s ease-in-out infinite 0.3s; }
    .t3{ animation:twinkle 2.5s ease-in-out infinite 0.8s; }
    .t4{ animation:twinkle 1.8s ease-in-out infinite 0.5s; }
    .t5{ animation:twinkle 3.2s ease-in-out infinite 1.2s; }
    .t6{ animation:twinkle 2.7s ease-in-out infinite 1.5s; }
    .bot{ animation:float 4s ease-in-out infinite; }
    .nm { animation:pulse 3s ease-in-out infinite; }
    .cur{ animation:blink 1s step-end infinite; }
    .p1 { animation:particle 3.2s ease-in-out infinite 0.0s; }
    .p2 { animation:particle 4.0s ease-in-out infinite 1.0s; }
    .p3 { animation:particle 3.5s ease-in-out infinite 0.5s; }
    .sc { animation:scanline 2s linear infinite; }
    .eg { animation:eyeglow 1.5s ease-in-out infinite; }
    .lr { stroke-dasharray:400; animation:linerun 2s ease-out forwards; }
  </style>

  <!-- Gradients -->
  <linearGradient id="bg" x1="0" y1="0" x2="854" y2="200" gradientUnits="userSpaceOnUse">
    <stop offset="0%"   stop-color="#0a0818"/>
    <stop offset="50%"  stop-color="#07061a"/>
    <stop offset="100%" stop-color="#0a0818"/>
  </linearGradient>
  <linearGradient id="tg" x1="0" y1="0" x2="500" y2="0" gradientUnits="userSpaceOnUse">
    <stop offset="0%"   stop-color="#c084fc"/>
    <stop offset="50%"  stop-color="#e879f9"/>
    <stop offset="100%" stop-color="#818cf8"/>
  </linearGradient>

  <!-- Glow filters -->
  <filter id="gf"  x="-60%" y="-60%" width="220%" height="220%">
    <feGaussianBlur stdDeviation="3.5" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>
  <filter id="gf2" x="-80%" y="-80%" width="260%" height="260%">
    <feGaussianBlur stdDeviation="8" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>
  <filter id="sgf" x="-40%" y="-40%" width="180%" height="180%">
    <feGaussianBlur stdDeviation="1.8" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>

  <!-- Clip for robot screen -->
  <clipPath id="sc-clip">
    <rect x="686" y="130" width="80" height="26"/>
  </clipPath>
</defs>

<!-- ═══════════════ BACKGROUND ═══════════════ -->
<rect width="854" height="200" fill="url(#bg)"/>

<!-- Ambient glow orbs -->
<ellipse cx="170" cy="110" rx="130" ry="70" fill="#7c3aed" opacity="0.04"/>
<ellipse cx="710" cy="95"  rx="110" ry="80" fill="#0ea5e9" opacity="0.04"/>

<!-- ═══════════════ CYBERPUNK GRID FLOOR ═══════════════ -->
<line x1="0" y1="160" x2="854" y2="160" stroke="#7c3aed" stroke-width="0.4" opacity="0.22"/>
<line x1="0" y1="170" x2="854" y2="170" stroke="#7c3aed" stroke-width="0.3" opacity="0.15"/>
<line x1="0" y1="180" x2="854" y2="180" stroke="#7c3aed" stroke-width="0.3" opacity="0.10"/>
<line x1="0" y1="190" x2="854" y2="190" stroke="#7c3aed" stroke-width="0.2" opacity="0.07"/>
<!-- Vanishing lines -->
<line x1="427" y1="210" x2="0"   y2="148" stroke="#7c3aed" stroke-width="0.5" opacity="0.18"/>
<line x1="427" y1="210" x2="180" y2="158" stroke="#7c3aed" stroke-width="0.4" opacity="0.13"/>
<line x1="427" y1="210" x2="320" y2="165" stroke="#7c3aed" stroke-width="0.3" opacity="0.09"/>
<line x1="427" y1="210" x2="534" y2="165" stroke="#7c3aed" stroke-width="0.3" opacity="0.09"/>
<line x1="427" y1="210" x2="674" y2="158" stroke="#7c3aed" stroke-width="0.4" opacity="0.13"/>
<line x1="427" y1="210" x2="854" y2="148" stroke="#7c3aed" stroke-width="0.5" opacity="0.18"/>

<!-- ═══════════════ STARS ═══════════════ -->
<circle cx="22"  cy="17"  r="1.5" fill="#fff"    class="t1"/>
<circle cx="72"  cy="36"  r="1"   fill="#c084fc" class="t2"/>
<circle cx="138" cy="9"   r="1.5" fill="#fff"    class="t3"/>
<circle cx="196" cy="44"  r="1"   fill="#7dd3fc" class="t4"/>
<circle cx="255" cy="20"  r="2"   fill="#fff"    class="t5"/>
<circle cx="328" cy="50"  r="1"   fill="#c084fc" class="t6"/>
<circle cx="392" cy="13"  r="1.5" fill="#fff"    class="t1"/>
<circle cx="452" cy="41"  r="1"   fill="#7dd3fc" class="t2"/>
<circle cx="508" cy="11"  r="1.5" fill="#fff"    class="t4"/>
<circle cx="562" cy="47"  r="1"   fill="#c084fc" class="t5"/>
<circle cx="52"  cy="64"  r="1"   fill="#fff"    class="t3"/>
<circle cx="192" cy="70"  r="1.5" fill="#7dd3fc" class="t6"/>
<circle cx="374" cy="62"  r="1"   fill="#fff"    class="t2"/>
<circle cx="518" cy="72"  r="1"   fill="#c084fc" class="t1"/>

<!-- ═══════════════ FLOATING CODE PARTICLES ═══════════════ -->
<text x="592" y="52"  font-family="'Courier New',monospace" font-size="13" fill="#7c3aed" opacity="0.75" class="p1">&lt;/&gt;</text>
<text x="570" y="90"  font-family="'Courier New',monospace" font-size="12" fill="#00e5ff" opacity="0.65" class="p2">{}</text>
<text x="608" y="120" font-family="'Courier New',monospace" font-size="11" fill="#c084fc" opacity="0.65" class="p3">AI</text>
<text x="548" y="130" font-family="'Courier New',monospace" font-size="10" fill="#7c3aed" opacity="0.5"  class="p1">⚡</text>

<!-- ═══════════════ LEFT ACCENT ═══════════════ -->
<rect x="27" y="31" width="6" height="6" fill="#00e5ff" opacity="0.9" rx="1"/>
<line x1="30" y1="37" x2="30" y2="152" stroke="#7c3aed" stroke-width="2"   opacity="0.55"/>
<line x1="30" y1="37" x2="30" y2="82"  stroke="#00e5ff" stroke-width="2"   opacity="0.4" class="lr"/>
<rect x="27" y="152" width="6" height="6" fill="#7c3aed" opacity="0.7" rx="1"/>

<!-- ═══════════════ TEXT ═══════════════ -->
<!-- Greeting -->
<text x="47" y="56"
      font-family="'Courier New',Courier,monospace"
      font-size="12" fill="#00e5ff" letter-spacing="3" opacity="0.9">
  &lt; Hello World! /&gt;
</text>

<!-- Main name with glow -->
<text x="44" y="107"
      font-family="Arial,'Arial Black',Helvetica,sans-serif"
      font-size="52" font-weight="900"
      fill="url(#tg)" filter="url(#gf2)"
      class="nm">Shafayat Alam</text>

<!-- Blinking cursor -->
<text x="458" y="107"
      font-family="'Courier New',monospace"
      font-size="52" font-weight="900"
      fill="#c084fc" class="cur">_</text>

<!-- Subtitle -->
<text x="47" y="132"
      font-family="'Courier New',Courier,monospace"
      font-size="13" letter-spacing="1.5" fill="#94a3b8">
  &#x1F916; AI Builder &nbsp;&#183;&nbsp; &#x1F3A8; UI Designer &nbsp;&#183;&nbsp; &#x1F50D; SEO Expert
</text>

<!-- Divider - double line -->
<line x1="47"  y1="139" x2="536" y2="139" stroke="#7c3aed" stroke-width="1"   opacity="0.45"/>
<line x1="47"  y1="140" x2="180" y2="140" stroke="#00e5ff" stroke-width="1.5" opacity="0.55" class="lr"/>

<!-- Location -->
<text x="47" y="158"
      font-family="'Courier New',Courier,monospace"
      font-size="11.5" fill="#64748b" letter-spacing="0.3">
  &#x1F4CD; Bangladesh &nbsp;&#183;&nbsp; Building with AI &#x1F680; &nbsp;&#183;&nbsp; Open to Collab &#x2728;
</text>

<!-- ═══════════════════════════════════════ -->
<!-- PIXEL ART ROBOT  (bx=662, by=12, px=8) -->
<!-- col c → x = 662 + c*8                  -->
<!-- row r → y = 12  + r*8                  -->
<!-- ═══════════════════════════════════════ -->
<g class="bot">

  <!-- Shadow beneath robot -->
  <ellipse cx="726" cy="196" rx="62" ry="5" fill="#7c3aed" opacity="0.12"/>

  <!-- ── ANTENNA ── -->
  <!-- Left stem: cols 4-5, row 0 → x=694,y=12,w=16,h=8 -->
  <rect x="694" y="12" width="16" height="8"  fill="#4c1d95"/>
  <!-- Left tip: row 1 → y=20 -->
  <rect x="694" y="20" width="16" height="8"  fill="#00e5ff" filter="url(#sgf)" class="eg"/>
  <!-- Right stem: cols 10-11 → x=742 -->
  <rect x="742" y="12" width="16" height="8"  fill="#4c1d95"/>
  <!-- Right tip -->
  <rect x="742" y="20" width="16" height="8"  fill="#00e5ff" filter="url(#sgf)" class="eg"/>

  <!-- ── HEAD ── -->
  <!-- row 2: cols 2-13 → x=678,w=96 -->
  <rect x="678" y="28" width="96"  height="8"  fill="#6d28d9" rx="2"/>
  <!-- row 3: cols 1-14 → x=670,w=112 -->
  <rect x="670" y="36" width="112" height="8"  fill="#7c3aed"/>
  <!-- row 4: full 0-15 → x=662,w=128 -->
  <rect x="662" y="44" width="128" height="8"  fill="#7c3aed"/>

  <!-- ── EYES rows 5-6 (h=16) ──
       Pattern: PP·CC·PPPP·CC·PP
       cols 0-1 P | col2 gap | cols 3-4 C | col5 gap
             | cols 6-9 P | col10 gap | cols 11-12 C | col13 gap | cols 14-15 P -->
  <rect x="662" y="50" width="16" height="16" fill="#7c3aed"/>
  <!-- left eye glow bg -->
  <rect x="682" y="48" width="20" height="20" fill="#00e5ff" opacity="0.10" filter="url(#sgf)"/>
  <!-- left eye -->
  <rect x="686" y="50" width="16" height="16" fill="#00e5ff" filter="url(#sgf)" class="eg"/>
  <rect x="710" y="50" width="32" height="16" fill="#7c3aed"/>
  <!-- right eye glow bg -->
  <rect x="746" y="48" width="20" height="20" fill="#00e5ff" opacity="0.10" filter="url(#sgf)"/>
  <!-- right eye -->
  <rect x="750" y="50" width="16" height="16" fill="#00e5ff" filter="url(#sgf)" class="eg"/>
  <rect x="774" y="50" width="16" height="16" fill="#7c3aed"/>

  <!-- row 7: full solid -->
  <rect x="662" y="66" width="128" height="8"  fill="#7c3aed"/>

  <!-- ── MOUTH row 8 ──
       PPP·DDDDDDDD·PPP
       cols 0-2 P | col3 gap | cols 4-11 D | col12 gap | cols 13-15 P -->
  <rect x="662" y="74" width="24"  height="8"  fill="#7c3aed"/>
  <rect x="694" y="74" width="64"  height="8"  fill="#1e0a40"/>
  <!-- teeth -->
  <rect x="700" y="76" width="6"   height="4"  fill="#00e5ff" opacity="0.6"/>
  <rect x="714" y="76" width="6"   height="4"  fill="#00e5ff" opacity="0.6"/>
  <rect x="728" y="76" width="6"   height="4"  fill="#00e5ff" opacity="0.6"/>
  <rect x="742" y="76" width="6"   height="4"  fill="#00e5ff" opacity="0.6"/>
  <rect x="766" y="74" width="24"  height="8"  fill="#7c3aed"/>

  <!-- ── HEAD BOTTOM ── -->
  <!-- row 9: cols 1-14 → x=670,w=112 -->
  <rect x="670" y="82" width="112" height="8"  fill="#7c3aed"/>
  <!-- row 10: cols 2-13 → x=678,w=96 -->
  <rect x="678" y="90" width="96"  height="8"  fill="#6d28d9" rx="1"/>

  <!-- ── NECK rows 11-12 (h=16) ── cols 4-11 → x=694,w=64 -->
  <rect x="694" y="98" width="64"  height="16" fill="#5b21b6"/>

  <!-- ── SHOULDERS row 13 ── cols 2-13 → x=678,w=96 -->
  <rect x="678" y="114" width="96"  height="8"  fill="#7c3aed"/>

  <!-- ── BODY row 14 ── full -->
  <rect x="662" y="122" width="128" height="8"  fill="#7c3aed"/>

  <!-- ── CHEST PANEL rows 15-17 (h=24) ──
       PP·SSSSSSSSSS·PP
       cols 0-1 | col2 gap | cols 3-12 S | col13 gap | cols 14-15 -->
  <rect x="662" y="130" width="16"  height="24" fill="#7c3aed"/>
  <rect x="686" y="130" width="80"  height="24" fill="#0b0926"/>
  <rect x="774" y="130" width="16"  height="24" fill="#7c3aed"/>
  <!-- Screen border -->
  <rect x="686" y="130" width="80"  height="24" fill="none" stroke="#7c3aed" stroke-width="1" opacity="0.45"/>

  <!-- Code pixels on screen row 15 (y=130) -->
  <rect x="694" y="133" width="8"  height="5" fill="#00e5ff" opacity="0.9"/>
  <rect x="710" y="133" width="16" height="5" fill="#a78bfa" opacity="0.9"/>
  <rect x="734" y="133" width="8"  height="5" fill="#f472b6" opacity="0.9"/>
  <rect x="750" y="133" width="8"  height="5" fill="#00e5ff" opacity="0.9"/>
  <!-- row 16 (y=140) -->
  <rect x="694" y="141" width="24" height="5" fill="#a78bfa" opacity="0.9"/>
  <rect x="726" y="141" width="8"  height="5" fill="#00e5ff" opacity="0.9"/>
  <rect x="742" y="141" width="16" height="5" fill="#f472b6" opacity="0.9"/>
  <!-- row 17 (y=148) -->
  <rect x="694" y="149" width="8"  height="5" fill="#00e5ff" opacity="0.9"/>
  <rect x="710" y="149" width="24" height="5" fill="#a78bfa" opacity="0.9"/>
  <rect x="750" y="149" width="8"  height="5" fill="#00e5ff" opacity="0.9"/>

  <!-- Scan line on screen -->
  <rect x="686" y="130" width="80" height="3" fill="#00e5ff" opacity="0.4"
        clip-path="url(#sc-clip)" class="sc"/>

  <!-- ── BODY BOTTOM row 18 ── -->
  <rect x="662" y="154" width="128" height="8"  fill="#6d28d9"/>

  <!-- ── ARMS ── -->
  <!-- Left upper: x=646,y=114,w=16,h=24 -->
  <rect x="646" y="114" width="16" height="24" fill="#6d28d9"/>
  <!-- Left lower: x=638,y=138,w=16,h=20 -->
  <rect x="638" y="138" width="16" height="20" fill="#5b21b6"/>
  <!-- Right upper -->
  <rect x="790" y="114" width="16" height="24" fill="#6d28d9"/>
  <!-- Right lower -->
  <rect x="790" y="138" width="16" height="20" fill="#5b21b6"/>

  <!-- ── LEGS rows 19-20 (h=16) ── -->
  <!-- Left leg: cols 4-7 → x=694,w=32 -->
  <rect x="694" y="162" width="32" height="16" fill="#5b21b6"/>
  <!-- Right leg: cols 9-12 → x=734,w=32 -->
  <rect x="734" y="162" width="32" height="16" fill="#5b21b6"/>

  <!-- ── FEET row 21 ── -->
  <!-- Left foot: x=686,w=40 -->
  <rect x="686" y="178" width="40" height="8"  fill="#4c1d95" rx="1"/>
  <rect x="686" y="186" width="40" height="4"  fill="#3b0764" rx="1"/>
  <!-- Right foot: x=734,w=40 -->
  <rect x="734" y="178" width="40" height="8"  fill="#4c1d95" rx="1"/>
  <rect x="734" y="186" width="40" height="4"  fill="#3b0764" rx="1"/>

  <!-- Neon rim highlight (top of head) -->
  <rect x="662" y="44" width="128" height="1" fill="#c084fc" opacity="0.5"/>

</g>

<!-- ═══════════════ BOTTOM ACCENT ═══════════════ -->
<line x1="0"   y1="199" x2="854" y2="199" stroke="#7c3aed" stroke-width="1.5" opacity="0.55"/>
<line x1="0"   y1="198" x2="427" y2="198" stroke="#00e5ff" stroke-width="0.8" opacity="0.28"/>

</svg>
<div align="center">

<!-- ══════════════════════════════════════════════ -->
<!--         CUSTOM PIXEL ART ANIMATED HEADER       -->
<!--  Upload header.svg to your profile repo first  -->
<!-- ══════════════════════════════════════════════ -->

![header](header.svg)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&pause=1200&color=A855F7&center=true&vCenter=true&width=600&lines=Building+Websites+%26+Apps+with+AI+%F0%9F%A4%96;App+UI+Designer+%7C+Keyword+Researcher+%F0%9F%94%8D;Turning+Ideas+into+Usable+Products+%F0%9F%9A%80;Vibe+Coder+from+Bangladesh+%F0%9F%87%A7%F0%9F%87%A9)](https://git.io/typing-svg)

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=shafayat83&style=for-the-badge&color=7c3aed&label=PROFILE+VIEWS)
&nbsp;
[![GitHub followers](https://img.shields.io/github/followers/shafayat83?label=Followers&style=for-the-badge&color=7c3aed&labelColor=1a1a2e)](https://github.com/shafayat83?tab=followers)
&nbsp;
[![Stars](https://img.shields.io/github/stars/shafayat83?label=Total%20Stars&style=for-the-badge&color=7c3aed&labelColor=1a1a2e)](https://github.com/shafayat83)

</div>

---

## 👤 About Me

<img align="right" width="290" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="Coding gif"/>

🏠 &nbsp;Based in **Bangladesh 🇧🇩**, building for the world  
🏢 &nbsp;Working at **Unifix**  
🤖 &nbsp;I create **websites & apps** fully powered by AI  
🎨 &nbsp;Passionate about **App UI Design** using AI tools  
🔍 &nbsp;Expert in **SEO Keyword Research** & content strategy  
💰 &nbsp;Focused on **earning online** through digital products  
🚀 &nbsp;Currently posting **portfolio projects** on GitHub  
🌱 &nbsp;Always learning the **latest AI tools & workflows**  
✨ &nbsp;Motto: ***"Turn any idea into a product with AI."***  

&nbsp;

---

## 🛠️ Skills & Tools

<div align="center">

**🤖 AI Tools**

![ChatGPT](https://img.shields.io/badge/ChatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white)
![Claude](https://img.shields.io/badge/Claude%20AI-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/Copilot-000000?style=for-the-badge&logo=github&logoColor=white)
![Midjourney](https://img.shields.io/badge/Midjourney-000000?style=for-the-badge&logoColor=white)

**💻 Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**🎨 Design & UI**

![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

**🔍 SEO & Research**

![Google Search Console](https://img.shields.io/badge/Search%20Console-458CF5?style=for-the-badge&logo=google&logoColor=white)
![Ahrefs](https://img.shields.io/badge/Ahrefs-FF7043?style=for-the-badge&logoColor=white)
![SEMrush](https://img.shields.io/badge/SEMrush-F96C25?style=for-the-badge&logoColor=white)

**☁️ Deploy & Platforms**

![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

</div>

---

## 📊 GitHub Stats

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=shafayat83&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0d1117&title_color=a855f7&icon_color=a855f7&text_color=ffffff" />
<img width="49%" src="https://github-readme-streak-stats.herokuapp.com/?user=shafayat83&theme=tokyonight&hide_border=true&background=0d1117&ring=a855f7&fire=ff6b35&currStreakLabel=a855f7" />

<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=shafayat83&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a855f7&text_color=ffffff&langs_count=6" />
<img width="49%" src="https://github-readme-activity-graph.vercel.app/graph?username=shafayat83&bg_color=0d1117&color=a855f7&line=7c3aed&point=ffffff&area=true&hide_border=true" />

<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://pixel-profile.vercel.app/api/github-stats?username=shafayat83&screen_effect=true&theme=blue_chill"/>
  <source media="(prefers-color-scheme: light)" srcset="https://pixel-profile.vercel.app/api/github-stats?username=shafayat83&theme=summer"/>
  <img alt="pixel stats" src="https://pixel-profile.vercel.app/api/github-stats?username=shafayat83&screen_effect=true&theme=blue_chill"/>
</picture>

</div>

---

## 🚀 Featured Projects

<div align="center">

| Project | Description | Stack | Link |
|:-------:|:-----------:|:-----:|:----:|
| 🖱️ **Virtual Mouse** | Control your PC with hand gestures via AI vision | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) | [→ View](https://github.com/shafayat83/Virtual-Mouse) |
| 🎙️ **Transcribe OG** | Retro AI transcription for YouTube & Instagram | ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) | [→ View](https://github.com/shafayat83/Transcribe-OG) |
| 📖 **Audiobook** | Text-to-speech audiobook generator | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) | [→ View](https://github.com/shafayat83/Audiobook) |
| 📷 **Snap Camera** | AI-powered camera tool | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) | [→ View](https://github.com/shafayat83/Snap-Cammera) |
| 🖥️ **Screen Capture** | Smart screen capture tool | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) | [→ View](https://github.com/shafayat83/Screen-Capture) |

</div>

---

## 🏆 GitHub Trophies

<div align="center">

[![trophy](https://github-profile-trophy.vercel.app/?username=shafayat83&theme=tokyonight&no-frame=true&row=1&column=7&margin-w=10)](https://github.com/ryo-ma/github-profile-trophy)

</div>

---

## 🌐 Let's Connect

<div align="center">

<a href="https://tinyurl.com/shafayat8"><img src="https://img.shields.io/badge/🌍 Portfolio-Visit%20Now-7c3aed?style=for-the-badge"/></a>
&nbsp;
<a href="https://www.facebook.com/shafayat83"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white"/></a>
&nbsp;
<a href="https://www.instagram.com/shafayat_8/"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/></a>
&nbsp;
<a href="https://github.com/shafayat83"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>

<br/><br/>

> 💬 *"I don't just code — I **vibe** with AI to build products that actually matter."*

<br/>

![footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=24,30,9&height=120&section=footer&animation=twinkling)

**⭐ Star my repos if you find them useful — it keeps me going! ⭐**

</div>
