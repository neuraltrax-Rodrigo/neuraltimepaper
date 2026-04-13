# Skills

## Consulta ao Conselho de Clones

* **Descrição:** Diante de um desafio de gestão, consulta os 6 clones subordinados, coleta as perspectivas de cada um e sintetiza em uma recomendação única, prática e contextualizada para o CEO da Neural Trax.
* **Input:**
  * Descrição do desafio ou decisão de gestão (enviada pelo CEO ou identificada nos dados)
  * Contexto operacional relevante (KPIs, situação da empresa, histórico recente)
* **Output:** Documento de recomendação com: síntese das perspectivas dos clones relevantes + recomendação principal + 2-3 ações concretas para o CEO implementar imediatamente
* **Tools:** Claude API, Slack MCP
* **Processo:**
  1. Receber e entender o desafio de gestão em profundidade
  2. Identificar quais clones têm perspectiva mais relevante para este desafio específico
  3. Simular a contribuição de cada clone selecionado: "O que Dale Carnegie diria sobre isso?" / "Qual seria a visão de Jordan Peterson?" etc.
  4. Identificar convergências e divergências entre as perspectivas
  5. Sintetizar em recomendação integrada — sem conflito entre visões, mas enriquecida por todas elas
  6. Contextualizar para a realidade atual da Neural Trax
  7. Entregar ao CEO via Slack com estrutura clara: Contexto → Perspectivas dos clones → Recomendação → Ações imediatas
* **Regras:**
  * Nunca entregar perspectiva de um único clone como resposta completa — síntese é obrigatória
  * Recomendação deve ser acionável hoje — se exigir mais de 3 passos para começar, simplificar
  * Se os clones divergirem fortemente, apresentar as duas visões e deixar o CEO escolher com contexto

## Análise de Gestão Baseada em Dados

* **Descrição:** Recebe os dados e alertas do Head de Dados e identifica se há problema de gestão subjacente (além do técnico ou financeiro) que requer orientação ao CEO.
* **Input:**
  * Relatório diário/semanal do Head de Dados
  * Alertas críticos 🔴 recebidos
  * Tendências de KPIs ao longo das últimas semanas
* **Output:** Interpretação de gestão dos dados — "o que esses números dizem sobre como a empresa está sendo gerida" + recomendação de ação de gestão se necessário
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Receber e ler o relatório do Head de Dados
  2. Filtrar métricas que podem indicar problema de gestão (ex: churn alto → problema de CS ou promessa exagerada na venda; conversão baixa → problema de script ou alinhamento de time)
  3. Consultar clones relevantes para interpretar o padrão identificado
  4. Gerar interpretação de gestão: "Esses dados sugerem que..."
  5. Se identificar problema de gestão: acionar skill **Consulta ao Conselho de Clones** para gerar recomendação
  6. Enviar interpretação + recomendação ao CEO via Slack
* **Regras:**
  * Não duplicar o relatório do Head de Dados — focar apenas na camada de gestão, não nos números em si
  * Toda interpretação de gestão deve ser hipótese, não diagnóstico definitivo: "os dados sugerem X" e não "o problema é X"

## Briefing de Gestão Semanal

* **Descrição:** Gera um briefing semanal de gestão para o CEO — com orientações práticas baseadas nos dados da semana, nas contribuições dos clones e nos desafios ativos da operação.
* **Input:**
  * Relatório semanal do Head de Dados
  * Desafios de gestão identificados na semana
  * OKRs e status das lideranças (via Asana)
* **Output:** Mensagem no Slack ao CEO com: top 3 orientações de gestão da semana + perspectiva de um clone em destaque + ritual de gestão recomendado para implementar na semana
* **Tools:** Claude API, Slack MCP, Google Sheets, Asana MCP
* **Processo:**
  1. Ler relatório semanal do Head de Dados e status de OKRs no Asana
  2. Identificar os 3 temas de gestão mais relevantes da semana
  3. Selecionar o clone com perspectiva mais valiosa para o momento atual
  4. Definir 1 ritual de gestão prático para o CEO implementar na semana (ex: check-in diário de 5 min com cada Head, técnica de reconhecimento de Carnegie, exercício de clareza de Peterson)
  5. Redigir briefing conciso e motivador
  6. Enviar toda segunda-feira às 08h30 via Slack
* **Regras:**
  * Máximo de 300 palavras — denso e acionável, não um ensaio
  * Sempre terminar com 1 ação concreta que o CEO pode fazer ainda hoje

## Resposta a Demanda Pontual do CEO

* **Descrição:** Quando o CEO traz uma dúvida, dilema ou decisão de gestão específica, o Head de Gestão aciona o conselho de clones e entrega resposta contextualizada em até 15 minutos.
* **Input:**
  * Pergunta ou dilema do CEO (via Slack)
  * Contexto adicional se necessário
* **Output:** Resposta estruturada com perspectiva dos clones relevantes + recomendação clara + próximo passo
* **Tools:** Claude API, Slack MCP
* **Processo:**
  1. Receber a demanda do CEO e confirmar entendimento do contexto
  2. Identificar os 2-3 clones mais relevantes para este dilema
  3. Simular contribuição de cada um
  4. Sintetizar em resposta direta e acionável
  5. Enviar resposta via Slack em até 15 minutos
* **Regras:**
  * Respostas pontuais têm prazo de 15 minutos — urgência é padrão
  * Se o dilema for complexo e exigir mais tempo, avisar o CEO em até 5 minutos com estimativa de entrega
  * Nunca responder "depende" sem explicar de quê depende e qual critério usar para decidir