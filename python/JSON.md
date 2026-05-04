JSON — это синтаксис для хранения и обмена данными.

JSON — это текст, записанный с использованием объектной нотации JavaScript.

---

## JSON в Python

В Python есть встроенный пакет `json`, который можно использовать для работы с данными в формате JSON.

### Пример
Импортируйте модуль json:

import json

---

## Анализ JSON — преобразование из JSON в Python

Если у вас есть JSON-строка, вы можете разобрать её, используя соответствующий `json.loads()`метод.

В результате получится [[словарь]] Python .

### Пример

Преобразование из JSON в Python:

import json  
  
#' some JSON:  
x =  '{ "name":"John", "age":30, "city":"New York"}'  
  
#' parse x:  
y = json.loads(x)  
  
#' the result is a Python dictionary:  
print(y["age"])

---

## Преобразование из Python в JSON

Если у вас есть объект Python, вы можете преобразовать его в строку JSON, используя соответствующий `json.dumps()`метод.

### Пример

Преобразование из Python в JSON:

import json  
  
#' a Python object (dict):  
x = {  
  "name": "John",  
  "age": 30,  
  "city": "New York"  
}  
  
#' convert into JSON:  
y = json.dumps(x)  
  
#' the result is a JSON string:  
print(y)

---

Вы можете преобразовывать объекты Python следующих типов в строки JSON:

- дикт
- список
- кортеж
- нить
- инт
- плавать
- Истинный
- ЛОЖЬ
- Никто

### Пример

Преобразуйте объекты Python в строки JSON и выведите значения:

import json  
  
print(json.dumps({"name": "John", "age": 30}))  
print(json.dumps(["apple", "bananas"]))  
print(json.dumps(("apple", "bananas")))  
print(json.dumps("hello"))  
print(json.dumps(42))  
print(json.dumps(31.76))  
print(json.dumps(True))  
print(json.dumps(False))  
print(json.dumps(None))

---

При преобразовании из Python в JSON объекты Python преобразуются в эквивалентные объекты JSON (JavaScript):

|Python|JSON|
|---|---|
|dict|Object|
|list|Array|
|tuple|Array|
|str|String|
|int|Number|
|float|Number|
|True|true|
|False|false|
|None|null|

---

### Пример

Преобразовать объект Python, содержащий все допустимые типы данных:

import json  
  
x = {  
  "name": "John",  
  "age": 30,  
  "married": True,  
  "divorced": False,  
  "children": ("Ann","Billy"),  
  "pets": None,  
  "cars": [  
    {"model": "BMW 230", "mpg": 27.5},  
    {"model": "Ford Edge", "mpg": 24.1}  
  ]  
}  
  
print(json.dumps(x))  

---

## Отформатировать результат

В приведенном выше примере выводится JSON-строка, но она не очень легко читается, так как в ней отсутствуют отступы и переносы строк.

Данный `json.dumps()`метод имеет параметры, облегчающие чтение результата:

### Пример

Используйте этот `indent`параметр для определения количества отступов:

json.dumps(x, indent=4)  

Вы также можете задать разделители; значение по умолчанию — (", ", ": "), что означает использование запятой и пробела для разделения каждого объекта, а также двоеточия и пробела для разделения ключей и значений:

### Пример

Используйте этот `separators`параметр для изменения разделителя по умолчанию:

json.dumps(x, indent=4, separators=(". ", " = "))  

---

## Упорядочить результат

Метод `json.dumps()`имеет параметры для упорядочивания ключей в результате:

### Пример

Используйте этот `sort_keys`параметр, чтобы указать, следует ли сортировать результат или нет:

json.dumps(x, indent=4, sort_keys=True)