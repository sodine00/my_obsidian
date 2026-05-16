# Python PIP

---

## Что такое PIP?

PIP — это менеджер пакетов для Python, или, если хотите, модулей.

**Примечание:** Если у вас установлена ​​версия Python 3.4 или более поздняя, ​​PIP включен по умолчанию.

---

## Что такое пакет?

Пакет содержит все файлы, необходимые для работы модуля.

Модули — это библиотеки кода Python, которые вы можете включить в свой проект.

---

## Проверьте, установлен ли PIP.

Перейдите в командную строку в каталог, где находится каталог скриптов Python, и введите следующее:

### Пример

Проверить версию PIP:

C:\Users\_Your Name_\AppData\Local\Programs\Python\Python36-32\Scripts>pip --version

---

## Установите PIP

Если у вас не установлен PIP, вы можете скачать и установить его с этой страницы: [https://pypi.org/project/pip/](https://pypi.org/project/pip/)

---

## Скачать пакет

Скачивание пакета очень просто.

Откройте интерфейс командной строки и укажите PIP загрузить нужный вам пакет.

Перейдите в командную строку в каталог, где находится каталог скриптов Python, и введите следующее:

### Пример

Загрузите пакет с именем "camelcase":

C:\Users\_Your Name_\AppData\Local\Programs\Python\Python36-32\Scripts>pip install camelcase

Теперь вы скачали и установили свой первый пакет!

---

---

## Использование пакета

После установки пакет готов к использованию.

Импортируйте пакет "camelcase" в свой проект.

### Пример

Импортируйте и используйте "camelcase":

import camelcase  
  
c = camelcase.CamelCase()  
  
txt = "hello world"  
  
print(c.hump(txt))

---

## Найти пакеты

Больше пакетов можно найти по адресу [https://pypi.org/](https://pypi.org/) .

---

## Удалить упаковку

`uninstall`Для удаления пакета используйте следующую команду:

### Пример

Удалите пакет с именем "camelcase":

C:\Users\_Your Name_\AppData\Local\Programs\Python\Python36-32\Scripts>pip uninstall camelcase

Менеджер пакетов PIP запросит подтверждение удаления пакета в формате camelcase:

Uninstalling camelcase-02.1:  
  Would remove:  
    c:\users\_Your Name_\appdata\local\programs\python\python36-32\lib\site-packages\camelcase-0.2-py3.6.egg-info  
    c:\users\_Your Name_\appdata\local\programs\python\python36-32\lib\site-packages\camelcase\*  
Proceed (y/n)?

Нажмите `y`, и упаковка будет удалена.

---

## Список пакетов

Используйте эту `list`команду, чтобы вывести список всех пакетов, установленных в вашей системе:

### Пример

Список установленных пакетов:

C:\Users\_Your Name_\AppData\Local\Programs\Python\Python36-32\Scripts>pip list

Результат:

Package         Version  
-----------------------  
camelcase       0.2  
mysql-connector 2.1.6  
pip             18.1  
pymongo         3.6.1  
setuptools      39.0.1