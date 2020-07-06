## Declaração global

- Variáveis ​​criadas fora de uma função são conhecidas como variáveis ​​globais;
- Variáveis ​​globais podem ser usadas por todos, dentro e fora das funções.

```python
In[]:

    x = "4noobs"

    def myfunc():
        print("Python" + x)

    myfunc()

```
```python
Out[]:

    Python4noobs
```

- Se você criar uma variável com o mesmo nome dentro de uma função, essa variável será local e só poderá ser usada dentro da função. A variável global com o mesmo nome permanecerá como era, global e com o valor original.

```python
In[]:

    x = "4noobs"

    def myfunc():
    x = "He4rt"
    print(x + " developers")

    myfunc()

    print("Python" + x)


```
```python
Out[]:

    He4rt developers
    Python4noobs  
```

## Palavra-chave global

- como dito anteriormente, quando você cria uma variável dentro de uma função, essa variável é local e só pode ser usada dentro dessa função;

- Para criar uma variável global dentro de uma função, você pode usar a palavra-chave __global__.

Se você usar a palavra-chave __global__, a variável pertencerá ao escopo global:

```python
In[]:

    def string_func():
        global x
        x = "fantastico"

    string_func()
    print("Python é " + x)

```
```python
Out[]:

    Python é fantastico
```

- Além disso, use a palavra-chave __global__ se desejar alterar uma variável global dentro de uma função:


```python
In[]:

    x = "divertido"

    def string_func():
        global x
        x = "fantastico"

    string_func()
    print("Python é " + x)

```
```python
Out[]:

    Python é fantastico
```