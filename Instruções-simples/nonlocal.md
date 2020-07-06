## Nonlocal

- A palavra-chave __nonlocal__ é usada para trabalhar com variáveis ​​dentro de funções aninhadas, nas quais a variável não deve pertencer à função interna.


```python
In[]:

    def nonlocal_string():
        x = "Drxw"
        def nonlocal_string2():
            x = "hello"
        nonlocal_string2() 
        return x

    print(nonlocal_string())

```
```Python
Out[]:

    Drxw
```

- Agora criamos uma função dentro de uma função, que use a variável *x* como uma variável __nonlocal__:

```python
In[]:

    def nonlocal_string():
        x = "Drxw"
        def nonlocal_string2():
            nonlocal x
            x = "hello"
        nonlocal_string2() 
        return x

    print(nonlocal_string())

```
```Python
Out[]:

    hello
```