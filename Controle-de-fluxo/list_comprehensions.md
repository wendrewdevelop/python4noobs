## List Comprehensions em python


- O List Comprehensions fornece uma maneira concisa de criar listas;
- O List Comprehensions sempre retorna uma lista de resultados.

Se você costumava fazer assim:

```python

    nova_lista = []
    for i in lista_antiga:
        if filter(i):
            nova_lista.append(expressions(i))
```

Você pode obter a mesma coisa usando o list comprehensions:


```python
    
    new_list = [expression(i) for i in old_list if filter(i)]
    # Observe que o método de acréscimo desapareceu
```

## Sintaxe

O list comprehension começa com colchetes *‘[‘* e fecha com colchetes *‘]’*, para ficar melhor o entendimento, vamos para um exemplo mais pratico, visualmente falando:

```python

    [ expressao for item in list if condicao ]
```

Isso é equivalente a:

```python

    for item in list:
        if condicao:
            expressao
```

Vamos analisar isso e ver o que ele faz:

```python

    nova_lista = [expression(i) for i in lista_antiga if filter(i)]
```

__nova_lista__: Lista nova que será gerada;
__for i in lista_antiga__: A palavra __for__ seguida pelo nome da variável a ser usada, seguida pela palavra lista_antiga;
__expression(i)__: A expressão é baseada na variável usada para cada elemento na lista_antiga;
__if filter(i)__: Aplique um filtro com uma instrução __if__.


## Complementando...

- List Comprehensions é um assunto complexo e mais complexo do que o apresentado acima, mas deixaremos conteudo para que veja mais sobre o tema:

<a href="https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions"> Documentação oficial - list-comprehensions</a>
<a href="https://medium.com/better-programming/list-comprehension-in-python-8895a785550b"> Medium - Indo mais além no assunto</a>
