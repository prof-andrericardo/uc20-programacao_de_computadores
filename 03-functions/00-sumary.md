# **Funções em Python**

## **1. Introdução às Funções**

- O que são funções e por que utilizá-las?
- Benefícios do uso de funções:
  - Organização do código
  - Reutilização de código
  - Redução de redundância
- Tipos de funções:
  - Funções internas (built-in)
  - Funções definidas pelo usuário

------

## **2. Estrutura de uma Função**

- Sintaxe básica:
  - Palavra-chave `def`
  - Nome da função
  - Parâmetros opcionais
  - Bloco de código indentado
  - Retorno de valores com `return`
- Convenções de nomenclatura
- Exemplos simples:
  - Função sem parâmetros
  - Função com parâmetros
  - Função com retorno

------

## **3. Parâmetros e Argumentos**

- Diferença entre parâmetros e argumentos
- Tipos de argumentos:
  - Padrão
  - Posicional
  - Nomeado
  - *args e **kwargs
- Exemplos práticos:
  - Função que aceita valores padrão
  - Função que utiliza `*args` para múltiplos argumentos
  - Função que utiliza `**kwargs` para argumentos nomeados

------

## **4. Escopo e Variáveis**

- Escopo local e global
- Uso de `global` para modificar variáveis globais
- Boas práticas para evitar conflitos de escopo
- Exemplos de como escopos influenciam o comportamento de funções

------

## **5. Funções Built-in**

- Introdução às funções internas do Python
- Organização por categorias:

### **5.1 Funções de Entrada/Saída**

- `print()` - Exibição de dados
- `input()` - Entrada de dados do usuário

### **5.2 Funções de Tipo e Conversão**

- `type()` - Verificação de tipo
- `int()`, `float()`, `str()`, `bool()` - Conversão de tipos básicos
- `list()`, `tuple()`, `set()`, `dict()` - Conversão para estruturas de dados

### **5.3 Funções de Manipulação de Sequências**

- `len()` - Comprimento/tamanho
- `range()` - Geração de sequências numéricas
- `enumerate()` - Iteração com índices
- `zip()` - Combinação de iteráveis
- `reversed()` - Inversão de sequências

### **5.4 Funções Matemáticas**

- `sum()` - Soma de elementos
- `max()` - Valor máximo
- `min()` - Valor mínimo
- `abs()` - Valor absoluto
- `round()` - Arredondamento
- `pow()` - Potenciação

### **5.5 Funções de Ordenação e Filtragem**

- `sorted()` - Ordenação
- `filter()` - Filtragem de elementos
- `map()` - Aplicação de função a iteráveis

### **5.6 Funções de Verificação**

- `any()` - Verifica se algum elemento é `True`
- `all()` - Verifica se todos elementos são `True`
- `isinstance()` - Verifica tipo de objeto
- `hasattr()` - Verifica existência de atributo

### **5.7 Funções de String**

- `chr()` - Converte inteiro para caractere
- `ord()` - Converte caractere para inteiro
- `format()` - Formatação de strings
- `repr()` - Representação de objetos

### **5.8 Funções de Sistema**

- `id()` - Identificador único do objeto
- `help()` - Documentação de ajuda
- `dir()` - Lista de atributos
- `vars()` - Dicionário de atributos

------

## **6. Funções Lambda**

- O que são funções anônimas (lambda)?
- Diferenças entre `lambda` e funções tradicionais
- Sintaxe de uma função lambda
- Exemplos práticos:
  - Usando `lambda` com `map()` e `filter()`
  - Ordenação com base em funções lambda

------

## **7. Documentação de Funções**

- Importância de documentar funções
- Docstrings em Python:
  - Convenção de uso
  - Exemplos de boas práticas
- Como utilizar ferramentas como `help()` para exibir a documentação

------

## **8. Debugging em Funções**

- Erros comuns em funções:
  - Falta de retorno
  - Argumentos em ordem errada
  - Modificação inesperada de variáveis globais
- Técnicas de depuração:
  - Uso de `print()`
  - Uso de depuradores como o disponível no VS Code ou PyCharm

------

## **9. Práticas Avançadas com Funções**

- Recursão:
  - O que é e como funciona
  - Exemplos clássicos, como cálculo de fatorial e sequência de Fibonacci
- Funções como objetos de primeira classe:
  - Passar funções como argumentos
  - Retornar funções de outras funções
- Decoração de funções (decorators):
  - Introdução e casos de uso
  - Exemplos simples e práticos

------

## **10. Projetos Práticos com Funções**

- Criando um sistema de cálculo:
  - Soma, subtração, multiplicação e divisão
  - Validação de entradas
- Gerador de senhas automáticas
- Simulação de dados com funções e randomização
- Análise de dados:
  - Média, mediana e moda de listas
  - Contagem de palavras em textos

------

## **11. Conclusão e Próximos Passos**

- Recapitulação dos tópicos estudados
- Importância das funções na programação modular
- Sugestões de estudos futuros:
  - Orientação a Objetos (Classes e Métodos)
  - Bibliotecas populares como NumPy, pandas e matplotlib