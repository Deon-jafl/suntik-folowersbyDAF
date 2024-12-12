# suntik-folowersbyDAF
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suntik Followers</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            text-align: center;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        input[type="text"], input[type="number"] {
            padding: 10px;
            width: 80%;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            padding: 10px 20px;
            color: #fff;
            background-color: #007bff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Suntik Followers</h1>
        <p>Masukkan username Instagram Anda:</p>
        <form id="formSuntik">
            <input type="text" id="username" placeholder="Username Instagram" required><br>
            <input type="number" id="jumlah" placeholder="Jumlah Followers" required><br>
            <button type="submit">Suntik Followers</button>
        </form>
        <p id="result"></p>
    </div>
    <script>
        document.getElementById('formSuntik').addEventListener('submit', function(e) {
            e.preventDefault();
            const username = document.getElementById('username').value;
            const jumlah = document.getElementById('jumlah').value;

            if (username && jumlah) {
                document.getElementById('result').innerText = `Followers berhasil disuntik ke ${username} sebanyak ${jumlah}!`;
            } else {
                document.getElementById('result').innerText = 'Harap isi semua data!';
            }
        });
    </script>
</body>
</html>
