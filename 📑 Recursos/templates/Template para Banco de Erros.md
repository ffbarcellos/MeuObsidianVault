---
title: Template para Banco de Erros
created: <% tp.date.now("YYYY-MM-DD") %>
tags: ["Erros", "Revisão", "Aprendizado"]
tipo: Erro Recorrente
assunto:
dificuldade:
data_erro: <% tp.date.now("YYYY-MM-DD") %>
ultima_revisao: <% tp.date.now("YYYY-MM-DD") %>
proxima_revisao: <% moment().add(7, "days").format("YYYY-MM-DD") %>
segunda_revisão: <% moment().add(30, "days").format("YYYY-MM-DD") %>
status: Precisa
---





## **🎯 Objetivo**

Este template serve para registrar **erros recorrentes**, identificar padrões e garantir que **cada erro leve a um aprendizado real**, reduzindo a chance de repeti-los no futuro.

---

## **📂 Estrutura do Banco de Erros**

### **❌ Erro Cometido**

📌 **Título do erro:** _Descreva o erro de forma objetiva._  
📌 **Assunto:** _Matéria ou tema relacionado ao erro._  
📌 **Dificuldade:** Baixa / Média / Alta  
📌 **Data do erro:** <% tp.date.now("YYYY-MM-DD") %>  
📌 **Última Revisão:** <% tp.date.now("YYYY-MM-DD") %>

### **🔍 O que aconteceu?**

📌 Descreva exatamente **como e por que** esse erro aconteceu.  
📌 O que você pensou na hora que levou à resposta errada?  
📌 O erro foi conceitual, de interpretação ou desatenção?

### **🧠 Motivo do erro**

📌 Qual foi a raiz do problema?  
📌 Esse erro já aconteceu antes? Ele segue um padrão?  
📌 O que faltou para acertar?

### **✅ Como corrigir?**

📌 Como resolver corretamente esse tipo de questão?  
📌 Qual estratégia pode evitar esse erro no futuro?  
📌 Existe um conceito que precisa ser revisado?

---

## **📅 Revisão Programada**

✅ Próxima Revisão: <% moment().add(7, "days").format("YYYY-MM-DD") %>
✅ Segunda Revisão: <% moment().add(30, "days").format("YYYY-MM-DD") %>
✅ **Status:** Precisa Revisão / Resolvido

---

## **🔗 Notas Relacionadas**

🔹 [[Mapa de Conhecimento - Tema Relacionado]]  
🔹 [[Diário de Estudos - Reflexão sobre esse erro]]  
🔹 [[Simulado - Questão em que o erro ocorreu]]

---

# **🚀 Como Usar Este Modelo?**

✅ Criar uma entrada para **cada erro relevante**.  
✅ Revisar periodicamente para garantir que o erro foi corrigido.  
✅ Atualizar o status para "Resolvido" quando o erro não for mais um problema.

🚀 **Agora, seu Banco de Erros será uma ferramenta poderosa para aprendizado contínuo!**

---
<%*
const root = "📌 Sistema de Estudos/🛑 Banco de Erros"
let title = tp.file.title
await tp.file.move(root + "/" + title)
%>