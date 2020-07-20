# Bloco de notas

## Introdução

- Esse contéudo extra trata-se de um bloco de notas simples, somente para fins de complementar os estudos e conhecimentos adquiridos nesse projeto;
- Para comerçarmos, precisamos estar a par de algumas configurações, sendo elas:

    - Virtualenv:
    ```python

        # Instalando virtualenv
        sudo apt install virtualenv
        pip install virtualenv

        # Criando o ambiente virtual
        virtualenv -p python3 venv
    ```

    - Tkinter:
    ```python

        # Instalando módulo tkinter
        sudo apt-get install python3-tk 
    ```

- Para chegar até aqui, iremos supor que você ja passou pelos outros capitulos desse projeto. É de suma importancia que tal ação seja feita, para que surja o minimo de duvidas possiveis, quanto aos assuntos mais basicos.


## Hora do código

- Dando inicio ao codigo, iremos importar a biblioteca tkinter e alguns de seus módulos:

```python

    # importando todos os objetos do modulo tkinter
    from tkinter import *

    # importando os objetos asksaveasfilename e askopenfilename, usados para salvar e abrir arquivos.
    from tkinter.filedialog import asksaveasfilename,askopenfilename
```

- Agora, vamos instanciar nossa classe que comportará todo o codigo do nosso bloco de notas.

Vamos dar o nome de __PyNotePad__ e definir o construtor da nossa classe:


```python

    # Instanciando nossa classe
    class PyNotePad:
        # instanciando nosso construtor 
        def __init__(self):
            # Inicializando o interpretador
            self.root = Tk() 

            # Nomeando a janela do bloco de notas
            self.root.wm_title("Bloco de notas da he4rt")

            # criando uma barra de rolagem e permitindo que a mesma seja "ativada" quando for necessario. 
            scrollbar = Scrollbar(self.root)
            scrollbar.pack(side=RIGHT, fill=Y)


            # Nesse trecho de código estamos criando o menu de navegação do nosso bloco de notas.
            menubar = Menu(self.root)
            MENUarquivo = Menu(menubar)

            MENUarquivo.add_command(label="Salvar", command=self.salvar)

            MENUarquivo.add_command(label="Abrir", command=self.abrir)

            menubar.add_cascade(label="Arquivo", menu=MENUarquivo)

            MENUajuda = Menu(menubar)
            MENUajuda.add_command(label="Sobre", command=self.sobre)

            menubar.add_cascade(label="Ajuda", menu=MENUajuda)
            self.root.config(menu=menubar)

            # Aqui estamos criando um campo que permite escrevermos varias linhas de texto.
            self.text = Text(self.root)
            self.text.pack(expand=YES, fill=BOTH)
            self.text.config(yscrollcommand=scrollbar.set)
            scrollbar.config(command=self.text.yview)

            self.root.mainloop()
```

Com nosso construtor criado, vamos iniciar nossa função que será responsavel por executar a ação de salvar o nosso arquivo de texto:


```python

    # Aqui é a função que salva o arquivo
    def salvar(self): 

        # Instanciando a função que permite que a gente salve nosso arquivo e execute a janela de dialogo para escolher o local onde será salvo e o nome do arquivo.
        fileName = asksaveasfilename()

        # o bloco de codigo a seguir, resumidamente, permite que o nosso arquivo seja salvo, porém essa execução vem dentro de um bloco try/except/finally, fazendo com que a coordenação da ação seja feita de forma primordial.
        try:
            file = open(fileName, 'w')
            textoutput = self.text.get(0.0, END)
            file.write(textoutput)
        except:
            pass
        finally:
            file.close()
```


Temos o construtor da nossa classe e nossa função para salvar nosso arquivo, então vamos para a função que permite abrir arquivos salvos em nosso computador:

```python

    # Aqui é a função que abre um arquivo
    def abrir(self):

        # Instanciando a função que permite que a gente abra um arquivo salvo em nosso computador.
        fileName = askopenfilename()

        # o bloco de codigo a seguir, resumidamente, permite que a gente possa abrir um arquivo dentro do nosso bloco de notas, porém essa execução vem dentro de um bloco try/except/finally, fazendo com que a coordenação da ação seja feita de forma primordial.
        try:
            file = open(fileName, 'r')
            contents = file.read()

            self.text.delete(0.0, END)
            self.text.insert(0.0, contents)
        except:
            pass
```

Por ultimo, mas não menos importante, teremos uma área do nosso bloco de notas, onde podemos excrever um texto grande ou apenas a versão do bloco de notas:


```python

    # uma pequena função "sobre" :D
    def sobre(self):

        # Inicializando o interpretador
        root = Tk()

        # Definindo o titulo da janela
        root.wm_title("Sobre")

        # O bloco abaixo cria um label e atribui um texto somente de leitura (intuito do widget label)
        texto=("python4noobs notepad: Versão 1.0")
        textONlabel = Label(root, text=texto)
        textONlabel.pack() 
```

Fora da nossa clase, iremos instancia-la para que o python consiga chamar e executar a mesma:

```python

    # inicia o programa:
    PyNotePad()
```

Nosso bloco de notas esta pronto, segue abaixo o codigo completo e comentado para facilitar a visualização e entendimento do mesmo:

```python
    # Instanciando nossa classe
    class PyNotePad:
        # instanciando nosso construtor 
        def __init__(self):
            # Inicializando o interpretador
            self.root = Tk() 

            # Nomeando a janela do bloco de notas
            self.root.wm_title("Bloco de notas da he4rt")

            # criando uma barra de rolagem e permitindo que a mesma seja "ativada" quando for necessario. 
            scrollbar = Scrollbar(self.root)
            scrollbar.pack(side=RIGHT, fill=Y)


            # Nesse trecho de código estamos criando o menu de navegação do nosso bloco de notas.
            menubar = Menu(self.root)
            MENUarquivo = Menu(menubar)

            MENUarquivo.add_command(label="Salvar", command=self.salvar)

            MENUarquivo.add_command(label="Abrir", command=self.abrir)

            menubar.add_cascade(label="Arquivo", menu=MENUarquivo)

            MENUajuda = Menu(menubar)
            MENUajuda.add_command(label="Sobre", command=self.sobre)

            menubar.add_cascade(label="Ajuda", menu=MENUajuda)
            self.root.config(menu=menubar)

            # Aqui estamos criando um campo que permite escrevermos varias linhas de texto.
            self.text = Text(self.root)
            self.text.pack(expand=YES, fill=BOTH)
            self.text.config(yscrollcommand=scrollbar.set)
            scrollbar.config(command=self.text.yview)

            self.root.mainloop()

        # Aqui é a função que salva o arquivo
        def salvar(self): 

            # Instanciando a função que permite que a gente salve nosso arquivo e execute a janela de dialogo para escolher o local onde será salvo e o nome do arquivo.
            fileName = asksaveasfilename()

            # o bloco de codigo a seguir, resumidamente, permite que o nosso arquivo seja salvo, porém essa execução vem dentro de um bloco try/except/finally, fazendo com que a coordenação da ação seja feita de forma primordial.
            try:
                file = open(fileName, 'w')
                textoutput = self.text.get(0.0, END)
                file.write(textoutput)
            except:
                pass
            finally:
                file.close()

        # Aqui é a função que abre um arquivo
        def abrir(self):

            # Instanciando a função que permite que a gente abra um arquivo salvo em nosso computador.
            fileName = askopenfilename()

            # o bloco de codigo a seguir, resumidamente, permite que a gente possa abrir um arquivo dentro do nosso bloco de notas, porém essa execução vem dentro de um bloco try/except/finally, fazendo com que a coordenação da ação seja feita de forma primordial.
            try:
                file = open(fileName, 'r')
                contents = file.read()

                self.text.delete(0.0, END)
                self.text.insert(0.0, contents)
            except:
                pass

        # uma pequena função "sobre" :D
        def sobre(self):

            # Inicializando o interpretador
            root = Tk()

            # Definindo o titulo da janela
            root.wm_title("Sobre")

            # O bloco abaixo cria um label e atribui um texto somente de leitura (intuito do widget label)
            texto=("python4noobs notepad: Versão 1.0")
            textONlabel = Label(root, text=texto)
            textONlabel.pack()


    # inicia o programa:
    PyNotePad()
```