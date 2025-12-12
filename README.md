<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Lar & Meu - Especial de Natal</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f2f2f2;
    }

    /* Logo */
    header {
      background: #c40000 url('https://images.unsplash.com/photo-1607082349566-187342175e2f?w=1600');
      background-size: cover;
      color: white;
      padding: 30px;
      text-align: center;
      font-size: 32px;
      font-weight: bold;
      text-shadow: 2px 2px 5px black;
    }

    /* Menu */
    nav {
      background: #fff;
      padding: 15px;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
      font-size: 18px;
      border-bottom: 2px solid #ddd;
    }
    nav a {
      text-decoration: none;
      color: #c40000;
      font-weight: bold;
    }

    /* Search Bar */
    #search {
      margin: 20px auto;
      max-width: 600px;
      display: flex;
      gap: 10px;
    }
    #search input {
      flex: 1;
      padding: 12px;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    #search button {
      padding: 12px 20px;
      border: none;
      border-radius: 10px;
      background: #c40000;
      color: white;
      cursor: pointer;
    }

    /* Popup */
    #popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
      justify-content: center;
      align-items: center;
    }
    #popup-content {
      background: white;
      padding: 25px;
      border-radius: 15px;
      text-align: center;
      width: 90%;
      max-width: 350px;
    }
    #popup button {
      background: #c40000;
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      color: white;
      border-radius: 10px;
      cursor: pointer;
    }

    .banner {
      background: url('https://images.unsplash.com/photo-1544457070-4cd773b4d71e?w=1600');
      background-size: cover;
      height: 250px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 35px;
      font-weight: bold;
      text-shadow: 2px 2px 5px black;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 25px;
    }

    .title-section {
      font-size: 26px;
      margin-bottom: 20px;
      color: #c40000;
      font-weight: bold;
      text-align:center;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .card {
      background: white;
      padding: 15px;
      border-radius: 15px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.2);
      text-align: center;
      transition: transform .2s;
    }

    .card:hover {
      transform: scale(1.03);
    }

    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 10px;
    }

    .price {
      font-size: 20px;
      color: green;
      font-weight:bold;
    }
    .old-price {
      text-decoration: line-through;
      color: gray;
    }

    /* Footer */
    footer {
      background: #c40000;
      color: white;
      padding: 25px;
      text-align: center;
      margin-top: 40px;
    }

    /* Mobile Optimization */
    @media (max-width: 600px) {
      header { font-size: 24px; }
      nav { font-size: 16px; }
      .banner { font-size: 24px; height: 180px; }
    }
  </style>
</head>
<body>

<!-- POPUP -->
<div id="popup">
  <div id="popup-content">
    <h2>🎄 Oferta Exclusiva de Natal!</h2>
    <p>Use o cupom <b>NATAL10</b> e ganhe 10% OFF!</p>
    <button onclick="closePopup()">Fechar</button>
  </div>
</div>

<header>Lar & Meu 🎄 Super Especial de Natal</header>

<nav>
  <a href="#home">Home</a>
  <a href="#produtos">Produtos</a>
  <a href="#ofertas">Ofertas</a>
  <a href="#contato">Contato</a>
</nav>

<!-- MENU SECUNDÁRIO (IGUAL GRANDES LOJAS) -->
<nav style="background:#fff;padding:12px;display:flex;justify-content:center;gap:30px;border-bottom:2px solid #eee;font-size:17px;">
  <a href="#pagamento">Pagamento</a>
  <a href="#minhaconta">Minha Conta</a>
  <a href="#suporte">Suporte</a>
</nav>


<!-- SEARCH BAR -->
<div id="search">
  <input type="text" id="searchInput" placeholder="Buscar produtos...">
  <button onclick="searchProduct()">Buscar</button>
</div>

<!-- SEÇÕES NOVAS TIPO GRANDES LOJAS -->
<div class="container" id="pagamento" style="margin-top:30px;">
  <div class="title-section">💳 Formas de Pagamento</div>
  <p>Aceitamos PIX, cartão de crédito e débito com segurança total no site.</p>
</div>

<div class="container" id="minhaconta">
  <div class="title-section">👤 Minha Conta</div>
  <p>Consulte pedidos, acompanhe entregas e veja dados da sua conta.</p>
</div>

<div class="container" id="suporte">
  <div class="title-section">📞 Suporte ao Cliente</div>
  <p>Atendimento rápido via chat integrado diretamente no site.</p>
</div>

<!-- ÁREA DE LOGIN / MINHA CONTA COMPLETA -->
<div class="container" id="login" style="background:white;padding:25px;border-radius:15px;box-shadow:0 3px 8px rgba(0,0,0,0.2);margin-top:30px;">
  <div class="title-section">🔐 Acessar Minha Conta</div>
  <input type="text" placeholder="E-mail" style="width:100%;padding:12px;border-radius:10px;border:1px solid #ccc;margin-bottom:10px;">
  <input type="password" placeholder="Senha" style="width:100%;padding:12px;border-radius:10px;border:1px solid #ccc;margin-bottom:10px;">
  <button style="width:100%;padding:12px;border:none;background:#c40000;color:white;border-radius:10px;font-size:18px;cursor:pointer;">Entrar</button>
</div>

<!-- CARRINHO DE COMPRAS -->
<div class="container" id="carrinho">
  <div class="title-section">🛒 Meu Carrinho</div>
  <p>Nenhum item no carrinho ainda.</p>
</div>

<!-- PÁGINA INDIVIDUAL DE PRODUTO (MODELO) -->
<div class="container" id="produto-exemplo" style="background:white;padding:20px;border-radius:15px;box-shadow:0 3px 8px rgba(0,0,0,0.2);">
  <div class="title-section">📦 Página de Produto (Exemplo)</div>
  <img src="https://images.unsplash.com/photo-1601040043675-62b1f3fda3a4?w=800" style="width:100%;max-width:400px;border-radius:10px;margin:auto;display:block;">
  <h2>Panela Antiaderente Premium</h2>
  <p class="old-price">R$ 149,90</p>
  <p class="price">R$ 89,90</p>
  <button style="padding:12px 20px;background:#c40000;color:white;border:none;border-radius:10px;cursor:pointer;">Adicionar ao Carrinho</button>
</div>

<!-- AVALIAÇÕES DE CLIENTES -->
<div class="container" id="avaliacoes">
  <div class="title-section">⭐ Avaliações de Clientes</div>
  <div style="background:white;padding:15px;border-radius:10px;margin-bottom:10px;box-shadow:0 2px 5px rgba(0,0,0,0.2);">
    <b>Maria S.</b><br>⭐ ⭐ ⭐ ⭐ ⭐<br>Ótima qualidade! Chegou rápido.
  </div>
  <div style="background:white;padding:15px;border-radius:10px;margin-bottom:10px;box-shadow:0 2px 5px rgba(0,0,0,0.2);">
    <b>João P.</b><br>⭐ ⭐ ⭐ ⭐<br>Produto muito bom, recomendo.
  </div>
</div>

<!-- Rastreamento de Pedido -->
<div class="container" id="rastreamento">
  <div class="title-section">🚚 Rastreamento de Pedido</div>
  <input type="text" placeholder="Digite o código de rastreamento..." style="width:100%;padding:12px;border-radius:10px;border:1px solid #ccc;margin-bottom:10px;">
  <button style="width:100%;padding:12px;background:#c40000;border:none;color:white;border-radius:10px;font-size:18px;cursor:pointer;">Rastrear</button>
</div>

<div class="banner">Ofertas Incríveis de Natal 🎅✨</div>

<div class="container" id="produtos">
  <div class="title-section">🎁 Produtos com Mega Descontos 🎁</div>

  <div class="grid" id="productGrid">
    <!-- Produtos são filtráveis pelo buscador -->

    <div class="card" data-name="Panela Antiaderente">
      <img src="https://images.unsplash.com/photo-1601040043675-62b1f3fda3a4?w=800" />
      <h3>Panela Antiaderente Premium</h3>
      <p class="old-price">R$ 149,90</p>
      <p class="price">R$ 89,90</p>
    </div>

    <div class="card" data-name="Utensílios de Silicone">
      <img src="https://images.unsplash.com/photo-1616627987399-0cb57e7d4689?w=800" />
      <h3>Kit Utensílios de Silicone</h3>
      <p class="old-price">R$ 79,90</p>
      <p class="price">R$ 39,90</p>
    </div>

    <div class="card" data-name="Panelas Inox">
      <img src="https://images.unsplash.com/photo-1585409677983-0641c8e6df6e?w=800" />
      <h3>Jogo de Panelas Inox</h3>
      <p class="old-price">R$ 499,90</p>
      <p class="price">R$ 349,90</p>
    </div>

    <div class="card" data-name="Airfryer">
      <img src="https://images.unsplash.com/photo-1610440042657-6122a51bc0de?w=800" />
      <h3>Airfryer 4L - Edição Natal</h3>
      <p class="old-price">R$ 599,90</p>
      <p class="price">R$ 449,90</p>
    </div>
