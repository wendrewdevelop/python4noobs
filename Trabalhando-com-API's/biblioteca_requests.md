## Biblioteca requests

Seguindo a [docmentação oficial](https://requests.readthedocs.io/pt_BR/latest/index.html) do projeto:


*"Requests é uma biblioteca HTTP licensiada sob Apache2, escrita em Python, para seres humanos.*

*O módulo urllib2, parte da biblioteca padrão do Python, oferece a maioria das funcionalidades do protocolo HTTP que você precisa, mas a API está completamente quebrada. Ela foi feita para uma época diferente — e uma web diferente. Ela demanda uma enorme quantidade de trabalho (inclusive para sobrescrever métodos) para realizar as tarefas mais simples."*
<hr>

## Instalação

Para instalar esse biblioteca recomendamos o uso de um ambiente virtual, para que todo o seu projeto fique isolado dentro de um ambiente onde não afetará seu S.O ou outros projetos que esteja fazendo, então:

```python

    # Instalando a biblioteca virtualenv
    pip install virtualenv

    # Verifique se foi instalado corretamente
    virtualenv --version

    # Criando o ambiente virtual
    virtualenv -p python3 venv

    # Acessando o ambiente virtual no linux
    . venv/bin/activate

    # instalando a biblioteca requests
    pip install requests
```

Após seguir esse script de instalação e configuração, estamos prontos para seguir adiante.