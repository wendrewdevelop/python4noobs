## Cookies

- Basicamente, os __cookies__ são arquivos de internet que armazenam temporariamente o que o internauta está visitando na rede. Esses bytes geralmente possuem formato de texto e não ocupam praticamente nenhum espaço no disco rígido do computador.


Se uma resposta contém alguns cookies, você tem acesso rápido a eles:

```python
In[]:

    import requests


    # Instanciando a URL
    url = 'http://httpbin.org/cookies'

    # criando um dicionario do cookie
    cookies = dict(cookies_are='working')

    # Realizando a requisição
    r = requests.get(url, cookies=cookies)

    # Retornando o dict criado
    print(r.text)

```
```python
Out[]:

    {
        "cookies": {
            "cookies_are": "working"
        }
    }
```