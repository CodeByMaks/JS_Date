# JS_Date

# 🌟 Введение в `new Date`, `new Set` и `new Map` 🌟

<div align="center">
  <img src="https://guypursey.com/images/observable-two-date-fields-and-number-field.gif" width="full" height="400px">
</div>

## 🕰️ `new Date` — Время под контролем

Объект `Date` в JavaScript помогает работать с датами и временем. Вот несколько способов его использования:

### 📅 Создание объекта даты:
```js
const now = new Date(); // Текущая дата и время
const specificDate = new Date('2025-01-01'); // Конкретная дата
```

# 🕰️ Четыре способа создания `new Date` в JavaScript

## 1️⃣ **Создание текущей даты и времени**
Самый простой способ создать объект `Date` — без параметров. Он возвращает текущую дату и время.

```js
const now = new Date();
console.log(now); // Например: 2025-01-02T12:34:56.789Z
```

2️⃣ Создание объекта с использованием строки
Передайте строку с датой в формате ISO или другом поддерживаемом формате.

```js
const specificDate = new Date('2025-01-01T00:00:00');
console.log(specificDate); // 2025-01-01T00:00:00.000Z
```
Поддерживаются различные форматы, например:
```js
YYYY-MM-DD (ISO)
MM/DD/YYYY (американский)
Month Day, Year (английский текстовый формат)
```
3️⃣ Создание с использованием числовых параметров
Передайте параметры: год, месяц (от 0 до 11), день, часы, минуты, секунды и миллисекунды. Непереданные параметры принимают значения по умолчанию.
```js
const dateWithParams = new Date(2025, 0, 1, 12, 30, 0); // Месяц: 0 = январь
console.log(dateWithParams); // 2025-01-01T12:30:00.000Z
```

Если указать только часть параметров:

```js
const partialDate = new Date(2025, 0, 1);
console.log(partialDate); // 2025-01-01T00:00:00.000Z
```

4️⃣ Создание на основе миллисекунд
Можно передать количество миллисекунд, прошедших с 1 января 1970 года (UTC).
```js
const timestampDate = new Date(1672531200000); // Таймстамп в миллисекундах
console.log(timestampDate); // 2023-01-01T00:00:00.000Z
```

Для получения текущего таймстампа используйте:
```js
const nowTimestamp = Date.now();
console.log(new Date(nowTimestamp));
```

## ⏳ Основные методы объекта `Date`

<div align="center">
  <img src="https://user-images.githubusercontent.com/133780/45768594-b01ea900-bc13-11e8-950a-584a3bb1c026.gif" width="full" height="400px">
</div>

### 📅 Получение компонентов даты:
- `getFullYear()` — Получить год.  
  ```js
  const date = new Date();
  console.log(date.getFullYear()); // Например: 2025
  ```

## getMonth() — Получить месяц (от 0 до 11, где 0 — январь).
```js
console.log(date.getMonth()); // Например: 0 (январь)
```

## getDate() — Получить день месяца (от 1 до 31).
```js
console.log(date.getDate()); // Например: 2
```

# 🕒 Получение компонентов времени:
## getHours() — Часы (от 0 до 23).
```js
console.log(date.getHours()); // Например: 15
```

## getMinutes() — Минуты (от 0 до 59).
```js
console.log(date.getMinutes()); // Например: 45
```

## getSeconds() — Секунды (от 0 до 59).
```js
console.log(date.getSeconds()); // Например: 30
```

## getMilliseconds() — Миллисекунды (от 0 до 999).
```js
console.log(date.getMilliseconds()); // Например: 500
```

## 🌍 Получение компонентов в формате UTC:
- getUTCFullYear() — Год в UTC.
- getUTCMonth() — Месяц в UTC.
- getUTCDate() — День месяца в UTC.
- getUTCHours() — Часы в UTC.
- getUTCMinutes() — Минуты в UTC.
- getUTCSeconds() — Секунды в UTC.
- getUTCMilliseconds() — Миллисекунды в UTC.

Пример:
```js
console.log(date.getUTCFullYear()); // Например: 2025
console.log(date.getUTCHours());    // Например: 12
```

# 🕰️ Таймстамп и время:
## getTime() — Возвращает количество миллисекунд с 1 января 1970 года.
```js
console.log(date.getTime()); // Например: 1735737600000
```

## getDay() — День недели (от 0 до 6, где 0 — воскресенье).
```js
console.log(date.getDay()); // Например: 4 (четверг)
```

# 🔄 new Set — Уникальность превыше всего

## Set — это коллекция, которая хранит только уникальные значения.

🚀 Примеры использования:
```js
const uniqueNumbers = new Set([1, 2, 2, 3, 4]);
console.log(uniqueNumbers); // Set { 1, 2, 3, 4 }
```
### 🎯 Методы Set:
* add(value) — Добавить элемент.
* delete(value) — Удалить элемент.
* has(value) — Проверить наличие элемента.
* size — Количество элементов.

Пример:
```js
uniqueNumbers.add(5);
console.log(uniqueNumbers.has(5)); // true
uniqueNumbers.delete(2);
console.log(uniqueNumbers.size);   // 4
```

🗺️ new Map — Карта к успеху
Map — коллекция, которая хранит ключи и значения. В отличие от объектов, ключом может быть что угодно!

🔑 Пример создания:
```js
const userMap = new Map();
userMap.set('name', 'Макс');
userMap.set('age', 25);
console.log(userMap.get('name')); // Макс
```

🔎 Методы Map:
* set(key, value) — Установить значение.
* get(key) — Получить значение.
* has(key) — Проверить наличие ключа.
* delete(key) — Удалить запись.
* size — Количество записей.

Пример:
```js
userMap.set('country', 'Russia');
console.log(userMap.has('age')); // true
userMap.delete('name');
console.log(userMap.size);       // 2
```

🎉 Итог
🛠️ Что выбрать?
- Используйте Date, если вы работаете с датами и временем.
- Используйте Set, когда нужны только уникальные значения.
- Используйте Map, если вы хотите гибкость с ключами.

---

<div align="center">
  <img src="https://a.d-cd.net/fGkj61MC91njUbKjZUahzEm1-IA-960.jpg" width="600px" height="300px">
</div>

---
