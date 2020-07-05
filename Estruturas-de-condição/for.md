## Python "For" Loops


O loop __for__ é usado para iteragir em uma sequencia, sendo uma lista, tupla, dicionario, etc...

Podemos usar o loop __for__ para percorrer uma lista, como no exemplo abaixo:

```python
In[]:

    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        print(x)

```

```python
Out[]:

    apple
    banana
    cherry

```

- Podemos fazer com que o loop pare assim que ache uma opção desejada. Para que isso ocorra, usamos a declaração __break__:

```python
In[]:

    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        print(x) 
    if x == "banana":
        break


```

```python
Out[]:

    apple
    banana

```

- E se colocarmos o retorno do loop após do __break__:

```python
In[]:

    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            break
        print(x) 


```

obteremos o seguinte retorno:

```python
Out[]:

    apple

```

## Declaração continue

Com a declaração __continue__ podemos parar a iteração atual e ir para a proxima:

```python
In[]:
    
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            continue
        print(x)

```

```python
Out[]:

    apple
    cherry

```

## Função range()

- Para percorrer um conjunto de códigos um número especificado de vezes, podemos usar a função range().

- A função range() retorna uma sequência de números, iniciando em 0 por padrão e incrementando em 1 (por padrão), e termina em um número especificado.

```python
In[]:

    for x in range(6):
        print(x)

```

```python
Out[]:

    0
    1
    2
    3
    4
    5

```

- Como dito, por padrão a função __range()__ inicia do contador 0, mas podemos especificar o valor inicial adicionando os parâmetros iniciais e finais, da seguinte forma:

```python
In[]:

    for x in range(2, 6):
        print(x)

```

```python
Out[]:

    2
    3
    4
    5

```

- Por padrão, a função __range()__ incrementa os valores de um a um, mas podemos mudar isso adicionando um terceiro parâmetro à função:

```python
In[]:

    for x in range(2, 30, 3):
        print(x)

```

```python
Out[]:

    2
    5
    8
    11
    14
    17
    20
    23
    26
    29

```

## Keyword ELSE

- A Keyword __else__ em um loop __for__, especifica um bloco de código a ser executado quando o loop for concluído:

```python
In[]:

    for x in range(6):
        print(x)
    else:
        print("Finally finished!")

```

```python
Out[]:
    
    0
    1
    2
    3
    4
    5
    Finally finished!

```

## Loops aninhados

- Loops aninhados são loops dentro de outros;

- O "loop interno" será executado uma vez para cada iteração do "loop externo":

```python
In[]:

    adj = ["red", "big", "tasty"]
    fruits = ["apple", "banana", "cherry"]

    for x in adj:
        for y in fruits:
            print(x, y)

```

```python
Out[]:
    
    red apple
    red banana
    red cherry
    big apple
    big banana
    big cherry
    tasty apple
    tasty banana
    tasty cherry

```

## Declaração pass

- os loops __for__ não podem estar vazios, mas se, por algum motivo, você tiver um loop for sem conteúdo, insira a instrução pass para evitar erros:

```python
In[]:

    for x in [0, 1, 2]:
        pass

```

```python
Out[]:
    
    # ter um loop for vazio como esse, geraria um erro sem a instrução pass

```

## Importante saber...

É importante que saiba a diferença entre interação e iteração.

- __Iteração__: se define por um processo que se repete diversas vezes para se chegar a um resultado e a cada vez gera um resultado parcial que será usado na vez seguinte;

- __Interação__: Diferente do tópico anterior onde é preciso realizar uma ação, na interação é a ação realizada pelo usuário com determinada situação ou produto.