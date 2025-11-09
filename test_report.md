# 🧩 Relatório de Execução de Testes - Sardine QA Security Demo

**Autora:** Letícia Gabriella  
**Data da Execução:** 09/11/2025  
**Versão do App:** v1.2.3  
**Ambiente:** Android 12 (Pixel 4a Rooted) / iOS 15 (Simulador) / Web Chrome  

---

## 🎯 Objetivo
Apresentar os resultados da execução de testes focados em **segurança de dispositivo**, **comportamento de rede (VPN/Proxy)** e **resiliência do SDK de segurança**, simulando um ambiente semelhante ao monitorado pela **Sardine**.

---

## 🧪 Casos de Teste Executados

| ID | Título | Prioridade | Resultado | Observações |
|----|---------|-------------|------------|--------------|
| TC-001 | Detecção de Root | Alta | ❌ Falhou | App não bloqueou ações sensíveis em dispositivo rootado |
| TC-002 | VPN Ativa | Alta | ✅ Passou | Log de risco gerado corretamente |
| TC-003 | Interceptação de Dados | Alta | ✅ Passou | Nenhum dado sensível visível em interceptação Charles Proxy |
| TC-004 | Falha de SDK | Média | ⚠️ Parcial | Fallback executado, mas log incompleto |
| TC-005 | Sessão Duplicada | Média | ✅ Passou | Token antigo invalidado |
| TC-006 | Proxy Ativo | Baixa | ✅ Passou | App registrou alerta e manteve estabilidade |

---

## 📊 Resumo de Resultados

| Métrica | Valor |
|----------|--------|
| Total de Casos | 6 |
| Passaram | 4 |
| Falharam | 1 |
| Parciais | 1 |
| Taxa de Sucesso | **83%** |
| Bugs Criados | 2 |
| Logs Coletados | 5 |

---

## 🐞 Bugs Registrados
| ID | Título | Severidade | Status |
|----|----------|-------------|---------|
| BUG-20251109-001 | App não bloqueia operação em dispositivo rootado | Crítica | Aberto |
| BUG-20251109-002 | Log incompleto no fallback de SDK | Média | Aberto |

---

## 📈 Análise Geral
- O sistema apresentou **bom comportamento em cenários de rede** (VPN, proxy, interceptação).  
- A **detecção de root** precisa de reforço — alto risco de fraude se não for tratada.  
- O SDK de segurança funciona, mas **carece de logging completo** em falhas simuladas.  
- Nenhum dado sensível foi interceptado, o que indica **boa proteção criptográfica**.  

---

## 💡 Recomendações
1. Revisar integração da biblioteca de detecção de root/jailbreak.  
2. Adicionar logs estruturados e eventos de auditoria para falhas de SDK.  
3. Aumentar cobertura de testes de dispositivo com diferentes versões de Android/iOS.  
4. Automatizar execução e alerta via **n8n** para casos críticos de segurança.  

---

## 🧠 Conclusão
Os testes demonstraram que o aplicativo apresenta **nível de segurança consistente**, com **boas práticas de rede e SDK**, mas ainda precisa fortalecer a **detecção de dispositivos comprometidos**.

Este relatório exemplifica **como a validação de segurança pode ser tratada com método, empatia pelo usuário e foco na prevenção de riscos**, alinhando-se à missão da **Sardine** de construir confiança digital com IA e dados comportamentais.

---

*Documento criado para fins demonstrativos por Letícia Gabriella como parte do portfólio de QA focado em segurança e prevenção de fraudes.*
