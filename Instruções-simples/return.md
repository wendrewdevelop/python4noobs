## Instrução return


- O **return** é utilizado em funções para sinalizar que a função obeteve um resultado e este deve ser retornado;
- Após a declaração dessa instrução, outras instruções não serão executadas até que a função seja chamada novamente;
- Se a instrução **return** estiver sem nenhuma expressão, será retornado `None`.
    * Caso a instrução não seja declarada, o retorno será `None`.


## Sintaxe

```python
def function_name():
    statements
    .
    .
    return [expression]
```

## Exemplos

Vamos fazer uma soma de dois numeros e usar o **return** para nos mostrar o valor da operação

```python
>>> def add(a, b): 
...    """Essa função junta `a` com `b` e retorna o resultado.""
...    return a + b 
...
>>>
>>> resultado = add(2, 3) 
>>> print("O resultado da operação é:", res)
O resultado da operação é: 5
```

Vamos ver o que a função retorna se não colocarmos o **return**.
```python
>>> def algo():
...     pass
...
>>> resultado = algo()
>>> resultado
None
```
Eita, mas eu não utilizei o **return**, por que ele retornou `None`?
Todas as funções em Python retornam alguma coisa quando executadas, por padrão, esse retorno é `None`.
Ou seja, a nossa função não retorna nada, literalmente!

Faça o teste, tente guardar o retorno da função `print` e veja o que acontece!
