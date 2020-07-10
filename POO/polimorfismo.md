# Polimorfismo

Já vimos anteriormente a definição de <b>polimorfismo</b>, seguiremos para a parte prática agora.

## Hora do código

Peguemos como exemplo os objetos cão, gato e galinha, todos herdeiros da classe mãe <b>animal</b>, esses objetos tem um método em comum que é emitir um som, porém, os sons desses animais são diferentes, afinal, um cachorro late, um gato mia e uma galinha cacareja, então os retornos do método emitir som devem ser diferentes. Para resolver esse problema usaremos o polimorfismo.

<ul>
    <li>Abra seu editor.</li>
    <li>Crie um arquivo .py de nome poo, onde ficaram as classes.</li>
    <li>Crie outro arquivo no nome que desejar, este script conterá as instâncias dos objetos.</li>
    <li>Vamos começar </li>
</ul>

<code>
    
    #Classe mãe animal
    class animal():
        def emitir_som(self):
            pass    
    
    #Classe cao
    class cao(animal):
        #Método em que o polimorfismo é aplicado
        def emitir_som(self):
            return "Au Au Au"

    #Classe gato
    class gato(animal):
        #Método em que o polimorfismo é aplicado
        def emitir_som(self):
            return "Miau Miau Miau"

    #Classe galinha
    class galinha(animal):
        #Método em que o polimorfismo é aplicado
        def emitir_som(self):
            return "Cocoricó"

</code>

Agora, com as classes prontas vamos instanciar nossos objetos, no outro script.

<code>

    #Importação do script com as classes
    import poo

    #Instâncias
    cao = poo.cao()
    gato = poo.gato()
    galinha = poo.galinha()
    
    #Exibindo o retorno do método emitir_som
    print(cao.emitir_som())
    print(gato.emitir_som())
    print(galinha.emitir_som())
</code>
Por fim, com os dois scripts basta executar o script com as instâncias e visualizar como ficou.