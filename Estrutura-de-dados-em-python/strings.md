# 3.2 - String
String é uma cadeia de caracteres. Uma string **sempre** estará entre aspas simples, duplas, triplas simples ou triplas duplas.
Como nos seguintes, exemplos:

Exemplo 1:
```python
>>> 'Olá Mundo'
'Olá Mundo'
>>> "H4rtDevs o melhor grupo de devs do Brasil"
'H4rtDevs o melhor grupo de devs do Brasil'
>>> """Nossa, bem grande essa string..."""
'Nossa, bem grande essa string...'
```

Agora, vamos tirar a prova e conferir se o python reconhece estas cadeias como uma string.


## Hora do código
1. Agora você irá abrir o seu editor de código, criar um arquivo com extensão a **.py**.
2. Criar três variáveis com nomes de sua escolha.
3. Em seguida, usaremos duas funções, **print** e **type**.
    * Usaremos **type** para verificar o tipo das variáveis e o **print** para ver o que **type** nos retorna!

O seu arquivo deverá ficar assim:
```python
string1 = 'Olá mundo'
string2 = "H4rtDevs é maior grupo de devs do Brasil"
string3 = """Nossa, bem grande essa string..."""

print(type(string1))
print(type(string2))
print(type(string3))
```

## Hora de ver funcionando!
Basta executar o script para recebermos a seguinte saída.</p>
```python
<class 'str'>
<class 'str'>
<class 'str'>
```

## Conversão para String
Variáveis que inicialmente não são do tipo **string** podem ser convertidas para uma.
Vamos conferir retirando as aspas do valor da váriavel `string3`.
```
>>> string3 = "321123"
>>> string3 = 321123
>>> # Vamos agora conferir o novo tipo da variável `string3`.
>>> type(string3)
<class 'int'>
```

O novo tipo da nossa variável é **int** (integer ou inteiro), ou seja, o interpretador do python reconheceu nossa variável como um número do tipo **int**.
Mas, se quiséssemos transformar esta variável em string novamente sem usar as aspas?
Basta, usar o "método" interno **str** na nossa impressão. 
```
>>> string3 = 321123
>>> str(string3)
'321123'
```
E assim, a nossa `string3` "volta a ser" uma **string**.

## Concatenação

A concatenação é uma operação de unir duas strings.
Crie uma nova variável e atribua a ela duas strings e separe-as por um sinal de adição e veja a saída.
```python
>>> string4 = "Python" + "é legal"
>>> string4
'Pythoné legal'
```

Que tal demonstrarmos o quanto gostamos de <b>python</b>, repetindo três vezes a palavra muito na nossa saída?<br>
Use a <b>String4</b>.
</p>

<code>

    String4 = "Python é" + " muito " * 3 + " legal" 

</code>
Agora, basta rodar nosso script para recerbemos a seguinte saída.
<code>
    
    Python é muito  muito  muito   legal

</code>


## Descontruindo uma String

<p>No <b>python</b>, todas as classes/tipos que possuem ideia de
ordenação (como a classe STRING) podem ser
acessadas por partes.
</p>

|P|Y|T|H|O|N|
|-|-|-|-|-|-|
|0|1|2|3|4|5|
|-6|-5|-4|-3|-2|-1|

Crie uma nova variável do tipo <b>String</b> e atribua a ela a palavra: <b>python</b>
<code>
    
    String5 = "python"

</code>
<p>Agora, quero exibir apenas a letra p.<br>
</p>
<code>

    print(String5[0])
</code>
Ou
<code>

    print(String5[-6])
</code>
Saída
<code>

    p
    p
</code>
Agora, eu quero exibir todas as letras com exceção do <b>P</b> e <b>N</b>.
<code>

    print(String5[1:4])
</code>
saída.
<code>

    ytho
</code>
Agora, eu quero todas as letras com exceção do <b>O</b> e <b>N</b>
<code>

    print(String5[:4])
</code>
 
saída.
<code>
    
    pyth
</code>

Por fim, vamos pegar caracteres alternados
<code>
    
    print(String5[0:5:2])
</code>
Saída.
<code>

    pto
</code>


## Métodos internos
Um dos métodos internos do <b>python</b> é o len.</b><br>
O método <b>len,</b> tem como utilidade mostrar o número de caracteres de uma string. <br>
Crie uma nova variável do tipo <b>String</b>.

<code>

    String6 = "Python4Noobs"
</code>
Agora, vejamos o método len em ação.
<code>

    print(len(String6))
</code>
Saída.
<code>

    12  
</code>

<b>Count</b> é mais uma destes métodos internos.
A sua função é verificar quantas vezes determinado caractere aparece, em uma <b>String</b>.
<code>
    
    print(String6.count("o"))
</code>
saída.
<code>
    
    3
</code>
Podemos definir também de onde iniciar e onde parar.
<code>

    print(String6.count("o",3,7))
    
</code>
Saída.
<code>

    1
</code>
Entre o caractere de índice três e o de índice sete, contém apenas uma letra <b>O</b>, segundo a nossa saída.<br>
<br>
<p>
Outros, dois métodos são o <b>UPPER</b> e <b>LOWER.</b><br>
Suas funções, são respectivamente, deixar a string em caixa alta e caixa baixa.<br>
Vejamos, com nossa String5.
</p>
<code>
    
    print(String5.upper())
    print(String5.lower())
</code>
Saída.
<code>

    PYTHON
    python
</code>
<p>
Por fim, temos mais três métodos.<br>
Os métodos: Isalnum, replace e split.<br>
<b>Isalnum:</b> Retorna true se todos os caracteres forem alfanúmericos.<br>
<b>replace:</b>Retorna uma nova string
substituindo na string a todas
as ocorrências de uma string b
por uma nova string c.<br>
<b>split:</b>Separa a string a toda vez que
for encontrada uma string b.
</p>

Vejamos, estes métodos na prática.

<code>

    String7 = "melancia321"
    String8 = "melancia321*%#"
    String9 = "Brasil"

    print(String7.isalnum())
    print(String8.isalnum())
    print(String9.replace("s","z"))
    print(String9.split("as"))
</code>
Saída.
<code>

    #Isto é um comentário, ou seja, a linha não é executada pelo interpretador

    True #True, pois não há caracteres alfanúmericos na String7

    False #False, pois há caracteres alfanúmericos na String8

    Brazil #A letra s foi substituida pela letra z

    ['Br', 'il'] #Foi criado um vetor para separar entre a letra a
</code>


## Finalizando
Você agora possui conhecimento sobre oque é uma string, em<b> python</b> e como fazer manipulações com a mesma. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>
