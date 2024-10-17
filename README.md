# Puretalk-Spam-Detection-software
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SGL Technologies - PureTalk Spam Detection</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background: #007bff;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            margin: 20px 0;
            text-align: center;
        }
        nav a {
            margin: 0 15px;
            color: #007bff;
            text-decoration: none;
            font-weight: bold;
        }
        section {
            padding: 20px;
            background: white;
            margin: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #333;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        h2 {
            color: #007bff;
        }
        .highlight {
            background: #e7f3ff;
            border-left: 5px solid #007bff;
            padding: 10px;
            margin: 10px 0;
        }
        /* Landing Page Styles */
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        h1 {
            color: #007bff;
        }
        p {
            line-height: 1.5;
            color: #555;
        }
        button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .hidden {
            display: none;
        }
        /* Overlay and Popup Styles */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: none;
            z-index: 5;
        }
        .otp-popup, .chat-popup {
            display: none;
            position: fixed;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background-color: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            z-index: 10;
        }
        .otp-popup button, .chat-popup button {
            margin-top: 10px;
        }
        /* App and Chat Styles */
        .app-list, .chat-list {
            margin-top: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .app-item, .chat-item {
            margin: 10px;
            padding: 10px;
            background: #e9ecef;
            border-radius: 5px;
            width: 80%;
            text-align: center;
            transition: background 0.3s;
            cursor: pointer;
        }
        .app-item:hover, .chat-item:hover {
            background: #d3d3d3;
        }
        .chat-options {
            display: flex;
            justify-content: space-around;
            margin-top: 10px;
        }
        /* Input Styles */
        input[type="text"], input[type="password"], input[type="email"] {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        /* Section Styles for Main Content */
        #main-content section {
            margin: 20px auto;
            max-width: 800px;
        }
    </style>
</head>
<body>
    <!-- Overlay for Popups -->
    <div class="overlay" id="overlay"></div>

    <!-- Header and Navigation -->
    <header>
        <p>SGL Technologies </p>
        <p>Innovative Software Development</p>
    </header>

    <nav>
        <a href="#" onclick="showLanding()">Home</a>
        <a href="#about" onclick="navigateTo('about')">About Us</a>
        <a href="#services" onclick="navigateTo('services')">Services</a>
        <a href="#project" onclick="navigateTo('project')">Our Project</a>
        <a href="#contact" onclick="navigateTo('contact')">Contact</a>
    </nav>

    <!-- Main Content -->
    <div id="main-content">
        <!-- Landing Page -->
        <div id="landing-page">

             <section id="project">
                <h2>Our Innovative Project</h2>
                <div class="highlight">
                    <p>We are developing a unique solution to identify spam calls and messages across platforms like WhatsApp, addressing a critical need in today's communication landscape. This aligns with SDG 9: Industry, Innovation, and Infrastructure.  <section id="about">
                <h2>About Us</h2>
                <p>Founded by Lingesh, SGL Technologies is dedicated to providing cutting-edge software solutions.</p>
                <p>We leverage our extensive knowledge to deliver innovative and effective solutions tailored to our clients' needs.</p>
            </section></p>
                </div>
                <p>Our goal is to enhance user experience and safety by implementing advanced algorithms that detect unwanted communications.</p>
                <button onclick="startPureTalk()">Get Started with PureTalk</button>
            </section>
  <section id="services">
                <h2>Our Services</h2>
                <ul>
                    <li>Custom Software Development</li>
                    <li>Mobile App Development</li>
                    <li>Web Development</li>
                    <li>Consulting Services</li>
                </ul>
            </section>

            <section id="contact">
                <h2>Contact Us</h2>
                <p>Email: info@sgltechnologies.com</p>
                <p>Phone: +123 456 7890</p>
            </section>
        </div>

        <!-- Sign Up Page -->
        <div class="container hidden" id="signup-page">
            <h2>Sign Up</h2>
            <input type="text" id="signup-username" placeholder="Enter your username" required>
            <input type="password" id="signup-password" placeholder="Create a password" required>
            <button onclick="signUp()">Sign Up</button>
            <button onclick="showLanding()">Back</button>
        </div>

        <!-- Login Page -->
        <div class="container hidden" id="login-page">
            <h2>Login</h2>
            <input type="text" id="login-username" placeholder="Enter your username" required>
            <input type="password" id="login-password" placeholder="Enter your password" required>
            <button onclick="login()">Login</button>
            <button onclick="showSignUp()">Back to Sign Up</button>
        </div>

        <!-- OTP Page -->
        <div class="container hidden" id="otp-page">
            <h2>Link Your Phone</h2>
            <input type="text" id="phone-number" placeholder="Enter your phone number" required>
            <input type="email" id="email" placeholder="Enter your email" required>
            <button onclick="sendOTP()">Send OTP</button>
            <button onclick="showLanding()">Back to Home</button>
        </div>

        <!-- Apps Page -->
        <div class="container hidden" id="apps-page">
            <h2>Messaging Apps</h2>
            <div class="app-list">
                <div class="app-item" onclick="showChatPage()">WhatsApp</div>
                <div class="app-item" onclick="showChatPage()">Telegram</div>
                <div class="app-item" onclick="showChatPage()">Messenger</div>
                <div class="app-item" onclick="showChatPage()">Viber</div>
                <div class="app-item" onclick="showChatPage()">LINE</div>
            </div>
            <button onclick="showLanding()">Back to Home</button>
        </div>

        <!-- Chat Page -->
        <div class="container hidden" id="chat-page">
            <h2>Chat Inbox</h2>
            <div class="chat-list" id="chat-list">
                <div class="chat-item" onclick="checkMessage('Hey, give your bank details')">Chat 1: Hey, give your bank details (Spam)</div>
                <div class="chat-item" onclick="checkMessage('Hi there, how are you?')">Chat 2: Hi there, how are you? (Normal)</div>
                <div class="chat-item" onclick="checkMessage('You won a lottery!')">Chat 3: You won a lottery! (Spam)</div>
                <div class="chat-item" onclick="checkMessage('Let’s meet for coffee')">Chat 4: Let’s meet for coffee (Normal)</div>
                <div class="chat-item" onclick="checkMessage('This is your invoice')">Chat 5: This is your invoice (Normal)</div>
            </div>
            <button onclick="showAppsPage()">Back to Apps</button>
        </div>

        <!-- OTP Popup -->
        <div class="otp-popup" id="otp-popup">
            <h2>Enter OTP</h2>
            <input type="text" id="otp-input" placeholder="Enter the OTP" required>
            <button onclick="verifyOTP()">Verify OTP</button>
            <button onclick="closeOTPPopup()">Cancel</button>
        </div>

        <!-- Chat Options Popup -->
        <div class="chat-popup" id="chat-popup">
            <h2>Chat Options</h2>
            <div class="chat-options">
                <button onclick="detectSpam()">Spam Detection</button>
                <button onclick="blockChat()">Block</button>
                <button onclick="reportChat()">Report</button>
                <button onclick="saveNumber()">Save Number</button>
            </div>
            <button onclick="closeChatOptions()">Close</button>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 SGL Technologies. All rights reserved.</p>
    </footer>

    <!-- JavaScript -->
    <script>
        let generatedOTP;
        let currentChatMessage;

        // Navigation Functions
        function navigateTo(sectionId) {
            document.getElementById('landing-page').style.display = 'block';
            document.getElementById('signup-page').classList.add('hidden');
            document.getElementById('login-page').classList.add('hidden');
            document.getElementById('otp-page').classList.add('hidden');
            document.getElementById('apps-page').classList.add('hidden');
            document.getElementById('chat-page').classList.add('hidden');
            const sections = document.querySelectorAll('#main-content section');
            sections.forEach(section => {
                if (section.id === sectionId) {
                    section.scrollIntoView({ behavior: 'smooth' });
                }
            });
        }

        // Start PureTalk
        function startPureTalk() {
            document.getElementById('landing-page').style.display = 'none';
            showSignUp();
        }

        // Show Sign Up Page
        function showSignUp() {
            document.getElementById('signup-page').classList.remove('hidden');
            document.getElementById('login-page').classList.add('hidden');
        }

        // Sign Up Function
        function signUp() {
            const username = document.getElementById('signup-username').value;
            const password = document.getElementById('signup-password').value;
            if (username && password) {
                alert(`Signed up with username: ${username}`);
                showLogin();
            } else {
                alert('Please fill in all fields.');
            }
        }

        // Show Login Page
        function showLogin() {
            document.getElementById('signup-page').classList.add('hidden');
            document.getElementById('login-page').classList.remove('hidden');
        }

        // Login Function
        function login() {
            const username = document.getElementById('login-username').value;
            const password = document.getElementById('login-password').value;
            if (username && password) {
                alert(`Logged in as: ${username}`);
                showOTPPage();
            } else {
                alert('Please fill in all fields.');
            }
        }

        // Show OTP Page
        function showOTPPage() {
            document.getElementById('login-page').classList.add('hidden');
            document.getElementById('otp-page').classList.remove('hidden');
        }

        // Send OTP
        function sendOTP() {
            const phoneNumber = document.getElementById('phone-number').value;
            const email = document.getElementById('email').value;
            if (phoneNumber && email) {
                generatedOTP = Math.floor(1000 + Math.random() * 9000);
                alert(`OTP sent to ${phoneNumber}: ${generatedOTP}`);
                showOTPPopup();
            } else {
                alert('Please fill in all fields.');
            }
        }

        // Show OTP Popup
        function showOTPPopup() {
            document.getElementById('overlay').style.display = 'block';
            document.getElementById('otp-popup').style.display = 'block';
        }

        // Close OTP Popup
        function closeOTPPopup() {
            document.getElementById('overlay').style.display = 'none';
            document.getElementById('otp-popup').style.display = 'none';
        }

        // Verify OTP
        function verifyOTP() {
            const otpInput = document.getElementById('otp-input').value;
            if (otpInput == generatedOTP) {
                alert('OTP verified successfully!');
                showAppsPage();
            } else {
                alert('Invalid OTP. Please try again.');
            }
            closeOTPPopup();
        }

        // Show Apps Page
        function showAppsPage() {
            document.getElementById('otp-page').classList.add('hidden');
            document.getElementById('apps-page').classList.remove('hidden');
        }

        // Show Chat Page
        function showChatPage() {
            document.getElementById('apps-page').classList.add('hidden');
            document.getElementById('chat-page').classList.remove('hidden');
        }

        // Check Message
        function checkMessage(message) {
            currentChatMessage = message;
            showChatOptions();
        }

        // Show Chat Options
        function showChatOptions() {
            document.getElementById('overlay').style.display = 'block';
            document.getElementById('chat-popup').style.display = 'block';
        }

        // Close Chat Options
        function closeChatOptions() {
            document.getElementById('overlay').style.display = 'none';
            document.getElementById('chat-popup').style.display = 'none';
        }

        // Detect Spam
        function detectSpam() {
            const spamKeywords = ["give your bank details", "won a lottery", "prize money", "urgent response needed", "please confirm your identity"];
            const isSpam = spamKeywords.some(keyword => currentChatMessage.toLowerCase().includes(keyword));
            if (isSpam) {
                alert('This message is marked as spam and will be removed from your inbox.');
                removeChatMessage(currentChatMessage);
            } else {
                alert('This message is not spam.');
            }
            closeChatOptions();
        }

        // Remove Chat Message
        function removeChatMessage(message) {
            const chatList = document.getElementById('chat-list');
            const chats = chatList.getElementsByClassName('chat-item');
            for (let i = 0; i < chats.length; i++) {
                if (chats[i].innerText.includes(message)) {
                    chatList.removeChild(chats[i]);
                    break;
                }
            }
        }

        // Block Chat
        function blockChat() {
            alert('Chat has been blocked and removed.');
            removeChatMessage(currentChatMessage);
            closeChatOptions();
        }

        // Report Chat
        function reportChat() {
            alert('Chat has been reported.');
            closeChatOptions();
        }

        // Save Number
        function saveNumber() {
            alert('Number has been saved successfully.');
            closeChatOptions();
        }

        // Show Landing Page
        function showLanding() {
            document.getElementById('landing-page').style.display = 'block';
            document.getElementById('signup-page').classList.add('hidden');
            document.getElementById('login-page').classList.add('hidden');
            document.getElementById('otp-page').classList.add('hidden');
            document.getElementById('apps-page').classList.add('hidden');
            document.getElementById('chat-page').classList.add('hidden');
            window.scrollTo(0, 0);
        }

        // Initialize Landing Page Visibility
        document.addEventListener('DOMContentLoaded', () => {
            showLanding();
        });
    </script>
</body>
</html>
