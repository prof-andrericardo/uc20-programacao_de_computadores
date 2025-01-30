# 6. Comentários em Python

## 6.1. Introdução

Comentários são partes do código ignoradas pelo interpretador Python. Eles servem para documentar o código, explicar sua lógica e facilitar a manutenção.

## 6.2. Sintaxe Básica

### 6.2.1. Comentário de Uma Linha
```python
# Isto é um comentário de uma linha
nome = "João"  # Aqui guardamos o nome do usuário
```

### 6.2.2. Comentários Múltiplas Linhas
```python
"""
Este é um comentário
de múltiplas linhas
usando aspas triplas
"""

'''
Também podemos usar
aspas simples triplas
para comentários longos
'''
```

## 6.3. Uso Avançado

### 6.3.1. Documentação de Funções (Docstrings)
```python
def calcular_media(notas):
    """
    Calcula a média de uma lista de notas.
    
    Parâmetros:
        notas (list): Lista com as notas dos alunos
    
    Retorno:
        float: Média das notas
    """
    return sum(notas) / len(notas)
```

### 6.3.2. Comentários para Debugging
```python
def processar_dados():
    # DEBUG: Verificando entrada de dados
    dados = obter_dados()
    
    # DEBUG: Verificando processamento
    resultado = calcular(dados)
    return resultado
```

## 6.4. Melhores Práticas

### 6.4.1. Faça
```python
# Bom: Explica o "por quê", não o "o quê"
def calcular_desconto(valor):
    # Aplicamos 20% para compras acima de 100
    if valor > 100:
        return valor * 0.8
    return valor
```

### 6.4.2. Evite
```python
# Ruim: Comentário óbvio
x = x + 1  # Incrementa x

# Ruim: Comentário desatualizado
# Divide por 2
resultado = valor * 3  # Código mudou, comentário não
```

## 6.5. Exemplo Prático Completo
```python
def calcular_nota_final(provas, trabalhos):
    """
    Calcula nota final do aluno.
    Peso das provas: 70%
    Peso dos trabalhos: 30%
    """
    # Validação das notas
    if not (0 <= provas <= 10 and 0 <= trabalhos <= 10):
        return "Notas inválidas"
    
    # Cálculo com pesos
    nota_final = (provas * 0.7) + (trabalhos * 0.3)
    return nota_final
```

## 6.6. Diretrizes Importantes

### 6.6.1. Quando Usar Comentários
1. Para explicar o raciocínio por trás de decisões complexas
2. Para documentar APIs e interfaces
3. Para marcar TODO's e pontos de melhoria
4. Para explicar código que não pode ser simplificado

### 6.6.2. Quando Evitar Comentários
1. Para explicar código óbvio
2. Quando o código pode ser escrito de forma mais clara
3. Para comentários que podem ficar desatualizados
4. Para substituir nomes descritivos de variáveis e funções

## 6.7. Boas Práticas Adicionais

### 6.7.1. Estrutura de Docstrings
```python
def funcao_complexa(param1, param2):
    """
    Breve descrição da função.

    Descrição detalhada da função,
    que pode ocupar múltiplas linhas.

    Args:
        param1 (tipo): descrição do primeiro parâmetro
        param2 (tipo): descrição do segundo parâmetro

    Returns:
        tipo: descrição do retorno

    Raises:
        ExcecaoTipo: descrição da exceção
    """
    pass
```

### 6.7.2. Comentários em Debugging
```python
def processar_pedido(pedido):
    # TODO: Implementar validação de estoque
    # FIXME: Corrigir cálculo do frete
    # NOTE: Política de desconto pode mudar em 2024
    # WARNING: Esta função precisa de otimização
    pass
```

## 6.8. Lembre-se

1. Use comentários para explicar "por quê", não "o quê"
2. Mantenha comentários atualizados
3. Prefira código legível a comentários extensos
4. Use docstrings para documentar funções
5. Evite comentários óbvios

## 6.9. Conclusão

O uso adequado de comentários é uma habilidade fundamental na programação Python, permitindo criar código mais compreensível e manutenível.

### 6.9.1. Resumo dos Conceitos Principais
1. Tipos de comentários (linha única, múltiplas linhas)
2. Docstrings e documentação
3. Comentários para debugging
4. Boas práticas e diretrizes
5. Estruturação de documentação

### 6.9.2. Princípios Fundamentais
```python
# 1. Comentários explicativos
def calcular_hash(dados):
    # Usando SHA-256 por sua segurança e velocidade
    return hashlib.sha256(dados).hexdigest()

# 2. Docstrings informativas
def validar_cpf(cpf):
    """
    Valida um número de CPF.
    
    Aplica o algoritmo oficial de validação de CPF,
    incluindo verificação de dígitos e formato.
    """
    pass

# 3. Marcadores úteis
# TODO: Implementar cache
# FIXME: Corrigir bug de arredondamento
# NOTE: Atualizar conforme nova regulamentação
```

### 6.9.3. Guia Rápido de Melhores Práticas

#### O que Fazer
- Explicar o "por quê" do código
- Manter comentários atualizados
- Usar docstrings para documentação
- Comentar decisões complexas
- Marcar pontos importantes com TODO/FIXME

#### O que Evitar
- Comentar o óbvio
- Deixar comentários desatualizados
- Usar comentários em excesso
- Substituir nomes claros por comentários
- Comentar código ruim em vez de melhorá-lo

### 6.9.4. Ferramentas e Padrões
1. **Docstring Generators**
   - Sphinx
   - pydoc
   - Google Style Python Docstrings

2. **Marcadores Padrão**
   - TODO: Tarefas futuras
   - FIXME: Correções necessárias
   - NOTE: Observações importantes
   - WARNING: Avisos relevantes
   - HACK: Soluções temporárias

### 6.9.5. Exercícios Práticos Recomendados

1. **Documentação de Módulo**
```python
"""
Módulo de Processamento de Dados

Este módulo contém funções para processar e validar
dados de entrada do sistema.

Funções:
    - validar_entrada(dados): Valida dados de entrada
    - processar_dados(dados): Processa dados validados
    - gerar_relatorio(dados): Gera relatório de processamento
"""
```

2. **Documentação de Classe**
```python
class ProcessadorDados:
    """
    Classe para processamento de dados.

    Attributes:
        dados (list): Lista de dados a serem processados
        config (dict): Configurações do processador

    Methods:
        processar(): Executa o processamento dos dados
        validar(): Valida os dados antes do processamento
    """
```

### 6.9.6. Próximos Passos
1. Estudar padrões de documentação (Google, NumPy, reStructuredText)
2. Explorar ferramentas de geração de documentação
3. Praticar escrita de docstrings efetivas
4. Aprender sobre integração com IDEs
5. Desenvolver projetos com documentação completa

### 6.9.7. Considerações Finais
O domínio da arte de comentar código é essencial para:
- Manutenibilidade do código
- Colaboração em equipe
- Documentação efetiva
- Debugging eficiente
- Qualidade do software

Lembre-se: Um bom comentário é como um bom professor - explica o que não é óbvio, guia o entendimento e evita confusões. Use-os com sabedoria para criar código que não apenas funcione, mas que também seja compreensível e manutenível a longo prazo.
