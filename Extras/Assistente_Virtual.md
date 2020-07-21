# Desenvolvendo uma assistente virtual
<b>Requisitos:</b> 
<ul>
    <li>Um microfone.</li>
    <li>Python e o pacote pip instalados na máquina.</li>
</ul>
Já pensou em desenvolver uma nova siri?<br>
Já pensou em desenvolver a sua cortana?<br>
Então, você está no lugar certo.<br>
Neste .md te ensinarei a desenvolver sua própria assistente virtual.

## Instalação 
Como primeiro passo, precisamos baixar a biblioteca e ferramenta cli, <b>gtts</b> (Google Text-to-Speech) para interagir com a API do google translate. Para gravar os dados falados num arquivo .mp3.<br>
Para instalar é preciso usar o seguinte comando:
(Use este comando no seu terminal)
<br>

<code>
    
    pip install gTTS
</code>
<br>
Após, instalado o <b>gtts</b> é necessário a biblioteca playsound para reproduzir este áudio.
Para instalar só preciso usar o seguinte comando:
(Use este comando no seu terminal)
<code>

    pip install playsound
</code>

Agora, com todas as bibliotecas instaladas podemos iniciar a parte de desenvolvimento.

## 1° linhas de código

### Função de fala
Vamos começar!!!

<ol>
    <li>Abra o seu editor de código favorito.</li>
    <li>Crie um arquivo .py</li>


</ol>

Para iniciar, devemos importar as bibliotecas instaladas.

<code>
    
    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    

</code>

Agora, vamos criar a função que faz nossa assistente virtual.

<code>

    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

</code>
A função de fala está pronta. Basta agora usarmos ela

<code>
    
    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Fazendo falar
    falar("Bom dia")
</code>
Agora, é só executar.

### Função para escutar

Para que nossa assistente nos escute é necessário baixar mais uma biblioteca.
(Use este comando no seu terminal)

<code>

    pip install SpeechRecognition
</code>

Com ela instalada vamos criar a função escutar.
Não esqueça de importar a biblioteca baixada.
<code>

    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    #biblioteca que recebe o áudio do microfone
    import speech_recognition as sr

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Função que faz a assistente virtual capturar áudio do microfone
    def escutar():
        #Cria "ouvidos"
        r = sr.Recognizer()
        #procura por um microfone     
        with sr.Microphone() as s:
            #Configura o ambiente
            r.adjust_for_ambient_noise(s)
            #Captura o audio 
            audio = r.listen(s)
            #Transforma em texto
            fala = r.recognize_google(audio, language="pt-br")
        return fala       
</code>

Agora, com a função escutar pronta, basta inicializarmos ela.

<code>

    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    #biblioteca que recebe o áudio do microfone
    import speech_recognition as sr

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Função que faz a assistente virtual capturar áudio do microfone
    def escutar():
        #Cria "ouvidos"
        r = sr.Recognizer()
        #procura por um microfone     
        with sr.Microphone() as s:
            #Configura o ambiente
            r.adjust_for_ambient_noise(s)
            #Captura o audio 
            audio = r.listen(s)
            #Transforma em texto
            fala = r.recognize_google(audio, language="pt-br")
        return fala  

    print(escutar())
</code> 
Por fim, é só executar no script e conferir como ficou.

### Contando piadas 

<p>Vamos, dar uma funcionalidade muito boa a nossa assistente virtual que é contar piadas.
Para isso, busquei algumas na internet e a salvei-as num vetor. 
</p>

<code>

    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    #biblioteca que recebe o áudio do microfone
    import speech_recognition as sr
    #biblioteca que gera números aleatórios
    import random    

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Função que faz a assistente virtual capturar áudio do microfone
    def escutar():
        #Cria "ouvidos"
        r = sr.Recognizer()
        #procura por um microfone     
        with sr.Microphone() as s:
            #Configura o ambiente
            r.adjust_for_ambient_noise(s)
            #Captura o audio 
            audio = r.listen(s)
            #Transforma em texto
            fala = r.recognize_google(audio, language="pt-br")
        return fala
       
    escutar()

    #Número aleatório
    #Não se esqueça de importar a biblioteca random
    num = random.radint(0,2)

    #Vetor com três piadas
    Piadas = ["Então, porque a aranha é o animal mais carente do mundo? Por que, ela é uma ar",
    "Afinal, você conhece a piada do pônei? Pô nei eu kkkkkkkkkkkk.",
    "Afinal, o que a vaca disse para o boi? Te amuuuuuuuuuuuuuuuu."]

    """Se a função escutar, retornar "piadas", então nossa assistente conta uma piada"""

    if escutar() == "piadas":
        falar(piadas[num])
</code>

### Enviando e-mails 

Enviar e-mails é uma tarefa tão repetitiva, por que não deixarmos nossa assistente fazer isso por nós.<br>

<b>OBS:</b> Para darmos esta funcionalidade a nossa assistente usaremos uma biblioteca no próprio python.

<code>
    
    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    #biblioteca que recebe o áudio do microfone
    import speech_recognition as sr
    #biblioteca que gera números aleatórios
    import random    
    #biblioteca para envio de e-mails
    import smtplib    

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Função que faz a assistente virtual capturar áudio do microfone
    def escutar():
        #Cria "ouvidos"
        r = sr.Recognizer()
        #procura por um microfone     
        with sr.Microphone() as s:
            #Configura o ambiente
            r.adjust_for_ambient_noise(s)
            #Captura o audio 
            audio = r.listen(s)
            #Transforma em texto
            fala = r.recognize_google(audio, language="pt-br")
        return fala
    
    escutar()   
    #Número aleatório
    #Não se esqueça de importar a biblioteca random
    num = random.radint(0,2)

    #Vetor com três piadas
    Piadas = ["Então, porque a aranha é o animal mais carente do mundo? Por que, ela é uma ar",
    "Afinal, você conhece a piada do pônei? Pô nei eu kkkkkkkkkkkk.",
    "Afinal, o que a vaca disse para o boi? Te amuuuuuuuuuuuuuuuu."]

    """Se a função escutar, retornar "piadas", então nossa assistente conta uma piada"""

    if escutar() == "piadas":
        falar(piadas[num])
    #Envia um e-mail
    elif escutar() == "e-mail":
        email_remetente = "Digite aqui seu e-mail"
        senha_rementente = "Digite aqui a senha do seu e-mail"
        email_destinatario = "Digite o e-mail que vai receber sua mensagem"
        mensagem = "Digite aqui a mensagem que você deseja enviar"

        #Conexão com o servidor do gmail, via protocolo SMTP
        """Caso, deseje mudar o servidor de e-mail, verifique o endereço smtp e a porta, do novo servidor""" 
        email = smtplib.SMTP("smtp.gmail.com",587)

        #Inicia conexão com protocolo TTLS
        email.starttls()

        #Faz login na sua conta de e-mail, no caso gmail
        email.login(email_remetente,senha_remetente)

        #Envia o e-mail
        email.sendmail(email_remetente,email_destinatario,mensagem)

        falar("Enviei o e-mail")
</code>

<b>OBS1:</b> Caso, esteja usando o gmail você terá que liberar o acesso da nossa assistente nas configurações do gmail.

### Acessando sites

Nossa assistente, já tem 4 funcionalidades, por que não programarmos mais uma?<br>
Vamos, ensinar ela a abrir um site agora.

<b>OBS:</b> Usaremos a biblioteca webbrowser não se esqueça de importa-la.

<code>

    #biblioteca de criação do áudio
    from gtts import gTTS
    #biblioteca de reprodução do áudio
    import playsound
    #biblioteca que recebe o áudio do microfone
    import speech_recognition as sr
    #biblioteca que gera números aleatórios
    import random    
    #biblioteca para envio de e-mails
    import smtplib  
    #biblioteca para controlar o navegador
    import webbrowser as nav

    #Função que faz a assistente virtual falar
    #O parâmetro text é o texto que desejamos que seja falado
    def falar(text):
        #Nesta linha acontece a mágica
        tts = gTTS(text=text,lang="pt")
        arquivo = "voz.mp3"
        #Aqui salvamos o arquivo .mp3
        tts.save(arquivo)
        #Aqui reproduzimos
        playsound.playsound(arquivo)

    #Função que faz a assistente virtual capturar áudio do microfone
    def escutar():
        #Cria "ouvidos"
        r = sr.Recognizer()
        #procura por um microfone     
        with sr.Microphone() as s:
            #Configura o ambiente
            r.adjust_for_ambient_noise(s)
            #Captura o audio 
            audio = r.listen(s)
            #Transforma em texto
            fala = r.recognize_google(audio, language="pt-br")
        return fala
    
    escutar()   
    #Número aleatório
    #Não se esqueça de importar a biblioteca random
    num = random.radint(0,2)

    #Vetor com três piadas
    Piadas = ["Então, porque a aranha é o animal mais carente do mundo? Por que, ela é uma ar",
    "Afinal, você conhece a piada do pônei? Pô nei eu kkkkkkkkkkkk.",
    "Afinal, o que a vaca disse para o boi? Te amuuuuuuuuuuuuuuuu."]

    """Se a função escutar, retornar "piadas", então nossa assistente conta uma piada"""

    if escutar() == "piadas":
        falar(piadas[num])
    #Envia um e-mail
    elif escutar() == "e-mail":
        email_remetente = "Digite aqui seu e-mail"
        senha_rementente = "Digite aqui a senha do seu e-mail"
        email_destinatario = "Digite o e-mail que vai receber sua mensagem"
        mensagem = "Digite aqui a mensagem que você deseja enviar"

        #Conexão com o servidor do gmail, via protocolo SMTP
        """Caso, deseje mudar o servidor de e-mail, verifique o endereço smtp e a porta, do novo servidor""" 
        email = smtplib.SMTP("smtp.gmail.com",587)

        #Inicia conexão com protocolo TTLS
        email.starttls()

        #Faz login na sua conta de e-mail, no caso gmail
        email.login(email_remetente,senha_remetente)

        #Envia o e-mail
        email.sendmail(email_remetente,email_destinatario,mensagem)

        falar("Enviei o e-mail")
        
        elif escutar() == "google":
            nav.open("www.google.com.br")
</code>

Enfim, projeto concluido, nomeie sua <b>AV</b> e divirta-se.


## Caso precise de ajuda
Caso, tenha ficado uma dúvida sobre o conteúdo apresentado neste readme, acesse o discord da heartdevs que a comunidade fornecerá o melhor suporte para você.<br>
Discord: <a href="https://discord.com/invite/7UJDgBG">discord</a>
<hr> 

