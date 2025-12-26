<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dalvan | Desenvolvedor</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

  body {
    margin: 0;
    padding: 0;
    font-family: 'Roboto', sans-serif;
    background: linear-gradient(120deg, #1f1c2c, #928dab);
    color: #fff;
    overflow-x: hidden;
  }

  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    text-align: center;
    padding: 20px;
  }

  h1 {
    font-size: 3rem;
    margin-bottom: 0.5rem;
    animation: fadeInDown 1s ease-out forwards;
  }

  p {
    font-size: 1.2rem;
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease-out forwards;
  }

  .tech-icons img {
    width: 50px;
    margin: 0 10px;
    transition: transform 0.3s ease;
  }

  .tech-icons img:hover {
    transform: scale(1.3) rotate(15deg);
  }

  @keyframes fadeInDown {
    0% { opacity: 0; transform: translateY(-50px);}
    100% { opacity: 1; transform: translateY(0);}
  }

  @keyframes fadeInUp {
    0% { opacity: 0; transform: translateY(50px);}
    100% { opacity: 1; transform: translateY(0);}
  }

  /* Partículas animadas */
  .particles {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    overflow: hidden;
  }

  .particle {
    position: absolute;
    border-radius: 50%;
    background: rgba(255,255,255,0.6);
    animation: float 6s linear infinite;
  }

  @keyframes float {
    0% { transform: translateY(100vh) scale(0.5);}
    50% { transform: translateY(50vh) scale(1);}
    100% { transform: translateY(-10vh) scale(0);}
  }
</style>
</head>
<body>

<div class="particles"></div>

<div class="container">
  <h1>👋 Olá, eu sou Dalvan!</h1>
  <p>💻 Desenvolvedor em aprendizado constante</p>
  <p>🚀 Focado em desenvolvimento web e lógica de programação</p>

  <h2>Tecnologias que estou aprendendo</h2>
  <div class="tech-icons">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JS">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python">
  </div>

  <p>✨ “Errar faz parte do processo, aprender com o erro é o que faz o programador.”</p>
</div>

<script>
  // Criando partículas animadas
  const particlesContainer = document.querySelector('.particles');

  for (let i = 0; i < 50; i++) {
    const particle = document.createElement('div');
    particle.classList.add('particle');
    particle.style.width = Math.random() * 10 + 5 + 'px';
    particle.style.height = particle.style.width;
    particle.style.left = Math.random() * window.innerWidth + 'px';
    particle.style.animationDuration = 4 + Math.random() * 4 + 's';
    particle.style.background = `rgba(255,255,255,${Math.random()})`;
    particlesContainer.appendChild(particle);
  }
</script>

</body>
</html>
