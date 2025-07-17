Вот пример `README.md` для вашего кастомного хука `useMediaQuery`:

---

# `useMediaQuery` – React хук для отслеживания медиа-запросов

`useMediaQuery` — это пользовательский хук React, который позволяет отслеживать изменения медиа-запросов (например, ширину экрана) в режиме реального времени.

## 📦 Установка

Добавьте файл `useMediaQuery.js` в вашу папку с хуками или утилитами.

```bash
your-project/
├── hooks/
│   └── useMediaQuery.js
```

## 📚 Использование

```jsx
import React from 'react';
import useMediaQuery from './hooks/useMediaQuery';

const MyComponent = () => {
  const isMobile = useMediaQuery('(max-width: 768px)');

  return (
    <div>
      {isMobile ? (
        <p>Вы используете мобильное устройство</p>
      ) : (
        <p>Вы используете десктоп</p>
      )}
    </div>
  );
};

export default MyComponent;
```

## ⚙️ Параметры

| Параметр | Тип      | Описание                                 |
| -------- | -------- | ---------------------------------------- |
| `query`  | `string` | Медиа-запрос (в формате CSS Media Query) |

Примеры возможных запросов:

* `(max-width: 768px)`
* `(min-width: 1024px)`
* `(orientation: portrait)`

## 🔄 Что делает хук

* При первом рендере проверяет, соответствует ли окно заданному медиа-запросу.
* Подписывается на изменения медиа-запроса с помощью `matchMedia().addEventListener("change", ...)`.
* Автоматически отписывается при размонтировании компонента.

## ✅ Преимущества

* Простота в использовании
* Поддерживает любые медиа-запросы
* Автоматическая подписка и отписка

## 📋 Пример с несколькими условиями

```jsx
const isLargeScreen = useMediaQuery('(min-width: 1200px)');
const isDarkMode = useMediaQuery('(prefers-color-scheme: dark)');
```

---

Если хочешь, могу оформить это как готовый `README.md` файл в виде кода.
