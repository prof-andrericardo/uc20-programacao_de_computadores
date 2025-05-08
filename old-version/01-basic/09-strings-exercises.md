# Exercícios - Capítulo 9: Strings em Python

## Questões Dissertativas

1. Explique as diferentes formas de formatar strings em Python (%, .format() e f-strings), destacando as vantagens e desvantagens de cada método. Forneça exemplos práticos.

2. Descreva o conceito de imutabilidade das strings em Python e explique como isso afeta a manipulação de strings no código. Ilustre com exemplos.

## Questões de Múltipla Escolha (única resposta)

3. Qual será o resultado do seguinte código?
```python
texto = "Python"
print(texto[1:4])
print(texto[-1])
```
   a) "yth", "n"
   b) "Pyt", "n"
   c) "yth", "P"
   d) "Pyt", "P"

4. Considere o seguinte código:
```python
mensagem = """Linha 1
Linha 2
Linha 3"""
print(len(mensagem.split('\n')))
```
Qual será a saída?
   a) 2
   b) 3
   c) 4
   d) 5

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais dos seguintes métodos de string retornam uma nova string em maiúsculas? (Selecione todas as corretas)
   a) upper()
   b) capitalize()
   c) title()
   d) swapcase()
   e) isupper()

6. Em relação aos caracteres de escape em Python, quais afirmações estão corretas? (Selecione todas as corretas)
   a) \n representa uma nova linha
   b) \t representa uma tabulação
   c) \' permite usar aspas simples dentro de strings
   d) \p representa um parágrafo novo
   e) \\ representa uma barra invertida

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) Strings em Python são mutáveis e podem ser modificadas após a criação
   ( ) O método split() sem argumentos divide a string por espaços em branco
   ( ) É possível usar aspas triplas para criar strings de uma única linha
   ( ) O método strip() remove espaços em branco do início e do fim da string

## Questões de Associação de Colunas

8. Associe o método de string com sua funcionalidade:

Coluna A (Método):
1. count()
2. replace()
3. find()
4. join()

Coluna B (Funcionalidade):
( ) Localiza a primeira ocorrência de uma substring
( ) Concatena strings usando um separador
( ) Conta ocorrências de uma substring
( ) Substitui parte de uma string por outra

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre strings em Python:

I. Uma string pode ser criada tanto com aspas simples quanto com aspas duplas
II. O método split() sempre retorna uma lista de strings
III. F-strings são mais lentas que outros métodos de formatação
IV. Strings em Python são indexadas começando do índice 0

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) V V F V
b) V F V F
c) F V V V
d) V V F F
