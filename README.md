<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🌿 MG Manisha Glow Ayurvedic</title>

<style>
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

    .company-details {
        text-align: center;
        margin-top: 35px;
        background: rgba(255,255,255,0.90);
        padding: 18px;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.08);
    }

    footer {
        text-align: center;
        margin-top: 40px;
        padding-bottom: 20px;
        color: #666;
    }

    /* Report Box */
    .report-box {
        margin-top: 40px;
        background: white;
        padding: 18px;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.10);
    }

    table {
        border-collapse: collapse;
        width: 100%;
        margin-top: 10px;
    }

    table th, table td {
        border: 1px solid #666;
        padding: 6px;
        text-align: left;
        background: #fff;
    }

    table th {
        background: #e6f4d7;
    }

    /* Highlight for View Report */
    .highlight {
        border: 3px solid #6b8e23 !important;
        box-shadow: 0 0 20px rgba(107,142,35,0.5);
        transition: 0.4s;
    }
</style>
</head>

<body>

<div class="container">

<img src="main-logo.jpg" class="top-logo">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>✨ Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP SECTION -->
<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

    <div class="card">
        <h3>🍃 Neem Soap</h3>
        <input type="number" id="Neem" min="0" placeholder="Quantity">
        <button class="btn" onclick="showReport('neem')">View Report</button>
    </div>

    <div class="card">
        <h3>🌿 Tulasi Soap</h3>
        <input type="number" id="Tulasi" min="0" placeholder="Quantity">
        <button class="btn" onclick="showReport('tulasi')">View Report</button>
    </div>

    <div class="card">
        <h3>🍀 Aloe Vera Soap</h3>
        <input type="number" id="Aloe" min="0">
        <button class="btn" onclick="showReport('aloe')">View Report</button>
    </div>

    <div class="card">
        <h3>🥛 Goat Milk Soap</h3>
        <input type="number" id="Goat" min="0">
        <button class="btn" onclick="showReport('goat')">View Report</button>
    </div>

    <div class="card">
        <h3>🖤 Charcoal Soap</h3>
        <input type="number" id="Charcoal" min="0">
        <button class="btn" onclick="showReport('charcoal')">View Report</button>
    </div>

    <div class="card">
        <h3>✨ Turmeric Soap</h3>
        <input type="number" id="Turmeric" min="0">
        <button class="btn" onclick="showReport('turmeric')">View Report</button>
    </div>

    <div class="card">
        <h3>🍚 Rice Potato Soap</h3>
        <input type="number" id="Rice" min="0">
        <button class="btn" onclick="showReport('rice')">View Report</button>
    </div>

    <div class="card">
        <h3>Bheem Sen Kapur Soap</h3>
        <input type="number" id="Bheem" min="0">
        <button class="btn" onclick="showReport('bheem')">View Report</button>
    </div>

</div>

<!-- FACE PACK SECTION -->
<h2>🌸 Face Pack Collection (₹30 Each)</h2>

<div class="facepack">
    <div class="card">
        <h3>🍃 Neem Leaf Powder</h3>
        <input type="number" id="NFP" min="0">
        <button class="btn" onclick="showReport('nfp')">View Report</button>
    </div>

    <div class="card">
        <h3>💧 Moisturizer Cream</h3>
        <input type="number" id="MFP" min="0">
        <button class="btn" onclick="showReport('mfp')">View Report</button>
    </div>
</div>

<!-- REPORT SECTION -->
<div class="report-box" id="report-section">
    <h2>🧪 Soap Chemical Parameters Report</h2>

    <!-- Neem Soap -->
    <h3 id="title-neem">🍃 Neem Soap Report</h3>
    <table id="report-neem">
        <tr><th>SR</th><th>PARAMETERS</th><th>Result</th><th>Limits</th><th>IS</th></tr>
        <tr><td>01</td><td>PH at 25°C</td><td>6.13</td><td>4-9</td><td>13498</td></tr>
        <tr><td>02</td><td>Lather (ml)</td><td>212.0</td><td>200</td><td>13498</td></tr>
        <tr><td>03</td><td>Mush</td><td>18.5</td><td>15</td><td>13498</td></tr>
        <tr><td>04</td><td>Free Caustic Alkali</td><td>Absent</td><td>0.05</td><td>13498</td></tr>
        <tr><td>05</td><td>Free Carbonated Alkali</td><td>Absent</td><td>1.0</td><td>13498</td></tr>
        <tr><td>06</td><td>Grittiness</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>07</td><td>Cracking</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>08</td><td>Cleaning Efficiency</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>09a</td><td>Total Fatty Matter</td><td>56.52</td><td>40</td><td>13498</td></tr>
        <tr><td>09b</td><td>Synthetic Agent</td><td>52.14</td><td>40</td><td>13498</td></tr>
        <tr><td>09c</td><td>Fatty Matter (Dissolved)</td><td>10.13</td><td>8</td><td>13498</td></tr>
    </table>

    <br><br>

    <!-- Tulasi Soap -->
    <h3 id="title-tulasi">🌿 Tulasi Soap Report</h3>
    <table id="report-tulasi">
        <tr><th>SR</th><th>PARAMETERS</th><th>Result</th><th>Limits</th><th>IS</th></tr>
        <tr><td>01</td><td>PH</td><td>5.89</td><td>4-9</td><td>13498</td></tr>
        <tr><td>02</td><td>Lather</td><td>204.3</td><td>200</td><td>13498</td></tr>
        <tr><td>03</td><td>Mush</td><td>18.5</td><td>15</td><td>13498</td></tr>
        <tr><td>04</td><td>Free Caustic</td><td>Absent</td><td>0.05</td><td>13498</td></tr>
        <tr><td>05</td><td>Carbonated Alkali</td><td>Absent</td><td>1.0</td><td>13498</td></tr>
        <tr><td>06</td><td>Grittiness</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>07</td><td>Cracking</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>08</td><td>Cleaning</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>09a</td><td>Fatty Matter</td><td>54.6</td><td>40</td><td>13498</td></tr>
        <tr><td>09b</td><td>Synthetic</td><td>46.2</td><td>40</td><td>13498</td></tr>
        <tr><td>09c</td><td>Dissolved Fatty</td><td>8.72</td><td>8</td><td>13498</td></tr>
    </table>

    <br><br>

    <!-- Charcoal Soap -->
    <h3 id="title-charcoal">🖤 Charcoal Soap Report</h3>
    <table id="report-charcoal">
        <tr><th>SR</th><th>PARAMETERS</th><th>Result</th><th>Limits</th><th>IS</th></tr>
        <tr><td>01</td><td>PH</td><td>6.64</td><td>4-9</td><td>13498</td></tr>
        <tr><td>02</td><td>Lather</td><td>202.0</td><td>200</td><td>13498</td></tr>
        <tr><td>03</td><td>Mush</td><td>16.1</td><td>15</td><td>13498</td></tr>
        <tr><td>04</td><td>Caustic</td><td>Absent</td><td>0.05</td><td>13498</td></tr>
        <tr><td>05</td><td>Carbonated</td><td>Absent</td><td>1.0</td><td>13498</td></tr>
        <tr><td>06</td><td>Grittiness</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>07</td><td>Cracking</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>08</td><td>Cleaning</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>09a</td><td>Fatty Matter</td><td>43</td><td>40</td><td>13498</td></tr>
        <tr><td>09b</td><td>Synthetic Agent</td><td>44.8</td><td>40</td><td>13498</td></tr>
        <tr><td>09c</td><td>Dissolved Fatty</td><td>11.02</td><td>8</td><td>13498</td></tr>
    </table>

    <br><br>

    <!-- Turmeric Soap -->
    <h3 id="title-turmeric">✨ Turmeric Soap Report</h3>
    <table id="report-turmeric">
        <tr><th>SR</th><th>PARAMETERS</th><th>Result</th><th>Limits</th><th>IS</th></tr>
        <tr><td>01</td><td>PH</td><td>6.28</td><td>4-9</td><td>13498</td></tr>
        <tr><td>02</td><td>Lather</td><td>216.5</td><td>200</td><td>13498</td></tr>
        <tr><td>03</td><td>Mush</td><td>22.3</td><td>15</td><td>13498</td></tr>
        <tr><td>04</td><td>Caustic</td><td>Absent</td><td>0.05</td><td>13498</td></tr>
        <tr><td>05</td><td>Carbonated</td><td>Absent</td><td>1.0</td><td>13498</td></tr>
        <tr><td>06</td><td>Grittiness</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>07</td><td>Cracking</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>08</td><td>Cleaning</td><td>Passed</td><td>Passed</td><td>13498</td></tr>
        <tr><td>09a</td><td>Fatty Matter</td><td>64</td><td>40</td><td>13498</td></tr>
        <tr><td>09b</td><td>Synthetic</td><td>45.1</td><td>40</td><td>13498</td></tr>
        <tr><td>09c</td><td>Dissolved Fatty</td><td>18</td><td>8</td><td>13498</td></tr>
    </table>

</div>

<!-- ORDER FORM -->
<div class="order-box">
<h2>📝 Customer Details</h2>

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
<p><b>🌐 Website:</b> mgayurvedicc-ui.github.io</p>
</div>

<img src="main-logo.jpg" class="bottom-logo">

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic 🌿
</footer>

</div>

<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* CALCULATE TOTAL */
function calcTotal() {
    let total =
        (Neem.value * 50) +
        (Tulasi.value * 50) +
        (Aloe.value * 50) +
        (Goat.value * 50) +
        (Charcoal.value * 50) +
        (Turmeric.value * 50) +
        (Rice.value * 50) +
        (Bheem.value * 50) +
        (NFP.value * 30) +
        (MFP.value * 30);

    totalAmount.value = total;
}

document.querySelectorAll("input[type='number']").forEach(input=>{
    input.addEventListener("input", calcTotal);
});

/* VIEW REPORT BUTTON FUNCTION */
function showReport(type) {
    document.querySelectorAll("table").forEach(t => t.classList.remove("highlight"));

    let rpt = document.getElementById("report-" + type);
    if (rpt) {
        rpt.classList.add("highlight");
        rpt.scrollIntoView({ behavior: "smooth", block: "center" });
    }
}

/* SEND ORDER */
function placeOrder() {
    let name = custName.value;
    let phone = custPhone.value;
    let addr = custAddr.value;
    let total = totalAmount.value;

    if (!name || !phone || !addr) {
        alert("❗ कृपया Name, Phone और Address भरें!");
        return;
    }

    let msg =
`🧾 New Order  
---------------------------  
Neem: ${Neem.value}  
Tulasi: ${Tulasi.value}  
Aloe: ${Aloe.value}  
Goat: ${Goat.value}  
Charcoal: ${Charcoal.value}  
Turmeric: ${Turmeric.value}  
Rice: ${Rice.value}  
Bheem: ${Bheem.value}  
---------------------------  
Facepack:  
NFP: ${NFP.value}  
MFP: ${MFP.value}  
---------------------------  
Total: ₹${total}  
Name: ${name}  
Phone: ${phone}  
Address: ${addr}`;

    window.open(https://wa.me/918888942084?text=${encodeURIComponent(msg)});
}
</script>

</body>
</html>
