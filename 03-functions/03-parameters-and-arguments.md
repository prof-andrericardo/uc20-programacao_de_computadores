# **3. Parâmetros e Argumentos**

### **3.1 Diferença entre parâmetros e argumentos**

Ao trabalhar com funções, é importante entender a diferença entre **parâmetros** e **argumentos**:

- **Parâmetros:** São as variáveis declaradas na definição da função. Elas atuam como "espaços reservados" para receber valores.
- **Argumentos:** São os valores reais passados para a função no momento em que ela é chamada.

#### **Exemplo: Diferença prática**

```python
def saudacao(nome):  # nome é o parâmetro
    print(f"Olá, {nome}!")

saudacao("Ana")  # "Ana" é o argumento
```

**Explicação:**

1. `nome` é o parâmetro definido na função `saudacao`.
2. "Ana" é o argumento passado no momento da chamada da função, substituindo o valor de `nome`.

------

### **3.2 Tipos de argumentos**

Python oferece diferentes maneiras de passar argumentos para uma função. Esses tipos incluem:

#### **3.2.1 Argumentos padrão**

Argumentos padrão permitem definir valores predefinidos para os parâmetros. Caso nenhum valor seja passado, o valor padrão será utilizado.

#### **Exemplo: Função com argumentos padrão**

```python
def apresentar(nome="Visitante", saudacao="Olá"):
    print(f"{saudacao}, {nome}!")

# Chamando a função
apresentar()  # Usa os valores padrão
apresentar("Carlos")  # Substitui apenas o nome
apresentar("Ana", "Bem-vinda")  # Substitui ambos os valores
```

**Explicação:**

1. `nome` e `saudacao` possuem valores padrão: "Visitante" e "Olá".
2. Se nenhum argumento for fornecido, os valores padrão são utilizados.
3. Argumentos passados na chamada da função substituem os valores padrão.

------

#### **3.2.2 Argumentos posicionais**

Argumentos posicionais são passados para a função na mesma ordem em que os parâmetros foram definidos.

#### **Exemplo: Função com argumentos posicionais**

```python
def calcular_total(preco, quantidade):
    total = preco * quantidade
    print(f"O total é R$ {total:.2f}")

# Chamando a função
calcular_total(10, 5)  # preco=10, quantidade=5
```

**Explicação:**

1. A ordem dos argumentos é importante e deve corresponder à ordem dos parâmetros.
2. No exemplo, `10` é atribuído a `preco` e `5` a `quantidade`.

------

#### **3.2.3 Argumentos nomeados**

Argumentos nomeados permitem especificar quais parâmetros receberão os valores, independentemente da ordem.

#### **Exemplo: Função com argumentos nomeados**

```python
def exibir_produto(nome, preco):
    print(f"Produto: {nome}, Preço: R$ {preco:.2f}")

# Chamando a função
exibir_produto(preco=15.99, nome="Caneta")
```

**Explicação:**

1. Argumentos nomeados usam `nome=valor` na chamada da função.
2. A ordem dos argumentos não importa, desde que sejam nomeados corretamente.

------

#### **3.2.4 Argumentos variáveis (`\*args` e `\**kwargs`)**

##### **`\*args`:**

Permite que uma função receba um número variável de argumentos posicionais.

#### **Exemplo: Função com `\*args`**

```python
def somar(*numeros):
    total = sum(numeros)
    print(f"A soma é {total}")

# Chamando a função
somar(1, 2, 3)  # Saída: A soma é 6
somar(10, 20, 30, 40)  # Saída: A soma é 100
```

**Explicação:**

1. `*numeros` captura todos os argumentos posicionais fornecidos e os armazena como uma tupla.
2. A função `sum()` calcula a soma de todos os valores fornecidos.

##### **`\**kwargs`:**

Permite que uma função receba um número variável de argumentos nomeados.

#### **Exemplo: Função com `\**kwargs`**

```python
def exibir_dados(**info):
    for chave, valor in info.items():
        print(f"{chave}: {valor}")

# Chamando a função
exibir_dados(nome="Ana", idade=25, cidade="São Paulo")
```

**Explicação:**

1. `**info` captura todos os argumentos nomeados fornecidos e os armazena como um dicionário.
2. O loop percorre o dicionário e exibe as informações na tela.

------

### **3.3 Exemplos práticos**

#### **3.3.1 Função que aceita valores padrão**

```python
def boas_vindas(nome="Visitante", curso="Python"):
    print(f"Bem-vindo, {nome}, ao curso de {curso}!")

# Chamando a função
boas_vindas()  # Usa valores padrão
boas_vindas("Carlos")  # Substitui apenas o nome
boas_vindas("Ana", "JavaScript")  # Substitui ambos
```

**Explicação:**

1. A função possui valores padrão para os parâmetros.
2. Eles são substituídos apenas se argumentos forem fornecidos.

#### **3.3.2 Função que utiliza `\*args` para múltiplos argumentos**

```python
def listar_itens(*itens):
    print("Itens fornecidos:")
    for item in itens:
        print(f"- {item}")

# Chamando a função
listar_itens("Livro", "Caderno", "Caneta")
```

**Explicação:**

1. `*itens` captura todos os argumentos posicionais em uma tupla.
2. O loop exibe cada item fornecido.

#### **3.3.3 Função que utiliza `\**kwargs` para argumentos nomeados**

```python
def descrever_pessoa(**detalhes):
    print("Descrição da pessoa:")
    for chave, valor in detalhes.items():
        print(f"{chave.capitalize()}: {valor}")

# Chamando a função
descrever_pessoa(nome="Carlos", idade=30, profissao="Engenheiro")
```

**Explicação:**

1. `**detalhes` captura argumentos nomeados como um dicionário.
2. O loop exibe os pares de chave-valor com formatação.

------

### **Conclusão**

Neste capítulo, exploramos como passar informações para funções usando parâmetros e argumentos. Vimos:

- A diferença entre parâmetros e argumentos.
- Diversos tipos de argumentos: padrão, posicional, nomeado e variáveis (`*args` e `**kwargs`).
- Exemplos práticos que demonstram como utilizar cada tipo de argumento.

Com esses conhecimentos, você está pronto para criar funções flexíveis e reutilizáveis, adaptadas a diferentes necessidades. Pratique combinando os diferentes tipos de argumentos em funções criativas!