
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Surprise Love Letter!</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0e68c; /* Light red like paper/envelope */
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      flex-direction: column;
    }

    .envelope {
      width: 200px;
      height: 150px;
      background-color: #f5f5dc; /* Beige envelope color */
      border: 3px solid #8b4513; /* Brown border */
      position: relative;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 24px;
      transition: transform 0.3s ease;
      margin-bottom: 20px;
    }

    .envelope:hover {
      transform: scale(1.05);
    }

    .envelope::before {
      content: "✉️";
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 48px;
    }

    .letter {
      display: none;
      width: 320px;
      padding: 20px;
      background-color: white;
      border: 2px solid #000;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
      animation: fadeIn 0.5s ease-in;
      font-size: 18px;
      font-family: "Courier New", monospace;
      line-height: 1.4;
      border-radius: 10px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      color: #8b4513;
      margin-bottom: 10px;
    }

    p {
      color: #333;
    }
  </style>
</head>

<body>
  <div class="envelope" onclick="openLetter()"></div>

  <div id="letter" class="letter">
    <h1>Uy, marunong na ako mag-code!</h1>
    <p>Hello JANNA ATIENZA AT MIKYLLA ROSAS, miss ko na kayo 💌</p>
  </div>

  <script>
    function openLetter() {
      const envelope = document.querySelector(".envelope");
      const letter = document.getElementById("letter");

      envelope.style.display = "none";
      letter.style.display = "block";
    }
  </script>
</body>
</html>
