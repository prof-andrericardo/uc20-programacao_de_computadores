# Exercícios - Capítulo 6: Comentários em Python

## Questões Dissertativas

1. Explique a diferença entre comentários de linha única e docstrings em Python, e descreva quando é mais apropriado usar cada um. Forneça exemplos práticos.

2. Descreva as melhores práticas para escrever comentários em Python, explicando por que comentários devem focar no "por quê" e não no "o quê". Ilustre sua resposta com exemplos de bons e maus comentários.

## Questões de Múltipla Escolha (única resposta)

3. Qual das seguintes é a forma correta de escrever um comentário de múltiplas linhas em Python?
   a) // Este é um comentário
      // de múltiplas linhas
   b) /* Este é um comentário
       de múltiplas linhas */
   c) """ Este é um comentário
       de múltiplas linhas """
   d) -- Este é um comentário
      -- de múltiplas linhas

4. Analise o seguinte código:
```python
def calcular_media(notas):
    # Soma todas as notas e divide pelo total de notas
    return sum(notas) / len(notas)
```
Qual é o principal problema com este comentário?
   a) Está sintaticamente incorreto
   b) Está explicando o óbvio (o que o código faz)
   c) Deveria usar docstring ao invés de #
   d) Está muito curto

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais são as situações apropriadas para usar comentários? (Selecione todas as corretas)
   a) Explicar decisões complexas de algoritmos
   b) Documentar APIs e interfaces
   c) Descrever o que cada linha de código faz
   d) Marcar seções que precisam de revisão (TODO, FIXME)
   e) Substituir nomes descritivos de variáveis

6. Em relação às docstrings, quais afirmações estão corretas? (Selecione todas as corretas)
   a) Podem ser escritas com aspas triplas simples ou duplas
   b) São usadas para documentar funções, classes e módulos
   c) Devem incluir descrição dos parâmetros e retorno em funções
   d) São ignoradas pelo interpretador Python
   e) Só podem ser usadas no início do arquivo

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) Comentários sempre tornam o código mais fácil de entender
   ( ) Docstrings são acessíveis em tempo de execução através do atributo __doc__
   ( ) Todo comentário deve explicar exatamente o que o código faz
   ( ) Marcadores como TODO e FIXME são úteis para manutenção do código

## Questões de Associação de Colunas

8. Associe o tipo de comentário com seu uso mais apropriado:

Coluna A (Tipo):
1. # Comentário de linha única
2. """ Docstring """
3. # TODO:
4. # FIXME:

Coluna B (Uso):
( ) Documentar uma função ou classe
( ) Marcar código que precisa ser corrigido
( ) Explicar uma decisão complexa específica
( ) Indicar funcionalidade pendente de implementação

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre comentários em Python:

I. Comentários devem ser usados para explicar todo e qualquer código do programa
II. Docstrings são a forma recomendada de documentar funções e classes
III. Comentários desatualizados são piores que nenhum comentário
IV. Todo arquivo Python deve começar com um comentário explicando seu propósito

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) F V V F
b) V F V V
c) F V V V
d) V V F F