# Exercícios - Capítulo 4: Função input()

## Questões Dissertativas

1. Explique por que é necessário converter o valor retornado pela função input() quando queremos trabalhar com números. Forneça um exemplo prático dessa conversão.

2. Descreva a importância do tratamento de erros (try/except) ao trabalhar com a função input(). Ilustre sua resposta com um exemplo de código.

## Questões de Múltipla Escolha (única resposta)

3. Qual será o resultado do seguinte código?
```python
numero = input("Digite um número: ")
print(type(numero))
print(numero * 2)
```
Se o usuário digitar "5", a saída será:
   a) <class 'int'> e 10
   b) <class 'str'> e 55
   c) <class 'str'> e 5
   d) <class 'int'> e 55

4. Considere o código abaixo:
```python
idade = input("Digite sua idade: ") or "0"
print(f"Idade: {idade}")
```
Se o usuário pressionar Enter sem digitar nada, qual será a saída?
   a) Idade: None
   b) Idade: 
   c) Idade: 0
   d) O programa dará erro

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais das seguintes afirmações sobre a função input() são verdadeiras? (Selecione todas as corretas)
   a) Sempre retorna uma string
   b) Pode receber múltiplos valores em uma única linha usando split()
   c) Aceita um argumento opcional que serve como mensagem para o usuário
   d) Automaticamente converte números para o tipo int
   e) Pausa a execução do programa até o usuário fornecer uma entrada

6. Em relação ao tratamento de erros com input(), quais práticas são recomendadas? (Selecione todas as corretas)
   a) Usar try/except para tratar conversões de tipo
   b) Validar se a entrada está dentro de limites esperados
   c) Fornecer mensagens de erro claras para o usuário
   d) Implementar loops para repetir em caso de entrada inválida
   e) Ignorar o tratamento de erros em programas simples

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) A função input() pode receber mais de um argumento
   ( ) É possível usar o método split() para receber múltiplos valores em uma linha
   ( ) O operador 'or' pode ser usado para definir um valor padrão para entradas vazias
   ( ) A função input() sempre converte números automaticamente para int ou float

## Questões de Associação de Colunas

8. Associe o código Python com sua funcionalidade:

Coluna A (Código):
1. valor = input("Digite algo: ")
2. numeros = input().split()
3. idade = int(input("Idade: "))
4. nome = input("Nome: ") or "Anônimo"

Coluna B (Funcionalidade):
( ) Converte entrada para número inteiro
( ) Recebe múltiplos valores em uma linha
( ) Define valor padrão para entrada vazia
( ) Recebe entrada básica do usuário

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre a função input():

I. Todo valor retornado pelo input() precisa ser convertido para ser usado em operações matemáticas
II. O método split() só pode ser usado com espaços como separador
III. Não é possível usar input() dentro de um loop while
IV. O tratamento de erros com try/except é opcional mas recomendado para melhor experiência do usuário

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) V F F V
b) V V F F
c) F F V V
d) V F V F
