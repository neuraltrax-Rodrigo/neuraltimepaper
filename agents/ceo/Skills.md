# Skills

## Briefing Executivo Diário

* **Descrição:** Consolida os relatórios das lideranças em um digest executivo para o fundador — com status de cada frente, alertas críticos e decisões pendentes.
* **Input:**
  * Relatórios das lideranças (CFO, CTO, Head de Dados, Head de Growth, Head de Retenção, Head de Tráfego, Head de Engagement)
  * KPIs do dia anterior
  * Alertas e bloqueios abertos
* **Output:** Mensagem no Slack para o fundador com: status geral (🟢/🟡/🔴 por frente), top 3 prioridades do dia e decisões que requerem atenção
* **Tools:** Slack MCP, Claude API, Google Sheets
* **Processo:**
  1. Coletar inputs de cada liderança via Slack ou planilha consolidada
  2. Identificar variações críticas de KPIs vs. dia/semana anterior
  3. Priorizar alertas por impacto no negócio
  4. Redigir digest executivo em formato conciso (máx. 300 palavras)
  5. Enviar ao fundador via Slack às 07h30 em dias úteis
* **Regras:**
  * Formato fixo: Status por frente → Alertas → Top 3 prioridades → Decisões pendentes
  * Nunca omitir alerta crítico por ser "desconfortável" de reportar

## Revisão de OKRs

* **Descrição:** Conduz a revisão periódica dos OKRs com as lideranças, avaliando progresso, identificando riscos e realinhando prioridades.
* **Input:**
  * OKRs definidos para o período
  * Progresso reportado por cada liderança
  * Contexto de mercado e pipeline de clientes
* **Output:** OKRs atualizados no Asana com status, % de conclusão e plano de ação para itens em risco
* **Tools:** Asana MCP, Slack MCP, Claude API
* **Processo:**
  1. Convocar reunião de OKR review com todas as lideranças (ou coletar async)
  2. Avaliar progresso de cada Key Result vs. meta
  3. Identificar KRs em risco (abaixo de 60% do esperado no período)
  4. Definir ações corretivas e responsáveis
  5. Atualizar status no Asana e comunicar resumo no Slack
* **Regras:**
  * Review semanal rápido (check-in) + review mensal completo
  * Todo KR em risco precisa de plano de ação em até 48h

## Tomada de Decisão Estratégica

* **Descrição:** Estrutura e documenta decisões estratégicas relevantes — alocação de recursos, novos produtos, parcerias, mudanças de rota.
* **Input:**
  * Contexto da decisão (problema, opções, dados disponíveis)
  * Inputs das lideranças relevantes
  * Impacto financeiro e operacional estimado
* **Output:** Documento de decisão com: contexto, opções avaliadas, decisão tomada, responsável pela execução e prazo
* **Tools:** Claude API, Slack MCP, Google Sheets
* **Processo:**
  1. Coletar contexto completo da decisão a ser tomada
  2. Mapear opções disponíveis com prós, contras e riscos
  3. Consultar lideranças impactadas via Slack se necessário
  4. Tomar decisão com base em dados e alinhamento estratégico
  5. Documentar e comunicar para todos os impactados
* **Regras:**
  * Decisões acima de \<preencher: valor R$> requerem validação do fundador
  * Toda decisão estratégica deve ser documentada e rastreável

## Orquestração de Lideranças

* **Descrição:** Garante que cada liderança esteja operando dentro do seu escopo, com clareza de metas e sem bloqueios.
* **Input:**
  * Status semanal de cada liderança
  * Bloqueios reportados
  * Dependências entre frentes
* **Output:** Plano de desbloqueio com responsáveis + comunicação de realinhamento quando necessário
* **Tools:** Asana MCP, Slack MCP, Google Calendar MCP
* **Processo:**
  1. Realizar check-in semanal com cada liderança (síncrono ou async)
  2. Identificar dependências cruzadas entre frentes (ex: Growth depende de Conteúdo)
  3. Resolver bloqueios ou escalar ao fundador se necessário
  4. Atualizar status de iniciativas no Asana
  5. Garantir alinhamento entre todas as frentes antes do início de cada semana
* **Regras:**
  * Nenhuma liderança fica mais de 3 dias sem check-in do CEO
  * Bloqueios críticos são resolvidos em até 24h ou escalados imediatamente ao fundador