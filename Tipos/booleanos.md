# Booleanos
<p>Booleano, são os valores True (verdadeiro) ou False (falso). Esses valores são úteis para representar, o resultado de uma comparação.</p>

<b>OBS1:</b> Antes dos exemplos precisamos conferir as tabelas verdade. 
 
|and  | A   | B   |
|-----|-----|-----|
|True |True |True |
|False|False|False|
|False|True |False|
|False|False|True |
<br>
<b>OBS2:</b> Observe que quando usamos <b>AND</b> uma preposição só é verdadeira quando as duas condições forem verdadeiras.<br>


|or   | A   | B   |
|-----|-----|-----|
|True |True |True |
|False|False|False|
|True |True |False|
|True |False|True |

<br>
<b>OBS2:</b> Observe que quando usamos <b>OR</b> uma preposição só é falsa quando as duas condições forem falsas.

## Exemplos

<code>
 
    a = True
    b = False

    c = a and b
    print(c)
    c = a or b
    print(c)
    c = a and a
    print(c)
    c = a or a
    print(c)
    c = b or b 
    print(c)
</code>
Saída
<code>

    False
    True
    True
    True
    False
</code>

## Finalizando
Você agora possui conhecimento sobre oque são os booleanos e como eles funcionam, em<b> python</b>. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>
