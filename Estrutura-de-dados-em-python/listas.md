# Listas
## Definição
O interpretador <b>python</b> reconhece como uma lista, uma sequência de objetos que estejam envolvidas por [ ] (conchetes) e separadas por vírgulas.

Assim, como as Strings, as listas também tem índices.

|"python"|"php"|
|--------|-----|
|    0   |  1  |
|   -2   | -1  | 


## Exemplos

<code>
    
    #Estas duas listas são simples, e então denominadas de vetores.
    lista1 = ["python","php"]
    lista2 = [312.5,22 + 4j]

    #Esta lista é composta, e então considerada uma matriz.
    lista3 = [["c#","go lang"],[40,-8.980]]

</code> 

## Acessando os dados de uma lista 

<code>

    #Buscando na lista1 a palavra python
    print(lista1[0])
    print(lista1[-2])

    #Buscando na lista2 o número complexo
    print(lista2[1])
    print(lista2[-1])

</code>
Saída
<code>

    python
    python
    (22+4j)
    (22+4j)    
</code>

Agora, vamos buscar na matriz

<code>

    #Buscando na lista3 a palavra go lang
    print(lista3[0][1])

    #Buscando o número inteiro positivo
    print(lista3[1][0])

</code>
Saída
<code>

    go lang
    40
</code>

## Comprimento de uma lista

<p>Para verificar o comprimento de uma lista usaremos o método <b>len.</b></p>

<code>

    print(len(lista1))
    print(len(lista2))
    #Número de linhas
    print(len(lista3))
    #Número de colunas
    print(len(lista3[0]))
    print(len(lista3[1]))
</code>

<code>

    2
    2
    2
    2
    2

</code>

## Valores 

<code>
    
    #Valor máximo da lista3 coluna 1
    print(max(lista3[1]))

    #Valor mínimo da lista3 coluna 1
    print(min(lista3[1]))

    #soma da lista3 coluna 1
    print(sum(lista3[1]))

</code>
Saída

<code>

    40
    -8.98
    31.02

</code>


## Métodos 

<ul>
    <li><b>Append:</b> Usamos ele para acrescentar um novo dado a lista</li>
    <li><b>Insert:</b> Usamos ele para acrescentar um novo dado a lista, de acordo com o índice.</li>
    <li><b>Remove:</b> Remover um dado de acordo com índice.</li>
    <li><b>Sort:</b> Ordena a lista.</li>
    <li><b>Reserve:</b> Inverte a posição dos itens</li>
    <li><b>Count:</b> Número de vezes que um dado aparece na lista</li>

</ul>
<br>

### Como fica na prática

<code>

    lista1.append("java")
    print(lista1)
</code>
Saída
<code>
    
    ['python', 'php', 'java']
</code>
<br>
<code>

    lista1.insert(1,"c")
    print(lista1)

</code>
Saída
<code>

    ['python', 'c', 'php', 'java']
</code>
<br>
<code>

    lista1.remove("php")
    print(lista1)
</code>
Saída
<code>

    ['python', 'c', 'java']
</code>
<br>

<code>

    #Vamos,criar uma nova lista e adicionar diretamente agora, para testar o sort e reverse.

    lista_nova = [99,-9,6.7,86,10.6]
    lista_nova.sort()
    print(lista_nova)
</code>
Saída
<code>

    [-9, 6.7, 10.6, 86, 99]
</code>
<br>
<code>

    lista_nova.reverse()
    print(lista_nova)
</code>
Saída
<code>

    [10.6, 86, 6.7, -9, 99]
</code>
<br>
<code>
    
    #Vamos, criar nossas últimas listas para usar o método count

    ultima_lista1 = [0,11,2,"python","python"]
    ultima_lista2 = [11,22,45]

    print(ultima_lista1.count("python"))
    print(ultima_lista2.count("python")) 
</code>
Saída
<code>

    2
    0
</code>

## Finalizando
Você agora possui conhecimento sobre como funcionam as listas, em<b> python</b>. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>