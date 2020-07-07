# Desenvolvendo uma assistente virtual
<b>Requisitos:</b> 
<ul>
    <li>Um microfone.</li>
    <li>PyThon e o pacote pip instalados na máquina.</li>
</ul>
Já pensou em desenvolver uma nova siri?<br>
Já pensou em desenvolver a sua cortana?<br>
Então, você está no lugar.<br>
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
Por fim, é só executar no script e vê conferir como ficou.