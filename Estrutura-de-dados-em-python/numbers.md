# Numbers
 
## Tipos
<p>No <b>python</b>, existem três tipos de números:</p>
<ul>
    <li>int</li>
    <li>float</li>
    <li>complex</li>
</ul>

### Int

<p>Os números do tipo <b>int</b>, são os números inteiros, ou seja, são números positivos e negativos que não possuem casa decimal.</p>
Exemplos:

<code>
    
    #Exemplos de números inteiros
    num1 = 300
    num2 = -80 

</code>

Façamos como no arquivo anterior e perguntemos ao <b>python</b> como ele define estas variáveis.

<code>

    print(type(num1))
    print(type(num2))

</code>

Saída
<code>

    <class 'int'>
    <class 'int'>

</code>
Como já era esperado, o interpretador <b>python</b> definiu estas variáveis como números inteiros.

### Float

<p>Os números do tipo <b>float</b>, são os números racionais e irracionais, ou seja, são números positivos e negativos que  possuem casa decimal.</p>
Exemplos:
<code>

    #Exemplos de números do tipo float
    num3 = 300.5 #número positivo com uma casa decimal
    num4 = -433.6776 #número negativo com quatro casas decimais

</code>
Consultemos, agora ao interpretador <b>python</b>.

<code>

    print(type(num3))
    print(type(num4))

</code>
Saída
<code>

    <class 'float'>
    <class 'float'>
</code>

### Complex 

<p>Os números do tipo <b>complex</b>, são compostos por uma parte real e outra imaginária.</p>
Exemplos:

<code>

    num5 = 2 + 4j
    num6 = 4j
    num7 = -10j
</code>
Consultemos, agora ao interpretador <b>python</b>.
<code>

    print(type(num5))
    print(type(num6))
    print(type(num7))
</code>
Saída
<code>

    <class 'complex'>
    <class 'complex'>
    <class 'complex'>
</code>

### Número aleatório

<p>O <b>python</b>, possui um módulo que gera um número aleatório.</p>

<code>

    import random
    #Gera um número inteiro aleatório entre 0 e 10
    print(random.randint(0,10))    

</code>

## Conversões

<p>Como vimos no arquivo anterior podiamos transformar variáveis de um tipo inicial para um novo tipo.</p>
Vejamos agora conversões com números.
<code>
    
    num8 = 80 #Número do tipo int
    num9 = -9.6 #Número do tipo float

</code>

<code>

    print(type(float(num8))) #Convertendo de int para float
    
    print(type(int(num9))) #Convertendo de float para int 

    print(type(complex(num8)) #Convertendo de int para complex

    print(float(num8))
    print(int(num9))
    print(complex(num8)) 
</code>
Saída
<code>
    
    <class 'float'>
    <class 'int'>
    <class 'complex'>
    80.0
    -9
    (80+0j)
</code>

## Operações aritméticas

| Operação       | Operador  |
|----------------|-----------|
|Adição          |     +     |
|Subtração       |     -     |
|Multiplicação   |     *     |
|Divisão         |     /     |
|Divisão inteira |     //    |
|Exponenciação   |     **    |
|Resto da divisão|     %     |

### Operações com int.
<code>

    print(10 + 9) #Soma de inteiros
    print(9 - 8) #Subtração de inteiros
    print(-9 * -9) # Multiplicação de inteiros
    print(10 / 3) # Divisão de inteiros
    print(10 // 3) # Parte inteira da divisão entre inteiros
    print(10**2)  #Exponenciação entre inteiros
    print(10 % 2) #Resto da divisão entre inteiros
</code>
Saída
<code>

    19
    1
    81
    3.3333333333333335
    3
    100
    0
</code>

### Operações com float.

<code>

    print(10.5 + 8.2) #Soma com floats
    print(-98.66 - 8.99) #Subtração com floats
    print(27.5 * 3.7) # Multiplicação com floats
    print(99.2 / 3.2) # Divisão com floats
    print(99.2 // 3.2) # Parte inteira da divisão com floats
    print(0.25**2)  #Exponenciação com floats
    print(5.0 % 2.5) #Resto da divisão com floats
</code>
Saída
<code>

    18.7
    -107.64999999999999
    101.75
    31.0
    30.0
    0.0625
    0.0    
</code>

### Operações com complex.

<code>

    print(3 + 4j + 3 + 4j) #Soma com complex
    print(2 + 4j - 2 + 8j) #Subtração com complex
    print(-2 + 9j * 16 + 90j) # Multiplicação com complex
    print(2 + 10j/ 2j) # Divisão com complex
    print(25 + 2j ** 3 + 2j)  #Exponenciação com complex

</code>
<b>OBS1:</b> j equivale a -1 <br>
<b>OBS2:</b> Divisão inteira e resto não funcionam em números complexos.

Saída
<code>

    (6+8j)
    12j
    (-2+234j)
    (7+0j)
    (25-6j)
</code>

## Finalizando
Você agora possui conhecimento sobre como funcionam os números, em<b> python</b> e como fazer operações e conversões aos mesmos. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>