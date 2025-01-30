# 12. Boas Práticas: Escrevendo Códigos Claros e Eficientes

Uma das características mais importantes de um programador não é apenas fazer o código funcionar, mas também torná-lo legível, organizado e fácil de manter. Seguir boas práticas ao programar em Python ajuda você a criar códigos profissionais que outras pessoas (e você mesmo) poderão entender no futuro.

## 12.1. Nomenclatura de Variáveis

### 12.1.1. Conceitos Básicos
Uma variável com um bom nome é como um título claro de um livro: descreve de forma breve e objetiva o que está armazenando.

### 12.1.2. Sintaxe e Regras
1. Use snake_case em variáveis:
   - Python adota o estilo snake_case
   - Palavras são separadas por _ (underscore)
2. Evite palavras reservadas:
   - Não use palavras como `if`, `while`, `class`, etc.

### 12.1.3. Exemplos Práticos
```python
# Ruim
x = 20
n = "João"
l = [1, 2, 3]

# Bom
idade_aluno = 20
nome_cliente = "João"
lista_numeros = [1, 2, 3]
```

## 12.2. Type Hints

### 12.2.1. Conceitos Básicos
Python é uma linguagem de tipagem dinâmica, mas type hints ajudam a indicar os tipos esperados, melhorando a legibilidade e manutenibilidade do código.

### 12.2.2. Sintaxe Básica
```python
def soma(a: int, b: int) -> int:
    return a + b

def saudacao(nome: str) -> str:
    return f"Olá, {nome}!"
```

### 12.2.3. Exemplos Avançados
```python
from typing import List, Dict, Optional

# Lista tipada
def media(valores: List[float]) -> float:
    return sum(valores) / len(valores)

# Dicionário tipado
def processa_dados(dados: Dict[str, int]) -> None:
    pass

# Valor opcional
def busca_usuario(id: int) -> Optional[str]:
    pass
```

## 12.3. Convenções PEP 8

### 12.3.1. Conceitos Básicos
PEP 8 é o guia de estilo para código Python, estabelecendo padrões de formatação e estilo.

### 12.3.2. Regras Principais
1. Indentação:
   - Use 4 espaços para cada nível
   - Não use tabulação
2. Linhas:
   - Máximo de 79 caracteres por linha
   - Use parênteses para quebrar linhas longas

### 12.3.3. Exemplos Práticos
```python
# Imports organizados
import os
import sys

import requests

from meu_modulo import funcao

# Indentação e quebra de linhas
def funcao_longa():
    if condicao_complexa:
        resultado = (valor1 + 
                    valor2 + 
                    valor3)
        return resultado
```

## 12.4. Documentação

### 12.4.1. Conceitos Básicos
A documentação é essencial para explicar o que o código faz e como deve ser usado.

### 12.4.2. Docstrings
```python
def calcular_area(base: float, altura: float) -> float:
    """
    Calcula a área de um triângulo.

    Args:
        base (float): A base do triângulo
        altura (float): A altura do triângulo

    Returns:
        float: A área calculada
    """
    return (base * altura) / 2
```

### 12.4.3. Comentários
```python
# Constantes do programa
TAXA_IMPOSTO = 0.15
DESCONTO_MAXIMO = 0.30

# Calcula o preço final com impostos e desconto
def calcular_preco_final(preco_base: float, desconto: float) -> float:
    # Valida o desconto máximo
    if desconto > DESCONTO_MAXIMO:
        desconto = DESCONTO_MAXIMO
    
    # Aplica desconto e imposto
    preco_com_desconto = preco_base * (1 - desconto)
    preco_final = preco_com_desconto * (1 + TAXA_IMPOSTO)
    
    return preco_final
```

## 12.5. Boas Práticas de Performance

### 12.5.1. Estruturas Eficientes
```python
# List Comprehension vs Loops
# Ruim
numeros_quadrados = []
for n in range(10):
    numeros_quadrados.append(n ** 2)

# Bom
numeros_quadrados = [n ** 2 for n in range(10)]
```

### 12.5.2. Gerenciamento de Recursos
```python
# Context Managers
with open('arquivo.txt', 'r') as f:
    conteudo = f.read()
```

### 12.5.3. Otimizações
```python
# Uso de conjuntos para busca
# Ruim
lista_numeros = [1, 2, 3, 4, 5]
if 3 in lista_numeros:  # O(n)
    print("Encontrado")

# Bom
conjunto_numeros = {1, 2, 3, 4, 5}
if 3 in conjunto_numeros:  # O(1)
    print("Encontrado")
```

## 12.6. Resumo Geral

### 12.6.1. Principais Conceitos
1. Nomenclatura clara e consistente
2. Type hints para melhor documentação
3. Convenções PEP 8
4. Documentação adequada

### 12.6.2. Práticas Recomendadas
1. Use estruturas de dados apropriadas
2. Trate exceções adequadamente
3. Mantenha funções pequenas e focadas
4. Teste seu código regularmente

### 12.6.3. Dicas de Implementação
1. Revise seu código periodicamente
2. Mantenha-se atualizado com as melhores práticas
3. Use ferramentas de análise estática
4. Implemente testes automatizados

## 12.7. Exercícios para Praticar

### 12.7.1. Exercícios Básicos
1. Renomeie variáveis seguindo as convenções Python
2. Adicione type hints a funções simples
3. Documente uma função usando docstrings

### 12.7.2. Exercícios Avançados
4. Refatore um código existente seguindo PEP 8
5. Implemente um módulo completo com documentação

## 12.8. Conclusão

### 12.8.1. Revisão dos Objetivos
Neste capítulo, exploramos as principais boas práticas para escrever código Python limpo, eficiente e bem documentado.

### 12.8.2. Próximos Passos
Com este conhecimento sobre boas práticas, você está preparado para escrever código profissional e manter projetos mais organizados e escaláveis.