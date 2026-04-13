# HeartBeat

* **Frequência:** A cada 1 hora em dias úteis (06h–23h BRT); a cada 3 horas nos fins de semana
* **Gatilhos:**
  * KPI crítico (🔴) detectado em qualquer frente → alerta imediato ao CEO + Head da área, não aguarda próximo ciclo
  * Fonte de dados indisponível ou com erro de coleta → alerta ao Head de Dados e ao CTO
  * Novo dado recebido via webhook (ex: fechamento de contrato, pagamento confirmado, churn registrado) → atualizar dashboard e reavaliar KPIs afetados
  * Solicitação de análise ad hoc recebida via Slack do CEO ou de qualquer Head → executar e entregar em até 30 minutos
* **Ações automáticas:**
  * Rodar varredura completa de KPIs críticos e comparar com thresholds — classificar cada um: 🟢/🟡/🔴
  * Atualizar timestamp de "última atualização" no dashboard central
  * Verificar se algum alerta 🔴 emitido nas últimas 6h ainda está sem status de resolução — reenviar lembrete ao Head responsável
  * Consolidar novos dados recebidos desde o último ciclo nas abas do Google Sheets
* **Thresholds de referência (preencher com valores reais):**
  * MRR: 🟡 queda > \<preencher: %> | 🔴 queda > \<preencher: %>
  * Churn rate: 🟡 acima de \<preencher: %> | 🔴 acima de \<preencher: %>
  * Taxa de conversão de leads: 🟡 abaixo de \<preencher: %> | 🔴 abaixo de \<preencher: %>
  * Uptime de agentes: 🟡 abaixo de 99% | 🔴 abaixo de 95%
  * CAC: 🟡 acima de \<preencher: R$> | 🔴 acima de \<preencher: R$>
  * NPS: 🟡 abaixo de 50 | 🔴 abaixo de 30