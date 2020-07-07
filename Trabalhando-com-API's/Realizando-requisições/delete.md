## Requisição DELETE

- Com a lib *requests* podemos enviar uma simples requisição __DELETE__, da seguinte forma:

```python
In[]:

    import requests


    r = requests.delete("http://httpbin.org/delete")
    print(r)
```
```python
Out[]:

    # Retornando o codigo 504
    <Response [504]>

    # Esta resposta de erro é dada quando o servidor está atuando como um gateway e não obtém uma resposta a tempo. 
```

Se quiser saber mais sobre os retornos HTTP, entre em: [Respostas informativas](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)