Вместо написания **множества** `if..else` операторов можно использовать `match`оператор.

Данная `match`инструкция выбирает один из множества блоков кода для выполнения.

match _expression_:  
  case x:  
    code block  
  case y:  
    code block  
  case z:  
    code block
    
 Вот как это работает:
- Выражение `match`вычисляется один раз.
- Значение выражения сравнивается со значениями каждого из `case`.
- Если найдено совпадение, выполняется соответствующий блок кода.

day = 4  
match day:  
  case 1:  
    print("Monday")  
  case 2:  
    print("Tuesday")  
  case 3:  
    print("Wednesday")  
  case 4:  
    print("Thursday")  
  case 5:  
    print("Friday")  
  case 6:  
    print("Saturday")  
  case 7:  
    print("Sunday")

Используйте символ подчеркивания _ в качестве последнего значения регистра, если хотите, чтобы блок кода выполнялся, когда других совпадений нет: