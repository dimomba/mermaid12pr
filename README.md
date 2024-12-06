# Структура функциональных возможностей (Mind Map)
Карта мыслей представляет собой структурированное дерево, показывающее взаимосвязи между различными функциональными возможностями системы управления гостиницей.
Цель: Помогает визуализировать компоненты системы и определить их взаимосвязь.

## Архитектура системы
```mermaid
mindmap
  root((Управление гостиницей))
    Основные процессы
      Бронирование
        Онлайн
        Офлайн
        Групповые бронирования
      Прием гостей
        Регистрация
        Заселение
        Выселение
      Управление номерами
        Доступность
        Уборка
        Обслуживание
      Финансовый учет
        Оплата
        Возвраты
        Отчетность
    Инструменты и технологии
      Используемые системы
        PMS (Property Management System)
        CRM
        ERP
      Используемые технологии
        Базы данных
          SQL
        Языки программирования
          Python
          JavaScript
          Java
        Сетевые протоколы
          HTTP/HTTPS
          API
    Оптимизация и безопасность
      Оптимизация
        Автоматизация процессов
        Балансировка нагрузки
      Безопасность
        Шифрование данных
        Аутентификация
        Авторизация
    Примеры использования
      Гостиничные сети
      Апартаменты
    Архитектура системы
      Компоненты
        Клиент
          Веб-приложение
          Мобильное приложение
        Сервер
        Хранилище данных
          Реляционные БД
          Кеширование
            Redis
            Memcached
```

### Пояснение диаграммы
Включает модули: баз данных, сетевых протоколов, клиент-серверной архитектуры.
Подразделяется на подмодули, такие как авторизация, обработка данных, API, мобильные приложения и прочее.

# Диаграмма путешествия пользователя (User Journey Diagram)
```mermaid
journey
    title Путешествие пользователя информационной системы гостиницы
    section Регистрация
      Пользователь заходит на сайт: 5: Пользователь
      Заполняет форму регистрации: 4: Пользователь
      Получает подтверждение регистрации: 5: Система
    section Выбор номера
      Пользователь переходит в меню выбора: 5: Пользователь
      Выбирает фильтры или сортировку: 4: Пользователь
      Система отображает номера по заданным параметрам: 5: Система
      Пользователь открывает детали номера: 4: Пользователь
    section Добавление бронирования
      Пользователь добавляет бронирование: 5: Пользователь
      Система обновляет список бронирований: 5: Система
      Пользователь проверяет бронирования: 4: Пользователь
    section Оформление заказа
      Пользователь переходит к оформлению бронирования: 5: Пользователь
      Система отображает итоговую стоимость: 5: Система
      Пользователь подтверждает заказ: 5: Пользователь
      Система отправляет данные в платёжную систему: 5: Система
      Платёжная система подтверждает успешную транзакцию: 5: Платёжная система
      Система уведомляет пользователя об успешной оплате: 5: Система
    section Управление бронированием
      Пользователь изменяет статус бронирования: 4: Пользователь
      Система обновляет статус бронирования: 5: Система
    section Завершение
      Пользователь оставляет отзыв о гостинице: 4: Пользователь
      Система сохраняет отзыв: 5: Система
      Пользователь выходит из системы: 5: Пользователь
```

# Квадрант-граф
```mermaid
quadrantChart
  title Hotel Management Feature Prioritization
  x-axis Priority Low to High
  y-axis Complexity Low to High
  quadrant-1 Plan for the near future
  quadrant-2 Implement immediately
  quadrant-3 Consider discarding
  quadrant-4 Requires detailed analysis
  "Guest Chat": [0.3, 0.8]
  "Guest Feedback": [0.4, 0.7]
  "Booking History": [0.5, 0.6]
  "Financial Reports": [0.8, 0.9]
  "Payment Integration": [0.7, 0.9]
  "Room Occupancy Analytics": [0.9, 0.8]
  "Booking Notifications": [0.2, 0.3]
  "Service Recommendations": [0.3, 0.2]
  "Save Guest Preferences": [0.1, 0.2]
  "Room Sorting": [0.7, 0.4]
  "User Authorization": [0.9, 0.5]
  "Add to Favorites": [0.8, 0.4]
```

# Гит граф (Gitgraph)
```mermaid
gitGraph:
   commit id: "Initial commit"
   branch master
   commit id: "Commit to master"
   branch feature/room-booking
   commit id: "Room booking feature"
   commit id: "Room booking feature - second commit"
   checkout master
   merge feature/room-booking
   commit id: "Merged room booking feature into master"
   branch feature/guest-registration
   commit id: "Guest registration feature"
   commit id: "Guest registration feature - second commit"
   checkout master
   merge feature/guest-registration
   commit id: "Merged guest registration feature into master"
   branch feature/payment-processing
   commit id: "Payment processing feature"
   checkout master
   merge feature/payment-processing
   commit id: "Merged payment processing feature into master"
   branch feature/room-service
   commit id: "Room service feature"
   checkout master
   merge feature/room-service
   commit id: "Merged room service feature into master"
```
