## Работа с git и bash
В рамках данного раздела я выполнил следующие задания по написанию базовых команд bash:

### Задание 1:
| Задача | Решение |
|--------|----------|
Открыть домашнюю директорию через терминал|cd /c/Users/Elijah/Desktop/bash_training
Определить имя папки, в которой вы находитесь|pwd
Создать внутри этой папки каталог с именем test1|mkdir test1
Перейти в папку test1|cd test1
Создать файл 1,2 и 3 внутри каталога test1|touch 1 2 3
Проверить содержимое каталога test1|ls
Перейти в домашнюю директорию|cd ..
Создать папку test2 внутри домашней директории|mkdir test2
Удалить папку test2|rmdir test2
Удалить файл 2 из папки test1|rm test1/2
Создать папку в домашней директории test3 и добавить в нее два файла|mkdir test3; touch test3/11 test3/22
Удалить папку test3|rm -r test3
Создать папку test4 в домашней директории|mkdir test4
Переместить файлы 1 и 3 из папки test1 в папку test4|mv test1/1 test1/3 test4
Добавить в файл 1 три строки со словами line|echo line > test4/1; echo line>> test4/1; echo line>> test4/1
Посмотреть содержимое файла 1|cat test4/1
Добавьте в файл 3 три строки со словами line|echo -e "line\nline\nline" >> test4/3
Просмотрите содержимое двух файлов (1 и 3) сразу|cat test4/1 test4/3
Используя один из редакторов замените все строки в файле 1|nano test4/1 (без редактора: echo -e "text\ntext\ntext" > test4/1)

### Задание 2:
| Задача | Решение |
|--------|----------|
Зайти в домашнюю директорию через терминал|cd /c/Users/Elijah/Desktop/bash_training
Создать папку test 3|mkdir test3
Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4|echo -e "row1\nrow2\nrow3\nrow4" > test3/4; echo -e "row1\nrow2\nrow3\nrow4" > test3/5; echo -e "row1\nrow2\nrow3\nrow4" > test3/6
Найдите строку row2 в файле 5|grep "row2" test3/5
Найдите строку row в папке test3|grep "row" test3/*
Посчитайте сколько строк с содержимым row в файле 6|grep -c "row" test3/6
Найдите файл 5 внутри папки test3|find test3 -name "5"
Используя команду find, удалите файл 5|find test3 -name "5" -delete
Используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого)|echo "test" > test3/4
Замените слово test в файле 4 на fail|echo "fail" > test3/4
Добавьте в файл 4 слово test так, чтобы сохранилось содержимое|echo "test" >> test3/4
Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе|ps aux
Убейте процесс 666 в консоли (можно не убивать, а просто написать команду)|kill 666
Узнайте доступность ресурса rusau.net, используя ping|ping rusau.net
Отправьте 5 пакетов на сайт rusau.net|ping -n 5 rusau.net
Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/|curl https://petstore.swagger.io/v2/pet/findByStatus?status=available&status=pending&status=sold
Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/|curl -X POST https://petstore.swagger.io/v2/user -H "Content-Type: application/json" -d "{\"id\": 999009, \"username\": \"user_name999\", \"firstName\": \"John\", \"lastName\": \"Doe\", \"email\": \"exampl@exampl.com\", \"password\": \"secret123\", \"phone\": \"+79011234767\", \"userStatus\": 1}"
