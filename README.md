<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Tienda Online - CatálogoYa</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ESTILOS BÁSICOS */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', Arial, sans-serif; 
            line-height: 1.6; 
            color: #333; 
            background: #f5f5f5;
            padding: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        /* HEADER */
        .header {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 30px 20px;
            border-radius: 15px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .logo {
            font-size: 2.8rem;
            margin-bottom: 15px;
        }
        
        .store-name {
            font-size: 2.2rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .store-description {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }
        
        /* INFO */
        .info-bar {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            background: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
        }
        
        .info-item {
            text-align: center;
            padding: 10px;
            min-width: 200px;
        }
        
        .info-icon {
            color: #6a11cb;
            font-size: 1.8rem;
            margin-bottom: 10px;
        }
        
        /* PRODUCTOS */
        .section-title {
            text-align: center;
            font-size: 1.8rem;
            margin: 40px 0 20px;
            color: #333;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: #6a11cb;
            margin: 10px auto;
            border-radius: 2px;
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .product-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-img {
            width: 100%;
            height: 180px;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3.5rem;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: #333;
        }
        
        .product-desc {
            color: #666;
            font-size: 0.95rem;
            margin-bottom: 15px;
            line-height: 1.5;
        }
        
        .product-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #2575fc;
        }
        
        /* WHATSAPP BUTTON */
        .whatsapp-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            text-decoration: none;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.5);
            z-index: 1000;
            transition: all 0.3s ease;
        }
        
        .whatsapp-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 20px rgba(37, 211, 102, 0.7);
        }
        
        /* FOOTER */
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
            border-top: 1px solid #eee;
            margin-top: 40px;
        }
        
        /* RESPONSIVE */
        @media (max-width: 768px) {
            .info-bar {
                flex-direction: column;
                align-items: center;
            }
            
            .products {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            
            .store-name {
                font-size: 1.8rem;
            }
        }
        
        @media (max-width: 480px) {
            .products {
                grid-template-columns: 1fr;
            }
            
            body {
                padding: 10px;
            }
        }
        
        /* BADGE */
        .badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #ff4757;
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .product-card {
            position: relative;
        }
    </style>
</head>
<body>
    <!-- ENCABEZADO -->
    <header class="header">
        <div class="logo">🛒</div>
        <h1 class="store-name">Mi Tienda Ejemplo</h1>
        <p class="store-description">Productos de calidad con los mejores precios del mercado</p>
    </header>

    <!-- INFORMACIÓN -->
    <div class="info-bar">
        <div class="info-item">
            <div class="info-icon">⏰</div>
            <h3>Horarios</h3>
            <p>Lunes a Viernes: 9:00 - 20:00</p>
            <p>Sábados: 9:00 - 14:00</p>
        </div>
        
        <div class="info-item">
            <div class="info-icon">📍</div>
            <h3>Ubicación</h3>
            <p>Calle Principal 1234</p>
            <p>Buenos Aires, Argentina</p>
        </div>
        
        <div class="info-item">
            <div class="info-icon">📞</div>
            <h3>Contacto</h3>
            <p>Tel: (011) 1234-5678</p>
            <p>Consultas por WhatsApp</p>
        </div>
    </div>

    <!-- PRODUCTOS -->
    <h2 class="section-title">Nuestros Productos Destacados</h2>
    
    <div class="products">
        <!-- PRODUCTO 1 -->
        <div class="product-card">
            <div class="badge">NUEVO</div>
            <div class="product-img">📦</div>
            <div class="product-info">
                <h3 class="product-title">Producto Ejemplo 1</h3>
                <p class="product-desc">Descripción del producto. Características principales y beneficios.</p>
                <div class="product-price">$1.890</div>
            </div>
        </div>
        
        <!-- PRODUCTO 2 -->
        <div class="product-card">
            <div class="product-img">🎁</div>
            <div class="product-info">
                <h3 class="product-title">Producto Ejemplo 2</h3>
                <p class="product-desc">Descripción del producto. Ideal para regalos y ocasiones especiales.</p>
                <div class="product-price">$2.450</div>
            </div>
        </div>
        
        <!-- PRODUCTO 3 -->
        <div class="product-card">
            <div class="badge">OFERTA</div>
            <div class="product-img">🔥</div>
            <div class="product-info">
                <h3 class="product-title">Producto Ejemplo 3</h3>
                <p class="product-desc">Descripción del producto. Oferta limitada por tiempo.</p>
                <div class="product-price">
                    <span style="text-decoration: line-through; color: #999; font-size: 1.1rem;">$3.200</span><br>
                    $2.750
                </div>
            </div>
        </div>
        
        <!-- PRODUCTO 4 -->
        <div class="product-card">
            <div class="product-img">⭐</div>
            <div class="product-info">
                <h3 class="product-title">Producto Ejemplo 4</h3>
                <p class="product-desc">Descripción del producto. Más vendido de la temporada.</p>
                <div class="product-price">$3.800</div>
            </div>
        </div>
    </div>

    <!-- BOTÓN WHATSAPP -->
    <a 
        href="https://wa.me/5491112345678?text=Hola,%20vi%20tu%20catálogo%20online%20y%20quiero%20hacer%20una%20consulta" 
        class="whatsapp-btn" 
        target="_blank"
        title="Consultar por WhatsApp"
    >
        💬
    </a>

    <!-- PIE DE PÁGINA -->
    <footer class="footer">
        <p>© 2023 CatálogoYa - Tu vitrina digital</p>
        <p style="font-size: 0.8rem; margin-top: 10px; color: #888;">
            Comparte este link con tus clientes: <span id="page-url">[tu-url-aquí]</span>
        </p>
    </footer>

    <script>
        // Mostrar URL actual
        document.getElementById('page-url').textContent = window.location.href;
        
        // Contador de visitas simple
        let visits = localStorage.getItem('pageVisits') || 0;
        visits++;
        localStorage.setItem('pageVisits', visits);
        
        // Mostrar en consola (opcional)
        console.log(`Visitas a esta página: ${visits}`);
        
        // Hacer clic en producto actualiza mensaje de WhatsApp
        document.querySelectorAll('.product-card').forEach(card => {
            card.addEventListener('click', function() {
                const productName = this.querySelector('.product-title').textContent;
                const whatsappBtn = document.querySelector('.whatsapp-btn');
                const phone = '5491112345678'; // Cambiar por número real
                const message = `Hola, me interesa el producto: ${productName}. ¿Podrías darme más información?`;
                const encodedMessage = encodeURIComponent(message);
                whatsappBtn.href = `https://wa.me/${phone}?text=${encodedMessage}`;
            });
        });
    </script>
</body>
</html>
