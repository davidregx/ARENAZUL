<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ARENAZUL: Mantenimiento de Piscinas</title>
  <style>
    /* Reset and Global Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

   body {
      font-family: 'Arial', sans-serif;
      line-height: 1.6;
      background-color: #d6f0f1;
    }

    /* Header Section */
   header {
      background-color: #c7c7c2;
      padding: 10px 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-radius: 15px;
      margin: 20px;
      position: relative;
    }

  header .logo {
      display: flex;
      align-items: center;
    }

   header .logo img {
      background-color: transparent;
      width: 80px;
      height: auto;
    }

   nav ul {
      display: flex;
      justify-content: flex-end;
      list-style-type: none;
      padding: 0;
    }

   nav ul li {
      margin-left: 20px;
      font-size: 15px;
    }

   nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      text-transform: uppercase;
    }

   nav ul li a:hover {
      color: #d6f0f1;
    }

    /* Icono flotante del carrito */
   #floating-cart-icon {
      position: fixed;
      top: 30px;
      right: 30px;
      z-index: 1000;
      background-color: #00A9E0;
      color: white;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 24px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      transition: all 0.3s ease;
    }

   #floating-cart-icon:hover {
      background-color: #ffde00;
      transform: scale(1.1);
    }

   #cart-badge {
      position: absolute;
      top: -5px;
      right: -5px;
      background-color: #ff6b6b;
      color: white;
      border-radius: 50%;
      width: 20px;
      height: 20px;
      font-size: 12px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* Hamburguesa */
   .menu-toggle {
      display: none;
      flex-direction: column;
      cursor: pointer;
      margin-left: auto;
    }

   .menu-toggle span {
      background-color: white;
      height: 4px;
      width: 20px;
      margin: 4px 0;
      border-radius: 5px;
    }

    /* Hero Section */
   .hero {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: linear-gradient(to right, #e8fbff, #d6f0f1);
      padding: 10px 20px;
      color: #0f172a;
      text-align: left;
      background-size: cover;
      background-position: center;
    }

   .hero-content h1 {
      font-size: 50px;
      margin-bottom: 0px;
    }

   .hero-content p {
      font-size: 20px;
      margin-bottom: 30px;
    }

   .hero button {
      background-color: #0f172a;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      color: white;
      cursor: pointer;
      border-radius: 5px;
    }

   .hero button:hover {
      background-color: #00A9E0;
    }

   .hero img {
      width: 50%;
      border-radius: 20px 0px 30px 0px;
    }

    /* Projects Section */
   .projects {
      padding: 20px 0;
      background-color: white;
      text-align: center;
    }

   .projects h2 {
      font-size: 36px;
      margin-bottom: 40px;
    }

  .project-gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

   .project-gallery img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    /* Services Section */
   .services {
      padding: 0px 30px;
      text-align: center;
    }

   .service-stats {
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      margin-bottom: 50px;
    }

   .stat {
      padding: 30px;
      width: auto;
    }

   .stat h3 {
      font-size: 48px;
    }

   .stat p {
      font-size: 18px;
    }
    
    /* Sección de servicios */
   section {
      padding: 20px;
      margin: 20px;
    }

    /* Título centrado */
   h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    /* Contenedor de servicios */
   .service {
      display: inline-block;
      width: 48%;
      text-align: center;
      margin: 10px;
      box-sizing: border-box;
    }

    /* Imágenes dentro de los servicios */
  .service img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-radius: 10px;
    }

    /* Testimonials Section */
   .testimonials {
      background-color: #d6f0f1;
      text-align: center;
    }

   .testimonials h2 {
      font-size: 36px;
      margin-bottom: 30px;
    }

   .testimonial img {
      width: 100%;
      border-radius: 20px 0px 30px 0px;
    }

   .testimonial {
      background-color: white;
      padding: 10px;
      border-radius: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
      max-width: 600px;
      margin: 0 auto;
    }

   .testimonial p {
      font-size: 20px;
      color: #555;
      margin-bottom: 20px;
    }

   .testimonial strong {
      font-size: 18px;
      color: #00A9E0;
    }

    /* Products Section */
   .products {
      padding: 20px 20px;
      background-color: white;
      text-align: center;
    }

   .products h2 {
      font-size: 36px;
      margin-bottom: 40px;
    }

   .product-gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

   .product {
      background-color: #f9f9f9;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

   .product img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 20px;
    }

   .product p {
      font-size: 18px;
      color: #333;
      margin-bottom: 20px;
    }

   .product button {
      padding: 10px 20px;
      background-color: #ffde00;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }

   .product button:hover {
      background-color: #00A9E0;
    }

    /* Floating Cart */
   #floating-cart {
      position: fixed;
      top: 100px;
      right: 30px;
      width: 350px;
      padding: 20px;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
      z-index: 9999;
      max-height: 500px;
      overflow-y: auto;
      display: none;
      border: 2px solid #00A9E0;
    }

   #floating-cart h3 {
      margin-bottom: 20px;
      font-size: 22px;
      color: #00A9E0;
      text-align: center;
      border-bottom: 2px solid #eee;
      padding-bottom: 10px;
    }

   #floating-cart ul {
      list-style-type: none;
      padding: 0;
    }

   #floating-cart ul li {
      display: flex;
      align-items: center;
      margin-bottom: 15px;
      font-size: 16px;
      padding-bottom: 15px;
      border-bottom: 1px solid #eee;
    }

   #floating-cart ul li img {
      width: 60px;
      height: 60px;
      margin-right: 10px;
      object-fit: cover;
      border-radius: 5px;
    }

   .cart-item-details {
      flex-grow: 1;
    }

  .cart-item-name {
      font-weight: bold;
    }

   .cart-item-price {
      color: #00A9E0;
    }

   .cart-quantity-controls {
      display: flex;
      align-items: center;
      margin-top: 5px;
    }

   .cart-quantity-controls button {
      width: 30px;
      height: 30px;
      background: #00A9E0;
      color: white;
      border: none;
      border-radius: 50%;
      font-weight: bold;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
    }

  .cart-quantity-controls span {
      margin: 0 10px;
      min-width: 20px;
      text-align: center;
    }

   .remove-item {
      background: none;
      border: none;
      color: #ff6b6b;
      cursor: pointer;
      margin-left: 10px;
      font-size: 20px;
    }

   .cart-total {
      font-size: 20px;
      font-weight: bold;
      text-align: right;
      margin: 20px 0;
      padding-top: 10px;
      border-top: 2px solid #eee;
    }

   .cart-total span {
      color: #00A9E0;
    }

   #checkout-btn {
      padding: 12px 20px;
      background-color: #ffde00;
      color: #333;
      border: none;
      cursor: pointer;
      border-radius: 5px;
      font-size: 16px;
      font-weight: bold;
      width: 100%;
      transition: background-color 0.3s;
    }

   #checkout-btn:hover {
      background-color: #00A9E0;
      color: white;
    }

    /* Contact Section */
   .contact {
      padding: 50px 30px;
      background-color: #d6f0f1;
      text-align: center;
    }

   .contact h2 {
      font-size: 36px;
      margin-bottom: 30px;
    }

   .contact p {
      font-size: 20px;
      color: #555;
      margin-bottom: 30px;
    }

  .contact button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #00A9E0;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }

  .contact button:hover {
      background-color: #ffde00;
    }

    /* Footer Section */
   footer {
      background-color: #00A9E0;
      color: white;
      text-align: center;
      padding: 20px 0;
    }

   .social-media a {
      color: white;
      text-decoration: none;
      margin: 0 10px;
    }

   .social-media a:hover {
      color: #ffde00;
    }

    /* Estilos del pie de página */
   footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 20px;
    }

   footer a {
      color: #fff;
      text-decoration: none;
    }

    /* Estilos adicionales */
   #ubicacion {
      margin-top: 20px;
    }

   #ubicacion h3 {
      font-size: 18px;
      margin-bottom: 10px;
    }

    /* Estilos para el logo */
   .logo img {
      width: 100px;
    }

    /* Notification */
   .notification {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background-color: #00A9E0;
      color: white;
      padding: 15px 30px;
      border-radius: 50px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      z-index: 10000;
      font-weight: bold;
      display: none;
    }
    
    /* ========================================== */
    /* MEJORAS ESPECÍFICAS PARA DISPOSITIVOS MÓVILES */
    /* ========================================== */
    
    /* Prevenir desbordamiento horizontal */
   html, body {
      max-width: 100%;
      overflow-x: hidden;
    }
    
    /* Header para móvil */
 @media (max-width: 768px) {
      header {
        padding: 10px 15px;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin: 10px;
      }

  .logo img {
        width: 50px;
      }

   nav ul {
        display: none;
        flex-direction: column;
        margin-top: 10px;
        width: 100%;
        padding: 10px 0;
        background-color: #363a3b;
        border-radius: 10px;
        position: absolute;
        top: 100%;
        left: 0;
        z-index: 100;
      }

   nav ul li {
        margin: 10px 0;
        font-size: 14px;
        text-align: center;
      }

   nav ul li a {
        font-size: 1rem;
        padding: 8px 0;
        display: block;
      }

  .menu-toggle {
        display: flex;
      }

   nav ul.open {
        display: flex;
      }
      
  #floating-cart-icon {
        top: 20px;
        right: 20px;
        width: 40px;
        height: 40px;
        font-size: 18px;
      }
    }

    /* Hero section para móvil */
   @media (max-width: 768px) {
      .hero {
        flex-direction: column;
        text-align: center;
        padding: 20px 15px;
        margin: 10px;
      }

   .hero-content h1 {
        font-size: 2rem;
        line-height: 1.2;
      }

   .hero-content p {
        font-size: 1.1rem;
        margin-bottom: 20px;
      }

   .hero button {
        padding: 12px 25px;
        font-size: 1rem;
        width: 100%;
        max-width: 300px;
        margin: 10px 0;
      }

   .hero img {
        width: 100%;
        border-radius: 10px;
        margin-top: 20px;
      }
    }

    /* Servicios para móvil */
   @media (max-width: 768px) {
      section {
        margin: 10px;
        padding: 15px;
      }
      
  .service {
        display: block;
        width: 100%;
        margin: 15px 0;
      }
      
   .service img {
        height: 200px;
      }
    }

    /* Proyectos para móvil - 2 en 2 */
   @media (max-width: 768px) {
      .projects {
        margin: 10px;
        padding: 15px 0;
      }
      
   .projects h2 {
        font-size: 1.8rem;
        margin-bottom: 20px;
      }
      
   .project-gallery {
        grid-template-columns: repeat(2, 1fr);
        gap: 10px;
      }
      
   .project-gallery img {
        height: 180px;
      }
    }

    /* Testimonios para móvil */
   @media (max-width: 768px) {
      .testimonials {
        margin: 10px;
        padding: 15px;
      }
      
   .testimonials h2 {
        font-size: 1.8rem;
        margin-bottom: 20px;
      }
      
   .testimonial {
        padding: 15px;
      }
      
   .testimonial p {
        font-size: 1.1rem;
      }
    }

    /* Productos para móvil - 2 en 2 */
   @media (max-width: 768px) {
      .products {
        margin: 10px;
        padding: 15px;
      }
      
  .products h2 {
        font-size: 1.8rem;
        margin-bottom: 20px;
      }
      
   .product-gallery {
        grid-template-columns: repeat(2, 1fr);
        gap: 10px;
      }
      
   .product {
        padding: 15px;
      }
      
  .product p {
        font-size: 1.1rem;
      }
      
   .product button {
        width: 100%;
      }
    }

    /* Contacto para móvil */
   @media (max-width: 768px) {
      .contact {
        margin: 10px;
        padding: 30px 15px;
      }
      
   .contact h2 {
        font-size: 1.8rem;
      }
      
   .contact p {
        font-size: 1.1rem;
      }
      
   .contact button {
        padding: 12px 25px;
        font-size: 1rem;
        width: 100%;
        max-width: 300px;
      }
    }

    /* Carrito para móvil - centrado verticalmente */
   @media (max-width: 768px) {
      #floating-cart {
        width: 90%;
        max-width: 350px;
        padding: 15px;
        top: 50%;
        right: 15px;
        transform: translateY(-50%);
        max-height: 80vh;
      }
    }

    /* Footer para móvil */
 @media (max-width: 768px) {
      footer {
        padding: 15px;
      }
      
  #ubicacion h3 {
        font-size: 1.1rem;
      }
      
  #ubicacion p {
        font-size: 0.95rem;
      }
    }

    /* Estadísticas para móvil */
 @media (max-width: 768px) {
      .services {
        margin: 10px;
        padding: 0 15px;
      }
      
  .service-stats {
        flex-direction: row;
        flex-wrap: wrap;
        margin-bottom: 30px;
      }
      
  .stat {
        flex: 1 0 30%;
        padding: 15px;
        min-width: 120px;
      }
      
  .stat h3 {
        font-size: 2rem;
      }
      
   .stat p {
        font-size: 0.9rem;
      }
    }

    /* Notificación para móvil */
   @media (max-width: 768px) {
      .notification {
        padding: 12px 25px;
        font-size: 0.95rem;
        max-width: 90%;
      }
    }

    /* Ajustes para pantallas muy pequeñas */
  @media (max-width: 480px) {
      .hero-content h1 {
        font-size: 1.8rem;
      }
      
   .projects h2, .services h2, .testimonials h2, 
      .products h2, .contact h2 {
        font-size: 1.6rem;
      }
      
  .stat h3 {
        font-size: 1.8rem;
      }
      
      /* Ajustar a 1 columna en pantallas muy pequeñas */
   @media (max-width: 480px) {
        .project-gallery, .product-gallery {
          grid-template-columns: 1fr;
        }
      }
    }
  </style>
</head>
<body>
  <!-- Icono flotante del carrito - Siempre en la parte superior derecha -->
  <div id="floating-cart-icon">
    🛒
    <div id="cart-badge">0</div>
  </div>
  
  <!-- Header Section -->
  <header>
    <div class="logo">
      <img src="https://cdn.wegic.ai/assets/onepage/thread/icon/1750689479539.png" alt="ARENAZUL Logo">
    </div>
    <div class="menu-toggle" onclick="toggleMenu()">
      <span></span>
      <span></span>
    </div>
    <nav>
      <ul>
        <li><a href="#home">Inicio</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#projects">Proyectos</a></li>
        <li><a href="#testimonials">Testimonios</a></li>
        <li><a href="#contact">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>ARENAZUL</h1>
      <h1>Su Piscina Siempre Limpia</h1>
      <p>Disfrute de una piscina cristalina sin el estrés del mantenimiento. Ofrecemos servicios de limpieza y cuidado para propietarios de casas.</p>
      <button onclick="window.location.href='https://tulink.com';">Contáctenos Hoy</button>
    </div>
    <img src="https://txcdn-prod-a1art.xiaopiu.com/assets/images/app_1925013562074480641/1925013562078674945/6656a072-e611-491d-a643-628c73e7e2d6.jpeg?oldPrompt=A crystal-clear swimming pool reflecting the bright sunlight, surrounded by a well-maintained garden, showcasing pristine water and sparkling clean tiles. The pool is inviting and refreshing, with a sense of cleanliness and tranquility. In the background, a modern house can be seen, subtly suggesting the target audience of homeowners. (Emphasis on cleanliness, clarity, and inviting atmosphere:1.2), (no people in the scene), (professional photography)." alt="Piscina ARENAZUL">
  </section>
  
  <!-- Services Stats Section -->
  <section id="services" class="services">
    <div class="service-stats">
      <div class="stat">
        <h3>50+</h3>
        <p>Clientes Felices</p>
      </div>
      <div class="stat">
        <h3>7</h3>
        <p>AÑOS De Experiencia</p>
      </div>
      <div class="stat">
        <h3>3+</h3>
        <p>Personal Dedicado</p>
      </div>
    </div>
  </section>
  
  <!-- Sección de Servicios -->
  <section id="servicios">
    <h2>Nuestros servicios de limpieza de piscinas</h2>
    <div class="service">
        <img src="https://www.lavanguardia.com/files/image_449_220/uploads/2022/06/15/62a9ad6dd74fb.jpeg" alt="Limpieza básica de piscina">
        <h3>Limpieza básica de piscina</h3>
    </div>
    <div class="service">
        <img src="https://www.tuandco.com/aprendeymejora/wp-content/uploads/2020/04/principal.jpg" alt="Mantenimiento semanal de piscina">
        <h3>Mantenimiento semanal de piscina</h3>
    </div>
    <div class="service">
        <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YVIBZKeG3P0bh4GMiaCE6Vs_GuVz3pLWvFTmNnEdEgmIH6wGXXIFcNf4vRCoVbg8rkLztjS04R9fL_zsf956Nyin8dnQabBxbt-eVZy9n7g5x2Zegs7o4p1hANSBbcvKY-CpqRfRUiwHOJ1=w4000-h3000-p-k-no" alt="Limpieza intensiva de piscina">
        <h3>Limpieza intensiva de piscina</h3>
    </div>
    <div class="service">
        <img src="https://nautilusbr.com/dev/wp-content/uploads/close-up-de-mao-segurando-fita-de-medicao-de-ph-na-agua-da-piscina.jpeg" alt="Tratamiento de agua de piscina">
        <h3>Tratamiento de agua de piscina</h3>
    </div>
    <div class="service">
        <img src="https://www.hidrotec.com/wp-content/uploads/2024/01/preparar-piscina-verano.webp" alt="Puesta a punto de piscina">
        <h3>Puesta a punto de piscina</h3>
    </div>
  </section>

  <!-- Our Projects Section -->
  <section id="projects" class="projects">
    <h2>Nuestros Proyectos Recientes</h2>
    <div class="project-gallery">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YWTgWhMgCINg0P7MCRvFQ6S_2pjcHDxa0cGAqcu8sdChfAU5i5gX1RFxVovDp3MIxJ5UBeuacjPrHWbEvUI4nUSXVWShUJXGqH9a5nXzexSZDha55Xy2oUl0eWnkWxSS056mG7SSF8Vfm0=w3840-h2160-p-k-no" alt="Proyecto 1">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YWTgWhMgCINg0P7MCRvFQ6S_2pjcHDxa0cGAqcu8sdChfAU5i5gX1RFxVovDp3MIxJ5UBeuacjPrHWbEvUI4nUSXVWShUJXGqH9a5nXzexSZDha55Xy2oUl0eWnkWxSS056mG7SSF8Vfm0=w3840-h2160-p-k-no" alt="Proyecto 2">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YXRadNFxZwk-GjtcE5qCL4sILUiGbaS-xzHM8V30PhbIX_mOahPqyQmxIajXIyKjA5rcQtTIOFrY-dIXafAwD8qolFwVA3eDEWKtJKxZadhbGTLsPOl0bC9RPJwKSyMtH178_2wFImqK_kn=w4160-h3120-p-k-no" alt="Proyecto 3">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YXbcEZDRS2R4BlH1aIecDNpKgdSKlomaJJ-IZ_RGvv1F-zE8VJ-zCW4RyKbSSvxt7VFPkME-171ong9ulOOb2ouIpsb5NOwLUEoMj7E3OAbfGsNi65WLE_AY_Oyod0ZIPXu2RSLroCZCAu8=w4160-h3120-p-k-no" alt="Proyecto 4">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YWhbbPVB7G5IqJrstFiNOsmhQuRlXVeWgKxSAdMKsWrmKsVniqxDxtnrQSPxOZa3dZlq2gyJ3A7B2MC_tKjCfMmh9p7PkM0TGhKvxvgYd6uokFSZEwe_LUdJvqeulRd4AQWp9DzfkiDIOkI=w4608-h3456-p-k-no" alt="Proyecto 5">
      <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YWglv-HM0EpZ0Rrfm3_LA_Pd3oAU9WVk12GZL1qUNG9PHxOXJ2DdCeqyIQ6gb46_R-9YzLhw6O_Vmy8YX9DFeGrtRW7Qo6BLtIQB7g3T5l-pC7A6m6DfbUY9gCC7i2T7ruvIF6invi2Uwhg=w4608-h3456-p-k-no" alt="Proyecto 6">
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials" class="testimonials">
    <h2>Testimonios</h2>
    <div class="testimonial">
      <p>"¡Desde que contraté a ARENAZUL, mi piscina siempre está lista para disfrutar! El servicio es excelente y el personal muy profesional."</p>
      <img src="https://txcdn-prod-a1art.xiaopiu.com/assets/images/app_1925013562074480641/1925013562078674945/84d609b0-2f3d-4459-b9b7-6b3f0df73055.jpeg?oldPrompt=A serene and crystal-clear swimming pool reflecting the bright sky, surrounded by a well-maintained patio with comfortable lounge chairs, showcasing the joy and satisfaction of happy homeowners (trustworthy:1.2), suggesting relaxation and a carefree lifestyle (professional:1.1), pristine water (clean:1.3), natural sunlight, enhancing the inviting ambiance, no visible cleaning equipment" alt="Cliente satisfecho">
      <p><strong>Ana Rodríguez</strong> - Propietaria de Casa</p>
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="products">
    <h2>Productos Esenciales para el Cuidado de su Piscina</h2>
    <div class="product-gallery">
      <div class="product">
        <img src="https://ceramicorpcenter.pe/wp-content/uploads/2024/05/CLORO-PASTILLAS.jpg" alt="Tabletas de Cloro">
        <p>Tabletas de Cloro (1kg) S/38.50</p>
        <button onclick="addToCart('Tabletas de Cloro', 38.50, 'https://ceramicorpcenter.pe/wp-content/uploads/2024/05/CLORO-PASTILLAS.jpg')">Agregar 1kg</button>
      </div>
      <div class="product">
        <img src="https://insumosquimicos.pe/wp-content/uploads/2021/08/Cloro-granulado-.jpg" alt="Cloro Granulado">
        <p>Cloro Granulado (1kg) S/20.00</p>
        <button onclick="addToCart('Cloro Granulado', 20.00, 'https://insumosquimicos.pe/wp-content/uploads/2021/08/Cloro-granulado-.jpg')">Agregar 1kg</button>
      </div>
      <div class="product">
        <img src="https://aquagardens.com.ec/wp-content/uploads/2021/07/AQUA-7-800x800-1.jpg" alt="Sulfato de Aluminio">
        <p>Sulfato de Aluminio (1kg) S/7.50</p>
        <button onclick="addToCart('Sulfato de Aluminio', 7.50, 'https://aquagardens.com.ec/wp-content/uploads/2021/07/AQUA-7-800x800-1.jpg')">Agregar 1kg</button>
      </div>
      <div class="product">
        <img src="https://sulcosa.b-cdn.net/wp-content/uploads/2024/04/Sulfato-de-cobre-pentahidratado.webp" alt="Sulfato de Cobre">
        <p>Sulfato de Cobre (1kg) S/26.00</p>
        <button onclick="addToCart('Sulfato de Cobre', 26.00, 'https://sulcosa.b-cdn.net/wp-content/uploads/2024/04/Sulfato-de-cobre-pentahidratado.webp')">Agregar 1kg</button>
      </div>
    </div>
  </section>

  <!-- Floating Cart Section -->
  <div id="floating-cart">
    <h3>Carrito de Compras</h3>
    <ul id="cart-list"></ul>
    <div class="cart-total">Total: <span id="cart-total">S/0.00</span></div>
    <button id="checkout-btn" onclick="checkout()">Realizar pedido</button>
  </div>
  
  <!-- Notification -->
  <div class="notification" id="notification"></div>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <h2>¿Listo para una Piscina Impecable?</h2>
    <p>Obtenga un presupuesto gratuito y descubra cómo podemos ayudarle a mantener su piscina en perfectas condiciones durante todo el año.</p>
     <button onclick="window.location.href='https://tulink.com';">Solicitar Presupuesto</button>
  </section>
  
  <!-- Sección de ubicación -->
  <footer>
    <div id="ubicacion">
      <h3>Ubicación</h3>
      <p>A.V PERU AA, HH PUEBLO NUEVO SIN NÚMERO</p>
      <p>Contacto: <a href="mailto:davidregx@gmail.com">davidregx@gmail.com</a></p>
    </div>
  </footer>

  <!-- Footer Section -->
  <footer>
    <div class="footer-content">
      <p>&copy; Piscinas Impecables 2024, Todos los derechos reservados</p>
    </div>
  </footer>

  <script>
    // Variables globales
    let cart = [];
    let cartVisible = false;

    // Funciones del carrito
    function addToCart(productName, productPrice, productImage) {
      // Verificar si el producto ya está en el carrito
      const existingItem = cart.find(item => item.name === productName);
      
      if (existingItem) {
        // Incrementar en 1kg (1 unidad)
        existingItem.quantity++;
      } else {
        // Agregar nuevo producto (1kg)
        cart.push({ 
          name: productName, 
          price: productPrice, 
          image: productImage, 
          quantity: 1 
        });
      }
      
      updateCart();
      showNotification(`1kg de ${productName} añadido al carrito`);
      
      // Mantener el carrito abierto después de añadir
      document.getElementById('floating-cart').style.display = 'block';
      cartVisible = true;
    }

    function updateCart() {
      const cartList = document.getElementById('cart-list');
      const cartTotalElement = document.getElementById('cart-total');
      const cartBadge = document.getElementById('cart-badge');
      let total = 0;
      let itemCount = 0;
      
      cartList.innerHTML = '';
      
      cart.forEach((item, index) => {
        const li = document.createElement('li');
        const itemTotal = item.price * item.quantity;
        total += itemTotal;
        itemCount += item.quantity;
        
        li.innerHTML = `
          <img src="${item.image}" alt="${item.name}">
          <div class="cart-item-details">
            <p class="cart-item-name">${item.name}</p>
            <p class="cart-item-price">S/${item.price.toFixed(2)}/kg</p>
            <div class="cart-quantity-controls">
              <button onclick="changeQuantity(${index}, -1, event)">-</button>
              <span>${item.quantity} kg</span>
              <button onclick="changeQuantity(${index}, 1, event)">+</button>
            </div>
          </div>
          <button class="remove-item" onclick="removeFromCart(${index}, event)">×</button>
        `;
        
        cartList.appendChild(li);
      });
      
      cartTotalElement.textContent = `S/${total.toFixed(2)}`;
      cartBadge.textContent = itemCount;
      
      // Mostrar carrito si hay productos
      if (cart.length > 0 && !cartVisible) {
        document.getElementById('floating-cart').style.display = 'block';
        cartVisible = true;
      }
    }

    function changeQuantity(index, change, event) {
      // Detener la propagación del evento para evitar que se cierre el carrito
      event.stopPropagation();
      
      // Cambiar la cantidad en kg
      cart[index].quantity += change;
      
      // Si la cantidad es 0 o menos, eliminar el producto
      if (cart[index].quantity <= 0) {
        cart.splice(index, 1);
      }
      
      updateCart();
    }

    function removeFromCart(index, event) {
      // Detener la propagación del evento para evitar que se cierre el carrito
      event.stopPropagation();
      
      cart.splice(index, 1);
      updateCart();
      
      if (cart.length === 0) {
        document.getElementById('floating-cart').style.display = 'none';
        cartVisible = false;
      }
    }

    function toggleCart() {
      const cartElement = document.getElementById('floating-cart');
      
      if (cart.length === 0) {
        showNotification("El carrito está vacío");
        return;
      }
      
      if (cartElement.style.display === 'block') {
        cartElement.style.display = 'none';
        cartVisible = false;
      } else {
        cartElement.style.display = 'block';
        cartVisible = true;
      }
    }

    function checkout() {
      if (cart.length === 0) {
        showNotification("El carrito está vacío");
        return;
      }
      
      let message = "¡Hola ARENAZUL! Quiero hacer un pedido de productos para piscina:\n\n";
      let total = 0;
      
      cart.forEach(item => {
        const itemTotal = item.price * item.quantity;
        total += itemTotal;
        message += `- ${item.name}: ${item.quantity} kg - S/${itemTotal.toFixed(2)}\n`;
      });
      
      message += `\nTotal: S/${total.toFixed(2)}`;
      
      const whatsappUrl = `https://wa.me/51999999999?text=${encodeURIComponent(message)}`;
      window.open(whatsappUrl, '_blank');
    }

    // Funciones auxiliares
    function showNotification(message) {
      const notification = document.getElementById('notification');
      notification.textContent = message;
      notification.style.display = 'block';
      
      setTimeout(() => {
        notification.style.transition = 'opacity 0.5s';
        notification.style.opacity = '0';
        setTimeout(() => {
          notification.style.display = 'none';
          notification.style.opacity = '1';
        }, 500);
      }, 3000);
    }

    // Menú móvil
    function toggleMenu() {
      const navMenu = document.querySelector('nav ul');
      navMenu.classList.toggle('open');
    }

    // Cerrar carrito al hacer clic fuera de él
    document.addEventListener('click', function(event) {
      const cartElement = document.getElementById('floating-cart');
      const cartIcon = document.getElementById('floating-cart-icon');
      
      // Verificar si el clic fue fuera del carrito y fuera del icono del carrito
      if (cartVisible && 
          !cartElement.contains(event.target) && 
          event.target !== cartIcon &&
          !cartIcon.contains(event.target)) {
        cartElement.style.display = 'none';
        cartVisible = false;
      }
    });

    // Inicializar
    document.getElementById('floating-cart-icon').addEventListener('click', toggleCart);
    
    // Prevenir el desplazamiento horizontal en móvil
    window.addEventListener('resize', function() {
      if (window.innerWidth < 768) {
        document.body.style.overflowX = 'hidden';
      } else {
        document.body.style.overflowX = 'auto';
      }
    });
    
    // Ajustar posición del carrito al desplazar
    window.addEventListener('scroll', function() {
      if (window.innerWidth < 768 && cartVisible) {
        const cartElement = document.getElementById('floating-cart');
        cartElement.style.top = '50%';
        cartElement.style.transform = 'translateY(-50%)';
      }
    });
  </script>
</body>
</html>
