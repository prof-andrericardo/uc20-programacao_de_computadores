# 📗 Aula 1 — Introdução ao PyQt5 e às GUIs em Python

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
 ![Kubuntu](https://img.shields.io/badge/Kubuntu-24.04-0079C1?logo=kde&logoColor=white)
 ![PyQt5](https://img.shields.io/badge/PyQt-5.x-41CD52?logo=qt&logoColor=white)
 ![VSCode](https://img.shields.io/badge/Editor-VSCode-007ACC?logo=visualstudiocode&logoColor=white)

> 💬 *“Interfaces são pontes: quando bem construídas, o usuário atravessa sem perceber.”*

------

## 🎯 Objetivos de Aprendizagem

- Entender o que é **GUI** e por que utilizá-la.
- Conhecer o **PyQt5** e onde ele se encaixa no ecossistema Python.
- Aprender os **conceitos-chave**: *widgets*, *layouts*, *sinais* e *slots*, *loop de eventos*.
- Memorizar o **fluxo básico** de um app PyQt5 (*Code Burger* 🍔).
- Criar e executar o **primeiro app** (exemplo mínimo + exemplo com interação).

> ℹ️ **Importante**: a configuração do ambiente (Python 3.12+, `venv`, PyQt5, VSCode) será feita na **Aula 2**. Hoje focaremos em **conceitos** e **código mínimo**, para consolidar a base teórica e mental.

------

## 1) 🌐 O que é GUI?

**GUI** (*Graphical User Interface*) é a interface que permite o uso do computador via **elementos visuais**:

- **Botões** 🖱️, **rótulos** (textos), **caixas de entrada** ⌨️, **menus** 📂, **caixas de diálogo** 🪟.
- Facilita a vida do usuário, tornando a aplicação **mais intuitiva** e **acessível**.

### CLI x GUI — diferenças práticas

| Aspecto              | CLI (Terminal)     | GUI (Janela)                      |
| -------------------- | ------------------ | --------------------------------- |
| Interação            | Comandos digitados | Clique, arrastar, campos de texto |
| Curva de aprendizado | Maior              | Menor                             |
| Automação            | Excelente          | Possível (menos comum)            |
| Usuários             | Devs, admins       | Usuário geral e devs              |

> 📌 **Conclusão**: CLI e GUI **se complementam**. Em UC20, aprender GUI expande sua capacidade de construir ferramentas **amigáveis** para usuários.

------

## 2) 🧩 Onde entra o PyQt5?

**PyQt5** é um *binding* (ponte) que permite usar, em **Python**, o poder do **Qt** (framework C++ para GUIs).

- Você escreve **Python**, mas utiliza componentes Qt (estáveis, maduros e multiplataforma).
- Exemplos de softwares baseados em Qt: **QGIS**, **Anki**, **Spyder IDE**, parte da UI do **Blender**.

### Arquitetura simplificada (o trio que mais usaremos)

- `PyQt5.QtWidgets` → **componentes de interface** (janelas, botões, caixas de texto, layouts…).
- `PyQt5.QtCore` → **infraestrutura** (tipos, *signals/slots*, *timers*, *threads*).
- `PyQt5.QtGui` → **aparência e eventos** (fontes, ícones, cores, eventos de teclado/mouse).

------

## 3) 🧠 Conceitos-chave que você precisa dominar

- **Widget** → componente visível (ex.: `QPushButton`, `QLabel`, `QLineEdit`).
- **Janela** → “container” principal (ex.: `QWidget` ou `QMainWindow`).
- **Layout** → organiza widgets na tela (**vertical**, **horizontal**, **grade**).
- **Sinal (signal)** → “um evento aconteceu” (ex.: *botão foi clicado*).
- **Slot** → função **chamada** em resposta a um sinal (ex.: *atualizar texto*).
- **Loop de eventos** → coração da GUI: um laço que escuta e distribui eventos.

> 🧭 **Regra de ouro**: 1 **aplicação** (`QApplication`) por programa; **use layouts** (evite posicionamento absoluto com x/y).

------

## 4) 🍔 Code Burger — o fluxo mental de *todo* app PyQt5

1. **Importar módulos**
2. **Criar a aplicação** (`QApplication`)
3. **Criar/Configurar a janela e widgets**
4. **Montar os layouts**
5. **Exibir a janela** `show()` e **rodar o loop** `app.exec()`

> 💡 Memorize: isso se repete **sempre** — de um “Olá, mundo!” a um sistema completo.

------

## 5) 👋 Primeiro app: *Hello, PyQt5* (mínimo viável)

> Exemplo para fixar o **Code Burger**. Execute quando a Aula 2 estiver concluída.

```python
# 1) Importações essenciais
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QLabel

# 2) Cria a aplicação (apenas UMA por programa)
app = QApplication(sys.argv)   # gerencia o loop de eventos e o ciclo de vida da GUI

# 3) Cria a janela principal (container)
janela = QWidget()             # QWidget é uma janela genérica (sem barra de menus por padrão)
janela.setWindowTitle("Olá, PyQt5!")   # título exibido na barra da janela

# 4) Cria um widget de texto (rótulo) e define a janela como pai
rotulo = QLabel("Bem-vindo ao PyQt5 👋", parent=janela)  # parent=janela acopla o rótulo à janela

# 5) Configurações visuais e exibição
janela.resize(320, 120)        # largura x altura (opcional, só para ficar mais “bonito”)
janela.show()                  # torna a janela visível na tela

# 6) Inicia o loop de eventos (bloqueia aqui até a janela ser fechada)
sys.exit(app.exec())           # use .exec() (Qt5 recente); .exec_() em versões mais antigas
```

### 🧩 Por dentro do exemplo

- **`QApplication`**: sem ele, **não há GUI** (é o motor do app).
- **`QWidget`**: janela “crua”; ideal para exemplos e telas simples.
- **`QLabel`**: mostra texto; ao passar `parent=janela`, o label “vive” dentro da janela.
- **`show()` + `exec()`**: sem isso, **nada aparece**.

------

## 6) 🖱️ Interação: botão que altera o texto (sinal → slot)

> Agora você “escuta” um evento e **reage** a ele.

```python
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QLabel, QPushButton, QVBoxLayout

# 1) Aplicação
app = QApplication(sys.argv)

# 2) Janela
janela = QWidget()
janela.setWindowTitle("Interação Básica: Sinal e Slot")

# 3) Widgets
rotulo = QLabel("Clique no botão para alterar este texto.")
botao  = QPushButton("Clique aqui")

# 4) Lógica (slot) - função chamada quando o sinal for emitido
def mudar_texto():
    rotulo.setText("Texto alterado com sucesso ✅")

# 5) Conexão sinal → slot
botao.clicked.connect(mudar_texto)   # quando o botão é clicado, chama mudar_texto()

# 6) Layout (vertical)
layout = QVBoxLayout()
layout.addWidget(rotulo)
layout.addWidget(botao)
janela.setLayout(layout)             # aplica o layout na janela

# 7) Exibir
janela.resize(360, 160)
janela.show()
sys.exit(app.exec())
```

### 🧠 O que você aprendeu aqui

- **Sinal**: `clicked` (do botão)
- **Slot**: `mudar_texto()` (sua função)
- **Conexão**: `botao.clicked.connect(mudar_texto)`

> ✅ Padrão mental: *evento do usuário* → *sinal* → *minha função (slot)* → *atualiza a interface*.

------

## 7) 🧱 Layouts na prática (organização que se adapta)

> Layouts “responsivos” evitam posicionamento fixo (x, y). Eles **reorganizam** os widgets quando a janela muda de tamanho.

- **`QVBoxLayout`**: empilha de cima para baixo.
- **`QHBoxLayout`**: organiza lado a lado.
- **`QGridLayout`**: organiza em grade (linhas x colunas).

Exemplo (misto: HBox dentro de VBox):

```python
import sys
from PyQt5.QtWidgets import (
    QApplication, QWidget, QLabel, QPushButton,
    QVBoxLayout, QHBoxLayout
)

app = QApplication(sys.argv)

janela = QWidget()
janela.setWindowTitle("Layouts Múltiplos")

# Widgets
titulo = QLabel("Topo (explicação)")
btn_esq = QPushButton("← Esquerda")
btn_dir = QPushButton("Direita →")

# Linha horizontal (botões lado a lado)
linha = QHBoxLayout()
linha.addWidget(btn_esq)
linha.addWidget(btn_dir)

# Coluna vertical (título + linha de botões)
coluna = QVBoxLayout()
coluna.addWidget(titulo)
coluna.addLayout(linha)      # insere um layout dentro do outro!

janela.setLayout(coluna)
janela.resize(380, 180)
janela.show()

sys.exit(app.exec())
```

> 🧭 **Boa prática**: uma janela deve ter **um layout raiz**, mas você pode **aninhar** quantos layouts precisar.

------

## 8) 🩹 Diagnóstico rápido — erros comuns e soluções

- **Nada aparece?** 🔎
   → Verifique se chamou **`show()`** e **`app.exec()`**.
- **`ImportError: No module named PyQt5`?**
   → Instale no **venv** (Aula 2): `pip install pyqt5`.
- **“QApplication already exists”** (ou comportamento estranho)?
   → Garanta **apenas 1** `QApplication` por programa.
- **`.exec()` vs `.exec_()`**
   → Qt5 recente usa `.exec()`; em heranças antigas, `.exec_()`.

------

## 9) 🧰 Boas práticas desde o começo

- **Nomeação clara**: `janela_principal`, `btn_confirmar`, `lbl_status`.
- **Separação de responsabilidades**: (veremos em aulas futuras) lógica ↔ interface.
- **Use layouts** (sempre!) — evite *absolute positioning*.
- **Um app, um `QApplication`** — e finalize com `sys.exit(app.exec())`.

------

## ✅ Checklist da Aula 1 (autoavaliação)

-  Sei explicar **o que é GUI** e seus benefícios.
-  Sei o que são **widgets**, **layouts**, **sinais** e **slots**.
-  Memorizei o **Code Burger** (fluxo do app).
-  Rodei o **Hello, PyQt5** (após configurar o ambiente).
-  Consegui conectar um **clique** de botão a uma **função**.

------

## 🧪 Exercícios Práticos

1. **Olá, nome!**
   - Um `QLineEdit` para digitar o nome + um `QPushButton`.
   - Ao clicar, o `QLabel` deve exibir: **“Olá, `<nome>`!”**.
2. **Duas mensagens**
   - Crie dois botões: **“Mensagem A”** e **“Mensagem B”**.
   - Cada um seta um texto diferente no mesmo `QLabel`.
3. **Clique-contador (incremento)**
   - `QLabel` começa em “0”.
   - Cada clique em **“Contar”** incrementa +1 o valor exibido.

> 💡 Esses exercícios preparam para o **Projeto 1 (Contador +/–)** do Módulo 2.

------

## ❓ Perguntas de Fixação

1. Defina **GUI** e cite dois benefícios pedagógicos no contexto escolar.
2. Explique, com suas palavras, o que são **sinais** e **slots** no PyQt5.
3. Por que **`QApplication`** é obrigatório em qualquer app PyQt?
4. Qual a vantagem de usar **layouts** em vez de coordenadas fixas (x, y)?

------

## 🧠 Desafio (nível fácil)

Crie um app com:

- Um `QLabel`: **“Valor: 0”**.
- Dois botões: **“+1”** e **“–1”**.
- Ao clicar, atualize o número exibido.
- **Bônus**: adicione **“Zerar”** e impeça que o valor fique menor que **0**.

------

### 🔭 Próxima aula

**Aula 2 — Instalação no Kubuntu 24.04 (Python 3.12+, venv, PyQt5, VSCode)**: passo a passo no terminal, diagnóstico e verificação com um *Hello, PyQt5*.

