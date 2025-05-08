# **Sumário: Aprendizado de Funções em Python**

## **5. Funções Built-in**

### **5.1 Funções de Entrada/Saída**

As funções de entrada/saída são essenciais para interagir com o usuário, permitindo a exibição de informações e a obtenção de dados.

#### **`print()` - Exibição de dados**

A função `print()` exibe informações no console. Ela aceita múltiplos argumentos e permite a formatação de saída.

#### **Exemplo: Exibindo mensagens no console**

```python
print("Olá, mundo!")
print("O resultado é:", 42)
print("Python", "é", "incrível", sep="-", end="!\n")
```

**Explicação:**

1. `sep` define o separador entre os argumentos (padrão: espaço).
2. `end` define o caractere final da linha (padrão: nova linha `\n`).
3. Cada chamada exibe informações formatadas no console.

#### **`input()` - Entrada de dados do usuário**

A função `input()` permite que o usuário forneça dados durante a execução do programa. O valor retornado é sempre uma string.

#### **Exemplo: Solicitando informações ao usuário**

```python
nome = input("Digite seu nome: ")
idade = input("Digite sua idade: ")
print(f"Olá, {nome}! Você tem {idade} anos.")
```

**Explicação:**

1. `input()` exibe uma mensagem e espera que o usuário insira um valor.
2. O valor digitado é armazenado na variável como string.
3. `f-strings` são usadas para formatar a saída com as variáveis.

------

### **5.2 Funções de Tipo e Conversão**

Essas funções ajudam a verificar e converter tipos de dados em Python, tornando o programa mais dinâmico e flexível.

#### **`type()` - Verificação de tipo**

A função `type()` retorna o tipo de uma variável ou valor.

#### **Exemplo: Verificando tipos de dados**

```python
numero = 42
texto = "Python"
print(type(numero))  # Saída: <class 'int'>
print(type(texto))   # Saída: <class 'str'>
```

#### **Conversão de tipos básicos**

As funções `int()`, `float()`, `str()` e `bool()` convertem valores para os tipos inteiros, flutuantes, texto e booleanos, respectivamente.

#### **Exemplo: Convertendo tipos de dados**

```python
numero_str = "123"
numero = int(numero_str)
print(numero + 10)  # Saída: 133

valor = 3.14
print(str(valor))  # Saída: "3.14"
print(bool(0))     # Saída: False
```

**Explicação:**

1. `int()` converte uma string numérica para inteiro.
2. `str()` transforma qualquer valor em string.
3. `bool()` avalia valores como True ou False.

#### **Conversão para estruturas de dados**

As funções `list()`, `tuple()`, `set()` e `dict()` convertem iteráveis para listas, tuplas, conjuntos e dicionários.

#### **Exemplo: Convertendo iteráveis**

```python
valores = "12345"
print(list(valores))  # Saída: ['1', '2', '3', '4', '5']
print(tuple(valores))  # Saída: ('1', '2', '3', '4', '5')
print(set(valores))    # Saída: {'5', '2', '3', '4', '1'}
```

**Explicação:**

1. `list()` cria uma lista a partir de um iterável.
2. `tuple()` cria uma tupla (imutável).
3. `set()` cria um conjunto (sem valores duplicados).

------

### **5.3 Funções de Manipulação de Sequências**

Python oferece várias funções para manipular sequências, como listas, strings e tuplas.

#### **`len()` - Comprimento/tamanho**

A função `len()` retorna o número de itens em uma sequência.

#### **Exemplo: Obtendo o tamanho de sequências**

```python
frutas = ["maçã", "banana", "laranja"]
print(len(frutas))  # Saída: 3

palavra = "Python"
print(len(palavra))  # Saída: 6
```

#### **`range()` - Geração de sequências numéricas**

A função `range()` gera uma sequência de números, ideal para loops.

#### **Exemplo: Gerando sequências com `range()`**

```python
for i in range(1, 6):
    print(i)
```

**Explicação:**

1. `range(1, 6)` gera os números de 1 a 5 (exclui o 6).
2. Pode ser usado com passos: `range(início, fim, passo)`.

#### **`enumerate()` - Iteração com índices**

A função `enumerate()` retorna pares (índice, valor) de um iterável.

#### **Exemplo: Iterando com índices**

```python
animais = ["gato", "cachorro", "pássaro"]
for indice, animal in enumerate(animais):
    print(f"{indice}: {animal}")
```

**Explicação:**

1. `enumerate()` adiciona índices automaticamente.
2. Ideal para iterar com acesso ao índice e ao valor.

#### **`zip()` - Combinação de iteráveis**

A função `zip()` combina elementos de dois ou mais iteráveis em pares.

#### **Exemplo: Combinando listas com `zip()`**

```python
nomes = ["Ana", "Carlos", "Beatriz"]
idades = [25, 30, 22]
for nome, idade in zip(nomes, idades):
    print(f"{nome} tem {idade} anos.")
```

**Explicação:**

1. `zip()` combina os elementos correspondentes de cada iterável.
2. O loop desempacota os pares em variáveis separadas.

#### **`reversed()` - Inversão de sequências**

A função `reversed()` retorna uma versão invertida do iterável.

#### **Exemplo: Invertendo sequências**

```python
numeros = [1, 2, 3, 4, 5]
for numero in reversed(numeros):
    print(numero)
```

**Explicação:**

1. `reversed()` inverte a sequência.
2. Útil para iterar ou exibir dados na ordem inversa.

-----

### **5.4 Funções Matemáticas**

As funções matemáticas em Python permitem realizar cálculos de forma prática e eficiente, eliminando a necessidade de escrever operações básicas repetitivamente.

#### **`sum()` - Soma de elementos**

A função `sum()` calcula a soma de todos os elementos em um iterável (como listas ou tuplas).

#### **Exemplo: Calculando a soma de uma lista**

```python
numeros = [1, 2, 3, 4, 5]
resultado = sum(numeros)
print(f"A soma é: {resultado}")
```

**Explicação:**

1. `sum()` percorre os elementos da lista e os adiciona.
2. O resultado é armazenado na variável `resultado` e exibido.

#### **`max()` - Valor máximo**

A função `max()` retorna o maior valor de um iterável.

#### **Exemplo: Obtendo o maior número**

```python
valores = [10, 25, 8, 42, 15]
maior_valor = max(valores)
print(f"O maior valor é: {maior_valor}")
```

**Explicação:**

1. `max()` identifica o maior valor na lista `valores`.
2. O maior valor é armazenado em `maior_valor` e exibido.

#### **`min()` - Valor mínimo**

A função `min()` retorna o menor valor de um iterável.

#### **Exemplo: Obtendo o menor número**

```python
valores = [10, 25, 8, 42, 15]
menor_valor = min(valores)
print(f"O menor valor é: {menor_valor}")
```

**Explicação:**

1. `min()` funciona de forma semelhante a `max()`, mas retorna o menor valor.
2. O menor valor é armazenado em `menor_valor` e exibido.

#### **`abs()` - Valor absoluto**

A função `abs()` retorna o valor absoluto de um número, ou seja, transforma números negativos em positivos.

#### **Exemplo: Calculando valores absolutos**

```python
numero = -15
valor_absoluto = abs(numero)
print(f"O valor absoluto de {numero} é {valor_absoluto}")
```

**Explicação:**

1. `abs()` transforma `-15` em `15`.
2. Isso é útil em cálculos que exigem valores não negativos.

#### **`round()` - Arredondamento**

A função `round()` arredonda um número para o inteiro mais próximo ou para um número de casas decimais especificado.

#### **Exemplo: Arredondando números**

```python
valor = 3.14159
print(round(valor, 2))  # Saída: 3.14
print(round(valor))     # Saída: 3
```

**Explicação:**

1. O segundo argumento (opcional) especifica o número de casas decimais.
2. Sem o segundo argumento, o valor é arredondado para o inteiro mais próximo.

#### **`pow()` - Potenciação**

A função `pow()` calcula a potência de um número.

#### **Exemplo: Calculando potências**

```python
base = 2
expoente = 3
resultado = pow(base, expoente)
print(f"{base} elevado a {expoente} é {resultado}")
```

**Explicação:**

1. `pow(2, 3)` calcula `2^3` (2 elevado à potência 3).
2. O resultado é armazenado e exibido.

------

### **5.5 Funções de Ordenação e Filtragem**

Python oferece funções para organizar e filtrar dados, facilitando o trabalho com coleções.

#### **`sorted()` - Ordenação**

A função `sorted()` retorna uma nova lista com os elementos do iterável ordenados.

#### **Exemplo: Ordenando uma lista**

```python
numeros = [42, 10, 25, 7, 30]
numeros_ordenados = sorted(numeros)
print(f"Números ordenados: {numeros_ordenados}")
```

**Explicação:**

1. `sorted()` ordena os valores de forma crescente (padrão).
2. Para ordenar de forma decrescente, use `sorted(numeros, reverse=True)`.

#### **`filter()` - Filtragem de elementos**

A função `filter()` aplica um critério (função) para selecionar elementos de um iterável.

#### **Exemplo: Filtrando números pares**

```python
def eh_par(numero):
    return numero % 2 == 0

numeros = [1, 2, 3, 4, 5, 6]
numeros_pares = filter(eh_par, numeros)
print(list(numeros_pares))  # Saída: [2, 4, 6]
```

**Explicação:**

1. `eh_par` é uma função que verifica se um número é par.
2. `filter()` aplica essa função a cada elemento da lista, retornando apenas os pares.

#### **`map()` - Aplicação de função a iteráveis**

A função `map()` aplica uma função a cada elemento de um iterável e retorna um novo iterável com os resultados.

#### **Exemplo: Calculando o dobro dos números**

```python
def dobro(numero):
    return numero * 2

numeros = [1, 2, 3, 4]
dobros = map(dobro, numeros)
print(list(dobros))  # Saída: [2, 4, 6, 8]
```

**Explicação:**

1. `dobro` calcula o dobro de um número.
2. `map()` aplica essa função a cada elemento da lista.

-----

### **5.6 Funções de Verificação**

As funções de verificação são usadas para validar condições em iteráveis ou verificar propriedades específicas de objetos e variáveis. Essas funções são muito úteis em processos de validação e filtragem de dados.

#### **`any()` - Verifica se algum elemento é `True`**

A função `any()` retorna `True` se pelo menos um dos elementos de um iterável for avaliado como `True`.

#### **Exemplo: Verificando valores verdadeiros**

```python
valores = [0, 0, 1, 0]
resultado = any(valores)
print(f"Algum valor é verdadeiro? {resultado}")
```

**Explicação:**

1. `any()` avalia os elementos do iterável.
2. Retorna `True` porque o valor `1` é considerado verdadeiro.

#### **`all()` - Verifica se todos elementos são `True`**

A função `all()` retorna `True` apenas se todos os elementos do iterável forem avaliados como `True`.

#### **Exemplo: Verificando todos os valores**

```python
valores = [1, 1, 1, 0]
resultado = all(valores)
print(f"Todos os valores são verdadeiros? {resultado}")
```

**Explicação:**

1. `all()` retorna `False` porque o valor `0` é considerado falso.

#### **`isinstance()` - Verifica tipo de objeto**

A função `isinstance()` verifica se um objeto pertence a um tipo ou classe específica.

#### **Exemplo: Verificando tipos**

```python
numero = 10
print(isinstance(numero, int))  # Saída: True
print(isinstance(numero, str))  # Saída: False
```

**Explicação:**

1. `isinstance()` retorna `True` ou `False` dependendo do tipo do objeto.

#### **`hasattr()` - Verifica existência de atributo**

A função `hasattr()` verifica se um objeto possui um atributo específico.

#### **Exemplo: Verificando atributos de um objeto**

```python
class Pessoa:
    def __init__(self, nome):
        self.nome = nome

pessoa = Pessoa("Ana")
print(hasattr(pessoa, "nome"))  # Saída: True
print(hasattr(pessoa, "idade"))  # Saída: False
```

**Explicação:**

1. `hasattr()` retorna `True` se o atributo existir no objeto.
2. Retorna `False` caso contrário.

------

### **5.7 Funções de String**

As funções de string são úteis para manipulação e conversão de caracteres, facilitando o trabalho com textos.

#### **`chr()` - Converte inteiro para caractere**

A função `chr()` retorna o caractere correspondente a um código Unicode.

#### **Exemplo: Convertendo inteiro para caractere**

```python
codigo = 65
print(chr(codigo))  # Saída: A
```

**Explicação:**

1. `chr(65)` retorna o caractere `A`, que corresponde ao código Unicode 65.

#### **`ord()` - Converte caractere para inteiro**

A função `ord()` retorna o código Unicode de um caractere.

#### **Exemplo: Convertendo caractere para inteiro**

```python
letra = "A"
print(ord(letra))  # Saída: 65
```

**Explicação:**

1. `ord("A")` retorna `65`, o código Unicode da letra `A`.

#### **`format()` - Formatação de strings**

A função `format()` permite criar strings formatadas de maneira dinâmica.

#### **Exemplo: Usando `format()` para formatar texto**

```python
nome = "Carlos"
idade = 25
print("Meu nome é {} e tenho {} anos.".format(nome, idade))
```

**Explicação:**

1. Os valores `nome` e `idade` são inseridos nos espaços reservados `{}`.
2. A saída é: "Meu nome é Carlos e tenho 25 anos."

#### **`repr()` - Representação de objetos**

A função `repr()` retorna uma string que representa formalmente o objeto, útil para debugging.

#### **Exemplo: Representação de objetos**

```python
numero = 3.14
print(repr(numero))  # Saída: '3.14'
```

**Explicação:**

1. `repr()` retorna a representação oficial do objeto, incluindo detalhes como aspas.

------

### **5.8 Funções de Sistema**

As funções de sistema são usadas para interagir com o ambiente de execução e obter informações sobre objetos.

#### **`id()` - Identificador único do objeto**

A função `id()` retorna o identificador único de um objeto na memória.

#### **Exemplo: Obtendo o identificador de um objeto**

```python
numero = 10
print(id(numero))
```

**Explicação:**

1. O valor retornado representa o endereço na memória onde o objeto está armazenado.

#### **`help()` - Documentação de ajuda**

A função `help()` exibe a documentação de uma função, classe ou módulo.

#### **Exemplo: Usando `help()` para obter ajuda**

```python
help(print)
```

**Explicação:**

1. `help(print)` exibe a documentação da função `print`, incluindo seus parâmetros e exemplos de uso.

#### **`dir()` - Lista de atributos**

A função `dir()` retorna uma lista de atributos e métodos de um objeto.

#### **Exemplo: Listando atributos de um objeto**

```python
texto = "Python"
print(dir(texto))
```

**Explicação:**

1. `dir()` exibe métodos e atributos disponíveis para o objeto `texto`.

#### **`vars()` - Dicionário de atributos**

A função `vars()` retorna os atributos de um objeto em formato de dicionário.

#### **Exemplo: Obtendo atributos de uma classe**

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

pessoa = Pessoa("Ana", 30)
print(vars(pessoa))
```

**Explicação:**

1. `vars()` retorna `{"nome": "Ana", "idade": 30}`.
2. Isso permite acesso direto aos atributos e valores de um objeto.



