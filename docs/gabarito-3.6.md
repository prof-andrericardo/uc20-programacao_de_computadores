# 📝 Gabarito – Avaliação do Capítulo 3

------

## 📘 Parte 1 – Avaliação Teórica

### Questão 1

**O que faz o comando `continue` dentro de um laço?**
 **Resposta correta:** c) Pula para a próxima iteração
 🧠 Justificativa: O `continue` encerra a iteração atual e retorna ao início do laço, **sem finalizar o loop**.

------

### Questão 2

**Qual alternativa representa corretamente o uso de `match/case`?**
 **Resposta correta:** c) `match valor:\n  case 1:`
 🧠 Justificativa: Essa é a **sintaxe correta em Python 3.10+**, com `match valor:` e blocos indentados para cada `case`.

------

### Questão 3

**Para exibir todos os números pares de 0 a 10, o `range()` ideal é:**
 **Resposta correta:** b) `range(0, 11, 2)`
 🧠 Justificativa: Começa em 0, vai até 10 (o 11 é exclusivo) e pula de 2 em 2, o que garante apenas os pares.

------

## 💻 Parte 2 – Avaliação Prática

### Exercício 1 – Login com senha e tentativas

```python
tentativas = 0

while tentativas < 3:
    usuario = input("Usuário: ")
    senha = input("Senha: ")

    if usuario == "admin" and senha == "1234":
        print("Login bem-sucedido")
        break
    else:
        print("Credenciais inválidas.")
        tentativas += 1

if tentativas == 3:
    print("Conta bloqueada.")
```

🧠 Justificativa: Controla o número de tentativas com `while` + `break`.

------

### Exercício 2 – Menu com opções numeradas (`enumerate()`)

```python
opcoes = ["Cadastrar", "Listar", "Sair"]

for i, opcao in enumerate(opcoes):
    print(f"{i + 1} - {opcao}")

escolha = int(input("Escolha uma opção: "))

match escolha:
    case 1:
        print("Cadastrando...")
    case 2:
        print("Listando dados...")
    case 3:
        print("Saindo do sistema.")
    case _:
        print("Opção inválida.")
```

------

### Exercício 3 – Tabuada com `for`

```python
n = int(input("Digite um número: "))

for i in range(1, 11):
    print(f"{n} x {i} = {n * i}")
```

------

### Exercício 4 – Contagem regressiva com `while`

```python
contador = 10

while contador > 0:
    print(contador)
    contador -= 1

print("Tempo esgotado!")
```

------

### Exercício 5 – `match/case` para faixa etária

```python
idade = int(input("Digite sua idade: "))

match idade:
    case idade if idade < 12:
        print("Criança")
    case idade if idade < 18:
        print("Adolescente")
    case idade if idade < 60:
        print("Adulto")
    case _:
        print("Idoso")
```

------

## ⭐ Desafio Final – `enumerate()` + `zip()` + `break`

```python
nomes = []
idades = []

while True:
    nome = input("Digite um nome (ou 'sair'): ")
    if nome.lower() == "sair":
        break
    idade = int(input("Digite a idade: "))
    nomes.append(nome)
    idades.append(idade)

print("\n📋 Lista de pessoas:")
for i, (nome, idade) in enumerate(zip(nomes, idades)):
    print(f"{i + 1}) {nome} – {idade} anos")
```

------

