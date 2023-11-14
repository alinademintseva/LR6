# Лабораторная работа №6. Система контроля версий.
## Цель лабораторной работы:
изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
## Ход работы:
1. Создан аккаунт на сайте GitHub.
2. Сделана копия в личное хранилище (Fork)

3. Git уже был установлен на компьютер. Программа была обновлена и проведенка проверка версии.
  ```
  git --version
  ```
  ![Рисунок 1](https://github.com/alinademintseva/LR6/blob/report/screenshots/2_version.PNG)

4. Настройка клиента git. Введено имя пользователя и email.
  ```
  git config --global user.name "4216 Деминцева А.Е."
  git config --global user.email "alinademintseva@yandex.ru"
  ```
  ![Рисунок 2](https://github.com/alinademintseva/LR6/blob/report/screenshots/3_config.PNG)

5. Клонирование удаленного репозитория на компьютер
  ```
  git clone https://github.com/alinademintseva/LR6
  ```
  ![Рисунок 3](https://github.com/alinademintseva/LR6/blob/report/screenshots/3_3.PNG)

6. Добавлен файл через интерфейс GitHub. Загружены изменения в локальный репозиторий.  

  Добавлен текстовый файл в ветку master.

  ![Рисунок 4](https://github.com/alinademintseva/LR6/blob/report/screenshots/4_add%20file.PNG)

  После клонирования переходим в локальный репозиторий и загружаем изменения.
  ```
  git pull
  ```
  ![Рисунок 5](https://github.com/alinademintseva/LR6/blob/report/screenshots/5_pull.PNG)

7. Получена история операций для веток
   
  Для ветки master:
  ```
  git log
  ```
  ![Рисунок 6](https://github.com/alinademintseva/LR6/blob/report/screenshots/6_changes_master.PNG)
  
  Для ветки branch1:  
  ```
  git log origin/branch1
  ```
  ![Рисунок 7](https://github.com/alinademintseva/LR6/blob/report/screenshots/7_changes_branch1.PNG)

8. Просмотрены последние изменения
   
  ```
  git status
  ```
  Поскольку они отсутствуют, получаем:
  
  ![Рисунок 8](https://github.com/alinademintseva/LR6/blob/report/screenshots/8_changes.PNG)

9. Выполнено слияние в ветку master, при этом разрешив конфликт слияния в текстовом файле.
    
  Проверяем, что находимся в ветке master. Выполняем слияние.
   
  ```
  git switch master
  git merge branch1
  ```

  ![Рисунок 9](https://github.com/alinademintseva/LR6/blob/report/screenshots/9_merge.PNG)

  В текстовом файле был разрешен конфликт слияния. Выполнен коммит.
  
  ```
  git add mergefile.txt
  git commit -m "Конфликт разрешен"
  ```

   ![Рисунок 10](https://github.com/alinademintseva/LR6/blob/report/screenshots/10_conflict.PNG)

10. Побочная ветка была удалена автоматически после слияния. Проверка наличия веток.

  ```
  git  branch -D branch1
  git branch
  ```
  
  ![Рисунок 11](https://github.com/alinademintseva/LR6/blob/report/screenshots/11_del%20branch1.PNG)

  Удаление ветки с GitHub:

  ```
  git push origin -d branch1
  ```
  

11. Произведены различные изменения и выполнены коммиты.

  ```
  git  add
  git commit -m "..."
  ```

  Первое изменение (Добавлен текст в уже существующий файл new_file.txt)

  ![Рисунок 12](https://github.com/alinademintseva/LR6/blob/report/screenshots/commit1.PNG)

  Второе изменение (Добавлен новый файл file1.txt)

  ![Рисунок 13](https://github.com/alinademintseva/LR6/blob/report/screenshots/commit2.PNG)

  Третье изменение (Добавлен графический файл)

  ![Рисунок 14](https://github.com/alinademintseva/LR6/blob/report/screenshots/commit3.PNG)

12. Выполнен откат коммита (в данном случае - третьего)
    
  ```
  git reset --hard HEAD~
  ```

  ![Рисунок 15](https://github.com/alinademintseva/LR6/blob/report/screenshots/del%203%20commit.PNG)

  Выполнена проверка операций:

  ![Рисунок 16](https://github.com/alinademintseva/LR6/blob/report/screenshots/operations%20after%20del%20commit3.PNG)

13. Создана ветка для отчета (report)

  ```
  git branch report
  git switch report
  ```
  ![Рисунок 17](https://github.com/alinademintseva/LR6/blob/report/screenshots/create%20branch%20report.PNG)

14. История операций в форматированном виде:

  ```
  git log --pretty=format:"%h - %ad | %an | %s" --date=short
  ```
  ![Рисунок 18](https://github.com/alinademintseva/LR6/blob/report/screenshots/short%20list.PNG)

15. Отправка изменений из локального репозитория в удаленный

  ```
  git push
  ```
16. Загрузка скриншотов в отдельную папку и оформление отчета, с использованием *markdown* синтаксиса.


## Лог команд:

  ```
  git --version
  git config --global user.name "4216 Деминцева А.Е."
  git config --global user.email "alinademintseva@yandex.ru"
  git clone https://github.com/alinademintseva/LR6
  git pull
  git log
  git log origin/branch1
  git status
  git switch master
  git merge branch1
  git add mergefile.txt
  git  branch -D branch1
  git branch
  git push origin -d branch1
  git  add
  git commit -m "..."
  git reset --hard HEAD~
  git branch report
  git switch report
  git log --pretty=format:"%h - %ad | %an | %s" --date=short
  git push
  ```

## Вывод:
В ходе лабораторной работы были изучены базовые возможности системы управления версиями, получен опыт работы с Git Api и с локальным, удаленным репозиториями.
  




    
  
  
  
    


  
    

  

  

  

    

  




