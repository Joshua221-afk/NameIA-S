# NameIA-S
Las mejores inteligencias artificiales a tu alcance 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Directorio de IA Gratuitas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }

        header {
            background-color: #4CAF50;
            color: white;
            padding: 1rem 0;
            text-align: center;
        }

        .container {
            width: 90%;
            margin: 0 auto;
            max-width: 1200px;
            padding: 1rem 0;
        }

        .search {
            text-align: center;
            margin-bottom: 2rem;
        }

        .search input {
            padding: 0.5rem;
            width: 80%;
            max-width: 400px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .search button {
            padding: 0.5rem 1rem;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .search button:hover {
            background-color: #45a049;
        }

        .ai-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
        }

        .ai-item {
            background: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            width: 300px;
            padding: 1rem;
            text-align: center;
        }

        .ai-item h3 {
            margin-bottom: 0.5rem;
            color: #4CAF50;
        }

        .ai-item p {
            font-size: 0.9rem;
            color: #555;
        }

        .ads {
            margin: 2rem 0;
            text-align: center;
        }

        .ads div {
            margin: 1rem 0;
            background: #fff;
            border: 1px solid #ddd;
            padding: 1rem;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .premium-plan {
            margin: 2rem 0;
            text-align: center;
            background: #e0f7fa;
            padding: 1rem;
            border-radius: 5px;
            border: 1px solid #4CAF50;
        }

        footer {
            text-align: center;
            padding: 1rem 0;
            background: #333;
            color: white;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>Directorio de IA Gratuitas</h1>
        <p>Encuentra herramientas de inteligencia artificial gratuitas en un solo lugar.</p>
    </header>

    <div class="container">
        <div class="search">
            <input type="text" id="search" placeholder="Buscar IA...">
            <button onclick="searchAI()">Buscar</button>
        </div>

        <div class="ads">
            <div>
                <h3>Patrocinado por OpenAI</h3>
                <p>Explora ChatGPT y DALL·E, herramientas avanzadas de inteligencia artificial.</p>
            </div>
            <div>
                <h3>Hugging Face</h3>
                <p>Modelos preentrenados y gratuitos para múltiples aplicaciones.</p>
            </div>
            <div>
                <h3>Google AI</h3>
                <p>Accede a Google Bard y otras herramientas innovadoras de Google.</p>
            </div>
            <div>
                <h3>Runway ML</h3>
                <p>Transforma tus ideas creativas con herramientas de edición impulsadas por IA.</p>
            </div>
            <div>
                <h3>Stability AI</h3>
                <p>Generación de imágenes y más con tecnología de IA de vanguardia.</p>
            </div>
        </div>

        <div id="ai-list" class="ai-list">
            <!-- Los elementos de IA se añadirán dinámicamente aquí -->
        </div>

        <div class="premium-plan">
            <h2>Plan Premium</h2>
            <p>Accede a las mejores IA para cualquier tarea por solo $12 al mes.</p>
            <p>Para más información o suscribirte, contáctanos al: <strong>+50488067983</strong></p>
        </div>
    </div>

    <footer>
        <p>&copy; 2024 Directorio de IA Gratuitas. Todos los derechos reservados.</p>
    </footer>

    <script>
        const aiList = [
            { name: "ChatGPT Free", description: "Una IA avanzada para conversaciones." },
            { name: "DALL·E Mini", description: "Generador de imágenes basado en texto." },
            { name: "Hugging Face", description: "Modelos preentrenados para diversas aplicaciones." },
            { name: "Runway ML", description: "Edición de video y generación de medios impulsados por IA." },
            { name: "Google Bard", description: "Asistente de IA de Google." }
        ];

        function renderAIList(filter = "") {
            const listElement = document.getElementById("ai-list");
            listElement.innerHTML = "";

            const filteredAI = aiList.filter(ai =>
                ai.name.toLowerCase().includes(filter.toLowerCase())
            );

            filteredAI.forEach(ai => {
                const aiElement = document.createElement("div");
                aiElement.classList.add("ai-item");
                aiElement.innerHTML = `
                    <h3>${ai.name}</h3>
                    <p>${ai.description}</p>
                `;
                listElement.appendChild(aiElement);
            });
        }

        function searchAI() {
            const query = document.getElementById("search").value;
            renderAIList(query);
        }

        // Renderizar la lista inicial
        renderAIList();
    </script>
</body>
</html>
