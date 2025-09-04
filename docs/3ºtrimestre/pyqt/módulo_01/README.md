# 📘 Módulo 1 – Preparação do Ambiente

👨‍🏫 **Professor:** André Ricardo da Silva  
🏫 **Colégio Victorino – UC20: Programação de Computadores**  
💻 **Ambiente:** Kubuntu 24.04 + Python 3.12+ + PyQt5 + VSCode  

---

## 🚀 Checklist de Preparação do Ambiente

Antes de iniciar os estudos em PyQt5, siga este passo a passo para configurar corretamente seu ambiente no **Kubuntu 24.04**.

1. **Criar diretório de projetos**

```bash
mkdir pyqt && cd pyqt
```

2. **Verificar versão do Python**

```bash
python3 --version
```

✅ Esperado: **Python 3.12.x** ou superior

3. **Criar ambiente virtual (`venv`)**

```bash
python3 -m venv venv
```

4. **Ativar o ambiente virtual**

```bash
source venv/bin/activate
```

💡 **Indicador visual**: Após ativar, o terminal deve exibir `(venv)` no início da linha.

5. **Atualizar pip dentro do ambiente virtual**

```bash
pip install --upgrade pip
```

6. **Instalar ferramentas essenciais**

```bash
pip install setuptools wheel
```

7. **Instalar PyQt5 dentro do venv**

```bash
pip install pyqt5
```

8. **Verificar instalação**

```bash
python -m PyQt5.QtCore
```

✅ **Se não houver erro** → instalação concluída com sucesso

9. **Para desativar o ambiente virtual** (quando terminar)

```bash
deactivate
```

10. **Para reativar o ambiente virtual** (em sessões futuras)

```bash
# No diretório do projeto
source venv/bin/activate
```

---

📝 **Comandos Úteis para Gerenciamento do Ambiente**

```bash
# Verificar pacotes instalados no ambiente virtual
pip list

# Verificar informações do PyQt5 instalado
pip show pyqt5

# Congelar dependências em requirements.txt
pip freeze > requirements.txt

# Instalar dependências a partir do requirements.txt
pip install -r requirements.txt
```

## ⚠️ **Importante:**

- Sempre ative o ambiente virtual antes de trabalhar no projeto
- O ambiente virtual isola as dependências, evitando conflitos com o sistema
- O pip será atualizado apenas dentro do ambiente virtual, não afetando o sistema

Este método é a **melhor prática** para desenvolvimento Python no Kubuntu 24.04! 🚀

---

1. **Instalar extensões recomendadas no VSCode**

   - Python (Microsoft)
   - Pylance
   - Qt Tools
   - Material Icon Theme

2. **Selecionar o interpretador do VSCode**

   - Atalho: `Ctrl+Shift+P` → *Python: Select Interpreter* → escolha o `venv`.

3. **Criar primeiro app de teste**
   Arquivo: `hello.py`

   ```python
   from PyQt5.QtWidgets import QApplication, QLabel, QWidget
   import sys
   
   app = QApplication(sys.argv)
   window = QWidget()
   window.setWindowTitle("Teste PyQt5")
   label = QLabel("Olá, PyQt5!", window)
   window.show()
   sys.exit(app.exec())
   ```

4. **Executar o app**

   ```bash
   python hello.py
   ```

5. **Boas práticas extras**

    - Criar um `requirements.txt`:

      ```bash
      pip freeze > requirements.txt
      ```

    - Reativar o ambiente em novas sessões:

      ```bash
      source venv/bin/activate
      ```

    - Manter estrutura organizada:

      ```
      pyqt/
      ├── venv/
      ├── src/
      ├── tests/   (opcional)
      └── docs/
      ```

------

## 📑 Índice de Aulas

### 1. Introdução ao PyQt5 e às GUIs em Python

- O que são **GUIs (Interfaces Gráficas de Usuário)**
- Diferenças entre **programas de terminal** e **programas gráficos**
- Onde o PyQt5 é aplicado no mundo real
- Exemplos de softwares famosos que usam Qt

------

### 2. Instalação do Python 3.12 e PyQt5 no Kubuntu 24.04

- Verificando a versão instalada do Python
- Atualizando pacotes essenciais do sistema
- Instalação do `pip` e boas práticas de uso
- Instalação do **PyQt5** com `pip`

------

### 3. Criação de ambiente virtual com `venv`

- O que é um ambiente virtual e por que utilizá-lo
- Criando o diretório de projetos
- Criando e ativando o `venv`
- Instalando o **PyQt5** dentro do ambiente virtual

------

### 4. Configuração do VSCode e principais extensões

- Escolha do editor: por que o VSCode
- Configurando o **interpretador Python** para o `venv`
- Extensões recomendadas:
  - Python (Microsoft)
  - Pylance
  - Qt Tools
  - Material Icon Theme
- Configuração básica do terminal integrado

------

### 5. Estrutura básica de um app PyQt5 (Code Burger 🍔)

- Os 5 passos fundamentais:
  1. Importar módulos
  2. Criar aplicação (`QApplication`)
  3. Criar widgets
  4. Organizar em layout
  5. Executar o app
- Explicação do loop de eventos
- Exemplo mínimo de “Olá, Mundo!” no PyQt5

------

### 6. Widgets iniciais: `QLabel`, `QPushButton`, `QLineEdit`

- Introdução ao conceito de **widgets**
- Usando `QLabel` para exibir textos
- Criando botões com `QPushButton`
- Campos de entrada de texto com `QLineEdit`
- Propriedades básicas (texto, tamanho, alinhamento)

------

### 7. Layouts: `QVBoxLayout`, `QHBoxLayout`, `QGridLayout`

- O que são layouts e por que utilizá-los
- `QVBoxLayout` → disposição vertical
- `QHBoxLayout` → disposição horizontal
- `QGridLayout` → organização em tabela
- Combinação de layouts em um mesmo app

------

### 8. Eventos e interação com `.clicked.connect()`

- O que são eventos em uma GUI
- Conectando botões a funções (`.clicked.connect(func)`)
- Atualizando widgets em resposta a eventos
- Exemplo prático: botão que altera o texto de um `QLabel`

------

## ✅ Conclusão do Módulo 1

Ao final deste módulo, você será capaz de:

- Configurar o **ambiente Python 3.12+** no Kubuntu 24.04
- Criar e usar ambientes virtuais com `venv`
- Configurar o **VSCode** com extensões adequadas
- Criar **apps simples em PyQt5** com widgets, layouts e eventos