# Лабораторный отчет 5

### ФИО: Нгуен Динь Нам - К3140

## Выполните лабораторную работу 5.

### Задание 1 - Автоматизация проверки формата файлов при коммите

1.  Создание скрипта для проверки файлов

- Для проверки файлов перед фиксацией я создаю Git Hook `pre-commit`.

- Проверьте разрешения на выполнение и предоставьте разрешения на выполнение файлов.
- Запишите этот скрипт в файл, чтобы проверять файлы .txt перед фиксацией

![alt text](./img/image-29.png)

![alt text](./img/image-30.png)

1. Тестирование скрипта

- создайте файл `books.txt` с содержимым:

![alt text](./img/image.png)

- Затем коммит:

![alt text](./img/image-1.png)
_Действительный файл .txt._

- Проверка недействительного файла

- Создать файл `invalid.txt` и не записывать в него ничего

- После этого закоммитить, чтобы проверить

![alt text](./img/image-2.png)

_Файл недействителен, потому что он пустой._

- Добавьте содержимое в файл для коммита

![alt text](./img/image-3.png)

![alt text](./img/image-4.png)

_Файл успешно закоммичен._

### Задание 2 - Использование Git Flow в проекте

1. Инициализируем Git Flow в репозитории: При инициализации используем стандартные имена **_веток (main, develop)_**.

![alt text](./img/image-5.png)

![alt text](./img/image-6.png)
_Автоматически переключиться на ветку develop_

2. Создаем ветку для новой функциональности

```
git flow feature start task-management
```

![alt text](./img/image-7.png)

- Используйте команду git branch для проверки

![alt text](./img/image-8.png)

3. Создать файл `task_manager.py` и записать содержимое в файл

![alt text](./img/image-9.png)

4. Делаем коммит:
   ![alt text](./img/image-10.png)

5. Завершаем фичу и сливаем ее в develop:

   ![alt text](./img/image-11.png)
   ![alt text](./img/image-12.png)

- Дать этому файлу права на выполнение.

6. После этого создайте ветку `release`:

![alt text](./img/image-13.png)

- Используйте команду `git branch` для проверки

![alt text](./img/image-14.png)

7. В ветке release создайте файл `version.txt`, запишите в файл содержимое и закоммитьте"

![alt text](./img/image-15.png)

![alt text](./img/image-16.png)

8. Завершаем релиз:

![alt text](./img/image-17.png)

9. Создаем `hotfix`:

![alt text](./img/image-18.png)

![alt text](./img/image-19.png)

10. Вносим исправления в файл `file_with_error.py`:

![alt text](./img/image-20.png)

11. Затем сделайте коммит:

![alt text](./img/image-21.png)

12. После завершения используйте команду `git flow hotfix finish hotfix-1.0.1` чтобы объединить ветки main и develop.

![alt text](./img/image-22.png)

![alt text](./img/image-24.png)

13. Отправка изменений на удаленный репозиторий

![alt text](./img/image-25.png)

![alt text](./img/image-26.png)

- И вот результат:

![alt text](./img/image-27.png)

![alt text](./img/image-28.png)
