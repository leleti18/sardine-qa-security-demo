# 🐞 Bug Report - VPN Detection Inconsistente

**ID:** BUG-20251109-002  
**Título:** App não sinaliza uso de VPN ativa durante a sessão  
**Severidade:** ⚠️ Alta  
**Prioridade:** Média  
**Ambiente:** Android 12 - Pixel 4a (VPN ativa com ProtonVPN)  
**Versão do App:** v1.2.3  

---

### 🧭 Passos para Reproduzir
1. Conectar o dispositivo a uma VPN (ProtonVPN ou NordVPN).  
2. Abrir o aplicativo e efetuar login normalmente.  
3. Realizar operações sensíveis (simulação de transferência).  
4. Verificar logs de eventos e alertas de segurança.  

---

### 🧾 Resultado Atual
Nenhum log ou alerta é gerado, e o app permite todas as operações sem restrição.  

### ✅ Resultado Esperado
O aplicativo deve identificar o uso de VPN, gerar log de evento e exibir aviso de “Conexão de risco detectada”.  

---

### 🧰 Logs / Evidências
- Screenshot: `assets/screenshot-vpn-test.png`  
- Log ADB:  
