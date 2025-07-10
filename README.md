<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.6">
    <title>Restaurantes Los Órganos - Delivery & Reservas</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <!-- Leaflet CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

  body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

  .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }

  .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

  .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

   .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #333;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

  .logo i {
            color: #ff6b6b;
        }

  .search-bar {
            flex: 1;
            max-width: 400px;
            margin: 0 2rem;
            position: relative;
        }

  .search-input {
            width: 100%;
            padding: 0.8rem 1rem 0.8rem 2.5rem;
            border: none;
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.9);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

  .search-input:focus {
            outline: none;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            transform: translateY(-2px);
        }

  .search-icon {
            position: absolute;
            left: 1rem;
            top: 50%;
            transform: translateY(-50%);
            color: #666;
        }

   .filters {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }

   .filter-btn {
            padding: 0.5rem 1rem;
            border: none;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.9);
            color: #333;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

  .filter-btn:hover, .filter-btn.active {
            background: #ff6b6b;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(255, 107, 107, 0.3);
        }

  .main-content {
            display: grid;
            grid-template-columns: 1fr 400px;
            gap: 2rem;
            margin-top: 2rem;
        }

  .restaurants-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

  .restaurant-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            display: flex;
            flex-direction: column;
            height: 100%;
        }

  .restaurant-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

  .restaurant-image-container {
            width: 100%;
            height: 200px;
            position: relative;
            overflow: hidden;
        }
        
  .restaurant-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }
        
  .restaurant-card:hover .restaurant-image {
            transform: scale(1.05);
        }

   .restaurant-info {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

   .restaurant-name {
            font-size: 1.3rem;
            font-weight: bold;
            color: #333;
            margin-bottom: 0.5rem;
        }

  .restaurant-type {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

  .restaurant-rating {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

  .stars {
            color: #ffc107;
        }

  .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }

  .contact-item {
            display: flex;
            align-items: center;
            gap: 0.3rem;
            font-size: 0.9rem;
            color: #666;
            flex: 1 0 100%;
        }

   .social-links {
            display: flex;
            gap: 0.5rem;
            margin: 1rem 0;
        }

  .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

  .social-link.facebook { background: #3b5998; }
        .social-link.instagram { background: #e4405f; }
        .social-link.whatsapp { background: #25d366; }

   .social-link:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

   .action-buttons {
            display: flex;
            gap: 0.5rem;
            margin-top: auto;
            padding-top: 1rem;
        }

  .btn {
            flex: 1;
            padding: 0.8rem;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

  .btn-primary {
            background: #ff6b6b;
            color: white;
        }

  .btn-secondary {
            background: #4ecdc4;
            color: white;
        }

  .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

   .map-container {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 1.5rem;
            height: fit-content;
            position: sticky;
            top: 100px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

   .map-title {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 1rem;
            color: #333;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

  .map-title i {
            color: #ff6b6b;
        }

  #map {
            width: 100%;
            height: 400px;
            border-radius: 10px;
            margin-bottom: 1rem;
            border: 1px solid #eee;
        }

  .location-list {
            max-height: 200px;
            overflow-y: auto;
            border: 1px solid #eee;
            border-radius: 10px;
            padding: 0.5rem;
        }

   .location-item {
            padding: 0.8rem;
            border-bottom: 1px solid #eee;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 8px;
            margin-bottom: 0.5rem;
            position: relative;
        }

  .location-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }

   .location-item:hover {
            background: #f8f9fa;
            transform: translateX(5px);
        }

   .location-name {
            font-weight: 600;
            color: #333;
        }

   .location-address {
            font-size: 0.9rem;
            color: #666;
            margin-top: 0.2rem;
        }
        
        /* Nuevo estilo para el botón Visitar */
   .btn-visitar {
            background: #4ecdc4;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 8px;
            font-size: 0.8rem;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        
 .btn-visitar:hover {
            background: #3a9c94;
            transform: translateY(-2px);
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

  @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }

   .search-bar {
                max-width: 100%;
                margin: 0;
            }

   .main-content {
                grid-template-columns: 1fr;
                gap: 1rem;
            }

   .restaurants-grid {
                grid-template-columns: 1fr;
            }

   .filters {
                justify-content: center;
            }

   .action-buttons {
                flex-direction: column;
            }

  .btn {
                flex: none;
            }
            
   .map-container {
                position: relative;
                top: 0;
            }
        }

   .floating-actions {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            z-index: 100;
        }

   .floating-btn {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            border: none;
            background: #ff6b6b;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 4px 20px rgba(255, 107, 107, 0.3);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }

   .floating-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 25px rgba(255, 107, 107, 0.4);
        }
        
   .image-placeholder {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            font-size: 2rem;
        }
        
   .notification {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 14px;
            z-index: 1000;
            display: flex;
            align-items: center;
            gap: 10px;
            animation: fadeInUp 0.5s, fadeOut 0.5s 4.5s;
        }
        
   @keyframes fadeInUp {
            from { opacity: 0; transform: translate(-50%, 20px); }
            to { opacity: 1; transform: translate(-50%, 0); }
        }
        
  @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }
        
        /* Leaflet custom styles */
   .leaflet-popup-content-wrapper {
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }
        
   .leaflet-popup-content {
            margin: 12px 16px;
        }
        
   .leaflet-popup-tip-container {
            margin-top: -1px;
        }
        
   .leaflet-popup-close-button {
            font-size: 20px !important;
            margin: 6px 6px 0 0;
        }
        
   .leaflet-marker-icon {
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3));
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-utensils"></i>
                    Restaurantes Los Órganos
                </div>
                <div class="search-bar">
                    <input type="text" class="search-input" placeholder="Buscar restaurantes..." id="searchInput">
                    <i class="fas fa-search search-icon"></i>
                </div>
            </div>
        </div>
    </header>

  <div class="container">
        <div class="filters">
            <button class="filter-btn active" data-filter="all">Todos</button>
            <button class="filter-btn" data-filter="mariscos">Mariscos</button>
            <button class="filter-btn" data-filter="criolla">Criolla</button>
            <button class="filter-btn" data-filter="pizzas">Pizzas</button>
            <button class="filter-btn" data-filter="internacional">Internacional</button>
            <button class="filter-btn" data-filter="delivery">Delivery</button>
            <button class="filter-btn" data-filter="familiar">Familiar</button>
        </div>

   <div class="main-content">
            <div class="restaurants-grid" id="restaurantsGrid">
                <!-- Los restaurantes se cargarán aquí -->
            </div>

   <div class="map-container">
                <h3 class="map-title">
                    <i class="fas fa-map-marker-alt"></i>
                    Ubicaciones
                </h3>
                <div id="map">
                    <div style="display: flex; align-items: center; justify-content: center; height: 400px; background: linear-gradient(45deg, #667eea, #764ba2); color: white; border-radius: 10px;">
                        <div style="text-align: center;">
                            <div style="font-size: 3rem; margin-bottom: 1rem;">🗺️</div>
                            <p style="font-size: 1.2rem; margin-bottom: 0.5rem;">Cargando mapa...</p>
                            <p style="font-size: 0.9rem; opacity: 0.8;">Por favor espera mientras se carga el mapa</p>
                        </div>
                    </div>
                </div>
                <div class="location-list" id="locationList">
                    <!-- Las ubicaciones se cargarán aquí -->
                </div>
            </div>
        </div>
    </div>

   <div class="floating-actions">
        <button class="floating-btn" title="Ir arriba" onclick="scrollToTop()">
            <i class="fas fa-arrow-up"></i>
        </button>
    </div>

    <!-- Leaflet JS -->
   <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

   <script>
// Restaurantes completos de Los Órganos, Perú con imágenes
const restaurantes = [
    {
        id: 1,
        nombre: "Restaurant Turístico Bambú",
        tipo: "Peruana / Latina / Mariscos",
        rating: 4.7,
        telefono: "+51 972 833 374",
        direccion: "Malecón Los Órganos 20840",
        lat:  -4.1776737,
        lng: -81.1318589,
        whatsapp: "51972833374",
        facebook: "",
        instagram: "restauranteturisticobambu",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Cocina peruana, latina y mariscos con vista al mar",
        descripcion: "Favorito de locales y turistas por su variada carta y ambiente con vista al mar. Experiencia auténtica y completa.",
        imagen: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "https://maps.app.goo.gl/8QkywT5waMiiD7mS8"
    },
    {
        id: 2,
        nombre: "Rinconcito Encantado",
        tipo: "Internacional / Peruana",
        rating: 4.6,
        telefono: "+51 945 123 456",
        direccion: "Pasaje Olaya s/n, Los Órganos",
        lat: -4.1712,
        lng: -81.1248,
        whatsapp: "51945123456",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "criolla",
        especialidad: "Comida casera peruana e internacional",
        descripcion: "Muy recomendado por ambiente agradable y comida casera. Lugar tranquilo con buena relación calidad-precio.",
        imagen: "https://images.unsplash.com/photo-1552566626-52f8b828add9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.rinconcitoencantado.com"
    },
    {
        id: 3,
        nombre: "La Cabaña De Wilo",
        tipo: "Pizzería / Peruana",
        rating: 4.0,
        telefono: "+51 987 654 321",
        direccion: "Panamericana, Los Órganos",
        lat: -4.1703,
        lng: -81.1258,
        whatsapp: "51987654321",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "pizzas",
        especialidad: "Pizzas artesanales y ambiente familiar",
        descripcion: "Famosa por sus pizzas y ambiente familiar. Excelente alternativa en entorno acogedor con buena atención.",
        imagen: "https://images.unsplash.com/photo-1590947132387-155cc02f3212?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.cabanawilo.com"
    },
    {
        id: 4,
        nombre: "El Manglar de Rosa",
        tipo: "Peruana / Mariscos",
        rating: 4.2,
        telefono: "+51 912 345 678",
        direccion: "Barrio Miraflores Sur 2 No 306, Los Órganos",
        lat: -4.1715,
        lng: -81.1245,
        whatsapp: "51912345678",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Ceviches y pescados frescos",
        descripcion: "Especializado en ceviches y pescados frescos. Cuenta con reseñas en YouTube y TripAdvisor.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.manglarrosa.com"
    },
    {
        id: 5,
        nombre: "Ocean Blue & Venezia Restobar",
        tipo: "Internacional / Peruana / Cócteles",
        rating: 4.6,
        telefono: "+51 934 567 890",
        direccion: "Frente al mar, Los Órganos",
        lat: -4.1779690, 
        lng: -81.1323430,
        whatsapp: "51934567890",
        facebook: "",
        instagram: "oceanbluevenezia_restuobar",
        delivery: true,
        reservas: true,
        categoria: "internacional",
        especialidad: "Comida internacional, local, cervezas y cócteles",
        descripcion: "Ambiente moderno y trendy frente al mar. Excelente selección de cervezas y cócteles. Ideal para cenar o tomar algo.",
        imagen: "https://images.unsplash.com/photo-1555396273-367ea4eb4db5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.oceanbluevenezia.com"
    },
    {
        id: 6,
        nombre: "Donde Maru",
        tipo: "Peruana / Café / Delicatessen",
        rating: 4.3,
        telefono: "+51 923 456 789",
        direccion: "Malecón Los Órganos 162, 20840",
        lat: -4.1708,
        lng: -81.1255,
        whatsapp: "51923456789",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "criolla",
        especialidad: "Comida peruana, café y delicatessen",
        descripcion: "Lugar acogedor en el malecón, ideal para desayunos, almuerzos y café. Ambiente tranquilo.",
        imagen: "https://images.unsplash.com/photo-1514933651103-005eec06c04b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.dondemaru.com"
    },
        {
        id: 7,
        nombre: "El Point de Órganos",
        tipo: "Peruana / Mariscos",
        rating: 4.5,
        telefono: "",
        direccion: "Los Órganos 20000",
        lat: -4.1715,
        lng: -81.1245,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "criolla",
        especialidad: "Platos bien preparados a precios accesibles",
        descripcion: "Ambiente acogedor y tranquilo. Recomendado para cenas relajadas y grupos. Atención personalizada.",
        imagen: "https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.elpointorganos.com"
    },
    {
        id: 8,
        nombre: "Sushi El Mirador de Vichayito",
        tipo: "Sushi / Fusión",
        rating: 4.1,
        telefono: "+51 986 727 227",
        direccion: "Vichayito, Antigua Panamericana Norte 1212",
        lat: -4.1650,
        lng: -81.1300,
        whatsapp: "51986727227",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "internacional",
        especialidad: "Sushi y comida fusión",
        descripcion: "Cercano a Los Órganos, especializado en sushi y fusión. Cuenta con sitio web: elmiradordevichayito.com",
        imagen: "https://images.unsplash.com/photo-1611143669185-af224c5e3252?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.elmiradordevichayito.com"
    },
    {
        id: 9,
        nombre: "El Imperio del Sabor",
        tipo: "Peruana / Latina",
        rating: 4.2,
        telefono: "+51 972 934 453",
        direccion: "Av. Perú A-16, frente al parque de Pueblo Nuevo, Los Órganos",
        lat: -4.1708,
        lng: -81.1255,
        whatsapp: "51972934453",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "criolla",
        especialidad: "Platos típicos peruanos y mariscos frescos",
        descripcion: "Ideal para almuerzos. Opción familiar y cómoda para experiencia local auténtica. Servicio de delivery disponible.",
        imagen: "https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.imperiodelsabor.com"
    },
    {
        id: 10,
        nombre: "Las 10 Lukas de Pino",
        tipo: "Peruana / Mariscos",
        rating: 4.2,
        telefono: "",
        direccion: "Los Órganos",
        lat: -4.1710,
        lng: -81.1250,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Mariscos frescos y platos peruanos",
        descripcion: "Reconocido localmente por sus mariscos frescos. Tiene presencia en videos y recomendaciones locales.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.las10lukas.com"
    },
    {
        id: 11,
        nombre: "El Manglar Cevichería",
        tipo: "Peruana / Mariscos",
        rating: 4.3,
        telefono: "",
        direccion: "Pasaje Olaya s/n, Los Órganos",
        lat: -4.1710,
        lng: -81.1250,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Ceviches y pescados frescos",
        descripcion: "Especializado en ceviches y pescados frescos. Excelente opción para sabores marinos en ambiente agradable.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.manglarcevicheria.com"
    },
    {
        id: 12,
        nombre: "Restaurante Brisas del Pacífico",
        tipo: "Peruana / Mariscos",
        rating: 4.0,
        telefono: "",
        direccion: "Los Órganos 20840",
        lat: -4.1705,
        lng: -81.1252,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Mariscos frescos y cocina peruana",
        descripcion: "Restaurante tradicional especializado en mariscos frescos con vista al Pacífico.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.brisasdelpacifico.com"
    },
    {
        id: 13,
        nombre: "Pollería Beach Chicken",
        tipo: "Pollo a la brasa / Parrilla",
        rating: 4.0,
        telefono: "",
        direccion: "Av. Túpac Amaru 437, Los Órganos 20841",
        lat: -4.1714,
        lng: -81.1247,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "parrilla",
        especialidad: "Pollo a la brasa y parrillas",
        descripcion: "Especializado en pollo a la brasa y parrillas. Opción familiar con buen sabor y precios accesibles.",
        imagen: "https://images.unsplash.com/photo-1544025162-d76694265947?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.beachchicken.com"
    },
    {
        id: 14,
        nombre: "Restaurante Punto Marino",
        tipo: "Mariscos / Peruana",
        rating: 4.1,
        telefono: "",
        direccion: "Los Órganos 20841",
        lat: -4.1709,
        lng: -81.1254,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Mariscos frescos y cocina marina",
        descripcion: "Punto de encuentro para los amantes de los mariscos frescos y la cocina marina tradicional.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.puntomarino.com"
    },
    {
        id: 15,
        nombre: "Parrillas El Encanto",
        tipo: "Parrilla / Peruana",
        rating: 4.2,
        telefono: "",
        direccion: "Los Órganos 20840",
        lat: -4.1707,
        lng: -81.1256,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "parrilla",
        especialidad: "Parrillas y carnes a la brasa",
        descripcion: "Especializado en parrillas y carnes a la brasa. Ambiente familiar con buen sabor y atención.",
        imagen: "https://images.unsplash.com/photo-1544025162-d76694265947?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.parrillaelencanto.com"
    },
    {
        id: 16,
        nombre: "El Fogón",
        tipo: "Mariscos / Comida rápida",
        rating: 4.0,
        telefono: "",
        direccion: "Malecón Los Órganos 158, 20840",
        lat: -4.1706,
        lng: -81.1253,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Mariscos frescos y comida rápida",
        descripcion: "Ubicado en el malecón, ofrece mariscos frescos y comida rápida en ambiente casual.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.elfogonorganos.com"
    },
    {
        id: 17,
        nombre: "Cevichería Bendición de Dios",
        tipo: "Mariscos / Peruana",
        rating: 4.1,
        telefono: "",
        direccion: "Los Órganos 20840",
        lat: -4.1711,
        lng: -81.1249,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "mariscos",
        especialidad: "Ceviches y mariscos frescos",
        descripcion: "Cevichería tradicional conocida por sus ceviches frescos y mariscos de calidad.",
        imagen: "https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.bendiciondedios.com"
    },
    {
        id: 18,
        nombre: "La Esquina",
        tipo: "Peruana",
        rating: 4.0,
        telefono: "",
        direccion: "Los Órganos 20840",
        lat: -4.1713,
        lng: -81.1251,
        whatsapp: "",
        facebook: "",
        instagram: "",
        delivery: true,
        reservas: true,
        categoria: "criolla",
        especialidad: "Comida peruana tradicional",
        descripcion: "Restaurante de barrio que ofrece comida peruana tradicional en ambiente acogedor y familiar.",
        imagen: "https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
        web: "www.laesquinaorganos.com"
    }
];

        let restaurantesFiltrados = [...restaurantes];
        let map;
        let markers = [];
        let mapLoaded = false;

        // Inicializar mapa con Leaflet
        function initMap() {
            try {
                // Eliminar placeholder
                const mapDiv = document.getElementById('map');
                mapDiv.innerHTML = '';
                
                // Crear el mapa
                map = L.map('map').setView([-4.1706, -81.1253], 15);
                
                // Añadir capa de OpenStreetMap
                L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
                    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
                }).addTo(map);
                
                mapLoaded = true;
                
                // Mostrar notificación
                showNotification('Mapa cargado correctamente', 'success');

                // Agregar marcadores
                agregarMarcadores();
            } catch (error) {
                console.error("Error al cargar el mapa:", error);
                showNotification('Error al cargar el mapa', 'error');
                initMapFallback();
            }
        }

        function agregarMarcadores() {
            if (!mapLoaded) return;
            
            // Limpiar marcadores existentes
            markers.forEach(marker => map.removeLayer(marker));
            markers = [];

            restaurantesFiltrados.forEach(restaurante => {
                // Crear marcador personalizado
                const customIcon = L.divIcon({
                    className: 'custom-marker',
                    html: `
                        <div style="
                            width: 40px; 
                            height: 40px; 
                            background: #ff6b6b; 
                            border-radius: 50%; 
                            display: flex;
                            align-items: center;
                            justify-content: center;
                            color: white;
                            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
                        ">
                            🍽️
                        </div>
                    `,
                    iconSize: [40, 40],
                    iconAnchor: [20, 40]
                });
                
                const marker = L.marker([restaurante.lat, restaurante.lng], {
                    icon: customIcon
                }).addTo(map);
                
                markers.push(marker);

                // Crear contenido para el popup
                const popupContent = `
                    <div style="max-width: 250px;">
                        <h3 style="margin: 0 0 8px 0; color: #333;">${restaurante.nombre}</h3>
                        <p style="margin: 0 0 8px 0; color: #666; font-size: 14px;">${restaurante.tipo}</p>
                        <p style="margin: 0 0 8px 0; color: #666; font-size: 12px;">${restaurante.descripcion}</p>
                        <div style="margin-top: 10px; display: flex; gap: 5px;">
                            <a href="https://wa.me/${restaurante.whatsapp}" target="_blank" style="
                                background: #25d366; 
                                color: white; 
                                padding: 8px 12px; 
                                text-decoration: none; 
                                border-radius: 4px; 
                                font-size: 12px;
                                flex: 1;
                                text-align: center;
                            ">
                                WhatsApp
                            </a>
                            <a href="tel:${restaurante.telefono}" style="
                                background: #007bff; 
                                color: white; 
                                padding: 8px 12px; 
                                text-decoration: none; 
                                border-radius: 4px; 
                                font-size: 12px;
                                flex: 1;
                                text-align: center;
                            ">
                                Llamar
                            </a>
                        </div>
                    </div>
                `;

                marker.bindPopup(popupContent);
            });
        }

        function crearTarjetaRestaurante(restaurante) {
            // Generar contenido de imagen
            let imagenContent = '';
            if (restaurante.imagen) {
                imagenContent = `<img src="${restaurante.imagen}" alt="${restaurante.nombre}" class="restaurant-image">`;
            } else {
                // Si no hay imagen, mostrar un placeholder con icono
                const iconos = {
                    mariscos: 'fas fa-fish',
                    criolla: 'fas fa-drumstick-bite',
                    pizzas: 'fas fa-pizza-slice',
                    internacional: 'fas fa-globe',
                    parrilla: 'fas fa-fire'
                };
                const icono = iconos[restaurante.categoria] || 'fas fa-utensils';
                imagenContent = `
                    <div class="image-placeholder">
                        <i class="${icono}"></i>
                    </div>
                `;
            }

            return `
                <div class="restaurant-card" data-categoria="${restaurante.categoria}">
                    <div class="restaurant-image-container">
                        ${imagenContent}
                    </div>
                    <div class="restaurant-info">
                        <h3 class="restaurant-name">${restaurante.nombre}</h3>
                        <p class="restaurant-type">${restaurante.tipo}</p>
                        <div class="restaurant-rating">
                            <div class="stars">
                                ${'★'.repeat(Math.floor(restaurante.rating))}${'☆'.repeat(5 - Math.floor(restaurante.rating))}
                            </div>
                            <span>${restaurante.rating}</span>
                        </div>
                        <div class="restaurant-description">
                            <p style="color: #666; font-size: 0.9rem; margin-bottom: 1rem; line-height: 1.4;">
                                ${restaurante.descripcion}
                            </p>
                        </div>
                        <div class="contact-info">
                            <div class="contact-item">
                                <i class="fas fa-phone"></i>
                                <span>${restaurante.telefono}</span>
                            </div>
                            <div class="contact-item">
                                <i class="fas fa-map-marker-alt"></i>
                                <span>${restaurante.direccion}</span>
                            </div>
                            <div class="contact-item">
                                <i class="fas fa-star"></i>
                                <span>${restaurante.especialidad}</span>
                            </div>
                        </div>
                        <div class="social-links">
                            <a href="https://wa.me/${restaurante.whatsapp}" class="social-link whatsapp" target="_blank">
                                <i class="fab fa-whatsapp"></i>
                            </a>
                            <a href="https://facebook.com/${restaurante.facebook}" class="social-link facebook" target="_blank">
                                <i class="fab fa-facebook"></i>
                            </a>
                            <a href="https://instagram.com/${restaurante.instagram}" class="social-link instagram" target="_blank">
                                <i class="fab fa-instagram"></i>
                            </a>
                        </div>
                        <div class="action-buttons">
                            ${restaurante.delivery ? `
                                <a href="https://wa.me/${restaurante.whatsapp}?text=Hola! Me gustaría hacer un pedido delivery" class="btn btn-primary">
                                    <i class="fas fa-motorcycle"></i>
                                    Delivery
                                </a>
                            ` : ''}
                            ${restaurante.reservas ? `
                                <a href="https://wa.me/${restaurante.whatsapp}?text=Hola! Me gustaría hacer una reserva" class="btn btn-secondary">
                                    <i class="fas fa-calendar-check"></i>
                                    Reservar
                                </a>
                            ` : ''}
                            <a href="tel:${restaurante.telefono}" class="btn btn-secondary">
                                <i class="fas fa-phone"></i>
                                Llamar
                            </a>
                        </div>
                    </div>
                </div>
            `;
        }

        function crearItemUbicacion(restaurante) {
            return `
                <div class="location-item" onclick="mostrarEnMapa(${restaurante.id})">
                    <div class="location-name">${restaurante.nombre}</div>
                    <div class="location-address">${restaurante.direccion}</div>
                    <a href="http://${restaurante.web}" class="btn-visitar" target="_blank">Visitar</a>
                </div>
            `;
        }

        function cargarRestaurantes() {
            const grid = document.getElementById('restaurantsGrid');
            const locationList = document.getElementById('locationList');
            
            grid.innerHTML = restaurantesFiltrados.map(crearTarjetaRestaurante).join('');
            locationList.innerHTML = restaurantesFiltrados.map(crearItemUbicacion).join('');
            
            // Actualizar marcadores del mapa
            if (mapLoaded) {
                agregarMarcadores();
            }
        }

        function filtrarRestaurantes(categoria) {
            if (categoria === 'all') {
                restaurantesFiltrados = [...restaurantes];
            } else if (categoria === 'delivery') {
                restaurantesFiltrados = restaurantes.filter(r => r.delivery);
            } else if (categoria === 'familiar') {
                restaurantesFiltrados = restaurantes.filter(r => 
                    r.tipo.toLowerCase().includes('familiar') || 
                    r.descripcion.toLowerCase().includes('familiar') ||
                    r.nombre.toLowerCase().includes('cabaña')
                );
            } else {
                restaurantesFiltrados = restaurantes.filter(r => r.categoria === categoria);
            }
            cargarRestaurantes();
        }

        function buscarRestaurantes(termino) {
            const terminoLower = termino.toLowerCase();
            restaurantesFiltrados = restaurantes.filter(r => 
                r.nombre.toLowerCase().includes(terminoLower) ||
                r.tipo.toLowerCase().includes(terminoLower) ||
                r.especialidad.toLowerCase().includes(terminoLower) ||
                r.descripcion.toLowerCase().includes(terminoLower)
            );
            cargarRestaurantes();
        }

        function mostrarEnMapa(restauranteId) {
            const restaurante = restaurantes.find(r => r.id === restauranteId);
            if (restaurante && mapLoaded) {
                map.setView([restaurante.lat, restaurante.lng], 17);
                
                // Encontrar el marcador correspondiente y abrir su popup
                const marker = markers.find(m => {
                    const latLng = m.getLatLng();
                    return latLng.lat === restaurante.lat && latLng.lng === restaurante.lng;
                });
                if (marker) {
                    marker.openPopup();
                }
            } else {
                showNotification('Mapa no disponible. Intente recargar la página.', 'error');
            }
        }

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        
        function showNotification(message, type) {
            const notification = document.createElement('div');
            notification.className = 'notification';
            notification.innerHTML = `
                <i class="fas fa-${type === 'success' ? 'check-circle' : 'exclamation-triangle'}"></i>
                ${message}
            `;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.remove();
            }, 5000);
        }

        // Función de respaldo para el mapa si Leaflet no carga
        function initMapFallback() {
            const mapDiv = document.getElementById('map');
            if (mapDiv) {
                mapDiv.innerHTML = `
                    <div style="display: flex; align-items: center; justify-content: center; height: 400px; background: linear-gradient(45deg, #667eea, #764ba2); color: white; border-radius: 10px;">
                        <div style="text-align: center;">
                            <div style="font-size: 3rem; margin-bottom: 1rem;">⚠️</div>
                            <p style="font-size: 1.2rem; margin-bottom: 0.5rem;">Mapa no disponible</p>
                            <p style="font-size: 0.9rem; opacity: 0.8;">Haz click en los restaurantes de la lista para ver sus detalles</p>
                        </div>
                    </div>
                `;
            }
        }

        // Event listeners
        document.addEventListener('DOMContentLoaded', function() {
            // Inicializar mapa
            initMap();
            
            // Cargar restaurantes
            cargarRestaurantes();

            // Filtros
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    filtrarRestaurantes(this.dataset.filter);
                });
            });

            // Búsqueda
            document.getElementById('searchInput').addEventListener('input', function() {
                buscarRestaurantes(this.value);
            });
        });
    </script>
</body>
</html> 
