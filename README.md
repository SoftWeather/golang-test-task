# SoftWeather. Тестовое задание в команду финтеха Golang.

## Проблема

В ходе работы зачастую приходится искать нестандартные и оптимизированные пути решения задач. Этим тестовым заданием мы хотим оценить твое умение выполнять задачу, имея неполные данные о ней, а также умение самостоятельно принимать решения и соблюдать качество кода, поэтому пиши код так, как бы ты его писал, работая над энтерпрайз проектом.

Представим, что у ты учишься в университете на программиста, и к тебе постоянно обращаются люди с учебного потока, которые ничего не понимают в алгоритмах, с просьбой помочь им с решением за деньги. В один прекрасный день тебе пришла в голову идея, что было бы неплохо создать приложение, которое делало бы за тебя всю работу, а тебе оставалось бы лишь собирать деньги с людей. Вдобавок, ты сможешь попрактиковаться с микросервисной арихектурой.

Тебе надо реализовать два микросервиса, которые будут образовывать систему платного решения алгоритмических задач.


## Задача

Реализовать два микросервиса (далее для краткости пускай будет сA и сБ).

**сА предоставляет API:**
1. Создание нового студента, используя его ФИО и номер группы, например, Штирлиц Иван Васильевич ИП-394. Для удобства дальнейших запросов, каждому пользователю можно присваивать логин, который будет в роли ярлыка для этого студента.
2. Изменение долга студента (уменьшение и увеличение). Максимальный долг 1000 рублей. При достижении максимального долга, приложение не должно давать ответы на новые запросы решения алгоритмических задач.

**сБ предоставляет API:**
1. Получение ответа на алгоритмическую задачу. У каждой задачи есть своя стоимость для получения ответа, поэтому необходимо изменять долг студента, для которого надо получить ответ (не забудь про максимальный долг).
2. Получение списка запросов на решение задач для конкретного студента, используя пагинацию. На выходе мы хотим получить ответ, который будет содержать название задачи и стоимость решения задачи.
3. Изменение стоимости получения ответа для конкретной задачи.

**Единственная алгоритмическая задача, на которую можно получить ответ и которую надо реализовать:**

```
Дан массив из n неотрицательных целых чисел, представляющий карту высот.
Ширина каждой отметки равна 1. 
Вычислите, сколько уровней может быть заполнено водой после дождя.

       #
   #---##-#
_#-##-######
Input: height = [0,1,0,2,1,0,1,3,2,1,2,1]
Ответ: 6
```

## Требования к сервисам

1. Язык Golang.
2. Можно использовать любые фреймворки и библиотеки.
3. Реляционная СУБД - PostgreSQL.
4. Использование docker и docker-compose для поднятия и развертывания рабочей среды
5. Весь код должен быть выложен на Github или Gitlab с Readme файлом, в котором содержится инструкция по запуску и примерами запросов/ответов.

При возникновении вопросов по ТЗ оставляем принятие решения за кандидатом (в таком случае в Readme файле к проекту должен быть указан список вопросов с которыми кандидат столкнулся и каким образом он их решил).

Разработка интерфейса в браузере НЕ ТРЕБУЕТСЯ. Для тестирования можно использовать любой удобный инструмент. Например: в терминале через curl или Postman.


## Будет плюсом

1. Покрытие кода тестами.
2. Swagger для вашего API.
3. Makefile.
4. Примитивное CI/CD.
5. Все API имеет единую точку входа, т.е. реализован API Gateway.
