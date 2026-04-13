**# Skills**




\- Nome: Transcrição de Áudio

  Descrição: Transcrever gravações de reuniões do Google Drive para texto

  Input:

    - Arquivo de áudio/vídeo do Google Drive

  Output:

    - Texto completo da transcrição com timestamps e identificação de falantes

  Tools:

    - Google Drive Connector

    - Transcription Engine

  Processo:

    1. Monitorar Google Drive por novas gravações

    2. Identificar cliente associado à gravação

    3. Baixar arquivo de áudio

    4. Transcrever para texto com timestamps

    5. Identificar falantes (se possível)

    6. Marcar arquivo como processado no Drive

  Regras:

    - Transcrição fiel, sem alterar conteúdo

    - Português brasileiro

    - Incluir timestamps a cada mudança de falante

    - Se áudio ruim: flaggar trechos ininteligíveis




\- Nome: Extração de Insights de Vendas

  Descrição: Analisar transcrição e extrair sinais de compra, objeções e próximos passos

  Input:

    - Transcrição completa da reunião

  Output:

    - Lista de insights: sinais de compra, objeções, decisões, próximos passos, score de fechamento

  Tools:

    - Insight Extractor

  Processo:

    1. Analisar transcrição completa

    2. Identificar sinais de compra (interesse explícito, urgência, perguntas sobre preço/prazo)

    3. Capturar objeções levantadas pelo cliente

    4. Extrair decisões tomadas na reunião

    5. Listar próximos passos com responsáveis e prazos

    6. Calcular sentimento geral (positivo/neutro/negativo)

    7. Gerar score de probabilidade de fechamento (0-100%)

  Regras:

    - Sinais de compra: citar trechos exatos da transcrição

    - Objeções: categorizar (preço, prazo, confiança, necessidade)

    - Próximos passos: sempre com responsável e prazo

    - Score baseado em BANT implícito na conversa




\- Nome: Geração de Arquivo MD

  Descrição: Criar arquivo .md estruturado com transcrição + insights

  Input:

    - Transcrição completa

    - Insights extraídos

    - Metadata da reunião (data, duração, participantes, cliente)

  Output:

    - Arquivo .md salvo no Asana

  Tools:

    - MD File Generator

    - Asana CRM

  Processo:

    1. Montar estrutura do arquivo .md:

       - Header: metadata (cliente, data, duração, participantes)

       - Seção 1: Transcrição completa

       - Seção 2: Insights de Vendas (sinais de compra, objeções, decisões)

       - Seção 3: Próximos Passos (responsável, prazo)

       - Seção 4: Score de Fechamento e Sentimento

       - Seção 5: Instruções para Head de Vendas

       - Seção 6: Sugestões para Head de Processo

    2. Gerar arquivo com nome: "Transcrição\_\[Cliente]\_\[Data].md"

    3. Salvar no Asana na pasta do cliente (projeto CRM)

  Regras:

    - Formato markdown consistente

    - Cliente identificável no Asana antes de salvar

    - Se não encontrar cliente: criar task pendente e alertar




\- Nome: Instruções ao Head de Vendas

  Descrição: Gerar email com instruções para Head de Vendas montar relatório

  Input:

    - Insights da reunião

    - Transcrição resumida

  Output:

    - Email enviado ao Head de Vendas

  Tools:

    - Email Sender

  Processo:

    1. Compilar resumo executivo (3-5 linhas)

    2. Listar sinais de compra detectados

    3. Listar objeções que precisam ser tratadas

    4. Incluir score de fechamento

    5. Instruções para relatório:

       - "Montar relatório de follow-up para \[Cliente]"

       - "Tratar objeção de \[tipo] antes da próxima reunião"

       - "Agendar próxima reunião até \[data]"

    6. Enviar email ao Head de Vendas

  Regras:

    - Email conciso e direto

    - Incluir link para transcrição no Asana

    - Priorizar ações por urgência




\- Nome: Sugestões ao Head de Processo

  Descrição: Gerar email com sugestões de melhoria de processo baseadas em padrões

  Input:

    - Transcrição e insights

    - Histórico de transcrições anteriores

  Output:

    - Email enviado ao Head de Processo

  Tools:

    - Email Sender

    - Insight Extractor

  Processo:

    1. Identificar padrões recorrentes (objeções frequentes, gargalos, erros de processo)

    2. Gerar sugestões de melhoria:

       - "Objeção de preço aparece em 60% das reuniões → revisar proposta comercial"

       - "Clientes confundem etapa X → simplificar explicação no roteiro"

       - "Fechamento trava em Y → criar material de apoio"

    3. Incluir dados de suporte (quantas reuniões, qual padrão)

    4. Enviar email ao Head de Processo

  Regras:

    - Sugestões baseadas em dados, não opiniões

    - Incluir frequência do padrão observado

    - Priorizar por impacto no fechamento




\- Nome: Identificação de Cliente no Asana

  Descrição: Identificar cliente associado à gravação e localizar pasta no Asana CRM

  Input:

    - Nome do arquivo ou metadata da gravação

  Output:

    - Cliente localizado no Asana ou pendência de identificação

  Tools:

    - Asana CRM

    - Google Drive Connector

  Processo:

    1. Extrair nome do cliente do nome do arquivo ou pasta

    2. Buscar cliente no Asana CRM

    3. Se encontrado: retornar ID e pasta

    4. Se não encontrado: criar task pendente com detalhes

    5. Alertar usuário para identificação manual

  Regras:

    - Busca fuzzy para variações de nome

    - Se múltiplos matches: pedir confirmação

    - Não salvar transcrição sem cliente identificado