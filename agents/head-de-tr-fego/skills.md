# Skills

## Gestão de Performance de Campanhas

* **Descrição:** Monitora e otimiza campanhas pagas em tempo real, garantindo CPL dentro do alvo e volume de leads consistente.
* **Input:** Dados do Media Buyer (CPL, leads, ROAS, budget) + feedback de qualidade de lead do Head de Conversão
* **Output:** Decisões de otimização comunicadas ao Media Buyer: pausar criativo, ajustar segmentação, realocar budget ou testar novo ângulo
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Ler relatório do Media Buyer com performance do período
  2. Cruzar com feedback de qualidade do Head de Conversão (lead que chega, mas não converte \= problema de segmentação)
  3. Identificar campanha ou criativo abaixo do threshold de CPL
  4. Definir ação: pausar, otimizar ou testar nova variação
  5. Comunicar decisão ao Media Buyer com briefing claro
* **Regras:**
  * CPL acima do threshold por mais de 3 dias → intervenção obrigatória
  * Nenhum criativo fica ativo sem ter sido testado por pelo menos 500 impressões

## Diagnóstico de Mix de Canais

* **Descrição:** Avalia a performance de cada canal de tráfego (pago, orgânico, email, conteúdo) e otimiza a alocação de esforço e budget entre eles.
* **Input:** Relatório consolidado do Analista de Relatórios com CPL, volume e qualidade de lead por canal
* **Output:** Recomendação de mix de canais para a próxima semana/mês com justificativa baseada em dados
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Comparar CPL e qualidade de lead por canal
  2. Identificar canal com melhor relação custo-qualidade
  3. Identificar canal com performance deteriorando
  4. Recomendar realocação de budget ou esforço
  5. Comunicar decisão ao squad e registrar no Google Sheets
* **Regras:**
  * Diagnóstico mensal obrigatório — ou imediato após queda abrupta de performance em qualquer canal
  * Nenhum canal é abandonado sem 30 dias de teste em condições justas

## Briefing de Criativos e Conteúdo

* **Descrição:** Gera briefings de campanha para o Media Buyer e de conteúdo para Pedro Sobral com base nos dados de performance e no ICP da Neural Trax.
* **Input:** Dados de criativos que performaram, ICP atual, ângulos não testados identificados
* **Output:** Briefing de criativo com: objetivo, audiência, ângulo de comunicação, formato recomendado e métrica de sucesso
* **Tools:** Claude API, Slack MCP
* **Processo:**
  1. Analisar criativos ativos e identificar ângulos esgotados ou abaixo da média
  2. Mapear ângulos não testados baseados em dores do ICP
  3. Redigir briefing específico por canal (pago ou orgânico)
  4. Enviar ao Media Buyer e/ou Pedro Sobral com prazo de execução
* **Regras:**
  * Mínimo de 2 novos criativos testados por semana no pago
  * Briefing sempre inclui: problema do ICP que o criativo resolve + call to action esperado

## Relatório Semanal de Tráfego para o Head de Growth

* **Descrição:** Consolida a performance de todos os canais da semana e entrega visão clara ao Head de Growth.
* **Input:** Relatórios do squad da semana — leads por canal, CPL, ROAS, orgânico, email
* **Output:** Mensagem no Slack ao Head de Growth com: total de leads gerados, CPL médio, canal destaque, canal problemático e próxima ação
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Consolidar dados de todos os canais no Google Sheets
  2. Calcular: total de leads, CPL médio, lead-to-meeting rate (com dado do Head de Conversão)
  3. Identificar canal com melhor e pior performance da semana
  4. Definir prioridade tática para a semana seguinte
  5. Enviar toda sexta-feira às 15h30 ao Head de Growth
* **Regras:**
  * Sempre inclui o feedback de qualidade de lead recebido do Head de Conversão
  * Se CPL acima do alvo: enviar junto com plano de ajuste