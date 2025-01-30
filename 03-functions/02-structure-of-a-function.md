# **2. Estrutura de uma Função**

### **2.1 Sintaxe básica**

Para criar uma função em Python, seguimos uma estrutura bem definida. A sintaxe básica inclui:

1. **Palavra-chave `def`:** Indica que estamos definindo uma função.
2. **Nome da função:** Deve ser descritivo e seguir as convenções de nomenclatura.
3. **Parâmetros opcionais:** Variáveis entre parênteses que recebem valores ao chamar a função.
4. **Bloco de código indentado:** Contém as instruções que a função executará.
5. **Retorno de valores (`return`):** Opcional, usado para enviar resultados para fora da função.

#### **Exemplo: Função que exibe uma saudação**

```python
def saudacao():
    print("Olá! Bem-vindo ao aprendizado de funções em Python.")

# Chamando a função
saudacao()
```

**Explicação:**

1. `def saudacao():` define a função chamada `saudacao` sem parâmetros.
2. O bloco de código dentro da função exibe uma mensagem.
3. Quando chamamos `saudacao()`, o código indentado é executado.

------

### **2.2 Palavra-chave `def`**

A palavra-chave `def` é usada para indicar o início da definição de uma função. Ela é obrigatória e deve ser seguida pelo nome da função e parênteses.

#### **Exemplo: Função com `def`**

```python
def exibir_mensagem():
    print("Esta é uma função definida pelo usuário.")

# Chamando a função
exibir_mensagem()
```

**Nota:** Após a definição da função, sempre inclua dois pontos (`:`) no final da linha.

------

### **2.3 Nome da função**

Os nomes de funções devem ser descritivos e seguir as boas práticas de nomenclatura:

- Usar letras minúsculas.
- Separar palavras com underscore (`_`), como em `calcular_media`.
- Evitar nomes genéricos, como `funcao1`.

#### **Exemplo: Nome descritivo**

```python
def calcular_media(nota1, nota2, nota3):
    media = (nota1 + nota2 + nota3) / 3
    print(f"A média é {media}")

# Chamando a função
calcular_media(8, 7, 9)
```

**Dica:** Escolher nomes claros facilita a leitura e a manutenção do código.

------

### **2.4 Parâmetros opcionais**

Parâmetros são variáveis que permitem passar informações para dentro de uma função. Eles podem ser opcionais, com valores padrão definidos.

#### **Exemplo: Função com parâmetros opcionais**

```python
def saudacao(nome="Visitante"):
    print(f"Olá, {nome}! Seja bem-vindo.")

# Chamando a função
saudacao()  # Usa o valor padrão "Visitante"
saudacao("Ana")  # Substitui o valor padrão por "Ana"
```

**Explicação:**

1. O parâmetro `nome` tem o valor padrão "Visitante".
2. Se nenhum argumento for passado, o valor padrão será usado.
3. Caso um valor seja fornecido, ele substituirá o padrão.

------

### **2.5 Bloco de código indentado**

O corpo de uma função deve ser indentado para indicar que faz parte da função. Em Python, a indentação é obrigatória.

#### **Exemplo: Função com várias instruções**

```python
def verificar_idade(idade):
    if idade >= 18:
        print("Você é maior de idade.")
    else:
        print("Você é menor de idade.")

# Chamando a função
verificar_idade(20)
verificar_idade(15)
```

**Explicação:**

1. O bloco de código dentro da função é indentado.
2. A indentação permite que Python identifique quais instruções pertencem à função.

------

### **2.6 Retorno de valores com `return`**

A instrução `return` é usada para enviar um resultado da função para quem a chamou. Isso permite que o valor retornado seja usado em outras partes do programa.

#### **Exemplo: Função que calcula o quadrado de um número**

```python
def calcular_quadrado(numero):
    return numero ** 2

# Usando o valor retornado
resultado = calcular_quadrado(5)
print(f"O quadrado de 5 é {resultado}")
```

**Explicação:**

1. A função `calcular_quadrado` retorna o valor do número ao quadrado.
2. Esse valor pode ser armazenado em uma variável (`resultado`) ou usado diretamente.

------

### **2.7 Convenções de nomenclatura**

As boas práticas de nomenclatura tornam o código mais legível e profissional:

- Use nomes descritivos para indicar claramente o que a função faz.
- Evite nomes curtos e sem significado.
- Use underscore (`_`) para separar palavras em nomes longos.

#### **Exemplo: Nomes claros**

```python
def calcular_area_circulo(raio):
    from math import pi
    return pi * raio ** 2

# Chamando a função
area = calcular_area_circulo(3)
print(f"A área do círculo é {area:.2f}")
```

**Dica:** Bons nomes evitam a necessidade de comentários excessivos no código.

------

### **2.8 Exemplos simples**

#### **2.8.1 Função sem parâmetros**

```python
def mensagem_boas_vindas():
    print("Bem-vindo ao curso de Python!")

# Chamando a função
mensagem_boas_vindas()
```

**Explicação:**

1. A função não recebe nenhum dado externo.
2. Quando chamada, exibe sempre a mesma mensagem.

#### **2.8.2 Função com parâmetros**

```python
def soma(n1, n2):
    print(f"A soma de {n1} e {n2} é {n1 + n2}")

# Chamando a função
soma(10, 5)
```

**Explicação:**

1. A função `soma` recebe dois valores como parâmetros.
2. Ela realiza a soma e exibe o resultado diretamente.

#### **2.8.3 Função com retorno**

```python
def multiplicar(n1, n2):
    return n1 * n2

# Chamando a função e usando o retorno
resultado = multiplicar(4, 5)
print(f"O resultado da multiplicação é {resultado}")
```

**Explicação:**

1. A função `multiplicar` retorna o produto de dois números.
2. O valor retornado pode ser armazenado e usado em outras partes do programa.

------

### **Conclusão**

Nesta seção, exploramos a estrutura de uma função em Python. Aprendemos sobre:

- A sintaxe básica de uma função e os elementos essenciais, como `def`, nome, parâmetros, bloco de código e `return`.
- Convenções de nomenclatura para tornar o código mais claro.
- Exemplos práticos para funções sem parâmetros, com parâmetros e com retorno.

Com essas bases, você está pronto para criar funções úteis e organizadas no Python. Pratique criando funções para resolver problemas do dia a dia, como cálculos ou automações!