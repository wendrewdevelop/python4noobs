# Desenvolvendo uma calculadora

## Requisitos 
- Python instalado no computador
- Biblioteca tkinter instalada no computador
<code>

        pip install python-tk

</code>

## Hora do código
Após, a criação do .py começamos importando a biblioteca.

<code>

    from tkinter import *

</code>
Depois inicialize ela.

<code>

    tela = Tk()
</code>
Vamos definir algumas configurações da nossa tela.
<code>
    
    #Importando a biblioteca
    from tkinter import *
    #Definindo um título para a janela
    tela.title("4noobs")
    #cor de fundo da tela
    tela.configure(background="#F4F5F4")
    tela.resizable(False,False)
    #Icone da janela
    tela.iconbitmap("ico.ico")
    #Manter a janela aberta
    tela.mainloop()
</code>

<b>OBS:</b> O ícone deve estar no mesmo diretório do .py<br>
<b>OBS:</b> Nomeie o ícone com o nome ico.
link do ícone: https://icon-icons.com/pt/icone/calculadora/34473

Depois, basta executar e conferir como ficou.<br>

Vamos, criar agora os botões e a caixa texto que receberá as operações.

<code>


    #Criando caixa de texto 
    txt = Entry(tela)
    
    #Criando botões
    btn0 = Button(tela,text="0",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn1 = Button(tela,text="1",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn2 = Button(tela,text="2",fg="black",bg="#F4F5F4",width = 5 ,height = 2
    btn3 = Button(tela,text="3",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn4 = Button(tela,text="4",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn5 = Button(tela,text="5",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn6 = Button(tela,text="6",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn7 = Button(tela,text="7",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn8 = Button(tela,text="8",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btn9 = Button(tela,text="9",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    
    btnPonto = Button(tela,text=".",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btnLimpar = Button(tela,text="Limpar",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btnResul = Button(tela,text="=",fg="black",bg="#F4F5F4",width = 10 ,height = 2)
    
    btnSoma = Button(tela,text="+",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btnSubt = Button(tela,text="-",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btnDiv = Button(tela,text="/",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    btnMulti = Button(tela,text="*",fg="black",bg="#F4F5F4",width = 5 ,height = 2)
    

    #Definindo como aloca-los na interface

    txt.grid(row = 0, columnspan = 10,padx = 10, pady = 2)
    
    btn7.grid(row = 1, column = 1, padx = 5, pady = 5)
    btn8.grid(row = 1, column = 2, padx = 5, pady = 5)
    btn9.grid(row = 1, column = 3, padx = 5, pady = 5)
    btnSoma.grid(row = 1, column = 4, padx = 5, pady = 5)
    
    btn4.grid(row = 2, column = 1, padx = 5, pady = 5)
    btn5.grid(row = 2, column = 2, padx = 5, pady = 5)
    btn6.grid(row = 2, column = 3, padx = 5, pady = 5)
    btnSubt.grid(row = 2, column = 4, padx = 5, pady = 5)
    
    btn1.grid(row = 3, column = 1, padx = 5, pady = 5)
    btn2.grid(row = 3, column = 2, padx = 5, pady = 5)
    btn3.grid(row = 3, column = 3, padx = 5, pady = 5)
    btnDiv.grid(row = 3, column = 4, padx = 5, pady = 5)
    
    btnPonto.grid(row = 4,column = 1, padx = 5, pady = 5)
    btn0.grid(row = 4, column = 2, padx = 5, pady = 5)
    btnLimpar.grid(row = 4, column = 3, padx = 5, pady = 5)
    btnMulti.grid(row = 4, column = 4, padx = 5, pady = 5)
    
    btnResul.grid(row = 5, column = 1, columnspan = 10,padx = 5, pady = 5)
    #Mantém a janela aberta
    tela.mainloop()
</code>

Antes de execurtamos novamente vamos criar as funções dos botões e adiciona-las.

<code>

    #Importa a biblioteca
    from tkinter import *
    
    tela = Tk()
    i = 0
    #Título da janela
    tela.title("4noobs")
    #cor de fundo da tela
    tela.configure(background="#F4F5F4")
    #Redimensionamento da janela
    tela.resizable(False,False)
    #Icone da janela
    tela.iconbitmap("ico.ico")
    
    def clickEscrever(valor):
        global i 
        txt.insert(i,valor)
        i += 1
    
    def clickLimpar():
        txt.delete(0,END)
        i = 0
    
    def clickResul():
        conta = txt.get()
        resultado = eval(conta)
        txt.delete(0,END)
        txt.insert(i,str(resultado))
    #Criando caixa de texto 
    txt = Entry(tela)
    
    #Criando botões
    btn0 = Button(tela,text="0",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(0))
    btn1 = Button(tela,text="1",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(1))
    btn2 = Button(tela,text="2",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(2))
    btn3 = Button(tela,text="3",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(3))
    btn4 = Button(tela,text="4",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(4))
    btn5 = Button(tela,text="5",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(5))
    btn6 = Button(tela,text="6",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(6))
    btn7 = Button(tela,text="7",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(7))
    btn8 = Button(tela,text="8",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(8))
    btn9 = Button(tela,text="9",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever(9))
    
    btnPonto = Button(tela,text=".",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever("."))
    btnLimpar = Button(tela,text="Limpar",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickLimpar())
    btnResul = Button(tela,text="=",fg="black",bg="#F4F5F4",width = 10 ,height = 2,command = lambda: clickResul())
    
    btnSoma = Button(tela,text="+",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever("+"))
    btnSubt = Button(tela,text="-",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever("-"))
    btnDiv = Button(tela,text="/",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever("/"))
    btnMulti = Button(tela,text="*",fg="black",bg="#F4F5F4",width = 5 ,height = 2,command = lambda: clickEscrever("*"))
    
    txt.grid(row = 0, columnspan = 10,padx = 10, pady = 2)
    
    btn7.grid(row = 1, column = 1, padx = 5, pady = 5)
    btn8.grid(row = 1, column = 2, padx = 5, pady = 5)
    btn9.grid(row = 1, column = 3, padx = 5, pady = 5)
    btnSoma.grid(row = 1, column = 4, padx = 5, pady = 5)
    
    btn4.grid(row = 2, column = 1, padx = 5, pady = 5)
    btn5.grid(row = 2, column = 2, padx = 5, pady = 5)
    btn6.grid(row = 2, column = 3, padx = 5, pady = 5)
    btnSubt.grid(row = 2, column = 4, padx = 5, pady = 5)
    
    btn1.grid(row = 3, column = 1, padx = 5, pady = 5)
    btn2.grid(row = 3, column = 2, padx = 5, pady = 5)
    btn3.grid(row = 3, column = 3, padx = 5, pady = 5)
    btnDiv.grid(row = 3, column = 4, padx = 5, pady = 5)
    
    btnPonto.grid(row = 4,column = 1, padx = 5, pady = 5)
    btn0.grid(row = 4, column = 2, padx = 5, pady = 5)
    btnLimpar.grid(row = 4, column = 3, padx = 5, pady = 5)
    btnMulti.grid(row = 4, column = 4, padx = 5, pady = 5)
    
    btnResul.grid(row = 5, column = 1, columnspan = 10,padx = 5, pady = 5)
    #Mantém a janela aberta
    tela.mainloop()

</code>

Agora, sua calculadora está pronta, basta executar e verificar como ficou. Enfim,você tem uma calculadora desenvolvida por sí mesmo, aproveite. Fique a vontade para explorar o código da calculadora e entender como cada linha funciona.

## Caso precise de ajuda
Caso, tenha ficado uma dúvida sobre o conteúdo apresentado neste readme, acesse o discord da heartdevs que a comunidade fornecerá o melhor suporte para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr>
