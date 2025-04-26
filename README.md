<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guía Turística Virtual - Depresión Momposina</title>
    <style>
        :root {
            --primary-color: #3a7d44;
            --secondary-color: #f9c74f;
            --accent-color: #277da1;
            --text-color: #333;
            --light-bg: #f8f9fa;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/api/placeholder/1200/600');
            background-size: cover;
            background-position: center;
            height: 500px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }
        
        nav {
            background-color: var(--primary-color);
            position: relative;
            width: 100%;
            z-index: 100;
        }
        
        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            padding: 15px 0;
        }
        
        .hamburger-menu {
            display: none;
            cursor: pointer;
            flex-direction: column;
            justify-content: space-between;
            width: 30px;
            height: 21px;
        }
        
        .hamburger-menu .bar {
            height: 3px;
            width: 100%;
            background-color: white;
            border-radius: 10px;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li {
            position: relative;
        }
        
        nav ul li a {
            display: block;
            color: white;
            text-decoration: none;
            padding: 15px 20px;
            transition: background-color 0.3s;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            background-color: var(--primary-color);
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
        }
        
        .dropdown-content a {
            padding: 12px 16px;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        section {
            padding: 60px 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary-color);
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .section-title p {
            color: #777;
        }
        
        .destinations {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .destination-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .destination-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .card-image {
            height: 200px;
            overflow: hidden;
        }
        
        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .destination-card:hover .card-image img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 20px;
        }
        
        .card-content h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }
        
        .features {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 40px;
        }
        
        .feature {
            flex: 1;
            min-width: 300px;
            text-align: center;
            padding: 20px;
        }
        
        .feature-icon {
            background-color: var(--light-bg);
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: var(--primary-color);
            font-size: 2rem;
        }
        
        .testimonials {
            background-color: var(--light-bg);
        }
        
        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        
        .testimonial {
            padding: 20px;
        }
        
        .testimonial-text {
            font-style: italic;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .cta {
            background-color: var(--secondary-color);
            text-align: center;
            padding: 80px 20px;
        }
        
        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            transition: background-color 0.3s;
            font-weight: bold;
            margin-top: 20px;
        }
        
        .btn:hover {
            background-color: #2c5e34;
        }
        
        footer {
            background-color: #333;
            color: white;
            padding: 60px 20px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 40px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 10px;
        }
        
        .footer-section ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section ul li a:hover {
            color: var(--secondary-color);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #444;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary-color);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 30px;
            border-top: 1px solid #444;
        }
        
        /* Media Queries para Responsive Design */
        @media (max-width: 992px) {
            .section-title h2 {
                font-size: 2rem;
            }
            
            header {
                height: 400px;
            }
        }
        
        @media (max-width: 768px) {
            .hamburger-menu {
                display: flex;
            }
            
            nav ul {
                position: absolute;
                top: 100%;
                left: 0;
                flex-direction: column;
                background-color: var(--primary-color);
                width: 100%;
                box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
                max-height: 0;
                overflow: hidden;
                transition: max-height 0.5s ease;
            }
            
            nav ul.active {
                max-height: 500px;
            }
            
            .dropdown-content {
                position: static;
                box-shadow: none;
                width: 100%;
                background-color: rgba(0, 0, 0, 0.1);
            }
            
            .dropdown-content a {
                padding-left: 40px;
            }
            
            .feature {
                min-width: 100%;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
        }
        
        @media (max-width: 480px) {
            header {
                height: 350px;
            }
            
            header h1 {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 1.5rem;
            }
            
            .destinations {
                grid-template-columns: 1fr;
            }
            
            .cta h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
   
    
    <nav>
        <div class="container">
            <div class="logo">MaicolTour</div>
            <div class="hamburger-menu" id="hamburger-menu">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
            <ul id="nav-menu">
                <li><a href="#inicio">Inicio</a></li>
                <li class="dropdown">
                    <a href="#destinos" class="dropdown-toggle">Destinos</a>
                    <div class="dropdown-content">
                        <a href="#mompox">Mompox</a>
                        <a href="#magangue">Magangué</a>
                        <a href="#sanmartin">San Martín de Loba</a>
                        <a href="#talaigua">Talaigua Nuevo</a>
                    </div>
                </li>
                <li><a href="#experiencias">Experiencias</a></li>
                <li><a href="#gastronomia">Gastronomía</a></li>
                <li><a href="#cultura">Cultura y Tradiciones</a></li>
                <li><a href="#consejos">Consejos de Viaje</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </div>
    </nav>
    
    <section id="inicio">
        <div class="container">
            <div class="section-title">
                <h2>Bienvenidos a la Depresión Momposina</h2>
                <p>Un territorio mágico rodeado de agua, historia y tradición</p>
            </div>
            
            <p>La Depresión Momposina es una región geográfica situada en el norte de Colombia, principalmente en el departamento de Bolívar, formada por la confluencia de los ríos Magdalena, Cauca y San Jorge. Este territorio de humedales y ciénagas es un paraíso cultural y natural que conserva intacto el encanto colonial y las tradiciones ancestrales de sus habitantes.</p>
            
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">🏛️</div>
                    <h3>Patrimonio Cultural</h3>
                    <p>Descubre el legado colonial español y la riqueza arquitectónica de pueblos como Santa Cruz de Mompox, declarado Patrimonio de la Humanidad por la UNESCO.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🛶</div>
                    <h3>Naturaleza Exuberante</h3>
                    <p>Explora los complejos de ciénagas, caños y ríos que conforman un ecosistema único, hogar de una gran diversidad de flora y fauna.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🎭</div>
                    <h3>Tradiciones Vivas</h3>
                    <p>Vive las festividades religiosas, la orfebrería tradicional y las manifestaciones culturales que han perdurado por siglos en esta región.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="destinos" class="bg-light">
        <div class="container">
            <div class="section-title">
                <h2>Destinos Imperdibles</h2>
                <p>Conoce los lugares más emblemáticos de la Depresión Momposina</p>
            </div>
            
            <div class="destinations">
                <div class="destination-card" id="mompox">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Santa Cruz de Mompox">
                    </div>
                    <div class="card-content">
                        <h3>Santa Cruz de Mompox</h3>
                        <p>Ciudad colonial fundada en 1540, declarada Patrimonio de la Humanidad por la UNESCO en 1995. Sus calles empedradas, iglesias barrocas y casas coloniales la convierten en un verdadero museo al aire libre.</p>
                        <p><strong>No te pierdas:</strong> La iglesia de Santa Bárbara, el taller de filigrana, la Albarrada y las procesiones de Semana Santa.</p>
                    </div>
                </div>
                
                <div class="destination-card" id="magangue">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Magangué">
                    </div>
                    <div class="card-content">
                        <h3>Magangué</h3>
                        <p>Principal puerto comercial de la región, ubicado a orillas del río Magdalena. Un punto estratégico para explorar las ciénagas cercanas y disfrutar del comercio tradicional ribereño.</p>
                        <p><strong>No te pierdas:</strong> El mercado flotante, el Festival del Río y las vistas panorámicas desde el malecón.</p>
                    </div>
                </div>
                
                <div class="destination-card" id="sanmartin">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="San Martín de Loba">
                    </div>
                    <div class="card-content">
                        <h3>San Martín de Loba</h3>
                        <p>Municipio con rica tradición minera y cultural, ubicado en la serranía de mismo nombre. Famoso por sus tamboras y bailes cantados que son Patrimonio Cultural Inmaterial.</p>
                        <p><strong>No te pierdas:</strong> El Festival de la Tambora, las minas artesanales y los recorridos por el río Magdalena.</p>
                    </div>
                </div>
                
                <div class="destination-card" id="talaigua">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Talaigua Nuevo">
                    </div>
                    <div class="card-content">
                        <h3>Talaigua Nuevo</h3>
                        <p>Pueblo tradicional conocido por su artesanía en caña flecha y por la conservación de tradiciones como la fabricación de instrumentos musicales autóctonos.</p>
                        <p><strong>No te pierdas:</strong> Los talleres artesanales, el Festival del Bocachico y los recorridos por la ciénaga.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- El resto de las secciones se mantienen igual... -->
    
    <section id="experiencias">
        <div class="container">
            <div class="section-title">
                <h2>Experiencias Únicas</h2>
                <p>Actividades que no puedes dejar de vivir en la Depresión Momposina</p>
            </div>
            
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">🚣</div>
                    <h3>Recorridos Fluviales</h3>
                    <p>Navega por los ríos y ciénagas para descubrir la biodiversidad de este ecosistema acuático, observar aves y conocer la forma de vida ribereña.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🔨</div>
                    <h3>Talleres de Filigrana</h3>
                    <p>Aprende el arte tradicional de la orfebrería momposina, reconocida mundialmente por su delicadeza y precisión.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🎭</div>
                    <h3>Semana Santa en Mompox</h3>
                    <p>Vive una de las celebraciones religiosas más antiguas y solemnes de Colombia, con procesiones que datan de la época colonial.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🥘</div>
                    <h3>Gastronomía Local</h3>
                    <p>Degusta platos tradicionales como el bocachico en cabrito, la viuda de pescado y los dulces típicos elaborados con frutas de la región.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="gastronomia" class="bg-light">
        <div class="container">
            <div class="section-title">
                <h2>Sabores de la Depresión Momposina</h2>
                <p>Una gastronomía rica en tradición y sabores únicos</p>
            </div>
            
            <p>La cocina de la Depresión Momposina está influenciada por las tradiciones indígenas, africanas y españolas, utilizando ingredientes locales como pescados de río, tubérculos, frutas tropicales y hierbas aromáticas.</p>
            
            <div class="destinations">
                <div class="destination-card">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Bocachico en Cabrito">
                    </div>
                    <div class="card-content">
                        <h3>Bocachico en Cabrito</h3>
                        <p>Plato emblemático donde el pescado bocachico se cocina en hojas de bijao con especias locales, creando un sabor único y tradicional.</p>
                    </div>
                </div>
                
                <div class="destination-card">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Dulces Típicos">
                    </div>
                    <div class="card-content">
                        <h3>Dulces Típicos</h3>
                        <p>La región es famosa por sus dulces artesanales como el cabello de ángel, las cocadas, el dulce de icaco y las conservas de frutas tropicales.</p>
                    </div>
                </div>
                
                <div class="destination-card">
                    <div class="card-image">
                        <img src="/api/placeholder/400/320" alt="Sancocho de Pescado">
                    </div>
                    <div class="card-content">
                        <h3>Sancocho de Pescado</h3>
                        <p>Sopa tradicional preparada con pescado, yuca, plátano, ñame y especias locales, ideal para recuperar energías después de un día de exploración.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="cultura">
        <div class="container">
            <div class="section-title">
                <h2>Cultura y Tradiciones</h2>
                <p>Un patrimonio cultural inmaterial de valor incalculable</p>
            </div>
            
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">💍</div>
                    <h3>Filigrana Momposina</h3>
                    <p>Técnica de orfebrería de origen español que los artesanos locales han perfeccionado durante siglos, creando delicadas joyas en oro y plata.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🥁</div>
                    <h3>Música de Tambora</h3>
                    <p>Género musical y danza tradicional con influencias africanas que utiliza tamboras, maracas y voces para expresar historias y tradiciones.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🎭</div>
                    <h3>Festividades Religiosas</h3>
                    <p>Las celebraciones religiosas, especialmente la Semana Santa, conservan rituales y tradiciones que datan de la época colonial.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🧶</div>
                    <h3>Artesanías en Fibras Naturales</h3>
                    <p>Elaboración de sombreros, esteras y cestos utilizando técnicas ancestrales y materiales como la palma de iraca y la caña flecha.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="consejos" class="bg-light">
        <div class="container">
            <div class="section-title">
                <h2>Consejos para Viajeros</h2>
                <p>Recomendaciones para aprovechar al máximo tu visita</p>
            </div>
            
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">🗓️</div>
                    <h3>Mejor Época para Visitar</h3>
                    <p>Diciembre a marzo es la temporada seca, ideal para recorrer la región. Semana Santa ofrece una experiencia cultural única, pero con mayor afluencia de turistas.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🚌</div>
                    <h3>Cómo Llegar</h3>
                    <p>Desde Cartagena o Barranquilla se puede llegar por carretera. También hay opciones de transporte fluvial desde varios puntos del río Magdalena.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">🧴</div>
                    <h3>Qué Llevar</h3>
                    <p>Ropa ligera, repelente de insectos, protector solar, sombrero y calzado cómodo. No olvides una cámara para capturar los paisajes y arquitectura.</p>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">💰</div>
                    <h3>Presupuesto</h3>
                    <p>La región ofrece opciones para todos los presupuestos, desde hospedajes en casas familiares hasta hoteles boutique en casonas coloniales restauradas.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Experiencias de Viajeros</h2>
                <p>Lo que otros visitantes opinan sobre la Depresión Momposina</p>
            </div>
            
            <div class="testimonial-slider">
                <div class="testimonial">
                    <p class="testimonial-text">"Visitar Mompox fue como viajar en el tiempo. Las calles coloniales, el río Magdalena y la amabilidad de su gente hacen de este lugar un destino único en Colombia."</p>
                    <p class="testimonial-author">Carlos Rodríguez, Medellín</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="cta">
        <div class="container">
            <h2>¿Listo para Descubrir la Depresión Momposina?</h2>
            <p>Planifica tu viaje virtual o presencial y déjate maravillar por uno de los tesoros mejor guardados de Colombia</p>
            <a href="#contacto" class="btn">Contáctanos para más información</a>
        </div>
    </section>
    
    <footer id="contacto">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Guía Turística Virtual</h3>
                    <p>Tu compañero digital para explorar todos los rincones de la Depresión Momposina en el departamento de Bolívar, Colombia.</p>
                    <div class="social-links">
                        <a href="#" title="Facebook">f</a>
                        <a href="#" title="Instagram">i</a>
                        <a href="#" title="Twitter">t</a>
                        <a href="#" title="YouTube">y</a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#destinos">Destinos</a></li>
                        <li><a href="#experiencias">Experiencias</a></li>
                        <li><a href="#gastronomia">Gastronomía</a></li>
                        <li><a href="#cultura">Cultura</a></li>
                        <li><a href="#consejos">Consejos</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Contacto</h3>
                    <ul>
                        <li>Email: carranzamaicol71.com</li>
                        <li>Teléfono: +57 3218558111 </li>
                        <li>Santa Cruz de Mompox, Bolívar, Colombia</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 Guía Turística Virtual Depresión Momposina. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Script para navegación suave
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Script para testimoniales
        const testimonials = [
            {
                text: "Visitar Mompox fue como viajar en el tiempo. Las calles coloniales, el río Magdalena y la amabilidad de su gente hacen de este lugar un destino único en Colombia.",
                author: "Leonardo Diaz, El Banco"
            },
            {
                text: "Las ciénagas de la Depresión Momposina son un paraíso para los amantes de la naturaleza. Nunca había visto tanta diversidad de aves y paisajes acuáticos.",
                author: "Ana Martínez, Bogotá"
            },
            {
                text: "La filigrana momposina es simplemente impresionante. Me llevé varias piezas y cada vez que las uso recibo cumplidos por su belleza y originalidad.",
                author: "Laura Gómez, Cali"
            }
        ];
        
        let currentTestimonial = 0;
        const testimonialText = document.querySelector('.testimonial-text');
        const testimonialAuthor = document.querySelector('.testimonial-author');
        
        function changeTestimonial() {
            currentTestimonial = (current# Tour-
