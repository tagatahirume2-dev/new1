<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>認証成功</title>
    <style>
        body {
            font-family: sans-serif;
            text-align: center;
            margin-top: 100px;
            background: #f0f0f0;
        }
        .box {
            background: white;
            padding: 30px;
            border-radius: 12px;
            display: inline-block;
            box-shadow: 0 0 15px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <div class="box">
        <h1 id="msg">読み込み中…</h1>
    </div>

    <script>
        const params = new URLSearchParams(window.location.search);
        const name = params.get("name");
        const id = params.get("id");

        if (name && id) {
            document.getElementById("msg").innerText = `${name} さん（ID: ${id}）、認証成功！`;
        } else {
            document.getElementById("msg").innerText = "認証情報がありません。";
        }
    </script>
</body>
</html>
