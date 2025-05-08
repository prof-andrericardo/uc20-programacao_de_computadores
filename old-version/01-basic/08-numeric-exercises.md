# Exercícios - Capítulo 8: Tipos Numéricos e Operações Matemáticas em Python

## Questões Dissertativas

1. Explique a diferença entre números inteiros (int) e números de ponto flutuante (float) em Python. Quando devemos usar cada um? Forneça exemplos práticos.

2. Descreva como funcionam os números complexos em Python e cite um exemplo prático de sua aplicação. Inclua código que demonstre as operações básicas com números complexos.

## Questões de Múltipla Escolha (única resposta)

3. Qual será o resultado da seguinte operação?
```python
import math
x = 3.7
y = math.floor(x)
z = math.ceil(x)
print(y + z)
```
   a) 7
   b) 8
   c) 7.7
   d) 8.0

4. Considere o seguinte código:
```python
a = 17
b = 5
resultado = a // b + a % b
```
Qual será o valor de resultado?
   a) 3.4
   b) 5
   c) 6
   d) 7

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais das seguintes expressões resultam em um número do tipo float? (Selecione todas as corretas)
   a) 10 / 2
   b) 10 // 2
   c) 3 * 2.0
   d) 4 + 3.14
   e) 5 % 2

6. Na biblioteca math, quais funções podem ser usadas para arredondamento? (Selecione todas as corretas)
   a) math.floor()
   b) math.ceil()
   c) math.round()
   d) math.trunc()
   e) math.approx()

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) Todo número float em Python ocupa mais memória que um número int
   ( ) O resultado de uma divisão (/) é sempre um número float
   ( ) Números complexos só podem ter parte imaginária inteira
   ( ) A função abs() pode ser usada com números complexos

## Questões de Associação de Colunas

8. Associe a função matemática com sua finalidade:

Coluna A (Função):
1. math.sqrt()
2. math.pow()
3. math.sin()
4. math.log()

Coluna B (Finalidade):
( ) Calcula o logaritmo natural
( ) Calcula a raiz quadrada
( ) Calcula o seno de um ângulo
( ) Eleva um número a uma potência

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre operações matemáticas em Python:

I. O operador ** e a função math.pow() sempre produzem resultados idênticos
II. A divisão por zero em Python gera um ZeroDivisionError
III. Números complexos são representados internamente como dois floats
IV. A função round() sempre arredonda para o número inteiro mais próximo

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) V V V F
b) F V V V
c) F V V F
d) V F F V
