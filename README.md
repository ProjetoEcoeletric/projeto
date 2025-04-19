<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Projeto EcoEletric</title>

  <!-- FontAwesome for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f5f5f5;
      margin: 0;
      padding: 0;
    }

    header {
      text-align: center;
      background-color: #005a4f;
      padding: 20px;
      color: white;
    }

    header img {
      max-width: 300px;
      margin-bottom: 10px;
    }

    header h1 {
      margin-top: 10px;
      font-size: 2rem;
    }

    section {
      max-width: 900px;
      margin: 40px auto;
      padding: 20px;
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    h2 {
      color: #005a4f;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin: 20px 0;
    }

    .buttons button {
      padding: 10px 20px;
      background-color: #00796b;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .buttons button:hover {
      transform: scale(1.1);
    }

    .map-container {
      display: flex;
      justify-content: center;
      margin-top: 20px;
    }

    iframe {
      width: 90%;
      max-width: 600px;
      height: 350px;
      border: none;
      border-radius: 10px;
    }

    form {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }

    form input, form textarea {
      width: 90%;
      max-width: 500px;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }

    form button {
      padding: 10px 20px;
      background-color: #00796b;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    /* Quiz styling */
    .quiz-container {
      margin-top: 30px;
      text-align: center;
    }

    .quiz-question {
      font-size: 1.2rem;
      margin-bottom: 10px;
    }

    .quiz-option {
      display: block;
      margin: 5px;
      background-color: #00796b;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
    }

    .quiz-option:hover {
      background-color: #004d40;
    }

    /* Responsive Design */
    @media (max-width: 600px) {
      header h1 {
        font-size: 1.5rem;
      }

      .buttons {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>

  <header>
    <img src="ideia de logo.png" alt="Logo EcoEletric" />
    <h1>EcoEletric - Conscientização sobre o Lixo Eletrônico</h1>
  </header>

  <section>
    <h2>O que é lixo eletrônico?</h2>
    <p>O lixo eletrônico é composto por dispositivos eletrônicos descartados, como celulares, computadores, TVs, cabos, baterias, entre outros...</p>
  </section>

  <section>
    <h2>Como separar e descartar corretamente?</h2>
    <ul>
      <li><strong>Separe:</strong> Não misture lixo eletrônico com lixo comum...</li>
    </ul>
  </section>

  <section>
    <h2>📹 Assista ao vídeo sobre Lixo Eletrônico:</h2>
    <div class="video-container">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/somevideoid" title="Lixo Eletrônico" allowfullscreen></iframe>
    </div>
  </section>

  <section>
    <h2>🧑‍🏫 Quiz Interativo sobre Lixo Eletrônico</h2>
    <div class="quiz-container">
      <p class="quiz-question">O que é considerado lixo eletrônico?</p>
      <button class="quiz-option" onclick="checkAnswer('errado')">Papel e Plástico</button>
      <button class="quiz-option" onclick="checkAnswer('certo')">Computadores e Celulares</button>
      <button class="quiz-option" onclick="checkAnswer('errado')">Latas e Garrafas</button>
    </div>
    <p id="quiz-feedback"></p>
  </section>

  <section>
    <h2>📍 Locais de Descarte Próximos</h2>
    <div class="map-container">
      <iframe src="https://www.google.com/maps/embed?pb=..." allowfullscreen="" loading="lazy"></iframe>
    </div>
  </section>

  <section id="formulario">
    <h2>📨 Contato / Denúncia de Descarte Irregular</h2>
    <form>
      <input type="text" placeholder="Seu nome" required />
      <input type="email" placeholder="Seu e-mail" required />
      <textarea rows="5" placeholder="Descreva o local ou problema..." required></textarea>
      <button type="submit">Enviar</button>
    </form>
  </section>

  <script>
    function checkAnswer(answer) {
      let feedback = document.getElementById('quiz-feedback');
      if (answer === 'certo') {
        feedback.textContent = "Parabéns! Resposta correta.";
        feedback.style.color = "green";
      } else {
        feedback.textContent = "Resposta incorreta. Tente novamente!";
        feedback.style.color = "red";
      }
    }
  </script>

</body>
</html>
