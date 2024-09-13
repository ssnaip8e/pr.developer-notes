# Колоночная сетка через grid-сетку


```html
<!-- ПРИМЕР РАЗМЕТКИ -->
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Сетка</title>
</head>
<body>

  <div class="container">
    <header class="header"></header>
    <nav class="nav"></nav>
    <main class="main"></main>
    <footer class="footer"></footer>
  </div>

</body>
</html>
```

```css
/* Настройка сетки, где контейнер определяет
  колоночную систему */
.container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
}
.header {
  grid-column: span 12;
}
.nav {
  grid-column: span 4;
}
.main {
  grid-column: span 8;
}
.footer {
  grid-column: span 12;
}

/* Адаптив под планшеты и смартфоны */
@media screen and (max-width: 768px) {
  .nav {
    grid-column: span 6;
  }
  .main {
    grid-column: span 6;
  }
}
@media screen and (max-width: 480px) {
  .nav {
    grid-column: span 12;
  }
  .main {
    grid-column: span 12;
  }
}

/* Настройка навигации выше всех блоков */
@media screen and (max-width: 480px) {
  .nav {
    grid-row: 1;
    grid-column: span 12;
  }
}
```