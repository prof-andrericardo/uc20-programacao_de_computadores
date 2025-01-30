# **5. Projetos Práticos**

Projetos práticos são fundamentais para consolidar os conceitos aprendidos na programação. Eles ajudam a conectar a teoria à prática e permitem que os alunos desenvolvam habilidades importantes, como resolver problemas e criar soluções eficientes. Nesta seção, abordaremos cinco projetos didáticos e progressivos, pensados para iniciantes que estão aprendendo Python.

------

## **5.1 Calculadora**

### **Introdução**

Uma calculadora é um dos projetos mais básicos e úteis para aprender os fundamentos da programação. Ela envolve conceitos essenciais, como entrada de dados, operadores matemáticos e lógica condicional. Vamos desenvolver este projeto de forma progressiva, começando com operações simples e evoluindo para funcionalidades mais avançadas.

### **Etapas de Desenvolvimento**

1. **Operações básicas:**
   - Inicialmente, a calculadora deve realizar apenas adição e subtração.
   - A lógica envolve:
     - Solicitar dois números ao usuário.
     - Perguntar a operação desejada (adição ou subtração).
     - Exibir o resultado da operação escolhida.
2. **Multiplicação e divisão:**
   - Adicione as operações de multiplicação e divisão.
   - A divisão deve incluir validação para evitar divisões por zero, exibindo uma mensagem de erro se isso ocorrer.
3. **Validação de entradas:**
   - Garanta que os valores inseridos pelo usuário sejam números.
   - Se o usuário digitar algo inválido, exiba uma mensagem de erro e solicite a entrada novamente.
4. **Interface amigável:**
   - Adicione mensagens claras para orientar o usuário, como "Escolha uma operação: 1 para Adição, 2 para Subtração...".
   - Permita que o usuário realize várias operações sem precisar reiniciar o programa.

------

## **5.2 Validador de Dados**

### **Introdução**

Validar dados é uma habilidade essencial em qualquer aplicação real. Neste projeto, os alunos aprenderão a verificar a validade de informações inseridas pelo usuário, como e-mails e CPFs.

### **Etapas de Desenvolvimento**

1. **Validação de e-mails:**
   - Um e-mail válido geralmente segue o padrão: "[texto@dominio.com](mailto:texto@dominio.com)".
   - A lógica envolve:
     - Verificar se o texto contém "@" e ".".
     - Garantir que haja texto antes e depois do "@".
     - Validar que o domínio termina com uma extensão comum, como ".com" ou ".org".
2. **Validação de CPFs:**
   - Um CPF válido possui 11 dígitos e segue um formato específico.
   - A lógica inclui:
     - Remover caracteres não numéricos, como pontos e traços.
     - Garantir que o CPF tenha exatamente 11 dígitos.
     - (Opcional para iniciantes) Implementar a lógica matemática que verifica a validade de um CPF usando os dígitos verificadores.
3. **Mensagens de erro claras:**
   - Se os dados forem inválidos, exiba mensagens específicas, como "O e-mail deve conter '@'." ou "O CPF deve ter 11 dígitos.".

------

## **5.3 Menu Interativo**

### **Introdução**

Menus interativos tornam os programas mais organizados e fáceis de usar. Neste projeto, os alunos aprenderão a criar um sistema dinâmico utilizando `match/case` (Python 3.10+) e loops.

### **Etapas de Desenvolvimento**

1. **Estrutura básica do menu:**
   - Apresente uma lista de opções para o usuário, como "1 - Calcular", "2 - Validar Dados" e "3 - Sair".
   - Use um loop para garantir que o menu continue sendo exibido até que o usuário escolha sair.
2. **Implementação das opções:**
   - Cada opção deve executar uma ação específica, como abrir a calculadora ou validar dados.
   - Utilize o comando `match/case` para organizar as opções do menu.
3. **Tratamento de entradas inválidas:**
   - Se o usuário digitar uma opção inválida, exiba uma mensagem, como "Opção inválida. Tente novamente.".

------

## **5.4 Processamento de Dados**

### **Introdução**

Processar dados é uma das tarefas mais comuns na programação. Neste projeto, os alunos aprenderão a contar palavras em um texto e calcular a frequência de letras, desenvolvendo habilidades em manipulação de strings.

### **Etapas de Desenvolvimento**

1. **Contagem de palavras:**
   - Solicite um texto ao usuário.
   - Divida o texto em palavras utilizando o método `.split()`.
   - Conte o número de palavras e exiba o resultado.
2. **Frequência de letras:**
   - Converta o texto para letras minúsculas para evitar duplicações causadas por diferenças de maiúsculas e minúsculas.
   - Use um dicionário para armazenar cada letra e sua respectiva contagem.
   - Exiba o número de vezes que cada letra aparece no texto.
3. **Melhorias adicionais:**
   - Ignore espaços e caracteres especiais ao calcular a frequência de letras.
   - Exiba os resultados de forma ordenada, como "A: 5, B: 3, C: 0...".

------

## **5.5 Jogos Simples**

### **Introdução**

Criar jogos simples é uma maneira divertida de praticar lógica e estruturas básicas de programação. Neste projeto, os alunos aprenderão a desenvolver três jogos clássicos.

### **Jogos e suas Lógicas**

1. **Pedra, Papel e Tesoura:**
   - O jogador escolhe entre pedra, papel ou tesoura.
   - O computador faz uma escolha aleatória.
   - As regras do jogo determinam o vencedor:
     - Pedra vence tesoura.
     - Tesoura vence papel.
     - Papel vence pedra.
2. **Jogo de Adivinhação:**
   - O programa escolhe um número aleatório dentro de um intervalo (por exemplo, 1 a 100).
   - O jogador tenta adivinhar o número, recebendo dicas como "Tente um número maior" ou "Tente um número menor".
   - O jogo termina quando o jogador acerta ou esgota as tentativas.
3. **Simulação de Dados:**
   - O jogador escolhe um número de lados para o dado (por exemplo, 6 lados para um dado comum).
   - O programa "rola" o dado e exibe o resultado.
   - Adicione a possibilidade de realizar várias rolagens e exibir estatísticas, como a frequência de cada número.

------

## **Conclusão**

Os projetos práticos apresentados são ótimos para consolidar os conceitos básicos de Python. Eles cobrem desde cálculos simples até validação de dados, processamento de texto e criação de jogos. Esses exercícios permitirão aos alunos aplicar o que aprenderam de forma criativa e dinâmica, enquanto desenvolvem suas habilidades de programação. Pratique cada projeto e desafie-se a expandi-los com novas funcionalidades!