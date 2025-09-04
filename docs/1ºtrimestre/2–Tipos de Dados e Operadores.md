# 🟨 **Capítulo 2 – Tipos de Dados e Operadores**

# 🧮 Capítulo 2.1 – Trabalhar com Tipos Numéricos e Operadores

> ✨ _“A base da computação é a manipulação de dados. E entre os dados, os números são os mais usados para expressar lógica, cálculo e decisão.”_

---

## 📘 O que são Tipos Numéricos?

Em Python, números são classificados em três tipos principais:

| Tipo      | Descrição                    | Exemplo         |
| --------- | ---------------------------- | --------------- |
| `int`     | Números inteiros             | `10`, `-3`, `0` |
| `float`   | Números com ponto flutuante  | `3.14`, `-0.5`  |
| `complex` | Números com parte imaginária | `3 + 2j`        |

---

## 🔢 2.1.1 Tipo `int` – Inteiros

Representa números **sem casas decimais**. Usado em contagens, idade, ano, quantidade etc.

```python
alunos = 32
ano = 2025
saldo = -100
print(alunos, ano, saldo)
```

🔎 **Comentando:**

- A variável `alunos` recebe um número inteiro.
- O Python aceita inteiros positivos e negativos.
- O comando `print()` exibe os valores na tela.

---

## 🔡 2.1.2 Tipo `float` – Decimais

Representa números com **casas decimais**. Usado para médias, notas, pesos, distâncias etc.

```python
nota = 7.5
altura = 1.72
media = (6.0 + nota) / 2
print("Média:", media)
```

🔎 **Observação importante:**

- Em Python, o separador decimal é o **ponto (`.`)**, nunca a vírgula.

---

## 🔮 2.1.3 Tipo `complex` – Números Complexos

Contêm **parte real e imaginária**, raramente usado no dia a dia da programação básica.

```python
z = 3 + 2j
print("Parte real:", z.real)
print("Parte imaginária:", z.imag)
```

---

## ➕ 2.1.4 Operadores Aritméticos

Permitem realizar cálculos matemáticos:

| Operador | Significado      | Exemplo  | Resultado |
| -------- | ---------------- | -------- | --------- |
| `+`      | Adição           | `5 + 3`  | `8`       |
| `-`      | Subtração        | `9 - 2`  | `7`       |
| `*`      | Multiplicação    | `4 * 2`  | `8`       |
| `/`      | Divisão real     | `7 / 2`  | `3.5`     |
| `//`     | Divisão inteira  | `7 // 2` | `3`       |
| `%`      | Resto da divisão | `7 % 2`  | `1`       |
| `**`     | Potência         | `2 ** 3` | `8`       |

```python
a = 10
b = 3
print("Soma:", a + b)
print("Divisão real:", a / b)
print("Divisão inteira:", a // b)
print("Resto:", a % b)
print("Potência:", a ** 2)
```

---

## 🧮 2.1.5 Precedência de Operadores

A ordem de execução dos operadores segue a lógica matemática:

1. `()` → Parênteses
2. `**` → Potência
3. `*`, `/`, `//`, `%` → Multiplicações e divisões
4. `+`, `-` → Adições e subtrações

```python
resultado = 2 + 3 * 4
print(resultado)  # Resultado: 14

resultado = (2 + 3) * 4
print(resultado)  # Resultado: 20
```

---

## 🔄 2.1.6 Conversão entre Tipos

Em muitos casos, você vai querer converter entre `int`, `float` e `str`.

```python
idade_texto = "17"
idade_num = int(idade_texto)
print("Ano que vem:", idade_num + 1)
```

### Funções úteis:

| Função         | O que faz                    |
| -------------- | ---------------------------- |
| `int("10")`    | Converte string para inteiro |
| `float("7.5")` | Converte string para decimal |
| `str(30)`      | Converte número para texto   |

---

## ✅ Boas Práticas

| Dica                                  | Por que aplicar?                                       |
| ------------------------------------- | ------------------------------------------------------ |
| Usar tipo adequado para o contexto    | Evita erros em cálculos ou arredondamentos indesejados |
| Usar `//` se quiser um número inteiro | Evita casas decimais desnecessárias                    |
| Comentar contas complexas             | Ajuda a revisar e depurar o raciocínio                 |
| Validar entradas do usuário           | Garante que o valor possa ser usado em cálculos        |

---

## 🧠 Desafio guiado com comentários

```python
# Programa: Calcular a média de duas notas
print("=== Cálculo de Média ===")

n1 = float(input("Digite a primeira nota: "))
n2 = float(input("Digite a segunda nota: "))

media = (n1 + n2) / 2

print("A média final é:", media)
```

---

## 🔍 Exercícios Propostos

1. 🧠 Peça ao usuário dois números e mostre:
   - Soma
   - Subtração
   - Produto
   - Divisão real e divisão inteira
2. 🧾 Solicite o valor de um produto e mostre:
   - Preço com 10% de desconto
   - Preço com 8% de imposto
3. 📐 Receba o lado de um quadrado e mostre sua área e perímetro.
4. 💸 Peça o valor de um salário e mostre:
   - Reajuste de 12%
   - Salário final
5. 🔁 Converta uma temperatura digitada em Celsius para Fahrenheit.

---

## 🔗 Referências

- [Documentação oficial – Tipos Numéricos](https://docs.python.org/pt-br/3/library/numbers.html)
- [Curso em Vídeo – Operadores Aritméticos](https://www.youtube.com/watch?v=RYnZzvWx7WU)
- [Python Brasil – Tipos de Dados Numéricos](https://wiki.python.org.br/TiposDeDados)

---

# 🔢 Capítulo 2.2 – Funções Matemáticas e Operações Avançadas

> ✨ _“Matemática sem função é como código sem lógica. Neste capítulo, você aprenderá a usar o poder das funções matemáticas em Python para resolver problemas do mundo real.”_

---

## 🧠 2.2.1 Por que usar funções matemáticas?

Funções matemáticas são **ferramentas prontas** do Python que ajudam a:

- Realizar cálculos com mais precisão
- Reaproveitar código
- Evitar reinvenção da roda

---

## 🛠️ 2.2.2 Funções matemáticas internas (built-in)

Essas funções já estão disponíveis no Python **sem precisar importar nada**:

| Função       | Descrição                      | Exemplo        | Resultado |
| ------------ | ------------------------------ | -------------- | --------- |
| `abs(x)`     | Valor absoluto                 | `abs(-8)`      | `8`       |
| `round(x)`   | Arredonda número               | `round(3.6)`   | `4`       |
| `pow(x, y)`  | Potência: x elevado a y        | `pow(2, 3)`    | `8`       |
| `sum(lista)` | Soma os elementos de uma lista | `sum([1,2,3])` | `6`       |
| `max(...)`   | Retorna o maior valor          | `max(5, 8, 1)` | `8`       |
| `min(...)`   | Retorna o menor valor          | `min(5, 8, 1)` | `1`       |

```python
numeros = [3, 7, -2, 8]
print("Soma:", sum(numeros))
print("Maior:", max(numeros))
print("Menor:", min(numeros))
print("Valor absoluto do menor:", abs(min(numeros)))
```

---

## 📦 2.2.3 Módulo `math`: mais poder para cálculos

Para cálculos mais avançados, usamos o módulo `math`:

```python
import math
```

### Principais funções do módulo `math`

| Função            | Descrição                       | Exemplo                              |
| ----------------- | ------------------------------- | ------------------------------------ |
| `math.sqrt(x)`    | Raiz quadrada                   | `math.sqrt(25)` → `5.0`              |
| `math.pow(x, y)`  | Potência                        | `math.pow(2, 4)` → `16`              |
| `math.pi`         | Valor de π (~3.14159)           | `math.pi`                            |
| `math.exp(x)`     | Exponencial (eˣ)                | `math.exp(1)`                        |
| `math.log10(x)`   | Logaritmo na base 10            | `math.log10(100)` → `2`              |
| `math.radians(x)` | Converte graus para radianos    | `math.radians(180)` → `3.14`         |
| `math.sin(x)`     | Seno de um ângulo (em radianos) | `math.sin(math.radians(30))` → `0.5` |

```python
import math

print("Raiz quadrada de 144:", math.sqrt(144))
print("PI:", math.pi)
print("Seno de 30 graus:", math.sin(math.radians(30)))
```

---

## 🔁 2.2.4 Conversões entre tipos

Muito útil quando se trabalha com entrada de dados e cálculos.

```python
nota1 = float(input("Digite a nota 1: "))
nota2 = float(input("Digite a nota 2: "))
media = (nota1 + nota2) / 2
print("Média:", round(media, 1))
```

| Conversão      | Uso                         |
| -------------- | --------------------------- |
| `int(valor)`   | Para converter para inteiro |
| `float(valor)` | Para decimal                |
| `str(valor)`   | Para texto                  |

---

## 🧠 2.2.5 Exemplos aplicados no cotidiano

### ✅ Exemplo 1 – Cálculo de desconto

```python
valor = float(input("Valor do produto: R$ "))
desconto = valor * 0.10
preco_final = valor - desconto
print(f"Desconto de R$ {desconto:.2f}")
print(f"Preço com desconto: R$ {preco_final:.2f}")
```

---

### ✅ Exemplo 2 – Área de um círculo

```python
import math

raio = float(input("Digite o raio: "))
area = math.pi * (raio ** 2)
print(f"Área do círculo: {area:.2f}")
```

---

### ✅ Exemplo 3 – Tempo de viagem

```python
distancia = float(input("Distância em km: "))
velocidade = float(input("Velocidade média km/h: "))
tempo = distancia / velocidade
print(f"Tempo estimado: {round(tempo, 2)} horas")
```

---

## 🧠 Desafio Guiado

**Crie um programa que calcule a raiz quadrada da média entre três notas.**

```python
import math

n1 = float(input("Nota 1: "))
n2 = float(input("Nota 2: "))
n3 = float(input("Nota 3: "))

media = (n1 + n2 + n3) / 3
raiz = math.sqrt(media)

print(f"A raiz quadrada da média é: {raiz:.2f}")
```

---

## 📘 Exercícios Recomendados

1. 🧮 Crie uma calculadora simples que recebe dois números e um operador (`+`, `-`, `*`, `/`) do usuário.
2. 📐 Peça o raio de uma circunferência e mostre a área.
3. 🔢 Solicite um número inteiro e exiba seu quadrado, cubo e raiz quadrada.
4. 📊 Receba quatro notas, calcule a média e informe se o aluno foi aprovado (≥ 6).
5. 💰 Calcule o montante de um investimento com juros compostos (`M = C * (1+i)^t`).

---

## ✅ Boas práticas

| Prática                      | Por quê aplicar?           |
| ---------------------------- | -------------------------- |
| Comentar fórmulas            | Torna o raciocínio claro   |
| Importar módulos no início   | Boa organização            |
| Arredondar valores com `.2f` | Melhor apresentação visual |
| Validar entrada do usuário   | Evita travamentos e erros  |

---

## 🔗 Referências

- [Documentação do módulo `math`](https://docs.python.org/pt-br/3/library/math.html)
- [Curso em Vídeo – Módulo Matemático](https://www.youtube.com/watch?v=qS_Y3pUq5ZU)
- [Python Brasil – Módulo math](https://wiki.python.org.br/ModulosEmbutidos#math)

---
