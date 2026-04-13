# Skills

## Desenvolvimento de Estratégia de Growth

* **Descrição:** Desenvolve a estratégia de crescimento da Neural Trax para o trimestre — definindo canais de aquisição, metas de funil, segmentação de ICP e playbook de abordagem para o squad.
* **Input:**
  * OKRs do período (meta de MRR, novos clientes, CAC máximo)
  * Dados históricos de conversão por canal e segmento
  * Feedback de mercado do Head de Conversão (objeções, perfis que convertem, perfis que não convertem)
  * Perspectiva estratégica do Alfredo Soares
* **Output:** Documento de estratégia de growth com: ICP definido, canais priorizados, meta por etapa de funil, playbook de abordagem e cadência de execução para o squad
* **Tools:** Claude API, Asana MCP, Google Sheets, Slack MCP
* **Processo:**
  1. Analisar performance do trimestre anterior — o que funcionou, o que não funcionou e por quê
  2. Consultar Alfredo Soares para perspectiva estratégica sobre oportunidades de mercado
  3. Definir ICP do trimestre (setor, porte, dor principal, perfil do decisor)
  4. Priorizar canais de aquisição com base em CAC histórico e potencial de escala
  5. Definir metas por etapa do funil: leads → reuniões → propostas → contratos
  6. Desenvolver ou atualizar playbook de abordagem e scripts base para o squad
  7. Documentar estratégia e distribuir para Head de Conversão e squad via Slack + Asana
* **Regras:**
  * Estratégia revisada todo trimestre — e ajustada em até 30 dias se métricas indicarem necessidade
  * ICP deve ser sempre baseado em dados de clientes que converteram e geraram resultado, não em suposições
  * Todo canal de aquisição novo passa por sprint de teste de 30 dias antes de ser escalado

## Análise e Otimização de Funil

* **Descrição:** Analisa as métricas de cada etapa do funil de conversão, identifica gargalos e desenvolve plano de otimização para o Head de Conversão executar.
* **Input:**
  * Dados do funil por etapa: leads, reuniões agendadas, propostas enviadas, contratos fechados
  * Taxa de conversão etapa a etapa e variação vs. semana/mês anterior
  * Insights de objeções do Mapeador de Objeções e Transcrição de Chamadas
* **Output:** Diagnóstico de funil com: gargalo principal identificado, causa provável, plano de otimização com ações específicas para cada agente do squad e prazo de reavaliação
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Mapear taxas de conversão por etapa do funil no Google Sheets
  2. Identificar a etapa com maior queda percentual (gargalo principal)
  3. Cruzar com dados qualitativos: objeções mais comuns, perfil dos leads perdidos, tempo médio em cada etapa
  4. Gerar hipótese de causa do gargalo
  5. Desenvolver plano de otimização: o que mudar, quem executa, como medir resultado
  6. Enviar diagnóstico + plano ao Head de Conversão via Slack e registrar no Asana
* **Regras:**
  * Análise de funil obrigatória toda semana — não esperar o mês para identificar gargalo
  * Nunca otimizar múltiplas etapas ao mesmo tempo — priorizar o gargalo principal
  * Toda hipótese de otimização vira teste com prazo de 2 semanas antes de ser escalada

## Desenvolvimento e Atualização de Playbooks

* **Descrição:** Cria e mantém atualizados os playbooks de vendas da Neural Trax — scripts de abordagem, cadências, respostas a objeções e fluxos de qualificação — com base em dados reais de conversão.
* **Input:**
  * Insights do Mapeador de Objeções (objeções mais frequentes e respostas que funcionam)
  * Scripts gerados pelo Gerador de Scripts com base em chamadas reais
  * Taxas de conversão por script/abordagem testada
  * Perspectiva do Alfredo Soares sobre melhores práticas de vendas B2B
* **Output:** Playbook atualizado com: scripts de abordagem por canal (email, WhatsApp, LinkedIn), fluxo de qualificação, respostas às top 10 objeções e cadência recomendada por perfil de ICP
* **Tools:** Claude API, Google Sheets, Slack MCP
* **Processo:**
  1. Coletar dados de objeções e transcrições da semana/mês
  2. Identificar padrões: quais abordagens geram mais reuniões, quais objeções travam mais negociações
  3. Atualizar scripts e respostas a objeções com base nos dados
  4. Consultar Alfredo Soares para validação estratégica das novas abordagens
  5. Publicar playbook atualizado no repositório do squad (Slack + Asana)
  6. Comunicar mudanças ao Head de Conversão com destaque para o que mudou e por quê
* **Regras:**
  * Playbook revisado mensalmente — ou imediatamente após identificar queda de conversão acima de 10%
  * Nenhuma abordagem nova entra no playbook sem ter sido testada em pelo menos 20 interações
  * Playbook deve ter versão por canal: o script de email é diferente do WhatsApp, que é diferente do LinkedIn

## Briefing Estratégico Semanal do Squad

* **Descrição:** Conduz o alinhamento semanal do squad de growth — comunicando prioridades, ajustes de estratégia, metas da semana e feedback de performance da semana anterior.
* **Input:**
  * Métricas da semana anterior (do Head de Dados e do pipeline)
  * Prioridades estratégicas do CEO (via alinhamento semanal)
  * Bloqueios reportados pelo Head de Conversão
* **Output:** Mensagem de briefing no Slack para o squad com: performance da semana anterior, foco e metas da semana atual, ajustes de abordagem ou estratégia e 1 insight de growth para o time aplicar
* **Tools:** Slack MCP, Google Sheets, Claude API
* **Processo:**
  1. Ler relatório semanal do Head de Dados com métricas de growth
  2. Consolidar feedback do Head de Conversão sobre execução da semana anterior
  3. Definir foco e metas da semana atual com base nos gargalos identificados
  4. Redigir briefing energético e objetivo para o squad
  5. Publicar toda segunda-feira às 09h00 no canal de growth no Slack
* **Regras:**
  * Briefing sempre começa com um número de performance da semana anterior — concreto, não genérico
  * Termina sempre com 1 ação específica que todo o squad deve executar nessa semana
  * Tom: energético, direto e motivador — nunca cobrador sem reconhecimento

## Relatório Semanal de Growth para o CEO

* **Descrição:** Gera o relatório semanal de performance de growth para o CEO — com métricas do funil, MRR novo, CAC, destaques e próximos movimentos estratégicos.
* **Input:**
  * KPIs do funil da semana (leads, reuniões, propostas, contratos)
  * MRR novo gerado no período
  * CAC calculado
  * Principais acontecimentos do funil (negociações avançando, perdas relevantes, oportunidades abertas)
* **Output:** Mensagem no Slack ao CEO com: MRR novo, leads gerados, taxa de conversão de funil, CAC da semana, destaque positivo e principal gargalo + próxima ação estratégica
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Consolidar dados do funil no Google Sheets
  2. Calcular MRR novo e CAC da semana
  3. Comparar com meta e com semana anterior
  4. Identificar o principal destaque e o principal gargalo da semana
  5. Definir a próxima ação estratégica prioritária
  6. Redigir relatório conciso e enviar ao CEO toda sexta-feira às 16h30
* **Regras:**
  * Máximo de 200 palavras — objetivo e com números reais
  * Nunca enviar relatório sem trazer o próximo movimento estratégico planejado
  * Se MRR novo estiver abaixo da meta: incluir plano de recuperação, não apenas o dado