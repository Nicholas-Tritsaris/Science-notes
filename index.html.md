---
created: 2025-12-18T14:37:09+11:00
modified: 2025-12-18T14:37:20+11:00
---

# index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Nicholas Tritsaris – Science Notes</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      font-family: Tahoma, Verdana, Arial, sans-serif;
      background: radial-gradient(circle at top, #001a33, #000);
      color: #e0f2ff;
    }

    /* ===== 2000s-style layout ===== */
    .header {
      background: linear-gradient(#003366, #001f3f);
      border-bottom: 3px solid #00ccff;
      padding: 15px;
      text-align: center;
    }

    .header h1 {
      margin: 0;
      font-size: 28px;
      letter-spacing: 2px;
      text-shadow: 0 0 8px #00ccff;
    }

    .header p {
      margin: 6px 0 0;
      font-size: 13px;
      color: #9fdfff;
    }

    .container {
      display: grid;
      grid-template-columns: 220px 1fr 220px;
      gap: 10px;
      padding: 10px;
    }

    .sidebar {
      background: rgba(0, 51, 102, 0.85);
      border: 2px ridge #00ccff;
      padding: 10px;
    }

    .sidebar h2 {
      font-size: 14px;
      margin-top: 0;
      border-bottom: 1px dashed #00ccff;
      padding-bottom: 4px;
    }

    .main {
      background: rgba(0, 20, 40, 0.9);
      border: 2px ridge #00ccff;
      padding: 15px;
      min-height: 500px;
    }

    /* ===== DNA animation ===== */
    .dna {
      height: 120px;
      position: relative;
      margin-bottom: 15px;
      overflow: hidden;
    }

    .strand {
      position: absolute;
      width: 4px;
      height: 100%;
      background: #00ccff;
      animation: spin 6s linear infinite;
    }

    .strand:nth-child(2) {
      left: 50px;
      background: #66ffcc;
      animation-delay: -3s;
    }

    @keyframes spin {
      0% { transform: rotate(0deg) translateY(0); }
      100% { transform: rotate(360deg) translateY(0); }
    }

    /* ===== Periodic table ===== */
    .ptable {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 6px;
      margin-top: 10px;
    }

    .element {
      background: linear-gradient(#003366, #001a33);
      border: 1px solid #00ccff;
      text-align: center;
      font-size: 11px;
      padding: 6px 2px;
      cursor: pointer;
      box-shadow: inset 0 0 6px #00ccff;
    }

    .element:hover {
      background: #005599;
    }

    /* ===== Badges ===== */
    .badges img {
      margin: 4px;
      image-rendering: pixelated;
    }

    footer {
      text-align: center;
      font-size: 11px;
      padding: 10px;
      color: #88ccff;
      border-top: 2px solid #00ccff;
      background: #001a33;
    }

    a { color: #66ddff; text-decoration: none; }
    a:hover { text-decoration: underline; }
  </style>
</head>
<body>

  <div class="header">
    <h1>SCIENCE NOTES ARCHIVE</h1>
    <p>Nicholas Tritsaris • Experiments • References • Retro Web</p>
  </div>

  <div class="container">

    <!-- LEFT SIDEBAR -->
    <div class="sidebar">
      <h2>Navigation</h2>
      <ul>
        <li><a href="#chem">Chemistry</a></li>
        <li><a href="#phys">Physics</a></li>
        <li><a href="#bio">Biology</a></li>
        <li><a href="#space">Astronomy</a></li>
        <li><a href="#refs">References</a></li>
      </ul>

      <h2>Web Badges</h2>
      <div class="badges">
        <!-- Classic-style science & web badges -->
        <img src="https://img.shields.io/badge/SCIENCE-FACTS-blue" />
        <img src="https://img.shields.io/badge/CHEMISTRY-LAB-green" />
        <img src="https://img.shields.io/badge/PHYSICS-ENERGY-purple" />
        <img src="https://img.shields.io/badge/BIOLOGY-DNA-teal" />
        <img src="https://img.shields.io/badge/ASTRONOMY-STARS-black" />
        <img src="https://img.shields.io/badge/GITHUB-PAGES-orange" />
        <img src="https://img.shields.io/badge/HTML-4.01-red" />
      </div>
    </div>

    <!-- MAIN CONTENT -->
    <div class="main">

      <div class="dna">
        <div class="strand"></div>
        <div class="strand"></div>
      </div>

      <h2 id="chem">Interactive Periodic Table</h2>
      <p>Click an element to jump to a subject area or notes page.</p>

      <div class="ptable">
        <div class="element" onclick="location.href='#chem'">H<br>1</div>
        <div class="element" onclick="location.href='#phys'">He<br>2</div>
        <div class="element" onclick="location.href='#bio'">C<br>6</div>
        <div class="element" onclick="location.href='#chem'">O<br>8</div>
        <div class="element" onclick="location.href='#phys'">Fe<br>26</div>
        <div class="element" onclick="location.href='#space'">U<br>92</div>
      </div>

      <hr />

      <h2 id="phys">Physics</h2>
      <p>Motion, electricity, magnetism, waves, nuclear physics, and experiments.</p>

      <h2 id="bio">Biology</h2>
      <p>DNA, cells, genetics, microbiology, and human systems.</p>

      <h2 id="space">Astronomy</h2>
      <p>Stars, planets, cosmology, telescopes, and space missions.</p>

      <h2 id="refs">References & Links</h2>
      <ul>
        <li><a href="https://www.nasa.gov" target="_blank">NASA</a></li>
        <li><a href="https://www.noaa.gov" target="_blank">NOAA</a></li>
        <li><a href="https://pubchem.ncbi.nlm.nih.gov" target="_blank">PubChem</a></li>
        <li><a href="https://www.khanacademy.org/science" target="_blank">Khan Academy Science</a></li>
      </ul>

    </div>

    <!-- RIGHT SIDEBAR -->
    <div class="sidebar">
      <h2>Status</h2>
      <p>🧪 Actively maintained</p>
      <p>📚 Growing archive</p>

      <h2>Retro Extras</h2>
      <ul>
        <li>CRT-style UI</li>
        <li>Animated DNA</li>
        <li>Clickable elements</li>
        <li>Classic badges</li>
      </ul>
    </div>

  </div>

  <footer>
    © 2025 Nicholas Tritsaris • Hosted on GitHub Pages
  </footer>

</body>
</html>
