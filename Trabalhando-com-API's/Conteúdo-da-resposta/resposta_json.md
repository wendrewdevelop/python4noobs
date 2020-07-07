## Resposta JSON


- No caso de você estar lidando com dados JSON, a biblioteca contém o decodificador integrado:

```python
In[]:

    import requests


    r = requests.get('https://jsonplaceholder.typicode.com/todos/1')
    print(r.json())
```
```python
Out[]:

    {'userId': 1, 'id': 1, 'title': 'delectus aut autem', 'completed': False}
```

- No caso da decodificação do __JSON__ falhar, __r.json__ levanta uma exceção retornada pelo servidor.

