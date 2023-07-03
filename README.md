# SoftWeather. Тестовое задание в команду финтеха Golang.

## Проблема

В ходе работы зачастую приходится искать нестандартные и оптимизированные пути решения задач. Этим тестовым заданием мы хотим оценить твое умение выполнять задачу, имея неполные данные о ней, а также умение самостоятельно принимать решения и соблюдать качество кода, поэтому пиши код так, как бы ты его писал, работая над энтерпрайз проектом.

Представим, что у ты учишься в университете на программиста, и к тебе постоянно обращаются люди с учебного потока, которые ничего не понимают в алгоритмах, с просьбой помочь им с решением за деньги. В один прекрасный день тебе пришла в голову идея, что надо создать приложение, которое делало бы за тебя всю работу, а тебе оставалось только собирать деньги с обратившихся к тебе людей.

## Задача

Реализовать сервис, который предоставляет следующий функционал:

1. Создание нового студента, используя его ФИО, номер группы, а также email, например, Штирлиц Иван Васильевич ИП-394 vasya@mail.ru. Для удобства дальнейших запросов, каждому пользователю можно присваивать логин, который будет в роли ярлыка для этого студента.
2. Изменение долга студента (уменьшение и увеличение). Максимальный долг 1000 рублей. При достижении максимального долга, приложение не должно давать ответы на новые запросы решения алгоритмических задач.
3. Получение ответа на алгоритмическую задачу. У каждой задачи есть своя стоимость для получения ответа, поэтому необходимо изменять долг студента, для которого надо получить ответ (не забудь про максимальный долг).

**Единственная алгоритмическая задача, на которую можно получить ответ и надо реализовать:**

```
Дан неотсортированный массив из N чисел от 1 до N,
при этом несколько чисел из диапазона [1, N] пропущено, 
а некоторые присутствуют дважды.

Найти все пропущенные числа.
```

## Пути разработки сервиса

Сервис можно реализовать одним из следующих путей:

1. REST API.
2. CLI-утилита.

Выбранный путь необходимо отметить в README файле.

## Требования к сервису

1. Язык Golang. Можно использовать любые фреймворки и библиотеки.
2. В качестве БД использовать PostgreSQL.
3. Весь код должен быть выложен на Github или Gitlab с README файлом, в котором содержится инструкция по запуску и примерами запросов/ответов.

При возникновении вопросов по ТЗ оставляем принятие решения за кандидатом (в таком случае в README файле к проекту должен быть указан список вопросов с которыми кандидат столкнулся и каким образом он их решил).

Разработка интерфейса в браузере НЕ ТРЕБУЕТСЯ. Для тестирования можно использовать любой удобный инструмент. Например: в терминале через curl или Postman.

Систему авторизации и аутентификации реализовывать НЕ ТРЕБУЕТСЯ. Предполагается, что проект будет использоваться на личном компьютере.

## Будет плюсом

Если ты дополнительно сделаешь что-то из этого списка, то ты заметно выделишься среди других кандидатов!

1. Покрытие кода тестами.
2. Отправка email на почту студента, в котором будет содержаться ответ на задачу или уведомление о том, что у этого студента превышен долг.
3. Использование docker и docker-compose для поднятия и развертывания рабочей среды.
4. Примитивное CI/CD (достаточно только сборки и авто-тестов).
5. Makefile.
