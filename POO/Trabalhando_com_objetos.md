# Trabalhando com objetos

Como vimos nos <b>readmes</b> anteriores, um objeto, é uma classe quando instanciada.<br>
<b>EXEMPLO:</b><br> 

<code>

    #Classe pc
    class pc:
        #Método inicializador
        def __init__(self, placaMae, cpu, memRam, hd, fonte, placaVideo):
            self.placaMae = placaMae
            self.cpu = cpu
            self.memRam = memRam 
            self.hd = hd
            self.fonte = fonte
            self.placaVideo = placaVideo

        #Método
        def ligar(self):
            return "Ligando..." 
   
    #Inicializando a classe
    #Objeto pc
    MeuPc = pc("GigaByte","Intel","Corsair","80GB","500w","Nvidia")

</code>

<b>OBS1:</b> Essa classe, pode ter funções, que quando englobadas a ela se tornam métodos como o método ligar. 

<b>OBS2:</b> Já quando a classe possui variáveis, denominamo-as como atributos.

## Acessando os atributos e métodos do objeto  
<br>
Vamos agora acessar os atributos e métodos do objeto meu PC.<br>
Digite no seu computador a classe PC e inicialize ela.
<br>
<br>
Primeiro eu quero saber a marca da placa mãe do meu PC.
Para isso preciso exibir na tela, através do comando print o atributo do objeto <b>MeuPc</b>, placaMae. 
<br>
<br>
<code>

    print("A placa mãe do seu PC é: ",MeuPc.placaMae)

</code>
Saída:

<code>

    A placa mãe do seu PC é:  GigaByte
    
</code>

Eu quero experimentar uma nova configuração para o meu PC.

Então, vou mudar o atributo <b>cpu.</b>

<code>

    MeuPc.cpu = "AMD"
    print("O processador do seu PC é: ",MeuPc.cpu)    

</code>
Saída:
<code>
    
    O processador do seu PC é:  AMD

</code>

Agora eu to afim de jogar alguma coisa, quero ligar meu PC.

Basta nós usarmos o método <b>ligar</b> do nosso objeto.

<code>

    print(MeuPc.ligar())
</code>
Saída:

<code>

    Ligando...

</code>

Por último, mas não menos importante eu quero saber toda a configuração do meu PC, em apenas um print.

Para isso acontecer usaremos o __dict__ que é: um atributo da classe.

<code>

    print(MeuPc.__dict)

</code>
Saída:
<code>

    {'placaMae': 'GigaByte', 'cpu': 'Intel', 'memRam': 'Corsair', 'hd': '80GB', 'fonte': '500w', 'placaVideo': 'Nvidia'}
</code>

Temos todos os atributos do objeto MeuPc, em um dicionário quando utilizamos o atributo __dict__.

## Considerações finais.

Agora, você possui uma visão básica de como trabalhar com um objeto em python.
<br>
Pule para os próximos readmes e bons estudos.
<br>
<br>
<b>OBS:</b> Qualquer dúvida relacionada ao contéudo apresentado neste repositório.<br>
Acesse o discord da heart developers, que a comunidade irá fornecer o suporte necessário, para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>