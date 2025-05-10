<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f2f5;
      display: flex;
      height: 100vh;
      justify-content: center;
      align-items: center;
    }

    .login-container {
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      width: 300px;
    }

    .login-container h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    input[type="text"],
    input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }

    button {
      width: 100%;
      padding: 10px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background: #0056b3;
    }

    .message {
      text-align: center;
      margin-top: 15px;
      color: green;
    }
  </style>
</head>
<body>

  <div class="login-container">
    <h2>Login</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Username" required>
      <input type="password" id="password" placeholder="Password" required>
      <button type="submit">Submit</button>
    </form>
    <div class="message" id="message"></div>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function(event) {
      event.preventDefault(); // Prevent form from reloading the page

      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      // Example: simple login validation
      if (username === "admin" && password === "admin123") {
        document.getElementById("message").textContent = "Login successful!";
      } else {
        document.getElementById("message").textContent = "Invalid username or password.";
        document.getElementById("message").style.color = "red";
      }
    });
  </script>

</body>
</html>
