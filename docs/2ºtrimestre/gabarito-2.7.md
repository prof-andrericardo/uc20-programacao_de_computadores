# 📝 Gabarito – Avaliação do Módulo 2

------

## 📘 Parte 1 – Avaliação Teórica

### 🔢 Múltipla Escolha

1. **b) `round(3.7)`**
    🔎 A função `round()` arredonda o número para o inteiro mais próximo → `4`
2. **b) `False`**
    🔎 Uma string vazia `""` é considerada `False` em contexto booleano (`bool("") → False`)
3. **b) `.split(",")`**
    🔎 A função `split()` divide a string com base no separador fornecido (vírgula neste caso)
4. **c) `Nada definido`**
    🔎 `None` representa a **ausência de valor** em Python, e não deve ser confundido com zero, `False` ou string vazia
5. **b) Pelo menos um lado for `True`**
    🔎 O operador `or` retorna `True` se **qualquer um** dos operandos for verdadeiro

------

## 💻 Parte 2 – Avaliação Prática

### ✅ Soluções esperadas (modelos simplificados)

1. **Calculadora de IMC**

```python
peso = float(input("Peso em kg: "))
altura = float(input("Altura em metros: "))
imc = peso / (altura ** 2)

if imc < 18.5:
    print("Abaixo do peso")
elif imc < 25:
    print("Peso normal")
elif imc < 30:
    print("Sobrepeso")
else:
    print("Obesidade")
```

------

1. **Validador de e-mail (regex)**

```python
import re

email = input("Digite seu e-mail: ")
padrao = r"^[\w\.-]+@[\w\.-]+\.\w{2,}$"

if re.fullmatch(padrao, email):
    print("E-mail válido")
else:
    print("E-mail inválido")
```

------

1. **Filtro de nomes com mais de 5 letras**

```python
entrada = input("Digite nomes separados por vírgula: ")
nomes = entrada.split(",")

filtrados = [n.strip().title() for n in nomes if len(n.strip()) > 5]
print("Nomes com mais de 5 letras:", filtrados)
```

------

1. **Verificador de acesso**

```python
usuario = input("Usuário: ")
senha = input("Senha: ")

if usuario == "admin" and senha == "1234":
    print("Acesso liberado")
else:
    print("Acesso negado")
```

------

1. **Validação de idade**

```python
idade = int(input("Digite sua idade: "))

if idade < 18:
    print("Menor de idade")
elif idade < 60:
    print("Adulto")
else:
    print("Idoso")
```

------

## ⭐ Desafio Bônus

```python
import re

cpf = input("Digite seu CPF (xxx.xxx.xxx-xx): ")
padrao = r"^\d{3}\.\d{3}\.\d{3}-\d{2}$"

if re.fullmatch(padrao, cpf):
    nome = input("Digite seu nome completo: ")
    nome_formatado = " ".join(n.strip().capitalize() for n in nome.split())
    print("Cadastro finalizado para:", nome_formatado)
else:
    print("CPF inválido.")
```

------

