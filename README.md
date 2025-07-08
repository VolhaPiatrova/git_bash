# Работа с git и bash  
If the project provides access to the server, a QA engineer can view logs or other artifacts on it. This requires knowledge of basic Bash commands. For this task i use the terminal in Visual Studio Code.  

## Основные команды для работы с файлами и каталогами в терминале

| №  | Команда                                                                                 | Описание                                                                                         |
|-----|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 1   | `cd`                                                                                   | Без аргументов перемещает пользователя в домашний каталог                                        |
| 2   | `pwd`                                                                                  | Выводит полный путь к текущему рабочему каталогу                                                |
| 3   | `mkdir test1`                                                                          | Создаёт папку `test1` внутри текущего каталога                                                  |
| 4   | `cd test1`                                                                            | Переходит в директорию `test1`                                                                  |
| 5   | `touch 1 2 3`                                                                         | Создаёт файлы `1`, `2` и `3` внутри папки `test1`                                              |
| 6   | `cd`                                                                                   | Возвращается в домашний каталог                                                                 |
| 7   | `mkdir test2`                                                                          | Создаёт папку `test2`                                                                           |
| 8   | `rm -r test2`                                                                         | Рекурсивно удаляет папку `test2` и всё её содержимое                                           |
| 9   | `rm test1/2`                                                                          | Удаляет файл `2` внутри папки `test1`                                                          |
| 10  | `mkdir test3`                                                                         | Создаёт папку `test3`                                                                           |
| 11  | `touch test3/file1.txt test3/file2.txt`                                              | Создаёт файлы `file1.txt` и `file2.txt` внутри папки `test3`                                   |
| 12  | `rm -r test3`                                                                         | Удаляет папку `test3` с содержимым                                                             |
| 13  | `mkdir test4`                                                                         | Создаёт папку `test4`                                                                           |
| 14  | `mv test1/1 test1/3 test4/`                                                          | Перемещает файлы `1` и `3` из папки `test1` в папку `test4`                                    |
| 15  | `echo -e "line\nline\nline" >> test4/1`                                             | Добавляет в файл `test4/1` три строки со словом `line`                                         |
| 16  | `cat test4/1`                                                                         | Выводит содержимое файла `test4/1` в терминал                                                  |
| 17  | `echo -e "line\nline\nline" >> test4/3`                                             | Добавляет в файл `test4/3` три строки со словом `line`                                         |
| 18  | `cat test4/1 test4/3`                                                                | Выводит содержимое двух файлов `test4/1` и `test4/3`                                           |
| 19  | `nano test4/1`                                                                        | Открывает файл `test4/1` для редактирования                                                    |
| 20  | `mkdir test3`                                                                         | Создаёт папку `test3`                                                                           |
| 21  | `echo -e "row1\nrow2\nrow3\nrow4" > test3/4`<br>`echo -e "row1\nrow2\nrow3\nrow4" > test3/5`<br>`echo -e "row1\nrow2\nrow3\nrow4" > test3/6` | Создаёт файлы `4`, `5`, `6` в `test3` с 4 строками в каждом                                   |
| 22  | `grep "row2" test3/5`                                                                 | Находит строку `row2` в файле `test3/5`                                                        |
| 23  | `grep "row" test3/*`                                                                  | Находит все строки, содержащие `row` во всех файлах папки `test3`                              |
| 24  | `grep -c "row" test3/6`                                                               | Подсчитывает количество строк с `row` в файле `test3/6`                                        |
| 25  | `find test3 -name 5`                                                                  | Находит файл с именем `5` в папке `test3`                                                      |
| 26  | `find test3 -name 5 -exec rm {} \;`                                                  | Находит файл `5` в `test3` и удаляет его                                                       |
| 27  | `echo test > test3/4`                                                                 | Записывает слово `test` в файл `test3/4`, заменяя содержимое                                  |
| 28  | `sed -i 's/test/fail/g' test3/4`                                                     | Заменяет слово `test` на `fail` в файле `test3/4`                                              |
| 29  | `echo test >> test3/4`                                                                | Добавляет слово `test` в конец файла `test3/4`, сохраняя содержимое                            |
| 30  | `ps aux`                                                                             | Показывает все процессы в системе                                                              |
| 31  | `kill 666`                                                                           | Завершает процесс с PID 666                                                                     |
| 32  | `ping rusau.net`                                                                     | Проверяет доступность ресурса `rusau.net`                                                      |
| 33  | `ping -c 5 rusau.net`                                                                | Отправляет 5 ping-запросов на `rusau.net`                                                     |
| 34  | `curl https://petstore.swagger.io/v2/pet/findByStatus?status=available`              | Выполняет GET-запрос к API и выводит полученные данные                                        |
| 35  | ```curl -X POST https://petstore.swagger.io/v2/pet --data "id=0" --data "category.id=0" --data "category.name=dog" --data "name=Anna" --data "photoUrls[0]=" --data "tags[0].id=" --data "tags[0].name=" --data "status=available"``` | Выполняет POST-запрос к API с передачей данных                                                 |


