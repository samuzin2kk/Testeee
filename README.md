PHONE_NUMBER (sem +), WHATSAPP_LINK (ex: https://wa.me/55NUMERO), ADDRESS_TEXT, MAP_IFRAME_SRC (Google Maps embed URL), LOGO_SRC (URL da imagem).
  2) Salve como arquivo .html e abra no navegador do celular, ou hospede no GitHub Pages / Netlify / Vercel.
  3) Para publicar no Google Sites ou Canva, copie o conteúdo necessário (imagens e textos) para os editores dessas plataformas.
-->

<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Pizza Testes - Pizzaria</title>
  <meta name="description" content="Pizzaria Pizza Testes — Delivery, Retirada e Atendimento no Local">
  <style>
    :root{--accent:#d84315;--bg:#fff;--muted:#666}
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; background:var(--bg); color:#111}
    header{background:linear-gradient(90deg, rgba(216,67,21,0.95), rgba(231,94,55,0.9)); color:#fff; padding:22px 16px}
    .container{max-width:980px; margin:0 auto; padding:16px}
    .brand{display:flex; align-items:center; gap:12px}
    .brand img{width:56px; height:56px; border-radius:8px; object-fit:cover}
    .brand h1{font-size:20px; margin:0}
    .subtitle{font-size:13px; opacity:0.95}

    nav{display:flex; gap:8px; margin-top:12px; overflow:auto}
    nav a{background:rgba(255,255,255,0.12); padding:8px 12px; border-radius:999px; color:#fff; text-decoration:none; font-size:13px}

    .hero{display:flex; gap:12px; align-items:center; margin-top:18px}
    .hero .left{flex:1}
    .hero h2{margin:0 0 8px 0}
    .hero p{margin:0 0 12px 0; color:var(--muted)}
    .cta{display:inline-block; background:#fff; color:var(--accent); padding:10px 14px; border-radius:8px; text-decoration:none; font-weight:700}

    .card{background:#fff; border-radius:12px; box-shadow:0 6px 20px rgba(0,0,0,0.06); padding:14px; margin-bottom:14px}
    h3{margin:0 0 8px 0}
    .grid{display:grid; grid-template-columns:repeat(2,1fr); gap:8px}
    .menu-item{display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed #eee}
    .price{font-weight:700}

    .map{height:200px; border-radius:10px; overflow:hidden}

    footer{padding:18px 16px; text-align:center; color:var(--muted); font-size:13px}

    /* Floating WhatsApp */
    .wa{position:fixed; right:16px; bottom:16px; z-index:999}
    .wa a{display:flex; align-items:center; gap:10px; background:linear-gradient(180deg,#25D366,#128C7E); color:#fff; padding:12px 14px; border-radius:999px; text-decoration:none; box-shadow:0 8px 24px rgba(37,211,102,0.2)}

    /* Responsive */
    @media(min-width:700px){
      .hero{margin-top:30px}
      .grid{grid-template-columns:repeat(3,1fr)}
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <div class="brand">
        <img src="LOGO_SRC" alt="Pizza Testes logo">
        <div>
          <h1>PIZZA TESTES</h1>
          <div class="subtitle">Pizza artesanal • Delivery • Retirada • Atendimento no local</div>
        </div>
      </div>
      <nav aria-label="menu">
        <a href="#cardapio">Cardápio</a>
        <a href="#promocoes">Promoções</a>
        <a href="#sobre">Sobre</a>
        <a href="#local">Local</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="left">
        <h2>Sua pizza favorita em poucos minutos</h2>
        <p>Massas frescas, ingredientes selecionados e sabores que conquistam a família inteira. Peça agora pelo WhatsApp.</p>
        <a class="cta" id="btn-pedir" href="WHATSAPP_LINK">Pedir pelo WhatsApp</a>
      </div>
      <div class="right">
        <div class="card" style="width:210px; text-align:center">
          <strong>Horário</strong>
          <div style="margin-top:8px">Seg–Qui: 18h–23h<br>Sex–Sáb: 18h–00h<br>Dom: 17h–23h</div>
        </div>
      </div>
    </section>

    <section id="cardapio" class="card">
      <h3>🍕 Cardápio</h3>
      <div class="grid">
        <div>
          <h4>Tradicionais</h4>
          <div class="menu-item"><span>Mussarela</span><span class="price">R$ 29,90</span></div>
          <div class="menu-item"><span>Calabresa</span><span class="price">R$ 29,90</span></div>
          <div class="menu-item"><span>Frango com Catupiry</span><span class="price">R$ 34,90</span></div>
          <div class="menu-item"><span>Portuguesa</span><span class="price">R$ 34,90</span></div>
        </div>

        <div>
          <h4>Especiais</h4>
          <div class="menu-item"><span>Quatro Queijos</span><span class="price">R$ 39,90</span></div>
          <div class="menu-item"><span>Pepperoni</span><span class="price">R$ 39,90</span></div>
          <div class="menu-item"><span>Bacon Cremoso</span><span class="price">R$ 42,90</span></div>
          <div class="menu-item"><span>Carne de Sol</span><span class="price">R$ 44,90</span></div>
        </div>

        <div>
          <h4>Doces & Bebidas</h4>
          <div class="menu-item"><span>Brigadeiro</span><span class="price">R$ 24,90</span></div>
          <div class="menu-item"><span>Chocolate</span><span class="price">R$ 24,90</span></div>
          <div class="menu-item"><span>Refrigerante 2L</span><span class="price">R$ 9,90</span></div>
          <div class="menu-item"><span>Cerveja</span><span class="price">R$ 6,90</span></div>
        </div>
      </div>
    </section>

    <section id="promocoes" class="card">
      <h3>💥 Promoções</h3>
      <ul>
        <li>Compre 1 pizza grande e ganhe 1 refrigerante 1L</li>
        <li>Combo Smash + Batata + Refri por R$ 24,90</li>
        <li>Terça da Pizza: qualquer sabor tradicional por preço promocional</li>
      </ul>
    </section>

    <section id="sobre" class="card">
      <h3>Sobre a Pizza Testes</h3>
      <p>Na Pizza Testes nós usamos massa fresca e ingredientes selecionados. Atendimento rápido e sabor que conquista. Delivery, retirada e espaço para consumo no local.</p>
    </section>

    <section id="local" class="card">
      <h3>📍 Localização</h3>
      <p id="address">ADDRESS_TEXT</p>
      <div class="map">
        <!-- Substitua MAP_IFRAME_SRC pelo src do embed do Google Maps -->
        <iframe src="MAP_IFRAME_SRC" width="100%" height="100%" style="border:0" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      <div>© <strong>PIZZA TESTES</strong> • Feito com carinho</div>
      <div style="margin-top:6px">Telefone/WhatsApp: <a href="WHATSAPP_LINK" style="color:var(--accent); text-decoration:none">WHATSAPP_NUMBER</a></div>
    </div>
  </footer>

  <div class="wa">
    <!-- Substitua WHATSAPP_LINK pelo link do seu WhatsApp (ex: https://wa.me/5511999999999) -->
    <a id="waLink" href="WHATSAPP_LINK" target="_blank">
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M20.52 3.481C18.27 1.233 15.35 0 12.11 0 5.65 0 .66 5.99 .66 12.45c0 2.17.58 4.29 1.68 6.18L0 24l5.63-1.46c1.83 1 3.86 1.54 5.9 1.54 6.46 0 11.45-5.99 11.45-12.45 0-3.24-1.23-6.15-3.66-8.14z" fill="#fff"/></svg>
      <span style="font-weight:700">Pedir</span>
    </a>
  </div>

  <script>
    // Script opcional para preencher o número legível
    (function(){
      const waLinks = document.querySelectorAll('[href="WHATSAPP_LINK"]');
      waLinks.forEach(a => a.textContent = a.textContent.replace('WHATSAPP_NUMBER', ' (clique para pedir)'));
    })();
  </script>
</body>
</html>
PHONE_NUMBER (sem +), WHATSAPP_LINK (ex: https://wa.me/55NUMERO), ADDRESS_TEXT, MAP_IFRAME_SRC (Google Maps embed URL), LOGO_SRC (URL da imagem).
  2) Salve como arquivo .html e abra no navegador do celular, ou hospede no GitHub Pages / Netlify / Vercel.
  3) Para publicar no Google Sites ou Canva, copie o conteúdo necessário (imagens e textos) para os editores dessas plataformas.
-->

<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Pizza Testes - Pizzaria</title>
  <meta name="description" content="Pizzaria Pizza Testes — Delivery, Retirada e Atendimento no Local">
  <style>
    :root{--accent:#d84315;--bg:#fff;--muted:#666}
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; background:var(--bg); color:#111}
    header{background:linear-gradient(90deg, rgba(216,67,21,0.95), rgba(231,94,55,0.9)); color:#fff; padding:22px 16px}
    .container{max-width:980px; margin:0 auto; padding:16px}
    .brand{display:flex; align-items:center; gap:12px}
    .brand img{width:56px; height:56px; border-radius:8px; object-fit:cover}
    .brand h1{font-size:20px; margin:0}
    .subtitle{font-size:13px; opacity:0.95}

    nav{display:flex; gap:8px; margin-top:12px; overflow:auto}
    nav a{background:rgba(255,255,255,0.12); padding:8px 12px; border-radius:999px; color:#fff; text-decoration:none; font-size:13px}

    .hero{display:flex; gap:12px; align-items:center; margin-top:18px}
    .hero .left{flex:1}
    .hero h2{margin:0 0 8px 0}
    .hero p{margin:0 0 12px 0; color:var(--muted)}
    .cta{display:inline-block; background:#fff; color:var(--accent); padding:10px 14px; border-radius:8px; text-decoration:none; font-weight:700}

    .card{background:#fff; border-radius:12px; box-shadow:0 6px 20px rgba(0,0,0,0.06); padding:14px; margin-bottom:14px}
    h3{margin:0 0 8px 0}
    .grid{display:grid; grid-template-columns:repeat(2,1fr); gap:8px}
    .menu-item{display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed #eee}
    .price{font-weight:700}

    .map{height:200px; border-radius:10px; overflow:hidden}

    footer{padding:18px 16px; text-align:center; color:var(--muted); font-size:13px}

    /* Floating WhatsApp */
    .wa{position:fixed; right:16px; bottom:16px; z-index:999}
    .wa a{display:flex; align-items:center; gap:10px; background:linear-gradient(180deg,#25D366,#128C7E); color:#fff; padding:12px 14px; border-radius:999px; text-decoration:none; box-shadow:0 8px 24px rgba(37,211,102,0.2)}

    /* Responsive */
    @media(min-width:700px){
      .hero{margin-top:30px}
      .grid{grid-template-columns:repeat(3,1fr)}
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <div class="brand">
        <img src="LOGO_SRC" alt="Pizza Testes logo">
        <div>
          <h1>PIZZA TESTES</h1>
          <div class="subtitle">Pizza artesanal • Delivery • Retirada • Atendimento no local</div>
        </div>
      </div>
      <nav aria-label="menu">
        <a href="#cardapio">Cardápio</a>
        <a href="#promocoes">Promoções</a>
        <a href="#sobre">Sobre</a>
        <a href="#local">Local</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="left">
        <h2>Sua pizza favorita em poucos minutos</h2>
        <p>Massas frescas, ingredientes selecionados e sabores que conquistam a família inteira. Peça agora pelo WhatsApp.</p>
        <a class="cta" id="btn-pedir" href="WHATSAPP_LINK">Pedir pelo WhatsApp</a>
      </div>
      <div class="right">
        <div class="card" style="width:210px; text-align:center">
          <strong>Horário</strong>
          <div style="margin-top:8px">Seg–Qui: 18h–23h<br>Sex–Sáb: 18h–00h<br>Dom: 17h–23h</div>
        </div>
      </div>
    </section>

    <section id="cardapio" class="card">
      <h3>🍕 Cardápio</h3>
      <div class="grid">
        <div>
          <h4>Tradicionais</h4>
          <div class="menu-item"><span>Mussarela</span><span class="price">R$ 29,90</span></div>
          <div class="menu-item"><span>Calabresa</span><span class="price">R$ 29,90</span></div>
          <div class="menu-item"><span>Frango com Catupiry</span><span class="price">R$ 34,90</span></div>
          <div class="menu-item"><span>Portuguesa</span><span class="price">R$ 34,90</span></div>
        </div>

        <div>
          <h4>Especiais</h4>
          <div class="menu-item"><span>Quatro Queijos</span><span class="price">R$ 39,90</span></div>
          <div class="menu-item"><span>Pepperoni</span><span class="price">R$ 39,90</span></div>
          <div class="menu-item"><span>Bacon Cremoso</span><span class="price">R$ 42,90</span></div>
          <div class="menu-item"><span>Carne de Sol</span><span class="price">R$ 44,90</span></div>
        </div>

        <div>
          <h4>Doces & Bebidas</h4>
          <div class="menu-item"><span>Brigadeiro</span><span class="price">R$ 24,90</span></div>
          <div class="menu-item"><span>Chocolate</span><span class="price">R$ 24,90</span></div>
          <div class="menu-item"><span>Refrigerante 2L</span><span class="price">R$ 9,90</span></div>
          <div class="menu-item"><span>Cerveja</span><span class="price">R$ 6,90</span></div>
        </div>
      </div>
    </section>

    <section id="promocoes" class="card">
      <h3>💥 Promoções</h3>
      <ul>
        <li>Compre 1 pizza grande e ganhe 1 refrigerante 1L</li>
        <li>Combo Smash + Batata + Refri por R$ 24,90</li>
        <li>Terça da Pizza: qualquer sabor tradicional por preço promocional</li>
      </ul>
    </section>

    <section id="sobre" class="card">
      <h3>Sobre a Pizza Testes</h3>
      <p>Na Pizza Testes nós usamos massa fresca e ingredientes selecionados. Atendimento rápido e sabor que conquista. Delivery, retirada e espaço para consumo no local.</p>
    </section>

    <section id="local" class="card">
      <h3>📍 Localização</h3>
      <p id="address">ADDRESS_TEXT</p>
      <div class="map">
        <!-- Substitua MAP_IFRAME_SRC pelo src do embed do Google Maps -->
        <iframe src="MAP_IFRAME_SRC" width="100%" height="100%" style="border:0" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      <div>© <strong>PIZZA TESTES</strong> • Feito com carinho</div>
      <div style="margin-top:6px">Telefone/WhatsApp: <a href="WHATSAPP_LINK" style="color:var(--accent); text-decoration:none">WHATSAPP_NUMBER</a></div>
    </div>
  </footer>

  <div class="wa">
    <!-- Substitua WHATSAPP_LINK pelo link do seu WhatsApp (ex: https://wa.me/5511999999999) -->
    <a id="waLink" href="WHATSAPP_LINK" target="_blank">
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M20.52 3.481C18.27 1.233 15.35 0 12.11 0 5.65 0 .66 5.99 .66 12.45c0 2.17.58 4.29 1.68 6.18L0 24l5.63-1.46c1.83 1 3.86 1.54 5.9 1.54 6.46 0 11.45-5.99 11.45-12.45 0-3.24-1.23-6.15-3.66-8.14z" fill="#fff"/></svg>
      <span style="font-weight:700">Pedir</span>
    </a>
  </div>

  <script>
    // Script opcional para preencher o número legível
    (function(){
      const waLinks = document.querySelectorAll('[href="WHATSAPP_LINK"]');
      waLinks.forEach(a => a.textContent = a.textContent.replace('WHATSAPP_NUMBER', ' (clique para pedir)'));
    })();
  </script>
</body>
</html>
