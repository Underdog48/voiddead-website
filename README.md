<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>VoidDead Login</title>
  <style>
    body {
      background-color: #121212;
      color: #f0f0f0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background-color: #1e1e1e;
      padding: 2rem;
      border-radius: 12px;
      box-shadow: 0 0 20px rgba(0,0,0,0.6);
      text-align: center;
      max-width: 400px;
      width: 90%;
    }
    input[type="password"], button {
      padding: 10px;
      margin: 10px 0;
      width: 100%;
      border: none;
      border-radius: 8px;
    }
    input {
      background-color: #2c2c2c;
      color: #fff;
    }
    button {
      background-color: #03a9f4;
      color: white;
      cursor: pointer;
    }
    iframe {
      width: 100%;
      height: 500px;
      border: none;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <div class="container" id="login-box">
    <h1>VoidDead Access</h1>
    <p>Enter the server password to access:</p>
    <input type="password" id="password" placeholder="Enter password" />
    <button onclick="login()">Enter</button>
    <p id="error" style="color:red;"></p>
  </div>

  <div class="container" id="iframe-box" style="display: none;">
    <h2>Welcome to VoidDead</h2>
    <iframe src="https://your-eaglercraft-url.com"></iframe>
  </div>

  <script>
    function login() {
      const pass = document.getElementById('password').value;
      if (pass === 'Killer47!') {
        document.getElementById('login-box').style.display = 'none';
        document.getElementById('iframe-box').style.display = 'block';
      } else {
        document.getElementById('error').textContent = 'Incorrect password';
      }
    }
  </script>
</body>
</html>
