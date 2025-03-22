<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exclusive Shipping</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">
            <h1>Exclusive Shipping</h1>
        </div>
    </header>

    <main>
        <div class="login-container">
            <h2>Login</h2>
            <form id="login-form" onsubmit="return validateForm()">
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email" required>
                </div>

                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" name="password" placeholder="Enter your password" required>
                </div>

                <button type="submit" class="submit-btn">Login</button>
            </form>
            <p class="signup-link">Don't have an account? <a href="#">Sign up</a></p>
        </div>
    </main>

    <footer>
        <p>&copy; 2025 Exclusive Shipping. All Rights Reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>




/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f3f3f3;
    color: #333;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px 0;
}

header h1 {
    margin: 0;
}

main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.login-container {
    background-color: white;
    padding: 30px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    width: 300px;
}

h2 {
    text-align: center;
    margin-bottom: 20px;
}

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

input[type="email"], input[type="password"] {
    margin-bottom: 10px;
}

button.submit-btn {
    width: 100%;
    padding: 10px;
    background-color: #333;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button.submit-btn:hover {
    background-color: #555;
}

.signup-link {
    text-align: center;
    margin-top: 20px;
}

.signup-link a {
    color: #333;
    text-decoration: none;
}

.signup-link a:hover {
    text-decoration: underline;
}

footer {
    text-align: center;
    padding: 10px 0;
    background-color: #333;
    color: white;
    position: fixed;
    width: 100%;
    bottom: 0;
}





// Simple form validation
function validateForm() {
    var email = document.getElementById('email').value;
    var password = document.getElementById('password').value;

    // Basic validation for email and password
    if (email == "" || password == "") {
        alert("Both fields are required.");
        return false;
    }
    return true;
}


