---
title: Dashboard de Monitoramento de Progresso
created: <% tp.date.now("YYYY-MM-DD") %>
tags: ["Dashboard", "Progresso", "Monitoramento"]
---
## **🎯 Objetivo**

Este painel fornece uma visão geral do seu desempenho por matéria, permitindo ajustes estratégicos no estudo.

---

### 📈 **Média de Acertos nos Últimos Simulados**

```dataview
TABLE file.name AS "Simulado", data, desempenho
FROM "Simulados"
WHERE desempenho != null
SORT data DESC
LIMIT 5
```

📌 **Dica:** Se a média de acertos de uma matéria estiver baixa, priorize revisões e exercícios extras.

---

### 🔄 **Erros Mais Recorrentes**

```dataview
TABLE file.name AS "Erro", assunto, dificuldade, ultima_revisao
FROM "Banco de Erros"
WHERE status = "Precisa Revisão" AND dificuldade != null
SORT dificuldade DESC, ultima_revisao ASC
LIMIT 5
```

📌 **Dica:** Se um erro aparece repetidamente, ele **precisa ser resolvido urgentemente**.

---

### 📅 **Revisões Pendentes por Matéria**

```dataview
TABLE file.name AS "Tema", proxima_revisao
FROM "Mapa de Conhecimento"
WHERE proxima_revisao != null AND proxima_revisao <= date(today)
SORT proxima_revisao ASC
```

📌 **Dica:** Priorize revisões antes da data programada para evitar acumular conteúdo.

---

### 🔗 **Links Rápidos**

🔹 [[Simulados]]  
🔹 [[Banco de Erros]]  
🔹 [[Mapa de Conhecimento]]  
🔹 [[Plano de Estudo Personalizado]]

---

# 🚀 **Como Usar esta Dashboard?**

✅ **Acompanhe o progresso semanalmente** e ajuste o estudo conforme necessário.  
✅ **Se uma matéria estiver com desempenho baixo, aumente o foco nela.**  
✅ **Monitore os erros mais comuns para garantir que eles não se repitam.**

🔥 **Com essa visão geral, seu estudo será ainda mais estratégico e eficiente!**