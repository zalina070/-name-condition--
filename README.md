# -name-condition--
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Проверка имени</title>
</head>
<body>
  <h2>🎁 Проверка подарка по имени</h2>

  <label for="name">Введите ваше имя:</label>
  <input type="text" id="name">
  <button onclick="checkName()">Проверить</button>

  <p id="result"></p>

  <script>
    function checkName() {
      const name = document.getElementById("name").value;
      let message = "";

      if (name === "Жасмин") {
        message = "Сегодня твой счастливый день! Получи свой приз 🎉";
      } else if (name === "Aidana") {
        message = "Сегодня и твой счастливый день! Получи свою скидку 🛍️";
      } else {
        message = `Добро пожаловать, ${name} 🙂`;
      }

      document.getElementById("result").textContent = message;
    }
  </script>
</body>
</html>
