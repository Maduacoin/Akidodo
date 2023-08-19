# Akidodo
<html>
<head>
    <title>Spin and Win Game</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css">
    <style>
        body {
            background-color: #f8f9fa;
        }
        .container {
            text-align: center;
            margin-top: 100px;
        }
        .spin-btn {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background-color: #007bff;
            color: #fff;
            font-size: 24px;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .spin-btn:hover {
            background-color: #0056b3;
        }
        .prize {
            font-size: 36px;
            font-weight: bold;
            margin-top: 50px;
            text-transform: uppercase;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Spin and Win Game</h1>
        <div class="spinner">
            <div class="spin-btn">SPIN</div>
        </div>
        <h2 class="prize"></h2>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.min.js"></script>
    <script>
        const prizes = [
            'Cash',
            'Phone',
            'Watches',
            'Grocery',
            'Food Voucher',
            'Sweets',
            'Chocolate',
            'Airtime'
        ];

        const spinBtn = document.querySelector('.spin-btn');
        const prizeElement = document.querySelector('.prize');

        spinBtn.addEventListener('click', () => {
            spinBtn.disabled = true;
            prizeElement.textContent = '';
            const randomIndex = Math.floor(Math.random() * prizes.length);
            const prize = prizes[randomIndex];

            setTimeout(() => {
                prizeElement.textContent = prize;
                spinBtn.disabled = false;
            }, 3000);
        });
    </script>
</body>
</html>
