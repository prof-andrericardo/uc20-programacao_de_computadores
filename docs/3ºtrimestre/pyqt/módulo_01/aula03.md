# 📗 Aula 3 — Criação e Uso de Ambientes Virtuais com `venv`

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
 ![Kubuntu](https://img.shields.io/badge/Kubuntu-24.04-0079C1?logo=kde&logoColor=white)
 ![PyQt5](https://img.shields.io/badge/Framework-PyQt5-41CD52?logo=qt&logoColor=white)
 ![Terminal](https://img.shields.io/badge/Ferramenta-Terminal-black?logo=gnu-bash&logoColor=white)

> 💬 *“Um bom programador não cria apenas código, mas também organiza seu ambiente de trabalho.”*

------

## 🎯 Objetivos da Aula

- Entender o que é um **ambiente virtual** e sua importância.
- Criar, ativar e desativar ambientes virtuais com `venv`.
- Instalar pacotes (como o PyQt5) dentro do `venv`.
- Adotar boas práticas de organização de projetos Python.

------

## 1) 🌱 O que é um ambiente virtual?

Um **ambiente virtual** é como uma **caixa isolada** onde você instala pacotes Python apenas para um projeto específico.

### 🔎 Vantagens do `venv`:

- Isola pacotes de cada projeto.
- Evita conflitos de versões.
- Permite ter **projetos diferentes** usando versões diferentes da mesma biblioteca.
- Facilita o compartilhamento com outros desenvolvedores (usando `requirements.txt`).

📌 Exemplo prático:

- Projeto A precisa do **PyQt5 5.15**.
- Projeto B precisa do **PyQt5 5.13**.
   Com `venv`, cada projeto tem sua própria versão, sem conflito.

------

## 2) 📁 Criando um ambiente virtual

Primeiro, crie uma pasta de projetos:

```bash
mkdir meus_projetos && cd meus_projetos
```

Agora, crie o ambiente virtual chamado `venv`:

```bash
python3 -m venv venv
```

📌 Isso cria uma pasta chamada `venv/` contendo tudo que o Python precisa para rodar isoladamente.

------

## 3) 🔑 Ativando e desativando o `venv`

### Ativar no Linux (Kubuntu 24.04):

```bash
source venv/bin/activate
```

🔎 Ao ativar, o terminal exibirá algo assim:

```
(venv) usuario@pc:~/meus_projetos$
```

### Desativar:

```bash
deactivate
```

💡 Sempre **ative** o `venv` antes de instalar pacotes do projeto.

------

## 4) 📦 Instalando pacotes no ambiente

Com o `venv` ativo, instale o **PyQt5**:

```bash
pip install pyqt5
```

Verifique os pacotes instalados:

```bash
pip list
```

Exporte as dependências para compartilhar:

```bash
pip freeze > requirements.txt
```

Isso gera o arquivo `requirements.txt`, que pode ser usado em outra máquina com:

```bash
pip install -r requirements.txt
```

------

## 5) 🧰 Estrutura de diretórios recomendada

```bash
meus_projetos/
├── venv/          # ambiente virtual
├── src/           # código-fonte do projeto
│   └── hello.py
├── docs/          # documentação
└── requirements.txt
```

📌 Essa organização ajuda os alunos a separarem **código, ambiente e documentação**.

------

## 6) 🧪 Testando com um app PyQt5

Crie a pasta `src/` e o arquivo `app.py`:

```python
from PyQt5.QtWidgets import QApplication, QWidget, QLabel
import sys

app = QApplication(sys.argv)

janela = QWidget()
janela.setWindowTitle("App com venv")
rotulo = QLabel("PyQt5 rodando dentro do venv ✅", parent=janela)

janela.resize(300, 100)
janela.show()

sys.exit(app.exec())
```

Execute:

```bash
python src/app.py
```

✅ Se abrir a janela, significa que o ambiente está funcionando corretamente.

------

## 7) 🩹 Erros comuns

- ❌ Instalei pacotes fora do `venv`.
  - 🔎 Solução: ative o `venv` com `source venv/bin/activate` antes do `pip install`.
- ❌ O terminal não mostra `(venv)`.
  - 🔎 Solução: o ambiente não está ativo. Rode novamente `source venv/bin/activate`.
- ❌ Projeto não roda em outra máquina.
  - 🔎 Solução: use `requirements.txt` para replicar dependências.

------

## ✅ Checklist da Aula 3

-  Sei o que é um `venv` e sua utilidade.
-  Consigo criar e ativar/desativar ambientes virtuais.
-  Instalei pacotes (PyQt5) dentro do ambiente.
-  Organizei o projeto com boas práticas de diretórios.
-  Rodei um app PyQt5 dentro do `venv`.

------

## 🧪 Exercícios Práticos

1. Crie uma pasta chamada **`uc20_projetos`**.

   - Dentro dela, crie um `venv`.
   - Ative-o e instale o PyQt5.

2. Crie um arquivo `test_venv.py` que imprime a mensagem:

   ```
   Ambiente virtual ativo e PyQt5 funcionando!
   ```

3. Gere um `requirements.txt` e simule a reinstalação dos pacotes usando:

   ```bash
   pip install -r requirements.txt
   ```

------

## ❓ Perguntas de Fixação

1. Qual a principal vantagem de usar `venv` em projetos Python?
2. Qual comando ativa o ambiente virtual no Kubuntu 24.04?
3. Por que devemos exportar um `requirements.txt`?
4. O que acontece se tentarmos usar o PyQt5 fora do `venv`?

------

## 🧠 Desafio

Crie um projeto chamado **`meu_primeiro_app`** com a seguinte estrutura:

```
meu_primeiro_app/
├── venv/
├── src/
│   └── contador.py
└── requirements.txt
```

O arquivo `contador.py` deve exibir uma janela com:

- Um `QLabel` mostrando **“Valor: 0”**.
- Dois botões: **“+1”** e **“–1”** que alteram o valor.

> 🔹 **Bônus:** adicione um botão **“Zerar”**.

------

🔭 **Próxima aula:**
 👉 **Aula 4 — Configuração do VSCode e principais extensões** para produtividade com PyQt5.