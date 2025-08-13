<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Site Fofo para Meu Namorado</title>
  <style>
    /* Cores em tons pasteis claros */
    :root {
      --cor-fundo: #f9f7f7;
      --cor-caixa: #f0e6f6;
      --cor-botao: #c4aead;
      --cor-coracao: #f4c4c4;
      --cor-texto: #6e6a70;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--cor-fundo);
      color: var(--cor-texto);
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px;
    }

    h1 {
      margin-bottom: 10px;
      font-weight: 600;
    }

    .text-container {
      background-color: var(--cor-caixa);
      border-radius: 12px;
      padding: 15px;
      width: 320px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 30px;
    }

    textarea {
      width: 100%;
      min-height: 80px;
      border: none;
      border-radius: 10px;
      padding: 10px;
      font-size: 16px;
      resize: vertical;
      background-color: #f7f0fa;
      color: var(--cor-texto);
      box-shadow: inset 1px 1px 5px #d6cbe1;
      font-family: inherit;
      outline: none;
    }

    textarea::placeholder {
      color: #bfb7c8;
    }

    button {
      margin-top: 15px;
      background-color: var(--cor-botao);
      border: none;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 3px 6px rgba(0,0,0,0.12);
      transition: background-color 0.3s ease;
      position: relative;
    }

    button:hover {
      background-color: #d3b6be;
    }

    button:active {
      transform: scale(0.95);
    }

    /* Coração SVG */
    button svg {
      fill: var(--cor-coracao);
      width: 24px;
      height: 24px;
      transition: fill 0.3s ease;
    }

    button.liked svg {
      fill: #f08080;
    }

    /* Polaroid photos section */
    .polaroid-section {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
      max-width: 700px;
    }

    .polaroid {
      background: white;
      padding: 10px 10px 25px 10px;
      box-shadow: 0 8px 12px rgba(0,0,0,0.15);
      border-radius: 8px;
      width: 150px;
      text-align: center;
      font-size: 14px;
      color: #555;
      font-family: 'Courier New', Courier, monospace;
      transform: rotate(-2deg);
      transition: transform 0.2s ease;
      position: relative;
    }

    .polaroid:hover {
      transform: rotate(0deg) scale(1.05);
      box-shadow: 0 12px 18px rgba(0,0,0,0.25);
      z-index: 10;
    }

    .polaroid img {
      width: 100%;
      border-radius: 5px;
      display: block;
      margin-bottom: 8px;
    }

  </style>
</head>
<body>
  <h1>Para Meu Amor 💖</h1>

  <div class="text-container">
    <textarea id="mensagem" placeholder="Escreva um textinho fofo aqui..."></textarea>
    <button id="btn-coracao" aria-label="Curtir">
      <svg viewBox="0 0 24 24" >
        <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42
        4.42 3 7.5 3c1.74 0 3.41 0.81 4.5 2.09
        C13.09 3.81 14.76 3 16.5 3
        19.58 3 22 5.42 22 8.5
        c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
      </svg>
    </button>
  </div>

  <section class="polaroid-section">
    <div class="polaroid" style="transform: rotate(-3deg);">
      <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=150&q=80" alt="Foto 1" />
      <div>Nosso momento</div>
    </div>
    <div class="polaroid" style="transform: rotate(2deg);">
      <img src="https://images.unsplash.com/photo-1494526585095-c41746248156?auto=format&fit=crop&w=150&q=80" alt="Foto 2" />
      <div>Memórias lindas</div>
    </div>
    <div class="polaroid" style="transform: rotate(-1deg);">
      <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=150&q=80" alt="Foto 3" />
      <div>Você e eu</div>
    </div>
  </section>

  <script>
    const btn = document.getElementById('btn-coracao');
    btn.addEventListener('click', () => {
      btn.classList.toggle('liked');
    });
  </script>
</body>
</html>
