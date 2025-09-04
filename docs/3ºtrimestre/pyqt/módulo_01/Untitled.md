# Tutorial PyQt5 com Ambiente Virtual

## 1. **Criar diretório de projetos**

```bash
mkdir pyqt && cd pyqt
```

## 2. **Verificar versão do Python**

```bash
python3 --version
```

✅ Esperado: **Python 3.12.x** ou superior

## 3. **Criar ambiente virtual (`venv`)**

```bash
python3 -m venv venv
```

## 4. **Ativar o ambiente virtual**

```bash
source venv/bin/activate
```

💡 **Indicador visual**: Após ativar, o terminal deve exibir `(venv)` no início da linha.

## 5. **Atualizar pip dentro do ambiente virtual**

```bash
pip install --upgrade pip
```

## 6. **Instalar ferramentas essenciais**

```bash
pip install setuptools wheel
```

## 7. **Instalar PyQt5 dentro do venv**

```bash
pip install pyqt5
```

## 8. **Verificar instalação**

```bash
python -m PyQt5.QtCore
```

✅ **Se não houver erro** → instalação concluída com sucesso

## 9. **Para desativar o ambiente virtual** (quando terminar)

```bash
deactivate
```

## 10. **Para reativar o ambiente virtual** (em sessões futuras)

```bash
# No diretório do projeto
source venv/bin/activate
```

---

## 📝 **Comandos Úteis para Gerenciamento do Ambiente**

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