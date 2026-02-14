<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hunter FM Extreme</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Orbitron',sans-serif;
}

body{
    background:#0b0b0b;
    color:white;
    scroll-behavior:smooth;
}

header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px;
    background:black;
    border-bottom:2px solid red;
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
}

.logo{
    color:red;
    font-size:22px;
    font-weight:bold;
}

nav a{
    color:white;
    margin-left:20px;
    text-decoration:none;
    transition:0.3s;
}

nav a:hover{
    color:red;
}

section{
    padding:120px 20px;
    text-align:center;
}

.hero{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(45deg,#ff0000,#000);
}

.hero h1{
    font-size:60px;
    text-shadow:0 0 20px red;
    margin-bottom:20px;
}

.player-box{
    background:#111;
    padding:30px;
    border-radius:10px;
    border:1px solid red;
    box-shadow:0 0 20px red;
}

.play-btn{
    margin-top:15px;
    padding:15px 30px;
    background:red;
    border:none;
    font-size:18px;
    cursor:pointer;
    border-radius:5px;
    transition:0.3s;
}

.play-btn:hover{
    background:#ff3333;
    box-shadow:0 0 15px red;
}

/* TABELA PROGRAMAÇÃO */

.programacao-table{
    width:100%;
    max-width:900px;
    margin:40px auto;
    border-collapse:collapse;
    background:#111;
}

.programacao-table th{
    background:red;
    color:white;
    padding:15px;
}

.programacao-table td{
    border:1px solid #333;
    padding:12px;
}

.programacao-table tr:hover{
    background:#1a1a1a;
}

footer{
    background:black;
    padding:20px;
    text-align:center;
    border-top:2px solid red;
}

.email{
    margin-top:20px;
    font-size:14px;
}

.email a{
    color:red;
    text-decoration:none;
}

@media(max-width:768px){
    .hero h1{
        font-size:35px;
    }
    .programacao-table{
        font-size:14px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">🔥 HUNTER FM</div>
    <nav>
        <a href="#home">Início</a>
        <a href="#programacao">Programação</a>
        <a href="#contato">Contato</a>
    </nav>
</header>

<!-- HERO -->
<section id="home" class="hero">
    <div class="player-box">
        <h1>AO VIVO 24H</h1>
        <audio id="radioPlayer">
            <source src="https://usa16.fastcast4u.com/proxy/wisllan?mp=/1" type="audio/mpeg">
        </audio>
        <button class="play-btn" onclick="togglePlay()">▶ OUVIR AGORA</button>
        <p style="margin-top:15px;">A frequência que domina 🔊</p>
    </div>
</section>

<!-- PROGRAMAÇÃO -->
<section id="programacao">
    <h2>📅 Programação Semanal</h2>

    <table class="programacao-table">
        <tr>
            <th>Dia</th>
            <th>Programa</th>
            <th>Horário</th>
        </tr>
        <tr><td>Segunda</td><td>Top Hits Hunter</td><td>18h às 20h</td></tr>
        <tr><td>Terça</td><td>Top Hits Hunter</td><td>18h às 20h</td></tr>
        <tr><td>Quarta</td><td>Top Hits Hunter</td><td>18h às 20h</td></tr>
        <tr><td>Quinta</td><td>Top Hits Hunter</td><td>18h às 20h</td></tr>
        <tr><td>Sexta</td><td>Top Hits Hunter</td><td>18h às 20h</td></tr>
        <tr><td>Sábado</td><td>Flashback Night</td><td>20h às 23h</td></tr>
        <tr><td>Domingo</td><td>Extreme Mix</td><td>20h às 22h</td></tr>
    </table>
</section>

<!-- CONTATO -->
<section id="contato">
    <h2>📩 Contato</h2>
    <p>Email oficial:</p>
    <div class="email">
        <a href="mailto:hunterfm1021@gmail.com">hunterfm1021@gmail.com</a>
    </div>
</section>

<footer>
    <p>© 2026 Hunter FM Extreme - Todos os direitos reservados</p>
</footer>

<script>
function togglePlay(){
    const player=document.getElementById("radioPlayer");
    if(player.paused){
        player.play();
    } else{
        player.pause();
    }
}
</script>

</body>
</html>
