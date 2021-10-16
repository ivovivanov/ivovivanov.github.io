
# Цикли

В Python има два вградени цикъла:

 - `while`
 - `for`

## While цикъл

While изпълнява своя suite (блок от код) докато условието му е вярно.

```python
i = 0 
while i < 10:  
	print(i)  
	i += 1
```

### Break statement

`break` прекъсва изпълнието на цикъла, дори и условието на цикъла да продължава да бъде вярно.

```python
i = 0 
while i < 10:
	if i==5:
		break
	print(i)  
	i += 1
```

### Continue statement

`continue` прекъсва изпълнието на текущата итерация и продължава със следващата.

```python
i = 0 
while i < 10:
	i += 1
	if i==5:
		continue
	print(i)
```

### Else statement

Благодарение на `else` можем да изпълним suite(блок от код), когато условието на цикъла вече не е вярно и не сме прекъснали принудително изпълнението на цикъла, напр. с `break`.

```python
i = 0 
while i < 10:  
	print(i)  
	i += 1
else:
	print('while condition is no longer true')
```

## For цикъл

Цикълът `for` се използва за итерация на iterables (това е напр. `list`, `dictionary`, `set` и др.).

Чрез `for` цикъла for можем да изпълним набор от *statements*, за всеки елемент от iterable (това е напр. `list`, `dictionary`, `set` и др.).

`continue`, `break` и `else`  имат същото приложение при `for` цъкъла както при `while`.

### Итерация върху стринг

=== "Python" 

```python
for letter in 'abcde':  
	print(letter)
``` 
	
=== "Output"

```
a
b
c
d
e
```

### range() функция

Функцията `range()` връща поредица от числа, започвайки от 0 по подразбиране и увеличавайки с 1 (по подразбиране), и спира преди определено от задължителния аргумент число.


=== "Python" 

```python
for i in range(5):  
	print(i)
``` 
	
=== "Output"

```
0
1
2
3
4
```
##### range() с използване на `start` аргумент

=== "Python" 

```python
for i in range(3, 5):  
	print(i)
``` 
	
=== "Output"

```
3
4
```
##### range() с използване на `start` и `step` аргументи

=== "Python" 

```python
for i in range(2, 5, 2):  
	print(i)
``` 
	
=== "Output"

```
2
4
```
## Вграждане на цикли (Nested loops)

Вграждането на цикли означава 'поставянето' на един цикъл в тялото(suite) на друг цикъл. Така на всяка итерация на външния цикъл се изпълняват пълен набор от итерации на вътрепния цикъл.

=== "Python" 

```python
gender = ['boy', 'girl']
city = ['New York', 'Sofia', 'London']
for g in gender: 
	for c in city: 
		print(f'I am a {g} and I live in {c}!')
``` 
	
=== "Output"

```
I am a boy and I live in New York!
I am a boy and I live in Sofia!
I am a boy and I live in London!
I am a girl and I live in New York!
I am a girl and I live in Sofia!
I am a girl and I live in London!
```
