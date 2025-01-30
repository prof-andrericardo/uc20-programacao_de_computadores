# Exercícios - Capítulo 12: Boas Práticas em Python

## Questões Dissertativas

1. Explique a importância dos Type Hints em Python e como eles melhoram a qualidade do código. Forneça exemplos práticos de seu uso em diferentes situações.

2. Compare diferentes formas de documentar código em Python (comentários vs docstrings) e explique quando usar cada uma. Ilustre sua resposta com exemplos de boas e más práticas de documentação.

## Questões de Múltipla Escolha (única resposta)

3. Qual das seguintes opções representa a melhor prática de nomenclatura de variáveis em Python?
   a) numeroDeAlunos = 10
   b) numero_de_alunos = 10
   c) NumeroDeAlunos = 10
   d) NUMERO_DE_ALUNOS = 10

4. Analise o seguinte código:
```python
def calc(n, x):
    """Calculate something"""
    return n * x + 2
```
Qual é o principal problema com este código?
   a) O nome da função é muito curto
   b) A docstring não é descritiva
   c) Faltam type hints
   d) Todas as anteriores

## Questões de Múltipla Escolha (múltiplas respostas)

5. Quais das seguintes são boas práticas segundo a PEP 8? (Selecione todas as corretas)
   a) Usar 4 espaços para indentação
   b) Limitar linhas a 79 caracteres
   c) Separar funções com duas linhas em branco
   d) Usar CamelCase para nomes de variáveis
   e) Importar módulos em linhas separadas

6. Em relação à documentação de código, quais práticas são recomendadas? (Selecione todas as corretas)
   a) Usar docstrings para funções e classes
   b) Documentar parâmetros e retornos
   c) Comentar cada linha do código
   d) Incluir exemplos de uso
   e) Explicar o óbvio

## Questões Verdadeiro ou Falso

7. Analise as afirmações:
   ( ) Type hints são obrigatórios em Python 3
   ( ) Docstrings devem ser usadas em todas as funções
   ( ) Snake_case é o padrão para nomes de classes
   ( ) Comentários devem explicar o "por quê" e não o "o quê"

## Questões de Associação de Colunas

8. Associe a prática com sua justificativa:

Coluna A (Prática):
1. Type hints
2. Context managers
3. List comprehension
4. Docstrings

Coluna B (Justificativa):
( ) Documenta a função de forma padronizada
( ) Garante liberação adequada de recursos
( ) Torna o código mais conciso e legível
( ) Facilita a detecção de erros de tipo

## Questão de Análise de Sentenças

9. Analise as seguintes sentenças sobre boas práticas em Python:

I. Type hints tornam o código mais lento em tempo de execução
II. Comentários devem ser atualizados sempre que o código muda
III. Snake_case deve ser usado para todas as variáveis
IV. Docstrings são ignoradas pelo interpretador Python

Assinale a alternativa que indica se as sentenças são verdadeiras (V) ou falsas (F):
a) F V V V
b) V F V F
c) F V V F
d) V V F V
