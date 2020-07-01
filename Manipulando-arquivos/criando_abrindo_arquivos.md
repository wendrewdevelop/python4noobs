## Criando e abrindo arquivos

- Aqui, veremos como criar e abrir um arquivo ja criado;
- A criação e abertura de um arquivo funciona usando o método __open()__. Este método irá abrir o arquivo que passarmos como parâmetro com um determinado modo de uso (que também será passado como parâmetro).

__Obs:__ Os modos de uso estão descritos na [Introdução](/Manipulando-arquivos/entendendo_manipulacao_arquivos.md) desse módulo.

<hr>

- Para abrir um arquivo da forma mais basica possivel, usa-se o seguinte trecho de codigo:

```python
arquivo = open("lista_de_compras.txt", "r")
```

- No techo de codigo acima, passamos dois parâmetros ao metodo __open()__, sendo eles, o nome do arquivo (ou o caminho do mesmo) e o modo de uso do método, nesse caso, a letra *r* (modo de leitura);
- Caso o arquivo não exista o console retornará: *FileNotFoundError: [Errno 2] No such file or directory: 'nome_do_arquivo'*.
- Para que a mensagem acima não ocorra, podemos trocar o modo de uso e fazer com que o python crie o arquivo caso ele não e exista, dessa forma, garantimos que o erro não ocorra e o sistema continue sendo executado normalmente. Para isso, alteraremos o modo de uso para *"a"*:

```python
arquivo = open("lista_de_compras.txt", "a")
```

## Importante saber...

- Quando usamos o operador *"b"* junto com outro parâmetro, por exemplo *"rb"*, dizemos que o arquivo será aberto para leitura em modo binário, segue o exemplo:

```python
arquivo = open("teste.bin", "ab")
```