## Erros e Exceções


- Toda __API__ contém um tratamento de erros e exceções, para caso haja a necessidade de retornar alguma mensagem de erro/aviso ao usuário. Por exemplo, se houver uma falha na conexão o *Requests* irá levantar uma exceção *ConnectionError*;
- Na ocasião de uma rara resposta *HTTP* inválida, *Requests* irá levantar uma exceção *HTTPError*;
- Se uma requisição excede o tempo limite, uma exceção *Timeout* é levantada;
- Se uma requisição excede o número máximo de redirecionamentos configurado, uma exceção *TooManyRedirects* é levantada;
- Todas as exceções levantadas explicitamente pelo *Requests* são herdadas de *requests.exceptions.RequestException*.

