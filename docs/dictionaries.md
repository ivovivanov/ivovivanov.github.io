# Речници (Dictionaries)

Речниците(dictioaries or dicts) са един от четирите вида вградени структури от данни в Python. Те представляват последователност от т.нар key-value pairs (двойки с ключ и стойност). Тези двойно могат да бъдат 0(празен dict), 1, 2 или повече.

Спрямо своите елементи dicts позволяват:

-  добавяне
-  промяна
-  изтриване

## Достъп до елементите на dict  

Достъп до стойност с даден ключ: директно и чрез `get()` метод.

=== "Python"
    ```python
    vegetable = {
    "type": "apple",
    "color": "red",
    "weight": 0.138
    }
    col = vegetable["color"]
    print(col)
    w = vegetable.get('weight')
    print(w)
    ```
=== "Output"
    ```
    red
    0.138
    ```


## Основни действия върху dict

### Добавяне на двойка

Добавяне в dict става с метода директно или чрез метода `update()`:

=== "Python"
    ```python
    vegetable = {
    "type": "apple",
    "color": "red",
    "weight": 0.138
    }
    vegetable['taste'] = 'sweet'
    vegetable.update({'country_of_origin':'Bulgaria'})
    print(vegetable)
    ```
=== "Output"
    ```
    {'type': 'apple', 'color': 'red', 'weight': 0.138, 'taste': 'sweet', 'country_of_origin': 'Bulgaria'}
    ```


### Премахване на двойка

Премахване на двойка става с `del`, метода `pop()`(премахва двойка с даден ключ) и `popitem()`(премахва последната двойка в Python >v3.7)

=== "Python"
    ```python
    vegetable = {
    "type": "apple",
    "color": "red",
    "taste": "sweet",
    "weight": 0.138
    }
    del vegetable["taste"]
    vegetable.pop("color")
    vegetable.popitem()
    print(vegetable)
    ```
=== "Output"
    ```
    {'type': 'apple'}
    ``` 

### Промяна на двойка

Промяната на стойност може да стане чрез директен достъп по ключ или чрез update() метода. Промяна на ключ значи на практика вмъкване на нова двойка.

## Други методи за действия върху dicts

 - `copy()` копира съдържанието на един речник в друг. Не може да се копира чрез `dict2 = dict1`, защото така се създава референция.
 - `clear()` нулира dict, т.е. изтрива съдържанието му
 - `items()` връща всички двойки
 - `keys()` връща всички ключове
 - `values()` връща всички стойности
 - `fromkeys()` създава dict от подаден iterable за ключове и по избор втори за стойности
