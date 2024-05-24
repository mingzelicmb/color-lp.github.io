<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color LP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 500px;
            border-radius: 8px;
            text-align: center;
        }
        h1 {
            text-align: center;
        }
        .color-box {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
        }
        .circle {
            width: 200px;
            height: 200px;
            border: 1px solid #ccc;
            border-radius: 50%;
        }
        .controls {
            margin-bottom: 30px;
        }
        .controls div {
            margin-bottom: 30px;
        }
        .controls input[type="range"] {
            width: 100%;
        }
        #result {
            font-weight: bold;
            margin-top: 10px;
        }
        button {
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Color LP</h1>
        <div class="color-box">
            <div id="userColor" class="circle"></div>
            <div id="randomColor" class="circle"></div>
        </div>
        <div class="controls">
            <div>
                Mode:
                <select id="modeSelect">
                    <option value="rgb">RGB</option>
                    <option value="cmyk">CMYK</option>
                    <option value="hsv">HSV</option>
                </select>
            </div>
            <div id="rgbControls">
                <div>R: <input type="range" id="rRange" min="0" max="255" value="0"></div>
                <div>G: <input type="range" id="gRange" min="0" max="255" value="0"></div>
                <div>B: <input type="range" id="bRange" min="0" max="255" value="0"></div>
            </div>
            <div id="cmykControls" style="display: none;">
                <div>C: <input type="range" id="cRange" min="0" max="100" value="0"></div>
                <div>M: <input type="range" id="mRange" min="0" max="100" value="0"></div>
                <div>Y: <input type="range" id="yRange" min="0" max="100" value="0"></div>
                <div>K: <input type="range" id="kRange" min="0" max="100" value="0"></div>
            </div>
            <div id="hsvControls" style="display: none;">
                <div>H: <input type="range" id="hRange" min="0" max="359" value="0"></div>
                <div>S: <input type="range" id="sRange" min="0" max="100" value="0"></div>
                <div>V: <input type="range" id="vRange" min="0" max="100" value="0"></div>
            </div>
        </div>
        <button id="confirmButton">Confirm</button>
        <button id="resetButton">Try Again</button>
        <div id="result"></div>
    </div>

    <script>
        function cmykToRgb(c, m, y, k) {
            let r = 255 * (1 - c) * (1 - k);
            let g = 255 * (1 - m) * (1 - k);
            let b = 255 * (1 - y) * (1 - k);
            return [r, g, b];
        }

        function hsvToRgb(h, s, v) {
            let r, g, b;
            let i = Math.floor(h * 6);
            let f = h * 6 - i;
            let p = v * (1 - s);
            let q = v * (1 - f * s);
            let t = v * (1 - (1 - f) * s);
            switch (i % 6) {
                case 0: r = v, g = t, b = p; break;
                case 1: r = q, g = v, b = p; break;
                case 2: r = p, g = v, b = t; break;
                case 3: r = p, g = q, b = v; break;
                case 4: r = t, g = p, b = v; break;
                case 5: r = v, g = p, b = q; break;
            }
            return [r * 255, g * 255, b * 255];
        }

        function updateColors() {
            const mode = document.getElementById('modeSelect').value;
            let userColor, randomColor;

            if (mode === 'rgb') {
                const r = document.getElementById('rRange').value;
                const g = document.getElementById('gRange').value;
                const b = document.getElementById('bRange').value;
                userColor = `rgb(${r}, ${g}, ${b})`;
                randomColor = `rgb(${randomRgb[0]}, ${randomRgb[1]}, ${randomRgb[2]})`;
            } else if (mode === 'cmyk') {
                const c = document.getElementById('cRange').value / 100;
                const m = document.getElementById('mRange').value / 100;
                const y = document.getElementById('yRange').value / 100;
                const k = document.getElementById('kRange').value / 100;
                const rgb = cmykToRgb(c, m, y, k);
                userColor = `rgb(${rgb[0]}, ${rgb[1]}, ${rgb[2]})`;
                randomColor = `rgb(${randomRgb[0]}, ${randomRgb[1]}, ${randomRgb[2]})`;
            } else if (mode === 'hsv') {
                const h = document.getElementById('hRange').value / 360;
                const s = document.getElementById('sRange').value / 100;
                const v = document.getElementById('vRange').value / 100;
                const rgb = hsvToRgb(h, s, v);
                userColor = `rgb(${rgb[0]}, ${rgb[1]}, ${rgb[2]})`;
                randomColor = `rgb(${randomRgb[0]}, ${randomRgb[1]}, ${randomRgb[2]})`;
            }

            document.getElementById('userColor').style.backgroundColor = userColor;
            document.getElementById('randomColor').style.backgroundColor = randomColor;
        }

        function calculateError() {
            const mode = document.getElementById('modeSelect').value;
            let userRgb, error;

            if (mode === 'rgb') {
                userRgb = [
                    parseInt(document.getElementById('rRange').value),
                    parseInt(document.getElementById('gRange').value),
                    parseInt(document.getElementById('bRange').value)
                ];
            } else if (mode === 'cmyk') {
                const c = document.getElementById('cRange').value / 100;
                const m = document.getElementById('mRange').value / 100;
                const y = document.getElementById('yRange').value / 100;
                const k = document.getElementById('kRange').value / 100;
                userRgb = cmykToRgb(c, m, y, k);
            } else if (mode === 'hsv') {
                const h = document.getElementById('hRange').value / 360;
                const s = document.getElementById('sRange').value / 100;
                const v = document.getElementById('vRange').value / 100;
                userRgb = hsvToRgb(h, s, v);
            }

            error = Math.sqrt(
                Math.pow(userRgb[0] - randomRgb[0], 2) +
                Math.pow(userRgb[1] - randomRgb[1], 2) +
                Math.pow(userRgb[2] - randomRgb[2], 2)
            );

            document.getElementById('result').innerText = `Error: ${error.toFixed(2)}`;
        }

        function resetRandomColor() {
            randomRgb = [
                Math.floor(Math.random() * 256),
                Math.floor(Math.random() * 256),
                Math.floor(Math.random() * 256)
            ];
            updateColors();
            document.getElementById('result').innerText = '';
        }

        let randomRgb = [
            Math.floor(Math.random() * 256),
            Math.floor(Math.random() * 256),
            Math.floor(Math.random() * 256)
        ];

        // Handle mode change
        document.getElementById('modeSelect').addEventListener('change', function () {
            const mode = this.value;
            document.getElementById('rgbControls').style.display = 'none';
            document.getElementById('cmykControls').style.display = 'none';
            document.getElementById('hsvControls').style.display = 'none';

            if (mode === 'rgb') {
                document.getElementById('rgbControls').style.display = 'block';
            } else if (mode === 'cmyk') {
                document.getElementById('cmykControls').style.display = 'block';
            } else if (mode === 'hsv') {
                document.getElementById('hsvControls').style.display = 'block';
            }

            updateColors();
        });

        // Update colors on slider change
        document.querySelectorAll('input[type="range"]').forEach(input => {
            input.addEventListener('input', updateColors);
        });

        // Handle confirm button click
        document.getElementById('confirmButton').addEventListener('click', calculateError);

        // Handle reset button click
        document.getElementById('resetButton').addEventListener('click', resetRandomColor);

        // Initial color update
        updateColors();
    </script>
</body>
</html>
