<h1>Magic Methods</h1>
<br>

- O metodos magicos são uma forma de adicionar uma "magia" para seu codigo. Esses metodos não são invocados diretamente por você, mas são usados internomente pelo python;
- Por exemplo, em uma soma de dois numeros usamos o operador **+**, porém, internomente o método **__ add __()** é chamado. Veja o exemplo pratico, realizando uma soma da forma convencional:

    ```python

        >>> num = 10
        >>> num + 5
        15
    ```

- O mesmo resultado é retornado se usarmos o método **__ add __()**:

    ```python

        >>> num.__add__(5)
        15
    ```

- As classes padrões no python usam esses métodos magicos. Para visualizar esses métodos, use a função **dir()**, veja abaixo a lista de atributos e métodos magicos usados pela classe **int**:

    ```python

        >>> dir(int)

        ['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__',
         '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', 
         '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', 
         '__getattribute__', '__getnewargs__', '__gt__', '__hash__', 
         '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', 
         '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', 
         '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', 
         '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', 
         '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', 
         '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', 
         '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', 
         '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 
         'as_integer_ratio', 'bit_length', 'conjugate', 'denominator', 
         'from_bytes', 'imag', 'numerator', 'real', 'to_bytes']
    ```

##### Como invocar esses métodos

<table>
    <thead>
        <tr>
            <th>Método magico</th>
            <th>Quando é invocado (exemplo)</th>
            <th>Explicação</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>__new__(cls [,...])</code></td>
            <td><code>instancia = MinhaClasse(arg1, arg2)</code></td>
            <td><code>__new__</code> é chamado quando criamos um instancia.</td>
        </tr>
        <tr>
            <td><code>__init__(self [,...])</code></td>
            <td><code>instancia = MinhaClasse(arg1, arg2)</code></td>
            <td><code>__init__</code> é chamado quando a instancia que criamos será inicializada.</td>
        </tr>
        <tr>
            <td><code>__cmp__(self, other)</code></td>
            <td><code>self == other</code>, <code>self &gt; other</code>, etc...</td>
            <td>Chamado quando vamos realizar qualquer compração.</td>
        </tr>
        <tr>
            <td><code>__pos__(self)</code></td>
            <td><code>+self</code></td>
            <td>Sinal de "mais".</td>
        </tr>
        <tr>
            <td><code>__neg__(self)</code></td>
            <td><code>-self</code></td>
            <td>Sinal de "menos".</td>
        </tr>
        <tr>
            <td><code>__invert__(self)</code></td>
            <td><code>~self</code></td>
            <td>Inversão de bits.</td>
        </tr>
        <tr>
            <td><code>__index__(self)</code></td>
            <td><code>x[self]</code></td>
            <td>Para ser chamado na conversão de tipo para um int quando o objeto é usado em uma slice expression. (explicado no final desse tópico).</td>
        </tr>
        <tr>
            <td><code>__bool__(self)</code></td>
            <td><code>bool(self)</code></td>
            <td>Retorna o valor booleano de um objeto.</td>
        </tr>
        <tr>
            <td><code>__getattr__(self, nome)</code></td>
            <td><code>self.nome # nome doesn't exist</code></td>
            <td>Você pode usar para dizer a uma classe como lidar com atributos que ela não gerencia explicitamente.</td>
        </tr>
        <tr>
            <td><code>__setattr__(self, nome, val)</code></td>
            <td><code>self.nome = val</code></td>
            <td>Definir um valor para um atributo.</td>
        </tr>
        <tr>
            <td><code>__delattr__(self, nome)</code></td>
            <td><code>del self.nome</code></td>
            <td>Deletar um atributo.</td>
        </tr>
        <tr>
            <td><code>__getattribute__(self, nome)</code></td>
            <td><code>self.nome</code></td>
            <td>Acessar qualquer atributo.</td>
        </tr>
        <tr>
            <td><code>__getitem__(self, key)</code></td>
            <td><code>self[key]</code></td>
            <td>Acessar qualquer item, usando um indice.</td>
        </tr>
        <tr>
            <td><code>__setitem__(self, key, val)</code></td>
            <td><code>self[key] = val</code></td>
            <td>Atribuir um valor a um item, por meio de um indice.</td>
        </tr>
        <tr>
            <td><code>__delitem__(self, key)</code></td>
            <td><code>del self[key]</code></td>
            <td>Deletar um item, por meio de um indice.</td>
        </tr>
        <tr>
            <td><code>__iter__(self)</code></td>
            <td><code>for x in self</code></td>
            <td>Interação</td>
        </tr>
        <tr>
            <td><code>__contains__(self, value)</code></td>
            <td><code>value in self</code>, <code>value not in self</code></td>
            <td>Usado para verificar se um item contém certo valor.<code>in</code></td>
        </tr>
        <tr>
            <td><code>__call__(self [,...])</code></td>
            <td><code>self(args)</code></td>
            <td>"Chamar" uma instancia de algo (variavel, função, etc...).</td>
        </tr>
        <tr>
            <td><code>__enter__(self)</code></td>
            <td><code>with self as x:</code></td>
            <td><code>with</code> Gerenciador de contexto.</td>
        </tr>
        <tr>
            <td><code>__exit__(self, exc, val, trace)</code></td>
            <td><code>with self as x:</code></td>
            <td><code>with</code> Gerenciador de contexto.</td>
        </tr>
        <tr>
            <td><code>__getstate__(self)</code></td>
            <td><code>pickle.dump(pkl_file, self)</code></td>
            <td>Serialização.</td>
        </tr>
        <tr>
            <td><code>__setstate__(self)</code></td>
            <td><code>data = pickle.load(pkl_file)</code></td>
            <td>Serialização.</td>
        </tr>
        <tr>
            <td><code>__slots__(self)</code></td>
            <td><code>__slots__ = 'foo', 'bar'</code></td>
            <td>permite que você indique explicitamente quais atributos de instância você espera que suas instâncias de objeto tenham.</td>
        </tr>
    </tbody>
</table>
    

#### Bom saber:

- **slice expression**:
  - A função **slice()** retorna a fatia de um objeto;
  - Você pode usar essa função para separar uma sequencia de valores (uma lista, por exemplo).
  - **Syntax**:
    - <code>slice(inicio, fim, intervalo)</code>

    <table class="w3-table-all notranslate"> 
        <tbody>
            <tr>
                <th style="width:20%">Parametro</th>
                <th>Descrição</th>  
            </tr>  
            <tr>
                <td><em>inicio</em></td>
                <td><em>Opcional</em>. Usando um numero inteiro, você poderá definir por onde o "corte" iniciará. O padrão 0 (zero).</td>
            </tr>
            <tr>
                <td><em>fim</em></td>
                <td>Usando um numero inteiro, você poderá definir por onde o "corte" terminará.</td>
            </tr>
            <tr>
                <td><em>intervalo</em></td>
                <td><em>Opcional</em>. Um numero inteiro definirá o intervalo no qual a função irá percorrer. O padrão é 1 (Um).</td>
            </tr>
        </tbody>
    </table>

- **gerenciadores de contexto**:
  - Os gerenciadores de contexto permitem que você aloque e libere recursos precisamente quando desejar. O exemplo mais amplamente usado de gerenciadores de contexto é a instrução with. Por exemplo:

    ```python

        with open('arquivo.txt', 'w') as arq:
            arq.write('Olá, mundo!')
    ```


