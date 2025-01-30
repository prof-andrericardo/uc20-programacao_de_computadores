# **Estruturas de Controle em Python**

## **2. Estruturas Condicionais**

### **2.1 Introdução às Estruturas Condicionais**

As estruturas condicionais permitem que os programas tomem decisões baseadas em condições. Elas são fundamentais para tornar um programa dinâmico, pois controlam quais partes do código serão executadas dependendo das circunstâncias. Em Python, utilizamos as palavras-chave `if`, `else` e `elif` para implementar essas condições.

#### **Por que usar estruturas condicionais?**

Imagine um sistema de semáforo:

- Se o sinal estiver verde, os carros podem seguir.
- Se estiver vermelho, os carros devem parar.

Essa lógica simples é aplicada em programação por meio das estruturas condicionais, permitindo que o programa "pense" e tome decisões.

Um fluxograma para essa lógica seria:

```
          Início
            |
     [Sinal Verde?]
         /    \
       Sim     Não
       /         \
[Siga em frente]  [Pare]
            |
         Fim
```

---

### **2.2 O Comando `if`**

O comando `if` é usado para verificar se uma condição é verdadeira. Se for, o código dentro do bloco `if` será executado.

#### **Sintaxe do `if`**

```python
if condição:
    # código executado se a condição for verdadeira
```

#### **Exemplo 1: Verificando a maioridade**

```python
idade = int(input("Digite sua idade: "))
if idade >= 18:
    print("Você é maior de idade.")
```

**Passo a passo:**

1. O programa solicita que o usuário insira sua idade.
2. A condição `idade >= 18` é avaliada.
3. Se for verdadeira, a mensagem "Você é maior de idade." será exibida.

---

### **2.3 O Comando `if/else`**

O comando `if/else` adiciona uma alternativa. Caso a condição no `if` seja falsa, o código no bloco `else` será executado.

#### **Sintaxe do `if/else`**

```python
if condição:
    # código executado se a condição for verdadeira
else:
    # código executado se a condição for falsa
```

#### **Exemplo 2: Verificando aprovação em uma prova**

```python
nota = float(input("Digite sua nota: "))
if nota >= 7.0:
    print("Aprovado!")
else:
    print("Reprovado.")
```

**Passo a passo:**

1. O programa solicita que o usuário insira sua nota.
2. A condição `nota >= 7.0` é avaliada.
3. Se for verdadeira, "Aprovado!" será exibido.
4. Se for falsa, "Reprovado." será exibido.

---

### **2.4 O Comando `if/elif/else`**

Quando temos várias condições, podemos usar o comando `elif` (abreviação de "else if"). Ele permite testar múltiplas condições em sequência.

#### **Sintaxe do `if/elif/else`**

```python
if condição1:
    # código executado se condição1 for verdadeira
elif condição2:
    # código executado se condição2 for verdadeira
else:
    # código executado se nenhuma condição for verdadeira
```

#### **Exemplo 3: Classificação de notas**

```python
nota = float(input("Digite sua nota: "))
if nota >= 9.0:
    print("Excelente!")
elif nota >= 7.0:
    print("Bom trabalho.")
elif nota >= 5.0:
    print("Recuperação.")
else:
    print("Reprovado.")
```

#### **Quadro Comparativo: `if/elif` vs `match/case`**

| **Aspecto**             | **`if/elif`**       | **`match/case`**                 |
| ----------------------- | ------------------- | -------------------------------- |
| Sintaxe                 | Simples e universal | Mais organizada para casos fixos |
| Versão Python requerida | Todas as versões    | Python 3.10 ou superior          |
| Ideal para              | Condições dinâmicas | Padrões fixos ou combinações     |

---

### **2.5 O Comando `match/case` (Python 3.10+)**

O comando `match/case` é usado para verificar padrões em uma variável. Ele é útil para substituir várias condições `if/elif` em alguns casos.

#### **Sintaxe do `match/case`**

```python
match variável:
    case valor1:
        # código executado se variável == valor1
    case valor2:
        # código executado se variável == valor2
    case _:
        # código executado se nenhuma condição for verdadeira
```

#### **Exemplo 4: Menu interativo**

```python
opcao = int(input("Escolha uma opção (1, 2 ou 3): "))
match opcao:
    case 1:
        print("Você escolheu a opção 1.")
    case 2:
        print("Você escolheu a opção 2.")
    case 3:
        print("Você escolheu a opção 3.")
    case _:
        print("Opção inválida.")
```

---

## **2.6 Exercícios**

### **Questões Dissertativas** 📖

1. Explique a diferença entre `if/elif/else` e `match/case`. Em quais cenários cada um é mais eficiente?
2. O que acontece se omitirmos o `else` em uma estrutura condicional? Quando isso pode ser útil?

### **Questões de Múltipla Escolha (Única Resposta Correta)** ✅

1. Qual a saída do código abaixo?

```python
x = 10
y = 5
if x < y:
    print("Menor")
else:
    print("Maior")
```

a) Menor b) Maior ✅ c) Erro

d) Nenhuma das anteriores

### **Questões de Múltipla Escolha (Múltiplas Respostas Corretas)** 🔲🔲

1. Quais das opções abaixo representam boas práticas para evitar erros em estruturas condicionais? (Marque todas as corretas)

- 🔲 Usar `assert` para verificar pré-condições.
- 🔲 Encadear múltiplos `elif` sempre que possível.
- ✅ Testar entradas do usuário com `print()`.
- ✅ Utilizar `logging` para monitoramento.

### **Questões Verdadeiro ou Falso** ✔❌

1. `if/else` é necessário em todas as verificações condicionais. **(F)**
2. O `match/case` pode ser usado em qualquer versão do Python. **(F)**

### **Questões de Associação de Colunas** 🔄

1. Relacione os operadores com sua função: | Operador | Função | |---------|----------| | `==` | ( ) Verifica igualdade | | `!=` | ( ) Verifica diferença | | `>=` | ( ) Verifica maior ou igual |

### **Questões de Análise de Sentenças** 🔢

1. Analise as sentenças sobre `if` e `match/case`: I. `match/case` é mais eficiente para verificações múltiplas. II. O `if` só pode ser usado com `else`. III. Estruturas condicionais podem ser aninhadas. IV. `elif` é obrigatório em todas as estruturas condicionais.

a) V F V F ✅ b) F V V F c) V V F F d) F F V V

#### **Respostas e Justificativas**

📌 Todas as respostas corretas são acompanhadas de explicações detalhadas.

-----

### **2.7 Conclusão**

Nesta seção, aprendemos como usar estruturas condicionais para criar programas mais inteligentes e responsivos. Exploramos:

- O básico do comando `if` para decisões simples;
- O uso de `if/else` para oferecer alternativas;
- O comando `if/elif/else` para lidar com múltiplas condições;
- O `match/case` como uma forma moderna e eficiente de lidar com múltiplos casos;
- Um quadro comparativo entre `if/elif` e `match/case`.

Esses conceitos são essenciais para criar sistemas dinâmicos, como menus interativos, verificadores de condições e classificadores. Pratique os exemplos e aplique-os em problemas reais para consolidar o aprendizado!