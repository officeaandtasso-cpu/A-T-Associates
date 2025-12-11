<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic</title>

<style>
    body {
        margin: 0;
        padding: 0;
        background: #fffdf9;
        font-family: Arial;
    }

    .container {
        padding: 20px;
        max-width: 1100px;
        margin: auto;
    }

    h1, h2 {
        text-align: center;
        color: #1f3812;
    }

    .products {
        display: grid;
        grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
        gap: 15px;
        margin-top: 20px;
    }

    .card {
        background: white;
        padding: 15px;
        border-radius: 12px;
        box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        text-align: center;
    }

    .card input {
        width: 100%;
        padding: 8px;
        margin-top: 6px;
        border-radius: 6px;
        border: 1px solid #aaa;
    }

    .btn {
        width: 100%;
        background: #2c5f2d;
        color: white;
        margin-top: 10px;
        padding: 10px;
        border: none;
        border-radius: 6px;
        cursor: pointer;
    }

    /* Bottom Slide Sheet */
    .sheet-bg {
        position: fixed;
        inset: 0;
        background: rgba(0,0,0,0.55);
        backdrop-filter: blur(5px);
        display: none;
        justify-content: flex-end;
        z-index: 999;
    }

    .sheet {
        width: 100%;
        max-height: 70%;
        background: #ffffff;
        border-radius: 20px 20px 0 0;
        padding: 20px;
        animation: slideUp 0.35s ease;
        overflow-y: auto;
    }

    @keyframes slideUp {
        from { transform: translateY(100%); }
        to { transform: translateY(0); }
    }

    .close-btn {
        background: #d9534f;
        color: white;
        border: none;
        padding: 8px 18px;
        float: right;
        border-radius: 6px;
        cursor: pointer;
    }

    table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 12px;
    }

    th, td {
        border: 1px solid #999;
        padding: 6px;
    }

    th {
        background: #e8f5e9;
    }

</style>
</head>

<body>

<div class="container">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

    <div class="card">
        <h3>🍃 Neem Soap</h3>
        <input type="number" id="Neem" min="0">
        <button class="btn" onclick="openSheet('neem')">View Report</button>
    </div>

    <div class="card">
        <h3>🌿 Tulasi Soap</h3>
        <input type="number" id="Tulasi" min="0">
        <button class="btn" onclick="openSheet('tulasi')">View Report</button>
    </div>

    <div class="card">
        <h3>🖤 Charcoal Soap</h3>
        <input type="number" id="Charcoal" min="0">
        <button class="btn" onclick="openSheet('charcoal')">View Report</button>
    </div>

    <div class="card">
        <h3>✨ Turmeric Soap</h3>
        <input type="number" id="Turmeric" min="0">
        <button class="btn" onclick="openSheet('turmeric')">View Report</button>
    </div>

</div>

<h2>📝 Customer Details</h2>

<input type="text" id="custName" placeholder="Name" style="width:100%;padding:10px;border:1px solid #aaa;border-radius:6px;">
<br><br>
<input type="text" id="custPhone" placeholder="Phone" style="width:100%;padding:10px;border:1px solid #aaa;border-radius:6px;">
<br><br>
<textarea id="custAddr" placeholder="Full Address" style="width:100%;height:70px;padding:10px;border:1px solid #aaa;border-radius:6px;"></textarea>
<br><br>

<input id="totalAmount" readonly placeholder="Total Amount" style="width:100%;padding:10px;border:1px solid #aaa;border-radius:6px;background:#eee;">

</div>


<!-- ⭐ Bottom Slide Sheet -->
<div class="sheet-bg" id="sheetBG">
    <div class="sheet">
        <button class="close-btn" onclick="closeSheet()">Close</button>
        <h2 id="reportTitle"></h2>
        <div id="reportData"></div>
    </div>
</div>


<script>
/* 🔢 AUTO TOTAL CALC */
function calcTotal(){
    let total =
        (Neem.value * 50) +
        (Tulasi.value * 50) +
        (Charcoal.value * 50) +
        (Turmeric.value * 50);

    totalAmount.value = "₹ " + total;
}

document.querySelectorAll("input[type='number']").forEach(inp=>{
    inp.addEventListener("input", calcTotal);
});


/* 🧪 SOAP REPORT DATA */
const REPORTS = {

    neem: `
    <table>
        <tr><th>Parameter</th><th>Result</th></tr>
        <tr><td>pH</td><td>6.13</td></tr>
        <tr><td>Lather</td><td>212 ml</td></tr>
        <tr><td>Mush</td><td>18.5 g</td></tr>
        <tr><td>Free Caustic</td><td>Absent</td></tr>
        <tr><td>Total Fatty Matter</td><td>56.52%</td></tr>
    </table>`,

    tulasi: `
    <table>
        <tr><th>Parameter</th><th>Result</th></tr>
        <tr><td>pH</td><td>5.89</td></tr>
        <tr><td>Lather</td><td>204.3 ml</td></tr>
        <tr><td>Mush</td><td>18.5 g</td></tr>
        <tr><td>Free Caustic</td><td>Absent</td></tr>
        <tr><td>Total Fatty Matter</td><td>54.6%</td></tr>
    </table>`,

    charcoal: `
    <table>
        <tr><th>Parameter</th><th>Result</th></tr>
        <tr><td>pH</td><td>6.64</td></tr>
        <tr><td>Lather</td><td>202 ml</td></tr>
        <tr><td>Mush</td><td>16.1 g</td></tr>
        <tr><td>Free Caustic</td><td>Absent</td></tr>
        <tr><td>Total Fatty Matter</td><td>43%</td></tr>
    </table>`,

    turmeric: `
    <table>
        <tr><th>Parameter</th><th>Result</th></tr>
        <tr><td>pH</td><td>6.28</td></tr>
        <tr><td>Lather</td><td>216.5 ml</td></tr>
        <tr><td>Mush</td><td>22.3 g</td></tr>
        <tr><td>Free Caustic</td><td>Absent</td></tr>
        <tr><td>Total Fatty Matter</td><td>64%</td></tr>
    </table>`
};


/* 📱 OPEN BOTTOM SLIDE SHEET */
function openSheet(type){
    document.getElementById("reportTitle").innerHTML =
        type.charAt(0).toUpperCase() + type.slice(1) + " Soap Report";

    document.getElementById("reportData").innerHTML = REPORTS[type];

    document.getElementById("sheetBG").style.display = "flex";
}


/* ❌ CLOSE SHEET */
function closeSheet(){
    document.getElementById("sheetBG").style.display = "none";
}

</script>

</body>
</html>
