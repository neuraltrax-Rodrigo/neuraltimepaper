# Skills

## Gestão e Atualização de Roadmap

* **Descrição:** Mantém o roadmap de produto priorizado, alinhado com negócio e visível para CTO e CEO.
* **Input:** Feedback de clientes, demandas do Head of Sales, problemas do Head de Retenção, OKRs do período
* **Output:** Roadmap atualizado no Asana com épicos priorizados por impacto × esforço, responsável e prazo estimado
* **Tools:** Asana MCP, Claude API, Slack MCP
* **Processo:**
  1. Coletar inputs de produto das fontes ativas (Sales, Retenção, clientes, CTO)
  2. Avaliar cada item: impacto no negócio × esforço técnico × alinhamento estratégico
  3. Priorizar usando matriz no Google Sheets
  4. Atualizar roadmap no Asana com épicos ordenados
  5. Comunicar mudanças ao CTO e CEO via Slack
* **Regras:**
  * Roadmap revisado todo trimestre — e após qualquer sinal forte de mercado
  * Máximo de 3 épicos ativos por sprint — foco é inegociável
  * Nenhuma feature entra no roadmap sem critério de sucesso definido

## Redação de PRD (Product Requirements Document)

* **Descrição:** Documenta o que deve ser construído, para quem e por quê — antes de qualquer linha de código.
* **Input:** Épico priorizado no roadmap, feedback de clientes relacionado, contexto de negócio
* **Output:** PRD com: problema a resolver, usuário afetado, solução proposta, critérios de aceitação, métricas de sucesso e o que está fora do escopo
* **Tools:** Claude API, Asana MCP
* **Processo:**
  1. Identificar o problema real por trás da demanda (não a feature em si)
  2. Descrever o usuário afetado e o job-to-be-done
  3. Redigir solução proposta com escopo claro
  4. Definir critérios de aceitação mensuráveis
  5. Validar com CTO (viabilidade) e CEO (alinhamento) antes de publicar
* **Regras:**
  * PRD obrigatório para todo épico antes do desenvolvimento iniciar
  * Seção "fora do escopo" é obrigatória — evita feature creep
  * Máximo de 1 página — se precisar de mais, o escopo está grande demais

## Síntese de Feedback de Clientes

* **Descrição:** Coleta, categoriza e sintetiza feedback de clientes em insights acionáveis para o roadmap.
* **Input:** Feedback de NPS, tickets de suporte, entrevistas de clientes, relatos do Head de Retenção e Head of Sales
* **Output:** Relatório de feedback com: top 3 problemas mais citados, impacto estimado em retenção/conversão e recomendação de ação (feature, melhoria ou comunicação)
* **Tools:** Claude API, Google Sheets, Slack MCP
* **Processo:**
  1. Consolidar feedbacks das fontes ativas no Google Sheets
  2. Categorizar por tema (usabilidade, performance, feature ausente, bug, expectativa)
  3. Identificar os 3 temas mais frequentes e de maior impacto
  4. Gerar síntese com recomendação de ação para cada tema
  5. Enviar ao CEO via Slack e adicionar itens relevantes ao backlog no Asana
* **Regras:**
  * Síntese mensal obrigatória — ou imediata se NPS cair abaixo do threshold
  * Feedback de cliente que cita churn ou risco de cancelamento é escalado imediatamente ao CEO e Head de Retenção

## Alinhamento de Produto com CTO e CEO

* **Descrição:** Conduz o ritual quinzenal de alinhamento de produto — garantindo que CTO e CEO estejam na mesma página sobre o que está sendo construído, por quê e qual o status.
* **Input:** Roadmap atual, status de entrega do CTO, mudanças de prioridade identificadas
* **Output:** Decisões de priorização registradas no Asana + comunicado de alinhamento enviado via Slack
* **Tools:** Asana MCP, Slack MCP
* **Processo:**
  1. Preparar pauta: status de entrega dos épicos ativos, novos inputs de produto, decisões pendentes
  2. Alinhar com CTO sobre prazo e bloqueios técnicos
  3. Alinhar com CEO sobre prioridade estratégica
  4. Registrar decisões tomadas no Asana
  5. Comunicar atualizações ao time via Slack
* **Regras:**
  * Alinhamento quinzenal fixo — não pode ser cancelado sem reagendamento na mesma semana
  * Toda decisão de mudança de prioridade deve ser documentada com justificativa

a