# Планирование автоматизации.
## Тест план

**Теустируемые функции:** 
- переход с гавной страницы к курсу "Тестировщик ПО"
- переход к форме записи на курс и ее заполнение

# Автоматизируемые сценарии

### Переход к странице курса "Тестировщик ПО" и фоме записи.

**Варианты перхода к выбору профессии Тестировщик ПО**

1. Переход с главной страницы [Нетологии](https://netology.ru/) с помощью кнопки "Католог курсов" через вбыор раздела "Программирование"
![Католог курсов](Pictures/финальное%20дз1.png)
![Выбор направления](Pictures/финальное%20дз2.png)
![Выбор профессии](Pictures/финальное%20дз3.png)

2. Переход с главной страницы [Нетологии](https://netology.ru/) через информационный блок "Учим прфессиям и навыкам" и выбор направления обучения "Программирование"
![Выбор направления](Pictures/финальное%20дз4.png)
![Выбор профессии](Pictures/финальное%20дз3.png)

3. Переход с главной страницы [Нетологии](https://netology.ru/) через блок "Выберите вектор развития" по кнопке "Выберите курс"
![Выбпать курс](Pictures/финальное%20дз5.png)
![Выбор профессии](Pictures/финальное%20дз6.png)


**Варианты перехода к форме записи на курс**
1. С начального экрана страницы курса "Тестировщик" по кнопке "Записаться"
![Записаться](Pictures/финальное%20дз7.png)

2. При скролле страницы курса "Тестировщик" вниз до появления кнопки записаться в верхнем правом углу.
![Записаться](Pictures/финальное%20дз8.png)

3. При скролле страницы курса "Тестировщик" вниз до появления формы записи на курс.
   ![Форма записи](Pictures/финальное%20дз9.png)

**Заполнение и отправка формы**

_Требования к заполнению полей (валидные значения*)_

- _обязательное поле "Имя": заполняется на латинице или кириллице, может содеожать пробел и дефис/тире, заполняется минимум двумя буквами_
- _обязательное поле "Телефон": может содержать цифры, круглые скобки, пробел и дефис/тире в формате +9 (999) 999-99-99, от 9 до 14 символов включительно_
- _обязательное поле "Электронная почта": заполняется латиницей, должно содержать локальную часть адреса состаящую из букв и/или цифр, "собачку" ( @ ) и доменную часть имени с точкой (.)._
- _не обязательное поле "Промокод": латиница, кириллица, цифры и спецсимволы, кроме пробела_

1. Успешная отправка валидно* заполненной формы записи на курс "Тестировщик ПО", включая проверку ввода действующего промокода (с изменением стоимости курса) и перехода на страницы с условиями политики и пользовательского соглашения
2. Появление сообщение "Обязательное поле" у полей "Имя", "Телефон" и "Электроннаяпочта" при оставлении их пустыми и нажатии на кнопку "Записаться"
3. Появление сообщения "Должно состоять из букв" у поля "Имя" при заполнение его спецсимволами в форме записи на курс "Тестировщик ПО"
4. Появление сообщения "Должно состоять из букв" у поля "Имя" при заполнение его цифрами в форме записи на курс "Тестировщик ПО"
5. Появление сообщения "Должно быть не короче 2 символов" у поля "Имя" при заполнение его одной буквой в форме записи на курс "Тестировщик ПО"
6. Появление сообщения "Обязательное поле" у поля "Имя" при оставление поля пустым в форме записи на курс "Тестировщик ПО"
7. Появление сообщения "Номер в формате +9 (999) 999-99-99" у поля "Телефон" при заполнение поля не валидными данными
8. Появление сообщения "Обязательное поле" у поля "Телефон" при оставление поля пустым в форме записи на курс "Тестировщик ПО"
9.  Появление сообщения "Обязательное поле" при оставлении поля "Электронная почта" пустым
10. Появление сообщения "Неверный email" у поля "Электронная почта" при заполнении не валидными данными
11. Появление сообщения "Устаревший промокод" у поля "Промокод" при вводе устаревшего валидного промокода в форме записи на курс "Тестировщик ПО" 
12. Появление сообщения "Промокод не найден" у поля "Промокод" при вводе не валидного промокода в форме записи на курс "Тестировщик ПО"

## Перечень используемых инструментов с обоснованием выбора:
- IntelliJ IDEA, удобная среда подготовки авто-тестов;
- Язык программирования Java;
- JDK 11 или выше, т.к. потребуются инструменты работающие с Java;
- JUnit Jupiter, инструмент тестирования, более превычен нежели JUnit4 или TestNG;
- Gradle, система сборки с удобной настройкой зависимостей
- Selenide, очень удобен при тестировании веб-интерфейса;
- Faker, для генерации данных при отправке формы;
- DBeaver, для просмотра базы данных; если будет предостален "слепок" SUT, то необходим доступ к удаленному серверу с предустановленными:
  
  GIT

   Docker

   Bash

   для развертывания SUT и базы данных;

- GIT, в качестве системы контроля версий и хранилища авто-тестов;
- Allure, система репортинга для контроля прогона тестов и анализа возникающих ошибок (более сложные системы репортинга будут излишни);

## Перечень необходимых разрешений/данных/доступов:
- Hеобходимо письменное разрешение на проведение тестирования администрации веб-сайта Нетологии;
- Hеобходим доступ к базе данных записи на обучение профессии "Тестировщик ПО": либо к действующей базе данных (что всегда несет риски); либо "слепок" SUT, готовый к интеграции с пустой базой данных (либо "слепок" SUT и данные для интеграции с пустой базой данных).
- Доступ к существующим тестовым данным (если они есть).
## Перечень и описание возможных рисков при автоматизации:
- Зависимость авто-тестов от текущей реализации веб-элементов, даже не значительное их изменение может привести к падению авто-тестов;
- Авто-тесты не проверяют графическую составляющую, а именно едет ли верстка при тех или иных действиях, комфортна ли выбранная цветовая схема оформления и тд.
- Появление "мусорных" записей в БД.
- Дополнительная нагрузка на сервер.
## Перечень необходимых специалистов для автоматизации:
Данный проект не сложный, поэтому будет достаточно одного инженера по автоматизации, который знаком с основами необходимого инструментария, основами UI и API тестирования и базовыми навыками написания автотестов с использованием паттерна Page Object.
## Интервальная оценка с учётом рисков (в часах):
Для осуществления этого плана автоматизации, ориентировочно потребуется 24 рабочих часа.