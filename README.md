# DnD5E
======
"DnD5E - проект" предназначен для помощи по игре в системе Dungeon and Dragons (Версии: 5e) 
Доступны возможности: создания, кастомизации персонажей, 
получения информации по заклинаниям, регистрация пользователей. 
Проект написан на фреймворке Django.
 
### Установка:
______
1. Создайте виртуальное окружение и активируйте его
2. Установите необходимые зависимости:


    pip install -r requirements.txt

### Список файлов:
______
* **requirements.txt** - список требуемых библиотек для работы со скриптом pdf_to_html
* **ksardas/classes_for_spells.py** - Программа парсит файл '**data/char_spells.html**' полученный скриптом pdf_to_html.py
и заносит соответствие классов к заклинаниям в БД SQLite
* **ksardas/settings.py** - Программа с настройками проекта

* **data/spells.html** - Страницы заклинаний из книги игрока
* **data/char_spells.html** - Список доступных заклинаний для каждого класса персонажа


### Настройка
______


### Занесение заклинаний в БД:
______

    shell:./ksardas/$ ./mange.py import_html_spells data/spells.html
    
### Добавление соответствий классов персонажа к заклинаниям:
______
Укажите путь до директории с приложением:
```python
    KSA_PATH = '/%Full_Path_To_Project_Dir%/ksardas/'
```

Выполните:


    shell:./ksardas/ksardas$ ./classes_for_spells.py ../data/char_spells.html
    
