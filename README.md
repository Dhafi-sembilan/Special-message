# Special-message
For the pookie one
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Special Message</title>
    <style>
        /* Gaya umum */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #f3ec78, #af4261);
            color: white;
            overflow: hidden;
        }

        .container {
            text-align: center;
            padding: 20px;
            max-width: 500px;
            width: 90%;
            background: rgba(0, 0, 0, 0.6);
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            transition: opacity 0.5s ease;
        }

        .click-box {
            margin-top: 20px;
            padding: 15px;
            background: #ff4b2b;
            color: white;
            font-size: 1.2em;
            font-weight: bold;
            cursor: pointer;
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .click-box:hover {
            transform: scale(1.1);
        }

        /* Gaya pesan */
        .message, .final-message, .end-message {
            display: none;
            font-size: 1.5em;
            line-height: 1.6;
            opacity: 0;
            transition: opacity 1s ease;
        }

        .nav-buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        .nav-button {
            padding: 10px;
            background: #ff4b2b;
            color: white;
            font-weight: bold;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.3s ease;
            flex: 1;
            text-align: center;
            margin: 0 5px;
        }

        .nav-button:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <div class="container" id="container">
        <!-- Halaman Pertama -->
        <div id="first-page">
            <h1>For the pookie one</h1>
            <p>Click the box below to reveal a special message.(harap tidak terjemahkan halaman)</p>
            <div class="click-box" onclick="showMessage('second')">Click Here!</div>
        </div>

        <!-- Halaman Kedua -->
        <div class="message" id="second-page">
            <p>Surprise! Here is your special message:</p>
            <p><font color="pink">kamu tahu gak? kenapa air laut itu rasanya asin? ya karena laut mengandung garam yang tinggi. bukan karena kencing ikan loh,ya.</font></p>
            <div class="nav-buttons">
                <div class="nav-button" onclick="showMessage('first')">Back</div>
                <div class="nav-button" onclick="showMessage('third')">Next</div>
            </div>
        </div>

        <!-- Halaman Ketiga -->
        <div class="final-message" id="third-page">
            <p>apalagi yang manis itu kamu, salah loh,ya.</p>
            <div class="nav-buttons">
                <div class="nav-button" onclick="showMessage('second')">Back</div>
                <div class="nav-button" onclick="showMessage('fourth')">Next</div>
            </div>
        </div>

        <!-- Halaman Keempat -->
        <div class="end-message" id="fourth-page">
            <p>Tapi sumpah, kamu itu emang manis. hehe...</p>
            <h6>BTW, kamu kangen gak sih, sama aku?</h6>
            <div class="nav-buttons">
                <div class="nav-button" onclick="showMessage('third')">Back</div>
            </div>
        </div>
    </div>

    <script>
        function showMessage(page) {
            // Sembunyikan semua halaman terlebih dahulu
            document.getElementById('first-page').style.display = 'none';
            document.getElementById('second-page').style.display = 'none';
            document.getElementById('third-page').style.display = 'none';
            document.getElementById('fourth-page').style.display = 'none';

            // Tampilkan halaman yang diminta
            const requestedPage = document.getElementById(page + '-page');
            requestedPage.style.display = 'block';
            setTimeout(() => {
                requestedPage.style.opacity = '1';
            }, 100);
        }
    </script>
</body>
</html>
