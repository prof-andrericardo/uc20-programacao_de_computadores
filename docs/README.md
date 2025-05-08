# 📘 **Sumário Geral – UC20: Programação de Computadores**

------

## 🔵 **Capítulo 0 – Introdução e Ambiente de Desenvolvimento**

> *Conhecer o terreno antes de começar a programar é essencial para não se perder no caminho.*

### 0.1 Entender o que é Python

- História e evolução da linguagem
- Vantagens e aplicações reais

### 0.2 Instalar o Python

- Instalação no Windows
- Instalação no Linux (Zorin, Ubuntu, Mint)
  - Instalação do pacote `python-is-python3`
  - Verificação dos comandos `python` e `python3`
- Introdução ao VSCode como editor padrão
- Testar ambiente com arquivo `.py`

### 0.3 Executar o primeiro programa

- Criar e salvar scripts `.py`
- Usar o terminal interativo e arquivos
- Diferença entre terminal, console e editor de código

------

## 🟩 **Capítulo 1 – Fundamentos da Linguagem Python**

> *Toda construção sólida começa com uma boa fundação.*

### 1.1 Utilizar a função `print()`

- Exibir textos e variáveis
- Concatenação com `+`, `,` e `f-strings`
- Caracteres de escape (`\n`, `\t`, `\\`)
- Parâmetros `end` e `sep`

### 1.2 Utilizar a função `input()`

- Receber dados do usuário
- Entender que tudo vem como texto (`str`)
- Converter tipos: `int()`, `float()`
- Validar e tratar entradas com `try/except`
- Usar `.split()` para múltiplos dados
- Oferecer valores padrão
- Aplicar boas práticas de entrada de dados

------

## 🟨 **Capítulo 2 – Tipos de Dados e Operadores**

> *Manipular os dados corretamente é o segredo de um programa funcional.*

### 2.1 Trabalhar com tipos numéricos e operadores

- Tipos `int`, `float` e `complex`
- Atribuição e declaração de variáveis numéricas
- Operadores aritméticos: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- Precedência de operadores
- Conversão básica entre tipos
- Exemplos práticos comentados

### 2.2 Usar funções matemáticas e operações avançadas

- Funções embutidas: `abs()`, `round()`, `pow()`, `sum()`, `max()`, `min()`
- Conversão entre tipos com `int()`, `float()`, `str()`
- Introdução ao módulo `math`
- Raiz quadrada, seno, logaritmo, exponencial
- Problemas do cotidiano com cálculos matemáticos
- Exercícios práticos e contextualizados

### 2.3 Manipular textos (fundamentos de strings)

- Criação de strings com aspas
- Fatiamento e indexação
- Concatenação e repetição
- Caracteres de escape
- Principais métodos de transformação e busca
- F-strings e formatação
- Exercícios básicos com strings

### 2.4 Transformar e normalizar strings com eficiência

- Uso intensivo de `replace()`, `strip()`, `split()`, `join()`
- Limpeza de entradas (acentos, espaços, caixa alta/baixa)
- List comprehension com strings
- Aplicação de `map()` e `filter()` em textos
- Conversão entre listas e strings
- Casos práticos: nomes, senhas, padronização de formulários

### 2.5 Validar textos com expressões regulares

- Introdução aprofundada: o que são expressões regulares e para que servem
- Sintaxe básica: metacaracteres e padrões comuns
- Validação com `re.match()`, `re.search()` e `re.fullmatch()`
- Busca e substituição com `re.findall()` e `re.sub()`
- Expressões para e-mail, CPF, telefones, datas, senhas
- Desafios e exercícios comentados com explicação do padrão

### 2.6 Trabalhar com valores booleanos, operadores lógicos e o uso de `None`

- Tipo `bool` e valores `True` e `False`
- Operadores de comparação: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Conversão implícita com `bool()`
- Operadores lógicos: `and`, `or`, `not`
- Precedência lógica e uso com parênteses
- O valor especial `None` e comparações com `is` e `is not`
- Aplicações práticas com validações, login, campos opcionais
- Boas práticas e exercícios guiados

### 2.7 Conclusão e Avaliação do Módulo 2

- Recapitulação dos conceitos principais (números, strings, booleanos, regex)
- Avaliação teórica: múltipla escolha com foco conceitual
- Avaliação prática: pequenos programas com validações e lógica
- Desafio bônus: integração de tipos de dados com lógica condicional
- Recomendações para aprofundamento e continuidade

------

## 🟦 **Capítulo 3 – Estruturas de Controle de Fluxo**

> *Quando o código aprende a decidir e repetir, nasce a lógica de programação de verdade.*

### 3.1 Estruturas Condicionais com `if`, `elif`, `else`
- Conceito de condição lógica e decisão
- Sintaxe e indentação obrigatória
- Uso de `if`, `elif`, `else` com explicações linha por linha
- Comparações com strings e números
- Composição de condições com `and`, `or`, `not`
- Estruturas aninhadas e validações encadeadas
- Boas práticas e exercícios aplicados

### 3.2 Estrutura Condicional com `match/case` (Python 3.10+)
- Introdução e contexto do `match`
- Sintaxe completa e uso com `case _`
- Comparação com `if/elif`
- Agrupamento de casos com `|`
- Combinação com `.lower()`, `break`, entradas de menu
- Casos práticos e exercícios temáticos

### 3.3 Estrutura de Repetição com `while`
- Conceito de repetição condicionada
- Sintaxe, uso e exemplos passo a passo
- Cuidado com laços infinitos
- Uso de `break`, `continue`, controle com `bool`
- Simulação de login, menus interativos e contadores
- Exercícios guiados e aplicação real

### 3.4 Estrutura de Repetição com `for`: Fundamentos
- Conceito de iteração controlada por `range()`
- Variações de `range()`: início, fim, passo
- Contadores crescentes e decrescentes
- Repetições aritméticas, tabelas, gráficos e somatórios
- Exercícios com lógica aplicada

### 3.5 Recursos Avançados com `for`: `enumerate()`, `zip()`, `break`, `continue`
- Uso de `enumerate()` com menus e tabelas numeradas
- Combinação de listas com `zip()`
- Controle de fluxo com `break` e `continue`
- Casos práticos com interação simulada e entradas paralelas
- Boas práticas e exercícios criativos

### 3.6 Tratamento de Exceções com `try/except`
- Compreensão de erros em tempo de execução
- Uso de blocos `try`, `except`, `else` e `finally`
- Tipos de exceções mais comuns: `ValueError`, `ZeroDivisionError`, etc.
- Validação de entrada com tratamento de erro
- Exemplos práticos com loops e estruturas condicionais
- Integração com lógica de controle de fluxo

### 3.7 Conclusão e Avaliação do Capítulo 3
- Revisão dos conceitos de decisão e repetição
- Comparação entre `if`, `match`, `while` e `for`
- Avaliação teórica e prática
- Desafio integrador com lógica condicional, repetição e tratamento de exceções
- Reforço das boas práticas aprendidas

------

## 🟧 **Capítulo 4 – Estruturas de Dados Simples**

> *Organizar e manipular coleções de valores é essencial para qualquer aplicação prática.*

### 4.1 Introdução às listas
- Criação de listas e tipos mistos
- Acesso a elementos por índice positivo e negativo
- Modificação de valores e substituições
- Adição de elementos com `append()`, `insert()`
- Remoção com `del`, `remove()`, `pop()`
- Verificação de tamanho com `len()`

### 4.2 Métodos, fatiamento e boas práticas com listas
- Métodos úteis: `append()`, `insert()`, `remove()`, `pop()`, `sort()`, `reverse()`, `clear()`
- Fatiamento com `[:]`, intervalos, saltos negativos
- Conversão de outros tipos para lista com `list()`
- Cópia segura com `copy()`
- Boas práticas para organização e clareza no uso de listas

### 4.3 Iteração sobre listas com `for` e `while`, e operadores `in` e `not in`
- Uso de `for` simples para percorrer listas
- Uso de `range()` com listas
- Controle por `while` com índice manual
- Verificação de presença com `in` e `not in`
- Contadores, somatórios e buscas em listas

### 4.4 Listas aninhadas e estruturas em tabela com `zip()`
- Criação de listas dentro de listas (listas bidimensionais)
- Acesso por coordenadas [linha][coluna]
- Iteração com `for` aninhado
- Exibição formatada de tabelas
- Combinação de linhas com `zip()` para exibição paralela

### 4.5 Tuplas: segurança e imutabilidade
- Diferença entre listas e tuplas
- Criação de tuplas com e sem parênteses
- Acesso por índice e iteração
- Usos comuns: valores fixos, retorno múltiplo
- Conversão com `tuple()` e desempacotamento

### 4.6 Conclusão e Avaliação do Capítulo 4
- Revisão dos principais conceitos: listas, métodos, tuplas e listas aninhadas
- Exercícios práticos e teóricos com manipulação de dados
- Desafio de modelagem com listas de alunos e notas

---

## 🟦 **Capítulo 5 – Funções em Python**

> *Funções tornam seu código reutilizável, modular e mais bonito.*

### 5.1 Introdução às Funções

- O que são funções e por que usá-las
- Sintaxe básica com `def`, parâmetros e `return`
- Diferença entre `print()` e `return`
- Boas práticas de nomeação e organização
- Exercícios e desafios guiados

### 5.2 Parâmetros, Argumentos e Escopo

- Diferença entre parâmetros e argumentos
- Argumentos posicionais, nomeados e com valor padrão
- Uso de `*args` e `**kwargs`
- Escopo local e global de variáveis
- Uso da palavra-chave `global`
- Boas práticas com escopo e entrada de dados em funções
- Exercícios comentados e contextualizados

### 5.3 Funções com Múltiplos Retornos e Desempacotamento

- Retornando múltiplos valores com tuplas
- Desempacotamento de retornos em variáveis
- Retornos estruturados: listas e dicionários
- Boas práticas para múltiplos retornos
- Exercícios aplicados e desafios

### 5.4 Escopo, Variáveis Locais e Globais (Exemplos Avançados)

- Revisão e aprofundamento de escopo
- Variáveis mutáveis e imutáveis no contexto global
- Uso de `global` e seus riscos
- Alternativas com retorno e boas práticas
- Exercícios explicativos e comparativos

### 5.5 Documentação de Funções e Docstrings

- O que são docstrings e por que usá-las
- Estrutura de documentação de função
- Como acessar documentação com `help()`
- Exemplo de documentação real com parâmetros e retorno
- Exercícios com escrita de docstrings claras e objetivas

### 5.6 Funções Lambda (Funções Anônimas)

- Conceito de função anônima
- Sintaxe completa e estrutura com exemplos
- Diferença entre `def` e `lambda`
- Uso com `map`, `filter`, `sorted`, `apply`
- Boas práticas e limitações
- Exercícios e desafios contextualizados

### 5.7 Funções Recursivas

- Definição e estrutura básica de recursão
- Exemplo do fatorial explicado passo a passo
- Comparativo com laço (iterativo vs recursivo)
- Casos práticos e aplicações reais
- Cuidados com recursão infinita e performance
- Boas práticas e exercícios guiados

---

## 🟥 **Capítulo 6 – Interfaces Gráficas com PyQt**

> *Dar vida ao seu programa com interfaces visuais elegantes é transformar código em experiência de usuário.*

### 6.1 Introdução ao PyQt e ao modelo de janelas
- O que é PyQt e por que usar
- Diferenças entre PyQt5 e PyQt6
- Instalação do PyQt com `pip`
- Conceitos: QApplication, QWidget, loop de eventos

### 6.2 Criando janelas e widgets básicos
- Primeira janela com PyQt
- Widgets essenciais: `QLabel`, `QPushButton`, `QLineEdit`
- Criação de layouts com `QVBoxLayout`, `QHBoxLayout` e `QGridLayout`
- Agrupando elementos com `QGroupBox` e `QFrame`

### 6.3 Eventos, sinais e slots
- O que são sinais (`signals`) e slots
- Conectando ações a funções com `.connect()`
- Coletando dados de entrada
- Atualizando elementos da interface dinamicamente

### 6.4 Personalização visual com CSS (Qt Style Sheets)
- Aplicando estilos com `.setStyleSheet()`
- Alterando cores, fontes e tamanhos
- Estilizando botões, caixas de texto e janelas

### 6.5 Organização em classes e separação de lógica
- Estrutura de projeto com classes: GUI + lógica
- Criação de métodos internos para interações
- Boas práticas para organização e manutenção do código

### 6.6 Diálogos, mensagens e caixas de alerta
- `QMessageBox`: mensagens de aviso, erro e confirmação
- Diálogos de entrada: `QInputDialog`, `QFileDialog`
- Interação guiada com o usuário

### 6.7 Avaliação e Projeto Final com PyQt
- Projeto prático: calculadora, agenda, ou gerador de senhas
- Avaliação prática com foco em:
  - Organização de código
  - Uso correto de widgets
  - Estética e usabilidade
- Dicas para ir além: PyQt Designer, sinais customizados e deploy

------

## 🔗 **Referências e Materiais de Apoio**

### 📘 Documentação Oficial
- [Documentação do Python (pt-br)](https://docs.python.org/pt-br/)
- [Documentação da biblioteca `re` – Expressões Regulares](https://docs.python.org/pt-br/3/library/re.html)
- [Documentação oficial do PyQt6](https://doc.qt.io/qtforpython/)

### 🎥 Cursos e Vídeos Didáticos
- [Curso em Vídeo – Python (Gustavo Guanabara)](https://www.cursoemvideo.com/)
- [Python para Zumbis – Prof. Fernando Masanori](https://www.youtube.com/playlist?list=PLx4x_zx8csUj3IbPQ4_YDq3pK5zA1DzuP)
- [Curso de PyQt5 – Hashtag Programação (YouTube)](https://www.youtube.com/playlist?list=PLbIBj8vQhvm3TwmS6woDJhCWzZp1poaer)

### 🧠 Prática e Exercícios
- [Exercícios interativos em Python – Py.Dev](https://pydev.com.br/exercicios/)
- [Python Tutor (visualizador de código passo a passo)](https://pythontutor.com/)

---

