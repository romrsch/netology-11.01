## Домашнее задание к занятию "11.01 Введение в микросервисы"

### Задача 1: Интернет Магазин

>Руководство крупного интернет магазина, у которого постоянно растёт пользовательская база и количество заказов рассматривает возможность переделки своей внутренней ИТ системы на основе микросервисов.
>
>Вас пригласили в качестве консультанта для оценки целесообразности перехода на микросервисную архитектуру.
>
>Опишите какие выгоды может получить компания от перехода на микросервисную архитектуру и какие проблемы необходимо будет решить в первую очередь.

***

### Ответ:

Выгоды, которые может получить компания от перехода на микросервисную архитектуру:

* Отказоустойчивость: при падении одного из сервисов, все остальные остаются в работе. 
* Масштабируемость: нужные сервисы можно безболезненно дополнить и расширить, когда появится такая необходимость. 
* Легко разрабатывать и поддерживать: микросервис будет ориентирован только на конкретную бизнес-функцию.
* Одна микрослужба запускается быстрее: одна микрослужба содержит меньше кода, поэтому она будет запускаться быстрее.
* Гибкость, можно попробовать внедрить новую технологию, внести правки в код "своего сервсиса" без рисков сломать остальные сервисы, а при неудаче, можно просто откатить изменения.
* Лёгкость выведения написанного кода в работу. Небольшое количество кода обеспечивает быстрый деплой, возможность автоматизации CI/CD 

Микросервисы - это не "лекарство от всех бед", 
Проблемы, которые нужно будет решить:

* Нужно будет понять, что именно нужно "дробить" на микросервисы, чтобы не получить избыточное количество микросервисов.
* Потребуется подумать над инфрастуктурой, где и на чём будет работать наша распределенная система (СХД, вычислительные мощности, сеть)
* Потребуется время, чтобы перестроить и наладить работу отделов разработки, тестировщиков, инженеров, руководителей.
* Потребуется грамотно построить коммуникации между микросервисами, они хоть и изолированы, но им в любом случае придётся обмениваться запросами и ответами друг с другом. 
* Сложность тестирования: сначала нужно тестировать каждый отдельный микросервис, а потом тестировать корректное взаимодействие его с другими микросервисами.
* Рост числа сервисов повлечет за собой и рост числа баз данных, в отличие от монолитной архитектуры, микросервисы используют не одну общую базу данных.


