# Dependencies and Setup for Projex Backend

Этот документ описывает зависимости и инструменты, установленные для проекта `projex-backend`, и объясняет их назначение.

## Установленные зависимости

### 1. `typescript`
- **Описание**: TypeScript — это строго типизированное надмножество JavaScript, которое компилируется в обычный JavaScript.
- **Причина установки**: Он используется для того, чтобы добавить статическую типизацию и улучшить качество кода, упрощая выявление ошибок на этапе разработки.

### 2. `ts-node`
- **Описание**: Это утилита для выполнения TypeScript кода напрямую в Node.js, без предварительной компиляции.
- **Причина установки**: Используется для запуска TypeScript файлов непосредственно, что упрощает процесс разработки, избегая ручной компиляции кода в JavaScript.

### 3. `@types/node`
- **Описание**: Это определения типов для Node.js, которые позволяют использовать встроенные функции Node.js с поддержкой типов TypeScript.
- **Причина установки**: Эти определения типов позволяют писать типобезопасный код, использующий API Node.js в проектах с TypeScript.

### 4. `express`
- **Описание**: Express — это минималистичный веб-фреймворк для Node.js, используемый для создания серверных приложений.
- **Причина установки**: Express используется для создания маршрутов и обработки HTTP-запросов в backend приложении.

### 5. `body-parser`
- **Описание**: Body-parser используется для парсинга тела запросов в формате JSON или URL-encoded.
- **Причина установки**: Эта библиотека позволяет серверу обрабатывать данные, отправленные в теле запросов, такие как формы или JSON данные.

### 6. `cors`
- **Описание**: CORS — это middleware для управления политикой кросс-доменных запросов.
- **Причина установки**: Используется для разрешения или ограничения доступа к API из других доменов.

### 7. `dotenv`
- **Описание**: Библиотека для работы с переменными окружения, загружающимися из файла `.env`.
- **Причина установки**: Позволяет управлять конфиденциальными данными (такими как ключи API или настройки базы данных) через файл `.env`, что улучшает безопасность.

### 8. `helmet`
- **Описание**: Helmet помогает защитить Express-приложение, устанавливая различные заголовки HTTP для безопасности.
- **Причина установки**: Улучшает безопасность приложения за счёт автоматического управления безопасностью HTTP-заголовков.

### 9. `morgan`
- **Описание**: Morgan — это middleware для логирования HTTP-запросов.
- **Причина установки**: Используется для ведения логов запросов на сервер, что помогает в диагностике и мониторинге.

### 10. `rimraf`
- **Описание**: Rimraf — это утилита для удаления файлов и папок.
- **Причина установки**: Используется для очистки файлов и директорий в процессе сборки и разработки.

### 11. `concurrently`
- **Описание**: Concurrently — это инструмент для параллельного запуска нескольких команд одновременно.
- **Причина установки**: Используется для запуска нескольких процессов, таких как сервер и клиент, в одном командном окне.

### 12. `nodemon`
- **Описание**: Nodemon — это утилита для автоматической перезагрузки сервера при изменении файлов.
- **Причина установки**: Упрощает процесс разработки, автоматически перезагружая сервер при изменении кода.

### 13. `@types/cors`
- **Описание**: Определения типов для библиотеки `cors`.
- **Причина установки**: Эти определения позволяют использовать CORS с поддержкой типов TypeScript.

### 14. `@types/morgan`
- **Описание**: Определения типов для библиотеки `morgan`.
- **Причина установки**: Эти определения позволяют использовать Morgan с поддержкой типов TypeScript.

## Структура проекта

### package.json

Файл `package.json` был обновлён для управления зависимостями и скриптами. В частности, после установки зависимостей файл выглядит следующим образом:

```json
{
  "name": "projex-backend",
  "version": "1.0.0",
  "main": "index.js",
  "directories": {
    "doc": "docs"
  },
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "seed": "ts-node prisma/seed.ts"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "devDependencies": {
    "@types/cors": "^2.8.17",
    "@types/morgan": "^1.9.9",
    "@types/node": "^22.7.5",
    "concurrently": "^9.0.1",
    "nodemon": "^3.1.7",
    "rimraf": "^6.0.1",
    "ts-node": "^10.9.2",
    "typescript": "^5.6.2"
  },
  "dependencies": {
    "@prisma/client": "^5.20.0",
    "body-parser": "^1.20.3",
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.21.1",
    "helmet": "^8.0.0",
    "morgan": "^1.10.0",
    "prisma": "^5.20.0"
  }
}
