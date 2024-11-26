 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Charity for Life</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #f8f9fa;
            opacity: 0;
            animation: fadeIn 2s forwards;
        }
        header {
            background: #004080;
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
        }
        header img {
            width: 100px;
        }
        h1 {
            opacity: 0;
            animation: slideIn 2s forwards;
            animation-delay: 1s;
        }
        nav {
            background: #004080;
            color: white;
            display: flex;
            justify-content: center;
            padding: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            padding: 10px 15px;
        }
        nav a:hover {
            background: #003366;
            border-radius: 5px;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .section {
            margin-bottom: 40px;
        }
        .section h2 {
            color: #004080;
            border-bottom: 2px solid #004080;
            display: inline-block;
            padding-bottom: 5px;
        }
        .contact-info {
            background: #f1f1f1;
            padding: 20px;
            margin-top: 20px;
            border-radius: 8px;
        }
        .contact-info h3 {
            margin-bottom: 10px;
        }
        .contact-info p {
            margin: 5px 0;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        form label {
            margin: 10px 0 5px;
            font-weight: bold;
        }
        form input, form textarea, form select {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
        }
        form button {
            background: #004080;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            margin-top: 20px;
            cursor: pointer;
        }
        form button:hover {
            background: #003366;
        }
        footer {
            background: #004080;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }
        #admin-dashboard {
            display: none;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }

        @keyframes slideIn {
            from {
                transform: translateY(-50px);
            }
            to {
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <header>
        <img src="logo.png" alt="Charity for Life Logo">
        <h1>Welcome to Charity for Life</h1>
        <p>Join us to make a difference!</p>
    </header>
    <nav>
        <a href="#about">About Us</a>
        <a href="#services">Services</a>
        <a href="#join">Join Us</a>
        <a href="#download">Download App</a>
        <a href="#login">Member Login</a>
        <a href="#admin">Admin Login</a>
    </nav>
    <div class="container">
        <!-- About Section -->
        <div id="about" class="section">
            <h2>About Us</h2>
            <p>Charity for Life is dedicated to helping orphans and individuals in need by providing basic necessities and support. Join us to make an impact.</p>
        </div>
        <!-- Services Section -->
        <div id="services" class="section">
            <h2>Services</h2>
            <ul>
                <li>Providing food and clothing to orphans and families in need.</li>
                <li>Educational support for children.</li>
                <li>Organizing community events for awareness and support.</li>
            </ul>
        </div>
        <!-- Registration Section -->
        <div id="join" class="section">
            <h2>Join Our Group</h2>
            <form id="joinForm">
                <label for="photo">Upload Your Photo:</label>
                <input type="file" id="photo" name="photo" accept="image/*" required>
                
                <label for="fullname">Enter Your Full Name (Three Names):</label>
                <input type="text" id="fullname" name="fullname" placeholder="First Name, Middle Name, Last Name" required>
                
                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" placeholder="e.g., +255XXXXXXXXX" required>
                
                <label for="occupation">Occupation:</label>
                <input type="text" id="occupation" name="occupation" placeholder="Your Occupation" required>
                
                <label for="reason">Why Do You Want to Join This Group?</label>
                <textarea id="reason" name="reason" rows="4" placeholder="Explain your motivation..." required></textarea>
                
                <button type="submit">Submit</button>
            </form>
        </div>
        <!-- Download Section -->
        <div id="download" class="section">
            <h2>Download Our Application</h2>
            <p>Click the link below to download our mobile application:</p>
            <a href="charity_app.apk" download style="color: #004080; font-weight: bold;">Download App</a>
        </div>
        <!-- Member Login Section -->
        <div id="login" class="section">
            <h2>Member Login</h2>
            <form id="loginForm">
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required>
                
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
                
                <button type="submit">Login</button>
            </form>
        </div>
        <!-- Admin Login Section -->
        <div id="admin" class="section">
            <h2>Admin Login</h2>
            <form id="adminLoginForm">
                <label for="admin_username">Admin Username:</label>
                <input type="text" id="admin_username" name="admin_username" required>
                
                <label for="admin_password">Admin Password:</label>
                <input type="password" id="admin_password" name="admin_password" required>
                
                <button type="submit">Admin Login</button>
            </form>
        </div>

        <!-- Admin Dashboard Section -->
        <div id="admin-dashboard" class="section">
            <h2>Admin Dashboard</h2>
            <h3>Registered Members</h3>
            <ul id="member-list"></ul>
            <button id="contactButton">Contact Members</button>
        </div>

        <!-- Contact Info Section -->
        <div class="contact-info">
            <h3>Contact Information</h3>
            <p><strong>Chairperson:</strong> <a href="tel:+255XXXXXXXXX">+255XXXXXXXXX</a></p>
            <p><strong>Vice Chairperson:</strong> <a href="tel:+255XXXXXXXXX">+255XXXXXXXXX</a></p>
            <p><strong>Social Media Director:</strong> <a href="tel:+255XXXXXXXXX">+255XXXXXXXXX</a></p>
            <p><strong>Email:</strong> <a href="mailto:charityforlife@example.com">charityforlife@example.com</a></p>
        </div>
    </div>
    <footer>
        <p>&copy; 2024 Charity for Life. All rights reserved.</p>
    </footer>

    <script>
        // Local storage mockup for user registration and login
        const members = JSON.parse(localStorage.getItem('members')) || [];
        const admins = [{ username: 'admin',
