<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SMS System</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      padding: 20px;
    }

    .box {
      max-width: 400px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px gray;
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
    }

    button {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      background: green;
      color: white;
      border: none;
      cursor: pointer;
    }

    #result {
      margin-top: 10px;
      color: blue;
    }
  </style>
</head>
<body>

<div class="box">
  <h2>📱 SMS System</h2>

  <input type="text" id="number" placeholder="Enter phone number">

  <textarea id="message" placeholder="Write your message"></textarea>

  <button onclick="sendSMS()">Send SMS</button>

  <p id="result"></p>
</div>

<script>
function sendSMS() {
  let number = document.getElementById("number").value;
  let message = document.getElementById("message").value;

  if(number === "" || message === "") {
    document.getElementById("result").innerText = "Please fill all fields!";
    return;
  }

  // Hii ni simulation tu
  document.getElementById("result").innerText =
    "SMS sent to " + number + " (simulation)";
}
</script>

</body>
</html>
