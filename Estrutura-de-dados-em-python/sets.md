# Sets
<p>Os sets, são estruturas de dados, parcialmente imutáveis, que não podem conter itens duplicados e são envolvidos por ({}) ou inicializados com o método set.</p>

## Exemplos 

<code>

    set1 = ({1,2,3,4})
    set2 = set([2,90,8,5])

    print(type(set1))
    print(type(set2))
    
</code>
Saída
<code>

    <class 'set'>
    <class 'set'>
</code>

## Adicionando dados

<code>

    set1.add(40)
    print(set1)
    
    set2.add(65)
    print(set2)
</code>
Saída
<code>

    {1, 2, 3, 4, 40}
    {65, 2, 5, 8, 90}
</code>

## Atualizando dados

<code>

    set1.update([10,8,67])
    print(set1)

    set2.update([22,33,78])
    print(set2)
</code>
Saída 
<code>

    {1, 2, 3, 4, 67, 8, 10}
    {33, 2, 5, 8, 78, 22, 90}
</code>

## Remoção de dados

<code>
    
    #O método discard, só faz uma remoção por vez
    set1.discard(8)
    print(set1)

    set2.discard(78)
    print(set2)
</code>
Saída
<code>

    {1, 2, 3, 4, 67, 10}
    {33, 2, 5, 8, 22, 90}
</code>

## Operações matemáticas

### União
<p>Na união, todos os dados dos dois sets serão “unidos” em um  um único set com todos os elementos, não Haverá repetições.</p>

<b>OBS:</b> Crie dois novos sets
<code>

    set_novo1 = ({1,2,3})
    set_novo2 = set([4,5,6])

    print(set_novo1.union(set_novo2))

</code>
Saída
<code>

    {1, 2, 3, 4, 5, 6}
</code>

### Interseção
<p>
Na interseção, apenas os dados que estiverem nos dois sets serão exibidos.
</p>
<b>OBS2:</b> Crie dois novos sets
<code>

    set_novo3 = ({4,7,8})
    set_novo4 = set([4,5,6])

    print(set_novo3.intersection(set_novo4))

</code>
Saída
<code>

    {4}
</code>

### Diferença
<p>Na diferença, restarão apenas os dados que estiverem em um dos sets.</p>
<code>

    set_novo3 = ({4,7,8})
    set_novo4 = set([4,5,6])

    print(set_novo3.difference(set_novo4))
</code>
Saída
<code>

    {8, 7}
</code>

### Diferença simétrica
<p>Na diferença simétrica, apenas os dados que estiverem nos dois sets,não haverá repetições</p>
<code>

    set_novo3 = ({4,7,8})
    set_novo4 = set([4,5,6])

    print(set_novo3.symmetric_difference(set_novo4))
</code>
Saída
<code>

    {5, 6, 7, 8}
</code>

## Finalizando
Você agora possui conhecimento sobre oque é um set e como funciona, em<b> python</b>. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>