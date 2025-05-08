# Capítulo 0 - Introdução

# 🐍 0.1 Entender o que é Python

> 📘 *"Aprender Python é como destrancar a porta de um novo mundo da tecnologia com simplicidade e poder."*

------

## 📜 História da Linguagem Python

A linguagem **Python** foi criada por **Guido van Rossum** no final dos anos 1980, sendo oficialmente lançada em **1991** como um projeto de código aberto.

> 🧑‍💻 Guido van Rossum criou Python com a missão de desenvolver uma linguagem que fosse **fácil de aprender**, **legível** e **poderosa o suficiente** para aplicações reais.

A escolha do nome “Python” não tem relação direta com cobras. Na verdade, é uma homenagem ao grupo britânico de comédia **“Monty Python’s Flying Circus”**. Van Rossum queria um nome curto, marcante e “divertido”.

------

## 🧬 Características Fundamentais do Python

Abaixo estão as principais **características que fazem do Python uma das linguagens mais populares do mundo**:

| Característica              | Explicação                                                   |
| --------------------------- | ------------------------------------------------------------ |
| **Linguagem Interpretada**  | Não é necessário compilar o código antes de executá-lo. O Python interpreta linha por linha. |
| **Sintaxe Simples e Clara** | O código é fácil de ler e escrever, se assemelhando ao inglês. |
| **Multiplataforma**         | Funciona em sistemas Windows, Linux, macOS e até em dispositivos móveis. |
| **Tipagem Dinâmica**        | Você não precisa declarar o tipo da variável. Python define isso automaticamente. |
| **Multiparadigma**          | Suporta programação procedural, orientada a objetos e funcional. |
| **Grande Comunidade**       | Milhões de desenvolvedores utilizam Python e contribuem com bibliotecas e suporte. |
| **Ampla Biblioteca Padrão** | Oferece módulos prontos para diversas tarefas (rede, sistema, matemática, dados etc.). |

------

## 🚀 Por que Aprender Python?

Python se tornou uma das linguagens mais **relevantes da atualidade**, sendo usada por grandes empresas e instituições:

- **Ciência de Dados e Inteligência Artificial**: usada por empresas como Google, Netflix e IBM.
- **Desenvolvimento Web**: com frameworks como **Django** e **Flask**.
- **Automação de Tarefas**: ideal para scripts que economizam tempo.
- **Análise de Dados**: usada em pesquisas científicas, universidades e mercado financeiro.
- **Aplicações em Sistemas Embarcados e IoT**.

> 🧠 *Aprender Python no Ensino Médio é uma vantagem competitiva para qualquer estudante técnico.*

------

## 👨‍🎓 Exemplo Didático

A seguir, o tradicional **“Olá, Mundo!”**, primeiro programa que se escreve em qualquer linguagem de programação:

```python
# Este é o seu primeiro programa em Python!
print("Olá, mundo!")
```

### 🧾 Explicação do Código

- `# Este é o seu primeiro programa em Python!`
  → Comentário que **não será executado** pelo Python. Comentários começam com `#` e servem para explicar o código.
- `print("Olá, mundo!")`
  → Esta linha **imprime uma mensagem na tela**. A função `print()` é usada para exibir textos e valores no terminal.

------

## 🧭 Conclusão

Python é uma linguagem:

✅ Intuitiva
✅ Poderosa
✅ Versátil
✅ Presente em quase todas as áreas da computação moderna

> ✨ *Se você domina Python, pode criar desde jogos até sistemas bancários, robôs, sites, dashboards e ferramentas de automação.*

------

## 🔗 Referências

- [Documentação Oficial do Python (PT-BR)](https://docs.python.org/pt-br/)
- [Curso em Vídeo – Python para Iniciantes (Gustavo Guanabara)](https://www.youtube.com/playlist?list=PLHz_AreHm4dm6wYOIW20Nyg12TAjmMGT-)
- [Python.org – Página Oficial da Linguagem](https://www.python.org/)

------

# ⚙️ 0.2 Instalar o Python

> 💡 *"Para escrever código, é preciso preparar o ambiente. Assim como um artista prepara o estúdio antes de pintar."*

------

## 🧩 O que é necessário para programar em Python?

Antes de começar a codar, precisamos preparar 3 elementos básicos:

1. ✅ **O interpretador do Python** – É o programa que executa os seus códigos.
2. ✅ **Um editor de código** – Pode ser o **VSCode** ou outro que você prefira.
3. ✅ **Um terminal ou console** – Onde você verá os resultados do seu código.

------

## 🪟 Instalação no Windows

### 🛠️ Passo a passo:

1. **Acesse o site oficial**:
   https://www.python.org/downloads/

2. Clique em **"Download Python 3.x.x"**
   (a versão mais recente será exibida em destaque).

3. **Execute o instalador** baixado.

4. Marque a opção **“Add Python to PATH”** antes de clicar em “Install Now”

   > ⚠️ Essa etapa é MUITO importante. Sem isso, você não conseguirá usar o Python no terminal.

5. Aguarde a instalação e clique em **Close**.

------

### ✅ Verificar a instalação

Abra o **Prompt de Comando (cmd)** e digite:

```bash
python --version
```

Se aparecer algo como:

```
Python 3.12.1
```

Significa que a instalação foi feita com sucesso!

------

## 🐧 Instalação no Linux (Zorin OS, Ubuntu, Linux Mint)

A maioria das distribuições baseadas em Debian (como **Ubuntu**, **Zorin OS**, **Linux Mint**) já vem com Python instalado. Mas é fundamental entender como verificar, instalar e configurar o ambiente corretamente.

### 🔧 Passo a passo para instalar e configurar o Python 3

Abra o **terminal** (atalho: `Ctrl + Alt + T`) e execute os seguintes comandos, **um por vez**:

```bash
sudo apt update
sudo apt install python3
```

🔎 Verifique a instalação:

```bash
python3 --version
```

Se aparecer algo como:

```
Python 3.12.1
```

✅ **Parabéns! Python 3 está instalado corretamente.**

------

### 🧩 Tornar o comando `python` equivalente a `python3`

Por padrão, em muitas distribuições Linux o comando `python` ainda se refere ao Python 2 (ou nem existe).

Para resolver isso e garantir que ao digitar `python` o sistema execute o Python 3, instale o seguinte pacote:

```bash
sudo apt install python-is-python3
```

📌 Esse pacote cria um **link simbólico**, fazendo com que o comando `python` funcione da mesma forma que `python3`.

> 🧠 *Dessa forma, seu terminal estará alinhado com a maioria dos tutoriais e exemplos atuais, que usam apenas `python`.*

------

### ✅ Verificações Finais

Após instalar o pacote, teste os dois comandos:

```bash
python --version
python3 --version
```

Ambos devem exibir a mesma versão do Python 3:

```
Python 3.12.1
```

------

### 🐍 Testar ambiente com um arquivo `.py`

1. Crie uma pasta chamada `meus_códigos` na sua pasta pessoal:

   ```bash
   mkdir ~/meus_códigos
   cd ~/meus_códigos
   ```

2. Crie um novo arquivo chamado `ola.py`:

   ```bash
   nano ola.py
   ```

3. Escreva este código:

   ```python
   print("Ambiente Python pronto para codar no Linux!")
   ```

4. Salve com `Ctrl + O` → Enter → `Ctrl + X`.

5. Execute o programa:

   ```bash
   python ola.py
   ```

> ✅ Se a frase for exibida, está tudo funcionando corretamente!

------

## 🖥️ Escolher um Editor de Código

O mais recomendado para iniciantes (e profissionais!) é o **Visual Studio Code (VSCode)**:

### 📥 Instalar o VSCode

- Site oficial: https://code.visualstudio.com/

### 📦 Extensões essenciais

Após abrir o VSCode, instale a extensão chamada **Python** (ícone azul com o logo da cobra).

### 💡 Outras opções de editores:

| Editor                | Indicação                         |
| --------------------- | --------------------------------- |
| **Thonny**            | Para iniciantes absolutos         |
| **PyCharm Community** | Para projetos maiores             |
| **Sublime Text**      | Leve e rápido, mas menos amigável |

------

## 🧪 Testar no terminal (Windows ou Linux)

Crie um arquivo chamado `teste.py` com o seguinte conteúdo:

```python
print("Ambiente Python pronto para codar!")
```

### ▶️ Executar:

No terminal, digite:

```bash
python teste.py       # No Windows
python3 teste.py      # No Linux
```

------

## 🛟 Solução de Problemas Comuns

| Problema                                | Solução                                                      |
| --------------------------------------- | ------------------------------------------------------------ |
| `python` não é reconhecido no Windows   | Reinstale e **marque a opção “Add Python to PATH”**.         |
| O terminal abre mas fecha imediatamente | Use o terminal integrado do VSCode ou abra manualmente o cmd. |
| No Linux, `python` não funciona         | Use `python3` no lugar.                                      |
| Não sei onde salvar o arquivo `.py`     | Crie uma pasta específica, como `meus_programas_python`, e salve todos lá. |

------

## 🔗 Referências

- [Documentação Oficial – Instalação do Python](https://docs.python.org/pt-br/3/using/index.html)
- [Tutorial em Vídeo: Instalando Python no Windows (Curso em Vídeo)](https://www.youtube.com/watch?v=Vb0CXrYfzG4)
- [Baixar VSCode](https://code.visualstudio.com/)
- [Extensão Python no VSCode](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

------

# ▶️ 0.3 Executar o Primeiro Programa

> 🧠 *“A primeira linha de código é como a primeira pedalada de uma bicicleta: simples, mas cheia de possibilidades.”*

------

## 📦 O que é um script `.py`?

Em Python, qualquer arquivo de texto com extensão `.py` é chamado de **script Python**. Ele pode conter desde um simples comando até um sistema completo.

Você pode:

- Escrever o código no **terminal interativo**
- Ou salvar como **arquivo `.py`** e executar

------

## 💬 Usando o terminal interativo

Abra seu terminal e digite:

```bash
python
```

Ou, no Linux:

```bash
python3
```

Você verá algo como:

```
Python 3.12.1 (default, ...)
>>>
```

Esse `>>>` indica que você está no **modo interativo**. Agora digite:

```python
print("Olá, mundo!")
```

E a saída será:

```
Olá, mundo!
```

> ✅ Ideal para testes rápidos e entender a execução passo a passo.

Para sair, digite:

```python
exit()
```

ou pressione `Ctrl + D`.

------

## 📝 Escrevendo seu primeiro programa em arquivo `.py`

### 🧾 1. Criar um arquivo com o código

Abra o **VSCode**, clique em **"Novo Arquivo"** e salve como:

```text
primeiro_programa.py
```

Digite o seguinte código:

```python
# Este é o nosso primeiro programa em Python
print("Olá, mundo! Estou programando em Python.")
```

------

### 📂 2. Abrir o terminal na mesma pasta

No VSCode:

- Vá em **Terminal > Novo Terminal**
- Verifique se a pasta atual está correta
- Ou use o comando `cd` para ir até ela:

```bash
cd caminho/para/sua/pasta
```

------

### ▶️ 3. Executar o programa

No terminal, digite:

```bash
python primeiro_programa.py      # Windows
```

Ou:

```bash
python3 primeiro_programa.py     # Linux
```

A saída será:

```
Olá, mundo! Estou programando em Python.
```

> 🎉 Parabéns! Você executou seu primeiro script Python!

------

## 📚 Explicando o Código

```python
# Este é o nosso primeiro programa em Python
print("Olá, mundo! Estou programando em Python.")
```

### 🔍 Linha a linha:

- `# Este é o nosso primeiro programa...`
   → Comentário. O Python **ignora** tudo após `#`. Use para **explicar o código**.
- `print(...)`
   → Função que **exibe um texto no terminal**. Neste caso, mostra a mensagem `"Olá, mundo!..."`.

------

## 🖥️ Terminal, Console e Editor: Qual a diferença?

| Termo        | Explicação                                                   |
| ------------ | ------------------------------------------------------------ |
| **Terminal** | Interface para digitar comandos diretamente para o sistema operacional |
| **Console**  | Área no VSCode ou IDLE onde o resultado do código é mostrado |
| **Editor**   | Local onde o código é escrito (como o VSCode, PyCharm ou Sublime Text) |

> 📌 A combinação **Editor + Terminal** forma o ambiente de desenvolvimento completo.

------

## 🧠 Dica Final

Você pode combinar vários comandos em um mesmo arquivo `.py`, como:

```python
print("Olá!")
print("Seja bem-vindo ao Python.")
print("Vamos aprender juntos!")
```

E verá:

```bash
Olá!
Seja bem-vindo ao Python.
Vamos aprender juntos!
```

------

## 🔗 Referências

- [Documentação Oficial – Função print()](https://docs.python.org/pt-br/3/library/functions.html#print)
- [Primeiro Programa em Python (Vídeo)](https://www.youtube.com/watch?v=T5pRlIbr6gg)
- [Curso Python – Execução de Código (Guanabara)](https://www.cursoemvideo.com/curso/python-3-mundo-1/aula/3-executando-o-seu-primeiro-codigo/)

------

