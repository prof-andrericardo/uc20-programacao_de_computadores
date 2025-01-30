# **4. Práticas e Otimização**

A prática e a otimização são etapas fundamentais no aprendizado de programação, especialmente para iniciantes. Nesta seção, você aprenderá a depurar, melhorar e escrever códigos mais eficientes e organizados em Python. Vamos explorar ferramentas de depuração, como refatorar soluções ineficientes e identificar boas práticas na construção de programas.

------

## **4.1 Depuração de Estruturas de Controle**

### **Introdução**

Depuração é o processo de identificar e corrigir erros no código. Esses erros podem ser lógicos, sintáticos ou de execução. Para iniciantes, dominar a depuração ajuda a entender o comportamento do programa e a melhorar a habilidade de resolver problemas.

Python oferece ferramentas e técnicas simples e poderosas para depurar programas, como o uso de `print()` para visualizar valores, bem como o módulo `pdb` para depuração mais avançada.

### **Exemplo 1: Identificando um erro lógico**

```python
# Código com erro lógico
numero = int(input("Digite um número: "))
if numero % 2 == 1:
    print("O número é par!")
else:
    print("O número é ímpar!")
```

**Problema:** A lógica da condição está invertida. Números pares têm resto 0 ao serem divididos por 2.

#### **Passo a passo para corrigir o erro:**

1. Insira `print()` para verificar os valores intermediários.
2. Leia a mensagem de erro (se houver) ou analise o comportamento do programa.

**Correção:**

```python
# Código corrigido
numero = int(input("Digite um número: "))
if numero % 2 == 0:
    print("O número é par!")
else:
    print("O número é ímpar!")
```

------

### **Exemplo 2: Depurando com o módulo `pdb`**

```python
# Programa com erro
def calcular_media(notas):
    soma = sum(notas)
    return soma / len(notas)

notas = [10, 8, 7]
print("Média:", calcular_media(notas))
```

Caso ocorra um erro inesperado, podemos usar o módulo `pdb`:

```python
import pdb

notas = [10, 8, 7]
pdb.set_trace()  # Pausa o código aqui para inspeção
print("Média:", calcular_media(notas))
```

No terminal interativo, você poderá inspecionar variáveis, testar comandos e entender melhor o problema.

------

## **4.2 Refatoração de Código**

### **Introdução**

Refatoração é o processo de melhorar a estrutura interna de um código sem alterar seu comportamento externo. É uma prática essencial para criar programas mais eficientes, legíveis e fáceis de manter.

Um código refatorado geralmente reduz redundâncias, melhora o desempenho e segue melhores práticas de programação.

### **Exemplo 1: Melhorando um algoritmo ineficiente**

#### **Código original (ineficiente):**

```python
# Ordenação de uma lista de forma manual
numeros = [3, 1, 4, 1, 5]

for i in range(len(numeros)):
    for j in range(len(numeros) - 1):
        if numeros[j] > numeros[j + 1]:
            temp = numeros[j]
            numeros[j] = numeros[j + 1]
            numeros[j + 1] = temp

print("Números ordenados:", numeros)
```

#### **Problemas:**

1. O algoritmo utiliza um laço aninhado, o que reduz a eficiência.
2. A lógica é mais difícil de ler e propensa a erros.

#### **Código refatorado:**

```python
# Refatorando com sorted()
numeros = [3, 1, 4, 1, 5]
numeros_ordenados = sorted(numeros)
print("Números ordenados:", numeros_ordenados)
```

#### **Atividade: Refatorando um algoritmo manual**

1. Receba uma lista de números do usuário.
2. Implemente uma solução para ordenar os números sem usar funções prontas.
3. Refatore o código para utilizar o `sorted()`.

------

## **4.3 Padrões e Anti-Padrões Comuns**

### **Introdução**

Boas práticas ajudam a evitar problemas comuns e tornam o código mais legível e sustentável. Por outro lado, anti-padrões são abordagens problemáticas que dificultam o entendimento e a manutenção do código.

Vamos explorar alguns exemplos de boas práticas e anti-padrões em loops e condicionais.

### **Exemplo 1: Evitando o uso excessivo de variáveis globais**

#### **Anti-padrão:**

```python
# Uso excessivo de variáveis globais
contador = 0

def incrementar():
    global contador
    contador += 1

def exibir_contador():
    global contador
    print(f"Contador: {contador}")

incrementar()
exibir_contador()
```

#### **Padrão recomendado:**

Use variáveis locais e, se necessário, encapsule-as em uma classe ou função.

```python
# Padrão recomendado
class Contador:
    def __init__(self):
        self.valor = 0

    def incrementar(self):
        self.valor += 1

    def exibir(self):
        print(f"Contador: {self.valor}")

c = Contador()
c.incrementar()
c.exibir()
```

------

### **Exemplo 2: Evitando condicionais redundantes**

#### **Anti-padrão:**

```python
idade = int(input("Digite sua idade: "))
if idade >= 18:
    print("Maior de idade")
else:
    if idade < 18:
        print("Menor de idade")
```

#### **Padrão recomendado:**

```python
idade = int(input("Digite sua idade: "))
if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
```

------

## **Conclusão**

Nesta seção, aprendemos sobre a importância da depuração, refatoração e boas práticas em Python. Pratique depuração com ferramentas simples e avançadas, otimize seus algoritmos com refatoração e evite anti-padrões para escrever códigos mais eficientes e legíveis. A prática constante dessas habilidades fará de você um programador mais confiante e preparado para desafios reais.