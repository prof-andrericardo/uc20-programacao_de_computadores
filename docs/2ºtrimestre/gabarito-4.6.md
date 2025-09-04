# 📝 Gabarito – Avaliação do Capítulo 4

------

## 📘 Parte 1 – Avaliação Teórica (Múltipla escolha)

------

### **1. Qual das opções cria uma tupla válida com um único item?**

**Resposta correta:** b) `(10,)`

🔎 *Justificativa:* Tuplas unitárias **exigem a vírgula** para diferenciar de um número entre parênteses.

------

### **2. O método `.append()` serve para:**

**Resposta correta:** c) Adicionar um item ao final da lista

🔎 *Justificativa:* `.append()` é o método padrão para adicionar **um único elemento** ao final de uma lista.

------

### **3. Em `lista[::2]`, o que significa o `2`?**

**Resposta correta:** b) Saltar de 2 em 2

🔎 *Justificativa:* No fatiamento `[início:fim:passo]`, o terceiro elemento define o **intervalo entre os índices acessados**.

------

## 💻 Parte 2 – Avaliação Prática (Modelos esperados)

------

### **Exercício 1 – Controle de alunos**

```python
alunos = []

for i in range(5):
    nome = input(f"Nome do aluno {i+1}: ")
    alunos.append(nome)

print("\nAlunos cadastrados:")
for i, nome in enumerate(alunos):
    print(f"{i + 1}) {nome}")

remover = input("\nDigite o nome a remover: ")
if remover in alunos:
    alunos.remove(remover)
    print(f"{remover} removido com sucesso.")
else:
    print("Nome não encontrado.")
```

------

### **Exercício 2 – Média com lista**

```python
notas = []

for i in range(4):
    nota = float(input(f"Nota {i+1}: "))
    notas.append(nota)

media = sum(notas) / len(notas)
print(f"\nMédia: {media:.2f}")
print(f"Maior nota: {max(notas)}")
print(f"Menor nota: {min(notas)}")
```

------

### **Exercício 3 – Matriz 3x3**

```python
matriz = []

for i in range(3):
    linha = []
    for j in range(3):
        valor = int(input(f"Valor [{i}][{j}]: "))
        linha.append(valor)
    matriz.append(linha)

soma = 0
for linha in matriz:
    soma += sum(linha)

print("\nMatriz:")
for linha in matriz:
    print(linha)

print("Soma total:", soma)

# Diagonal principal
soma_diag = sum(matriz[i][i] for i in range(3))
print("Soma da diagonal principal:", soma_diag)
```

------

### **Exercício 4 – Função com retorno em tupla**

```python
def operacoes(a, b):
    return a + b, a - b, a * b

soma, subtracao, produto = operacoes(10, 5)
print(f"Soma: {soma}, Subtração: {subtracao}, Produto: {produto}")
```

------

### 🧠 **Desafio Final – Sistema de lançamento**

```python
alunos = []
notas = []

for i in range(3):
    nome = input(f"Nome do aluno {i+1}: ")
    alunos.append(nome)
    
    linha_notas = []
    for j in range(3):
        nota = float(input(f"Nota {j+1} de {nome}: "))
        linha_notas.append(nota)
    notas.append(linha_notas)

print("\n📊 Relatório de Notas:")
for i, aluno in enumerate(alunos):
    media = sum(notas[i]) / len(notas[i])
    print(f"{aluno}: notas = {notas[i]}, média = {media:.2f}")
```

------

---

------

### 📄 Gabarito Oficial – Avaliação do Capítulo 4: Estruturas de Dados Simples

------

## ✅ Parte 1 – Questões Teóricas (Múltipla Escolha)

------

### **1. Qual das opções cria uma tupla válida com um único item?**

a) `(10)`
 b) `(10,)` ✅
 c) `[10]`
 d) `tuple[10]`

**✔ Resposta correta:** b) `(10,)`

> 📌 *Comentário:* Em Python, para criar uma **tupla unitária**, a vírgula é obrigatória. Caso contrário, `(10)` será interpretado apenas como o número 10 entre parênteses.

------

### **2. O método `.append()` serve para:**

a) Remover o último elemento da lista
 b) Ordenar a lista
 c) Adicionar um item ao final da lista ✅
 d) Criar uma cópia da lista

**✔ Resposta correta:** c)

> 📌 *Comentário:* O método `.append()` adiciona **um único item ao final da lista**, expandindo seu tamanho em 1.

------

### **3. Em `lista[::2]`, o que significa o `2`?**

a) Começar do índice 2
 b) Saltar de 2 em 2 ✅
 c) Inverter a lista
 d) Limitar a dois elementos

**✔ Resposta correta:** b)

> 📌 *Comentário:* No fatiamento `[início:fim:passo]`, o `passo` define **quantos índices pular** a cada iteração. Com `2`, ele percorre a lista pulando 1 elemento a cada passo.

------

## 💻 Parte 2 – Questões Práticas

> 🧠 *Objetivo: Avaliar a habilidade do aluno em construir, manipular e exibir dados armazenados em listas, tuplas e listas aninhadas.*

------

### **Exercício 1 – Controle de Alunos**

**Enunciado:**

- Peça o nome de 5 alunos usando `input()`
- Armazene os nomes em uma lista
- Exiba a lista com numeração
- Permita remover um nome informado pelo usuário

**Modelo de Resolução:**

```python
alunos = []

# Entrada de dados
for i in range(5):
    nome = input(f"Nome do aluno {i+1}: ")
    alunos.append(nome)

# Listagem com numeração
print("\n📋 Lista de alunos:")
for i, nome in enumerate(alunos):
    print(f"{i + 1}. {nome}")

# Remoção
remover = input("\nDigite o nome a remover: ")
if remover in alunos:
    alunos.remove(remover)
    print(f"{remover} foi removido.")
else:
    print("Nome não encontrado.")
```

------

### **Exercício 2 – Cálculo de Média**

**Enunciado:**

- Peça 4 notas e armazene em uma lista
- Calcule a média, maior e menor nota

**Modelo de Resolução:**

```python
notas = []

for i in range(4):
    nota = float(input(f"Nota {i+1}: "))
    notas.append(nota)

media = sum(notas) / len(notas)
print(f"\nMédia: {media:.2f}")
print("Maior nota:", max(notas))
print("Menor nota:", min(notas))
```

------

### **Exercício 3 – Matriz 3x3 e Soma da Diagonal**

**Enunciado:**

- Monte uma matriz 3x3 com `input()`
- Exiba a matriz formatada
- Calcule a soma total e a da diagonal principal

**Modelo de Resolução:**

```python
matriz = []

for i in range(3):
    linha = []
    for j in range(3):
        valor = int(input(f"Valor [{i}][{j}]: "))
        linha.append(valor)
    matriz.append(linha)

# Exibição da matriz
print("\n📊 Matriz:")
for linha in matriz:
    print(linha)

# Soma total
soma_total = sum(sum(linha) for linha in matriz)
print("Soma total:", soma_total)

# Soma da diagonal
soma_diag = sum(matriz[i][i] for i in range(3))
print("Soma da diagonal principal:", soma_diag)
```

------

### **Exercício 4 – Retorno com Tupla**

**Enunciado:**

- Crie uma função que receba 2 números
- Retorne: soma, subtração e multiplicação em uma tupla
- Faça o desempacotamento

**Modelo de Resolução:**

```python
def operacoes(a, b):
    return a + b, a - b, a * b

s, sub, mult = operacoes(8, 3)

print("Soma:", s)
print("Subtração:", sub)
print("Multiplicação:", mult)
```

------

### **Desafio Final – Sistema de Lançamento de Alunos e Notas**

**Enunciado:**

- Armazene nomes de alunos em uma lista
- Para cada aluno, armazene 3 notas em uma lista aninhada
- Calcule e mostre a média de cada aluno

**Modelo de Resolução:**

```python
alunos = []
notas = []

for i in range(3):
    nome = input(f"Nome do aluno {i+1}: ")
    alunos.append(nome)

    linha_notas = []
    for j in range(3):
        nota = float(input(f"Nota {j+1} de {nome}: "))
        linha_notas.append(nota)
    notas.append(linha_notas)

print("\n📈 Relatório Final:")
for i in range(len(alunos)):
    media = sum(notas[i]) / len(notas[i])
    print(f"{alunos[i]} → Notas: {notas[i]} | Média: {media:.2f}")
```

------

