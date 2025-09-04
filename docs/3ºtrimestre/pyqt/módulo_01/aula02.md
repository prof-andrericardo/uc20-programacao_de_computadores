# 📗 Aula 2 — Instalação do Python 3.12 e PyQt5 no Kubuntu 24.04

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
 ![Kubuntu](https://img.shields.io/badge/Kubuntu-24.04-0079C1?logo=kde&logoColor=white)
 ![PyQt5](https://img.shields.io/badge/Framework-PyQt5-41CD52?logo=qt&logoColor=white)
 ![Terminal](https://img.shields.io/badge/Ferramenta-Terminal-black?logo=gnu-bash&logoColor=white)

> 💬 *“Antes de programar com PyQt5, precisamos preparar o terreno: o ambiente de desenvolvimento.”*

------

## 🎯 Objetivos da Aula

- Verificar a versão do **Python 3.12+** no Kubuntu 24.04.
- Atualizar ferramentas essenciais (`pip`, `setuptools`, `wheel`).
- Instalar o **PyQt5** dentro de um ambiente virtual.
- Validar a instalação rodando um **primeiro teste prático**.

------

## 1) 🐍 Verificando o Python instalado

Kubuntu 24.04 já traz o Python por padrão. Vamos confirmar a versão:

```bash
python3 --version
```

🔎 **Saída esperada:**

```
Python 3.12.x
```

Se a versão for **menor que 3.12**, será necessário atualizar via `apt` ou instalar manualmente (explicaremos em materiais extras, se necessário).

------

## 2) 📦 Atualizando ferramentas básicas

Mesmo que o Python esteja atualizado, o **pip** pode estar desatualizado. Vamos garantir que tudo esteja em ordem:

```bash
python3 -m pip install --upgrade pip setuptools wheel
```

- `pip` → gerenciador de pacotes Python.
- `setuptools` → auxilia na instalação de bibliotecas.
- `wheel` → formato moderno de distribuição de pacotes.

💡 **Boa prática**: sempre atualizar antes de instalar novos pacotes.

------

## 3) 📁 Criando diretório do projeto

Organizar o trabalho desde o início é essencial.

```bash
mkdir pyqt && cd pyqt
```

- `mkdir pyqt` → cria a pasta do projeto.
- `cd pyqt` → entra na pasta.

------

## 4) 🌱 Criando o ambiente virtual (`venv`)

Ambientes virtuais isolam as dependências de cada projeto.

```bash
python3 -m venv venv
source venv/bin/activate
```

- `python3 -m venv venv` → cria a pasta `venv` com o ambiente.
- `source venv/bin/activate` → ativa o ambiente virtual.

🔎 Quando ativado, o terminal mostrará `(venv)` no início da linha.

📌 Para desativar:

```bash
deactivate
```

------

## 5) 📥 Instalando o PyQt5

Agora sim, vamos instalar o **PyQt5** dentro do `venv`.

```bash
pip install pyqt5
```

🔎 A saída mostrará algo como:

```
Successfully installed PyQt5-5.x.x
```

------

## 6) 🧪 Testando a instalação

Crie o arquivo `hello.py`:

```python
from PyQt5.QtWidgets import QApplication, QLabel, QWidget
import sys

# Cria a aplicação
app = QApplication(sys.argv)

# Cria a janela
janela = QWidget()
janela.setWindowTitle("Teste PyQt5")

# Adiciona um texto
rotulo = QLabel("Olá, PyQt5!", parent=janela)

# Exibe
janela.resize(300, 100)
janela.show()

# Executa o loop de eventos
sys.exit(app.exec())
```

Execute no terminal:

```bash
python hello.py
```

✅ Se aparecer uma janela com o texto **“Olá, PyQt5!”**, está tudo pronto!

------

## 7) 🩹 Solução de problemas comuns

- ❌ `ModuleNotFoundError: No module named 'PyQt5'`
   → Verifique se o `venv` está ativo antes de instalar.
- ❌ Janela não abre no Kubuntu
   → Confirme se está em ambiente gráfico (não WSL sem X11).
- ❌ Permissão negada no `pip`
   → Ative o `venv`; nunca instale global sem necessidade.

------

## ✅ Checklist da Aula 2

-  Verifiquei a versão do Python (3.12+).
-  Atualizei `pip`, `setuptools` e `wheel`.
-  Criei a pasta `pyqt` e entrei nela.
-  Configurei o ambiente virtual (`venv`).
-  Instalei o PyQt5 dentro do ambiente.
-  Executei o app `hello.py` com sucesso.

------

## 🧪 Exercícios Práticos

1. **Verificação de versão**
   - Digite `python3 --version` e anote a saída.
   - Se não for 3.12+, pesquise como atualizar.
2. **Criação de ambiente**
   - Crie uma pasta chamada `meu_primeiro_pyqt`.
   - Dentro dela, crie um `venv` chamado `ambiente`.
   - Ative-o e instale o PyQt5.
3. **Rodando o Hello World**
   - Reescreva o código `hello.py`.
   - Altere o título da janela para **“Meu Primeiro App”**.
   - Troque a mensagem para **“Estou aprendendo PyQt5 no Kubuntu!”**.

------

## ❓ Perguntas de Fixação

1. Para que serve o **pip**?
2. Qual a vantagem de usar um **venv** em projetos Python?
3. Qual comando ativa o ambiente virtual no Linux?
4. O que acontece se rodarmos um app PyQt5 sem `app.exec()`?

------

## 🧠 Desafio

Crie um app chamado `saudacao.py` que:

- Mostra uma janela com o título **“Saudação Personalizada”**.
- Contém um `QLabel` escrito **“Seja bem-vindo ao PyQt5 no Kubuntu!”**.
- Altere a cor de fundo da janela para cinza claro.

------

🔭 **Próxima aula:**
 👉 **Aula 3 — Criação e uso de ambientes virtuais (`venv`) em projetos PyQt5**.

