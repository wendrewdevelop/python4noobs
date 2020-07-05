## Python While Loops

- Python contém dois tipos primitivos de loops:

```
    - while loops;
    - for loops.
```

## While

- Com o loop __while__, podemos executar um conjunto de instruções desde que uma condição seja verdadeira:

```python
In[]:

    i = 1
    while i < 6:
        print(i)
        i += 1

```
```python
Out[]:

    1
    2
    3
    4
    5

```

__Observação__: *lembre-se de incrementar i, caso contrário, o loop continuará para sempre.*

## Break

Com a instrução __break__, podemos parar o loop mesmo se a condição while for verdadeira:

```python
In[]:

    i = 1
    while i < 6:
        print(i)
        if i == 3:
            break
        i += 1

```
```python
Out[]:

    1
    2
    3

```

## Continue

Com a instrução __continue__, podemos parar a iteração atual e continuar com a próxima:

```python
In[]:

    i = 0
    while i < 6:
        i += 1
        if i == 3:
            continue
        print(i)

```
```python
Out[]:

    1
    2
    4
    5
    6

    # Observe que o número 3 está ausente no resultado

```

## Else

Com a instrução __else__, podemos executar um bloco de código uma vez, quando a condição não for mais verdadeira:

```python
In[]:

    i = 1
    while i < 6:
        print(i)
        i += 1
    else:
        print("i não é menor que 6")

```

```python
Out[]:

    1
    2
    3
    4
    5
    i não é menor que 6

```