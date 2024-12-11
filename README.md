# Веб-приложение для управления киберспортивными соревнованиями

## Описание проекта
Данный проект представляет собой веб-приложение для реализации балльно-рейтинговой системы оценки успеваемости студентов. Система предназначена для учета и оценки знаний студентов в учебных заведениях с помощью баллов, которые накапливаются за различные виды деятельности, такие как контрольные работы, лекции, экзамены, практические задания и участие в дополнительных активностях.
Технологический стек: **Spring Boot** для серверной части и **React** для фронтенда.

---

## Диаграммы

### 1. Диаграмма структуры функциональных возможностей (Mind Map)

Эта диаграмма отображает основные функции системы, включая регистрацию пользователей, управление оценками, вычисление итогового рейтинга, отчеты и уведомления.

```mermaid
mindmap
  root((Балльно-рейтинговая система))
    Регистрация
      Студентов
      Преподавателей
    Оценка успеваемости
      Практические задания
      Экзамены
      Дополнительные активности
    Итоговый рейтинг
      Вычисление баллов
      Формирование рейтинга
    Отчеты
      Индивидуальные
      Групповые
      Академическая успеваемость
    Уведомления
      Оценки
      Статусы заданий
```

### 2. Диаграмма путешествия пользователя (User Journey)

Эта диаграмма иллюстрирует путь пользователя (студента или преподавателя) в системе — от регистрации до получения отчетов о результатах.

```mermaid
journey
    title Путешествие пользователя в балльно-рейтинговой системе
    section Регистрация пользователя
      Студент: 5: Регистрируется в системе
      Преподаватель: 5: Регистрируется в системе
    section Проставление оценок
      Преподаватель: 5: Проставляет баллы за лекции и задания
      Система: 4: Обрабатывает баллы и сохраняет в базе данных
    section Вычисление итогового рейтинга
      Система: 5: Вычисляет итоговый балл студента
      Студент: 4: Просматривает итоговый рейтинг
    section Формирование отчетов
      Система: 5: Генерирует отчет по успеваемости
      Преподаватель: 5: Анализирует отчет по студентам
    section Оповещение о результатах
      Система: 5: Отправляет уведомление о новых оценках студенту
      Студент: 4: Получает уведомление и проверяет оценки
```

### 3. Квадрантная диаграмма (Quadrant Chart)

Эта диаграмма показывает распределение функциональных возможностей системы по важности и сложности.

```mermaid
quadrantChart
    title Quadrant Chart of System Features
    x-axis Ease of Use --> Complexity of Use
    y-axis Value --> Low Value
    quadrant-1 High value, easy to use
    quadrant-2 Low value, easy to use
    quadrant-3 High value, complex to use
    quadrant-4 Low value, complex to use
    User Registration: [0.9, 0.7]
    Grade Management: [0.8, 0.6]
    Rating Calculation: [0.7, 0.9]
    Report Generation: [0.9, 0.5]
    Notification System: [0.8, 0.4]
    Activity Monitoring: [0.7, 0.8]
```

### 4. Диаграмма истории разработки (Git Graph)

Эта диаграмма демонстрирует этапы разработки приложения, включая создание микросервисов для оценки, регистрации пользователей, генерации отчетов и системы уведомлений.


```mermaid
gitGraph
    commit id: "Initial commit - Setup project structure"
    commit id: "Added student registration service"
    branch develop
    checkout develop
    commit id: "Implemented grade management functionality"
    commit id: "Added rating calculation module"
    checkout main
    commit id: "Integrated user registration and grade management"
    
    checkout develop
    branch feature/grade-service
    checkout feature/grade-service
    commit id: "Developed grade management microservice"
    checkout develop

    branch feature/rating-service
    checkout feature/rating-service
    commit id: "Developed rating calculation service"
    checkout develop

    branch feature/report-service
    checkout feature/report-service
    commit id: "Developed report generation service"
    checkout develop

    branch feature/notification-service
    checkout feature/notification-service
    commit id: "Developed notification service"
    checkout develop

    checkout main
    commit id: "Integrated all microservices into main"
    checkout develop
    merge feature/grade-service id: "Merged grade service"
    merge feature/rating-service id: "Merged rating service"
    merge feature/report-service id: "Merged report service"
    merge feature/notification-service id: "Merged notification service"
    commit id: "Final version with all services integrated"
    commit id: "Bug fixes and optimizations"
```
