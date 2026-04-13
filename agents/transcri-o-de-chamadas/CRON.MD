**# CronJobs**




\- Nome: Monitorar Google Drive por Gravações

  Frequência:

    - A cada 1 hora (0 \* \* \* \*)

  Trigger:

    - Novos arquivos de áudio/vídeo no Drive

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Transcrição de Áudio

  Input:

    - Pasta do Google Drive com gravações

  Ação:

    - Listar novos arquivos não processados

    - Identificar cliente associado

    - Iniciar transcrição

  Output:

    - Lista de gravações pendentes de transcrição




\- Nome: Transcrever Gravações Pendentes

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Gravações detectadas e prontas para transcrição

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Transcrição de Áudio

  Input:

    - Arquivos de áudio do Google Drive

  Ação:

    - Transcrever cada gravação

    - Identificar falantes e timestamps

    - Marcar como transcrita

  Output:

    - Transcrições completas prontas para análise




\- Nome: Gerar Insights e Arquivo MD

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Transcrições concluídas

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Extração de Insights de Vendas

    - Geração de Arquivo MD

  Input:

    - Transcrição completa

    - Metadata da reunião

  Ação:

    - Extrair sinais de compra, objeções, decisões, próximos passos

    - Calcular score de fechamento e sentimento

    - Gerar arquivo .md estruturado

    - Salvar no Asana na pasta do cliente

  Output:

    - Arquivo .md salvo no Asana




\- Nome: Enviar Instruções ao Head de Vendas

  Frequência:

    - Diariamente às 11:00 (0 11 \* \* \*)

  Trigger:

    - Transcrições processadas nas últimas 24h

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Instruções ao Head de Vendas

  Input:

    - Insights das reuniões transcritos

  Ação:

    - Compilar resumos executivos

    - Listar sinais de compra e objeções

    - Incluir scores de fechamento

    - Enviar instruções de relatório

  Output:

    - Email enviado ao Head de Vendas




\- Nome: Enviar Sugestões ao Head de Processo

  Frequência:

    - Toda sexta às 14:00 (0 14 \* \* 5)

  Trigger:

    - Histórico de transcrições da semana

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Sugestões ao Head de Processo

  Input:

    - Transcrições e insights da semana

  Ação:

    - Identificar padrões recorrentes

    - Gerar sugestões de melhoria de processo

    - Incluir dados de suporte

  Output:

    - Email com sugestões enviado ao Head de Processo




\- Nome: Relatório Semanal de Transcrições

  Frequência:

    - Toda sexta às 17:00 (0 17 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Extração de Insights de Vendas

  Input:

    - Todas as transcrições da semana

  Ação:

    - Compilar métricas:

      - Reuniões transcritas: X

      - Sinais de compra detectados: X

      - Objeções mais frequentes: lista

      - Score médio de fechamento: X%

      - Clientes não identificados: X

    - Gerar report semanal

  Output:

    - Report enviado ao Head de Vendas e Head de Processo




\- Nome: Limpeza de Pendências

  Frequência:

    - Toda segunda às 09:00 (0 9 \* \* 1)

  Trigger:

    - Transcrições com cliente não identificado

  Agent:

    - Agente de Transcrição de Chamadas

  Skill:

    - Identificação de Cliente no Asana

  Input:

    - Lista de transcrições pendentes de identificação

  Ação:

    - Rebuscar clientes no Asana com busca fuzzy

    - Se ainda não encontrar: alertar usuário

    - Resolver pendências possíveis

  Output:

    - Pendências resolvidas ou escaladas