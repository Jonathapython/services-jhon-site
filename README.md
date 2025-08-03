<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Services JHON | Soluções em Segurança e Tecnologia</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    /* Reset & Base */
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      font-family: 'Poppins', sans-serif;
    }
    body {
      background: #f5f7fa;
      color: #333;
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    a {
      text-decoration: none;
      color: #1e88e5;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #1565c0;
    }

    /* Header */
    header {
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: white;
      padding: 60px 20px 80px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    header::after {
      content: '';
      position: absolute;
      top: -30%;
      left: -30%;
      width: 160%;
      height: 160%;
      background: radial-gradient(circle, rgba(255,255,255,0.15) 30%, transparent 70%);
      animation: pulse 10s ease-in-out infinite alternate;
      border-radius: 50%;
      z-index: 0;
    }
    @keyframes pulse {
      0% { transform: scale(1) translate(0,0); opacity: 0.7; }
      100% { transform: scale(1.2) translate(10px, 10px); opacity: 0.4; }
    }
    header .header-content {
      position: relative;
      z-index: 1;
      max-width: 720px;
      margin: 0 auto;
    }
    header h1 {
      font-weight: 700;
      font-size: 3.5rem;
      margin-bottom: 20px;
      letter-spacing: 2px;
      text-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    header p {
      font-size: 1.4rem;
      margin-bottom: 30px;
      font-weight: 500;
      text-shadow: 0 2px 8px rgba(0,0,0,0.2);
    }
    .btn-primary {
      background: #25d366;
      color: white;
      padding: 15px 40px;
      border-radius: 50px;
      font-weight: 600;
      font-size: 1.1rem;
      box-shadow: 0 8px 15px rgba(37, 211, 102, 0.4);
      cursor: pointer;
      border: none;
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
      display: inline-block;
    }
    .btn-primary:hover, .btn-primary:focus {
      background-color: #1ebe57;
      box-shadow: 0 10px 20px rgba(30, 190, 87, 0.7);
      outline: none;
    }

    /* Nav */
    nav {
      background: #2a5298;
      display: flex;
      justify-content: center;
      gap: 40px;
      padding: 20px 10px;
      font-weight: 600;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      user-select: none;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    nav a {
      color: white;
      font-size: 1.1rem;
      padding-bottom: 4px;
      border-bottom: 2px solid transparent;
      transition: border-color 0.3s ease;
    }
    nav a:hover, nav a.active {
      border-bottom-color: #25d366;
      color: #25d366;
    }

    /* Main content */
    main {
      flex: 1;
      max-width: 1000px;
      margin: 60px auto 80px;
      padding: 0 20px;
    }

    h2.section-title {
      text-align: center;
      margin-bottom: 50px;
      font-size: 2.8rem;
      font-weight: 700;
      color: #1e3c72;
      letter-spacing: 1.5px;
    }

    /* Quem Somos */
    #quem-somos {
      background: white;
      padding: 40px 50px;
      border-radius: 20px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
      margin-bottom: 70px;
      color: #222;
      line-height: 1.7;
      font-size: 1.15rem;
    }
    #quem-somos h2 {
      margin-bottom: 20px;
      font-size: 2.6rem;
      font-weight: 700;
      color: #1e3c72;
      text-align: center;
      letter-spacing: 1.2px;
    }

    /* Cards Serviços */
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 40px;
      margin-bottom: 60px;
    }
    .card {
      background: white;
      padding: 30px 25px;
      border-radius: 20px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
      cursor: pointer;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      user-select: none;
    }
    .card:hover, .card:focus {
      transform: translateY(-10px);
      box-shadow: 0 30px 45px rgba(0,0,0,0.15);
      outline: none;
    }
    .card h3 {
      font-size: 1.8rem;
      color: #1e3c72;
      margin-bottom: 15px;
      font-weight: 700;
    }
    .card p {
      font-size: 1.1rem;
      color: #555;
      line-height: 1.5;
    }

    /* Detalhes Serviço */
    #detalhes-servico {
      max-width: 1000px;
      margin: 0 auto 80px;
      background: white;
      border-radius: 20px;
      padding: 40px 50px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.1);
      font-size: 1.3rem;
      color: #222;
      transition: opacity 0.5s ease;
      user-select: text;
    }
    #detalhes-servico h3 {
      font-weight: 700;
      font-size: 2.5rem;
      margin-bottom: 20px;
      color: #1e3c72;
      letter-spacing: 1.1px;
    }
    #detalhes-servico p {
      line-height: 1.7;
      color: #444;
    }

    /* Contato */
    #contato {
      text-align: center;
      padding: 60px 20px 40px;
      background: #1e3c72;
      color: white;
      border-radius: 20px;
      max-width: 800px;
      margin: 0 auto 80px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.15);
    }
    #contato h2 {
      font-size: 2.8rem;
      font-weight: 700;
      margin-bottom: 30px;
      letter-spacing: 1.3px;
    }
    #contato p {
      font-size: 1.3rem;
      margin-bottom: 15px;
      font-weight: 500;
    }
    #contato a {
      color: #25d366;
      font-weight: 700;
      font-size: 1.4rem;
    }
    #contato a:hover, #contato a:focus {
      text-decoration: underline;
      outline: none;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 30px 20px;
      color: #999;
      font-size: 0.95rem;
      background: #222e50;
      user-select: none;
      letter-spacing: 0.5px;
    }

    /* WhatsApp Flutuante */
    .whatsapp-float {
      position: fixed;
      width: 60px; height: 60px;
      bottom: 30px; right: 30px;
      background-color: #25d366;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 32px;
      box-shadow: 0 5px 15px rgba(37, 211, 102, 0.6);
      transition: background-color 0.3s ease;
      z-index: 10000;
      cursor: pointer;
      user-select: none;
    }
    .whatsapp-float:hover {
      background-color: #1ebe57;
    }
    .whatsapp-float svg {
      width: 32px; height: 32px;
    }

    /* Responsividade */
    @media (max-width: 768px) {
      header h1 {
        font-size: 2.5rem;
      }
      header p {
        font-size: 1.2rem;
      }
      main {
        margin: 40px 15px 60px;
      }
      .cards {
        grid-template-columns: 1fr;
        gap: 25px;
      }
      #detalhes-servico {
        padding: 30px 20px;
        font-size: 1.1rem;
      }
      #contato {
        font-size: 1.1rem;
        padding: 40px 15px 30px;
      }
      #quem-somos {
        padding: 25px 20px;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

<header role="banner">
  <div class="header-content">
    <h1>Services JHON</h1>
    <p>Soluções em Segurança Eletrônica, CFTV e Redes</p>
    <a href="#contato" class="btn-primary" aria-label="Solicitar orçamento via contato">Solicite um Orçamento</a>
  </div>
</header>

<!-- Quem Somos -->
<section id="quem-somos" aria-labelledby="quem-somos-title">
  <h2 id="quem-somos-title">Quem Somos</h2>
  <p>A <strong>SERVICES JHON</strong> é uma empresa especializada na prestação de serviços em cabeamento estruturado, instalação de sistemas de CFTV, montagem de rack e soluções de alarme de segurança.</p>
  <p>Com profissionais capacitados e atendimento personalizado, garantimos qualidade, segurança e confiabilidade em todos os nossos projetos, sempre alinhados às necessidades do cliente.</p>
</section>

<nav role="navigation" aria-label="Menu principal">
  <a href="#servicos" class="nav-link active" data-service="0">Instalação de Câmeras</a>
  <a href="#servicos" class="nav-link" data-service="1">Cabeamento Estruturado</a>
  <a href="#servicos" class="nav-link" data-service="2">Montagem de Racks</a>
</nav>

<main>
  <section id="servicos" aria-labelledby="servicos-title">
    <h2 id="servicos-title" class="section-title">Nossos Serviços</h2>

    <div class="cards" role="list" aria-label="Lista de serviços">
      <article class="card" tabindex="0" role="listitem" data-service="0" aria-describedby="desc0">
        <h3>Instalação de Câmeras (CFTV)</h3>
        <p id="desc0">Sistemas modernos com gravação, acesso remoto e monitoramento profissional.</p>
      </article>
      <article class="card" tabindex="0" role="listitem" data-service="1" aria-describedby="desc1">
        <h3>Cabeamento Estruturado</h3>
        <p id="desc1">Infraestrutura de rede organizada, cabeamento de alta performance e certificação.</p>
      </article>
      <article class="card" tabindex="0" role="listitem" data-service="2" aria-describedby="desc2">
        <h3>Montagem de Racks</h3>
        <p id="desc2">Organização de racks com switches, patch panels, roteadores e nobreaks.</p>
      </article>
    </div>

    <div id="detalhes-servico" aria-live="polite" aria-atomic="true">
      <h3>Instalação de Câmeras (CFTV)</h3>
      <p>Oferecemos sistemas modernos com gravação em alta definição, acesso remoto via aplicativo e monitoramento profissional 24 horas para garantir a segurança do seu patrimônio.</p>
    </div>
  </section>

  <section id="contato" aria-labelledby="contato-title">
    <h2 id="contato-title">Contato</h2>
    <p>📞 WhatsApp: <a href="https://wa.me/5511933043059" target="_blank" rel="noopener noreferrer">(11) 93304-3059</a></p>
    <p>📧 E-mail: <a href="jonathaprogramador@gmail.com">jonathaprogramador@gmail.com</a></p>
    <p>📍 Atendemos empresas, condomínios e comércios em toda a região</p>
  </section>
</main>

<footer role="contentinfo">
  <p>&copy; 2025 Services JHON. Todos os direitos reservados.</p>
</footer>

<!-- WhatsApp flutuante -->
<a href="https://wa.me/5511933043059" target="_blank" class="whatsapp-float" aria-label="Contato WhatsApp">
  <svg xmlns="http://www.w3.org/2000/svg" fill="white" viewBox="0 0 24 24"><path d="M20.52 3.48a11.93 11.93 0 0 0-16.91 0 11.93 11.93 0 0 0-3.57 8.48c0 2.11.55 4.17 1.6 6L2 21l3.94-1.63a11.92 11.92 0 0 0 5.58 1.48c6.63 0 12-5.37 12-12 0-3.22-1.26-6.23-3.56-8.37Zm-7.92 15.25a9.82 9.82 0 0 1-5.29-1.52l-.38-.24-2.94 1.21 1.24-2.89-.25-.37a9.81 9.81 0 0 1-1.53-5.3 9.82 9.82 0 0 1 9.82-9.82 9.81 9.81 0 0 1 6.95 2.88 9.82 9.82 0 0 1 2.88 6.94 9.81 9.81 0 0 1-9.82 9.83Zm5.42-7.1-1.2-.59c-.16-.08-.36-.11-.53-.03a3.9 3.9 0 0 0-1.62 1.2 4.72 4.72 0 0 1-2.2-1.31 4.32 4.32 0 0 1-1.31-2.21 3.9 3.9 0 0 0 1.2-1.62c.09-.18.05-.39-.03-.55l-.6-1.19c-.17-.33-.49-.57-.88-.57a.91.91 0 0 0-.62.24 4.94 4.94 0 0 0-1.42 3.5c0 1.14.9 3.27 3.36 5.73s4.61 3.42 5.73 3.36a4.94 4.94 0 0 0 3.5-1.42.91.91 0 0 0 .23-.63c0-.39-.23-.71-.57-.87Z"/></svg>
</a>

<script>
  const cards = document.querySelectorAll('.card');
  const detalhes = document.getElementById('detalhes-servico');
  const navLinks = document.querySelectorAll('nav a');

  const detalhesTexto = [
    {
      title: "Instalação de Câmeras (CFTV)",
      desc: "Oferecemos sistemas modernos com gravação em alta definição, acesso remoto via aplicativo e monitoramento profissional 24 horas para garantir a segurança do seu patrimônio."
    },
    {
      title: "Cabeamento Estruturado",
      desc: "Executamos infraestrutura de rede organizada, com cabeamento de alta performance e certificação para garantir velocidade e estabilidade na sua conexão."
    },
    {
      title: "Montagem de Racks",
      desc: "Realizamos a organização de racks com switches, patch panels, roteadores e nobreaks, assegurando eficiência e facilidade na manutenção da sua rede."
    }
 
