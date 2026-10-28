# cocina-del-mare-oap
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Cocina Del Mare — sabores e inspirações do oceano.">
<title>Cocina Del Mare | Sabores do Oceano</title>

<style>
:root {
  --navy: #062e38;
  --teal: #0b4650;
  --cream: #f6f2e9;
  --gold: #d8b477;
  --gold-dark: #a87835;
  --ink: #153b43;
  --muted: #5d7070;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  font-family: Arial, Helvetica, sans-serif;
  background: var(--cream);
  color: var(--ink);
  line-height: 1.7;
}
header {
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  flex-wrap: wrap;
  padding: 18px 6%;
  background: var(--navy);
  color: var(--cream);
  border-bottom: 1px solid #d8b47766;
}
.brand {
  color: var(--gold);
  text-decoration: none;
  font-family: Georgia, serif;
  font-size: 23px;
  letter-spacing: 3px;
}
nav { display: flex; flex-wrap: wrap; gap: 16px; }
nav a {
  color: var(--cream);
  font-size: 13px;
  text-decoration: none;
}
nav a:hover { color: var(--gold); }

.hero {
  min-height: 490px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 35px;
  padding: 75px 8%;
  color: var(--cream);
  background:
    radial-gradient(ellipse at 78% 45%, #12778288, transparent 42%),
    linear-gradient(115deg, #052d37, #07505b 55%, #062f3a);
}
.eyebrow {
  color: var(--gold);
  text-transform: uppercase;
  letter-spacing: 4px;
  font-size: 11px;
  margin-bottom: 15px;
}
.hero h1 {
  font: normal clamp(48px, 7vw, 82px)/1 Georgia, serif;
  margin-bottom: 23px;
}
.hero h1 span { display: block; color: var(--gold); }
.intro { max-width: 470px; color: #e4e9e4; font-size: 17px; }
.button {
  display: inline-block;
  margin-top: 25px;
  padding: 12px 23px;
  border: 1px solid var(--gold);
  background: var(--gold);
  color: var(--navy);
  text-decoration: none;
  font-weight: bold;
  transition: .2s;
}
.button:hover { background: #e8c990; transform: translateY(-2px); }

.hero-art { width: 100%; max-width: 440px; justify-self: center; }
section { padding: 75px 7%; scroll-margin-top: 90px; }
.section-head { max-width: 750px; margin: 0 auto 38px; text-align: center; }
.section-head .eyebrow { color: var(--gold-dark); margin-bottom: 8px; }
h2 { font: normal clamp(30px, 4vw, 44px)/1.2 Georgia, serif; }
.section-head p:last-child { color: var(--muted); margin-top: 14px; }

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 24px;
  max-width: 1240px;
  margin: auto;
}
.card {
  background: #fff;
  border: 1px solid #153b4312;
  overflow: hidden;
  box-shadow: 0 12px 35px #062e381a;
}
.card-image {
  display: block;
  width: 100%;
  height: 255px;
  overflow: hidden;
  background: #e5e0d5;
}
.card-image img {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  transition: transform .35s;
}
.card:hover .card-image img { transform: scale(1.04); }
.card-content { padding: 22px; }
.card h3 { font: normal 29px Georgia, serif; margin-bottom: 8px; }
.card p { color: var(--muted); font-size: 14px; margin-bottom: 13px; }
.text-link { color: var(--gold-dark); font-weight: bold; text-decoration: none; }
.text-link:hover { text-decoration: underline; }

.gallery { display: grid; grid-template-columns: repeat(3, 1fr); padding-top: 0; }
.gallery a {
  position: relative;
  min-height: 280px;
  display: flex;
  align-items: end;
  padding: 25px;
  color: white;
  text-decoration: none;
  background: var(--navy);
  overflow: hidden;
}
.gallery a::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(0deg, #03191ee8, transparent 75%);
}
.gallery img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform .4s;
}
.gallery a:hover img { transform: scale(1.04); }
.gallery-copy { position: relative; z-index: 1; }
.gallery h3 { font: normal 30px Georgia, serif; }
.gallery p { font-size: 13px; }

.article-section { background: #eae4d7; }
.article { max-width: 850px; margin: auto; }
.article .eyebrow { color: var(--gold-dark); }
.article h2 { margin-bottom: 18px; }
.article p, .article li { color: #53696a; margin-bottom: 12px; }
.article h3 { font: normal 25px Georgia, serif; margin: 25px 0 9px; }
.article ul { padding-left: 23px; }
.recipe {
  margin: 22px 0;
  padding: 24px;
  background: white;
  border-left: 4px solid var(--gold);
}
.recipe h3 { margin-top: 0; }

.contact { background: var(--navy); color: var(--cream); text-align: center; }
.contact h2 { color: white; }
.contact > p:not(.eyebrow) {
  max-width: 620px;
  margin: 16px auto;
  color: #dbe5e2;
}
.contact-links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px 30px;
  margin-top: 25px;
  font-size: 13px;
}
.contact-links a { color: var(--cream); text-decoration: none; }
.contact-links a:hover { color: var(--gold); }
footer {
  padding: 23px 6%;
  text-align: center;
  background: #041f27;
  color: #d9e2df;
  font-size: 13px;
}
footer p + p { color: #aabfbd; font-size: 12px; }

@media (max-width: 850px) {
  header { align-items: flex-start; flex-direction: column; }
  .hero { grid-template-columns: 1fr; padding: 60px 7%; }
  .hero-art { max-width: 360px; }
  .grid { grid-template-columns: 1fr 1fr; }
  .gallery { grid-template-columns: 1fr; }
  .gallery a { min-height: 230px; }
}
@media (max-width: 560px) {
  nav { gap: 10px 15px; }
  .grid { grid-template-columns: 1fr; }
  .card-image { height: 250px; }
  section { padding: 52px 5%; }
  .hero h1 { font-size: 54px; }
}
</style>
</head>

<body>
<header>
  <a class="brand" href="#inicio">〰 COCINA DEL MARE</a>
  <nav>
    <a href="#inicio">Início</a>
    <a href="#especialidades">Especialidades</a>
    <a href="#polvo">Polvo</a>
    <a href="#lagosta">Lagosta</a>
    <a href="#camarao">Camarão</a>
    <a href="#contato">Contato</a>
  </nav>
</header>

<main>
<section class="hero" id="inicio">
  <div>
    <p class="eyebrow">Gastronomia · Oceano · Experiências</p>
    <h1>COCINA <span>DEL MARE</span></h1>
    <p class="intro">
      Frutos do mar, receitas especiais e o verdadeiro sabor
      do oceano na sua mesa.
    </p>
    <a class="button" href="#especialidades">Explorar sabores →</a>
  </div>

  <svg class="hero-art" viewBox="0 0 420 330"
       xmlns="http://www.w3.org/2000/svg"
       role="img" aria-label="Ilustração decorativa marinha">
    <g fill="none" stroke="#d8b477" stroke-width="2"
       stroke-linecap="round" stroke-linejoin="round">
      <path d="M160 115 Q140 78 170 65 Q200 55 215 82
               Q232 105 207 122 Q180 140 160 115Z"/>
      <path d="M162 120 Q130 145 115 175 T80 180
               M176 127 Q160 160 175 180 T155 205
               M192 126 Q220 145 220 172 T250 180
               M207 120 Q237 122 250 145 T280 145"/>
      <circle cx="177" cy="91" r="3" fill="#d8b477"/>
      <circle cx="198" cy="91" r="3" fill="#d8b477"/>
      <path d="M280 210 Q300 180 330 200 L350 220 L330 240
               Q300 255 280 230Z"/>
      <path d="M280 210 L255 195 L260 215 L255 235 L280 230"/>
      <path d="M45 270 Q65 220 60 185 M60 230 Q85 210 88 190
               M375 280 Q355 240 370 205 M370 245 Q390 225 395 210"/>
      <path d="M45 70 Q85 45 120 70 T185 65 M290 45 Q325 20 365 45"/>
      <circle cx="100" cy="120" r="4"/>
      <circle cx="320" cy="100" r="3"/>
      <circle cx="350" cy="135" r="5"/>
    </g>
  </svg>
</section>

<section id="especialidades">
  <div class="section-head">
    <p class="eyebrow">Nossas especialidades</p>
    <h2>Sabores que vêm do oceano</h2>
    <p>
      Conheça três ingredientes marcantes da gastronomia marinha,
      suas características e dicas para preparar pratos especiais.
    </p>
  </div>

  <div class="grid">
    <article class="card" id="polvo">
      <a class="card-image" href="#artigo-polvo" aria-label="Saiba mais sobre polvo">
        <img
          src="https://plus.unsplash.com/premium_photo-1719530467953-446faaf0c877?auto=format&fit=crop&w=1000&q=80"
          alt="Prato real de polvo preparado com acompanhamentos"
          loading="lazy"
          onerror="this.onerror=null;this.src='https://images.unsplash.com/photo-1565680018434-b513d5e5fd47?auto=format&fit=crop&w=1000&q=80';">
      </a>
      <div class="card-content">
        <h3>Polvo</h3>
        <p>
          Uma iguaria versátil, conhecida por sua textura delicada
          e sabor marcante. Ideal para pratos especiais.
        </p>
        <a class="text-link" href="#artigo-polvo">Descobrir o polvo →</a>
      </div>
    </article>

    <article class="card" id="lagosta">
      <a class="card-image" href="#artigo-lagosta" aria-label="Saiba mais sobre lagosta">
        <img
          src="https://images.unsplash.com/photo-1707995546408-9815c70dd5c4?auto=format&fit=crop&w=1000&q=80"
          alt="Fotografia real de lagosta servida com limão e ervas"
          loading="lazy"
          onerror="this.onerror=null;this.src='https://images.unsplash.com/photo-1523275033438-8c0a9239935b?auto=format&fit=crop&w=1000&q=80';">
      </a>
      <div class="card-content">
        <h3>Lagosta</h3>
        <p>
          Um ingrediente sofisticado que combina com preparações
          simples, elegantes e cheias de sabor.
        </p>
        <a class="text-link" href="#artigo-lagosta">Descobrir a lagosta →</a>
      </div>
    </article>

    <article class="card" id="camarao">
      <a class="card-image" href="#artigo-camarao" aria-label="Saiba mais sobre camarão">
        <img
          src="https://images.unsplash.com/photo-1658803136255-9c4b243dcc6b?auto=format&fit=crop&w=1000&q=80"
          alt="Fotografia real de camarões servidos em um prato"
          loading="lazy">
      </a>
      <div class="card-content">
        <h3>Camarão</h3>
        <p>
          Prático e saboroso, é perfeito para receitas rápidas,
          massas, risotos e preparações especiais.
        </p>
        <a class="text-link" href="#artigo-camarao">Descobrir o camarão →</a>
      </div>
    </article>
  </div>
</section>

<section class="gallery">
  <a href="#artigo-polvo">
    <img
      src="https://plus.unsplash.com/premium_photo-1719530467953-446faaf0c877?auto=format&fit=crop&w=1000&q=80"
      alt="Prato de polvo"
      loading="lazy">
    <div class="gallery-copy">
      <h3>Polvo</h3>
      <p>Sabor e delicadeza</p>
    </div>
  </a>
  <a href="#artigo-lagosta">
    <img
      src="https://images.unsplash.com/photo-1707995546408-9815c70dd5c4?auto=format&fit=crop&w=1000&q=80"
      alt="Lagosta servida com acompanhamentos"
      loading="lazy">
    <div class="gallery-copy">
      <h3>Lagosta</h3>
      <p>Sofisticação em cada garfada</p>
    </div>
  </a>
  <a href="#artigo-camarao">
    <img
      src="https://images.unsplash.com/photo-1658803136255-9c4b243dcc6b?auto=format&fit=crop&w=1000&q=80"
      alt="Prato de camarões"
      loading="lazy">
    <div class="gallery-copy">
      <h3>Camarão</h3>
      <p>Versatilidade à mesa</p>
    </div>
  </a>
</section>

<section class="article-section" id="artigo-polvo">
  <article class="article">
    <p class="eyebrow">Especialidade 01</p>
    <h2>Polvo: sabor e delicadeza</h2>
    <p>
      O polvo é apreciado em diferentes cozinhas do mundo.
      Seu sabor combina com azeite, alho, limão, ervas e legumes.
      O preparo cuidadoso ajuda a alcançar uma textura agradável.
    </p>
    <h3>Dicas de preparo</h3>
    <ul>
      <li>Compre em estabelecimentos confiáveis.</li>
      <li>Mantenha o alimento refrigerado ou congelado corretamente.</li>
      <li>Respeite o tempo de cozimento indicado na receita.</li>
    </ul>
    <div class="recipe">
      <h3>Receita: polvo com alho e azeite</h3>
      <p><strong>Ingredientes:</strong> polvo cozido, azeite, alho,
      limão, sal e salsinha.</p>
      <p><strong>Preparo:</strong> corte o polvo em pedaços.
      Aqueça o azeite, doure levemente o alho e acrescente o polvo.
      Aqueça bem, tempere e finalize com limão e salsinha.</p>
    </div>
    <a class="text-link" href="#especialidades">↑ Voltar às especialidades</a>
  </article>
</section>

<section class="article-section" id="artigo-lagosta">
  <article class="article">
    <p class="eyebrow">Especialidade 02</p>
    <h2>Lagosta: sofisticação em cada garfada</h2>
    <p>
      A lagosta é valorizada pela carne delicada e pelo sabor
      característico. Preparações com manteiga, ervas e limão
      realçam seu sabor sem exigir muitos ingredientes.
    </p>
    <h3>Dicas de preparo</h3>
    <ul>
      <li>Compre de fornecedores confiáveis.</li>
      <li>Evite cozinhar por tempo excessivo para não ressecar a carne.</li>
      <li>Combine com legumes, arroz ou batatas.</li>
    </ul>
    <div class="recipe">
      <h3>Receita: lagosta na manteiga</h3>
      <p><strong>Ingredientes:</strong> lagosta preparada,
      manteiga, alho, limão, sal e ervas frescas.</p>
      <p><strong>Preparo:</strong> cozinhe a lagosta adequadamente.
      Aqueça a manteiga com alho, acrescente a carne e finalize
      com limão e ervas. Sirva imediatamente.</p>
    </div>
    <a class="text-link" href="#especialidades">↑ Voltar às especialidades</a>
  </article>
</section>

<section class="article-section" id="artigo-camarao">
  <article class="article">
    <p class="eyebrow">Especialidade 03</p>
    <h2>Camarão: versatilidade à mesa</h2>
    <p>
      O camarão aparece em diversas receitas, de pratos leves
      a preparações cremosas. Seu cozimento costuma ser rápido,
      por isso é importante acompanhar o ponto.
    </p>
    <h3>Limpeza e conservação</h3>
    <ul>
      <li>Mantenha refrigerado ou congelado conforme a embalagem.</li>
      <li>Descongele na geladeira, sem deixar por longos períodos fora dela.</li>
      <li>Use utensílios limpos durante o preparo.</li>
    </ul>
    <div class="recipe">
      <h3>Receita: camarão ao alho e limão</h3>
      <p><strong>Ingredientes:</strong> camarões limpos, alho,
      azeite ou manteiga, limão, sal e pimenta.</p>
      <p><strong>Preparo:</strong> aqueça o azeite ou a manteiga,
      doure o alho e acrescente os camarões. Cozinhe até ficarem
      opacos e completamente cozidos. Finalize com limão.</p>
    </div>
    <a class="text-link" href="#especialidades">↑ Voltar às especialidades</a>
  </article>
</section>

<section class="contact" id="contato">
  <p class="eyebrow">Fale conosco</p>
  <h2>Vamos conversar?</h2>
  <p>
    Tem sugestões de receitas, dúvidas ou ideias para o site?
    Entre em contato com a Cocina Del Mare.
  </p>
  <a class="button"
     href="mailto:delmarecocina@gmail.com?subject=Contato%20-%20Cocina%20Del%20Mare">
    Enviar e-mail →
  </a>
  <div class="contact-links">
    <a href="mailto:delmarecocina@gmail.com">
      ✉ E-mail: delmarecocina@gmail.com
    </a>
    <span>WhatsApp: +00 (27) 99999-999</span>
  </div>
</section>
</main>

<footer>
  <p>© 2026 Cocina Del Mare — Sabores e inspirações do oceano.</p>
  <p>Projeto desenvolvido em HTML e CSS.</p>
</footer>
</body>
</html>