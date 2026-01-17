# studious-parakeet <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avícola La Frescura | Pollo Premium</title>
    <style>
        /* --- ESTILOS GENERALES --- */
        :root {
            --primary: #e63946; /* Rojo Carnicería */
            --secondary: #f1faee; /* Blanco Hueso */
            --accent: #1d3557; /* Azul Oscuro para texto */
            --light: #f8f9fa;
            --shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--secondary);
            color: var(--accent);
            line-height: 1.6;
        }

        h1, h2, h3 { margin: 0; font-weight: 700; }
        a { text-decoration: none; }
        ul { list-style: none; padding: 0; }

        /* --- HEADER --- */
        header {
            background-color: white;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo { font-size: 1.5rem; color: var(--primary); font-weight: bold; }
        .nav-links a { margin-left: 20px; color: var(--accent); font-weight: 500; }
        
        /* Ocultar menú en móviles por simplicidad */
        @media (max-width: 768px) {
            .nav-links { display: none; }
        }

        /* --- HERO SECTION (Portada) --- */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1587593810167-a84920ea0781?auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 60vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .hero h1 { font-size: 3rem; margin-bottom: 10px; }
        .hero p { font-size: 1.2rem; margin-bottom: 20px; }
        
        .btn {
            background-color: var(--primary);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s;
            display: inline-block;
        }
        .btn:hover { transform: scale(1.05); background-color: #d62828; }

        /* --- PRODUCTOS (Grid) --- */
        .container { max-width: 1200px; margin: 0 auto; padding: 50px 20px; }
        .section-title { text-align: center; margin-bottom: 40px; color: var(--primary); }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }

        .product-card:hover { transform: translateY(-5px); }

        .product-img {
            height: 200px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #666;
            font-size: 0.9rem;
        }
        
        /* Nota: Uso imágenes de placeholder. Debes reemplazarlas por las tuyas reales */
        .img-placeholder { width: 100%; height: 100%; object-fit: cover; }

        .product-info { padding: 20px; }
        .product-price { color: var(--primary); font-size: 1.3rem; font-weight: bold; margin: 10px 0; }
        .product-desc { font-size: 0.9rem; color: #666; margin-bottom: 15px; }

        .btn-sm {
            display: block;
            text-align: center;
            background-color: #25D366; /* Verde WhatsApp */
            color: white;
            padding: 10px;
            border-radius: 8px;
        }

        /* --- COMBOS --- */
        .combos-section { background-color: #ffe8e8; padding: 50px 20px; }
        .combo-card {
            background: white;
            border: 2px solid var(--primary);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--accent);
            color: white;
            text-align: center;
            padding: 40px 20px;
        }

        /* --- BOTÓN FLOTANTE WHATSAPP --- */
        .float-wa {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .float-wa:hover { background-color: #128C7E; }

    </style>
</head>
<body>

    <header>
        <div class="logo">🐔 La Frescura</div>
        <nav class="nav-links">
            <a href="#productos">Productos</a>
            <a href="#combos">Combos</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <section class="hero">
        <h1>Pollo Fresco del Día</h1>
        <p>Directo del campo a tu mesa. Sin congelados, sabor 100% natural.</p>
        <a href="#productos" class="btn">Ver Precios</a>
    </section>

    <div class="container" id="productos">
        <h2 class="section-title">Nuestros Cortes</h2>
        
        <div class="products-grid">
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1604503468506-a8da13d82791?auto=format&fit=crop&w=500&q=60" alt="Pechuga" class="img-placeholder">
                </div>
                <div class="product-info">
                    <h3>Pechuga Deshuesada</h3>
                    <p class="product-desc">Supremas limpias, sin piel ni hueso. Ideales para plancha.</p>
                    <div class="product-price">$5.000 /kg</div>
                    <a href="https://wa.me/5491112345678?text=Hola,%20quiero%20pedir%20Pechuga" class="btn-sm" target="_blank">Pedir al WhatsApp</a>
                </div>
            </div>

            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1587593810167-a84920ea0781?auto=format&fit=crop&w=500&q=60" alt="Pata Muslo" class="img-placeholder">
                </div>
                <div class="product-info">
                    <h3>Pata Muslo</h3>
                    <p class="product-desc">Cuarto trasero con piel. Jugoso, ideal para horno.</p>
                    <div class="product-price">$3.500 /kg</div>
                    <a href="https://wa.me/5491112345678?text=Hola,%20quiero%20pedir%20Pata%20Muslo" class="btn-sm" target="_blank">Pedir al WhatsApp</a>
                </div>
            </div>

            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1567620832903-9fc6debc209f?auto=format&fit=crop&w=500&q=60" alt="Alitas" class="img-placeholder">
                </div>
                <div class="product-info">
                    <h3>Alitas de Pollo</h3>
                    <p class="product-desc">Perfectas para freír o hacer al horno con barbacoa.</p>
                    <div class="product-price">$2.000 /kg</div>
                    <a href="https://wa.me/5491112345678?text=Hola,%20quiero%20pedir%20Alitas" class="btn-sm" target="_blank">Pedir al WhatsApp</a>
                </div>
            </div>

            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1627246479705-d143d2c8038f?auto=format&fit=crop&w=500&q=60" alt="Milanesas" class="img-placeholder">
                </div>
                <div class="product-info">
                    <h3>Milanesas Caseras</h3>
                    <p class="product-desc">De pechuga, rebozado crocante con ajo y perejil.</p>
                    <div class="product-price">$6.000 /kg</div>
                    <a href="https://wa.me/5491112345678?text=Hola,%20quiero%20pedir%20Milanesas" class="btn-sm" target="_blank">Pedir al WhatsApp</a>
                </div>
            </div>

            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1543501708-250325f6966f?auto=format&fit=crop&w=500&q=60" alt="Pollo Trozado" class="img-placeholder">
                </div>
                <div class="product-info">
                    <h3>Pollo Trozado Mix</h3>
                    <p class="product-desc">Variedad de presas surtidas. Económico y rendidor.</p>
                    <div class="product-price">$3.000 /kg</div>
                    <a href="https://wa.me/5491112345678?text=Hola,%20quiero%20pedir%20Mix%20Trozado" class="btn-sm" target="_blank">Pedir al WhatsApp</a>
                </div>
            </div>
        </div>
    </div>

    <section class="combos-section" id="combos">
        <div class="container">
            <h2 class="section-title">🔥 Combos Ahorro</h2>
            <div class="products-grid">
                <div class="combo-card">
                    <h3>Combo Familiar</h3>
                    <p>2kg Pata Muslo + 1kg Milanesas + 1kg Alitas</p>
                    <p style="font-weight: bold; font-size: 1.5rem; color: #e63946;">$12.000</p>
                    <a href="https://wa.me/5491112345678?text=Quiero%20el%20Combo%20Familiar" class="btn">Encargar Ya</a>
                </div>
                <div class="combo-card">
                    <h3>Combo Fitness</h3>
                    <p>3kg Pechuga + 1 Maple de Huevos</p>
                    <p style="font-weight: bold; font-size: 1.5rem; color: #e63946;">$18.000</p>
                    <a href="https://wa.me/5491112345678?text=Quiero%20el%20Combo%20Fitness" class="btn">Encargar Ya</a>
                </div>
            </div>
        </div>
    </section>

    <footer id="contacto">
        <h3>🐔 Avícola La Frescura</h3>
        <p>Hacé tu pedido y te lo llevamos a domicilio.</p>
        <p>📍 Calle Falsa 123, Tu Ciudad</p>
        <p>📞 123-456-7890</p>
        <small>&copy; 2024 La Frescura. Todos los derechos reservados.</small>
    </footer>

    <a href="https://wa.me/5491112345678" class="float-wa" target="_blank">
        <svg viewBox="0 0 32 32" style="fill:white; width:35px; height:35px;"><path d="M19.11 17.205c-.372 0-1.088 1.39-1.518 1.39a.63.63 0 0 1-.315-.1c-.802-.402-1.504-.817-2.163-1.447-.545-.516-1.146-1.29-1.46-1.963a.426.426 0 0 1-.073-.215c0-.33.99-.945.99-1.49 0-.143-.73-2.09-.832-2.335-.143-.372-.214-.487-.6-.487-.187 0-.36-.043-.53-.043-.302 0-.53.115-.746.315-.688.645-1.032 1.318-1.06 2.264v.114c-.015.99.472 1.977 1.017 2.78 1.23 1.82 2.506 3.41 4.554 4.34.616.287 2.035.888 2.722.888.817 0 2.15-.515 2.478-1.318.13-.33.244-.73.244-1.088 0-.058 0-.144-.03-.215-.1-.172-2.434-1.39-2.678-1.39zm-2.908 7.593c-1.747 0-3.48-.53-4.942-1.49L7.793 24.41l1.132-3.337a8.955 8.955 0 0 1-1.72-5.272c0-4.955 4.04-8.995 8.997-8.995S25.2 10.845 25.2 15.8c0 4.958-4.04 8.998-8.998 8.998zm0-19.798c-5.96 0-10.8 4.842-10.8 10.8 0 1.964.53 3.898 1.546 5.574L5 27.176l5.974-1.92a10.807 10.807 0 0 1 5.23 1.34c5.96 0 10.8-4.842 10.8-10.8s-4.84-10.8-10.8-10.8z"/></svg>
    </a>

</body>
</html>
