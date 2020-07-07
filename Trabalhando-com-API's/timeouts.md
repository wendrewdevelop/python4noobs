## Timeouts


- Você pode dizer para as requisições pararem de esperar por uma resposta depois de um dado número de segundos com o parâmetro __timeout__:

```python
In[]:

    import requests

    # Criando o objeto e definindo o timeout da requisição.
    r = requests.get('http://github.com', timeout=0.001)
    print(r.text)
    
```
```python
Out[]:

    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    requests.exceptions.Timeout: HTTPConnectionPool(host='github.com', port=80): Request timed out. (timeout=0.001)
```

__OBS:__ *timeout somente afeta o processo da conexão, não o download do corpo da resposta.*

