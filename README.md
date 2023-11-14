# Лабораторная работа №6. Система контроля версий.
## Цель лабораторной работы:
изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
## Ход работы:
1. Создан аккаунт на сайте GitHub.
2. Сделана копия в личное хранилище (Fork)
![Рисунок 1] (https://github.com/alinademintseva/LR6/blob/report/screenshots/1_fork.PNG)
3. Git уже был установлен на компьютер. Программа была обновлена и проведенка проверка версии.
```
git --version
```
![Рисунок 2] (https://github.com/alinademintseva/LR6/blob/report/screenshots/2_version.PNG)
4. Настройка клиента git. Введено имя пользователя и email.
```
git config --global user.name "Деминцева А.Е."
git config --global user.email "alinademintseva@yandex.ru"
```
![Рисунок 3](https://github.com/alinademintseva/LR6/blob/report/screenshots/3_config.PNG)
5. Клонирование удаленного репозитория на компьютер
```
git clone https://github.com/alinademintseva/LR6
```
![Рисунок 4](https://github.com/alinademintseva/LR6/blob/report/screenshots/3_3.PNG)
6. Добавлен файл через интерфейс GitHub. Загружены изменения в локальный репозиторий.
Добавлен текстовый файл в ветку master.
![Рисунок 5](https://github.com/alinademintseva/LR6/blob/report/screenshots/4_add%20file.PNG)

После клонирования переходим в локальный репозиторий и загружаем изменения.
```
git pull
```
![Рисунок 6](https://github.com/alinademintseva/LR6/blob/report/screenshots/5_pull.PNG)
7. Получена история операций для веток
Для ветки master:
```
git log
```
![Рисунок 7](https://github.com/alinademintseva/LR6/blob/report/screenshots/6_changes_master.PNG)
Для ветки branch1:
```
git log origin/branch1
```
![Рисунок 8](https://github.com/alinademintseva/LR6/blob/report/screenshots/7_changes_branch1.PNG)
8. Просмотрены последние изменения
Поскольку они отсутствуют, получаем:
```
git status
```
![Рисунок 9](https://github.com/alinademintseva/LR6/blob/report/screenshots/8_changes.PNG)


