## Requisição PUT

- Com a lib *requests* podemos enviar uma simples requisição __PUT__, da seguinte forma:

```python
In[]:

    import requests


    r = requests.put("http://httpbin.org/put")
    print(r)
```
```python
Out[]:

    # Retornando o codigo 200
    <Response [200]>

    # Codigo 200 significa que essa requisição foi bem sucedida.
```

Se quiser saber mais sobre os retornos HTTP, entre em: [Respostas informativas](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)