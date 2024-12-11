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
      Регистрируется в системе: 5: Студент, Преподаватель
    section Проставление оценок
    Проставляет баллы за лекции и задания  : 5: Преподаватель
       Обрабатывает баллы и сохраняет в базе данных: 4:Система
    section Вычисление итогового рейтинга
      Вычисляет итоговый балл студента: 5: Система
      Просматривает итоговый рейтинг: 4: Студент
    section Формирование отчетов
     Генерирует отчет по успеваемости : 5: Система
      Анализирует отчет по студентам: 5: Преподаватель
    section Оповещение о результатах
     Отправляет уведомление о новых оценках студенту : 5: Система
     Получает уведомление и проверяет оценки : 4: Студент
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

    checkout develop
    merge feature/grade-service id: "Merged grade service"
    merge feature/rating-service id: "Merged rating service"
    merge feature/report-service id: "Merged report service"
    merge feature/notification-service id: "Merged notification service"
    commit id: "Final version with all services integrated"
  
    checkout main
    merge develop id: "Integrated all microservices into main"

    checkout develop
    commit id: "Bug fixes and optimizations"

    checkout main
    merge develop id: "Bug fixed"
```
