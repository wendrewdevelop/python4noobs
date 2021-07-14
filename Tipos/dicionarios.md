# Dicionários

<p>Os <b>dicionários</b>, são estruturas de dados envolvidas por chaves {} e identificadas por uma key.</p>

## Exemplos

<code>

    #nome_dicionario = {"key":"valor"}
    #nome_dicionario = {key:valor}
    telefones = {"Roberval":"3344-9090","Mônica":"1331-2020"}
    print("Número do Roberval: ",telefones["Roberval"])
    print("Número da Mônica: ",telefones["Mônica"]) 
</code>
Saída
<code>

    Número do Roberval:  3344-9090
    Número da Mônica:  1331-2020
</code>

## Métodos

Os <b>dicionários</b>, possuem um método que exibe uma resposta caso não seja encontrada a key.

<code>
    
    print(telefones.get("Antonio","Contato inexistente"))
</code>
Saída
<code>
    
    Contato inexistente
</code>

## Adicionando valores

<p>Vamos adicionar um novo número a nossa lista telefônica.</p>

<code>

    telefones["Yudi"] = "4002-8922"
    print(telefones)

</code>
Saída
<code>

    {'Roberval': '3344-9090', 'Mônica': '1331-2020', 'Yudi': '4002-8922'}
</code>
Pronto, o número do Yudi foi adicionado.

## Removendo valores

<p>Vamos remover o número do Roberval agora</p>

<code>

    del telefones["Roberval"]
    print(telefones)
</code>
Saída
<code>

    {'Mônica': '1331-2020', 'Yudi': '4002-8922'}
</code>

## Finalizando
Você agora possui conhecimento sobre como funcionam os dicionários, em<b> python</b>. Prossiga nos seus estudos e pule para o próximo <b>readme.</b>
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>