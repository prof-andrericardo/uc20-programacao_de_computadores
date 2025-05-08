# Exercícios - Capítulo 3: Função print()

## Questões Dissertativas

1. Explique a diferença entre usar o operador '+' e a vírgula ',' na função print(). Forneça um exemplo prático de cada uso.

2. Descreva o que são f-strings e por que elas são consideradas uma forma moderna de formatação de strings em Python. Inclua um exemplo em sua resposta.

## Questões de Múltipla Escolha (única resposta)

3. Qual será a saída do seguinte código Python?
```python
print("Python", end="!")
print("É", end="!")
print("Incrível")
```
   a) Python!É!Incrível
   b) Python É Incrível
   c) Python!É!Incrível!
   d) PythonÉIncrível

4. Para imprimir um texto com aspas dentro, qual é a forma INCORRETA?
   a) print('Ele disse: "Olá!"')
   b) print("Ele disse: 'Olá!'")
   c) print('Ele disse: 'Olá!'')
   d) print("""Ele disse: "Olá!" """)

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais dos seguintes são caracteres de escape válidos em Python? (Selecione todas as corretas)
   a) \n
   b) \t
   c) \p
   d) \'
   e) \k

6. Em relação ao parâmetro sep do print(), quais afirmações estão corretas? (Selecione todas as corretas)
   a) O separador padrão é um espaço em branco
   b) Pode ser usado para formatar datas com barras
   c) Aceita apenas caracteres únicos como separador
   d) Pode ser uma string vazia
   e) Pode ser usado junto com o parâmetro end

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) O print() sempre adiciona uma quebra de linha ao final da impressão
   ( ) É possível usar f-strings com aspas simples e duplas
   ( ) Quando usamos vírgula no print(), precisamos converter números para string
   ( ) O parâmetro sep pode ser usado para criar caminhos de arquivo

## Questões de Associação de Colunas

8. Associe o código Python com sua respectiva saída:

Coluna A (Código):
1. print("a", "b", "c", sep="-")
2. print("Python", end="!")
3. print(f"Soma: {2+2}")
4. print("Tab\teste")

Coluna B (Saída):
( ) Python!
( ) a-b-c
( ) Soma: 4
( ) Tab    teste

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre a função print():

I. F-strings permitem incluir expressões Python diretamente dentro das chaves
II. O parâmetro end só pode receber uma string vazia ou uma quebra de linha
III. É impossível misturar números e textos sem usar a função str()
IV. Aspas triplas são usadas exclusivamente para comentários em Python

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) V F F F
b) V V F F
c) F F V V
d) V F V F
