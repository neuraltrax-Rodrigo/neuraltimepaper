# Skills

## Precificação de Projetos de IA

* **Descrição:** Calcula o custo real de entrega de um projeto de agentes e define o preço ao cliente com margem saudável.
* **Input:**
  * Escopo do projeto (número de agentes, integrações, horas estimadas)
  * Custo de API (tokens estimados por mês)
  * Custo de infra (VPS, domínio, serviços)
* **Output:** Planilha de precificação com custo, margem e preço sugerido ao cliente
* **Tools:** Google Sheets, Claude API
* **Processo:**
  1. Mapear todos os custos diretos do projeto (API, infra, horas)
  2. Aplicar margem mínima definida pela Neural Trax
  3. Simular cenários de uso (baixo, médio, alto volume)
  4. Gerar proposta de preço com justificativa de valor
  5. Registrar na planilha de precificação histórica
* **Regras:**
  * Margem bruta mínima: \<preencher: % definido pelo CEO>
  * Todo projeto recorrente deve ter cálculo de custo mensal de manutenção incluso

## Relatório Financeiro Executivo

* **Descrição:** Gera resumo financeiro periódico em linguagem de negócio para o CEO.
* **Input:**
  * Dados do fluxo de caixa do período
  * MRR atual e histórico
  * Despesas categorizadas
* **Output:** Relatório narrativo com destaques, alertas e recomendações — enviado via Slack
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Coletar dados financeiros do período no Google Sheets
  2. Calcular indicadores: MRR, margem, burn rate, inadimplência
  3. Identificar variações relevantes vs. período anterior
  4. Redigir narrativa executiva com Claude API
  5. Enviar para o CEO via Slack com formatação clara
* **Regras:**
  * Relatório semanal toda segunda-feira às 08h00
  * Alertas críticos (caixa negativo projetado, inadimplência acima de X%) enviados imediatamente

## Controle de Recebíveis

* **Descrição:** Monitora pagamentos de clientes, emite cobranças e alerta sobre inadimplência.
* **Input:**
  * Lista de contratos ativos com datas de vencimento
  * Status de pagamentos registrados
* **Output:** Alerta de inadimplência + e-mail de cobrança automático para o cliente
* **Tools:** Google Sheets, Gmail MCP, Slack MCP
* **Processo:**
  1. Verificar vencimentos dos próximos 7 dias no Google Sheets
  2. Confirmar se pagamento foi registrado
  3. Se não pago: enviar lembrete amigável via Gmail no dia do vencimento
  4. Se 3 dias em atraso: enviar cobrança formal e alertar CEO no Slack
  5. Registrar status atualizado na planilha
* **Regras:**
  * Nunca enviar cobrança sem verificar se o pagamento não foi registrado com atraso no sistema
  * Tom da cobrança: cordial no 1º contato, formal a partir do 2º

## Projeção de Fluxo de Caixa

* **Descrição:** Projeta entradas e saídas dos próximos 30/60/90 dias com base em contratos ativos e despesas fixas.
* **Input:**
  * Contratos ativos com valores e datas de recebimento
  * Despesas fixas e variáveis do período
  * Pipeline de novos clientes (probabilidade de fechamento)
* **Output:** Planilha de projeção com 3 cenários + alerta se caixa projetado ficar abaixo do mínimo
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Consolidar receitas garantidas (contratos assinados)
  2. Adicionar receitas prováveis do pipeline com peso por probabilidade
  3. Subtrair despesas fixas e variáveis previstas
  4. Calcular saldo projetado para 30, 60 e 90 dias
  5. Emitir alerta se qualquer cenário projetar saldo abaixo do mínimo operacional
* **Regras:**
  * Mínimo operacional de caixa: \<preencher: valor definido pelo CEO>
  * Projeção atualizada toda sexta-feira e após qualquer novo contrato assinado