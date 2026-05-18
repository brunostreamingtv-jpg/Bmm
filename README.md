
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>BM STREAMING</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

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
    color:white;
}

/* NAVBAR */

header{
    width:100%;
    position:fixed;
    top:0;
    left:0;
    z-index:999;
    background:rgba(0,0,0,0.75);
    backdrop-filter:blur(10px);
    border-bottom:1px solid rgba(255,255,255,0.05);
}

.nav{
    max-width:1200px;
    margin:auto;
    padding:18px 20px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:30px;
    font-weight:800;
    color:white;
}

.logo span{
    color:#ff0000;
}

.menu{
    display:flex;
    gap:30px;
}

.menu a{
    color:#fff;
    text-decoration:none;
    transition:0.3s;
    font-weight:500;
}

.menu a:hover{
    color:#ff0000;
}

.btn-nav{
    background:#ff0000;
    padding:12px 22px;
    border-radius:12px;
    text-decoration:none;
    color:white;
    font-weight:600;
    transition:0.3s;
}

.btn-nav:hover{
    transform:translateY(-2px);
    box-shadow:0 0 20px rgba(255,0,0,0.5);
}

/* HERO */

.hero{
    width:100%;
    min-height:100vh;
    background:
    linear-gradient(rgba(0,0,0,.82), rgba(0,0,0,.88)),
    url('https://images.unsplash.com/photo-1585951237318-9ea5e175b891?q=80&w=1974&auto=format&fit=crop');
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:120px 20px 80px;
}

.hero-content{
    max-width:850px;
}

.hero h1{
    font-size:64px;
    line-height:1.1;
    margin-bottom:20px;
}

.hero h1 span{
    color:#ff0000;
}

.hero p{
    font-size:20px;
    color:#d9d9d9;
    margin-bottom:40px;
}

.hero-buttons{
    display:flex;
    gap:20px;
    justify-content:center;
    flex-wrap:wrap;
}

.btn-primary{
    background:#ff0000;
    color:white;
    padding:16px 34px;
    border-radius:14px;
    text-decoration:none;
    font-weight:600;
    transition:0.3s;
}

.btn-primary:hover{
    transform:translateY(-3px);
    box-shadow:0 0 30px rgba(255,0,0,.5);
}

.btn-secondary{
    border:2px solid #ffd000;
    color:#ffd000;
    padding:16px 34px;
    border-radius:14px;
    text-decoration:none;
    font-weight:600;
    transition:0.3s;
}

.btn-secondary:hover{
    background:#ffd000;
    color:black;
}

/* BENEFÍCIOS */

.section{
    padding:90px 20px;
}

.container{
    max-width:1200px;
    margin:auto;
}

.section-title{
    text-align:center;
    margin-bottom:60px;
}

.section-title h2{
    font-size:42px;
    margin-bottom:10px;
}

.section-title p{
    color:#bfbfbf;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:#101010;
    padding:35px;
    border-radius:22px;
    border:1px solid rgba(255,255,255,0.05);
    transition:0.3s;
}

.card:hover{
    transform:translateY(-5px);
    border-color:#ff0000;
}

.card-icon{
    font-size:42px;
    margin-bottom:20px;
}

.card h3{
    margin-bottom:10px;
}

.card p{
    color:#bfbfbf;
    font-size:15px;
}

/* PLANOS */

.planos{
    background:#0b0b0b;
}

.planos-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:30px;
}

.plano{
    background:#111;
    border-radius:25px;
    padding:40px 30px;
    text-align:center;
    border:1px solid rgba(255,255,255,0.06);
    transition:0.3s;
}

.plano:hover{
    transform:scale(1.03);
    border-color:#ff0000;
}

.plano h3{
    font-size:28px;
    margin-bottom:10px;
}

.preco{
    font-size:50px;
    color:#ff0000;
    font-weight:800;
    margin:20px 0;
}

.plano ul{
    list-style:none;
    margin-bottom:30px;
}

.plano ul li{
    margin:12px 0;
    color:#d2d2d2;
}

/* FAQ */

.faq-item{
    background:#111;
    padding:25px;
    border-radius:18px;
    margin-bottom:20px;
}

.faq-item h4{
    margin-bottom:10px;
}

/* FOOTER */

footer{
    padding:40px 20px;
    text-align:center;
    border-top:1px solid rgba(255,255,255,0.05);
    color:#9c9c9c;
}

/* WHATSAPP */

.whatsapp{
    position:fixed;
    bottom:25px;
    right:25px;
    width:65px;
    height:65px;
    background:#25d366;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    text-decoration:none;
    color:white;
    font-size:32px;
    box-shadow:0 0 25px rgba(37,211,102,.5);
    z-index:999;
}

/* RESPONSIVO */

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

    .section-title h2{
        font-size:32px;
    }

}

</style>
</head>

<body>

<header>
    <div class="nav">
        <div class="logo">
            BM <span>STREAMING</span>
        </div>

        <div class="menu">
            <a href="#">Home</a>
            <a href="#beneficios">Benefícios</a>
            <a href="#planos">Planos</a>
            <a href="#faq">FAQ</a>
        </div>

        <a href="https://wa.me/5567992010343" class="btn-nav">
            Pedir Agora
        </a>
    </div>
</header>

<section class="hero">

    <div class="hero-content">

        <h1>
            Filmes, Séries e Futebol na <span>Palma da Sua Mão</span>
        </h1>

        <p>
            Assista canais ao vivo, filmes e séries em HD/Full HD sem travamentos.
        </p>

        <div class="hero-buttons">
            <a href="https://wa.me/5567992010343" class="btn-primary">
                Teste Grátis
            </a>

            <a href="#planos" class="btn-secondary">
                Ver Planos
            </a>
        </div>

    </div>

</section>

<section class="section" id="beneficios">

    <div class="container">

        <div class="section-title">
            <h2>Nossos Diferenciais</h2>
            <p>Experiência premium em entretenimento digital.</p>
        </div>

        <div class="cards">

            <div class="card">
                <div class="card-icon">📺</div>
                <h3>+10 Mil Conteúdos</h3>
                <p>Filmes, séries, canais e esportes atualizados diariamente.</p>
            </div>

            <div class="card">
                <div class="card-icon">⚡</div>
                <h3>Sem Travamentos</h3>
                <p>Servidores rápidos e estáveis para máxima qualidade.</p>
            </div>

            <div class="card">
                <div class="card-icon">📱</div>
                <h3>Compatível</h3>
                <p>Smart TV, TV Box, Android, iPhone e muito mais.</p>
            </div>

            <div class="card">
                <div class="card-icon">🎧</div>
                <h3>Suporte Rápido</h3>
                <p>Atendimento rápido e suporte totalmente automatizado.</p>
            </div>

        </div>

    </div>

</section>

<section class="section planos" id="planos">

    <div class="container">

        <div class="section-title">
            <h2>Nossos Planos</h2>
            <p>Escolha o melhor plano para você.</p>
        </div>

        <div class="planos-grid">

            <div class="plano">
                <h3>Mensal</h3>

                <div class="preco">
                    R$25
                </div>

                <ul>
                    <li>✔ Filmes e Séries</li>
                    <li>✔ Futebol Ao Vivo</li>
                    <li>✔ Canais HD</li>
                    <li>✔ Suporte Incluso</li>
                </ul>

                <a href="https://wa.me/5567992010343" class="btn-primary">
                    Assinar
                </a>
            </div>

            <div class="plano">
                <h3>Trimestral</h3>

                <div class="preco">
                    R$65
                </div>

                <ul>
                    <li>✔ Conteúdo Completo</li>
                    <li>✔ Full HD</li>
                    <li>✔ Atualizações</li>
                    <li>✔ Melhor Custo</li>
                </ul>

                <a href="https://wa.me/5567992010343" class="btn-primary">
                    Assinar
                </a>
            </div>

        </div>

    </div>

</section>

<section class="section" id="faq">

    <div class="container">

        <div class="section-title">
            <h2>Perguntas Frequentes</h2>
        </div>

        <div class="faq-item">
            <h4>Funciona em Smart TV?</h4>
            <p>Sim, compatível com Smart TVs, TV Box, celular e computador.</p>
        </div>

        <div class="faq-item">
            <h4>Tem teste grátis?</h4>
            <p>Sim, solicite seu teste diretamente no WhatsApp.</p>
        </div>

        <div class="faq-item">
            <h4>O acesso é imediato?</h4>
            <p>Sim, após a confirmação o acesso é liberado rapidamente.</p>
        </div>

    </div>

</section>

<footer>
    © 2026 BM STREAMING - Todos os direitos reservados.
</footer>

<a class="whatsapp" href="https://wa.me/5567992010343">
    ☎
</a>

</body>
</html>
