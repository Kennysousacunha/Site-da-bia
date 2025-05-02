<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para Bia, com amor</title>

  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>

  <style>
  	.heart-btn {
  background-color: #ff85a2;
  border: none;
  color: white;
  font-size: 2rem;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  cursor: pointer;
  transition: transform 0.2s ease;
  position: relative;
  box-shadow: 0 0 10px #ff85a2aa;
}

.heart-btn:hover {
  transform: scale(1.2);
}

.heart-explosao {
  position: absolute;
  top: -40px;
  left: 50%;
  transform: translateX(-50%);
  background: #fff0f5;
  color: #d6336c;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
  animation: pop 0.6s ease-out, fadeOut 1.4s ease forwards;
  white-space: nowrap;
  z-index: 999;
  box-shadow: 0 0 8px #ff85a2aa;
}

@keyframes pop {
  0% { transform: translateX(-50%) scale(0.5); opacity: 0; }
  50% { transform: translateX(-50%) scale(1.2); opacity: 1; }
  100% { transform: translateX(-50%) scale(1); opacity: 1; }
}

@keyframes fadeOut {
  0% { opacity: 1; }
  100% { opacity: 0; transform: translateX(-50%) translateY(-50px); }
}

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #0d1b2a, #1b263b);
      color: #fff;
    }

    section {
      padding: 3rem 2rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      animation: fadeIn 1.5s ease;
      position: relative;
    }

    h1 {
      font-size: 3rem;
      color: #ff85a2;
      margin-bottom: 1rem;
      padding:1
    }

    p, li {
      font-size: 1.2rem;
      max-width: 800px;
      margin-bottom: 0.7rem;
    }

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: #1b263b;
      padding: 1rem;
      text-align: center;
      z-index: 1000;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    nav a {
      margin: 0 1rem;
      text-decoration: none;
      color: #ff85a2;
      font-weight: bold;
    }

    footer {
      background: #1b263b;
      padding: 2rem;
      text-align: center;
      font-size: 1rem;
      color: #888;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    button {
      background-color: #ff85a2;
      color: white;
      border: none;
      padding: 1rem 2rem;
      border-radius: 25px;
      font-size: 1rem;
      cursor: pointer;
    }

    button:hover {
      background-color: #e3607c;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    .star {
      position: fixed;
      width: 4px;
      height: 4px;
      background: white;
      border-radius: 50%;
      animation: twinkle 8s infinite ease-in-out;
    }

    @keyframes twinkle {
      0% { opacity: 0.2; transform: translateY(0); }
      50% { opacity: 1; transform: translateY(-50vh); }
      100% { opacity: 0; transform: translateY(-100vh); }
    }
    @keyframes subir {
  0% { transform: translateY(0); opacity: 0.8; }
  50% { opacity: 1; }
  100% { transform: translateY(-120vh); opacity: 0; }
}

.coracao {
  position: fixed;
  color: pink;
  font-size: 1.5rem;
  animation: subir 6s ease-in-out forwards;
  pointer-events: none;
}
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

#musicas-para-bia {
  animation: fadeInUp 1.5s ease;
}
#nossos-sonhos {
  background-color: #0d1b2a;
  padding: 3rem 2rem;
  text-align: center;
  animation: fadeIn 1.5s ease;
}

.sonhos-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
}

.sonho {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 15px;
  padding: 1.2rem;
  width: 180px;
  transition: transform 0.3s ease, background 0.3s ease;
  animation: flutuar 4s infinite ease-in-out;
}

.sonho:hover {
  transform: scale(1.08);
  background: rgba(255, 255, 255, 0.08);
}

.sonho img {
  width: 50px;
  margin-bottom: 0.7rem;
}

.sonho span {
  font-size: 1rem;
  color: #ffb6c1;
  font-weight: bold;
}

@keyframes flutuar {
  0% { transform: translateY(0); }
  50% { transform: translateY(-6px); }
  100% { transform: translateY(0); }
}
/* Estrelas flutuando no fundo da seção de sonhos */
#nossos-sonhos {
  position: relative;
  background: linear-gradient(180deg, #0d1b2a, #1b263b);
  overflow: hidden;
  transition: background 2s ease;
}

/* Estrelas específicas da seção */
#nossos-sonhos .estrela {
  position: absolute;
  width: 4px;
  height: 4px;
  background: white;
  border-radius: 50%;
  animation: brilhoEstrela 6s infinite ease-in-out;
  opacity: 0.8;
  z-index: 0;
}

@keyframes brilhoEstrela {
  0% { transform: translateY(0); opacity: 0.3; }
  50% { transform: translateY(-40px); opacity: 1; }
  100% { transform: translateY(-80px); opacity: 0; }
}
/* Corações subindo */
.coracao-subindo {
  position: fixed;
  bottom: 0;
  font-size: 2rem;
  color: #ff85a2;
  animation: subir 4s linear forwards;
  z-index: 9999;
}

/* Frases caindo */
.frase-cascata {
  position: fixed;
  top: -50px;
  font-size: 1.2rem;
  color: #ffd6e0;
  animation: cair 5s ease-in forwards;
  z-index: 9999;
}

@keyframes subir {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-100vh); opacity: 0; }
}

@keyframes cair {
  0% { transform: translateY(0); opacity: 0; }
  100% { transform: translateY(100vh); opacity: 1; }
}


@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
h1 {
  font-size: 2.8rem;
  color: #ff85a2;
  margin-bottom: 1rem;
  animation: heartbeat 2s infinite;
  text-shadow: 0 0 15px #ffbfd6;
}

@keyframes heartbeat {
  0% { transform: scale(1); }
  25% { transform: scale(1.05); }
  50% { transform: scale(1); }
  75% { transform: scale(1.05); }
  100% { transform: scale(1); }
}
.heart-button {
  font-size: 2rem;
  background-color: #ff4d6d;
  border: none;
  color: white;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  cursor: pointer;
  position: relative;
  transition: transform 0.2s ease;
  box-shadow: 0 0 10px #ffb3c6;
}

.heart-button:hover {
  transform: scale(1.2);
}

.heart-popup {
  position: absolute;
  top: -50px;
  left: 50%;
  transform: translateX(-50%);
  background-color: white;
  color: #ff4d6d;
  padding: 8px 12px;
  border-radius: 12px;
  font-size: 0.9rem;
  white-space: nowrap;
  animation: pop-up 0.5s ease-out, fade-up 1.5s ease forwards;
  box-shadow: 0 0 8px #ffc1d3;
  z-index: 100;
}

@keyframes pop-up {
  0% { opacity: 0; transform: translateX(-50%) scale(0.5); }
  50% { opacity: 1; transform: translateX(-50%) scale(1.2); }
  100% { transform: translateX(-50%) scale(1); }
}

@keyframes fade-up {
  0% { opacity: 1; }
  100% { opacity: 0; transform: translateX(-50%) translateY(-40px); }
}

  </style>
</head>
<body>

<nav>
  <a href="#inicio">Início</a>
  <a href="#poema">Poema</a>
  <a href="#cartinhas">Cartinhas</a>
  <a href="#promessas">Promessas</a>
  <a href="#motivos">Motivos</a>
  <a href="#musicas-para-bia">Músicas</a>
    <a href="#nossos sonhos">Nossos sonhos</a>
  
</nav>

<section id="inicio">
	
	
  <h1>Para Bia, com amor</h1>
  <p>Esse site é um pedacinho do quanto eu te amo. Cada detalhe aqui é feito com carinho só pra você, Bia.</p>
</section>
<section id="elogios" style="padding: 3rem 1rem; text-align: center;">
  <h2 style="color: #ff4d6d; font-size: 2rem;">Clique nos corações para ver o quanto eu te amo!</h2>
  <div id="heart-container" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 1rem; margin-top: 2rem;">
    <!-- 10 botões -->
    <button class="heart-button" onclick="explodeHeart(this, 'Você é a razão do meu sorriso!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Meu mundo é mais bonito com você!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Você é perfeita do jeitinho que é!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Com você, tudo faz sentido!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Você é minha melhor escolha!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Você é um sonho realizado!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Te amar é fácil demais!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Você é minha princesa linda!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Tudo em você me encanta!')">❤</button>
    <button class="heart-button" onclick="explodeHeart(this, 'Você é meu coração inteirinho!')">❤</button>
  </div>
</section>

<section id="poema">
  <h1>Um poema com flores</h1>
  <p class="poem">
    Em meio a flores, te encontrei,<br>
    Como rosa rara, me encantei.<br>
    Tua presença é jardim em flor,<br>
    Perfume doce, puro amor.<br><br>
    No campo calmo do teu abraço,<br>
    Brotou ternura em cada espaço.<br>
    Tu és a flor que sempre quis,<br>
    Te amar me faz tão feliz.
  </p>
</section>
  <section id="musicas-para-bia">
  <h1>Músicas que sempre canto pra você</h1>
  <div class="refrains">
    <p>
      <strong>Luan Santana – Sinais</strong><br>
      Sinais ,vindos de um lugar tão longe<br>
      Ás vezes se escondem<br>
      No farol, em uma ilha <br>
      Numa noite tão vazia eu beijei você<br>
      Até o amanhecer.
    </p>

    <p>
      <strong>Cleber e Kauan – Sonho</strong><br>
      Oi, tudo bem<br>
      Há quanto tempo eu não te via<br>
      Resolvi te visitar ,nos seus sonhos[..]<br>
      Tava morrendo de saudade<br>
      E logo a gente volta pra realidade 
	 De não estarmos juntos...
    </p>

    <p>
      <strong>Cristiano Araújo – Você Mudou</strong><br>
      E quando despertar não irá me encontrar<br>
      Quem sabe aí, meu bem<br>
      Talvez você consiga entender<br>
      Que a minha vida não pertence a você
    </p>

    <p>
      <strong>Felipe Araújo – Espaçosa demais </strong><br>
     Tem como ser um pouco menos linda?<br>
     Tem como eu ser o dono da minha vida?<br>
     Tem como não ser assim tão perfeita?<br>
     Já tomou meu coração e 'tá subindo pra cabeça
    </p>

    <p>
      <strong>Luan Santana – Chuva de Arroz</strong><br>
      Me apaixonei perdidamente<br>
      E o que eu sei<br>
      É que daqui pra frente<br>
      Vai ser nossa cidade, nosso telefone<br>
      Nosso endereço, nosso apartamento<br>
      Sabe aquela igreja, 'to aqui na frente<br>
      Imaginando chuvas de arroz na gente
    </p>

    <p>
      <strong>Humberto e Ronaldo– Hoje Sonhei com Você</strong><br>
      E quando te beijei você tão linda me abraçou<br>
      E disse assim, sorrindo: bom dia, meu amor<br>
      A minha vida é um sonho por poder te encontrar<br>
      E por você me amar
    </p>

    <p>
      <strong>Zé Neto e Cristiano  – Mulher Maravilha</strong><br>
       Sabe aquele amor que se multiplica<br>
	   Quem nunca sonhou ter isso na vida<br>
		Ser herói de alguém,e melhor ainda<br>
	   Ter do lado a mulher maravilha 
    </p>
<section id="cartinhas">
  <h1>Cartinhas Românticas</h1>
  <p>Clique nas cartinhas para ler o que sinto por você...</p>
  <div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin-top: 1.5rem;">
    <img src="https://cdn-icons-png.flaticon.com/512/561/561127.png" alt="Cartinha 1" width="60" style="cursor: pointer;" onclick="mostrarCarta(1)">
    <img src="https://cdn-icons-png.flaticon.com/512/561/561127.png" alt="Cartinha 2" width="60" style="cursor: pointer;" onclick="mostrarCarta(2)">
    <img src="https://cdn-icons-png.flaticon.com/512/561/561127.png" alt="Cartinha 3" width="60" style="cursor: pointer;" onclick="mostrarCarta(3)">
    <img src="https://cdn-icons-png.flaticon.com/512/561/561127.png" alt="Cartinha 4" width="60" style="cursor: pointer;" onclick="mostrarCarta(4)">
  </div>
</section>
<section id="quiz">
  <h1>Perguntas: Verdadeiro ou Falso</h1>
  <div class="quiz-question">
    <p>1. Começamos a namorar em dezembro.</p>
    <button onclick="resposta(this, true)">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>2. O nome da minha gata que eu amo é Maria.</p>
    <button onclick="resposta(this, true)">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>3. Quem é mais romântico na relação é você.</p>
    <button onclick="resposta(this, true)">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>4. Quem tem que ser menos ciumenta é você.</p>
    <button onclick="resposta(this, true)">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>5. Luan Santana é o nosso cantor favorito.</p>
    <button onclick="resposta(this, true)">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>6. A música "Amar Não É Pecado" é uma das mais românticas do Luan Santana.</p>
    <button onclick="resposta(this, true, 'Mais um “eu te amo”!')">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>7. “Te Esperando” fala de um amor que nunca desiste.</p>
    <button onclick="resposta(this, true, 'Você merece um elogio: linda, fofa e perfeita!')">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>8. “Sinais” é uma música triste do Luan Santana.</p>
    <button onclick="resposta(this, false)">Verdadeiro</button>
    <button onclick="resposta(this, true)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>9. “Escreve Aí” é sobre um amor impossível.</p>
    <button onclick="resposta(this, false)">Verdadeiro</button>
    <button onclick="resposta(this, true)">Falso</button>
  </div>

  <div class="quiz-question">
    <p>10. Em “Acordando o Prédio”, o amor é vivido com leveza e diversão.</p>
    <button onclick="resposta(this, true, 'Estrela cadente: BIA')">Verdadeiro</button>
    <button onclick="resposta(this, false)">Falso</button>
  </div>
</section>

<script>
  function mostrarCartinha(id) {
    let cartinhas = {
      cartinha1: "Bia, desde que você entrou na minha vida, tudo ganhou mais cor. Seu amor me transforma todos os dias.",
      cartinha2: "Amor, só de pensar em você, meu coração se enche de paz. Obrigado por ser meu abrigo e minha melhor amiga.",
      cartinha3: "Você é minha razão de sorrir, de sonhar e de continuar acreditando em um futuro lindo a dois. Te amo além das palavras."
    };

    Swal.fire({
      title: 'Minha cartinha pra você',
      text: cartinhas[id],
      icon: 'info',
      confirmButtonText: 'Te amo também!',
      confirmButtonColor: '#ff85a2',
      background: '#fff0f5',
      color: '#d6336c'
    });
  }
 
  </div>
</section>

</script>
<section id="promessas">
  <h1>Minhas Promessas pra Você</h1>
  <ul>
    <li>Te apoiar nos seus sonhos sempre.</li>
    <li>Ser seu melhor amigo e namorado todos os dias.</li>
    <li>Te fazer sorrir, mesmo nos dias difíceis.</li>
    <li>Construir um futuro lindo do seu ladinho.</li>
  </ul>
</section>
<section id="nossos-sonhos">
  <h1>Nossos Sonhos Juntos</h1>
  <p>Cada sonho é um pedacinho do nosso futuro. Vamos realizá-los juntinhos?</p>

  <div class="sonhos-container">
    <div class="sonho">
      <img src="https://cdn-icons-png.flaticon.com/512/686/686589.png" alt="Casa dos sonhos">
      <span>Casa do jeitinho da Bia</span>
    </div>
    <div class="sonho">
      <img src="https://cdn-icons-png.flaticon.com/512/892/892458.png" alt="Dormir de conchinha">
      <span>Dormir de conchinha todos os dias</span>
    </div>
    <div class="sonho">
      <img src="https://cdn-icons-png.flaticon.com/512/1146/1146869.png" alt="Filhos">
      <span>Ter nossos filhos</span>
    </div>
    <div class="sonho">
      <img src="https://cdn-icons-png.flaticon.com/512/2424/2424385.png" alt="Show do Luan">
      <span>Ir ao show do Luan Santana</span>
    </div>
    <div class="sonho">
      <img src="https://cdn-icons-png.flaticon.com/512/747/747376.png" alt="Dia coladinho">
      <span>Passar o dia inteiro coladinhos</span>
    </div>
  </div>
</section>
<button onclick="botaoSurpresa()" style="margin-top: 2rem;">Aperte e veja o quanto eu te amo</button>

<section id="motivos" style="position: relative;">
  <h1>10 Motivos para te Amar</h1>
  <ul style="list-style: none; padding: 0; max-width: 800px;">
    <li><span class="heart">❤️</span> Seu sorriso ilumina meu dia.</li>
    <li><span class="heart">❤️</span> Você me entende como ninguém.</li>
    <li><span class="heart">❤️</span> Seu jeitinho carinhoso me conquista sempre.</li>
    <li><span class="heart">❤️</span> Você é minha melhor amiga e amor em um só.</li>
    <li><span class="heart">❤️</span> Seus abraços são meu lugar favorito no mundo.</li>
    <li><span class="heart">❤️</span> Você me inspira a ser uma pessoa melhor.</li>
    <li><span class="heart">❤️</span> Nossos momentos juntos são mágicos.</li>
    <li><span class="heart">❤️</span> Seu olhar me acalma em qualquer situação.</li>
    <li><span class="heart">❤️</span> Você me apoia em tudo, sempre.</li>
    <li><span class="heart">❤️</span> Eu te amo simplesmente por você ser... você!</li>
  </ul>
</section>

<script>
  function resposta(btn, correta, bonus = '') {
    let icon = correta ? 'success' : 'error';
    let title = correta ? 'Acertou!' : 'Errou!';
    let text = correta
      ? (bonus || 'Você me conhece muito bem!')
      : 'Tente lembrar melhor, meu amor.';
    
    if (bonus.includes('Estrela cadente')) {
      const estrela = document.createElement("div");
      estrela.innerText = '★ BIA ★';
      estrela.style.position = "fixed";
      estrela.style.top = "0";
      estrela.style.left = Math.random() * 100 + "vw";
      estrela.style.fontSize = "1.5rem";
      estrela.style.color = "#ffd700";
      estrela.style.animation = "twinkle 3s ease-in-out forwards";
      document.body.appendChild(estrela);
    }

    Swal.fire({
      title: title,
      text: text,
      icon: icon,
      confirmButtonColor: '#ff85a2'
    });
  }
</script>

<footer>
  <p>Feito com todo meu amor, só pra você, Bia.</p>
</footer>

<script>
  function mostrarCarta(num) {
    let mensagens = {
      1: "Meu amor, você é o motivo do meu melhor sorriso todos os dias.",
      2: "Bia, te amar é a certeza mais linda que tenho em minha vida.",
      3: "Você é meu porto seguro, meu colo favorito, minha paz.",
      4: "Nada no mundo se compara ao quanto eu amo estar com você."
    };

    Swal.fire({
      title: 'Minha cartinha pra você',
      text: mensagens[num],
      icon: 'info',
      confirmButtonText: 'Te amo!',
      confirmButtonColor: '#ff85a2',
      background: '#1b263b',
      color: '#fff'
    });
  }

  for (let i = 0; i < 50; i++) {
    const star = document.createElement("div");
    star.className = "star";
    star.style.left = Math.random() * 100 + "vw";
    star.style.animationDuration = (3 + Math.random() * 7) + "s";
    document.body.appendChild(star);
  }
</script>
<script>
setInterval(() => {
  const coracao = document.createElement("div");
  coracao.innerText = "❤";
  coracao.className = "coracao";
  coracao.style.left = Math.random() * 100 + "vw";
  coracao.style.top = "100vh";
  document.body.appendChild(coracao);

  setTimeout(() => coracao.remove(), 7000);
}, 500);
</script>
<script>
function botaoSurpresa() {
  // Estrela popup
  Swal.fire({
    title: 'Incontáveis vezes...',
    text: 'Eu te amo!',
    icon: 'info',
    confirmButtonColor: '#ff85a2'
  });

  // Corações subindo
  for (let i = 0; i < 25; i++) {
    const coracao = document.createElement("div");
    coracao.className = "coracao-subindo";
    coracao.innerText = "❤️";
    coracao.style.left = Math.random() * 100 + "vw";
    coracao.style.animationDuration = (2 + Math.random() * 2) + "s";
    document.body.appendChild(coracao);
    setTimeout(() => coracao.remove(), 4000);
  }

  // Frases românticas em cascata
  const frases = [
    "Você é meu mundo",
    "Te amo mais do que ontem",
    "Minha eterna paixão",
    "Amar você é fácil",
    "Tudo é melhor com você"
  ];

  frases.forEach((frase, i) => {
    setTimeout(() => {
      const f = document.createElement("div");
      f.className = "frase-cascata";
      f.innerText = frase;
      f.style.left = Math.random() * 90 + "vw";
      f.style.animationDuration = (4 + Math.random() * 2) + "s";
      document.body.appendChild(f);
      setTimeout(() => f.remove(), 5000);
    }, i * 300);
  });
}
</script>

<script>
  const containerSonhos = document.querySelector("#nossos-sonhos");

  for (let i = 0; i < 30; i++) {
    const estrela = document.createElement("div");
    estrela.classList.add("estrela");
    estrela.style.left = Math.random() * 100 + "%";
    estrela.style.top = Math.random() * 100 + "%";
    estrela.style.animationDuration = (3 + Math.random() * 4) + "s";
    containerSonhos.appendChild(estrela);
  }
</script>
<script>
  function explodeHeart(button, message) {
    const span = document.createElement("span");
    span.className = "heart-popup";
    span.innerText = message;
    button.appendChild(span);

    setTimeout(() => {
      button.removeChild(span);
    }, 2000);
  }
</script>

</body>
</html>
