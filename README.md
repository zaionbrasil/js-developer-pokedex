<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pokedex</title>

    <!-- Normalize CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"
        integrity="sha512-NhSC1YmyruXifcj/KFRWoC561YpHpc5Jtzgvbuzx5VozKpWvQ+4nXhPdFgmx8xqexRcpAglTj9sIBWINXa8x5w=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />

    <!-- Font Roboto -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;500;700&display=swap" rel="stylesheet">

    <!-- Nosso CSS -->
    <link rel="stylesheet" href="/assets/css/global.css">
    <link rel="stylesheet" href="/assets/css/pokedex.css">
</head>

<body>
    <section class="content">
        <h1>Pokedex</h1>

        <ol class="pokemons">
            <li class="pokemon">
                <span class="number">#001</span>
                <span class="name">Bulbasaur</span>

                <div class="detail">
                    <ol class="types">
                        <li class="type">grass</li>
                        <li class="type">poison</li>
                    </ol>

                    <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/1.svg"
                        alt="Bulbasaur">
                </div>

                <button class="show-details">Mostrar Detalhes</button>
            </li>

            <li class="pokemon">
                <span class="number">#004</span>
                <span class="name">Charmander</span>

                <div class="detail">
                    <ol class="types">
                        <li class="type">fire</li>
                    </ol>

                    <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/4.svg"
                        alt="Charmander">
                </div>

                <button class="show-details">Mostrar Detalhes</button>
            </li>
        </ol>
    </section>

    <!-- Nosso JS -->
    <script src="/assets/js/main.js"></script>

    <script>
        // Adicione este trecho ao seu arquivo main.js para adicionar funcionalidade ao botão
        document.querySelectorAll('.show-details').forEach(button => {
            button.addEventListener('click', function () {
                const details = this.closest('.pokemon').querySelector('.detail');
                details.classList.toggle('visible');
            });
        });
    </script>
</body>

</html>

