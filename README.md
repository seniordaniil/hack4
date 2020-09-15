Для лаконичности проблема была решена одной строкой. В реальном приложении это могло бы выглядеть примерно так:

```javascript
const url = new URL(window.location.href);

// Сохраняем параметры
const params = url.search.slice(1);

// Удаляем параметры из url
url.search = '';

// Изменяем url страницы
window.history.replaceState(null, null, url.toString());

```
