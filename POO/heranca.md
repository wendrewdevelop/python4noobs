# Herança

Já vimos anteriormente a definição de <b>Herança</b>, seguiremos para a parte prática agora.

## Hora do código

Primeiros passos:
<ul>
    <li>Abra o seu editor de código ou IDE</li>
    <li>Crie um arquivo .py, com o nome poo</li>
    <li>Vamos começar!!!</li>
</ul>

Considere que você está desenvolvendo um jogo eletrônico de corrida entre carros e motos. Em que, o <b>objeto</b> é veículo e possui os <b>atributos:</b> rodas, cor e modelo e os <b>métodos:</b> andar e frear.<br>
Então, criemos agora o objeto, seus atributos e métodos.
<code>
    
    #Classe veiculo
    class veiculo():
    #Método inicializador
    def __init__(self,rodas,cor,modelo):
        #Atributos
        self.rodas = rodas
        self.cor = cor
        self.modelo = modelo

    #Método andar
    def andar(self):
        return "Andando..."
    #Método frear
    def freando(self):
        return "Freando"
                 
    
</code> 
Com a classe veiculo, pronta precisamos agora aplicar a herança nas classes no moto e carro, que serão os objetos usados no nosso game.

<code>

    #Classe veiculo
    class veiculo():
    #Método inicializador
    def __init__(self,rodas,cor,modelo):
        #Atributos
        self.rodas = rodas
        self.cor = cor
        self.modelo = modelo

    #Método andar
    def andar(self):
        return "Andando..."
    #Método frear
    def frear(self):
        return "Freando"

    #Classe carro 
    class carro(veiculo):
        pass
    
    #Classe moto
    class moto(veiculo):
        pass

</code>
Agora, para conferirmos a herança funcionando crie um outro arquivo .py de qualquer nome.<br>
nesse arquivo você vai instanciar os objetos carro e moto, e usar seus seus métodos.

<code>

    #Script que contém as classes
    import poo 
    
    #Instância do objeto carro
    carro1 = poo.carro(4,"vermelha","Ferrari")
    #Instância do objeto moto
    moto1 = poo.moto(2,"preta","Yamaha")
    #Usando o método andar do objeto carro1
    print(carro1.andar())

    #Usando o método frear do objeto carro1
    print(carro1.frear())

    #Usando o método andar do objeto moto1    
    print(moto1.andar())
    
    #Usando o método frear do objeto moto1
    print(moto1.frear())
    

</code> 
Execute o script com as instâncias e observe que a herança funcionou
e assim não precisamos digitar o método andar para as classes moto e carro, o mesmo ocorreu para o método frear, pois eles foram ,<b>HERDADOS</b> da classe mãe veiculo. 