# Стрингове

## Основна информация
Стринговете най-общо представляват текст. Стринговите литерали са текст обграден от:
- единични кавички
  ```python
  string1 = 'This is a single line string!'
  ```
- двойни кавички
  ```python
  string1 = "This is a single line string!"
  ```
- три единични кавички (многоредов стринг)
  ```python
  string1 = '''This is a 
  multi line string!'''
  ```
- три двойни кавички (многоредов стринг)
  ```python
  string1 = """This is a 
  multi line string!"""
  ```

## Slicing (Разрязване)

Този подход позволява връщане на желана част от даден стринг. Общият синтаксис е [*отстояние от началото*:*отстояние от края*]

```python
# Sample python string
st = "qwerty123456"

# Characters from position 2 to position 5 (not included):
print(st[2:5])

# Characters from the start to position 4 (not included):
print(st[:4])

# Characters from position 3 to the end:
print(st[3:])

# Characters: From: "t" (position -8) to, but not included: "5" (position -2):
print(st[-8:-2])
```

## Concatenation (Долепване) на стрингове

Извършва се чрез оператора `+`.

```python
# Sample python strings
st1 = "qwerty"
st2 = "123456"
# Concat st1 and st2
print(st1+st2)
```

## Форматиране на стрингове

Методът `format()` взима подадените му аргументи и ги поставя на местата (placeholder) оградени от `{}`.

### Неномерирани placeholders

```python
name = "Ivo"
nationality = "bulgarian"
output = "My name is {} and I am {}.".format(name, nationality)
print(output)
```

### Номерирани placeholders

```python
name = "Ivo"
city = "Sofia"
nationality = "bulgarian"
output = "My name is {0} and I am {2}, living in {1}."
print(output.format(name, city, nationality))
```

## Форматирани стрингове

Форматираните стрингове или т.нар. f-strings имат същата роля като `format()` метода, но работят по-оптимизирано. Те са въведени в Python 3.6.

```python
name = "Ivo"
nationality = "bulgarian"
output = f"My name is {name} and I am {nationality}."
print(output)
```

## Escaping (избягване) на символи

Избягването на символи става с `\` :
- `\'`	единични кавички
- `\"`	двойни кавички
- `\\`	наклонена черта	
- `\n`	нов ред	
- `\t`	Табулация	
- др

## Методи на стринговете

Вграденият тип стринг `str` има множество методи на разположение на програмистите. Тяхното описание може да бъде намерено на: [Офиациална Python документация за str методи](https://docs.python.org/3/library/stdtypes.html#string-methods)
 
