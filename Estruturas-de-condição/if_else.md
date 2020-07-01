## Estruturas de condição com o IF/ELSE


- Imagina a seguinte situação:
    - Temos que atravessar de um lado para outro na rua, precisamos montar uma estrutura de condição em nossa cabeça, para decidir se vamos atravessar ou não, sendo essas condições:

    ```
        Se vier carro:
            Eu espero
        Senão:
            Eu atravesso
    ```

    - Pode parecer besteira, mas uma estrutura de condição simples é, basicamente, isso. Vamos ver outro exemplo:

    ```
        Imagina que estamos calculando se um aluno passou de ano na escola, conforme as notas obtidas nas provas.

        Foram três provas, com as notas:

        Prova 1 => 7.0
        Prova 2 => 6.0
        Prova 3 => 5.0

        A média é 6.0, se somarmos as três notas e dividirmos pela mesma quantidade, teremos:

        (7.0 + 6.0 + 5.0) / 3 = 6.0

        Dessa forma o sistema irá decidir se ele passou de ano na escola, a estrutura de condição ficaria dessa forma:

        Se a nota > 6.0:
            APROVADO
        Senão:
            REPROVADO
    ```
- Agora que ja viu como é na lógico, vamos ver no codigo como funcionaria uma estrutura de if/else. Digamos que, uma pessoa abaixo dos 50 anos seja jovem senão, será considerada idosa. Coloquemos isso em codigo:

```python

    idade = 18
    if idade < 50:
        print('Você é jovem!')
    else:
        print('Você é idoso(a)!')

Na linguagem Python, a indentação (espaço dado antes de uma linha) é utilizada para demarcar os blocos de código, e são obrigatórios quando se usa estruturas de controle.

```

- Também é possível checar mais de uma condição com o __elif__. É a abreviatura para else __if__. Ou seja, se o __if__ for falso, testa outra condição antes do __else__:

```python
In[]:

    idade = 18
    if idade < 50:
        print('Você é jovem!')
    elif idade > 50:
        print('Você é velho(a)!')
    else:
        print('idade inválida!')
```
```python
Out[]:

    Você é jovem!
```

Outro exemplo, mais extenso:

```python
In[]:

    valor_entrada = 10
    if valor_entrada == 1:
        print("a entrada era 1")
    elif valor_entrada == 2:
        print("a entrada era 2")
    elif valor_entrada == 3:
        print("a entrada era 3")
    elif valor_entrada == 4:
        print("a entrada era 4")
    else:
        print("o valor de entrada não era esperado em nenhum if")
```

```python
Out[]:

    o valor de entrada não era esperado em nenhum if
```

- Note que quando uma condição for verdadeira, aquele bloco de código é executado e as demais condições (__elif__ e __else__) são puladas:

```python
In[]:

    a = 1
    if a == 1:
        print("é 1")
    elif a >= 1:
        print("é maior ou igual a 1")
    else:
        print("é qualquer outra coisa")
        
```

```python
Out[]:

    é 1
```


## É bom saber...

- Para condições muito extensas o correto é usar outro tipo de estrutura codigo, sendo elas, while/for. Veja isso, nos outros conteudos desse capitulo.