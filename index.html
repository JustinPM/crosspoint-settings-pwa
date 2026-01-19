<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#1a1a1a">
    <title>CrossPoint | Ultimate Remote Manager</title>
    
    <link rel="manifest" href='data:application/manifest+json,{"name":"CrossPoint Manager","short_name":"CrossPoint","start_url":".","display":"standalone","background_color":"#0d0d0d","theme_color":"#00ff41","icons":[{"src":"https://cdn-icons-png.flaticon.com/512/2906/2906274.png","sizes":"512x512","type":"image/png"}]}'>
    <link rel="apple-touch-icon" href="https://cdn-icons-png.flaticon.com/512/2906/2906274.png">

    <style>
        :root { --neon: #00ff41; --bg: #0d0d0d; --card: #1a1a1a; --border: #333; }
        body { font-family: 'Consolas', monospace; background: var(--bg); color: var(--neon); padding: 20px; line-height: 1.4; margin: 0; }
        .container { max-width: 950px; margin: 0 auto; }
        .card { background: var(--card); border: 1px solid var(--border); padding: 25px; border-radius: 12px; margin-bottom: 20px; }
        .remote-panel { background: #000; border: 1px solid #444; padding: 15px; margin-bottom: 20px; display: flex; gap: 15px; align-items: center; border-radius: 8px; }
        .log-stream { background: #000; color: #008f11; padding: 12px; font-size: 11px; height: 100px; overflow-y: auto; border: 1px solid #222; margin-bottom: 20px; }
        .wifi-node { background: #222; border-left: 4px solid var(--neon); padding: 15px; margin-bottom: 10px; display: grid; grid-template-columns: 1fr 1fr 45px; gap: 15px; align-items: end; }
        .settings-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 15px; margin-bottom: 20px; }
        .full-width { grid-column: 1 / -1; }
        input, select { background: #000; border: 1px solid #444; color: var(--neon); padding: 10px; border-radius: 4px; width: 100%; box-sizing: border-box; }
        button { cursor: pointer; padding: 10px 20px; border: none; border-radius: 4px; font-weight: bold; }
        .btn-upload { background: var(--neon); color: #000; }
        .btn-download { background: #fff; color: #000; }
        .btn-danger { background: #600; color: #fff; }
        label { color: #888; font-size: 10px; display: block; margin-bottom: 5px; text-transform: uppercase; letter-spacing: 1px; }
        h2 { margin-top: 0; color: #fff; border-bottom: 1px solid #333; padding-bottom: 10px; font-size: 18px; }
        
        @media (max-width: 600px) {
            .wifi-node { grid-template-columns: 1fr; }
            .remote-panel { flex-direction: column; align-items: stretch; }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="card">
        <h2>📡 DEVICE CONNECTION</h2>
        <div class="remote-panel">
            <div style="flex-grow: 1;">
                <label>Target Hostname / IP</label>
                <input type="text" id="deviceIP" value="crosspoint.local">
            </div>
        </div>
        <div id="terminal" class="log-stream">SYSTEM_OFFLINE_READY...</div>
    </div>

    <div class="card">
        <h2>⚙️ READER SETTINGS (settings.bin)</h2>
        <input type="file" id="setIn" onchange="readSettingsFile()" style="margin-bottom:20px; color: #888;">
        
        <div class="settings-grid" id="settingsForm">
            <div><label>Sleep Screen</label><input type="number" id="field_0" value="0"></div>
            <div><label>Extra Para Spacing</label><input type="number" id="field_1" value="0"></div>
            <div><label>Short Pwr Btn</label><input type="number" id="field_2" value="0"></div>
            <div><label>Status Bar</label><input type="number" id="field_3" value="1"></div>
            <div><label>Orientation</label>
                <select id="field_4">
                    <option value="0">Portrait</option>
                    <option value="1">Landscape CW</option>
                    <option value="2">Inverted</option>
                    <option value="3">Landscape CCW</option>
                </select>
            </div>
            <div><label>Front Btn Layout</label><input type="number" id="field_5" value="0"></div>
            <div><label>Side Btn Layout</label><input type="number" id="field_6" value="0"></div>
            <div><label>Font Family</label>
                <select id="field_7">
                    <option value="0">Bookerly</option>
                    <option value="1">Noto Sans</option>
                    <option value="2">Open Dyslexic</option>
                </select>
            </div>
            <div><label>Font Size</label><input type="number" id="field_8" value="14"></div>
            <div><label>Line Spacing</label><input type="number" id="field_9" value="0"></div>
            <div><label>Para Alignment</label><input type="number" id="field_10" value="0"></div>
            <div><label>Sleep Timeout</label><input type="number" id="field_11" value="10"></div>
            <div><label>Refresh Freq</label><input type="number" id="field_12" value="15"></div>
            <div><label>Screen Margin</label><input type="number" id="field_13" value="0"></div>
            <div><label>Sleep Cover Mode</label><input type="number" id="field_14" value="0"></div>
            <div class="full-width"><label>OPDS Server URL</label><input type="text" id="field_url" value="http://"></div>
            <div><label>Anti-Aliasing</label><input type="number" id="field_15" value="1"></div>
            <div><label>Hide Battery %</label><input type="number" id="field_16" value="0"></div>
            <div><label>Long Press Skip</label><input type="number" id="field_17" value="1"></div>
        </div>

        <div style="display:flex; gap:10px;">
            <button class="btn-download" onclick="exportSettings(true)">💾 DOWNLOAD BIN</button>
            <button class="btn-upload" style="flex-grow:1" onclick="uploadFile('settings')">🚀 UPLOAD TO DEVICE</button>
        </div>
    </div>

    <div class="card">
        <h2>🌐 WIFI PROFILES (wifi.bin)</h2>
        <input type="file" id="wifiIn" onchange="readWifiFile()" style="margin-bottom:15px; color: #888;">
        <div id="entryList"></div>
        <button onclick="addNewWifi('', '')" style="background:#333; color:#fff; width:100%; margin-bottom:15px;">+ ADD NETWORK</button>
        <div style="display:flex; gap:10px;">
            <button class="btn-download" onclick="exportWifi(true)">💾 DOWNLOAD BIN</button>
            <button class="btn-upload" style="flex-grow:1" onclick="uploadFile('wifi')">🚀 UPLOAD TO DEVICE</button>
        </div>
    </div>
</div>

<script>
    // --- SERVICE WORKER REGISTRATION ---
    if ('serviceWorker' in navigator) {
        window.addEventListener('load', () => {
            const swCode = `
                const CACHE_NAME = 'crosspoint-v1';
                self.addEventListener('install', e => {
                    e.waitUntil(caches.open(CACHE_NAME).then(cache => cache.addAll(['./'])));
                });
                self.addEventListener('fetch', e => {
                    e.respondWith(caches.match(e.request).then(res => res || fetch(e.request)));
                });
            `;
            const blob = new Blob([swCode], {type: 'text/javascript'});
            navigator.serviceWorker.register(URL.createObjectURL(blob));
        });
    }

    const WIFI_KEY = [0x43, 0x72, 0x6F, 0x73, 0x73, 0x50, 0x6F, 0x69, 0x6E, 0x74];

    function print(msg) {
        const t = document.getElementById('terminal');
        t.innerHTML += `[${new Date().toLocaleTimeString()}] ${msg}<br>`;
        t.scrollTop = t.scrollHeight;
    }

    async function readSettingsFile() {
        const file = document.getElementById('setIn').files[0];
        if (!file) return;
        const data = new Uint8Array(await file.arrayBuffer());
        let ptr = 0;
        const version = data[ptr++];
        const count = data[ptr++];
        print(`Settings: Version ${version}, Count ${count}`);
        for(let i=0; i<15; i++) {
            if (ptr < data.length) document.getElementById(`field_${i}`).value = data[ptr++];
        }
        const sLen = data[ptr] | (data[ptr+1] << 8) | (data[ptr+2] << 16) | (data[ptr+3] << 24);
        ptr += 4;
        document.getElementById('field_url').value = new TextDecoder().decode(data.slice(ptr, ptr + sLen));
        ptr += sLen;
        for(let i=15; i<18; i++) {
            if (ptr < data.length) document.getElementById(`field_${i}`).value = data[ptr++];
        }
    }

    function exportSettings(dl) {
        const out = [1, 18];
        for(let i=0; i<15; i++) out.push(parseInt(document.getElementById(`field_${i}`).value));
        const url = document.getElementById('field_url').value;
        const sBuf = new TextEncoder().encode(url);
        [sBuf.length, 0, 0, 0].forEach(b => out.push(b));
        sBuf.forEach(b => out.push(b));
        for(let i=15; i<18; i++) out.push(parseInt(document.getElementById(`field_${i}`).value));
        const blob = new Blob([new Uint8Array(out)], { type: 'application/octet-stream' });
        if (dl) triggerDownload(blob, 'settings.bin');
        return blob;
    }

    async function readWifiFile() {
        const file = document.getElementById('wifiIn').files[0];
        if (!file) return;
        const data = new Uint8Array(await file.arrayBuffer());
        document.getElementById('entryList').innerHTML = '';
        let ptr = 2; 
        for (let i = 0; i < data[1]; i++) {
            const sLen = data[ptr] | (data[ptr+1] << 8) | (data[ptr+2] << 16) | (data[ptr+3] << 24);
            const ssid = new TextDecoder().decode(data.slice(ptr + 4, ptr + 4 + sLen));
            ptr += 4 + sLen;
            const pLen = data[ptr] | (data[ptr+1] << 8) | (data[ptr+2] << 16) | (data[ptr+3] << 24);
            const pass = new TextDecoder().decode(data.slice(ptr + 4, ptr + 4 + pLen).map((b, j) => b ^ WIFI_KEY[j % 10]));
            ptr += 4 + pLen;
            addNewWifi(ssid, pass);
        }
    }

    function addNewWifi(s, p) {
        const div = document.createElement('div');
        div.className = 'wifi-node';
        div.innerHTML = `<div><label>SSID</label><input type="text" class="ssid" value="${s}"></div>
                         <div><label>PASS</label><input type="text" class="pass" value="${p}"></div>
                         <button class="btn-danger" onclick="this.parentElement.remove()">X</button>`;
        document.getElementById('entryList').appendChild(div);
    }

    function exportWifi(dl) {
        const rows = document.querySelectorAll('.wifi-node');
        const out = [1, rows.length];
        rows.forEach(row => {
            const s = new TextEncoder().encode(row.querySelector('.ssid').value);
            const p = new TextEncoder().encode(row.querySelector('.pass').value);
            [s.length, 0, 0, 0].forEach(b => out.push(b)); s.forEach(b => out.push(b));
            [p.length, 0, 0, 0].forEach(b => out.push(b)); p.forEach((b, i) => out.push(b ^ WIFI_KEY[i % 10]));
        });
        const blob = new Blob([new Uint8Array(out)], { type: 'application/octet-stream' });
        if (dl) triggerDownload(blob, 'wifi.bin');
        return blob;
    }

    function triggerDownload(blob, name) {
        const a = document.createElement('a');
        a.href = URL.createObjectURL(blob);
        a.download = name; a.click();
    }

    async function uploadFile(type) {
        const host = document.getElementById('deviceIP').value;
        const blob = (type === 'wifi') ? exportWifi(false) : exportSettings(false);
        const fileName = (type === 'wifi') ? 'wifi.bin' : 'settings.bin';
        const formData = new FormData();
        formData.append('file', blob, fileName);
        const url = `http://${host}/upload?path=/.crosspoint/`;
        print(`UPLOADING ${fileName} to ${host}...`);
        try {
            await fetch(url, { method: 'POST', body: formData, mode: 'no-cors' });
            print(`TRANSMITTED: Check device for update.`);
        } catch (err) { print(`ERROR: Request failed.`); }
    }
</script>
</body>
</html>
