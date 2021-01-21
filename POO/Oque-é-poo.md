# O que é POO

<b>POO(programação orientada a objetos)</b> é um paradigma de programação que tem como objetivo deixar o código, durante a fase desenvolvimento, mais inteligível e seguro.

## Pilares da POO
<b>Abstração:</b> É a capacidade de estipular características(atributos) e ações(métodos) a um objeto.  
<br>
<br>
<b>Encapsulamento:</b> O objetivo desta técnica é esconder os <b>atributos</b> do <b>objeto</b>, tornando assim sua aplicação mais segura.
<br>
<br>
<b>Herança:</b> O objetivo desta técnica é de poder reutilizar o código que já foi escrito, fazendo com que uma classe filha herde os atributos e métodos da classe mãe, assim, poupando tempo de desenvolvimento e linhas de código mais rápidas e menos volumosas em disco.
<br>
<br>
<b>Polimorfismo:</b> O objetivo desta técnica é reutilizar métodos e atributos.

<b>OBS:</b> No python, encapsulamento não é um assunto tão abordado, então, não haverá um .md para esta técnica.

### Algumas definições
<b>Objeto: </b>É a instância de uma classe.
<br>
<br>
<b>Atributos: </b>São as variáveis de uma classe.
<br>
<br>
<b>Métodos: </b>São funções de uma classe.

<b>OBS: </b>Estes arquivos, forneceram uma visão bem superficial sobre POO.

### Bom saber

- Em Python, todo valor é na verdade um objeto. Seja ele uma lista, um inteiro ou uma string, tanto faz. Um script manipula esses objetos e/ou seus métodos a modo de realizar uma ação. Por exemplo, em uma *class Pessoa* o nome *Wendrew* é um objeto, a altura *1,85* também é um objeto e assim sucessivamente. Uma classe em python é um construtor de objetos e não apenas uma declaração qualquer.

- Uma classe constrói objetos do tipo *type*, permitindo assim que criemos objetos desse tipo recém criado, veja:

```python
[IN]:

class Teste(object): pass
print(type(Teste))
```

```python
[OUT]:

<class 'type'>
```

Isso não é muito diferente de outras linguagens de programação, mas a magica ainda esta por vir, pois tendo criado o *objeto* com a declaração *class* podemos acessa-lo como qualquer outro objeto, inclusive acrescentar atributos a ele:

```python
[IN]:

Teste.x = 0
print(Teste.x)

```

```python
[OUT]:

0
```

Perceba que acrescentamos o atributo *x* ao objeto *Teste*, e isso faz com que as instancias desse objeto passe a ter esse atributo.