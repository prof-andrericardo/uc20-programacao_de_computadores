# **8. Exercícios Gamificados**

Exercícios gamificados são uma forma divertida e interativa de aprender programação. Eles incentivam os alunos a resolver problemas enquanto desenvolvem suas habilidades em Python. Nesta seção, os alunos enfrentarão desafios práticos que envolvem depuração de códigos, otimização e criação de soluções baseadas em cenários reais.

------

## **8.1 Debug: A Caça aos Erros**

### **Objetivo**

Os alunos devem identificar e corrigir erros em blocos de código fornecidos. Esses erros podem ser de lógica, sintaxe ou funcionamento, o que ajuda a aprimorar a atenção aos detalhes.

### **Exercício 1: Erro de Lógica**

#### **Código com Erro:**

```python
numero = 10
if numero > 5:
print("O número é menor que 5")
```

#### **O que está errado?**

1. A mensagem exibida está incorreta, já que `numero > 5`.
2. O código está mal indentado, o que gera um erro de sintaxe.

#### **Correção:**

```python
numero = 10
if numero > 5:
    print("O número é maior que 5")
```

### **Exercício 2: Erro de Sintaxe**

#### **Código com Erro:**

```python
for i in range(5)
    print(i)
```

#### **O que está errado?**

1. Falta o caractere `:` após o parêntese do `for`.

#### **Correção:**

```python
for i in range(5):
    print(i)
```

------

## **8.2 Transforme o Código**

### **Objetivo**

Os alunos receberão um código inicial que funciona, mas não é eficiente ou legível. A tarefa será melhorar a estrutura do código, tornando-o mais claro e otimizado.

### **Exercício 1: Soma de Elementos de uma Lista**

#### **Código Inicial:**

```python
numeros = [1, 2, 3, 4, 5]
soma = 0
for i in range(len(numeros)):
    soma += numeros[i]
print("A soma é:", soma)
```

#### **Como Melhorar:**

1. Substituir o uso de `range(len())` por uma iteração direta sobre a lista.
2. Tornar o código mais legível e eficiente.

#### **Código Melhorado:**

```python
numeros = [1, 2, 3, 4, 5]
soma = sum(numeros)
print("A soma é:", soma)
```

### **Exercício 2: Verificar Números Pares em uma Lista**

#### **Código Inicial:**

```python
numeros = [1, 2, 3, 4, 5]
pares = []
for i in range(len(numeros)):
    if numeros[i] % 2 == 0:
        pares.append(numeros[i])
print("Números pares:", pares)
```

#### **Como Melhorar:**

1. Iterar diretamente sobre a lista, sem usar `range(len())`.
2. Usar uma compreensão de lista para tornar o código mais compacto e legível.

#### **Código Melhorado:**

```python
numeros = [1, 2, 3, 4, 5]
pares = [numero for numero in numeros if numero % 2 == 0]
print("Números pares:", pares)
```

------

## **8.3 Desafios Baseados em Cenários Reais**

### **Objetivo**

Apresentar problemas práticos baseados em situações do mundo real, incentivando os alunos a aplicar o que aprenderam para criar soluções completas.

### **Desafio 1: Criar um Sistema de Senha Segura**

#### **Descrição:**

Crie um programa que:

1. Solicite ao usuário que crie uma senha.
2. Valide se a senha atende aos seguintes critérios:
   - Pelo menos 8 caracteres.
   - Contém pelo menos uma letra maiúscula, uma letra minúscula e um número.
3. Exiba uma mensagem indicando se a senha é válida ou inválida.

#### **Etapas para Resolução:**

1. Use `input()` para receber a senha.
2. Utilize condições (`if`) para verificar cada critério.
3. Exiba mensagens específicas para cada erro (ex.: "A senha precisa ter pelo menos 8 caracteres").

------

### **Desafio 2: Criar um Validador de Formulário**

#### **Descrição:**

Desenvolva um programa que:

1. Solicite ao usuário que preencha um formulário com nome, idade e e-mail.
2. Valide as entradas:
   - O nome não pode estar vazio.
   - A idade deve ser um número inteiro positivo.
   - O e-mail deve conter "@" e um domínio válido (ex.: ".com").
3. Exiba mensagens indicando se o formulário foi preenchido corretamente ou não.

#### **Etapas para Resolução:**

1. Verifique cada campo separadamente.
2. Exiba mensagens de erro específicas para cada campo inválido.
3. Se todos os campos forem válidos, exiba "Formulário enviado com sucesso".

------

### **Desafio 3: Simulação de Lançamento de Dados**

#### **Descrição:**

Crie um programa que:

1. Simule o lançamento de dois dados.
2. Exiba os valores de cada dado e a soma deles.
3. Permita que o usuário lance os dados quantas vezes quiser.

#### **Etapas para Resolução:**

1. Use a função `random.randint()` para gerar os valores dos dados.
2. Utilize um loop para permitir lançamentos repetidos.
3. Exiba os resultados de forma clara e organizada.

------

## **Conclusão**

Os exercícios gamificados apresentados nesta seção são projetados para tornar o aprendizado mais dinâmico e envolvente. Desde identificar e corrigir erros até criar soluções para cenários reais, esses desafios ajudam os alunos a consolidar os conceitos de Python de forma prática e divertida. Pratique, experimente e veja como sua compreensão de programação evolui!