---
created: 2025-12-18T14:44:49+11:00
modified: 2025-12-18T14:45:07+11:00
---

# element.html

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Element</title>
<style>
body{font-family:Tahoma;background:#000;color:#ccf}
svg{border:2px ridge #00ccff}
</style>
</head>
<body>
<h1 id="name"></h1>
<p id="info"></p>
<svg width="300" height="200">
<circle cx="150" cy="100" r="40" fill="none" stroke="#00ccff" stroke-width="2"/>
<circle cx="150" cy="100" r="70" fill="none" stroke="#66ffcc" stroke-dasharray="5,5"/>
<text x="110" y="105" fill="#00ccff">Electron Shells</text>
</svg>
<script>
const q=new URLSearchParams(location.search);
const el=q.get('el'),num=q.get('num');
document.getElementById('name').innerText=`${el} (Atomic #${num})`;
document.getElementById('info').innerText='Atomic structure, properties, and uses will be documented here.';
</script>
</body>
</html>
