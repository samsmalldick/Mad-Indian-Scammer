i wont get it, i wont get it


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gift Card Redemption Drama</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      font-size: 2rem;
      text-align: center;
      color: white;
      background-color: #ff5733;
      transition: background-color 0.5s ease;
    }
    button {
      background: none;
      border: none;
      color: white;
      font-size: inherit;
      font-family: inherit;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <button id="message">Why did you redeem it</button>

  <script>
    const messages = [
      "Why did you redeem it",
      "Do not redeem it",
      "NO NO NOOOOOOO",
      "Do not redeem the gift card",
      "I WONT GET IT!, I WONT GET IT!",
      "WHY DID YOU DO THAT"
    ];

    let index = 0;

    // Change the text and background color
    const messageButton = document.getElementById("message");
    messageButton.addEventListener("click", () => {
      index = (index + 1) % messages.length; // Cycle through messages
      messageButton.textContent = messages[index];
    });

    // Change background color every second
    setInterval(() => {
      document.body.style.backgroundColor = getRandomColor();
    }, 1000);

    // Function to get a random color
    function getRandomColor() {
      const letters = '0123456789ABCDEF';
      let color = '#';
      for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    }
  </script>
</body>
</html>
