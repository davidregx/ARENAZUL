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
  background-color: #363a3b;
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
  width: 50px; /* Ajusta el tamaño del logo */
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
  margin-bottom: 20px;
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
  height: auto;
  max-height: 250px;
  object-fit: cover;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Services Section */
.services {
  padding: 50px 30px;
  background-color: #d6f0f1;
  text-align: center;
}

.services h2 {
  font-size: 36px;
  margin-bottom: 30px;
}

.services p {
  font-size: 20px;
  color: #555;
  margin-bottom: 30px;
}

.service-stats {
  display: flex;
  justify-content: space-around;
  margin-bottom: 50px;
}

.stat {
  background-color: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.stat h3 {
  font-size: 48px;
  color: #00A9E0;
}

.stat p {
  font-size: 18px;
  color: #555;
}

.services button {
  padding: 15px 30px;
  font-size: 18px;
  background-color: #ffde00;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

.services button:hover {
  background-color: #00A9E0;
}

/* Testimonials Section */
.testimonials {
  padding: 50px 30px;
  background-color: #d6f0f1;
  text-align: center;
}

.testimonials h2 {
  font-size: 36px;
  margin-bottom: 30px;
}

.testimonial {
  background-color: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
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
  padding: 50px 30px;
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
    grid-template-columns: repeat(2, 1fr); /* Dos columnas */
  }

  .services .service-stats {
    flex-direction: column; /* Coloca los elementos en columna */
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
       <div class="menu-toggle">
    <span></span>
    <span></span>
    <span></span>
  </div>
          <nav>
      <ul>
        <li><a href="#home">Inicio</a></li>
        <li><a href="#services">Servicios</a></li>
        <li><a href="#projects">Proyectos</a></li>
        <li><a href="#testimonials">Testimonios</a></li>
        <li><a href="#contact">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>ARENAZUL: Su Oasis Siempre Listo</h1>
      <p>Disfrute de una piscina cristalina sin el estrés del mantenimiento. Ofrecemos servicios de limpieza y cuidado para propietarios de casas.</p>
      <button>Contáctenos Hoy</button>
    </div>
    <img src="https://txcdn-prod-a1art.xiaopiu.com/assets/images/app_1925013562074480641/1925013562078674945/6656a072-e611-491d-a643-628c73e7e2d6.jpeg?oldPrompt=A crystal-clear swimming pool reflecting the bright sunlight, surrounded by a well-maintained garden, showcasing pristine water and sparkling clean tiles. The pool is inviting and refreshing, with a sense of cleanliness and tranquility. In the background, a modern house can be seen, subtly suggesting the target audience of homeowners. (Emphasis on cleanliness, clarity, and inviting atmosphere:1.2), (no people in the scene), (professional photography)." alt="Piscina ARENAZUL"> <!-- Reemplaza con la URL de tu imagen -->
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

  <!-- Services Section -->
  <section id="services" class="services">
    <h2>Mantenimiento Integral para su Piscina</h2>
    <p>Desde la limpieza profunda hasta el equilibrio químico, nos encargamos de todo. Relájese y disfrute de su piscina mientras nosotros la mantenemos impecable.</p>
    <div class="service-stats">
      <div class="stat">
        <h3>150+</h3>
        <p>Clientes Felices</p>
      </div>
      <div class="stat">
        <h3>5</h3>
        <p>Años de Experiencia</p>
      </div>
      <div class="stat">
        <h3>10+</h3>
        <p>Profesionales Dedicados</p>
      </div>
    </div>
    <button>Descubra Nuestros Servicios</button>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials" class="testimonials">
    <h2>Testimonios</h2>
    <div class="testimonial">
      <p>"¡Desde que contraté a ARENAZUL, mi piscina siempre está lista para disfrutar! El servicio es excelente y el personal muy profesional."</p>
      <p><strong>Ana Rodríguez</strong> - Propietaria de Casa</p>
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="products">
    <h2>Productos Esenciales para el Cuidado de su Piscina</h2>
    <div class="product-gallery">
      <div class="product">
        <img src="https://ceramicorpcenter.pe/wp-content/uploads/2024/05/CLORO-PASTILLAS.jpg" alt="Tabletas de Cloro">
        <p>Tabletas de Cloro - $38.5</p>
        <button>Comprar ahora</button>
      </div>
      <div class="product">
        <img src="https://insumosquimicos.pe/wp-content/uploads/2021/08/Cloro-granulado-.jpg" alt="Cloro Granulado">
        <p>1K Cloro Granulado - $20.0</p>
        <button>Comprar ahora</button>
      </div>
      <div class="product">
        <img src="https://pdcinternacional.co/wp-content/uploads/2023/04/SULFATO-DE-ALUMINIO-TIPO-A-BULTO-25-KG_10_11zon.jpg" alt="Sulfato de Aluminio">
        <p>1K Sulfato de Aluminio - $7.5</p>
        <button>Comprar ahora</button>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <h2>¿Listo para una Piscina Impecable?</h2>
    <p>Obtenga un presupuesto gratuito y descubra cómo podemos ayudarle a mantener su piscina en perfectas condiciones durante todo el año.</p>
    <button>Solicitar Presupuesto</button>
  </section>

  <!-- Footer Section -->
  <footer>
    <div class="footer-content">
      <p>&copy; Piscinas Impecables 2024, Todos los derechos reservados</p>
      <div class="social-media">
        <a href="#">Twitter</a>
        <a href="#">Facebook</a>
        <a href="#">Instagram</a>
        <a href="#">YouTube</a>
      </div>
    </div>
  </footer>
 <script>
    const menuToggle = document.querySelector('.menu-toggle');
    const navMenu = document.querySelector('nav ul');

  menuToggle.addEventListener('click', () => {
      navMenu.classList.toggle('open'); // Alterna la visibilidad del menú
      menuToggle.classList.toggle('open'); // Opcional: Cambia el estilo del ícono de hamburguesa
    });
  </script>

</body>
</html>
