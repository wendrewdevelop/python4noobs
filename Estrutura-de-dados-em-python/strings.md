# 3.2 - String
String é uma cadeia de caracteres envolvida por aspas simples ou duplas.<br>
Como nos seguintes, exemplos:<br>

Exemplo 1:<br>
'Olá Mundo'<br>
<br>
Exemplo 2:<br>
"H4rtDevs o melhor grupo de devs do Brasil"<br>
<br>
Exemplo 3:<br>
"321123"<br>

<p>Agora, vamos tirar a prova e conferir se o python reconhece estas cadeias como uma String.</p>
<hr>

## Hora do código
<p>Então, agora você abrir seu editor de código criar um arquivo <b>.py .</b><br>
Criar três variáveis com nomes a sua escolha.<br> No exemplo, eu coloquei os nomes: String1, String2 e String3.<br>
Em seguida, digitar três comandos <b>print</b> e como paramêtro usaremos o <b>método interno type</b> para saber se são realmente strings as nossas três variáveis.
</p>
Assim, ficará o seu .py
<code>

    String1 = 'Olá mundo'
    String2 = "H4rtDevs é maior grupo de devs do Brasil"
    String3 = "321123"

    print(type(String1))
    print(type(String2))
    print(type(String3))


</code>
<hr>

## Hora de vê funcionando
<p>Basta executar o script para recebermos a seguinte saída.</p>

<code>

    <class 'str'>
    <class 'str'>
    <class 'str'>

</code>
<hr>

## Conversão para String
<p>Variáveis que inicialmente não são do tipo <b>string</b> podem ser convertidas.<br>
Vamos conferir, retirando as aspas da string3<br>
</p>

<code>
    
    String3 = 321123

</code>
Vamos usar agora conferir seu novo tipo.
<code>

    <class 'int'>

</code>

<p>O novo tipo da nossa variável é <b>inteiro</b>, ou seja, o <b>compilador python</b> reconheceu nossa variável como um número do tipo <b>inteiro.</b><br>
Mas, se quiséssemos transformar esta variável em string novamente sem usar as aspas?<br>
Basta, usar o método interno <b>str</b> na nossa impressão. 
</p>

<code>
 
    print(type(str(String3)))

</code>
E assim, a nossa String3 volta a ser uma <b>string</b>.

<code>

    <class 'str'>

</code>
<hr>

## Concatenação

<p><b>Concatenação</b> é a operação de unir o conteúdo de duas strings.
<br>
Crie uma nova variável e atribua a ela dois textos entre aspas separados por um sinal de adição.</p>
<code>

    String4 = "Python" + "é legal"

</code>

E terá como saída:

<code>

    Python é legal

</code>
<p>
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
<hr>

## Descontruindo uma String

<p>No <b>python</b>, todas as classes/tipos que possuem ideia de
ordenação (como a classe STRING) podem ser
acessadas por partes.
</p>

|P|Y|T|H|O|N|
|-|-|-|-|-|-|
|0|1|2|3|4|5|
|-6|-5|-4|-3|-2|-1|

Crie uma nova string e atribua a ela a palavra: <b>python</b>
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
<hr>

## Métodos internos
Um dos métodos internos do <b>python</b> é o len.</b><br>
O método <b>len,</b> tem como utilidade mostrar o número de caracteres de uma string <br>
Crie a nossa sexta string.

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

<b>Count</b>, é mais uma destes métodos internos.
A sua função é verificar quantas vezes tal caractere aparece.
<code>
    
    print(String6.count("o"))
</code>
saída.
<code>
    
    3
</code>
Podemos definir também de onde iniciar e onde parar
<code>

    print(String6.count("o",3,7))
    
</code>
Entre o caractere de índice três e índice sete, contém apenas uma letra <b>O.</b><br>
Vejamos, se a nossa saída é um.<br>
Saída.
<code>

    1
</code>
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

    #Isto é um comentário, ou seja, a linha não é executada pelo compilador

    True #True, pois não há caracteres alfanúmericos na String7

    False #False, pois há caracteres alfanúmericos na String8

    Brazil #A letra s foi substituida pela letra z

    ['Br', 'il'] #Foi criado um vetor para separar entre a letra a
</code>
<hr>

## Finalizando
Você agora possui conhecimento sobre oque é uma string, em<b> python</b> e como fazer manipulações com a mesma. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para sua você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>
