## O que são API's

- De uma maneira simples e ilustrativa, API's são "pontes" que conectam aplicações;
- As API's proporcionam a integração entre sistemas que possuem linguagens até mesmo distintas, de maneira agil e segura.

## Protocolo HTTP

*HTTP é um protocolo que permite enviar e receber informações na web.*

- Primeiramente, o que é protocolo?
__R:__ é um conjunto de regras que determinam que tipo de informações podem ser trocadas, basicamente.

- Agora, o que é HTTP?
__R:__ HTTP é um protocolo que permite enviar e receber informações na web.

<hr>

Dois importantes personagens no funcionamento do *HTTP* são o *cliente* e o *servidor*. Por padrão, o *cliente* sempre inicia a conversa e então o *servidor* responde.

## URLS

- __URLS__ são como identificamos o caminho que queremos operar;
- Cada __URL__ determina um recurso.

Digamos, que queremos obter a listagem de usuários de um sistema:

```
    /users/
```

Agora, quando queremos especificar qual usuário queremos retornar, normalmente, usamos o ID de registro do mesmo:

```
    /user/1
```

## Verbos HTTP

- Cada requisição está atrelada a um verbo *HTTP*, ou método, no cabeçalho de requisição. São as letras maiúsculas no início do cabeçalho. Por exemplo:

```
    GET / HTTP/1.1
```

Significa que o método __GET__ está sendo utilizado, enquanto:

```
    DELETE /users/1 HTTP/1.1
```
significa que o método __DELETE__ está sendo utilizado.

- Os verbos *HTTP* dizem ao servidor o que ele deve fazer com a informação identificada na __URL__.


#### Conhecendo os verbos HTTP

__GET__
```
GET pode ser considerado o método mais simples, com as informações passadas por meio dele o servidor retorna as informações.
```

__POST__
```
requisições POST devem executar o processo no corpo como um subordinado da URL que você está postando.
```

__DELETE__
```
O DELETE deve atuar ao contrária do PUT; deve ser utilizado quando você deseja deletar o recurso identificar pela URL, na requisição.
```

__PUT__
```
Uma requisição PUT é utilizada quando desejamos criar ou atualizar uma informação identificada por uma URL.
```