## Assert

- O __assert__ nada mais é do que uma verificação, em tempo de execução, de uma condição qualquer do codigo;
- Se a condição não for verdadeira, uma exceção __AssertionError__ acontece e o programa pára;
- Não se usa para condições de erro "esperadas", como por exemplo uma conexão de rede que não abriu. O objetivo do __assert__ é auxiliar na depuração, verificando a sanidade interna do programa.
<br>

A sintaxe usada é a seguinte:

```python

    assert Expression[, Arguments]
```

## Exemplo

```python
In[]:

    def kelvin_fahrenheit(Temperatura):
        assert (Temperatura >= 0),"Mais frio que o zero absoluto!"

        return ((Temperatura-273)*1.8)+32

    print kelvin_fahrenheit(273)
    print int(kelvin_fahrenheit(505.78))
    print kelvin_fahrenheit(-5)

```

```python
Out[]:

    32.0
    451

    Traceback (most recent call last):
    File "kelvin_fahrenheit.py", line 9, in <module>
        print kelvin_fahrenheit(-5)
    File "kelvin_fahrenheit.py", line 4, in kelvin_fahrenheit
        assert (Temperatura >= 0),"Mais frio que o zero absoluto!"
    AssertionError: Mais frio que o zero absoluto!
```