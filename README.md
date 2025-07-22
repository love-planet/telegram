
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Открытие Telegram</title>
  <style>
    body {
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #111;
      color: white;
      flex-direction: column;
      text-align: center;
    }
    .button {
      padding: 16px 28px;
      font-size: 20px;
      background-color: #2a9d8f;
      color: white;
      border-radius: 10px;
      text-decoration: none;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h2>Нажмите кнопку, чтобы открыть Telegram</h2>
  <a class="button" id="tgButton">Перейти в Telegram</a>

  <script>
    const url = "https://t.me/+wEM0vEXNm3o4ZTk6";

    document.getElementById("tgButton").addEventListener("click", () => {
      // Создаём ссылку и кликаем её для открытия во внешнем браузере
      const a = document.createElement("a");
      a.href = url;
      a.target = "_blank";
      a.rel = "noopener noreferrer";
      document.body.appendChild(a);
      a.click();

      // fallback: если TikTok заблокировал .click(), то пытаемся напрямую
      setTimeout(() => {
        window.location.href = url;
      }, 800);
    });
  </script>
</body>
</html>
