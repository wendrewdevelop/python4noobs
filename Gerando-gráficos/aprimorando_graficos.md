## Graficos aprimorados


- No [capitulo anterior](/Gerando-gráficos/grafico_simples.md), vimos uma forma basica de como gerar um grafico, agora vamos um pouco mais além;

- No próximo exemplo foram inseridos mais comandos para criar um gráfico mais completo e com mais informações:

```python
In[]:

    # Definindo variáveis
    x = [1, 3, 5]
    y = [1, 2, 5]

    # Criando um gráfico
    plt.plot(x, y)

    # Atribuindo um título ao gráfico
    plt.title('Exemplo utilizando Plot')
    plt.xlabel('Variavel 1')
    plt.ylabel('Variavel 2')

    # Atribuindo uma legenda
    plt.plot(x, y, label = 'Uma legenda')
    plt.legend()

    # Exibindo o gráfico gerado
    plt.show()
```

```python
Out[]:
```
<p align ="center"><img align=center src="assets/plot_aprimorado.png"></p>



