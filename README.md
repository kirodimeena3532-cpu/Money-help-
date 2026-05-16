# Money-help-
All people free helping website 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MoneyHelp - Smart Financial Tips</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: #f4f7f6;
            color: #333;
        }
        header {
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        header h1 {
            font-size: 2.5rem;
        }
        header p {
            margin-top: 5px;
            font-size: 1.1rem;
            opacity: 0.9;
        }
        .container {
            max-width: 1000px;
            margin: 30px auto;
            padding: 0 20px;
        }
        .section-title {
            text-align: center;
            margin-bottom: 30px;
            color: #1e3c72;
        }
        /* Grid Layout for Cards */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        .card {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card h3 {
            color: #2a5298;
            margin-bottom: 15px;
        }
        .card p {
            line-height: 1.6;
            color: #555;
        }
        /* Calculator Tool */
        .calculator-box {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            max-width: 500px;
            margin: 0 auto 40px auto;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .form-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
        }
        button {
            width: 100%;
            padding: 12px;
            background: #27ae60;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            cursor: pointer;
            font-weight: bold;
        }
        button:hover {
            background: #219653;
        }
        .result {
            margin-top: 20px;
            padding: 15px;
            background: #e8f8f5;
            border-left: 5px solid #27ae60;
            border-radius: 4px;
            display: none;
            font-size: 1.1rem;
            font-weight: bold;
            color: #27ae60;
        }
        footer {
            background: #1e3c72;
            color: white;
            text-align: center;
            padding: 15px 0;
            margin-top: 50px;
        }
    </style>
</head>
<body>

    <header>
        <h1>MoneyHelp</h1>
        <p>Apne Paise Ko Sahi Jagah Lagayein Aur Dhairya Se Badhayein</p>
    </header>

    <div class="container">
        
        <h2 class="section-title">Smart Financial Tips</h2>
        <div class="grid">
            <div class="card">
                <h3>1. Budget Banayein (50/30/20 Rule)</h3>
                <p>Apni kamai ka 50% zarooraton (Needs) par, 30% shouq (Wants) par, aur kam se kam 20% har mahine bachat (Savings) mein dalein.</p>
            </div>
            <div class="card">
                <h3>2. Emergency Fund Hai Zaroori</h3>
                <p>Kisi bhi unforeseen situation ya medical emergency ke liye kam se kam 6 mahine ka kharcha ek alag account mein save karke rakhein.</p>
            </div>
            <div class="card">
                <h3>3. Fuzool Kharqi Se Bachein</h3>
                <p>Koi bhi bada shouq ka saman khareodne se pehle 48 ghante ka intezar karein. Agar tab bhi zaroorat lage, tabhi paise kharch karein.</p>
            </div>
        </div>

        <h2 class="section-title">Interactive Tool: Savings Calculator</h2>
        <div class="calculator-box">
            <div class="form-group">
                <label for="income">Aapki Monthly Income (₹):</label>
                <input type="number" id="income" placeholder="E.g. 30000">
            </div>
            <div class="form-group">
                <label for="savingsPercent">Kitne % Bachana Chahte Hain?:</label>
                <input type="number" id="savingsPercent" placeholder="E.g. 20" value="20">
            </div>
            <button onclick="calculateSavings()">Calculate Budget</button>
            
            <div class="result" id="savingsResult"></div>
        </div>

    </div>

    <footer>
        <p>&copy; 2026 MoneyHelp. Built for Financial Awareness.</p>
    </footer>

    <script>
        function calculateSavings() {
            const income = document.getElementById('income').value;
            const percent = document.getElementById('savingsPercent').value;
            const resultDiv = document.getElementById('savingsResult');

            if(income === '' || percent === '') {
                alert('Kripya sahi number dalein!');
                return;
            }

            const savingsAmount = (income * percent) / 100;
            const expensesAmount = income - savingsAmount;

            resultDiv.style.display = 'block';
            resultDiv.innerHTML = `
                Aapki Monthly Bachat: ₹${savingsAmount.toLocaleString('en-IN')}<br>
                Kharch karne ke liye bache: ₹${expensesAmount.toLocaleString('en-IN')}
            `;
        }
    </script>
</body>
</html>
