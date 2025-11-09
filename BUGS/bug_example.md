# 🐞 Bug Report - Exemplo Prático

**ID:** BUG-20251109-001  
**Título:** App não bloqueia operação em dispositivo rootado  
**Severidade:** 🔴 Crítica  
**Prioridade:** Alta  
**Ambiente:** Android 12 - Pixel 4a (rooted via Magisk)  
**Versão do App:** v1.2.3  

---

### 🧭 Passos para Reproduzir
1. Instalar o app no Pixel 4a com root ativo (Magisk).  
2. Abrir o app e efetuar login.  
3. Realizar operação sensível (ex: simulação de transferência).  

---

### 🧾 Resultado Atual
O app permite a operação normalmente e **não exibe nenhum alerta de segurança**.

### ✅ Resultado Esperado
O app deveria bloquear a operação e **exibir aviso de segurança**, registrando o evento em log.  

---

### 🧰 Logs / Evidências
- Screenshot: `assets/screenshot-root-test.png`  
- Log ADB (trecho):  
