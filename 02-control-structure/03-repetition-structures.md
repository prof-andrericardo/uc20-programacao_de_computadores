# **Estruturas de Controle em Python**

## **3. Estruturas de Repetição**

### **3.1 Introdução às Estruturas de Repetição**

As estruturas de repetição permitem que um bloco de código seja executado várias vezes, dependendo de uma condição ou sequência. Elas são fundamentais em Python para automatizar tarefas repetitivas, como processar listas, calcular valores ou exibir informações.

Em Python, existem dois tipos principais de laços de repetição:

- **Laço `while`**: Repetição baseada em uma condição.
- **Laço `for`**: Repetição baseada em uma sequência ou intervalo.

Além disso, utilizamos comandos como `break`, `continue` e `else` para controlar o comportamento dos loops.

---

### **3.2 Laço `while`**

O laço `while` executa um bloco de código enquanto uma condição for verdadeira. Ele é útil quando não sabemos previamente quantas vezes o código será repetido.

#### **Sintaxe do `while`**

```python
while condição:
    # código a ser executado enquanto a condição for verdadeira
```

#### **Exemplo 1: Contagem regressiva**

```python
contador = 5
while contador > 0:
    print(f"Contando: {contador}")
    contador -= 1  # Decrementa o valor de contador
print("Fim da contagem!")
```

**Passo a passo:**

1. A variável `contador` é inicializada com o valor 5.
2. A condição `contador > 0` é avaliada. Enquanto for verdadeira, o bloco dentro do `while` será executado.
3. A cada iteração, `contador` é decrementado em 1.
4. Quando `contador` atinge 0, a condição se torna falsa e o loop termina.

---

### **3.3 Laço `for`**

O laço `for` é usado para iterar sobre uma sequência (como uma lista, string ou intervalo). Ele é útil quando sabemos previamente quantas vezes o código será executado.

#### **Sintaxe do `for`**

```python
for variável in sequência:
    # código a ser executado para cada elemento na sequência
```

#### **Exemplo 2: Iterando sobre uma lista**

```python
frutas = ["maçã", "banana", "laranja"]
for fruta in frutas:
    print(f"Eu gosto de {fruta}.")
```

**Passo a passo:**

1. A lista `frutas` contém três elementos.
2. O loop `for` percorre cada elemento da lista e armazena o valor atual na variável `fruta`.
3. A cada iteração, o programa exibe "Eu gosto de [fruta].".

---

### **3.4 Controle de Loops com `break`, `continue` e `else`**

#### **Comando `break`**

O `break` interrompe imediatamente a execução do loop.

#### **Exemplo 3: Parando ao encontrar um número específico**

```python
for numero in range(1, 11):
    if numero == 5:
        print("Número 5 encontrado, parando o loop!")
        break
    print(f"Número: {numero}")
```

#### **Comando `continue`**

O `continue` pula para a próxima iteração do loop, ignorando o código restante.

#### **Exemplo 4: Pulando números pares**

```python
for numero in range(1, 6):
    if numero % 2 == 0:
        continue
    print(f"Número ímpar: {numero}")
```

#### **Comando `else` com loops**

O bloco `else` é executado quando o loop termina normalmente, sem interrupções pelo `break`.

#### **Exemplo 5: Verificação concluída**

```python
for numero in range(1, 6):
    print(f"Verificando: {numero}")
else:
    print("Verificação concluída!")
```

---

### **3.5 Atividade Prática: Combinação de Repetição e Condicionais**

#### **Exemplo 6: Jogo de Adivinhação com Tentativas Limitadas**

Nesta atividade, combinamos repetição e estruturas condicionais para criar um jogo simples em que o usuário deve adivinhar um número secreto com um número limitado de tentativas.

```python
import random

numero_secreto = random.randint(1, 100)
tentativas = 5

print("Bem-vindo ao jogo de adivinhação!")
print(f"Você tem {tentativas} tentativas para adivinhar o número secreto entre 1 e 100.")

while tentativas > 0:
    palpite = int(input("Digite seu palpite: "))
    if palpite == numero_secreto:
        print("Parabéns! Você adivinhou o número secreto!")
        break
    elif palpite < numero_secreto:
        print("Tente um número maior.")
    else:
        print("Tente um número menor.")

    tentativas -= 1
    print(f"Você ainda tem {tentativas} tentativas restantes.")

if tentativas == 0:
    print(f"Que pena! O número secreto era {numero_secreto}.")
```

**Descrição:**

1. O número secreto é gerado aleatoriamente entre 1 e 100.
2. O jogador tem 5 tentativas para adivinhar o número.
3. A cada tentativa, o programa informa se o palpite está correto, ou se o jogador deve tentar um número maior ou menor.
4. Caso o jogador acerte, o loop é interrompido com `break`.
5. Se as tentativas se esgotarem, o programa revela o número secreto.

---

### **3.6 Conclusão**

Nesta seção, exploramos as estruturas de repetição em Python:

- O laço `while`, usado para repetições baseadas em condições dinâmicas.
- O laço `for`, ideal para iterar sobre sequências ou intervalos.
- Comandos como `break`, `continue` e `else`, que permitem controlar o fluxo dos loops.
- Um exemplo prático que combina repetição e condicionais, proporcionando um aprendizado dinâmico e aplicável.

Pratique os exemplos fornecidos e experimente criar seus próprios loops para resolver problemas do dia a dia. A prática é fundamental para dominar as estruturas de repetição!