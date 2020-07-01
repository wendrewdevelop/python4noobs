## Escrevendo informações em um arquivo

<p>
    Neste tópico, veremos como escrever dados e salvar em arquivo utilizando o Python.
</p>
<hr>

- Para isso, a linguagem fornece dois métodos. O primeiro é o método __write()__ que recebe uma string como parâmetro e a insere no arquivo:

```python
    arquivo = open("ola_mundo.txt", "a")
    arquivo.write("Olá, mundo!")
```

Com a execução das linhas acima o python criará o arquivo, caso não exista e irá inserir o texto *"Olá, mundo!"*.

<hr>

- O segundo método é o __writelines()__, onde pode ser usado um objeto iteravel (lista, tupla, dicionario, etc...). Dessa forma, varias linhas podem ser inseridas de uma unica vez no arquivo, diferente do método __write()__, que insere uma string por vez apenas.


```python
In[]:
    arquivo = open("texto.txt", "a")

    frases = list()
    frases.append("Python \n")
    frases.append("4 \n")
    frases.append("Noobs \n")
    frases.append("He4rt Developers \n")

    arquivo.writelines(frases)  
```

- A __lista__ é um objeto iterável, então podemos passa-la como parâmetro do método __writelines()__. Utilizamos, também, o *\n* para saltar a linha ao escrevê-la no arquivo. Com isso, o resultado será o seguinte:

```python
Out[]:
```

<p align="center">
    <img src="assets/writelines.png" width="300px" alt="writelines">
</p>
