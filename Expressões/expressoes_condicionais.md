## Expressões Condicionais

- Expressões condicionais (às vezes chamadas de “operador ternário”) têm a prioridade mais baixa de todas as operações Python;
- A expressão <code> if C else y </code> avalia primeiro a condição *C* em vez de *x*. Se *C* for verdadeiro, *x* é avaliado e seu valor é retornado; caso contrário, *y* é avaliado e seu valor é retornado.

Sintaxe:
```python
(if <condition>: <expression1> else: <expression2>)

# Primeiramente, a <condition> é avaliada.

# Se a <condition> receber True, <expression1> é validada e retorna o resultado;

# Se a <condition> receber False, <expression2> é validada e retorna o resultado.
```


Exemplo:
```python
[IN]:

num1 = 255
if(num1 % 2 == 0):
    s = "par"
else:
    s = "ímpar"

s = "par" if num1 % 2 == 0 else "ímpar"
print("O número digitado é ", s)
```

```python
[OUT]:

O número digitado é ímpar
```

## Para entender melhor


Consulte <a href="https://www.python.org/dev/peps/pep-0308/">PEP 308</a> para obter mais detalhes sobre expressões condicionais.