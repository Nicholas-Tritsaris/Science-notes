---
created: 2025-12-18T14:45:08+11:00
modified: 2025-12-18T14:45:24+11:00
---

# guestbook.html

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Guestbook</title>
</head>
<body>
<h1>Guestbook</h1>
<input id="name" placeholder="Name"><br>
<textarea id="msg" placeholder="Message"></textarea><br>
<button onclick="save()">Sign</button>
<ul id="entries"></ul>
<script>
const list=document.getElementById('entries');
function load(){
    list.innerHTML='';
    (JSON.parse(localStorage.gb||'[]')).forEach(e=>{
        let li=document.createElement('li');
        li.textContent=`${e.n}: ${e.m}`;
        list.appendChild(li)
    })
}
function save(){
    let g=JSON.parse(localStorage.gb||'[]');
    g.push({n:name.value,m:msg.value});
    localStorage.gb=JSON.stringify(g);
    load()
}
load();
</script>
</body>
</html>
