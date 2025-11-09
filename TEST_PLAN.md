# 🔍 Plano de Teste: Confiabilidade e Segurança de Dispositivos
**Autor:** Letícia Gabriella  
**Objetivo:** Garantir que os aplicativos mantenham comportamento seguro mesmo sob condições adversas (root, VPN, proxy, emulação e falhas de SDK).  

---

## 🧠 Escopo
- Testes manuais exploratórios em **web e mobile** (Android/iOS)
- Foco em **comportamento de dispositivo, detecção de fraude e segurança**
- Execução em dispositivos reais e simuladores  

---

## 🧩 Ambientes de Teste
| Ambiente | Descrição |
|-----------|------------|
| Android 12 | Pixel 4a (rooted via Magisk) |
| iOS 15 | iPhone 11 (simulado) |
| Web | Chrome, Firefox |
| Ferramentas | Charles Proxy, ADB, Xcode, Testmo |

---

## ⚙️ Tipos de Teste
1. **Testes de Dispositivo**
   - Detecção de Root/Jailbreak  
   - Comparativo entre emulador e dispositivo real  
2. **Testes de Rede**
   - VPN ativa/desativada  
   - Interceptação de tráfego com proxy  
3. **Testes de SDK**
   - Falha de inicialização simulada  
   - Logs e fallback  
4. **Testes de Sessão**
   - Logins concorrentes  
   - Expiração de token  
5. **Testes Exploratórios**
   - Captura de tráfego, crash e latência  

---

## 🔒 Casos Críticos
| ID | Cenário | Resultado Esperado |
|----|----------|--------------------|
| CEN-001 | App detecta root e bloqueia operação sensível | Acesso negado + alerta de segurança |
| CEN-002 | App identifica uso de VPN ativa | Log de risco e reforço de autenticação |
| CEN-003 | Tráfego interceptado com Charles | Nenhum dado sensível em plaintext |
| CEN-004 | Falha no SDK de segurança | App executa fallback e loga erro |
| CEN-005 | Sessão duplicada em outro dispositivo | Token anterior invalidado |

---

## 📊 Métricas de Qualidade
- Taxa de falhas detectadas  
- Tempo médio de investigação  
- Cobertura de casos críticos (%)  
- Número de falsos positivos  

---

## 🧩 Critérios de Aceite
- Nenhum dado sensível exposto em logs  
- Falhas de segurança documentadas e priorizadas  
- Alertas automáticos funcionando via n8n  
- SDK e logs operacionais sob condições adversas  

---

## 🪄 Resultado Esperado
> Demonstrar como uma mentalidade de QA centrada em **segurança e prevenção de fraude** agrega valor ao negócio e protege a experiência do usuário.
