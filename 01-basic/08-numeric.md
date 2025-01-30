# 8. Tipos Numéricos e Operações Matemáticas em Python

Os números são uma das bases fundamentais de qualquer linguagem de programação, e em Python, eles são extremamente versáteis e fáceis de trabalhar. Este tópico abrange os diferentes tipos de números disponíveis em Python, como inteiros, números de ponto flutuante e números complexos. Além disso, exploraremos operadores aritméticos e funções matemáticas básicas que nos ajudam a realizar cálculos e resolver problemas no dia a dia.

## 8.1. Inteiros (int)

### 8.1.1. O que são Inteiros?
Os inteiros são números sem casas decimais, como `-5`, `0`, ou `42`. Em Python, eles são representados pelo tipo de dado `int` e podem ser positivos, negativos ou até mesmo zero.

### 8.1.2. Sintaxe Básica
```python
# Exemplo de número inteiro
numero = 10
print("O número é:", numero)

# Soma de dois números inteiros
a = 15
b = 7
print("A soma de", a, "e", b, "é:", a + b)
```

### 8.1.3. Exemplos Práticos
```python
# Exemplos práticos com inteiros
numero_positivo = 42
numero_negativo = -17
numero_grande = 1000000

print(f"Positivo: {numero_positivo}")
print(f"Negativo: {numero_negativo}")
print(f"Número grande: {numero_grande}")
```

## 8.2. Ponto Flutuante (float)

### 8.2.1. O que são Números de Ponto Flutuante?
Os números de ponto flutuante são usados para representar valores com casas decimais, como `3.14`, `-0.5` ou `2.0`. Em Python, eles são do tipo `float`.

### 8.2.2. Sintaxe Básica
```python
pi = 3.14159
temperatura = -5.7
valor = 10.0
```

### 8.2.3. Exemplo Prático
```python
# Cálculo com números de ponto flutuante
nota1 = 8.5
nota2 = 9.2
media = (nota1 + nota2) / 2
print("A média das notas é:", media)
```

## 8.3. Números Complexos (complex)

### 8.3.1. O que são Números Complexos?
Números complexos são compostos por uma parte real e uma parte imaginária, sendo representados no formato `a + bj`, onde `a` é a parte real e `b` é a parte imaginária. Eles são usados em cálculos avançados.

### 8.3.2. Sintaxe Básica
```python
z = 3 + 4j
w = complex(1, 2)
print(z.real)    # Parte real
print(z.imag)    # Parte imaginária
```

### 8.3.3. Exemplo Prático
```python
# Operações com números complexos
z1 = 2 + 3j
z2 = 1 - 5j
resultado = z1 + z2
print("A soma dos números complexos é:", resultado)
```

## 8.4. Operadores Aritméticos

### 8.4.1. Operadores Básicos
| Operador | Descrição       | Exemplo | Resultado |
| -------- | --------------- | ------- | --------- |
| +        | Adição          | 5 + 3   | 8         |
| -        | Subtração       | 5 - 3   | 2         |
| *        | Multiplicação   | 5 * 3   | 15        |
| /        | Divisão         | 5 / 3   | 1.6667    |
| //       | Divisão inteira | 5 // 3  | 1         |
| %        | Módulo (resto)  | 5 % 3   | 2         |
| **       | Potência        | 5 ** 3  | 125       |

### 8.4.2. Sintaxe Básica
```python
x = 10
y = 3
soma = x + y
potencia = x ** y
```

### 8.4.3. Exemplo Prático
```python
# Operadores básicos
a = 10
b = 3

print("Adição:", a + b)
print("Subtração:", a - b)
print("Multiplicação:", a * b)
print("Divisão:", a / b)
print("Divisão inteira:", a // b)
print("Resto da divisão:", a % b)
print("Potência:", a ** b)
```

## 8.5. Funções Matemáticas

### 8.5.1. Funções Matemáticas Embutidas
| Função         | Descrição                               | Exemplo        | Resultado |
| -------------- | --------------------------------------- | -------------- | --------- |
| abs(x)         | Retorna o valor absoluto de x           | abs(-10)       | 10        |
| round(x)       | Arredonda x para o inteiro mais próximo | round(4.6)     | 5         |
| pow(x, y)      | Retorna x elevado à potência y          | pow(2, 3)      | 8         |
| min(x, y, ...) | Retorna o menor valor                   | min(3, 1, 4)   | 1         |
| max(x, y, ...) | Retorna o maior valor                   | max(3, 1, 4)   | 4         |
| sum(iterable)  | Soma de todos os elementos              | sum([1, 2, 3]) | 6         |

### 8.5.2. Sintaxe Básica
```python
valor_absoluto = abs(-10)
arredondado = round(3.7)
menor_valor = min(5, 2, 8)
```

### 8.5.3. Funções do Módulo math
```python
import math

# Funções matemáticas básicas
print("Raiz quadrada de 16:", math.sqrt(16))
print("Seno de 30 graus:", math.sin(math.radians(30)))
print("Valor de PI:", math.pi)

# Arredondamento
print("Arredondando para cima:", math.ceil(4.3))
print("Arredondando para baixo:", math.floor(4.8))

# Funções trigonométricas
angulo = math.pi/4
print("Seno:", math.sin(angulo))
print("Cosseno:", math.cos(angulo))
print("Tangente:", math.tan(angulo))

# Funções exponenciais e logarítmicas
print("e elevado a 2:", math.exp(2))
print("Logaritmo natural de 10:", math.log(10))
print("Log base 10 de 100:", math.log10(100))
```

## 8.6. Resumo Geral

### 8.6.1. Principais Conceitos
As operações matemáticas em Python são intuitivas e poderosas. Com a combinação de:
1. Diferentes tipos numéricos (`int`, `float`, `complex`)
2. Operadores aritméticos básicos
3. Funções matemáticas embutidas
4. Módulo `math` para operações mais avançadas

### 8.6.2. Aplicações Práticas
- Cálculos matemáticos em programas
- Operações financeiras e estatísticas
- Processamento de dados numéricos
- Cálculos científicos e de engenharia

### 8.6.3. Melhores Práticas
- Escolher o tipo numérico adequado para cada situação
- Utilizar as funções matemáticas apropriadas
- Considerar a precisão necessária nos cálculos
- Tratar possíveis erros de divisão por zero

## 8.7. Exercícios para Praticar

### 8.7.1. Exercícios Básicos
1. Crie um programa que calcule a área de um círculo usando o valor de PI.
2. Desenvolva uma calculadora simples que realize as operações básicas.
3. Faça um programa que converta temperatura de Celsius para Fahrenheit.

### 8.7.2. Exercícios Avançados
4. Crie um programa que calcule as raízes de uma equação do segundo grau.
5. Desenvolva um calculador de juros compostos usando funções matemáticas.

## 8.8. Conclusão

### 8.8.1. Revisão dos Objetivos
Neste capítulo, exploramos os diferentes tipos numéricos em Python e suas operações, desde conceitos básicos até funções matemáticas avançadas.

### 8.8.2. Próximos Passos
Com este conhecimento sobre tipos numéricos e operações matemáticas, você está preparado para explorar tópicos mais avançados como processamento de dados e análise numérica em Python.