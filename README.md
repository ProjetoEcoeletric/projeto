<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Projeto EcoEletric</title>
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
      padding: 30px 20px;
      color: white;
    }

    header img {
      max-width: 300px;
      margin-bottom: 10px;
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
      margin: 5px auto;
      background-color: #00796b;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      width: 60%;
      transition: background-color 0.3s ease;
    }

    .quiz-option:hover {
      background-color: #004d40;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 1.5rem;
      }

      .buttons {
        flex-direction: column;
      }

      .quiz-option {
        width: 90%;
      }
    }
  </style>
</head>
<body>

  <header>
    <img src="ideia de logo.png" alt="Logotipo EcoEletric">
    <h1>EcoEletric - Conscientização sobre o Lixo Eletrônico</h1>
  </header>

  <section>
    <h2>O que é lixo eletrônico?</h2>
    <p>O lixo eletrônico é formado por dispositivos descartados como celulares, computadores, TVs, baterias, carregadores, cabos e eletrodomésticos. Esses materiais contêm metais pesados como mercúrio e chumbo, que causam contaminação no solo e na água.</p>
  </section>

  <section>
    <h2>Como separar e descartar corretamente?</h2>
    <ul>
      <li><strong>Separe:</strong> Não misture lixo eletrônico com lixo orgânico ou reciclável comum.</li>
      <li><strong>Descarte:</strong> Leve os itens para postos de coleta, cooperativas ou empresas de reciclagem autorizadas.</li>
      <li><strong>Importância:</strong> A reciclagem reduz o impacto ambiental e permite o reaproveitamento de metais raros.</li>
    </ul>
  </section>

  <section>
    <h2>📹 Vídeo explicativo sobre o problema:</h2>
    <div class="map-container">
      <iframe src="https://www.youtube.com/embed/naAnmcR2u6M" title="Lixo Eletrônico" allowfullscreen></iframe>
    </div>
  </section>

  <section class="quiz-container">
    <h2>🧑‍🏫 Quiz Interativo</h2>
    <p class="quiz-question">O que é considerado lixo eletrônico?</p>
    <button class="quiz-option" onclick="checkAnswer('errado')">Papel e Plástico</button>
    <button class="quiz-option" onclick="checkAnswer('certo')">Computadores e Celulares</button>
    <button class="quiz-option" onclick="checkAnswer('errado')">Latas e Garrafas</button>
    <p id="quiz-feedback"></p>
  </section>

  <section>
    <h2>📍 Locais de Descarte Próximos</h2>
    <div class="map-container">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!..." loading="lazy"></iframe>
    </div>
  </section>

  <section>
    <h2>📨 Denuncie descarte irregular</h2>
    <form>
      <input type="text" placeholder="Seu nome" required>
      <input type="email" placeholder="Seu e-mail" required>
      <textarea rows="5" placeholder="Descreva o local ou problema..." required></textarea>
      <button type="submit">Enviar denúncia</button>
    </form>
  </section>

  <script>
    function checkAnswer(answer) {
      const feedback = document.getElementById('quiz-feedback');
      if (answer === 'certo') {
        feedback.textContent = "✅ Parabéns! Resposta correta.";
        feedback.style.color = "green";
      } else {
        feedback.textContent = "❌ Resposta incorreta. Tente novamente!";
        feedback.style.color = "red";
      }
    }
  </script>

</body>
</html>
