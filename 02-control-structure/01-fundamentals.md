# **Estruturas de Controle em Python**

## **1. Fundamentos**

### **1.1 Introdução ao Tipo Booleano (`True`/`False`)**

Os tipos booleanos representam dois valores: verdadeiro (`True`) e falso (`False`). Eles são fundamentais na programação, pois permitem controlar o fluxo de execução do programa por meio de condições.

#### **Exemplo 1: Verificando o estado de conexão**

Imagine que você tem um dispositivo conectado a uma rede. Podemos usar um tipo booleano para representar o estado:

```python
conectado = True
if conectado:
    print("O dispositivo está conectado.")
else:
    print("O dispositivo não está conectado.")
```

- Aqui, a variável `conectado` guarda um valor booleano (`True` ou `False`). O programa verifica o estado dela para exibir a mensagem adequada.

#### **Exemplo 2: Testando listas vazias**

Você pode verificar se uma lista está vazia, pois listas vazias são avaliadas como `False`:

```python
itens = []
if itens:
    print("A lista tem itens.")
else:
    print("A lista está vazia.")
```

- Quando `itens` é uma lista vazia, o bloco `else` é executado.

------

### **1.2 Operadores Relacionais e Exemplos Práticos**

Operadores relacionais comparam dois valores e retornam um resultado booleano. Esses operadores incluem:

| Operador | Significado      | Exemplo    | Resultado |
| -------- | ---------------- | ---------- | --------- |
| `>`      | Maior que        | `5 > 3`    | `True`    |
| `<`      | Menor que        | `2 < 4`    | `True`    |
| `>=`     | Maior ou igual a | `3 >= 3`   | `True`    |
| `<=`     | Menor ou igual a | `4 <= 2`   | `False`   |
| `==`     | Igual a          | `10 == 10` | `True`    |
| `!=`     | Diferente de     | `7 != 5`   | `True`    |

#### **Exemplo 1: Verificando se um número é par**

```python
numero = int(input("Digite um número: "))
if numero % 2 == 0:
    print("O número é par.")
else:
    print("O número é ímpar.")
```

- `numero % 2` calcula o resto da divisão do número por 2. Se o resto for `0`, o número é par.

#### **Exemplo 2: Validando aprovação de um aluno**

```python
media = float(input("Digite a média do aluno: "))
if media >= 7.0:
    print("Aluno aprovado!")
else:
    print("Aluno reprovado.")
```

- O operador relacional `>=` verifica se a nota é suficiente para a aprovação.

------

### **1.3 Operadores Lógicos (`and`, `or`, `not`)**

Os operadores lógicos combinam condições booleanas para criar expressões mais complexas:

- **`and`**: Retorna `True` se todas as condições forem verdadeiras.
- **`or`**: Retorna `True` se pelo menos uma condição for verdadeira.
- **`not`**: Inverte o valor booleano de uma condição.

#### **Exemplo 1: Combinação de condições com `and`**

```python
idade = int(input("Digite sua idade: "))
renda = float(input("Digite sua renda mensal: "))

if idade >= 18 and renda >= 2500:
    print("Você pode solicitar o empréstimo.")
else:
    print("Você não atende aos requisitos.")
```

- Ambas as condições precisam ser verdadeiras para a aprovação.

#### **Exemplo 2: Uso de `or` para multiplas possibilidades**

```python
cor = input("Digite uma cor (vermelho, azul, verde): ")
if cor == "vermelho" or cor == "azul":
    print("Você escolheu uma cor primária.")
else:
    print("Você escolheu outra cor.")
```

- Aqui, `or` permite verificar se a entrada é uma das cores primárias.

#### **Exemplo 3: Negando condições com `not`**

```python
logado = False
if not logado:
    print("Você precisa fazer login primeiro.")
```

- O operador `not` inverte o estado de `logado`, indicando que o usuário precisa fazer login.

------

### **1.4 Precedência de Operadores**

Assim como na matemática, em Python, os operadores têm uma ordem de execução. A ordem de precedência é:

1. Parênteses `()`
2. Operadores aritméticos (`*`, `/`, `+`, `-`)
3. Operadores relacionais (`>`, `<`, `==`, etc.)
4. Operadores lógicos (`not`, `and`, `or`)

#### **Exemplo: Resolva a expressão**

```python
resultado = (10 - 2) > 5 and 3 * 2 == 6
print(resultado)
```

**Passo a passo:**

1. `10 - 2 = 8`
2. `8 > 5 = True`
3. `3 * 2 = 6`
4. `6 == 6 = True`
5. `True and True = True`

**Resultado final:** `True`

#### **Exercícios Desafiadores**

1. Resolva as seguintes expressões e explique cada passo:
   - `(5 + 3 * 2) > 10 or (4 / 2 == 2)`
   - `not (10 > 3 and 3 == 3) or 2 ** 3 == 8`
2. Corrija o código abaixo para que a saída seja sempre `True`:

```python
resultado = 5 > 3 or 4 * 2 < 6 and not (10 == 10)
print(resultado)
```

1. Escreva um programa que avalie a seguinte condição:

```text
Se a soma de dois números for maior que 10 e ambos forem pares, exiba "Condição atendida". Caso contrário, exiba "Condição não atendida".
```

------

### **1.5 Conversão de Tipos para Booleano**

Em Python, alguns valores são automaticamente avaliados como `False`, como:

- `None`
- Número `0`
- Strings ou listas vazias (`""`, `[]`)

#### **Exemplo: Testando diferentes valores**

```python
valores = [0, 1, "", "Python", [], [1, 2, 3]]
for valor in valores:
    if valor:
        print(f"{valor} é avaliado como True.")
    else:
        print(f"{valor} é avaliado como False.")
```

- O loop verifica como diferentes tipos de dados são convertidos para booleanos.

------

### **1.6 Conclusão**

Nesta seção, você aprendeu os fundamentos essenciais para trabalhar com estruturas de controle em Python. Exploramos:

- O conceito de valores booleanos e sua importância;
- Como usar operadores relacionais para criar condições;
- A lógica por trás dos operadores lógicos para combinar condições;
- A precedência de operadores, garantindo a ordem correta de execução;
- A conversão de diferentes tipos de dados para valores booleanos.

Esses conhecimentos são a base para criar programas mais dinâmicos e interativos. Aprofunde-se praticando os exemplos fornecidos e aplique-os em problemas do dia a dia, como validação de dados ou controle de fluxo em aplicações simples. Agora, você está pronto para avançar para o próximo nível e explorar estruturas condicionais mais detalhadas no Python.