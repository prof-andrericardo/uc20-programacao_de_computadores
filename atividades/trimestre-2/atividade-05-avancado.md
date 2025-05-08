# 🧪 Atividade 05 – Funções em Python (Nível Avançado)

📅 **Trimestre:** 2º  
📘 **Capítulo abordado:**  
- Capítulo 5 – Modularização, Escopo, Projeto Final com Funções

🎯 **Objetivo da Atividade:**
Desenvolver um sistema completo utilizando funções modulares, escopos bem definidos e boas práticas de organização de código. Consolidar todo o aprendizado com um projeto prático.

---

## 🔧 Projeto: Sistema de Gestão de Boletins

Crie um programa completo com menu interativo que permita ao usuário:

1. Cadastrar alunos e notas
2. Listar todos os alunos
3. Gerar boletim com média e situação
4. Buscar aluno por nome
5. Excluir aluno
6. Sair

---

## 🧩 Requisitos Técnicos

### Funções obrigatórias:

- `menu()` → Exibe as opções disponíveis
- `cadastrar_aluno(lista)` → Recebe nome e 2 notas, armazena como sublista
- `calcular_media(n1, n2)` → Retorna média simples
- `situacao(m)` → Retorna situação textual com base na média
- `listar_alunos(lista)` → Mostra todos os alunos com notas e situação
- `buscar_aluno(lista, nome)` → Retorna as informações de um aluno específico
- `excluir_aluno(lista, nome)` → Remove aluno da lista
- `salvar_em_arquivo(lista)` → Exporta dados para um `.txt` ou `.csv` (bônus)

---

## 🔄 Regras de Implementação

- Use listas de listas: `[ ['João', 8.0, 7.5], ... ]`
- Crie um `while` principal com `match/case`
- Aplique tratamento de exceções com `try/except` onde necessário
- Organize o código com comentários e funções pequenas e reutilizáveis
- Utilize `if __name__ == "__main__":` para estrutura principal

---

## 🧠 Desafio Bônus

Implemente filtros personalizados:
- Mostrar somente alunos aprovados
- Mostrar alunos com média abaixo de 5
- Mostrar alunos com nomes iniciados por determinada letra

---

## ✍️ Entrega

- Entregar arquivo `.py` completo com as funções implementadas
- Incluir comentários explicativos em todas as funções
- Bônus se exportar os dados para arquivo externo
- Prazo: até **[INSERIR DATA DE ENTREGA]**

---

🔗 *Complemento de estudo disponível no Google Classroom da UC20.*