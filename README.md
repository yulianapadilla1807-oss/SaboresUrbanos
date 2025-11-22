# SaboresUrbanos
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menú de Perros Calientes y Hamburguesas</title>

    <!-- Estilos -->
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
        }

        header {
            text-align: center;
            background-color: #ff5733;
            color: white;
            padding: 20px;
        }

        /* Navegación */
        nav {
            text-align: center;
            background-color: #fff;
            padding: 15px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav button {
            background-color: #ff5733;
            color: white;
            border: none;
            margin: 0 10px;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: 0.3s;
        }

        nav button:hover,
        nav button.activo {
            background-color: #e24c28;
        }

        /* Contenedor general */
        .menu-container {
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 70vh;
            padding: 30px;
        }

        .menu-section {
            display: none;
            width: 100%;
            max-width: 1100px;
            background-color: white;
            padding: 20px 30px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        .menu-section.active {
            display: block;
        }

        h2 {
            color: #ff5733;
            border-bottom: 2px solid #ff5733;
            padding-bottom: 5px;
            text-align: center;
        }

        /* Cuadrícula */
        .grid-menu {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-top: 25px;
        }

        .item {
            background-color: #fff5f0;
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .item:hover {
            transform: scale(1.03);
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        .item img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 10px;
        }

        .item h3 {
            color: #333;
            margin-bottom: 10px;
        }

        .ingredientes {
            text-align: left;
            color: #555;
            margin: 10px 0;
            font-size: 14px;
            list-style-type: square;
        }

        .precio {
            font-weight: bold;
            color: white;
            background-color: #ff5733;
            padding: 6px 12px;
            border-radius: 5px;
            display: inline-block;
            margin-top: 10px;
        }

        footer {
            text-align: center;
            display: block;
            background-color:#fff;
            padding: 20px;
            color: #555;
            box-shadow: 0 -2px 5px rgba(0,0,0,0.05);
        }

        .social-icons {
            margin-top: 10px;
        }

        .social-icons a {
            margin: 0 10px;
            color: #ff5733;
            text-decoration: none;
            font-size: 28px;
            transition: 0.3s;
        }

        .social-icons a:hover {
            color: #e24c28;
        }

        @media (max-width: 900px) {
            .grid-menu {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            .grid-menu {
                grid-template-columns: 1fr;
            }
            nav button {
                display: block;
                margin: 10px auto;
                width: 80%;
            }
        }
    </style>

    <!-- ✅ Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
</head>
<body>

    <header>
        <h1>Perros Calientes y Hamburguesas</h1>
        <p>Sabores irresistibles, ingredientes frescos y la mejor calidad</p>
    </header>

    <!-- Navegación -->
    <nav>
        <button class="activo" onclick="mostrarSeccion(event, 'perros')">🌭 Perros Calientes</button>
        <button onclick="mostrarSeccion(event, 'hamburguesas')">🍔 Hamburguesas</button>
    </nav>

    <div class="menu-container">

        <!-- Sección Perros Calientes -->
        <section id="perros" class="menu-section active">
            <h2>🌭 Perros Calientes</h2>

            <div class="grid-menu">
                <div class="item">
                    <img src="https://zenu.com.co/wp-content/uploads/2023/12/receta-perro-caliente-colombiano.jpeg" alt="Perro Tradicional">
                    <h3>Perro Tradicional</h3>
                    <ul class="ingredientes">
                        <li>Pan de perro 60g-$3000</li>
                        <li>Salchicha americana 80g-$2900</li>
                        <li>Salsa de tomate 20ml-$400</li>
                        <li>Mostaza 10ml-400</li>
                        <li>Papas trituradas 30g-$2000</li>
                    </ul>
                
                  <!-- RECETA-->
    <p><strong>Receta:</strong> Cocina la salchicha en agua caliente por 5 minutos. Abre el pan, agrega la salchicha y cubre con salsa de tomate y mostaza. Finaliza con papas trituradas para dar crocancia.</p>

                    <p class="precio">$10.000</p>
                </div>

                <div class="item">
                    <img src="https://imag.bonviveur.com/perrito-caliente.jpg" alt="Perro Mexicano">
                    <h3>Perro Mexicano</h3>
                    <ul class="ingredientes">
                        <li>Pan artesanal 70g-$1700</li>
                        <li>Salchicha picante 90g-$2400</li>
                        <li>Guacamole 40g-$1600</li>
                        <li>Jalapeños 15g-$3000</li>
                        <li>Queso cheddar 25g-$3000</li>
                        
    <p><strong>Receta:</strong> Asa la salchicha hasta dorar. Coloca en el pan y agrega una capa de guacamole, luego jalapeños picados. Derrite queso cheddar por encima.</p>
                    </ul>
                    <p class="precio">$14.000</p>
                </div>

                <div class="item">
                    <img src="https://static.vecteezy.com/system/resources/previews/031/696/500/non_2x/a-scrumptious-grilled-hotdog-ai-generated-photo.jpg" alt="Perro BBQ">
                    <h3>Perro BBQ</h3>
                    <ul class="ingredientes">
                        <li>Pan artesanal 70g-$1700</li>
                        <li>Salchicha americana 80g-$1900</li>
                        <li>Salsa BBQ 25ml-$2000</li>
                        <li>Tocineta 30g-$4000</li>
                        <li>Queso mozzarella 20g-$5000</li>
                    </ul>
                    <p><strong>Receta:</strong> Fríe la tocineta hasta quedar crujiente. Asa la salchicha y colócala en el pan. Agrega salsa BBQ, la tocineta y queso mozzarella derretido.</p>

                    <p class="precio">$15.000</p>
                </div>

                <div class="item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxo7vFLEZfm2VY3VCowv527xPuzN7-17P-JudHwZa-hj-neYDRl0BSObGpWC9wArjhCtQ&usqp=CAU" alt="Perro Ranchero">
                    <h3>Perro Ranchero</h3>
                    <ul class="ingredientes">
                        <li>Pan de perro 70g-$2300</li>
                        <li>Salchicha de pollo 80g-$2600</li>
                        <li>Maíz tierno 30g-$2000</li>
                        <li>Tocineta 25g-$3000</li>
                        <li>Queso mozzarella 20g-$5000</li>
                    </ul>
                    <p><strong>Receta:</strong> Asa la salchicha y calienta el maíz con un toque de mantequilla. Coloca todo en el pan, añade la tocineta y cubre con queso mozzarella.</p>

                    <p class="precio">$16.000</p>
                </div>

                <div class="item">
                    <img src="https://i.ytimg.com/vi/m234S1ybKVU/sddefault.jpg" alt="Perro Especial">
                    <h3>Perro Especial</h3>
                    <ul class="ingredientes">
                        <li>Pan artesanal 70g-$1700</li>
                        <li>Salchicha jumbo 100g-$3600</li>
                        <li>Tocineta 30g-$3500</li>
                        <li>Papas trituradas 30g-$2000</li>
                        <li>Salsa especial de la casa 30g-$2500</li>
                    </ul>
                    <p><strong>Receta:</strong> Cocina la salchicha jumbo, envuélvela con tocineta dorada y colócala en el pan. Agrega salsa de la casa y finaliza con papas trituradas.</p>

                    <p class="precio">$18.000</p>
                </div>
            </div>
        </section>

        <!-- Sección Hamburguesas -->
        <section id="hamburguesas" class="menu-section">
            <h2>🍔 Hamburguesas</h2>

            <div class="grid-menu">
                <div class="item">
                    <img src="https://imag.bonviveur.com/hamburguesa-clasica.jpg" alt="Hamburguesa Clásica">
                    <h3>Hamburguesa Clásica</h3>
                    <ul class="ingredientes">
                        <li>Pan brioche 80g-$2300</li>
                        <li>Carne 100% res 150g-$4000</li>
                        <li>Lechuga 20g-$3000</li>
                        <li>Tomate 25g-$1000</li>
                        <li>Queso americano 20g-$6000</li>
                    </ul>
                    <p><strong>Receta:</strong> Sazona la carne y cocínala a la plancha. Tuesta el pan brioche, coloca la carne y el queso hasta derretir. Agrega lechuga y tomate fresco.</p>
                    <p class="precio">$18.000</p>
                </div>

                <div class="item">
                    <img src="https://static.wixstatic.com/media/29cc8e_aaad1f9b690b4176a0cef213b971f787~mv2.jpg/v1/fill/w_1000,h_667,al_c,q_85,usm_0.66_1.00_0.01/29cc8e_aaad1f9b690b4176a0cef213b971f787~mv2.jpg" alt="Hamburguesa Doble Carne">
                    <h3>Doble Carne</h3>
                    <ul class="ingredientes">
                        <li>Pan brioche 90g-$2500</li>
                        <li>2 carnes de res 300g-$8000</li>
                        <li>Queso cheddar 30g-$2500</li>
                        <li>Tocineta 30g-$3500</li>
                        <li>Salsa especial 25g-$4000</li>
                    </ul>
                    <p><strong>Receta:</strong> Cocina las dos carnes por separado, agrega queso cheddar en cada una. Tuesta el pan, coloca tocineta crujiente y arma la hamburguesa con salsa especial.</p>
                    <p class="precio">$24.000</p>
                </div>

                <div class="item">
                    <img src="https://tienda.customculinary.mx/cdn/shop/articles/burger-cheddar-baconn_copy.jpg?v=1673410421&width=3543" alt="Hamburguesa BBQ">
                    <h3>Hamburguesa BBQ</h3>
                    <ul class="ingredientes">
                        <li>Pan brioche 85g-$2400</li>
                        <li>Carne de res 150g-$4000</li>
                        <li>Salsa BBQ 25ml-$2000</li>
                        <li>Cebolla caramelizada 20g-$2000</li>
                        <li>Queso mozzarella 20g-$6.000</li>
                    </ul>
                    <p><strong>Receta:</strong> Cocina la carne y báñala con salsa BBQ. Añade cebolla caramelizada y queso mozzarella derretido. Sirve en pan brioche tostado.</p>

                    <p>
                    <p class="precio">$22.000</p>
                </div>

                <div class="item">
                    <img src="https://ranchera.com.co/wp-content/uploads/2022/12/HAMBURGUESA-MEXICANA-banner-1.png" alt="Hamburguesa Mexicana">
                    <h3>Hamburguesa Mexicana</h3>
                    <ul class="ingredientes">
                        <li>Pan brioche 80g-$2300</li>
                        <li>Carne de res 150g-$4000</li>
                        <li>Guacamole 35g-$2600</li>
                        <li>Jalapeños 15g-$3000</li>
                        <li>Queso cheddar 20g-$6000</li>
                    </ul>
                    <p><strong>Receta:</strong> Cocina la carne, agrega queso cheddar para fundir. Arma la hamburguesa y añade guacamole fresco y jalapeños en rodajas.</p>

                    <p>
                    <p class="precio">$22.000</p>
                </div>

                <div class="item">
                    <img src="https://www.clarin.com/img/2021/06/17/LC25eDtCT_1200x630__1.jpg" alt="Hamburguesa Especial">
                    <h3>Hamburguesa Especial</h3>
                    <ul class="ingredientes">
                        <li>Pan artesanal 90g-$3000</li>
                        <li>Carne premium 180g-$5000</li>
                        <li>Tocineta 30g-$3000</li>
                        <li>Queso doble capa 30g-$5000</li>
                        <li>Salsa secreta 30g-$4000</li>
                    </ul>
                     <p><strong>Receta:</strong> Cocina la carne premium al gusto. Agrega doble capa de queso hasta fundir. Añade tocineta crujiente y salsa secreta antes de cerrar el pan artesanal.</p>

                    <p class="precio">$26.000</p>
                </div>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer>
        <p>© 2025 Sabores Urbanos - Todos los derechos reservados</p>
        <div class="social-icons">
            <a href="https://wa.me/573001112233" target="_blank"><i class="fab fa-whatsapp"></i></a>
            <a href="https://www.instagram.com/" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://www.facebook.com/" target="_blank"><i class="fab fa-facebook"></i></a>
        </div>
    </footer>

    <!-- Script -->
    <script>
        function mostrarSeccion(event, id) {
            const secciones = document.querySelectorAll('.menu-section');
            const botones = document.querySelectorAll('nav button');
            secciones.forEach(sec => sec.classList.remove('active'));
            botones.forEach(btn => btn.classList.remove('activo'));
            document.getElementById(id).classList.add('active');
            event.target.classList.add('activo');
        }
    </script>
    <style>
    .receta-box {
        margin-top: 10px;
        background: #fff0e6;
        padding: 10px;
        border-radius: 6px;
        display: none;
        font-size: 14px;
    }

    .btn-receta {
        background-color: #ff5733;
        color: white;
        border: none;
        padding: 8px 15px;
        border-radius: 6px;
        cursor: pointer;
        margin-top: 10px;
        transition: .3s;
    }

    .btn-receta:hover {
        background-color: #d64722;
    }
    </style>
<script>
function toggleReceta(id) {
    const box = document.getElementById(id);
    box.style.display = box.style.display === "block" ? "none" : "block";
}
</script>
</body>
</html>
