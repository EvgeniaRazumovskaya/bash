# 📌 bash
Здесь вы можете увидеть примеры команд bash, которые я использовала для выполнения задач во время обучения.

Предусловия для выполнения задания:

Установить git bash или VScode

Выполненное задание сохранить в виде файла txt с каждым запросом.

### Задание Bash 1


Задание 1

1.	Открыть домашнюю директорию
2.	Определить имя папки, в которой вы находитесь

pwd

3.	Создать внутри этой папки каталог  с именем test1

mkdir test1

4.	Перейти в папку test1

cd test1

5.	Создать файл 1,2 и 3 внутри каталога test1

touch file1.txt
touch file2.txt
touch file3.txt

6.	Проверить содержимое каталога test1

ls

7.	Перейти в домашнюю директорию
   
cd ..

9.	Создать папку test2 внутри домашней директории

mkdir test2

9.	Удалить папку test2

rmdir test2

10.	Удалить файл 2 из папки test1

cd test1
rm file2.txt

11.	Создать папку в домашней директории test3 и добавить в нее два файла

cd ..

mkdir test3

cd test3

touch file31.txt

touch file32.txt

12.	Удалить папку test3

cd ..

rm -rf test3

13.	Создать папку test4 в домашней директории

mkdir test4

14.	Переместить файлы 1 и 3 из папки test1 в папку test4

mv test1/file1.txt test4

mv test1/file3.txt test4

15.	Добавить в файл 1 три строки со словами line

cd test4

echo line1 > file1.txt

echo line2 >> file1.txt

echo line3 >> file1.txt

16.	Посмотреть содержимое файла 1

cat file1.txt

17.	Добавьте в файл 3 три строки со словами line

echo line11 > file3.txt

echo line22 >> file3.txt

echo line33 >> file3.txt

18.	Просмотрите содержимое двух файлов (1 и 3) сразу

cat file1.txt file3.txt

19.	Используя один из редакторов замените все строки в файле 1
    
nano file1.txt

далее в редакторе команда Replace   (нажать ctrl + \ ) ввести значение которое нужно заменить, затем новое значение, подтвердить замену Y

ctrl + x       - выйти из редактора

 ### Задание Bash 2

Задание 2

1.	Зайти в домашнюю директорию
   
3.	Создать папку test 3

mkdir test3

3.	Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4

touch file4.txt

touch file5.txt

touch file6.txt

echo row1 > file4.txt

echo row2 >> file4.txt

echo row3 >> file4.txt

echo row4 >> file4.txt

echo row1 > file5.txt

echo row2 >> file5.txt

echo row3 >> file5.txt

echo row4 >> file5.txt

echo row1 > file6.txt

echo row2 >> file6.txt

echo row3 >> file6.txt

echo row4 >> file6.txt


4.	Найдите строку row2 в файле 5

grep 'row2' / file5.txt

5.	Найдите строку row в папке test3

grep 'row' /test3 -r|--recursive

6.	Посчитайте сколько строк с содержимым row в файле 6

grep 'row' / file6.txt -c|--count

7.	Найдите файл 5 внутри папки test3

cd test3

find . -name “file5.txt”

8.	Используя команду find, удалите файл 5

find /path -name file5.txt-delete

9.	Используя команду echo, добавьте слово test в файл 4

echo test > file4.txt

10.	Замените слово test в файле 4 на fail

sed 's/test/fail/g' file4.txt


11.	Добавьте в файл 4 слово test так, чтобы сохранилось содержимое

echo test >> file4.txt

12.	Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе

ps aux – увидеть все процессы

или

top -еще больше процессов


13.	Убейте процесс 666 в консоли

kill 666

14.	Узнайте доступность ресурса artsiomrusau.com, используя ping

ping artsiomrusau.com

15.	Отправьте 5 пакетов на сайт artsiomrusau.com

ping -c 5 artsiomrusau.com

16.	Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/

curl -X GET https://petstore.swagger.io/v2/pet/{petId}

17.	Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/

curl -X POST https://petstore.swagger.io/v2/pet --data “name = Kitty” --data “status = available”
