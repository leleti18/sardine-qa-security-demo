# 🐞 Bug Report - Falha no SDK de Segurança

**ID:** BUG-20251109-003  
**Título:** SDK de segurança falha silenciosamente sem gerar logs  
**Severidade:** ⚠️ Média  
**Prioridade:** Alta  
**Ambiente:** Android 12 (emulador)  
**Versão do App:** v1.2.3  

---

### 🧭 Passos para Reproduzir
1. Mockar retorno de erro do SDK de segurança (ex: `sdk.init() → error code 503`).  
2. Iniciar o aplicativo.  
3. Acompanhar logs no console e comportamento da tela inicial.  

---

### 🧾 Resultado Atual
O SDK falha na inicialização, o app continua executando, mas **não registra o evento em log nem executa fallback**.  

### ✅ Resultado Esperado
App deveria registrar o erro, exibir mensagem genérica e iniciar fallback para modo restrito.  

---

### 🧰 Logs / Evidências
- Logcat:  
