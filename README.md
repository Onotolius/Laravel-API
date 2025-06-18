# Laravel To-Do REST API

Простой API для управления задачами (To-Do) на Laravel 11.
Используется ресурсный контроллер и маршруты в `routes/api.php`.

## 🔧 Установка

```bash
git clone https://github.com/Onotolius/REST_API.git
cd REST_API
composer install
php artisan migrate
php artisan serve
```

## 📌 Эндпоинты

Все запросы идут через `/api` (например, `/api/tasks`).

### 🔍 Получить все задачи

```bash
curl -X GET http://localhost:8000/api/tasks
```

### ➕ Создать задачу

```bash
curl -X POST http://localhost:8000/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy milk", "description": "2 liters of milk"}'
```

### 📄 Показать задачу по ID

```bash
curl -X GET http://localhost:8000/api/tasks/1
```

### ✏️ Обновить задачу по ID

```bash
curl -X PUT http://localhost:8000/api/tasks/1 \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy oat milk", "description": "1 liter, unsweetened"}'
```

### ❌ Удалить задачу по ID

```bash
curl -X DELETE http://localhost:8000/api/tasks/1
```

---
