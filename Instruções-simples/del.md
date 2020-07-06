## Keyword del

- A palavra-chave __del__ é usada para excluir objetos. No Python, tudo é um objeto. Portanto, a palavra-chave __del__ também pode ser usada para excluir *variáveis*, *listas* ou *partes de uma lista*, etc.

## Exemplos

- Podemos excluir uma classe, por exemplo:

```python
In[]:

    class Name:
        name = "Drxw"

    del Name
    print(Name)

```
```python
Out[]:

    Traceback (most recent call last):
    File "keyword_del.py", line 6, in <modulegt>
        print(Name)
    NameError: name 'Name' is not defined
```

- Podemos usar o __del__ para remover uma variavel:

```python
In[]:

    x = "he4rt developers"

    del x
    print(x)

```
```python
Out[]:

    Traceback (most recent call last):
    File "keyword_del2.py", line 5, in <modulegt>
        print(x)
    NameError: name 'x' is not defined
```

- Também podemos remover um item de uma lista, como no exemplo a seguir:

```python
In[]:

    x = ["Coca-cola", "Fanta uva", "Pepsi"]

    del x[0]
    print(x)


```
```python
Out[]:

    ["Fanta uva", "Pepsi"]
```