# 7. Operadores em Python: Manipulando Dados e Tomando Decisões

Os operadores são fundamentais em qualquer linguagem de programação, e Python não é diferente. Eles permitem realizar operações matemáticas, comparar valores, atribuir informações a variáveis e muito mais. Com uma compreensão sólida dos operadores, você pode manipular dados de forma eficiente e criar programas mais complexos.

## 7.1. Operadores Aritméticos

Os operadores aritméticos permitem realizar cálculos matemáticos, como soma, subtração, multiplicação e divisão. Eles são usados para manipular números em Python.

### 7.1.1. Principais Operadores

| Operador | Descrição       | Exemplo | Resultado |
| -------- | --------------- | ------- | --------- |
| +        | Adição          | 5 + 3   | 8         |
| -        | Subtração       | 5 - 3   | 2         |
| *        | Multiplicação   | 5 * 3   | 15        |
| /        | Divisão         | 5 / 2   | 2.5       |
| //       | Divisão inteira | 5 // 2  | 2         |
| %        | Módulo (resto)  | 5 % 2   | 1         |

### 7.1.2. Exemplos Básicos
```python
# Operações básicas
print(5 + 3)  # Saída: 8
print(5 - 3)  # Saída: 2
print(5 * 3)  # Saída: 15
print(5 / 2)  # Saída: 2.5
```

### 7.1.3. Exemplos Práticos
```python
# Divisão inteira e módulo
print(5 // 2)  # Saída: 2
print(5 % 2)   # Saída: 1
```

## 7.2. Operadores de Atribuição

### 7.2.1. Principais Operadores

| Operador | Exemplo | Significado           |
| -------- | ------- | --------------------- |
| =        | x = 5   | Atribui o valor 5 a x |
| +=       | x += 2  | x = x + 2             |
| -=       | x -= 3  | x = x - 3             |
| *=       | x *= 4  | x = x * 4             |
| /=       | x /= 2  | x = x / 2             |

### 7.2.2. Exemplos Básicos
```python
x = 10
x += 5  # x = x + 5
print(x)  # Saída: 15
x *= 2  # x = x * 2
print(x)  # Saída: 30
```

### 7.2.3. Exemplos Práticos
```python
# Ajustando o preço com descontos
preco = 100
desconto = 10
preco -= desconto  # Reduz o desconto do preço
print(f"Preço final: {preco}")
```

## 7.3. Operadores de Comparação

### 7.3.1. Principais Operadores

| Operador | Descrição        | Exemplo | Resultado |
| -------- | ---------------- | ------- | --------- |
| ==       | Igualdade        | 5 == 5  | True      |
| !=       | Diferença        | 5 != 3  | True      |
| >        | Maior que        | 5 > 3   | True      |
| <        | Menor que        | 5 < 3   | False     |
| >=       | Maior ou igual a | 5 >= 5  | True      |
| <=       | Menor ou igual a | 3 <= 5  | True      |

### 7.3.2. Exemplos Básicos
```python
print(5 == 5)  # True
print(5 != 3)  # True
print(5 > 3)   # True
```

### 7.3.3. Exemplos Práticos
```python
# Validando idade
idade = int(input("Digite sua idade: "))
if idade >= 18:
    print("Você é maior de idade.")
else:
    print("Você é menor de idade.")
```

## 7.4. Operadores Lógicos

### 7.4.1. Principais Operadores

| Operador | Descrição                               | Exemplo        | Resultado |
| -------- | --------------------------------------- | -------------- | --------- |
| and      | Retorna True se ambas forem True        | True and False | False     |
| or       | Retorna True se pelo menos uma for True | True or False  | True      |
| not      | Inverte o valor booleano                | not True       | False     |

### 7.4.2. Exemplos Básicos
```python
print(True and True)   # True
print(True or False)   # True
print(not True)        # False
```

### 7.4.3. Exemplos Práticos
```python
# Verificação de login
usuario = input("Digite o usuário: ")
senha = input("Digite a senha: ")

if usuario == "admin" and senha == "1234":
    print("Login realizado com sucesso!")
else:
    print("Usuário ou senha incorretos.")
```

## 7.5. Operadores de Identidade

### 7.5.1. Principais Operadores

| Operador | Descrição                              | Exemplo    | Resultado |
| -------- | -------------------------------------- | ---------- | --------- |
| is       | Retorna True se são o mesmo objeto     | x is y     | True      |
| is not   | Retorna True se não são o mesmo objeto | x is not y | True      |

### 7.5.2. Exemplos Básicos
```python
a = [1, 2, 3]
b = a
print(a is b)      # True
```

### 7.5.3. Exemplos Práticos
```python
x = [1, 2, 3]
y = [1, 2, 3]
z = x

print(x is y)      # Saída: False (objetos diferentes)
print(x is z)      # Saída: True (mesmo objeto)
print(x is not y)  # Saída: True
```

## 7.6. Resumo Geral

### 7.6.1. Principais Conceitos

Os operadores são ferramentas essenciais para manipular dados e tomar decisões no seu programa. A prática com cada tipo de operador ajudará você a criar códigos mais poderosos e dinâmicos.

### 7.6.2. Aplicações Práticas 

- Cálculos matemáticos em programas
- Validação de condições em estruturas de controle
- Manipulação de valores em variáveis
- Verificação de identidade de objetos

## 7.7. Exercícios para Praticar

### 7.7.1. Exercícios Básicos

1. **Aritméticos**: Escreva um programa que calcule o dobro de um número fornecido pelo usuário.
2. **Atribuição**: Crie um código que atualize o preço de um produto com base em um desconto de 10%.
3. **Comparação**: Verifique se um número é maior que 50 e menor que 100.

### 7.7.2. Exercícios Avançados

4. **Lógicos**: Escreva um programa que verifique se um usuário é maior de idade e tem carteira de motorista.
5. **Identidade**: Verifique se duas listas criadas separadamente são o mesmo objeto.

## 7.8. Conclusão

### 7.8.1. Revisão dos Objetivos

Neste capítulo, exploramos os diferentes tipos de operadores em Python e como eles são fundamentais para a manipulação de dados e tomada de decisões em programação.

### 7.8.2. Próximos Passos

Com o conhecimento dos operadores, você está preparado para avançar para tópicos mais complexos como estruturas de controle e funções, onde estes operadores serão amplamente utilizados.