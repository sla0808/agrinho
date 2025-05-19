<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Conexão Campo-Cidade</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Estilos personalizados para o mapa interativo (Leaflet) */
        #map {
            height: 400px;
            border-radius: 0.5rem;
            margin-bottom: 2rem;
        }
    </style>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
</head>
<body class="bg-gray-100 font-inter">
    <header class="bg-green-500 text-white py-4 flex justify-between items-center shadow-md sticky top-0 z-10 rounded-md">
        <div class="logo text-xl font-bold ml-4">
            <a href="#" class="hover:text-green-300 transition duration-300">Conexão Campo-Cidade</a>
        </div>
        <nav class="mr-4">
            <ul class="flex space-x-4">
                <li><a href="#inicio" class="hover:text-green-300 transition duration-300">Início</a></li>
                <li><a href="#campo" class="hover:text-green-300 transition duration-300">Campo</a></li>
                <li><a href="#cidade" class="hover:text-green-300 transition duration-300">Cidade</a></li>
                <li><a href="#conexao" class="hover:text-green-300 transition duration-300">Conexão</a></li>
                <li><a href="#entrevistas" class="hover:text-green-300 transition duration-300">Entrevistas</a></li>
                <li><a href="#mapa" class="hover:text-green-300 transition duration-300">Mapa</a></li>
            </ul>
        </nav>
    </header>

    <main class="container mx-auto mt-8 p-4">
        <section id="inicio" class="mb-8">
            <h2 class="text-3xl font-semibold text-green-700 mb-4">Do Rural ao Urbano: Os Laços que Nos Alimentam</h2>
            <p class="text-gray-700 leading-relaxed">
                Explore a intrincada relação entre o campo e a cidade, uma parceria essencial que sustenta nossa sociedade. Descubra como a produção rural molda nossa alimentação, cultura e economia, e como a vida urbana influencia o desenvolvimento do campo.
            </p>
        </section>

        <section id="campo" class="mb-8">
            <h2 class="text-2xl font-semibold text-green-700 mb-4">O Campo: Berço da Produção</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <p class="text-gray-700 leading-relaxed">
                    O campo é onde a magia começa. É a fonte de nossos alimentos, matérias-primas e da própria vida. Explore os diversos tipos de produção agrícola, desde os grãos que compõem nossa mesa até as frutas e verduras que nos nutrem. Conheça o modo de vida dos produtores rurais, suas tradições e o importante papel que desempenham na preservação da natureza.
                </p>
                <div class="bg-green-100 rounded-lg p-4 flex items-center justify-center">
                    <img src="https://images.unsplash.com/photo-1501618255960-b7c529424515?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Plantação no Campo" class="rounded-md max-w-full h-auto">
                </div>
            </div>
        </section>

        <section id="cidade" class="mb-8">
            <h2 class="text-2xl font-semibold text-green-700 mb-4">A Cidade: Centro de Consumo e Distribuição</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-green-100 rounded-lg p-4 flex items-center justify-center">
                    <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Mercado na Cidade" class="rounded-md max-w-full h-auto">
                </div>
                <p class="text-gray-700 leading-relaxed">
                    A cidade pulsa com a energia do consumo e da distribuição. É onde os produtos do campo encontram seus consumidores, onde a economia se movimenta e onde as tendências alimentares são ditadas. Descubra como a cidade influencia o campo, moldando a produção e impulsionando a busca por alimentos frescos e de qualidade.
                </p>
            </div>
        </section>

        <section id="conexao" class="mb-8">
            <h2 class="text-2xl font-semibold text-green-700 mb-4">A Conexão: O Elo Vital</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                A verdadeira magia acontece na conexão entre o campo e a cidade. Feiras vibrantes, mercados movimentados, restaurantes que valorizam os ingredientes locais - cada um desses pontos é um elo que fortalece essa relação. Explore as iniciativas que promovem essa integração e descubra como a tecnologia está impulsionando essa parceria.
            </p>
             <div class="flex flex-wrap justify-around gap-4">
                <div class="bg-green-100 rounded-lg p-4 w-full sm:w-auto flex items-center justify-center">
                    <img src="https://images.unsplash.com/photo-1582155735636-69915f594515?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Feira Livre" class="rounded-md max-w-full h-auto">
                </div>
                <div class="bg-green-100 rounded-lg p-4 w-full sm:w-auto flex items-center justify-center">
                    <img src="https://images.unsplash.com/photo-1552334557-35fb89807c33?q=80&w=2073&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Restaurante com ingredientes locais" class="rounded-md max-w-full h-auto">
                </div>
            </div>
        </section>

        <section id="entrevistas" class="mb-8">
            <h2 class="text-2xl font-semibold text-green-700 mb-4">Entrevistas: Vozes da Conexão</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-green-100 rounded-lg p-4">
                    <h3 class="font-semibold text-green-600 mb-2">Produtor Rural</h3>
                    <p class="text-gray-700 leading-relaxed">
                        "A cidade é o nosso principal mercado, mas também é onde encontramos inspiração para inovar em nossa produção. A troca é constante e enriquecedora."
                    </p>
                </div>
                <div class="bg-green-100 rounded-lg p-4">
                    <h3 class="font-semibold text-green-600 mb-2">Chef de Cozinha</h3>
                    <p class="text-gray-700 leading-relaxed">
                        "Trabalhar com ingredientes frescos do campo eleva nossos pratos a outro nível. A conexão com o produtor é fundamental para garantir a qualidade e o sabor."
                    </p>
                </div>
            </div>
        </section>

        <section id="mapa" class="mb-8">
            <h2 class="text-2xl font-semibold text-green-700 mb-4">Mapa Interativo: Onde a Conexão Acontece</h2>
            <div id="map"></div>
            <p class="text-gray-700 mt-2">
                Explore o mapa e descubra os pontos de encontro entre o campo e a cidade.
            </p>
        </section>
    </main>

    <footer class="bg-green-500 text-white py-4 text-center rounded-md">
        <p>©️ 2025 Conexão Campo-Cidade. Todos os direitos reservados.</p>
    </footer>

    <script>
        var map = L.map('map').setView([-25.4294, -49.2723], 10); // Coordenadas de Curitiba
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);

        // Adiciona marcadores de exemplo (produtores, feiras, mercados)
        var produtorIcon = L.icon({
            iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-green.png',
            shadowUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/images/marker-shadow.png',
            iconSize: [25, 41],
            iconAnchor: [12, 41],
            popupAnchor: [1, -34],
            shadowSize: [41, 41]
        });

        var feiraIcon = L.icon({
            iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-yellow.png',
            shadowUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/images/marker-shadow.png',
            iconSize: [25, 41],
            iconAnchor: [12, 41],
            popupAnchor: [1, -34],
            shadowSize: [41, 41]
        });

        var mercadoIcon = L.icon({
            iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-red.png',
            shadowUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/images/marker-shadow.png',
            iconSize: [25, 41],
            iconAnchor: [12, 41],
            popupAnchor: [1, -34],
            shadowSize: [41, 41]
        });

        L.marker([-25.4500, -49.3000], {icon: produtorIcon}).addTo(map).bindPopup("Produtor de Orgânicos");
        L.marker([-25.4300, -49.2800], {icon: feiraIcon}).addTo(map).bindPopup("Feira Livre do Centro");
        L.marker([-25.4000, -49.2500], {icon: mercadoIcon}).addTo(map).bindPopup("Mercado Municipal");
    </script>
</body>
</html>
