Этот `try`блок позволяет проверить блок кода на наличие ошибок.

Этот `except`блок позволяет обработать ошибку.

Этот `else`блок позволяет выполнить код, даже если нет ошибок.

Этот `finally`блок позволяет выполнять код независимо от результата выполнения блоков try и except.

---

## Обработка исключений

При возникновении ошибки, или исключения, как мы это называем, Python обычно останавливается и генерирует сообщение об ошибке.

Эти исключения можно обработать с помощью `try`следующего оператора:

### Пример

Этот `try`блок вызовет исключение, поскольку `x`переменная не определена:

try:  
  print(x)  
except:  
  print("An exception occurred")

Поскольку блок try вызывает ошибку, будет выполнен блок except.

Без блока try программа завершится с ошибкой:

### Пример

Это утверждение вызовет ошибку, поскольку переменная `x`не определена:

print(x)

---

## Много исключений

Вы можете определить столько блоков обработки исключений, сколько хотите, например, если хотите выполнить специальный блок кода для определенного типа ошибки:

### Пример

Если блок try вызывает ошибку, выведите одно сообщение, `NameError`а при других ошибках — другое:

try:  
  print(x)  
except NameError:  
  print("Variable x is not defined")  
except:  
  print("Something else went wrong")

Дополнительные типы ошибок см. в нашем [справочнике по встроенным исключениям Python](https://www.w3schools.com/python/python_ref_exceptions.asp) 
В таблице ниже показаны встроенные исключения, которые обычно возникают в Python:

| Exception                                                                               | Description                                                                       |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| [ArithmeticError](https://www.w3schools.com/python/ref_exception_arithmeticerror.asp)   | Raised when an error occurs in numeric calculations                               |
| [AssertionError](https://www.w3schools.com/python/ref_exception_assertionerror.asp)     | Raised when an assert statement fails                                             |
| [AttributeError](https://www.w3schools.com/python/ref_exception_attributeerror.asp)     | Raised when attribute reference or assignment fails                               |
| Exception                                                                               | Base class for all exceptions                                                     |
| EOFError                                                                                | Raised when the input() method hits an "end of file" condition (EOF)              |
| FloatingPointError                                                                      | Raised when a floating point calculation fails                                    |
| GeneratorExit                                                                           | Raised when a generator is closed (with the close() method)                       |
| [ImportError](https://www.w3schools.com/python/ref_exception_importerror.asp)           | Raised when an imported module does not exist                                     |
| [IndentationError](https://www.w3schools.com/python/ref_exception_indentationerror.asp) | Raised when indentation is not correct                                            |
| [IndexError](https://www.w3schools.com/python/ref_exception_indexerror.asp)             | Raised when an index of a sequence does not exist                                 |
| [KeyError](https://www.w3schools.com/python/ref_exception_keyerror.asp)                 | Raised when a key does not exist in a dictionary                                  |
| KeyboardInterrupt                                                                       | Raised when the user presses Ctrl+c, Ctrl+z or Delete                             |
| LookupError                                                                             | Raised when errors raised cant be found                                           |
| MemoryError                                                                             | Raised when a program runs out of memory                                          |
| [NameError](https://www.w3schools.com/python/ref_exception_nameerror.asp)               | Raised when a variable does not exist                                             |
| NotImplementedError                                                                     | Raised when an abstract method requires an inherited class to override the method |
| OSError                                                                                 | Raised when a system related operation causes an error                            |
| [OverflowError](https://www.w3schools.com/python/ref_exception_overflowerror.asp)       | Raised when the result of a numeric calculation is too large                      |
| ReferenceError                                                                          | Raised when a weak reference object does not exist                                |
| RuntimeError                                                                            | Raised when an error occurs that do not belong to any specific exceptions         |
| StopIteration                                                                           | Raised when the next() method of an iterator has no further values                |
| SyntaxError                                                                             | Raised when a syntax error occurs                                                 |
| TabError                                                                                | Raised when indentation consists of tabs or spaces                                |
| SystemError                                                                             | Raised when a system error occurs                                                 |
| SystemExit                                                                              | Raised when the sys.exit() function is called                                     |
| [TypeError](https://www.w3schools.com/python/ref_exception_typeerror.asp)               | Raised when two different types are combined                                      |
| UnboundLocalError                                                                       | Raised when a local variable is referenced before assignment                      |
| UnicodeError                                                                            | Raised when a unicode problem occurs                                              |
| UnicodeEncodeError                                                                      | Raised when a unicode encoding problem occurs                                     |
| UnicodeDecodeError                                                                      | Raised when a unicode decoding problem occurs                                     |
| UnicodeTranslateError                                                                   | Raised when a unicode translation problem occurs                                  |
| [ValueError](https://www.w3schools.com/python/ref_exception_valueerror.asp)             | Raised when there is a wrong value in a specified data type                       |
| ZeroDivisionError                                                                       | Raised when the second operator in a division is zero                             |

## Еще

Вы можете использовать это `else`ключевое слово для определения блока кода, который будет выполнен, если не возникнут ошибки:

### Пример

В этом примере `try`блок не выдает никаких ошибок:

try:  
  print("Hello")  
except:  
  print("Something went wrong")  
else:  
  print("Nothing went wrong")

---

## Окончательно

Если указан этот `finally`блок, он будет выполнен независимо от того, вызовет ли блок try ошибку или нет.

### Пример

try:  
  print(x)  
except:  
  print("Something went wrong")  
finally:  
  print("The 'try except' is finished")

Это может быть полезно для закрытия объектов и очистки ресурсов:

### Пример

Попробуйте открыть и записать данные в файл, который недоступен для записи:

try:  
  f = open("demofile.txt")  
  try:  
    f.write("Lorum Ipsum")  
  except:  
    print("Something went wrong when writing to the file")  
  finally:  
    f.close()  
except:  
  print("Something went wrong when opening the file")

Программа может продолжать работу, не оставляя файловый объект открытым.

---

## Вызвать исключение

Разработчик на Python может выбрать вариант генерации исключения при возникновении определенного условия.

Для генерации (или создания) исключения используйте `[raise]

### Пример

Если значение x меньше 0, вывести сообщение об ошибке и остановить программу.

x = -1  
  
if x < 0:  
  raise Exception("Sorry, no numbers below zero")

Это `[raise]ключевое слово используется для генерации исключения.

Вы можете указать, какой тип ошибки следует выдать и какой текст вывести пользователю.

### Пример

Вызвать ошибку TypeError, если x не является целым числом:

x = "hello"  
  
if not type(x) is int:  
  raise TypeError("Only integers are allowed")