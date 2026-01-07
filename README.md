<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun yang Super Lucu!</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background: linear-gradient(to bottom, #ffeb3b, #ff9800);
            text-align: center;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        h1 {
            font-size: 3em;
            color: #d32f2f;
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-30px); }
            60% { transform: translateY(-15px); }
        }
        .cake {
            font-size: 5em;
            margin: 20px 0;
            animation: spin 4s linear infinite;
        }
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .balloons {
            font-size: 2em;
            animation: float 3s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        button {
            background: #4caf50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 10px;
            margin: 20px;
        }
        button:hover {
            background: #45a049;
        }
        #joke {
            font-size: 1.5em;
            margin-top: 20px;
            color: #2196f3;
        }
        img {
            max-width: 300px;
            border-radius: 10px;
            margin: 20px;
        }
    </style>
</head>
<body>
    <h1>Selamat Ulang Tahun, [Nama Kamu]!</h1>
    <div class="cake">🎂</div>
    <div class="balloons">🎈🎈🎈</div>
    <img src="https://via.placeholder.com/300x200?text=Ganti+dengan+Foto+Kue" alt="Kue Ulang Tahun">
    <p>Semoga tahun ini kamu makin tua, makin bijak... atau setidaknya makin suka makan kue! 😄</p>
    <button onclick="showJoke()">Klik untuk Lelucon Acak!</button>
    <p id="joke"></p>
    <audio id="music" loop>
        <source src="https://www.soundjay.com/misc/sounds/bell-ringing-05.wav" type="audio/wav">
        Browser kamu tidak mendukung audio.
    </audio>
    <button onclick="playMusic()">Putar Musik!</button>

    <script>
        const jokes = [
            "Kenapa ulang tahun itu seperti hari libur? Karena kamu bisa 'cuti' dari usia muda! 😂",
            "Apa bedanya ulang tahun dengan hari biasa? Hari ini kamu boleh makan kue tanpa alasan! 🍰",
            "Selamat ulang tahun! Semoga tahun depan kamu bisa naik tangga tanpa ngos-ngosan... atau setidaknya naik eskalator! 😅",
            "Kenapa orang ulang tahun suka balon? Karena mereka ingin 'menggelembung' usia mereka! 🎈",
            "Semoga ulang tahunmu penuh kejutan... seperti menemukan uang di saku celana lama! 💰",
            "Ulang tahunmu seperti baterai: makin tua, makin cepat habis! Tapi jangan khawatir, ganti aja dengan kue! 🔋"
        ];

        function showJoke() {
            const randomJoke = jokes[Math.floor(Math.random() * jokes.length)];
            document.getElementById('joke').innerText = randomJoke;
        }

        function playMusic() {
            const audio = document.getElementById('music');
            audio.play();
        }
    </script>
</body>
</html>
