# **4. Escopo e Variáveis**

### **4.1 Escopo local e global**

O escopo de uma variável determina onde ela pode ser acessada dentro do programa. Em Python, existem dois principais tipos de escopo:

- **Escopo local:** Variáveis definidas dentro de uma função. Elas só existem e podem ser usadas enquanto a função está sendo executada.
- **Escopo global:** Variáveis definidas fora de qualquer função. Elas podem ser acessadas em qualquer parte do programa.

#### **Exemplo: Escopo local e global**

```python
# Variável global
global_var = "Eu sou global!"

def exemplo_escopo():
    # Variável local
    local_var = "Eu sou local!"
    print(local_var)
    print(global_var)

# Chamando a função
exemplo_escopo()

# Tentando acessar a variável local fora da função
# print(local_var)  # Isso gera um erro
```

**Explicação:**

1. `global_var` é uma variável global e pode ser acessada tanto dentro quanto fora da função.
2. `local_var` é uma variável local e só pode ser usada dentro da função `exemplo_escopo`.
3. Tentar acessar `local_var` fora da função gera um erro.

------

### **4.2 Uso de `global` para modificar variáveis globais**

Normalmente, uma função não pode modificar uma variável global diretamente. Para fazer isso, usamos a palavra-chave `global`.

#### **Exemplo: Modificando uma variável global**

```python
contador = 0  # Variável global

def incrementar():
    global contador  # Declarando que iremos modificar a variável global
    contador += 1
    print(f"Contador dentro da função: {contador}")

# Chamando a função
incrementar()
incrementar()

# Verificando o valor da variável global
print(f"Contador fora da função: {contador}")
```

**Explicação:**

1. `global contador` permite que a função `incrementar` modifique a variável global `contador`.
2. Cada chamada da função aumenta o valor de `contador` globalmente.

**Atenção:** Use `global` com cuidado, pois modificar variáveis globais pode tornar o código mais difícil de entender e depurar.

------

### **4.3 Boas práticas para evitar conflitos de escopo**

Conflitos de escopo podem ocorrer quando variáveis locais e globais têm o mesmo nome, o que pode causar confusão. Para evitar problemas:

1. **Use variáveis locais sempre que possível:** Isso reduz o risco de modificar acidentalmente uma variável global.
2. **Escolha nomes descritivos para variáveis:** Nomes claros ajudam a identificar o propósito de cada variável e evitam conflitos.
3. **Evite o uso excessivo de `global`:** Sempre prefira passar variáveis como argumentos ou usar o retorno de funções para compartilhar dados.

#### **Exemplo: Boas práticas de nomenclatura**

```python
def calcular_total(preco, quantidade):
    total = preco * quantidade  # Variável local
    return total

# Chamando a função
resultado = calcular_total(10, 5)
print(f"O total é: {resultado}")
```

**Explicação:**

1. O nome da variável local `total` é claro e descreve seu propósito.
2. O uso de variáveis locais torna a função mais modular e segura.

------

### **4.4 Exemplos de como escopos influenciam o comportamento de funções**

#### **Exemplo 1: Variável local com mesmo nome que uma global**

```python
valor = 100  # Variável global

def redefinir_valor():
    valor = 50  # Variável local
    print(f"Valor dentro da função: {valor}")

# Chamando a função
redefinir_valor()

# Verificando o valor da variável global
print(f"Valor fora da função: {valor}")
```

**Explicação:**

1. Dentro da função, `valor` é uma variável local e não afeta a variável global de mesmo nome.
2. Fora da função, o valor global permanece inalterado.

#### **Exemplo 2: Modificando uma variável global explicitamente**

```python
valor = 100  # Variável global

def alterar_valor_global():
    global valor
    valor = 50  # Modifica a variável global
    print(f"Valor dentro da função: {valor}")

# Chamando a função
alterar_valor_global()

# Verificando o valor da variável global
print(f"Valor fora da função: {valor}")
```

**Explicação:**

1. Usando `global`, a função `alterar_valor_global` modifica a variável global `valor`.
2. O valor da variável global é alterado para 50 dentro e fora da função.

------

### **Conclusão**

Neste capítulo, aprendemos sobre:

- **Escopo local e global:** Onde as variáveis podem ser usadas e como isso afeta o código.
- **Uso da palavra-chave `global`:** Permite modificar variáveis globais dentro de funções, mas deve ser usada com cautela.
- **Boas práticas:** Evitar conflitos de escopo ao usar variáveis locais e nomes descritivos.
- **Impacto do escopo no comportamento:** Exemplos práticos que mostram como o escopo influencia a execução do programa.

Pratique criando funções que utilizem variáveis locais e globais para entender melhor como elas interagem no Python!