# 5. Variáveis em Python

Variáveis são elementos fundamentais em qualquer linguagem de programação, e no Python, elas oferecem uma flexibilidade e simplicidade notáveis. Este capítulo explora detalhadamente como criar, usar e manipular variáveis no Python, abordando aspectos como tipos de dados, escopo e boas práticas.

## 5.1. O que são Variáveis?

Uma variável é como uma "caixa" na memória do computador que guarda informações que podem ser usadas e manipuladas ao longo do programa. No Python, uma variável possui:

- Nome: Identifica a variável
- Valor: O dado armazenado na variável
- Tipo: O tipo de dado que a variável armazena (int, float, str, etc.)
- Endereço na memória: Local onde a informação está armazenada

### 5.1.1. Exemplo Básico
```python
idade = 25    # Nome: idade, Valor: 25, Tipo: int
nome = "Maria" # Nome: nome, Valor: "Maria", Tipo: str
altura = 1.68  # Nome: altura, Valor: 1.68, Tipo: float
```

## 5.2. Criando e Inicializando Variáveis

No Python, criar uma variável é simples: basta atribuir um valor a um nome usando o operador `=`.

### 5.2.1. Sintaxe Básica
```python
nome_variavel = valor
```

### 5.2.2. Exemplos Práticos
```python
# Diferentes tipos de dados em variáveis
numero = 10
texto = "Olá, mundo!"
preco = 19.99
esta_chovendo = False
```

### 5.2.3. Atribuição Múltipla
Python permite criar e inicializar várias variáveis ao mesmo tempo:
```python
x, y, z = 1, 2, 3  # Atribui valores distintos
a = b = c = 0      # Todas as variáveis têm o mesmo valor
```

## 5.3. Regras para Nomes de Variáveis

### 5.3.1. Regras Obrigatórias
1. Devem começar com uma letra (a-z, A-Z) ou underscore (_)
2. Podem conter letras, números e underscore
3. Não podem conter espaços ou caracteres especiais
4. Não podem usar palavras reservadas do Python

### 5.3.2. Palavras Reservadas
```python
import keyword
print(keyword.kwlist)  # Lista de palavras reservadas
```

### 5.3.3. Exemplos
```python
# Correto
idade = 30
_nome = "João"
nome_completo = "Ana Silva"

# Incorreto
2idade = 30            # Erro: Começa com número
nome-completo = "Ana Silva"  # Erro: Contém hífen
class = "3B"           # Erro: Palavra reservada
```

## 5.4. Tipos de Dados em Python

Python é uma linguagem de tipagem dinâmica, o que significa que não é necessário declarar explicitamente o tipo de uma variável. No entanto, cada variável possui um tipo associado ao seu valor.

### 5.4.1. Principais Tipos de Dados

1. Inteiros (int)
```python
idade = 25
saldo = -100
```

2. Ponto Flutuante (float)
```python
altura = 1.75
preco = 19.99
```

3. Strings (str)
```python
nome = "Carlos"
mensagem = 'Olá, mundo!'
```

4. Booleanos (bool)
```python
esta_chovendo = True
tem_aula = False
```

5. Listas (list)
```python
frutas = ["maçã", "banana", "laranja"]
```

6. Tuplas (tuple)
```python
coordenadas = (10, 20)
```

7. Dicionários (dict)
```python
aluno = {"nome": "João", "idade": 18}
```

## 5.5. Escopo de Variáveis

### 5.5.1. Escopo Global
- Variáveis definidas fora de qualquer função
- Podem ser acessadas em qualquer parte do programa
```python
mensagem = "Olá!"  # Variável global

def exibir_mensagem():
    print(mensagem)  # Acessa a variável global

exibir_mensagem()
```

### 5.5.2. Escopo Local
- Variáveis definidas dentro de uma função
- Existem apenas no contexto da função
```python
def funcao():
    numero = 10  # Variável local
    print(numero)

funcao()
# print(numero)  # Erro: variável não definida fora da função
```

### 5.5.3. Palavra-chave global
```python
contador = 0  # Variável global

def incrementar():
    global contador
    contador += 1

incrementar()
print(contador)  # Imprime: 1
```

## 5.6. Boas Práticas com Variáveis

### 5.6.1. Use nomes descritivos
```python
# Ruim
x = 15
y = "Silva"

# Bom
idade_aluno = 15
sobrenome = "Silva"
```

### 5.6.2. Prefira snake_case
```python
# Ruim
nomePessoa = "João Silva"     # camelCase
NomeCompleto = "Maria Santos" # PascalCase

# Bom
nome_pessoa = "João Silva"
nome_completo = "Maria Santos"
```

### 5.6.3. Evite nomes muito curtos
```python
# Ruim
n = "Carlos"
i = 42
l = [1, 2, 3]

# Bom
nome = "Carlos"
idade = 42
lista_numeros = [1, 2, 3]
```

### 5.6.4. Use constantes para valores fixos
```python
# Constantes são geralmente escritas em MAIÚSCULAS
PI = 3.14159
VELOCIDADE_DA_LUZ = 299792458
DIAS_DA_SEMANA = 7
```

### 5.6.5. Evite variáveis desnecessárias
```python
# Ruim
soma = a + b
return soma

# Bom
return a + b
```

### 5.6.6. Seja consistente com o estilo
```python
# Ruim: mistura de estilos
nome_pessoa = "João"
idadePessoa = 25
PESO_pessoa = 70

# Bom: consistente com snake_case
nome_pessoa = "João"
idade_pessoa = 25
peso_pessoa = 70
```

## 5.7. Manipulação de Variáveis

### 5.7.1. Operações com variáveis
```python
# Operações matemáticas
contador = 0
contador += 1        # Incremento
contador -= 1        # Decremento
valor = contador * 2 # Multiplicação
resultado = valor / 2 # Divisão
```

### 5.7.2. Conversão de tipos
```python
# Conversão entre tipos de dados
numero_texto = "42"
numero = int(numero_texto)     # String para inteiro
texto = str(numero)           # Inteiro para string
numero_float = float(numero)  # Inteiro para float
```

### 5.7.3. Verificação de tipos
```python
idade = 25
nome = "Maria"

# Verificando tipos
print(type(idade))  # <class 'int'>
print(type(nome))   # <class 'str'>

# Verificando se é de um tipo específico
print(isinstance(idade, int))  # True
print(isinstance(nome, str))   # True
```

## 5.8. Variáveis em Expressões

### 5.8.1. Expressões Matemáticas
```python
x = 10
y = 20
soma = x + y
diferenca = x - y
produto = x * y
quociente = x / y
```

### 5.8.2. Expressões Lógicas
```python
idade = 18
tem_carteira = True

pode_dirigir = idade >= 18 and tem_carteira
print(pode_dirigir)  # True
```

### 5.8.3. Expressões com Strings
```python
nome = "João"
sobrenome = "Silva"
nome_completo = nome + " " + sobrenome  # Concatenação
```

## 5.9. Considerações Finais

### 5.9.1. Dicas para um Código Mais Limpo
1. Mantenha as variáveis com nomes significativos
2. Use comentários quando necessário para explicar o propósito das variáveis
3. Evite variáveis globais quando possível
4. Inicialize suas variáveis antes de usá-las
5. Considere o escopo ao nomear variáveis

### 5.9.2. Práticas Recomendadas
```python
# Bom exemplo de organização de variáveis
TAXA_IMPOSTO = 0.15  # Constante

def calcular_salario(valor_base):
    bonus_desempenho = 0.1 * valor_base
    valor_imposto = valor_base * TAXA_IMPOSTO
    salario_liquido = valor_base + bonus_desempenho - valor_imposto
    
    return salario_liquido
```

### 5.9.3. Evite Armadilhas Comuns
```python
# Evite modificar variáveis globais
contador_global = 0

# Ruim
def incrementar():
    global contador_global
    contador_global += 1

# Melhor
def incrementar(contador):
    return contador + 1
```

## 5.10. Conclusão

O entendimento profundo de variáveis em Python é fundamental para qualquer programador. Este capítulo abordou desde conceitos básicos até práticas avançadas de manipulação de variáveis.

### 5.10.1. Resumo dos Conceitos Principais
1. Definição e natureza das variáveis em Python
2. Regras de nomenclatura e boas práticas
3. Tipos de dados e conversões
4. Escopos e suas implicações
5. Manipulação e operações com variáveis

### 5.10.2. Pontos-Chave do Aprendizado
- **Tipagem Dinâmica**: Python gerencia automaticamente os tipos de dados
- **Flexibilidade**: Múltiplas formas de atribuição e manipulação
- **Escopo**: Compreensão clara de variáveis globais e locais
- **Convenções**: Importância do snake_case e nomenclatura significativa
- **Boas Práticas**: Diretrizes para código limpo e manutenível

### 5.10.3. Padrões Comuns de Uso
```python
# 1. Atribuição com validação
idade = int(input("Digite sua idade: ")) if idade >= 0 else 0

# 2. Variáveis como flags
processamento_completo = False
while not processamento_completo:
    # processamento
    processamento_completo = True

# 3. Acumuladores
total = sum(valor for valor in valores if valor > 0)
```

### 5.10.4. Dicas para Depuração
1. Use `print(type(variavel))` para verificar tipos
2. Verifique o escopo em caso de comportamento inesperado
3. Mantenha um registro de variáveis importantes
4. Utilize nomes descritivos para facilitar a depuração
5. Inicialize variáveis com valores padrão seguros

### 5.10.5. Lista de Verificação de Boas Práticas
- [ ] Nomes significativos e descritivos
- [ ] Uso consistente de snake_case
- [ ] Inicialização adequada de variáveis
- [ ] Escopo apropriado (local vs global)
- [ ] Documentação clara quando necessário
- [ ] Uso apropriado de constantes
- [ ] Tratamento adequado de tipos

### 5.10.6. Exercícios Recomendados
1. **Básico**: Criar um programa que utilize diferentes tipos de variáveis
2. **Intermediário**: Implementar um sistema de gerenciamento de estado
3. **Avançado**: Desenvolver uma classe com propriedades e getters/setters
4. **Prático**: Criar um mini sistema de cadastro com validações
5. **Desafio**: Implementar um gerenciador de memória simples

### 5.10.7. Próximos Passos
Para aprofundar seus conhecimentos sobre variáveis em Python, sugerimos:

1. Estudar gerenciamento de memória em Python
2. Explorar decoradores e properties
3. Aprender sobre variáveis de classe e instância
4. Praticar com diferentes estruturas de dados
5. Experimentar com tipos de dados mais complexos

O domínio do uso de variáveis é essencial para o desenvolvimento de aplicações Python robustas e eficientes. Continue praticando e explorando os conceitos apresentados neste capítulo.
