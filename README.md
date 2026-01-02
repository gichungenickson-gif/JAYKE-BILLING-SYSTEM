# JAYKE-BILLING-SYSTEM
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Emmanuel Hostels WiFi</title>
    <style>
        :root {
            --primary: #2c3e50;
            --accent: #e67e22;
            --light: #ecf0f1;
            --white: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light);
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            width: 90%;
            max-width: 800px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            margin: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 2rem;
            border-bottom: 2px solid var(--light);
            padding-bottom: 1rem;
        }

        h1 { color: var(--primary); margin: 0; font-size: 1.8rem; }
        p.subtitle { color: #7f8c8d; margin-top: 5px; }

        .plan-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-bottom: 2rem;
        }

        .plan-card {
            border: 2px solid var(--light);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            transition: transform 0.2s, border-color 0.2s;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .plan-card:hover {
            border-color: var(--accent);
            transform: translateY(-3px);
        }

        .plan-card.multi-device {
            background-color: #fffaf5;
            border-style: dashed;
        }

        .duration { font-weight: bold; color: var(--primary); font-size: 1.1rem; }
        .price { color: var(--accent); font-size: 1.3rem; font-weight: 800; margin: 5px 0; }
        .device-tag { 
            font-size: 0.75rem; 
            background: var(--primary); 
            color: white; 
            padding: 2px 8px; 
            border-radius: 10px;
            display: inline-block;
        }

        .payment-section {
            background: #f9f9f9;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
        }

        input[type="text"] {
            width: 80%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .btn-pay {
            background: var(--accent);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            font-size: 1rem;
            width: 85%;
            transition: background 0.3s;
        }

        .btn-pay:hover { background: #d35400; }

        @media (max-width: 480px) {
            .plan-grid { grid-template-columns: 1fr 1fr; }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>Emmanuel Hostels WiFi</h1>
        <p class="subtitle">Select a plan to get connected</p>
    </header>

    <div class="plan-grid">
        <div class="plan-card">
            <div class="duration">1 Hour</div>
            <div class="price">KES 15</div>
        </div>
        <div class="plan-card">
            <div class="duration">2 Hours</div>
            <div class="price">KES 20</div>
        </div>
        <div class="plan-card">
            <div class="duration">12 Hours</div>
            <div class="price">KES 30</div>
        </div>

        <div class="plan-card multi-device">
            <div class="duration">24 Hours</div>
            <div class="price">KES 35</div>
            <div><span class="device-tag">2 Devices</span></div>
        </div>
        <div class="plan-card multi-device">
            <div class="duration">1 Week</div>
            <div class="price">KES 300</div>
            <div><span class="device-tag">2 Devices</span></div>
        </div>
        <div class="plan-card multi-device">
            <div class="duration">2 Weeks</div>
            <div class="price">KES 470</div>
            <div><span class="device-tag">2 Devices</span></div>
        </div>
        <div class="plan-card multi-device">
            <div class="duration">1 Month</div>
            <div class="price">KES 680</div>
            <div><span class="device-tag">2 Devices</span></div>
        </div>
    </div>

    <div class="payment-section">
        <h3>M-PESA Payment</h3>
        <p style="font-size: 0.9rem; color: #666;">Enter your phone number to receive a payment prompt</p>
        <input type="text" placeholder="0712345678" id="phone">
        <button class="btn-pay">Pay Now</button>
    </div>
</div>

<script>
    // Logic for selecting a plan
    const cards = document.querySelectorAll('.plan-card');
    cards.forEach(card => {
        card.addEventListener('click', () => {
            cards.forEach(c => c.style.borderColor = '#ecf0f1');
            card.style.borderColor = '#e67e22';
            card.style.background = '#fffaf5';
        });
    });
</script>

</body>
</html>
