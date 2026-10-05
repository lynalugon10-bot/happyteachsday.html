<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Happy Teacher's Day Sir</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #050505;
      color: white;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .card {
      width: 90%;
      max-width: 420px;
      padding: 30px;
      text-align: center;
      background: rgba(20,20,20,0.95);
      border: 1px solid #444;
      border-radius: 25px;
      box-shadow: 0 0 40px rgba(255,255,255,0.12);
      animation: appear 1.2s ease;
    }

    @keyframes appear {
      from {
        opacity: 0;
        transform: translateY(40px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    h1 {
      font-size: 28px;
      letter-spacing: 2px;
    }

    .subtitle {
      color: #aaa;
      margin-bottom: 25px;
    }

    .letter {
      text-align: left;
      line-height: 1.7;
      color: #ddd;
      min-height: 250px;
    }

    button {
      margin-top: 20px;
      padding: 12px 25px;
      border: 1px solid white;
      border-radius: 30px;
      background: transparent;
      color: white;
      font-size: 15px;
    }

    button:active {
      background: white;
      color: black;
    }

    .footer {
      margin-top: 20px;
      font-size: 9px;
      letter-spacing: 3px;
      color: #777;
    }
  </style>
</head>

<body>

  <div class="card">

    <h1>🎓 Happy Teacher's Day</h1>

    <div class="subtitle">
      To our amazing Sir
    </div>

    <div class="letter" id="letter">
      Click the button below to open my message.
    </div>

    <button onclick="showLetter()">
      Open Message 💌
    </button>

    <div class="footer">
      MADE WITH CODE • FROM YOUR STUDENT
    </div>

  </div>

  <script>

    const message = `
Dear Sir,

Happy Teacher's Day! 🎉

Thank you for your patience, guidance,
and all the lessons you have taught us.

Hindi lang po lessons ang itinuro ninyo
sa amin, kundi pati ang pagiging
responsable, matiyaga, at hindi
sumusuko kapag nahihirapan.

We may not always say it,
but we truly appreciate your effort
and sacrifices as our teacher.

Thank you for believing in us
and for continuing to guide us.

Happy Teacher's Day, Sir! ❤️

Keep inspiring students
and keep being an amazing teacher.

— From your student, LynxDta
`;

    function showLetter() {

      const letter = document.getElementById("letter");

      letter.innerHTML = "";

      let i = 0;

      function typeWriter() {

        if (i < message.length) {

          if (message[i] === "\n") {
            letter.innerHTML += "<br>";
          } else {
            letter.innerHTML += message[i];
          }

          i++;

          setTimeout(typeWriter, 25);
        }
      }

      typeWriter();
    }

  </script>

</body>
</html>
