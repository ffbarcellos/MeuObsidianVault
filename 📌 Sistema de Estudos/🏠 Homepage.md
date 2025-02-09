## 🏆 **Bem-vindo ao Sistema Mente Blindada**

Este painel fornece uma **visão geral** do seu estudo, destacando as **próximas revisões**, erros a corrigir e desempenho nos simulados.

---

### 📅 **Próximas Revisões**

```dataview
TABLE file.name AS "Tema", proxima_revisao
FROM "Mapa de Conhecimento" OR "Banco de Erros"
WHERE proxima_revisao <= date(today)
SORT proxima_revisao ASC
```

---

### ❌ **Erros a Revisar**

```dataview
TABLE file.name AS "Erro", dificuldade, proxima_revisao
FROM "Banco de Erros"
WHERE status = "Precisa Revisão"
SORT dificuldade DESC, proxima_revisao ASC
```

---

### 🎯 **Últimos Simulados**

```dataview
TABLE file.name AS "Simulado", data, desempenho, principais_erros
FROM "Simulados"
SORT data DESC
```

---

### 🔗 **Links Rápidos**

🔹 [[Banco de Erros]]  
🔹 [[Mapa de Conhecimento]]  
🔹 [[Diário de Estudos]]  
🔹 [[Plano de Estudo Personalizado]]  
🔹 [[Manual de Execução de Simulados]]

---

# 🚀 **Como Usar a Homepage?**

✅ **Verifique as próximas revisões diariamente** e priorize conteúdos críticos.  
✅ **Corrija erros do Banco de Erros** e ajuste revisões conforme necessário.  
✅ **Acompanhe seus simulados** e analise padrões de desempenho.

🔥 **Com essa dashboard, você terá controle total sobre seu estudo!**