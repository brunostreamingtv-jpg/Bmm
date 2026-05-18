<!DOCTYPE html><html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>BM STREAMING</title>  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    html{
      scroll-behavior:smooth;
    }

    body{
      background:#050505;
      color:#fff;
      overflow-x:hidden;
    }

    header{
      position:fixed;
      top:0;
      left:0;
      width:100%;
      z-index:999;
      background:rgba(0,0,0,.7);
      backdrop-filter:blur(10px);
      border-bottom:1px solid rgba(255,255,255,.08);
    }

    .container{
      width:100%;
      max-width:1200px;
      margin:auto;
      padding:0 20px;
    }

    .nav{
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:18px 0;
    }

    .logo{
      font-size:32px;
      font-weight:900;
      color:#e50914;
    }

    .logo span{
      color:#fff;
    }

    .menu{
      display:flex;
      gap:25px;
    }

    .menu a{
      color:#fff;
      text-decoration:none;
      transition:.3s;
      font-weight:500;
    }

    .menu a:hover{
      color:#e50914;
    }

    .btn{
      background:#e50914;
      color:#fff;
      border:none;
      padding:14px 26px;
      border-radius:12px;
      font-weight:700;
      cursor:pointer;
      transition:.3s;
    }

    .btn:hover{
      transform:scale(1.05);
      background:#ff1d28;
    }

    .hero{
      height:100vh;
      background:
      linear-gradient(to top, #050505, rgba(0,0,0,.6)),
      url('https://images.unsplash.com/photo-1524985069026-dd778a71c7b4?q=80&w=1600&auto=format&fit=crop') center/cover;
      display:flex;
      align-items:center;
      text-align:center;
      padding:0 20px;
    }

    .hero-content{
      max-width:900px;
      margin:auto;
      animation:fade 1.2s ease;
    }

    @keyframes fade{
      from{
        opacity:0;
        transform:translateY(30px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    .tag{
      display:inline-block;
      background:rgba(229,9,20,.2);
      color:#ff4d57;
      border:1px solid #e50914;
      padding:10px 18px;
      border-radius:50px;
      margin-bottom:25px;
      font-weight:700;
    }

    .hero h1{
      font-size:70px;
      line-height:1.1;
      margin-bottom:20px;
      font-weight:900;
    }

    .hero h1 span{
      color:#e50914;
    }

    .hero p{
      color:#ccc;
      font-size:20px;
      margin-bottom:35px;
    }

    .buttons{
      display:flex;
      gap:15px;
      justify-content:center;
      flex-wrap:wrap;
    }

    section{
      padding:90px 0;
    }

    .title{
      font-size:42px;
      margin-bottom:15px;
      font-weight:900;
    }

    .subtitle{
      color:#aaa;
      margin-bottom:50px;
    }

    .cards{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
      gap:25px;
    }

    .card{
      position:relative;
      overflow:hidden;
      border-radius:22px;
      transition:.4s;
      cursor:pointer;
      border:1px solid rgba(255,255,255,.08);
      background:#111;
    }

    .card:hover{
      transform:translateY(-10px) scale(1.02);
    }

    .card img{
      width:100%;
      height:360px;
      object-fit:cover;
      display:block;
    }

    .overlay{
      position:absolute;
      inset:0;
      background:linear-gradient(to top,#000,transparent);
    }

    .card-info{
      position:absolute;
      bottom:20px;
      left:20px;
    }

    .card-info h3{
      font-size:28px;
      margin-bottom:5px;
    }

    .apps-grid,
    .plans{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:25px;
    }

    .app-box,
    .plan,
    .panel-box{
      background:#111;
      border-radius:22px;
      padding:30px;
      border:1px solid rgba(255,255,255,.08);
      transition:.3s;
    }

    .app-box:hover,
    .plan:hover,
    .panel-box:hover{
      border-color:#e50914;
      transform:translateY(-5px);
    }

    .app-box h3{
      color:#e50914;
      margin-bottom:20px;
    }

    .app-box ul{
      list-style:none;
    }

    .app-box li{
      margin-bottom:12px;
      color:#ddd;
    }

    .plan.destaque{
      background:#e50914;
    }

    .plan h2{
      font-size:38px;
      margin-bottom:10px;
    }

    .price{
      font-size:55px;
      font-weight:900;
      margin-bottom:25px;
    }

    .badge{
      display:inline-block;
      background:#fff;
      color:#e50914;
      padding:8px 14px;
      border-radius:50px;
      font-size:13px;
      font-weight:800;
      margin-bottom:15px;
    }

    .panel{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:25px;
      margin-bottom:35px;
    }

    .panel-box h2{
      font-size:48px;
      color:#e50914;
      margin:15px 0;
    }

    .player{
      background:#111;
      border-radius:24px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.08);
      padding:30px;
    }

    .player-screen{
      width:100%;
      aspect-ratio:16/9;
      background:#000;
      border-radius:20px;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      border:1px solid rgba(255,255,255,.08);
    }

    footer{
      padding:50px 20px;
      text-align:center;
      border-top:1px solid rgba(255,255,255,.08);
    }

    footer h2{
      color:#e50914;
      font-size:36px;
      margin-bottom:10px;
    }

    @media(max-width:768px){
      .menu{
        display:none;
      }

      .hero h1{
        font-size:42px;
      }

      .hero p{
        font-size:16px;
      }

      .title{
        font-size:32px;
      }
    }
  </style></head>
<body><header>
  <div class="container nav">
    <div class="logo">BM <span>STREAMING</span></div><div class="menu">
  <a href="#apps">Apps</a>
  <a href="#catalogo">Catálogo</a>
  <a href="#planos">Planos</a>
  <a href="#painel">Painel</a>
</div>

<button class="btn" onclick="ativar()">ASSINAR</button>

  </div>
</header><section class="hero">
  <div class="hero-content"><div class="tag">🔥 ATIVAÇÃO IMEDIATA</div>

<h1>SUA EXPERIÊNCIA <span>STREAMING</span><br>ESTILO NETFLIX</h1>

<p>Filmes, séries, canais ao vivo e apps compatíveis para todos os dispositivos.</p>

<div class="buttons">
  <button class="btn" onclick="ativar()">🚀 ASSINAR AGORA</button>
  <button class="btn" onclick="demo()">▶ VER DEMONSTRAÇÃO</button>
</div>

  </div>
</section><section id="catalogo">
  <div class="container">
    <h2 class="title">🎬 Filmes & Séries</h2>
    <p class="subtitle">Catálogo premium atualizado diariamente.</p><div class="cards">

  <div class="card">
    <img src="https://images.unsplash.com/photo-1489599849927-2ee91cede3ba?q=80&w=1200&auto=format&fit=crop" alt="Filme">
    <div class="overlay"></div>
    <div class="card-info">
      <h3>Ação Total</h3>
      <p>Streaming HD</p>
    </div>
  </div>

  <div class="card">
    <img src="https://images.unsplash.com/photo-1517604931442-7e0c8ed2963c?q=80&w=1200&auto=format&fit=crop" alt="Série">
    <div class="overlay"></div>
    <div class="card-info">
      <h3>Série Premium</h3>
      <p>Streaming HD</p>
    </div>
  </div>

  <div class="card">
    <img src="https://images.unsplash.com/photo-1478720568477-152d9b164e26?q=80&w=1200&auto=format&fit=crop" alt="Cinema">
    <div class="overlay"></div>
    <div class="card-info">
      <h3>Cinema HD</h3>
      <p>Streaming HD</p>
    </div>
  </div>

  <div class="card">
    <img src="https://images.unsplash.com/photo-1513106580091-1d82408b8cd6?q=80&w=1200&auto=format&fit=crop" alt="Lançamentos">
    <div class="overlay"></div>
    <div class="card-info">
      <h3>Lançamentos</h3>
      <p>Streaming HD</p>
    </div>
  </div>

</div>

  </div>
</section><section id="apps">
  <div class="container">
    <h2 class="title">📺 BM STREAMING | LISTA RÁPIDA DE APPS</h2>
    <p class="subtitle">Compatível com Smart TVs, Android, iPhone e PC.</p><div class="apps-grid">

  <div class="app-box">
    <h3>📺 SAMSUNG / LG / ROKU</h3>
    <ul>
      <li>✔ Brasil Flex Play</li>
      <li>✔ Assist Plus</li>
      <li>✔ Vizzion Play</li>
      <li>✔ Super Player</li>
      <li>✔ Blessed Player</li>
    </ul>
  </div>

  <div class="app-box">
    <h3>📦 TV BOX / ANDROID TV</h3>
    <ul>
      <li>✔ XCIPTV</li>
      <li>✔ IPTV Smarters Pro</li>
      <li>✔ 9Xtream / XP IPTV</li>
      <li>✔ Geek Pro</li>
      <li>✔ Geek VU</li>
      <li>✔ Blessed Player</li>
    </ul>
  </div>

  <div class="app-box">
    <h3>📱 CELULAR ANDROID</h3>
    <ul>
      <li>✔ IPTV Smarters Pro</li>
      <li>✔ XCIPTV</li>
      <li>✔ 9Xtream</li>
      <li>✔ Blessed Player</li>
    </ul>
  </div>

  <div class="app-box">
    <h3>🍎 IPHONE (iOS)</h3>
    <ul>
      <li>✔ IPTV Smarters Pro</li>
      <li>✔ XCIPTV</li>
    </ul>
  </div>

  <div class="app-box">
    <h3>💻 PC / NOTEBOOK</h3>
    <ul>
      <li>✔ Max Play Windows</li>
      <li>✔ IPTV Smarters Web</li>
    </ul>
  </div>

</div>

  </div>
</section><section id="planos">
  <div class="container">
    <h2 class="title">💰 Planos</h2>
    <p class="subtitle">Escolha o melhor plano para você.</p><div class="plans">

  <div class="plan">
    <h2>Mensal</h2>
    <div class="price">R$20</div>
    <button class="btn" onclick="plano('Mensal')">ASSINAR</button>
  </div>

  <div class="plan">
    <h2>Trimestral</h2>
    <div class="price">R$60</div>
    <button class="btn" onclick="plano('Trimestral')">ASSINAR</button>
  </div>

  <div class="plan destaque">
    <div class="badge">🚀 MAIS VENDIDO</div>
    <h2>6 Meses</h2>
    <div class="price">R$120</div>
    <button class="btn" onclick="plano('6 Meses')">ASSINAR</button>
  </div>

  <div class="plan">
    <h2>Anual</h2>
    <div class="price">R$360</div>
    <button class="btn" onclick="plano('Anual')">ASSINAR</button>
  </div>

</div>

  </div>
</section><section id="painel">
  <div class="container">
    <h2 class="title">🎛 Painel Streaming</h2>
    <p class="subtitle">Dashboard estilo Netflix.</p><div class="panel">

  <div class="panel-box">
    <h3>👥 Usuários</h3>
    <h2>2.480</h2>
    <p>Usuários ativos</p>
  </div>

  <div class="panel-box">
    <h3>📺 Streams</h3>
    <h2>1.240</h2>
    <p>Online agora</p>
  </div>

  <div class="panel-box">
    <h3>⚡ Status</h3>
    <h2>99%</h2>
    <p>Sistema operacional</p>
  </div>

</div>

<div class="player">
  <h2 style="margin-bottom:20px">▶ PLAYER IPTV</h2>

  <div class="player-screen">
    <div>
      <h1 style="font-size:70px">📺</h1>
      <h2>Área pronta para integrar player IPTV</h2>
      <p style="margin-top:10px;color:#999">Compatível com iframe e m3u8</p>
    </div>
  </div>
</div>

  </div>
</section><footer>
  <h2>BM STREAMING</h2>
  <p style="color:#888;margin-bottom:10px">Streaming moderno estilo Netflix.</p>
  <p style="color:#e50914;font-weight:700;margin-bottom:25px">📞 WhatsApp: (67) 99201-0343</p><button class="btn" onclick="suporte()">📱 WHATSAPP SUPORTE</button>

</footer><script>

  function ativar(){
    alert('BM STREAMING ativado com sucesso!');
  }

  function demo(){
    alert('Demonstração iniciando...');
  }

  function suporte(){
    window.open('https://wa.me/5567992010343','_blank');
  }

  function plano(nome){
    alert('Plano selecionado: ' + nome);
  }

</script></body>
</html>
