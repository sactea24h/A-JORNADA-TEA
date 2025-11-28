<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A Jornada TEA - Guia completo para pais e educadores sobre autismo, inclusão e estratégias práticas.">
  <meta name="keywords" content="autismo, TEA, guia, educação, inclusão, pais, educadores">
  <title>A Jornada TEA - Entendendo, Acolhendo e Agindo</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #9fc5e8;
      --secondary: #c5b6e8;
      --dark: #1e3a8a;
      --light: #f3f4f6;
      --text: #374151;
      --text-light: #6b7280;
      --accent: #f59e0b;
      --success: #10b981;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: var(--text);
      background-color: #FFFFFF;
      overflow-x: hidden;
    }

    /* HEADER / NAVEGAÇÃO */
    header {
      background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
      padding: 15px 0;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    }

    .header-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.5em;
      font-weight: 700;
      color: white;
      text-decoration: none;
      letter-spacing: -0.5px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 30px;
      font-weight: 500;
      transition: all 0.3s;
      font-size: 0.95em;
    }

    nav a:hover {
      opacity: 0.8;
      text-decoration: underline;
    }

    /* HERO SECTION */
    .hero {
      background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
      color: white;
      padding: 120px 20px;
      min-height: 700px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      right: 0;
      width: 400px;
      height: 400px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      transform: translate(100px, -100px);
    }

    .hero::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 300px;
      height: 300px;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 50%;
      transform: translate(-100px, 100px);
    }

    .hero-content {
      max-width: 750px;
      margin: 0 auto;
      text-align: center;
      position: relative;
      z-index: 2;
    }

    .hero h1 {
      font-size: 3.8em;
      margin-bottom: 20px;
      font-weight: 700;
      line-height: 1.2;
      text-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }

    .hero h2 {
      font-size: 1.9em;
      margin-bottom: 30px;
      font-weight: 300;
      opacity: 0.95;
      line-height: 1.3;
    }

    .hero p {
      font-size: 1.15em;
      margin-bottom: 50px;
      line-height: 1.8;
      opacity: 0.9;
    }

    .hero-buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 16px 40px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 600;
      font-size: 1.05em;
      transition: all 0.3s ease;
      border: 2px solid transparent;
      cursor: pointer;
    }

    .btn-primary {
      background-color: white;
      color: var(--primary);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
    }

    .btn-secondary {
      background-color: transparent;
      color: white;
      border: 2px solid white;
    }

    .btn-secondary:hover {
      background-color: white;
      color: var(--primary);
    }

    /* SOCIAL PROOF */
    .social-proof {
      background-color: var(--light);
      padding: 40px 20px;
      text-align: center;
    }

    .social-proof-container {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 30px;
    }

    .proof-item {
      padding: 20px;
    }

    .proof-number {
      font-size: 2.5em;
      font-weight: 700;
      color: var(--primary);
      margin-bottom: 10px;
    }

    .proof-text {
      color: var(--text-light);
      font-size: 0.95em;
    }

    /* SEÇÃO GENÉRICA */
    .section {
      padding: 100px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section-title {
      font-size: 2.8em;
      color: var(--dark);
      text-align: center;
      margin-bottom: 60px;
      font-weight: 700;
      position: relative;
    }

    .section-title::after {
      content: '';
      display: block;
      width: 80px;
      height: 4px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      margin: 20px auto 0;
      border-radius: 2px;
    }

    .section-subtitle {
      font-size: 1.2em;
      color: var(--text-light);
      text-align: center;
      margin-bottom: 50px;
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
    }

    /* VSL SECTION */
    .vsl-section {
      background: linear-gradient(135deg, #f0f9ff 0%, #faf5ff 100%);
    }

    .vsl-container {
      max-width: 900px;
      margin: 0 auto;
    }

    .vsl-video-wrapper {
      background: white;
      border-radius: 16px;
      padding: 30px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
      margin: 40px 0;
    }

    .vsl-placeholder {
      background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
      border-radius: 12px;
      padding: 80px 40px;
      text-align: center;
      color: white;
    }

    .vsl-placeholder p {
      font-size: 1.2em;
      margin-bottom: 10px;
    }

    .vsl-placeholder small {
      opacity: 0.8;
    }

    .vsl-text {
      font-size: 1.1em;
      color: var(--text-light);
      line-height: 1.9;
      margin: 30px 0;
      padding: 30px;
      background: white;
      border-left: 4px solid var(--primary);
      border-radius: 8px;
    }

    /* BENEFÍCIOS */
    .benefits {
      background: white;
    }

    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 40px;
      margin-top: 60px;
    }

    .benefit-card {
      padding: 40px 30px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
      transition: all 0.3s ease;
      border-top: 4px solid transparent;
      border-top-color: var(--primary);
    }

    .benefit-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
    }

    .benefit-icon {
      font-size: 3em;
      margin-bottom: 20px;
      display: block;
    }

    .benefit-card h3 {
      font-size: 1.4em;
      color: var(--dark);
      margin-bottom: 15px;
      font-weight: 600;
    }

    .benefit-card p {
      color: var(--text-light);
      font-size: 1em;
      line-height: 1.7;
    }

    /* DEPOIMENTOS */
    .testimonials {
      background: var(--light);
    }

    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 40px;
      margin-top: 60px;
    }

    .testimonial {
      background: white;
      padding: 40px;
      border-radius: 12px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
      border-left: 5px solid var(--primary);
      transition: all 0.3s ease;
    }

    .testimonial:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
    }

    .star-rating {
      color: var(--accent);
      margin-bottom: 15px;
      font-size: 1.2em;
    }

    .testimonial-text {
      font-size: 1.05em;
      color: var(--text);
      margin-bottom: 20px;
      line-height: 1.8;
      font-style: italic;
    }

    .testimonial-author {
      font-weight: 600;
      color: var(--dark);
      font-size: 0.95em;
    }

    .testimonial-role {
      font-size: 0.85em;
      color: var(--text-light);
      margin-top: 5px;
    }

    /* QUIZ SECTION */
    .quiz-section {
      background: linear-gradient(135deg, #e0e7ff 0%, #f3e8ff 100%);
    }

    .quiz-content {
      max-width: 700px;
      margin: 0 auto;
      text-align: center;
    }

    .quiz-content p {
      font-size: 1.1em;
      color: var(--text-light);
      margin-bottom: 30px;
      line-height: 1.8;
    }

    .quiz-badge {
      display: inline-block;
      background: white;
      color: var(--primary);
      padding: 10px 20px;
      border-radius: 20px;
      font-weight: 600;
      margin-bottom: 20px;
      font-size: 0.9em;
    }

    /* GARANTIA */
    .guarantee-section {
      background: white;
    }

    .guarantee {
      background: linear-gradient(135deg, #fef3c7 0%, #fde68a 100%);
      border-radius: 16px;
      padding: 50px 40px;
      text-align: center;
      max-width: 700px;
      margin: 50px auto;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
    }

    .guarantee h3 {
      font-size: 2em;
      color: var(--dark);
      margin-bottom: 20px;
      font-weight: 700;
    }

    .guarantee p {
      font-size: 1.1em;
      color: var(--text);
      line-height: 1.8;
    }

    /* FAQ SECTION */
    .faq-section {
      background: var(--light);
    }

    .faq-container {
      max-width: 800px;
      margin: 0 auto;
    }

    .faq-item {
      background: white;
      margin-bottom: 20px;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
      transition: all 0.3s ease;
    }

    .faq-item:hover {
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    }

    .faq-question {
      padding: 25px;
      background: white;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-weight: 600;
      color: var(--dark);
      font-size: 1.05em;
      transition: all 0.3s ease;
    }

    .faq-question:hover {
      background: var(--light);
      padding-left: 30px;
    }

    .faq-toggle {
      font-size: 1.5em;
      transition: transform 0.3s ease;
    }

    .faq-item.active .faq-toggle {
      transform: rotate(180deg);
    }

    .faq-answer {
      padding: 0 25px;
      max-height: 0;
      overflow: hidden;
      transition: all 0.3s ease;
      color: var(--text-light);
      line-height: 1.8;
    }

    .faq-item.active .faq-answer {
      padding: 0 25px 25px 25px;
      max-height: 500px;
    }

    /* CTA SECTION */
    .cta-section {
      background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
      color: white;
      text-align: center;
      padding: 100px 20px;
      position: relative;
      overflow: hidden;
    }

    .cta-section::before {
      content: '';
      position: absolute;
      top: 0;
      right: 0;
      width: 500px;
      height: 500px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      transform: translate(100px, -100px);
    }

    .cta-content {
      max-width: 700px;
      margin: 0 auto;
      position: relative;
      z-index: 2;
    }

    .cta-section h2 {
      font-size: 2.8em;
      margin-bottom: 20px;
      font-weight: 700;
      line-height: 1.3;
    }

    .cta-section p {
      font-size: 1.2em;
      margin-bottom: 50px;
      opacity: 0.95;
      line-height: 1.8;
    }

    .urgency-badge {
      display: inline-block;
      background: rgba(255, 255, 255, 0.2);
      color: white;
      padding: 12px 24px;
      border-radius: 20px;
      font-weight: 600;
      margin-bottom: 30px;
      font-size: 0.9em;
      border: 1px solid rgba(255, 255, 255, 0.3);
    }

    /* FOOTER */
    footer {
      background-color: var(--dark);
      color: white;
      padding: 60px 20px 30px;
    }

    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 40px;
      margin-bottom: 40px;
    }

    .footer-section h4 {
      margin-bottom: 20px;
      font-size: 1.1em;
      font-weight: 600;
    }

    .footer-section ul {
      list-style: none;
    }

    .footer-section ul li {
      margin-bottom: 12px;
    }

    .footer-section a {
      color: #e0e7ff;
      text-decoration: none;
      transition: color 0.3s;
      font-size: 0.95em;
    }

    .footer-section a:hover {
      color: white;
    }

    .footer-copyright {
      border-top: 1px solid #3730a3;
      padding-top: 30px;
      text-align: center;
      color: #c7d2fe;
      font-size: 0.9em;
    }

    /* RESPONSIVIDADE */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.5em;
      }

      .hero h2 {
        font-size: 1.4em;
      }

      .hero {
        padding: 80px 20px;
        min-height: 500px;
      }

      .hero-buttons {
        flex-direction: column;
      }

      .btn {
        width: 100%;
      }

      .section-title {
        font-size: 2em;
      }

      nav {
        display: none;
      }

      .benefits-grid,
      .testimonials-grid {
        grid-template-columns: 1fr;
      }

      .cta-section h2 {
        font-size: 2em;
      }

      .section {
        padding: 60px 20px;
      }
    }

    @media (max-width: 480px) {
      .hero h1 {
        font-size: 1.8em;
      }

      .hero p {
        font-size: 1em;
      }

      .section-title {
        font-size: 1.5em;
      }

      .btn {
        padding: 12px 30px;
        font-size: 0.95em;
      }

      .guarantee {
        padding: 30px 20px;
      }

      .guarantee h3 {
        font-size: 1.5em;
      }
    }

    /* ANIMAÇÕES */
    @keyframes slideInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .benefit-card,
    .testimonial {
      animation: slideInUp 0.6s ease-out forwards;
    }

    .benefit-card:nth-child(1) { animation-delay: 0.1s; }
    .benefit-card:nth-child(2) { animation-delay: 0.2s; }
    .benefit-card:nth-child(3) { animation-delay: 0.3s; }
    .benefit-card:nth-child(4) { animation-delay: 0.4s; }
    .benefit-card:nth-child(5) { animation-delay: 0.5s; }
    .benefit-card:nth-child(6) { animation-delay: 0.6s; }
  </style>
</head>
<body>
  <!-- HEADER -->
  <header>
    <div class="header-container">
      <a href="#" class="logo">📘 A Jornada TEA</a>
      <nav>
        <a href="#beneficios">Benefícios</a>
        <a href="#depoimentos">Depoimentos</a>
        <a href="#garantia">Garantia</a>
        <a href="#faq">FAQ</a>
        <a href="#contato">Contato</a>
      </nav>
    </div>
  </header>

  <!-- HERO SECTION -->
  <section class="hero">
    <div class="hero-content">
      <h1>Seu filho é autista.<br>Você não está sozinho.</h1>
      <h2>Um guia que transforma dúvidas em ações práticas</h2>
      <p>Se você é pai, mãe ou educador de uma criança autista, sabe como é desafiador navegar por diagnósticos, terapias e inclusão. Este guia foi criado para você — com linguagem simples, exemplos reais e estratégias que funcionam no dia a dia.</p>
      <div class="hero-buttons">
        <a href="#" class="btn btn-primary">Fazer Quiz Gratuito</a>
        <a href="#" class="btn btn-secondary">Quero o Guia Completo</a>
      </div>
    </div>
  </section>

  <!-- SOCIAL PROOF -->
  <section class="social-proof">
    <div class="social-proof-container">
      <div class="proof-item">
        <div class="proof-number">2.500+</div>
        <div class="proof-text">Pais transformados</div>
      </div>
      <div class="proof-item">
        <div class="proof-number">4.9★</div>
        <div class="proof-text">Avaliação média</div>
      </div>
      <div class="proof-item">
        <div class="proof-number">98%</div>
        <div class="proof-text">Taxa de satisfação</div>
      </div>
      <div class="proof-item">
        <div class="proof-number">50+</div>
        <div class="proof-text">Estratégias práticas</div>
      </div>
    </div>
  </section>

  <!-- VSL SECTION -->
  <section class="section vsl-section" id="vsl">
    <div class="vsl-container">
      <h2 class="section-title">Conheça a História de Transformação</h2>
      <p class="section-subtitle">Uma mensagem especial para você, pai ou educador que deseja fazer a diferença na vida de uma criança autista.</p>
      
      <div class="vsl-video-wrapper">
        <div class="vsl-placeholder">
          <p>🎬 VSL Horizontal - Inserir vídeo aqui</p>
          <small>Duração: ~3 minutos | Narração masculina emocional</small>
        </div>
      </div>

      <p class="vsl-text">
        "Você já se sentiu perdido quando soube que seu filho é autista? Muitos pais passam por isso. Medo, dúvidas, falta de direção... Mas quando você entende o autismo, tudo muda. Pais que leram nosso guia relatam mais confiança, melhor comunicação e inclusão real. Você vai aprender: sinais precoces, tipos de autismo, terapias que funcionam, estratégias para a escola e a vida. Comece agora com nosso quiz gratuito."
      </p>
    </div>
  </section>

  <!-- BENEFÍCIOS SECTION -->
  <section class="section benefits" id="beneficios">
    <h2 class="section-title">Por que este guia é indispensável?</h2>
    <div class="benefits-grid">
      <div class="benefit-card">
        <span class="benefit-icon">🧠</span>
        <h3>Compreensão Profunda</h3>
        <p>Entenda o que é o TEA, seus subtipos, sinais precoces e por que o diagnóstico precoce muda tudo.</p>
      </div>
      <div class="benefit-card">
        <span class="benefit-icon">💛</span>
        <h3>Terapias e Abordagens</h3>
        <p>Conheça as terapias comportamentais, ocupacionais e de comunicação que realmente funcionam.</p>
      </div>
      <div class="benefit-card">
        <span class="benefit-icon">🏫</span>
        <h3>Inclusão na Prática</h3>
        <p>Estratégias para a sala de aula, dicas para convivência e recursos que facilitam a inclusão.</p>
      </div>
      <div class="benefit-card">
        <span class="benefit-icon">📖</span>
        <h3>Linguagem Simples</h3>
        <p>Sem termos técnicos pesados. Tudo explicado como se um amigo estivesse conversando com você.</p>
      </div>
      <div class="benefit-card">
        <span class="benefit-icon">👥</span>
        <h3>Exemplos Reais</h3>
        <p>Histórias de pais e educadores que transformaram a vida de crianças autistas.</p>
      </div>
      <div class="benefit-card">
        <span class="benefit-icon">✅</span>
        <h3>Ações Práticas</h3>
        <p>Não é só teoria. Cada seção tem dicas que você pode usar hoje mesmo.</p>
      </div>
    </div>
  </section>

  <!-- DEPOIMENTOS SECTION -->
  <section class="section testimonials" id="depoimentos">
    <h2 class="section-title">O que dizem pais e educadores</h2>
    <div class="testimonials-grid">
      <div class="testimonial">
        <div class="star-rating">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">"Este guia mudou completamente a forma como interagimos com nosso filho. Ele nos deu segurança, direção e, acima de tudo, esperança. Recomendo para todos os pais que estão começando essa jornada."</p>
        <p class="testimonial-author">Maria L.</p>
        <p class="testimonial-role">Mãe de uma criança autista</p>
      </div>
      <div class="testimonial">
        <div class="star-rating">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">"Como educadora, finalmente encontrei um material claro, acolhedor e baseado em evidências. Recomendo a todos que trabalham com crianças no espectro. Transformou minha prática em sala de aula."</p>
        <p class="testimonial-author">Carlos P.</p>
        <p class="testimonial-role">Educador especializado</p>
      </div>
      <div class="testimonial">
        <div class="star-rating">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">"Não é um livro técnico pesado. É um amigo que entende e guia você passo a passo. Minha avó autista agora se sente compreendida e incluída na família."</p>
        <p class="testimonial-author">Juliana S.</p>
        <p class="testimonial-role">Avó de uma criança autista</p>
      </div>
    </div>
  </section>

  <!-- QUIZ SECTION -->
  <section class="section quiz-section" id="quiz">
    <div class="quiz-content">
      <div class="quiz-badge">🎯 TESTE SEU CONHECIMENTO</div>
      <h2 class="section-title">Qual é seu nível de conhecimento sobre autismo?</h2>
      <p class="section-subtitle">Responda 10 perguntas simples e descubra. Receba o mini eBook "10 Sinais Precoces do Autismo" como bônus!</p>
      <a href="#" class="btn btn-primary">Fazer Quiz Gratuito Agora</a>
    </div>
  </section>

  <!-- GARANTIA SECTION -->
  <section class="section guarantee-section" id="garantia">
    <div class="guarantee">
      <h3>🛡️ Garantia de Satisfação 100%</h3>
      <p>Leia o guia por 7 dias. Se não gostar, devolvemos seu dinheiro, sem perguntas. Mas temos certeza de que você vai amar.</p>
    </div>
  </section>

  <!-- FAQ SECTION -->
  <section class="section faq-section" id="faq">
    <h2 class="section-title">Perguntas Frequentes</h2>
    <div class="faq-container">
      <div class="faq-item">
        <div class="faq-question">
          <span>Como funciona o acesso ao guia?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>Após a compra, você recebe um email com o link de download do guia em PDF. O acesso é imediato e vitalício. Você pode baixar quantas vezes quiser e compartilhar com familiares.</p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Qual é o formato do guia?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>O guia é um eBook em PDF com mais de 100 páginas, ilustrado e bem formatado. Você pode ler em qualquer dispositivo (computador, tablet, smartphone) e imprimir se desejar.</p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Posso devolver se não gostar?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>Sim! Oferecemos garantia de 7 dias. Se o guia não atender suas expectativas, devolvemos 100% do seu dinheiro, sem perguntas. Basta enviar um email para nosso suporte.</p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>O guia é baseado em evidências científicas?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>Sim! Todo o conteúdo é baseado em pesquisa científica atualizada, DSM-5 e melhores práticas internacionais de inclusão. Inclui referências bibliográficas completas.</p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>O guia substitui atendimento profissional?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>Não. O guia é informativo e educacional. Sempre recomendamos consultar profissionais especializados (psicólogos, fonoaudiólogos, terapeutas) para diagnóstico e tratamento personalizado.</p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Há bônus inclusos?</span>
          <span class="faq-toggle">▼</span>
        </div>
        <div class="faq-answer">
          <p>Sim! Ao fazer o quiz, você recebe o mini eBook "10 Sinais Precoces do Autismo" gratuitamente. Ao comprar o guia completo, você ganha acesso a uma comunidade privada de suporte.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA FINAL SECTION -->
  <section class="cta-section" id="compra">
    <div class="cta-content">
      <div class="urgency-badge">⏰ OFERTA LIMITADA</div>
      <h2>Pronto para transformar a vida de uma criança?</h2>
      <p>Acesso imediato ao guia completo em PDF + bônus exclusivos. Comece sua jornada hoje.</p>
      <a href="#" class="btn btn-primary">Quero o Guia Completo</a>
    </div>
  </section>

  <!-- FOOTER -->
  <footer id="contato">
    <div class="footer-content">
      <div class="footer-grid">
        <div class="footer-section">
          <h4>Sobre</h4>
          <ul>
            <li><a href="#">Sobre o Guia</a></li>
            <li><a href="#">Nossa Missão</a></li>
            <li><a href="#">Equipe</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Recursos</h4>
          <ul>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Comunidade</a></li>
            <li><a href="#">Suporte</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Legal</h4>
          <ul>
            <li><a href="#">Política de Privacidade</a></li>
            <li><a href="#">Termos de Uso</a></li>
            <li><a href="#">Contato</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Redes Sociais</h4>
          <ul>
            <li><a href="#">Instagram</a></li>
            <li><a href="#">Facebook</a></li>
            <li><a href="#">YouTube</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-copyright">
        <p>© 2025 - A Jornada TEA. Conteúdo informativo baseado em pesquisa científica.<br>Não substitui aconselhamento médico ou psicológico profissional.</p>
      </div>
    </div>
  </footer>

  <!-- FAQ INTERATIVO -->
  <script>
    document.querySelectorAll('.faq-item').forEach(item => {
      item.querySelector('.faq-question').addEventListener('click', () => {
        item.classList.toggle('active');
      });
    });
  </script>

</body>
</html>