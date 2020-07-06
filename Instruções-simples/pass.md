## Declaração pass

- Essa declaração é usada quando uma instrução é requerida sintaticamente, mas você não deseja que nenhum comando ou código seja executado;
- A declaração __pass__ é uma operação *null*, nada acontece quando ela é usada.

## Exemplo

```python
In[]:

    for letra in 'Python': 
        if letra == 'h':
            pass
            print 'Esse é um bloco usando a declaração pass'
        print 'Letra atual :', letra
    print "aaaaadeus!"

```
```python
Out[]:

    Letra atual : P
    Letra atual : y
    Letra atual : t
    Esse é um bloco usando a declaração pass
    Letra atual : h
    Letra atual : o
    Letra atual : n
    aaaaadeus!

```