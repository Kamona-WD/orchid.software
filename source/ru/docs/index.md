---
title: Документация
description: 
extends: _layouts.documentation.ru
section: main
---

## Введение

**ORCHID** - это пакет для создания приложений в стиле администрирования на фреймворке Laravel. Позволяет абстрагировать общие шаблоны бизнес-приложений, чтобы разработчикам было легко реализовывать красивые и элегантные интерфейсы без особых усилий. Основными местами применения являются: backoffice-приложения, админ панели, системы управления контентом и т.п.


> **Обратите внимание!** Руководство содержит информацию по использованию пакета, при этом не поясняет использование фреймворка. Настоятельно рекомендуется ознакомиться с документацией [«Laravel»](https://laravel.com/docs/)


## Почему разработка станет быстрее?

Классическое веб-приложение представляет собой подсистему с общей трёхъярусной архитектурой, которая включет в себя:

- **Презентационный уровень** - графический интерфейс, представленный пользователю (браузеру), включая javascript сценарии, стили и ресурсы.

- **Уровень прикладной логики** - в нашем случае это фреймворк - связующее звено, где сосредоточена большая часть бизнес-логики, работа с базой данных (Eloquent), отправка ресурсов и различная обработка.

- **Уровень управления ресурсами** - обеспечивает хранение данных, как правило реализуется средствами систем управления базами данных (MySQL,PostgreSQL,Microsoft SQL Server,SQLite).
 
 
![Architecture](https://orchid.software/assets/img/scheme/architecture.jpg)

Сокращение времени разработки непосредственно связано с распределением обязанностей между каждым из уровней. Это особенно заметно, когда необходимо создавать вспомогательный код, в то время как, большую часть действительно полезной работы берёт на себя прикладной слой.

Как различные примеры противопоставления обязанностями можно привести:
- Генерация `HTML` шаблонизатором `Blade` или фреймворком `Vue`.
- Использование `ORM` или хранимых процедур.

В зависимости от выбора решений будут и распределены обязанности, где у каждого решения есть как плюсы так и минусы.

Точно так же, платформа наделяет прикладной уровень новыми обязанностями по управлению отображением и прокладыванию моста к данным.

```php
Classic          |   Orchid
├── Route        |   ├── Route   
├── Model        |   ├── Model 
├── Controller   |   └── Screen
└── View         |
    ├── HTML     |
    ├── CSS      |
    └── JS       |
```

## Как установить платформу?

Платформа свободно распространяется через интернет, [исходные коды](https://github.com/orchidsoftware/platform) и [информация о выпусках](https://github.com/orchidsoftware/platform/releases) опубликованы на GitHub. В руководстве по [установке](/ru/docs/installation/) содержатся подробные инструкции. 


> Для предложения улучшений этого руководства, [создайте новый issue](https://github.com/orchidsoftware/orchid.software/issues). 
При появлении вопросов или нахождения ошибки по документации, пожалуйста, укажите главу и сопутствующий текст, что бы указать на ошибку.