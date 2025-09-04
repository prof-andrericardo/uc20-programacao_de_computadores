# Capítulo 1 – Fundamentos da Linguagem Python

# 🖨️ 1.1 Utilizar a função `print()`

> ✨ *“A função `print()` é a primeira aliada de quem começa a programar. Com ela, damos voz ao código.”*

------

## 📘 O que é a função `print()`?

A função `print()` é utilizada para **exibir dados no terminal**, como:

- Textos (strings)
- Números
- Resultados de operações matemáticas
- Variáveis e muito mais

É uma das primeiras ferramentas que aprendemos ao iniciar em Python, e também uma das mais utilizadas.

------

## 🧪 1.1.1 Saída de dados básica

```python
print("Olá, mundo!")  # Exibe uma mensagem
print(42)             # Exibe um número
print(7 + 3)          # Exibe o resultado de uma operação
```

🖨️ Saída:

```
Olá, mundo!
42
10
```

------

## ➕ 1.1.2 Concatenar com o operador `+`

```python
print("Olá, " + "mundo!")                     # Junta duas strings
print("A soma é: " + str(5 + 3))              # Precisa converter número em string
```

📌 Lembre-se: o operador `+` **só funciona entre strings**. Para juntar número e texto, use `str()`.

------

## 🧩 1.1.3 Concatenar com vírgula `,`

```python
print("A soma é:", 5 + 3)
print("Hoje", "é", "um", "bom", "dia!")
```

💡 A vírgula:

- Aceita diferentes tipos de dados (texto, número etc.)
- Adiciona **espaço automaticamente**

------

## ⚖️ 1.1.4 Diferença entre `+` e `,`

| Característica      | `+`             | `,`                   |
| ------------------- | --------------- | --------------------- |
| Apenas para strings | ✅ Sim           | ❌ Não (mistura tipos) |
| Adiciona espaço?    | ❌ Não           | ✅ Sim                 |
| Requer conversão?   | ✅ Sim (`str()`) | ❌ Não                 |

------

## 🧵 1.1.5 Aspas em Python

```python
print('Texto com aspas simples')
print("Texto com aspas duplas")
print("""Texto com
várias linhas""")
```

Use aspas triplas (`'''` ou `"""`) para **mensagens longas ou multilinha**.

------

## 🔠 1.1.6 Caracteres de escape

| Símbolo | Significado           |
| ------- | --------------------- |
| `\n`    | Quebra de linha       |
| `\t`    | Tabulação (tab)       |
| `\'`    | Aspa simples          |
| `\"`    | Aspa dupla            |
| `\\`    | Barra invertida (`\`) |

```python
print("Olá,\nMundo!")
print("Python\té\tincrível!")
```

------

## ⚙️ 1.1.7 Parâmetro `end`

Define **como a linha termina**.

```python
print("Linha 1", end=" ")
print("Linha 2")
```

🖨️ Saída:

```
Linha 1 Linha 2
```

------

## ⚙️ 1.1.8 Parâmetro `sep`

Define o **separador entre os elementos**:

```python
print("15", "08", "2024", sep="/")
print("home", "user", "documentos", sep="/")
print("www", "python", "org", sep=".")
```

------

## 🧬 1.1.9 F-strings: a forma moderna

F-strings são a maneira **mais prática e moderna** de formatar strings. Introduzidas no Python 3.6.

```python
nome = "João"
idade = 17
print(f"Meu nome é {nome} e tenho {idade} anos.")
print(f"A soma de 5 + 3 é {5 + 3}")
pi = 3.14159
print(f"O valor de pi com 2 casas decimais é {pi:.2f}")
```

------

## 🧼 1.1.10 Boas Práticas

| Prática                             | Por que aplicar?                                             |
| ----------------------------------- | ------------------------------------------------------------ |
| Usar f-strings                      | São mais legíveis e modernas                                 |
| Evitar concatenação com `+`         | Pode causar erros com tipos diferentes                       |
| Usar `sep` e `end`                  | Ajuda a personalizar a saída e evitar quebras de linha indesejadas |
| Comentar seus `print()` quando útil | Facilita leitura e manutenção do código                      |

------

## 📚 Conclusão

- A função `print()` é a **ferramenta principal de saída** em Python.
- É útil para **testes, comunicação com o usuário e depuração de código**.
- Dominar seus parâmetros e usos é essencial para **escrever programas claros e eficazes**.

------

## 🔗 Referências

- [Documentação oficial do `print()`](https://docs.python.org/pt-br/3/library/functions.html#print)
- [Vídeo: Curso Python – Guanabara – Print e concatenação](https://www.youtube.com/watch?v=Vb0CXrYfzG4)
- [Python Brasil – wiki sobre saída de dados](https://wiki.python.org.br/)

------

# 🎤 1.2 Utilizar a função `input()`

> ✨ *“Programas interativos transformam ideias em diálogo. Com `input()`, o Python começa a ouvir o usuário.”*

------

## 📘 O que é a função `input()`?

A função `input()` é uma **ferramenta de entrada de dados** do Python.
 Sempre que você quiser **perguntar algo ao usuário** e receber uma resposta durante a execução do programa, você usará `input()`.

💬 Quando executada, ela:

- Exibe uma **mensagem (opcional)** na tela.
- **Pausa o programa** enquanto o usuário digita uma resposta.
- Retorna o valor digitado como **uma string (texto)**.

------

## 🧪 1.2.1 Sintaxe básica

```python
nome = input("Qual é o seu nome? ")
print("Seja bem-vindo,", nome)
```

### 🧾 Explicando passo a passo:

- `input("Qual é o seu nome? ")` → exibe a pergunta entre parênteses e **espera o usuário digitar algo**.
- O valor digitado é **sempre tratado como texto (str)**.
- O conteúdo digitado é armazenado na variável `nome`.
- O `print()` então mostra uma mensagem usando o valor armazenado.

🖨️ Saída esperada:

```
Qual é o seu nome? Alice
Seja bem-vindo, Alice
```

------

## 🧬 1.2.2 Tudo que vem do `input()` é texto (`str`)

Mesmo que o usuário digite um número, ele será interpretado como **string**, ou seja, **não pode ser usado diretamente em cálculos**.

```python
valor = input("Digite um número: ")
print("Tipo:", type(valor))
```

🖨️ Exemplo de entrada e saída:

```
Digite um número: 10
Tipo: <class 'str'>
```

⚠️ Mesmo que o número seja "10", ele está no formato `"10"` (texto).

------

## 🔁 1.2.3 Convertendo tipos: `int()` e `float()`

Se você quiser **usar o valor digitado como número**, deve convertê-lo:

```python
idade = int(input("Qual sua idade? "))
print("No ano que vem, você terá", idade + 1)
```

### 🧾 Explicação:

- `int(...)` converte o texto para **número inteiro**.
- Você pode usar `float(...)` se quiser **números com casas decimais**.

⚠️ Se o usuário digitar algo inválido (como letras), o programa **vai dar erro**.

------

## 🧯 1.2.4 Evitando travamentos: `try` e `except`

Para evitar que o programa quebre com entradas inválidas, usamos o **tratamento de erros**:

```python
try:
    idade = int(input("Digite sua idade: "))
    print("Idade:", idade)
except ValueError:
    print("Erro! Você precisa digitar um número inteiro.")
```

📌 O que isso faz?

- `try`: tenta executar o código.
- `except`: caso aconteça um erro (por exemplo, o usuário digitar “dezessete”), ele **captura o erro** e mostra uma mensagem amigável.

------

## 📥 1.2.5 Vários dados em uma linha: `.split()`

O método `split()` quebra o texto digitado **em partes separadas** (por padrão, pelo espaço).

```python
entrada = input("Digite seu nome e idade: ")
nome, idade = entrada.split()
idade = int(idade)
print(f"{nome}, você tem {idade} anos.")
```

🧾 Explicação:

- O usuário digita, por exemplo: `João 17`
- `split()` separa em duas partes: `"João"` e `"17"`
- A variável `nome` recebe o primeiro valor, e `idade` o segundo (convertido em número)

------

## 🔎 1.2.6 Validar se o usuário digitou um número

Podemos usar o método `.isdigit()` para verificar se a entrada é numérica:

```python
idade = input("Digite sua idade: ")
if idade.isdigit():
    idade = int(idade)
    print("Idade válida!")
else:
    print("Por favor, digite apenas números.")
```

📌 `.isdigit()` retorna `True` se **todos os caracteres forem dígitos numéricos**.

------

## 🎛️ 1.2.7 Definir um valor padrão se o usuário não digitar nada

Às vezes, é interessante oferecer uma **opção padrão**:

```python
nome = input("Digite seu nome [Convidado]: ")
if nome == "":
    nome = "Convidado"
```

### Alternativa mais elegante:

```python
nome = input("Digite seu nome: ") or "Convidado"
```

💡 O operador `or` retorna `"Convidado"` se o valor digitado for vazio (`""`).

------

## ✅ Boas práticas ao usar `input()`

| Boas práticas                      | Justificativa                                                |
| ---------------------------------- | ------------------------------------------------------------ |
| Validar a entrada (`isdigit`, etc) | Evita erros e travamentos                                    |
| Converter tipo só após validação   | Impede que valores inválidos causem exceções                 |
| Usar mensagens claras e amigáveis  | Facilita a experiência do usuário                            |
| Tratar erros com `try/except`      | Evita que o programa pare inesperadamente                    |
| Oferecer valores padrão            | Mantém o fluxo do programa mesmo se o usuário não preencher algo |

------

## 🧠 Exemplo completo de boas práticas

```python
while True:
    idade = input("Digite sua idade entre 0 e 120: ")
    if idade.isdigit():
        idade = int(idade)
        if 0 <= idade <= 120:
            break
        else:
            print("Idade fora do intervalo.")
    else:
        print("Digite um número válido.")

nome = input("Digite seu nome [Anônimo]: ") or "Anônimo"

print(f"{nome}, sua idade é {idade}.")
```

------

## 🔗 Referências

- [📘 input() – Documentação Oficial (PT-BR)](https://docs.python.org/pt-br/3/library/functions.html#input)
- [🎥 Curso em Vídeo – Entrada de Dados](https://www.youtube.com/watch?v=XsE2nB1hG10)
- [📖 Python Brasil – Entrada de Dados](https://wiki.python.org.br/EntradaDeDados)

------

