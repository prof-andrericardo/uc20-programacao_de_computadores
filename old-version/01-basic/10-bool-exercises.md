# Exercícios - Capítulo 10: Booleanos em Python

## Questões Dissertativas

1. Explique como Python trata diferentes tipos de valores quando convertidos para booleano usando a função bool(). Forneça exemplos de valores que são convertidos para True e False.

2. Descreva a diferença entre os operadores lógicos 'and', 'or' e 'not' em Python, explicando a precedência entre eles. Ilustre com exemplos práticos.

## Questões de Múltipla Escolha (única resposta)

3. Qual será o resultado da seguinte expressão?
```python
a = True
b = False
c = True
resultado = (a and b) or (not b and c)
print(resultado)
```
   a) False
   b) True
   c) None
   d) TypeError

4. Considere o seguinte código:
```python
valor = 0
texto = "Python"
resultado = bool(valor) or bool(texto)
```
Qual será o valor de resultado?
   a) False
   b) True
   c) 0
   d) "Python"

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais das seguintes expressões resultam em True? (Selecione todas as corretas)
   a) bool(" ")
   b) bool([0])
   c) bool(0.0)
   d) bool(None)
   e) bool(-1)

6. Em relação aos operadores de comparação em Python, quais afirmações estão corretas? (Selecione todas as corretas)
   a) == verifica igualdade de valor
   b) is verifica identidade de objetos
   c) != é o mesmo que not ==
   d) >= significa maior ou igual
   e) => é um operador válido

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) A string vazia "" é convertida para True quando usada em contexto booleano
   ( ) O operador 'and' retorna o último valor True se todos os operandos forem True
   ( ) Em Python, 0 é o único número que é convertido para False
   ( ) O operador 'or' retorna o primeiro valor True que encontrar

## Questões de Associação de Colunas

8. Associe a expressão com seu resultado:

Coluna A (Expressão):
1. True and False
2. True or False
3. not True
4. bool([])

Coluna B (Resultado):
( ) True
( ) False
( ) False
( ) False

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre booleanos em Python:

I. True e False devem sempre ser escritos com a primeira letra maiúscula
II. O operador 'not' tem precedência maior que 'and' e 'or'
III. Uma lista vazia é considerada False em contexto booleano
IV. O operador 'is' sempre produz o mesmo resultado que '=='

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) V V V F
b) V F V F
c) F V F V
d) V V F V
