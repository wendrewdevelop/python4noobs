## Instrução return


- O __return__ é usado no final de uma função para sinalizar o fim da mesma e retornar um valor;
- Após a declara dessa instrução de retorno, as ações dentro daquela função não são mais executadas até que sejam chamadas novamente;
- Se a instrução __return__ estiver sem nenhuma expressão, será retornado *None*.


## Sintaxe

```python

    def sintaxe_example():
        statements
        .
        .
        return [expression]
```

## Exemplos

Vamos fazer uma soma de dois numeros e usar a instrução __return__ para nos mostrar o valor da operação:

```python
In[]:

    def add(a, b): 

        # retornando a soma a + b  
        return a + b 

res = add(2, 3) 
print("O resultado da operação é: {}".format(res)) 
```

```python
Out[]:

    O resultado da operação é: 5
```

E se quisermos tivermos uma função de retorno booleano (true/false), podemos utilizar o __return__ da seguinte forma:

```python
In[]:

    def is_true(a): 
  
        # retornando um valor booleano (true/false) 
        return bool(a) 

res = is_true(2<5) 
print("\nO resultado dessa função é: {}".format(res))
```

```python
Out[]:

   O resultado dessa função é: True
```

