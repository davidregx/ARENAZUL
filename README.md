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
}

header .logo {
  display: flex;
  align-items: center;
}

header .logo img {
  background-color: transparent;
  width: 80px; /* Ajusta el tamaño del logo */
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

/* Hamburguesa */
.menu-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
  margin-left: auto; /* Empuja la hamburguesa al extremo derecho */
}

.menu-toggle span {
  background-color: white;
  height: 4px;
  width: 20px; /* Ajusta el tamaño del ícono */
  margin: 4px 0;
  border-radius: 5px;
}

/* Adaptación para móviles */
@media (max-width: 768px) {
  header {
    padding: 10px 15px;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .logo img {
    width: 40px; /* Ajusta el tamaño del logo para pantallas pequeñas */
  }

  nav ul {
    display: none; /* Oculta el menú en pantallas pequeñas */
    flex-direction: column;
    margin-top: 10px;
    width: 100%;
    padding: 10px 0;
    background-color: #363a3b;
    border-radius: 10px;
  }

  nav ul li {
    margin: 10px 0;
    font-size: 14px;
    text-align: center;
  }

  .menu-toggle {
    display: flex; /* Muestra el ícono de hamburguesa */
  }

  nav ul.open {
    display: flex; /* Muestra el menú cuando la clase 'open' se añade */
  }
}

@media (max-width: 480px) {
  header {
    padding: 10px 10px;
  }

  .logo img {
    width: 35px; /* Ajusta el logo para pantallas muy pequeñas */
  }

  nav ul li {
    font-size: 12px;
    margin: 8px 0;
  }
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
  height: 250px; /* Altura fija para todas las imágenes */
  object-fit: cover; /* Mantiene la proporción sin distorsionar */
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
    flex-direction: column; /* En pantallas grandes los elementos estarán en una columna */
    justify-content: space-around;
    margin-bottom: 50px;
  }

  .stat {
    padding: 30px;
    width: auto; /* Ajuste automático en pantallas grandes */
  }

  .stat h3 {
    font-size: 48px;
  }

  .stat p {
    font-size: 18px;
  }
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
    width: 48%; /* Ajustamos el ancho para que haya espacio entre las imágenes */
    text-align: center;
    margin: 10px;
    box-sizing: border-box;
}

/* Imágenes dentro de los servicios */
.service img {
    width: 100%;
    height: 250px; /* Altura fija para todas las imágenes */
    object-fit: cover; /* Asegura que la imagen cubra el área sin distorsionarse */
    border-radius: 10px;
}

/* Estilos para dispositivos móviles */
@media (max-width: 768px) {
    .service {
        width: 38%; /* Dos imágenes por fila */
    }
    
    /* Centramos la sección */
   section {
        text-align: center;
    }
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
      bottom: 20px;
      right: 20px;
      width: 300px;
      padding: 20px;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      z-index: 9999;
      max-height: 400px;
      overflow-y: auto;
      display: none; /* Inicialmente oculto */
    }

   #floating-cart h3 {
      margin-bottom: 20px;
      font-size: 22px;
      color: #333;
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
    }

  #floating-cart ul li img {
      width: 60px;
      height: 60px;
      margin-right: 10px;
      object-fit: cover;
      border-radius: 5px;
    }

  #floating-cart button {
      padding: 12px 20px;
      background-color: #00A9E0;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
      font-size: 16px;
    }

  #floating-cart button:hover {
      background-color: #ffde00;
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

/* Responsividad para pantallas más pequeñas */
@media (max-width: 768px) {
  .hero {
    flex-direction: column; /* Coloca la imagen y el texto en columna */
    text-align: center;
  }

  .hero img {
    width: 80%; /* Ajusta el tamaño de la imagen */
    margin-top: 20px;
  }

  .projects .project-gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Dos columnas */
    gap: 10px;
  }

  .services .service-stats {
    flex-direction: row; /* Coloca los elementos en columna */
    align-items: center;
  }

  .product-gallery {
    grid-template-columns: repeat(2, 1fr); /* Dos columnas */
  }

  .testimonial {
    max-width: 90%; /* Ajusta el tamaño del testimonio */
  }

  .contact button {
    width: 100%; /* Hace que el botón ocupe todo el ancho */
  }

  .product button {
    width: 100%; /* Hace que el botón ocupe todo el ancho */
  }

  .stat {
    width: 100%; /* Hace que los stats ocupen el 100% */
    margin-bottom: 20px;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 10px 15px;
  }

  .hero img {
    width: 100%; /* Hace que la imagen ocupe todo el ancho */
  }

  .projects h2 {
    font-size: 28px; /* Ajusta el tamaño del título */
  }

  .services h2, .testimonials h2, .products h2, .contact h2 {
    font-size: 28px; /* Ajusta el tamaño de los títulos */
  }

  .services p, .testimonials p, .products p, .contact p {
    font-size: 16px; /* Ajusta el tamaño del texto */
  }

  .services button, .testimonial button, .contact button {
    font-size: 16px; /* Ajusta el tamaño del botón */
    padding: 12px 24px;
  }

  .stat h3 {
    font-size: 36px; /* Ajusta el tamaño de los números */
  }

  .testimonial {
    padding: 20px;
  }

  .product-gallery {
    grid-template-columns: 1fr; /* Una columna */
  }

  .product {
    padding: 15px; /* Reduce el padding */
  }
}
  </style></head>
<body>
  <!-- Header Section -->
  <header>
    <div class="logo">
      <img src="https://cdn.wegic.ai/assets/onepage/thread/icon/1750689479539.png" alt="ARENAZUL Logo"> <!-- Reemplaza con la URL de tu logo -->
    </div>
    <!-- Agregar el ícono del carrito en el menú -->
        <li><button class="cart-icon" onclick="toggleCart()">🛒</button></li>
       <div class="menu-toggle">
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
    <img src="https://txcdn-prod-a1art.xiaopiu.com/assets/images/app_1925013562074480641/1925013562078674945/6656a072-e611-491d-a643-628c73e7e2d6.jpeg?oldPrompt=A crystal-clear swimming pool reflecting the bright sunlight, surrounded by a well-maintained garden, showcasing pristine water and sparkling clean tiles. The pool is inviting and refreshing, with a sense of cleanliness and tranquility. In the background, a modern house can be seen, subtly suggesting the target audience of homeowners. (Emphasis on cleanliness, clarity, and inviting atmosphere:1.2), (no people in the scene), (professional photography)." alt="Piscina ARENAZUL"> <!-- Reemplaza con la URL de tu imagen -->
    
     <!-- Services Section -->
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
            <img src="https://lh3.googleusercontent.com/gps-cs/AIky0YVIBZKeG3P0bh4GMiaCE6Vs_GuVz3pLWvFTmNnEdEgmIH6wGXXIFcNf4vRCoVbg8rkLztjS04R9fL_zsf956Nyin8dnQabBxbt-eVZy9n7g5x2Zegs7o4p1hANSBbcvKY-CpqRfRUiwHOJ1=w4000-h3000-p-k-no">
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
      <img src="https://txcdn-prod-a1art.xiaopiu.com/assets/images/app_1925013562074480641/1925013562078674945/84d609b0-2f3d-4459-b9b7-6b3f0df73055.jpeg?oldPrompt=A serene and crystal-clear swimming pool reflecting the bright sky, surrounded by a well-maintained patio with comfortable lounge chairs, showcasing the joy and satisfaction of happy homeowners (trustworthy:1.2), suggesting relaxation and a carefree lifestyle (professional:1.1), pristine water (clean:1.3), natural sunlight, enhancing the inviting ambiance, no visible cleaning equipment">
      <p><strong>Ana Rodríguez</strong> - Propietaria de Casa</p>
    </div>
  </section>


  <!-- Products Section -->
  <section id="products" class="products">
    <h2>Productos Esenciales para el Cuidado de su Piscina</h2>
    <div class="product-gallery">
      <div class="product">
        <img src="https://ceramicorpcenter.pe/wp-content/uploads/2024/05/CLORO-PASTILLAS.jpg" alt="Tabletas de Cloro">
        <p>Tabletas de Cloro  S/38.50</p>
        <button onclick="addToCart('Tabletas de Cloro', 38.50, 'https://ceramicorpcenter.pe/wp-content/uploads/2024/05/CLORO-PASTILLAS.jpg')">Agregar al carrito</button>
      </div>
      <div class="product">
        <img src="https://insumosquimicos.pe/wp-content/uploads/2021/08/Cloro-granulado-.jpg" alt="Cloro Granulado">
        <p>1K Cloro Granulado  S/20.00</p>
        <button onclick="addToCart('Cloro Granulado', 20.00, 'https://insumosquimicos.pe/wp-content/uploads/2021/08/Cloro-granulado-.jpg')">Agregar al carrito</button>
      </div>
      <div class="product">
        <img src="https://aquagardens.com.ec/wp-content/uploads/2021/07/AQUA-7-800x800-1.jpg" alt="Sulfato de Aluminio">
        <p>1K Sulfato de Aluminio S/7.50</p>
        <button onclick="addToCart('Sulfato de Aluminio', 7.50, 'https://aquagardens.com.ec/wp-content/uploads/2021/07/AQUA-7-800x800-1.jpg')">Agregar al carrito</button>
      </div>
      <div class="product">
        <img src="https://sulcosa.b-cdn.net/wp-content/uploads/2024/04/Sulfato-de-cobre-pentahidratado.webp" alt="Sulfato de Cobre">
        <p>1K Sulfato de Cobre  S/26.00</p>
        <button onclick="addToCart('Sulfato de Cobre', 26.00, 'https://sulcosa.b-cdn.net/wp-content/uploads/2024/04/Sulfato-de-cobre-pentahidratado.webp')">Agregar al carrito</button>
      </div>
    </div>
  </section>

  <!-- Floating Cart Section -->
  <div id="floating-cart">
    <h3>Carrito de Compras</h3>
    <ul id="cart-list"></ul>
    <button onclick="checkout()">Realizar pedido</button>
  </div>

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
    const menuToggle = document.querySelector('.menu-toggle');
    const navMenu = document.querySelector('nav ul');

  menuToggle.addEventListener('click', () => {
      navMenu.classList.toggle('open'); // Alterna la visibilidad del menú
      menuToggle.classList.toggle('open'); // Opcional: Cambia el estilo del ícono de hamburguesa
    });
    
    
 let cart = [];

 function addToCart(productName, productPrice, productImage) {
      cart.push({ name: productName, price: productPrice, image: productImage, quantity: 1 });
      displayCart();
    }

 function displayCart() {
      const cartList = document.getElementById('cart-list');
      const floatingCart = document.getElementById('floating-cart');
      cartList.innerHTML = '';

 cart.forEach((item, index) => {
  const li = document.createElement('li');
   li.innerHTML = `
  <img src="${item.image}" alt="${item.name}"> 
  ${item.name} - S/${item.price} x ${item.quantity} 
 <button onclick="increaseQuantity(${index})">+</button>
  <button onclick="decreaseQuantity(${index})">-</button>
  <button onclick="removeFromCart(${index})">Eliminar</button>
        `;
        cartList.appendChild(li);
      });

   floatingCart.style.display = cart.length > 0 ? 'block' : 'none';
    }

  function increaseQuantity(index) {
      cart[index].quantity++;
      displayCart();
    }

   function decreaseQuantity(index) {
      if (cart[index].quantity > 1) {
        cart[index].quantity--;
      }
      displayCart();
    }

  function removeFromCart(index) {
      cart.splice(index, 1);
      displayCart();
    }

  function checkout() {
      let message = 'Pedido a través de ARENAZUL:\n';
      cart.forEach(item => {
        message += `${item.name} - S/${item.price} x ${item.quantity}\n`;
      });
      const whatsappUrl = `https://wa.me/573005555555?text=${encodeURIComponent(message)}`;
      window.open(whatsappUrl, '_blank');
    }

   function toggleCart() {
      const floatingCart = document.getElementById('floating-cart');
      floatingCart.style.display = floatingCart.style.display === 'none' ? 'block' : 'none';
    }

  function toggleMenu() {
      const navMenu = document.querySelector('nav ul');
      navMenu.classList.toggle('open');
    }
  </script>

</body>
</html>
