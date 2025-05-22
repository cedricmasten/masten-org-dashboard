# masten-org-dashboard
Dashboard
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Masten PR Firm Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .login-container {
      background-color: #fff;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 300px;
      text-align: center;
    }
    input, select {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background-color: #003366;
      color: white;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      width: 100%;
    }
    button:hover {
      background-color: #002244;
    }
    .message {
      margin-top: 20px;
      font-weight: bold;
      color: green;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <h2>Login to Masten Dashboard</h2>
    <input type="text" id="username" placeholder="Username" />
    <select id="role">
      <option value="executive">Executive</option>
      <option value="supervisor">Supervisor</option>
      <option value="employee">Employee</option>
    </select>
    <button onclick="login()">Login</button>
    <div class="message" id="message"></div>
  </div>
  <script>
    function login() {
      const user = document.getElementById('username').value.trim();
      const role = document.getElementById('role').value;
      const message = document.getElementById('message');

      if (user) {
        message.textContent = `Welcome ${user}! Loading ${role} dashboard...`;
        setTimeout(() => {
          // Simulate redirect with query param (or embed logic into index.html)
          window.location.href = `masten_dashboard.html?role=${role}`;
        }, 1500);
      } else {
        message.style.color = 'red';
        message.textContent = 'Please enter a valid username.';
      }
    }
  </script>
</body>
</html>

