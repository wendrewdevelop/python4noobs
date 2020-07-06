## raise Keyword

- Essa palavra chave tem como função gerar uma exceção;
- Você pode definir que tipo de erro gerar e o texto a ser impresso para o usuário.

Vejamos um exemplo simples:

```python
In[]:

    x = 7

    if x < 8:
        raise Exception("Desculpe, digite 8 caracteres ou mais")

```
```python
Out[]:

    Exception: Desculpe, digite 8 caracteres ou mais
```

Outro exemplo que podemos usar é a verificação do tipo do dado de entrada. Digamos que o sistema só aceite numeros *inteiros*, mas foi passado uma *string*, usariamos o seguinte trecho de codigo para retornar ao usuário uma mensagem:

```python
In[]:

    x = "He4rt developers"

    if not type(x) is int:
        raise TypeError("Digite apenas numeros inteiros!")

```
```python
Out[]:

    TypeError: Digite apenas numeros inteiros!
```