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

# -go-for-President- 
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Проверка кандидата в президенты</title>
</head>
<body>
  <h2>🗳️ Проверка на возможность баллотироваться в президенты</h2>

  <label>Возраст:</label>
  <input type="number" id="age"><br><br>

  <label>Вы гражданин страны?</label>
  <select id="citizen">
    <option value="yes">Да</option>
    <option value="no">Нет</option>
  </select><br><br>

  <label>Сколько лет вы прожили в стране?</label>
  <input type="number" id="years"><br><br>

  <button onclick="canRunForPresident()">Проверить</button>

  <p id="resultPresident"></p>

  <script>
    function canRunForPresident() {
      const age = parseInt(document.getElementById("age").value);
      const isCitizen = document.getElementById("citizen").value === "yes";
      const yearsInCountry = parseInt(document.getElementById("years").value);

      if (age >= 35 && isCitizen && yearsInCountry >= 10) {
        document.getElementById("resultPresident").textContent =
          "Вы можете баллотироваться в президенты! 🇰🇿";
      } else {
        document.getElementById("resultPresident").textContent =
          "К сожалению, вы не соответствуете условиям для участия в выборах.";
      }
    }
  </script>
</body>
</html>

