<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>🌿 MG Manisha Glow Ayurvedic</title>
<style>
    /* ====== base styles (from your original) ====== */
    body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
        background: #fffdf9;
        position: relative;
        overflow-x: hidden;
    }

    body::before {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url('main-logo.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: 520px;
        opacity: 0.13;
        z-index: -1;
    }

    .top-logo, .bottom-logo {
        display: block;
        margin: 20px auto;
    }
    .top-logo { width: 130px; }
    .bottom-logo { width: 110px; }

    .container {
        max-width: 1100px;
        margin: auto;
        padding: 20px;
    }

    h1, h2 {
        text-align: center;
        color: #1f3812;
    }

    .products, .facepack {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 15px;
        margin-top: 20px;
    }

    .card {
        background: rgba(255,255,255,0.90);
        border-radius: 12px;
        padding: 18px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.10);
        text-align: center;
    }

    .card input {
        width: 100%;
        padding: 8px;
        margin-top: 8px;
        border-radius: 6px;
        border: 1px solid #aaa;
    }

    .order-box {
        background: rgba(255,255,255,0.95);
        padding: 15px;
        border-radius: 12px;
        margin-top: 25px;
        width: 100%;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
        box-shadow: 0 6px 18px rgba(0,0,0,0.10);
    }

    .order-box input, .order-box textarea {
        width: 100%;
        padding: 8px;
        margin-top: 8px;
        border-radius: 6px;
        border: 1px solid #aaa;
        font-size: 14px;
    }

    .order-box textarea {
        height: 60px;
    }

    .btn {
        background: #6b8e23;
        color: white;
        padding: 10px;
        border: none;
        width: 100%;
        margin-top: 12px;
        border-radius: 6px;
        cursor: pointer;
        font-size: 15px;
    }

    .company-details {
        text-align: center;
        margin-top: 35px;
        background: rgba(255,255,255,0.90);
        padding: 18px;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.08);
    }

    .company-details p {
        margin: 6px 0;
        font-size: 15px;
    }

    footer {
        text-align: center;
        margin-top: 40px;
        padding-bottom: 20px;
        color: #666;
    }

    /* ====== Bottom slide sheet (app style) ====== */
    .sheet-overlay {
        position: fixed;
        inset: 0;
        display: none;              /* shown when active */
        justify-content: flex-end;
        z-index: 9999;
        background: rgba(0,0,0,0.45);
        backdrop-filter: blur(4px);
    }

    .sheet {
        width: 100%;
        max-width: 1100px;
        background: linear-gradient(180deg, rgba(255,255,255,0.98), rgba(250,250,250,0.99));
        border-radius: 18px 18px 0 0;
        box-shadow: 0 -12px 36px rgba(0,0,0,0.25);
        max-height: 72vh;
        overflow-y: auto;
        padding: 18px;
        transform: translateY(100%);
        transition: transform 300ms ease;
    }

    .sheet.open { transform: translateY(0%); }

    .sheet .sheet-header {
        display:flex;
        align-items:center;
        justify-content:space-between;
        gap:10px;
        margin-bottom:10px;
    }

    .sheet .sheet-title {
        font-weight:700;
        font-size:18px;
        color:#16360f;
    }

    .sheet .close {
        background: #2c5f2d;
        color:#fff;
        border:none;
        padding:8px 12px;
        border-radius:8px;
        cursor:pointer;
    }

    .sheet table {
        width:100%;
        border-collapse:collapse;
        margin-top:8px;
    }
    .sheet th, .sheet td {
        padding:8px 6px;
        border-bottom:1px solid #eee;
        text-align:left;
        font-size:14px;
    }
    .sheet .param { color:#333; }
    .sheet .value { color:#1f3812; text-align:right; }

    /* small helper when report not available */
    .no-report {
        padding: 18px;
        background: #fff8f0;
        border-radius: 10px;
        border: 1px dashed #e0c9b0;
        color: #6b4a2a;
    }

    /* highlight (optional) */
    .highlight {
        box-shadow: 0 0 18px rgba(107,142,35,0.28);
        border-radius: 12px;
    }

    /* responsive tweak for small screens */
    @media (max-width:520px) {
        .products, .facepack {
            grid-template-columns: 1fr;
        }
        .sheet { border-radius: 12px 12px 0 0; }
    }

</style>
</head>
<body>

<div class="container">

<img src="main-logo.jpg" class="top-logo" alt="logo">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>✨ Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP SECTION -->
<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

    <div class="card">
        <h3>🍃 Neem Soap</h3>
        <input type="number" id="Neem" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('neem')">View Report</button>
    </div>

    <div class="card">
        <h3>🌿 Tulasi Soap</h3>
        <input type="number" id="Tulasi" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('tulasi')">View Report</button>
    </div>

    <div class="card">
        <h3>🍀 Aloe Vera Soap</h3>
        <input type="number" id="Aloe" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('aloe')">View Report</button>
    </div>

    <div class="card">
        <h3>🥛 Goat Milk Soap</h3>
        <input type="number" id="Goat" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('goat')">View Report</button>
    </div>

    <div class="card">
        <h3>🖤 Charcoal Soap</h3>
        <input type="number" id="Charcoal" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('charcoal')">View Report</button>
    </div>

    <div class="card">
        <h3>✨ Turmeric Soap</h3>
        <input type="number" id="Turmeric" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('turmeric')">View Report</button>
    </div>

    <div class="card">
        <h3>🍚 Rice Potato Soap</h3>
        <input type="number" id="Rice" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('rice')">View Report</button>
    </div>

    <div class="card">
        <h3>Bheem Sen Kapur Soap</h3>
        <input type="number" id="Bheem" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('bheem')">View Report</button>
    </div>

</div>

<!-- FACE PACK SECTION -->
<h2>🌸 Face Pack Collection (₹30 Each)</h2>

<div class="facepack">
    <div class="card">
        <h3>🍃 Neem Leaf Powder</h3>
        <input type="number" id="NFP" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('nfp')">View Report</button>
    </div>
    <div class="card">
        <h3>💧 Moisturizer Cream</h3>
        <input type="number" id="MFP" min="0" placeholder="Quantity">
        <button class="btn" onclick="openSheet('mfp')">View Report</button>
    </div>
</div>

<!-- ORDER FORM -->
<div class="order-box">

<h2 style="text-align:center;">📝 Customer Details</h2>

<input type="text" id="custName" placeholder="👤 Your Name">
<input type="text" id="custPhone" placeholder="📞 Phone Number">
<textarea id="custAddr" placeholder="🏠 Full Address"></textarea>

<input type="text" id="totalAmount" placeholder="💵 Total Amount (Auto)" readonly>

<button class="btn" onclick="placeOrder()">📩 WhatsApp Order भेजें</button>

</div>

<!-- COMPANY DETAILS -->
<div class="company-details">
    <p><b>🏢 Contact Name:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>📞 Mobile:</b> 8888942084</p>
    <p><b>💬 WhatsApp:</b> 8888942084</p>
    <p><b>📍 Address:</b> Rawande, Kopargaon, Ahilyanagar 423601</p>
    <p><b>📧 Email:</b> mgayurvedicc@gmail.com</p>
    <p><b>📸 Instagram:</b> @mg_manisha_glow_Ayurvedic_</p>
    <p><b>🌐 Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/</p>
</div>

<img src="main-logo.jpg" class="bottom-logo" alt="logo">

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic 🌿
</footer>

</div> <!-- container end -->

<!-- ===== Bottom slide sheet (hidden until opened) ===== -->
<div class="sheet-overlay" id="sheetOverlay" aria-hidden="true">
    <div class="sheet" id="sheet">
        <div class="sheet-header">
            <div class="sheet-title" id="sheetTitle">Report</div>
            <button class="close" onclick="closeSheet()">Close</button>
        </div>
        <div id="sheetContent">
            <!-- dynamic content inserted here -->
        </div>
    </div>
</div>

<script>
/* set year */
document.getElementById('year').textContent = new Date().getFullYear();

/* ====== Auto total calculation for all numeric inputs ====== */
function calcTotal() {
    // list all product IDs and their prices
    const pricing = {
        Neem: 50, Tulasi: 50, Aloe: 50, Goat: 50,
        Charcoal: 50, Turmeric: 50, Rice: 50, Bheem: 50,
        NFP: 30, MFP: 30
    };

    let total = 0;
    for (let id in pricing) {
        const el = document.getElementById(id);
        if (el) {
            let qty = parseInt(el.value) || 0;
            total += qty * pricing[id];
        }
    }

    document.getElementById('totalAmount').value = total ? ("₹ " + total) : "";
}

// attach listener to every number input
document.querySelectorAll("input[type='number']").forEach(inp => {
    inp.addEventListener('input', calcTotal);
});

// initial calculate (in case default values present)
calcTotal();

/* ====== Reports data (only those from your PDF included) ====== */
const REPORTS = {
    neem: {
        title: "🍃 Neem Soap - Lab Report",
        html: `<table>
                <tr><td class="param">PH at 25°C</td><td class="value">6.13</td></tr>
                <tr><td class="param">Lather (ml)</td><td class="value">212.0</td></tr>
                <tr><td class="param">Mush g/50 cm²</td><td class="value">18.5</td></tr>
                <tr><td class="param">Free Caustic Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Free Carbonated Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Freedom From Grittiness</td><td class="value">Passed</td></tr>
                <tr><td class="param">Freedom From Cracking</td><td class="value">Passed</td></tr>
                <tr><td class="param">Cleaning Efficiency</td><td class="value">Passed</td></tr>
                <tr><td class="param">Total Fatty Matter</td><td class="value">56.52%</td></tr>
                <tr><td class="param">Synthetic Surface Active Agent</td><td class="value">52.14</td></tr>
                <tr><td class="param">Fatty Matter From Dissolved Actives</td><td class="value">10.13</td></tr>
               </table>`
    },

    tulasi: {
        title: "🌿 Tulasi Soap - Lab Report",
        html: `<table>
                <tr><td class="param">PH at 25°C</td><td class="value">5.89</td></tr>
                <tr><td class="param">Lather (ml)</td><td class="value">204.3</td></tr>
                <tr><td class="param">Mush g/50 cm²</td><td class="value">18.5</td></tr>
                <tr><td class="param">Free Caustic Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Free Carbonated Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Freedom From Grittiness</td><td class="value">Passed</td></tr>
                <tr><td class="param">Freedom From Cracking</td><td class="value">Passed</td></tr>
                <tr><td class="param">Cleaning Efficiency</td><td class="value">Passed</td></tr>
                <tr><td class="param">Total Fatty Matter</td><td class="value">54.6%</td></tr>
                <tr><td class="param">Synthetic Surface Active Agent</td><td class="value">46.2</td></tr>
                <tr><td class="param">Fatty Matter From Dissolved Actives</td><td class="value">8.72</td></tr>
               </table>`
    },

    charcoal: {
        title: "🖤 Charcoal Soap - Lab Report",
        html: `<table>
                <tr><td class="param">PH at 25°C</td><td class="value">6.64</td></tr>
                <tr><td class="param">Lather (ml)</td><td class="value">202.0</td></tr>
                <tr><td class="param">Mush g/50 cm²</td><td class="value">16.1</td></tr>
                <tr><td class="param">Free Caustic Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Free Carbonated Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Freedom From Grittiness</td><td class="value">Passed</td></tr>
                <tr><td class="param">Freedom From Cracking</td><td class="value">Passed</td></tr>
                <tr><td class="param">Cleaning Efficiency</td><td class="value">Passed</td></tr>
                <tr><td class="param">Total Fatty Matter</td><td class="value">43%</td></tr>
                <tr><td class="param">Synthetic Surface Active Agent</td><td class="value">44.8</td></tr>
                <tr><td class="param">Fatty Matter From Dissolved Actives</td><td class="value">11.02</td></tr>
               </table>`
    },

    turmeric: {
        title: "✨ Turmeric Soap - Lab Report",
        html: `<table>
                <tr><td class="param">PH at 25°C</td><td class="value">6.28</td></tr>
                <tr><td class="param">Lather (ml)</td><td class="value">216.5</td></tr>
                <tr><td class="param">Mush g/50 cm²</td><td class="value">22.3</td></tr>
                <tr><td class="param">Free Caustic Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Free Carbonated Alkali</td><td class="value">Absent</td></tr>
                <tr><td class="param">Freedom From Grittiness</td><td class="value">Passed</td></tr>
                <tr><td class="param">Freedom From Cracking</td><td class="value">Passed</td></tr>
                <tr><td class="param">Cleaning Efficiency</td><td class="value">Passed</td></tr>
                <tr><td class="param">Total Fatty Matter</td><td class="value">64%</td></tr>
                <tr><td class="param">Synthetic Surface Active Agent</td><td class="value">45.1</td></tr>
                <tr><td class="param">Fatty Matter From Dissolved Actives</td><td class="value">18.0</td></tr>
               </table>`
    },

    // placeholders for soaps without PDF data
    aloe: { title: "🍀 Aloe Vera Soap - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट अभी उपलब्ध नहीं है। आप चाहें तो रिपोर्ट upload कर दें, मैं यहाँ जोड़ दूँगा।</div>` },
    goat: { title: "🥛 Goat Milk Soap - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट अभी उपलब्ध नहीं है।</div>` },
    rice: { title: "🍚 Rice Potato Soap - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट अभी उपलब्ध नहीं है।</div>` },
    bheem: { title: "Bheem Sen Kapur Soap - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट अभी उपलब्ध नहीं है।</div>` },
    nfp: { title: "🍃 Neem Leaf Powder - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट उपलब्ध नहीं है।</div>` },
    mfp: { title: "💧 Moisturizer Cream - Report", html: `<div class="no-report">इस product की लैब रिपोर्ट उपलब्ध नहीं है।</div>` }
};

/* ===== open sheet for specific product ===== */
function openSheet(key) {
    const overlay = document.getElementById('sheetOverlay');
    const sheet = document.getElementById('sheet');
    const titleEl = document.getElementById('sheetTitle');
    const contentEl = document.getElementById('sheetContent');

    const data = REPORTS[key];
    if (!data) {
        titleEl.textContent = "Report";
        contentEl.innerHTML = `<div class="no-report">Report not found.</div>`;
    } else {
        titleEl.innerHTML = data.title;
        contentEl.innerHTML = data.html;
    }

    overlay.style.display = 'flex';
    // allow animation (sheet has transform; add open class)
    setTimeout(()=> sheet.classList.add('open'), 10);
    overlay.setAttribute('aria-hidden', 'false');
}

/* ===== close sheet ===== */
function closeSheet() {
    const overlay = document.getElementById('sheetOverlay');
    const sheet = document.getElementById('sheet');
    sheet.classList.remove('open');
    // wait for transition then hide overlay
    setTimeout(()=> {
        overlay.style.display = 'none';
        overlay.setAttribute('aria-hidden', 'true');
        // clear content to prevent stale data
        document.getElementById('sheetContent').innerHTML = '';
    }, 300);
}

/* close when clicking on overlay outside sheet */
document.getElementById('sheetOverlay').addEventListener('click', function(e){
    // if click is directly on overlay (not on sheet), close
    if (e.target === this) closeSheet();
});

/* ===== Place Order (WhatsApp) ===== */
function placeOrder() {
    const name = document.getElementById('custName').value.trim();
    const phone = document.getElementById('custPhone').value.trim();
    const addr = document.getElementById('custAddr').value.trim();
    const totalText = document.getElementById('totalAmount').value || "₹ 0";

    if (!name || !phone || !addr) {
        alert("❗ कृपया Name, Phone और Address भरें!");
        return;
    }

    // build product list and quantities
    const products = [
        'Neem','Tulasi','Aloe','Goat','Charcoal','Turmeric','Rice','Bheem','NFP','MFP'
    ];
    let lines = [];
    for (let id of products) {
        const el = document.getElementById(id);
        if (!el) continue;
        const q = parseInt(el.value) || 0;
        if (q > 0) {
            lines.push(`${id}: ${q}`);
        }
    }
    if (lines.length === 0) {
        if (!confirm("आपने कोई product select नहीं किया है। फिर भी ऑर्डर भेजना है?")) return;
    }

    const msg =
`🧾 New Order from Website
----------------------------------
Products:
${lines.length ? lines.join('\n') : 'No items selected'}

----------------------------------
Total: ${totalText}

👤 Customer Name: ${name}
📞 Phone: ${phone}
🏠 Address:
${addr}`;

    // open WhatsApp
    const phoneTo = "918888942084";
    const url = `https://wa.me/${phoneTo}?text=${encodeURIComponent(msg)}`;
    window.open(url, '_blank');
}

</script>
</body>
</html>
