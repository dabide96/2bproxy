<!DOCTYPE html>
<html lang="it" data-theme="dark">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
<title>2B Portal | Genesis OS</title>
<style>
:root {
  --primary: #00c853; --bg: #020617; --card: #0f172a; --text: #f1f5f9;
  --border: #1e293b; --danger: #ff4757; --topbar-h: 75px;
}
[data-theme="light"] {
  --bg: #f8fafc; --card: #ffffff; --text: #0f172a; --border: #e2e8f0;
}
* {
  box-sizing: border-box;
  font-family: 'Plus Jakarta Sans', sans-serif;
  -webkit-tap-highlight-color: transparent;
  outline: none;
}
body {
  margin: 0; background: var(--bg); color: var(--text);
  height: 100dvh; overflow: hidden;
}
/* UI ELEMENTS */
.glass {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 24px;
  box-shadow: 0 20px 40px -15px rgba(0,0,0,0.4);
}
.btn {
  padding: 12px 20px;
  border-radius: 12px;
  border: none;
  cursor: pointer;
  font-weight: 700;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: 0.2s;
  font-size: 14px;
}
.btn:active {
  transform: scale(0.96);
}
.btn-primary {
  background: var(--primary);
  color: white;
}
.btn-danger {
  background: var(--danger);
  color: white;
}
.btn-icon {
  width: 35px;
  height: 35px;
  border-radius: 10px;
  justify-content: center;
  padding: 0;
  font-size: 16px;
  line-height: 0;
  user-select:none;
}
input {
  padding: 14px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: var(--bg);
  color: var(--text);
  font-size: 15px;
}
/* LAYOUT */
.topbar {
  height: var(--topbar-h);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  border-bottom: 1px solid var(--border);
  background: var(--card);
  z-index: 100;
}
.page {
  display: none;
  height: calc(100dvh - var(--topbar-h));
  width: 100%;
  overflow-y: auto;
  padding: 20px;
}
.page.active {
  display: block;
  animation: slideUp 0.3s ease;
}
@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
/* ADMIN HUB */
.adm-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.user-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  border-bottom: 1px solid var(--border);
}
.user-row:last-child {
  border: none;
}
.status-pill {
  padding: 4px 10px;
  border-radius: 20px;
  font-size: 11px;
  font-weight: 800;
  text-transform: uppercase;
}
.online {
  background: rgba(0,200,83,0.2);
  color: var(--primary);
}
.banned {
  background: rgba(255,71,87,0.2);
  color: var(--danger);
}
/* TERMINAL */
.term {
  background: #000;
  color: #00ff41;
  font-family: 'JetBrains Mono', monospace;
  padding: 15px;
  border-radius: 15px;
  height: 180px;
  overflow-y: auto;
  font-size: 12px;
  border: 1px solid #334155;
  line-height: 1.5;
}
/* BROWSER */
#browser-page {
  padding: 0;
  overflow: hidden;
}
iframe {
  width: 100%;
  height: 100%;
  border: none;
}
/* NOTIF */
#notif-container {
  position: fixed;
  top: 90px;
  right: 20px;
  z-index: 2000;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.toast {
  background: var(--primary);
  color: white;
  padding: 15px 25px;
  border-radius: 15px;
  font-weight: 700;
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
  animation: slideIn 0.3s ease;
}
@keyframes slideIn {
  from {
    transform: translateX(100%);
  }
  to {
    transform: translateX(0);
  }
}
</style>
</head>
<body>

<div id="notif-container"></div>

<!-- LOGIN -->
<div id="login-screen" style="position:fixed; inset:0; background:var(--bg); z-index:10000; display:flex; align-items:center; justify-content:center; padding:20px;">
    <div class="glass" style="width:100%; max-width:420px; padding:45px; text-align:center;">
        <h1 style="color:var(--primary); font-size:4rem; margin:0; font-weight:900; letter-spacing:-2px;">2B.</h1>
        <p style="opacity:0.5; font-weight:700; margin-bottom:35px; font-size:13px;">GENESIS PORTAL v5.0</p>
        <div style="display:grid; gap:12px;">
            <input type="text" id="l-u" placeholder="Account Name" autocomplete="username" />
            <input type="password" id="l-p" placeholder="Security Key" autocomplete="current-password" />
            <button class="btn btn-primary" style="justify-content:center; padding:18px;" onclick="kernelAuth()">INIZIALIZZA SESSIONE</button>
        </div>
    </div>
</div>

<!-- APP -->
<div id="main-app" style="display:none; flex-direction:column;">
    <header class="topbar">
        <div style="font-weight:900; font-size:2rem; color:var(--primary); cursor:pointer;" onclick="showPage('browser-page')">2B.</div>
        <div style="flex:1; max-width:550px; display:flex; gap:10px; background:var(--bg); padding:8px; border-radius:16px; border:1px solid var(--border);">
            <input type="text" id="urlInput" placeholder="Cerca su Genesis o inserisci URL..." style="flex:1; border:none; background:transparent; color:var(--text); outline:none;" onkeydown="if(event.key==='Enter') loadUrl()" autocomplete="off" />
            <button class="btn btn-primary" style="padding:10px 18px;" onclick="loadUrl()">NAVIGA</button>
        </div>
        <div style="display:flex; align-items:center; gap:18px; cursor:pointer;" onclick="toggleMenu()">
            <div style="text-align:right">
                <div id="nav-coins" style="font-weight:800; color:var(--primary); font-size:18px;">0$</div>
                <div id="user-role" style="font-size:10px; font-weight:800; opacity:0.5; letter-spacing:1px;">IDENTIFYING...</div>
            </div>
            <div id="avatar" style="width:48px; height:48px; background:var(--primary); border-radius:15px; display:flex; align-items:center; justify-content:center; font-weight:900; color:white; font-size:18px;">?</div>
        </div>
    </header>

    <div id="drop-menu" class="glass" style="position:absolute; top:85px; right:20px; width:280px; z-index:1000; display:none; flex-direction:column; overflow:hidden;">
        <div class="user-row" style="padding:20px; background:var(--bg);"><b id="menu-user-name">User</b><span class="status-pill online">Attivo</span></div>
        <div class="user-row" id="adm-btn" style="display:none; color:var(--primary); cursor:pointer;" onclick="showPage('admin-page')"><b>⚡ MASTER ENGINE</b></div>
        <div class="user-row" style="cursor:pointer;" onclick="toggleTheme()">Cambia Interfaccia</div>
        <div class="user-row" style="color:var(--danger); cursor:pointer; font-weight:800;" onclick="logout()">LOGOUT SISTEMA</div>
    </div>

    <main>
        <div id="browser-page" class="page active"><iframe id="webframe" src="about:blank"></iframe></div>

        <div id="admin-page" class="page">
            <div style="display:flex; justify-content:space-between; align-items:center;">
                <h1>Genesis Control Unit</h1>
                <button class="btn btn-primary" onclick="createNewUser()">+ CREA UTENTE</button>
            </div>

            <div class="adm-grid">
                <div class="glass" style="padding:25px; grid-column: span 2;">
                    <h3 style="margin-top:0;">Database Utenti Locale</h3>
                    <div id="user-list-db"></div>
                </div>

                <div class="glass" style="padding:25px;">
                    <h3 style="margin-top:0;">Global Economy</h3>
                    <div style="display:grid; gap:15px;">
                        <input type="number" id="eco-amount" placeholder="Quantità Monete" min="0" />
                        <button class="btn btn-primary" onclick="setGlobalMoney()">IMPOSTA MONETE A TUTTI</button>
                        <hr style="border:0; border-top:1px solid var(--border); margin:10px 0;" />
                        <button class="btn btn-danger" onclick="resetDatabase()">FORMATTA DATABASE</button>
                    </div>
                </div>
            </div>
            <div class="term" id="kernel-log">[INIT]: Genesis Engine v5 caricato correttamente.<br></div>
        </div>
    </main>
</div>

<script>
let state = JSON.parse(localStorage.getItem('genesis_db')) || {
    users: [
        {id: 1, name: 'admin', pass: 'admin', role: 'ADMIN', balance: 50000, status: 'online'},
        {id: 2, name: 'guest', pass: '1234', role: 'USER', balance: 100, status: 'online'}
    ],
    currentUser: null
};

function save() {
    localStorage.setItem('genesis_db', JSON.stringify(state));
    renderUserList();
}

function kernelAuth() {
    const u = document.getElementById('l-u').value.trim();
    const p = document.getElementById('l-p').value.trim();
    if(!u || !p) {
        alert("Inserisci username e password.");
        return;
    }
    const found = state.users.find(x => x.name.toLowerCase() === u.toLowerCase() && x.pass === p);
    if(found){
        if(found.status === 'banned') {
            alert("ACCESSO NEGATO: Utente Bannato.");
            return;
        }
        state.currentUser = found;
        initUI();
        logKernel(`Accesso eseguito come ${found.name.toUpperCase()}`);
        showToast("Benvenuto nel Sistema Genesis");
    } else {
        alert("Chiave di sicurezza errata.");
    }
}

function initUI() {
    document.getElementById('login-screen').style.display = "none";
    document.getElementById('main-app').style.display = "flex";
    updateUserUI();
    showPage('browser-page');
    document.getElementById('drop-menu').style.display = "none";
    if(state.currentUser.role === 'ADMIN'){
        document.getElementById('adm-btn').style.display = "flex";
    } else {
        document.getElementById('adm-btn').style.display = "none";
    }
    renderUserList();
}

function updateUserUI(){
    const u = state.currentUser;
    document.getElementById('nav-coins').innerText = u.balance.toLocaleString() + "$";
    document.getElementById('user-role').innerText = u.role;
    document.getElementById('avatar').innerText = u.name[0].toUpperCase();
    document.getElementById('menu-user-name').innerText = u.name;
    document.getElementById('webframe').src = "https://www.bing.com";
}

function renderUserList(){
    const container = document.getElementById('user-list-db');
    container.innerHTML = "";
    if(state.users.length === 0){
        container.innerHTML = "<p style='opacity:0.5;'>Nessun utente registrato.</p>";
        return;
    }
    state.users.forEach(u => {
        container.innerHTML += `
            <div class="user-row">
                <div>
                    <b>${u.name}</b> <span style="font-size:10px; opacity:0.5;">ID:${u.id}</span><br>
                    <span class="status-pill ${u.status === 'online' ? 'online' : 'banned'}">${u.status}</span>
                    <span style="font-size:12px; margin-left:10px;">${u.balance.toLocaleString()}$</span>
                </div>
                <div style="display:flex; gap:5px;">
                    <button class="btn btn-icon" title="Modifica bilancio" onclick="editUserMoney(${u.id})">💰</button>
                    <button class="btn btn-icon btn-danger" title="Toggle ban" onclick="toggleBan(${u.id})">🚫</button>
                    ${u.name !== 'admin' ? `<button class="btn btn-icon btn-danger" title="Elimina utente" onclick="deleteUser(${u.id})">🗑️</button>` : ''}
                </div>
            </div>`;
    });
}

// ADMIN ACTIONS
function createNewUser(){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    const name = prompt("Nome nuovo utente:");
    if(!name || !name.trim()){
        alert("Nome non valido.");
        return;
    }
    if(state.users.some(u=>u.name.toLowerCase() === name.toLowerCase())){
        alert("Nome utente già esistente.");
        return;
    }
    const newUser = {id: Date.now(), name: name.trim(), pass: '1234', role:'USER', balance:100, status:'online'};
    state.users.push(newUser);
    save();
    logKernel(`Creato utente: ${name.trim()}`);
    showToast(`Utente '${name.trim()}' creato con password di default.`);
}

function toggleBan(id){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    const u = state.users.find(x => x.id === id);
    if(!u) return;
    if(u.name === 'admin') { alert("Non puoi bannare admin."); return;}
    u.status = u.status === 'online' ? 'banned' : 'online';
    save();
    logKernel(`Stato ${u.name} modificato in ${u.status}`);
}

function deleteUser(id){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    const u = state.users.find(x => x.id === id);
    if(!u) return;
    if(u.name === 'admin') { alert("Non puoi eliminare admin."); return; }
    if(confirm(`Eliminare definitivamente l'utente '${u.name}'?`)){
        state.users = state.users.filter(x => x.id !== id);
        if(state.currentUser.id === id) logout();
        save();
        logKernel(`Utente '${u.name}' rimosso dal database.`);
        showToast(`Utente '${u.name}' eliminato.`);
    }
}

function editUserMoney(id){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    const u = state.users.find(x => x.id === id);
    if(!u) return;
    const amount = prompt(`Inserisci nuovo bilancio per ${u.name}:`, u.balance);
    if(amount === null) return;
    const n = parseInt(amount);
    if(isNaN(n) || n < 0){ alert("Valore non valido."); return; }
    u.balance = n;
    if(state.currentUser.id === id) updateUserUI();
    save();
    logKernel(`Bilancio di ${u.name} aggiornato a ${n}$`);
    showToast(`Bilancio di ${u.name} aggiornato.`);
}

function setGlobalMoney(){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    const val = document.getElementById('eco-amount').value;
    if(!val) return alert("Inserisci un valore valido.");
    const n = parseInt(val);
    if(isNaN(n) || n < 0) return alert("Valore non valido.");
    state.users.forEach(u => u.balance = n);
    save();
    updateUserUI();
    logKernel(`Economia globale impostata a ${n} per tutti gli utenti.`);
    showToast("Economia sincronizzata per tutti gli utenti.");
    document.getElementById('eco-amount').value = '';
}

// UTILS
function loadUrl(){
    const val = document.getElementById('urlInput').value.trim();
    if(!val) return;
    let url;
    if(val.includes('.')){
        url = val.startsWith('http') ? val : 'https://' + val;
    } else {
        url = 'https://www.bing.com/search?q=' + encodeURIComponent(val);
    }
    document.getElementById('webframe').src = url;
    showPage('browser-page');
    document.getElementById('urlInput').value = '';
}

function showPage(id){
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    document.getElementById('drop-menu').style.display = "none";
}

function toggleMenu(){
    const m = document.getElementById('drop-menu');
    m.style.display = m.style.display === "flex" ? "none" : "flex";
}

function logKernel(msg){
    const log = document.getElementById('kernel-log');
    log.innerHTML += `[${new Date().toLocaleTimeString()}] > ${msg}<br>`;
    log.scrollTop = log.scrollHeight;
}

function showToast(msg){
    const container = document.getElementById('notif-container');
    const t = document.createElement('div');
    t.className = "toast";
    t.innerText = msg;
    container.appendChild(t);
    setTimeout(() => t.remove(), 3000);
}

function resetDatabase(){
    if(state.currentUser.role !== 'ADMIN') { alert("Permesso negato."); return; }
    if(confirm("ATTENZIONE: Formattare l'intero database? Tutti i dati andranno persi.")){
        localStorage.removeItem('genesis_db');
        location.reload();
    }
}

function logout(){
    state.currentUser=null;
    save();
    location.reload();
}

function toggleTheme(){
    const d = document.documentElement;
    d.setAttribute('data-theme', d.getAttribute('data-theme')==='dark' ? 'light' : 'dark');
}

// AUTO-LOGIN se possibile
if(state.currentUser){
    const u = state.users.find(x=> x.id === state.currentUser.id);
    if(u && u.status !== 'banned'){
        state.currentUser = u;
        initUI();
    } else {
        state.currentUser = null;
        save();
    }
}
</script>

</body>
</html>
