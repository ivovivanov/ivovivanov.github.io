# Синтаксис

Python не използва познатият ни от повече широко разпространени програмни езици, а именно C-like синтаксиса. Indentation се нарича способът в Python, чрез който разграничаваме и групираме отделни части от код. Тези части от кода се наричат `suits`. `Indentation-ът` е броя от space-и, които отместват всеки statement(код на един ред)
Обикновено е прието 2 или 4 space-а да се използват за `indenteation`.

## Примери:
```python
x, y = 3, 7
if x < y:
    print(x)
else:
    print(y)
```

```python
class indent_is_important():
    def __init__():
        pass
    def first_method(_self):
        pass
```
## Грешки:
```python
x, y = 3, 7
if x < y:
print(x)
```

```python
x, y = 3, 7
if x < y:
    print(x)
   print(y)
```

## Statements

- един на ред

    ```python
    #This is a single line statement
    print('This is a statement!')
    ```
- повече от един на ред


    ```python
    #This is a multi line statement
    str = 'This is a statement!' ; print(str)
    ```

## Празен suit:
```python
var = 'something'
if var:
    pass
var = 'something else'
```
