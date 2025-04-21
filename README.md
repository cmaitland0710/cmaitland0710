## Hi there 👋
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crypto Faucet</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        select, input, button {
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            font-size: 16px;
        }
        .message {
            margin-top: 10px;
            color: green;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Crypto Faucet - Get Large Amounts of Crypto</h2>
        <p>Receive generous amounts of cryptocurrency instantly!</p>
        <select id="crypto-select">
            <option>Bitcoin</option>
            <option>Ethereum</option>
            <option>Binance Coin</option>
            <option>Solana</option>
            <option>Polygon</option>
            <option>XRP</option>
            <option>Dogecoin</option>
            <option>Litecoin</option>
            <option>Cardano</option>
        </select>
        <input type="text" id="wallet-address" placeholder="Enter your wallet address">
        <input type="number" id="amount" placeholder="Enter amount" min="1" step="1">
        <button onclick="requestFunds()">Request Large Amount</button>
        <p id="message" class="message"></p>
    </div>

    <script>
        function requestFunds() {
            const walletAddress = document.getElementById("wallet-address").value;
            const selectedCrypto = document.getElementById("crypto-select").value;
            const amount = document.getElementById("amount").value;
            const message = document.getElementById("message");

            if (!walletAddress) {
                message.style.color = "red";
                message.textContent = "Please enter a valid wallet address.";
                return;
            }

            if (!amount || amount <= 0) {
                message.style.color = "red";
                message.textContent = "Please enter a valid amount.";
                return;
            }
            
            message.style.color = "green";
            message.textContent = `Success! A large amount of ${amount} ${selectedCrypto} has been sent to ${walletAddress}.`;
        }
    </script>
</body>
</html>
<!--
**cmaitland0710/cmaitland0710** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
