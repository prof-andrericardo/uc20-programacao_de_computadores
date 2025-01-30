# **7. Avaliação**

A avaliação é uma etapa essencial no aprendizado de programação, pois permite medir o entendimento dos conceitos e identificar pontos de melhoria. Nesta seção, serão apresentadas atividades avaliativas organizadas em quatro partes: quiz conceitual, resolução de problemas práticos, projeto final e code review. Todas as atividades foram pensadas para alunos iniciantes em Python.

------

## **7.1 Quiz Conceitual**

O quiz é uma forma rápida e interativa de testar os conhecimentos. Ele abrange fundamentos, condicionais e loops, temas centrais para iniciantes em Python.

### **Perguntas**

#### **1. Qual é a saída do código abaixo?**

```python
x = 10
y = 5
if x > y:
    print("A")
else:
    print("B")
```

**Resposta:**

```
A
```

**Justificativa:** A condição `x > y` é verdadeira, então o bloco dentro do `if` é executado, exibindo "A".

------

#### **2. Qual é o resultado de `10 % 3`?**

**Resposta:**

```
1
```

**Justificativa:** O operador `%` calcula o resto da divisão de 10 por 3. O quociente é 3 e o resto é 1.

------

#### **3. Qual é a saída do código abaixo?**

```python
contador = 0
while contador < 3:
    print(contador)
    contador += 1
```

**Resposta:**

```
0
1
2
```

**Justificativa:** O loop `while` inicia com `contador = 0` e continua enquanto `contador < 3`. A cada iteração, `contador` é incrementado em 1.

------

#### **4. O que o código a seguir faz?**

```python
numeros = [1, 2, 3, 4]
for numero in numeros:
    if numero % 2 == 0:
        print(numero)
```

**Resposta:**

```
2
4
```

**Justificativa:** O `for` percorre a lista e imprime apenas os números pares, que são divisíveis por 2.

------

## **7.2 Resolução de Problemas Práticos**

Esta seção apresenta problemas que desafiam os alunos a aplicar o conhecimento em Python para resolver tarefas com diferentes níveis de dificuldade.

### **Problema 1: Soma de Números**

**Descrição:** Escreva um programa que solicite ao usuário dois números e exiba a soma deles.

**Correção:**

- O programa deve usar `input()` para receber os números.
- Convertê-los para inteiros ou float antes de somar.

**Justificativa:** Operações matemáticas em Python exigem tipos numéricos.

------

### **Problema 2: Contar Letras em uma Palavra**

**Descrição:** Peça ao usuário para digitar uma palavra e exiba quantas letras ela possui.

**Correção:**

- Use `input()` para obter a palavra.
- Utilize `len()` para calcular o número de letras.

**Justificativa:** A função `len()` retorna o tamanho de uma string.

------

### **Problema 3: Verificar se um Número é Primo**

**Descrição:** Crie um programa que verifique se um número fornecido pelo usuário é primo.

**Correção:**

- O programa deve verificar se o número é divisível apenas por 1 e ele mesmo.
- Utilize um loop para testar divisores.

**Justificativa:** Um número primo só possui dois divisores.

------

## **7.3 Projeto Final**

Os projetos finais desafiam os alunos a aplicar o que aprenderam em projetos mais complexos e funcionais.

### **1. Gerenciador de Tarefas**

**Descrição:** Crie um programa que permita ao usuário:

- Adicionar tarefas a uma lista.
- Marcar tarefas como concluídas.
- Exibir a lista de tarefas.

**Etapas do Projeto:**

1. Criar uma lista vazia para armazenar as tarefas.
2. Utilizar um menu interativo para gerenciar as opções (adicionar, exibir e marcar como concluída).
3. Usar loops e condicionais para implementar a lógica do programa.

**Justificativa:** Este projeto ensina manipulação de listas, uso de loops e interação com o usuário.

------

### **2. Simulador de Loja Virtual**

**Descrição:** Desenvolva um programa que permita ao usuário:

- Adicionar itens ao carrinho.
- Exibir o total da compra.
- Finalizar a compra.

**Etapas do Projeto:**

1. Criar um dicionário para armazenar os itens e seus preços.
2. Utilizar um loop para gerenciar as opções (adicionar, exibir total e finalizar).
3. Validar a entrada do usuário para evitar erros.

**Justificativa:** Este projeto introduz dicionários e reforça conceitos de loops e condicionais.

------

## **7.4 Code Review**

O **code review** é a análise crítica de um código, com o objetivo de identificar melhorias e corrigir erros. Esta etapa ajuda os alunos a desenvolverem boas práticas.

### **Atividade: Análise de Código**

#### **Código para Análise:**

```python
itens = ["maçã", "banana", "laranja"]
for i in range(0, len(itens)):
    print(itens[i])
```

**Correção:**

- Substitua o uso de `range` e `len` por uma abordagem direta.

**Código Melhorado:**

```python
itens = ["maçã", "banana", "laranja"]
for item in itens:
    print(item)
```

**Justificativa:** Usar `for item in itens` é mais legível e evita cálculos desnecessários.

------

## **Conclusão**

Nesta seção, apresentamos diferentes métodos para avaliar o aprendizado dos alunos em Python, desde quizzes rápidos até projetos completos e análise de código. Essas atividades não apenas testam o conhecimento, mas também incentivam a prática e a aplicação em cenários reais. Com essas avaliações, os alunos estarão mais preparados para resolver problemas e criar soluções na programação.