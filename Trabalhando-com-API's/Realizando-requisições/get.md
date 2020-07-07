## Fazendo uma requisição

Fazer uma requisição com Requests é muito simples:

```python
In[]:

    # importe a biblioteca
    import requests


    # criando objeto para armazenar informações de uma requisição
    r = requests.get('https://github.com/timeline.json')
    print(r)
```
```python
Out[]:

    <Response [410]>
    # O retorno é uma resposta do servidor
    # Nesse caso, o código 410 siginifica que a pagina não esta mais disponivel

```

- O site da mozilla deixa a seguinte descrição para esse retorno:
    - __410 Gone__:
        - *"Esta resposta será enviada quando o conteúdo requisitado foi permanentemente deletado do servidor, sem nenhum endereço de redirecionamento. É experado que clientes removam seus caches e links para o recurso. A especificação HTTP espera que este código de status seja usado para "serviços promocionais de tempo limitado". APIs não devem se sentir obrigadas a indicar que recursos foram removidos com este código de status."*


Para entender como tratar melhor o retorno da requisição, acesse [Esse capitulo](/Trabalhando-com-API's/Conteúdo-da-resposta) desse módulo que estamos.

Se quiser saber mais sobre os retornos HTTP, entre em: [Respostas informativas](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)