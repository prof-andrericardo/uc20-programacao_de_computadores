# 🧪 Atividade 05 – Funções em Python (Nível Intermediário)

📅 **Trimestre:** 2º  
📘 **Capítulo abordado:**  
- Capítulo 5 – Funções com Listas, Validação e Parâmetros Dinâmicos

🎯 **Objetivo da Atividade:**
Aprofundar o uso de funções com estruturas como listas e strings, aplicar validação de dados, múltiplos retornos e parâmetros dinâmicos com `*args` e `**kwargs`.

---

## 🧪 Parte 1 – Funções com Listas

### 1.1 Quantos alunos passaram?
Crie uma função `contar_aprovados(lista)` que receba uma lista de médias e retorne quantos alunos têm média ≥ 7.

### 1.2 Maior e menor valor
Crie a função `extremos(lista)` que receba uma lista de números e retorne o menor e o maior valor.

### 1.3 Filtrar nomes por inicial
Crie uma função `filtrar_por_letra(nomes, letra)` que retorne apenas os nomes que começam com a letra dada (case insensitive).

---

## 🔍 Parte 2 – Validação e Estruturas

### 2.1 Validação de CPF
Crie uma função `validar_cpf(cpf)` que retorna True se o CPF estiver no formato `999.999.999-99` usando expressão regular (`re.fullmatch()`).

### 2.2 Cadastro com validação
Crie uma função `cadastrar_aluno()` que solicite nome e duas notas com `input()` e retorne os dados apenas se forem válidos.

### 2.3 Divisão segura
Crie uma função `dividir_seguro(a, b)` que trate divisão por zero com `try/except` e retorne o resultado ou uma mensagem de erro.

---

## 📦 Parte 3 – Retorno Múltiplo e Desempacotamento

### 3.1 Média e Situação
Crie `avaliar_aluno(n1, n2)` que retorna:
- A média
- A situação como texto: `"Aprovado"`, `"Recuperação"` ou `"Reprovado"`

### 3.2 Estatísticas de Lista
Função `estatisticas(lista)` que retorna: média, maior, menor e total de elementos.

---

## 🔄 Parte 4 – Parâmetros Dinâmicos

### 4.1 Soma com `*args`
Função `soma(*valores)` que recebe qualquer quantidade de números e retorna a soma total.

### 4.2 Montador de mensagem com `**kwargs`
Função `mensagem(**info)` que recebe qualquer quantidade de informações e imprime:
```bash
nome: João
idade: 17
turma: 3ºC
```

---

## 🧠 Desafio: Cadastro e Filtro com Funções

Crie um programa com as funções:

1. `cadastrar_alunos()` – cadastra n alunos com nome e média
2. `listar_alunos(lista)` – exibe todos com posição e média
3. `filtrar_aprovados(lista)` – exibe apenas os com média ≥ 7
4. `buscar_aluno(lista, nome)` – retorna dados do aluno pesquisado

Utilize funções pequenas, bem organizadas e modulares.

---

## ✍️ Entrega

- Subir os arquivos `.py` individualmente ou em uma pasta com nome padronizado
- Comentar as funções explicando cada lógica aplicada
- Prazo: até **[INSERIR DATA DE ENTREGA]**

---

🔗 *Complemento de estudo disponível no Google Classroom da UC20.*