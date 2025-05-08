# 🧪 Atividade 03 – Controle de Fluxo (Nível Avançado)

📅 **Trimestre:** 1º  
📘 **Capítulo abordado:**  
- Capítulo 3 – Fluxos Avançados, `match/case` e Exceções

🎯 **Objetivo da Atividade:**
Aprofundar o controle de fluxo com `match/case`, estruturas aninhadas, integração com repetição e uso de tratamento de exceções com `try/except`.

---

## 🎯 Parte 1 – Uso de `match/case` (Python 3.10+)

### 1.1 Menu com `match`
Implemente um menu com as opções:
- 1: Ver nome do professor
- 2: Ver nome da turma
- 3: Ver dia da aula
- 0: Sair

Use `match/case` para tratar cada escolha.

### 1.2 Escolha de disciplina
Peça ao usuário a inicial da disciplina:
- `p`: Python
- `r`: Redes
- `b`: Banco de Dados
- Outra: "Opção inválida"

---

## 🧩 Parte 2 – Estruturas Aninhadas

### 2.1 Classificação com nota e presença
Peça nota e faltas. Aprovado se:
- Nota ≥ 7 **e** faltas ≤ 5
- Caso contrário, "Reprovado"

### 2.2 Sistema de login com tentativa e validação
Implemente um sistema de login:
- Usuário: `aluno`
- Senha: `uc20`
- Três tentativas permitidas

---

## 🔒 Parte 3 – Tratamento de Exceções

### 3.1 Divisão protegida
Peça dois números. Faça a divisão e:
- Trate `ZeroDivisionError`
- Trate `ValueError` para entrada inválida

### 3.2 Conversor de idade
Peça a idade. Converta para inteiro com `int()` e trate caso o usuário digite letras.

### 3.3 Somador de lista
Peça 5 números. Se algum for inválido, ignore com `try/except` e continue a soma.

---

## 🧠 Desafio Final – Simulador de Caixa Escolar

Implemente:

1. Saldo inicial: 100
2. Menu com opções:
   - 1: Depositar valor
   - 2: Sacar valor
   - 3: Ver saldo
   - 0: Sair
3. Trate exceções:
   - Saque maior que saldo
   - Entrada inválida

Use `while` com `match/case` e `try/except`.

---

## ✍️ Entrega

- Entregar o arquivo `simulador_caixa.py` e demais exercícios separados
- Comentar o código explicando os fluxos e exceções
- Prazo: até **[INSERIR DATA DE ENTREGA]**

---

🔗 *Complemento de estudo disponível no Google Classroom da UC20.*