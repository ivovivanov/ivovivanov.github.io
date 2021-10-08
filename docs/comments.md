
# Коментари

Комнетарите са способ в програмните езици, който позволява отделни редове или части от редове, да не бъдат вземани в предвид като програмен код. Това позволя:

- да бъде пояснен част от кода
- сорс кода да бъде направен по лесно четим
- да се предотвратят грешки при тестване на код
- в Python да се тества сорс код
- за генериране на документация

Коментарите в Python могат да бъдат едноредови и многоредови.

## Едноредови коментари
Това са коментари, които представляват целият текст до края на реда след срещнат символ `#`.
```python
# This is a single line comment
print('Hello World!')
```
```python
print('Hello World!') # This is a single line comment
```
```python
# This is a single line comment
# And this is also a single line comment
print('Hello World!')
# And this as well
```
## Многоредови коментари
Това са коментари, които представляват целият текст ограден от двете страни с три единични (`'''`) или три двойни  (`"""`)  кавички.
```python
'''This is a multiline comment
with single quotes
'''
print('Hello World!')
```
```python
print('Hello World!')"""This is a multiline comment
with doube 
quotes
"""
print('Hello World again!')
```
