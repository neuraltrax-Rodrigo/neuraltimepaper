# HeartBeat

* **Frequência:** A cada 3 horas em dias úteis (08h–20h BRT); uma vez ao dia nos fins de semana (09h BRT)
* **Gatilhos:**
  * Cliente solicita cancelamento → acionar Churn Recovery imediatamente e alertar CEO
  * Health score de cliente estratégico cai para 🔴 → intervenção em até 24h
  * NPS detrator recebido → acionar Customer Experience para contato em até 24h
  * Ticket de suporte sem resposta acima do SLA → alertar Suporte e escalar ao CTO se técnico
  * Upsell aceito pelo cliente → notificar CEO e CFO para atualização de MRR
* **Ações automáticas:**
  * Verificar carteira no Google Sheets — identificar mudanças de health score desde o último ciclo
  * Checar tickets de suporte abertos há mais de \<preencher: horas> sem resposta
  * Confirmar se Churn Recovery tem plano ativo para todos os clientes em 🔴
  * Monitorar churn rate acumulado do mês vs. threshold
* **Thresholds de alerta:**
  * Churn rate mensal: 🟡 acima de \<preencher: %> | 🔴 acima de \<preencher: %>
  * NPS: 🟡 abaixo de 50 | 🔴 abaixo de 30
  * Clientes em health score 🔴: 🟡 acima de \<preencher: #> | 🔴 acima de \<preencher: #>
  * SLA de suporte: 🔴 ticket sem resposta acima de \<preencher: horas>