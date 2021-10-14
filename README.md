## Hi [Matias][website] here 👋

[![Twitter Follow](https://img.shields.io/twitter/follow/magamex_ma?color=%231DA1F2&label=magamex_ma&logo=twitter&logoColor=%231DA1F2&style=for-the-badge)](https://twitter.com/magamex_ma/)
[![LinkedIn](https://shields.io/badge/LinkedIn-matias%20angeluk-blue?logo=LinkedIn&logoColor=blue&style=for-the-badge)](https://www.linkedin.com/in/matiasangeluk/)
    <style>
        html {
            background: black;
            height: 100%;
            overflow: hidden;
        }
        body {
            margin: 0;
            padding: 0;
            height: 100%;
        }
    </style>
<body>
    <canvas id="Matrix"></canvas>
    <script>
        const canvas = document.getElementById('Matrix');
        const context = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = 250;
        const katakana = 'アァカサタナハマヤャラワガザダバパイィキシチニヒミリヰギジヂビピウゥクスツヌフムユュルグズブヅプエェケセテネヘメレヱゲゼデベペオォコソトノホモヨョロヲゴゾドボポヴッン';
        const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        const nums = '0123456789';
        const alphabet = katakana + latin + nums;
        const fontSize = 16;
        const columns = canvas.width/fontSize;
        const rainDrops = [];
        for( let x = 0; x < columns; x++ ) {
            rainDrops[x] = 1;
        }
        const draw = () => {
            context.fillStyle = 'rgba(0, 0, 0, 0.05)';
            context.fillRect(0, 0, canvas.width, canvas.height);
            context.fillStyle = '#0F0';
            context.font = fontSize + 'px monospace';
            for(let i = 0; i < rainDrops.length; i++){
                const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                context.fillText(text, i*fontSize, rainDrops[i]*fontSize);
                if(rainDrops[i]*fontSize > canvas.height && Math.random() > 0.975){
                    rainDrops[i] = 0;
                }
                rainDrops[i]++;
            }
        };
        setInterval(draw, 30);
    </script>
</body>


### My name is Matias and I live in Argentina. I'm a Backend Developer, I like linux and games.
<br>

Here are some ideas to get you started:

- 🔭 I’m currently working on "Grupo Digital".
- 🌱 I’m currently learning more about Node.
- 📫 How to reach me: Linkedin.
- ⚡ Fun fact: I like to play video games, make small projects to entertain myself and create post on taringa to teach.


[website]: https://magamex.github.io/
