**# CronJobs**




\- Nome: Verificar Novos Briefings de Campanha

  Frequência:

    - A cada 4 horas (0 \*/4 \* \* \*)

  Trigger:

    - Briefing enviado pelo Head de Marketing

  Agent:

    - Diretor de Arte

  Skill:

    - Conceito Visual de Campanha

  Input:

    - Briefing com objetivo, público, mensagem, canal

  Ação:

    - Analisar briefing e copy associada

    - Definir conceito visual (mood, paleta, referências)

    - Gerar mood board

    - Enviar para aprovação

  Output:

    - Conceito visual documentado + mood board




\- Nome: Validação de Peças Visuais Produzidas

  Frequência:

    - Diariamente às 11:00 (0 11 \* \* \*)

  Trigger:

    - Peças visuais finalizadas por designers

  Agent:

    - Diretor de Arte

  Skill:

    - Validação de Peças Visuais

  Input:

    - Peças visuais produzidas (ads, posts, LPs)

  Ação:

    - Validar cada peça contra conceito e guidelines

    - Analisar composição, hierarquia, contraste

    - Verificar acessibilidade WCAG

    - Gerar report de validação

  Output:

    - Peças aprovadas, aprovadas com ajustes, ou reprovadas




\- Nome: Curadoria de Referências para Campanhas Ativas

  Frequência:

    - Diariamente às 09:00 (0 9 \* \* \*)

  Trigger:

    - Campanhas ativas precisando de referências visuais

  Agent:

    - Diretor de Arte

  Skill:

    - Curadoria Visual

  Input:

    - Conceito visual de campanhas ativas

  Ação:

    - Buscar e curar imagens de bancos

    - Organizar mood boards por campanha

    - Incluir notas de curadoria

  Output:

    - Mood boards atualizados com 5-10 imagens por campanha




\- Nome: Direção Visual de Vídeos

  Frequência:

    - Sob demanda, verificar às 10:00 (0 10 \* \* \*)

  Trigger:

    - Scripts de vídeos aprovados pelo Copywriter

  Agent:

    - Diretor de Arte

  Skill:

    - Direção Visual para Vídeos

  Input:

    - Scripts de vídeos pendentes de direção visual

  Ação:

    - Analisar script e definir estilo visual

    - Especificar enquadramento, paleta, motion

    - Gerar briefing visual para editor

  Output:

    - Briefing visual completo do vídeo




\- Nome: Coordenação Copy + Visual

  Frequência:

    - Diariamente às 14:00 (0 14 \* \* \*)

  Trigger:

    - Copies novas ou atualizadas pelo Copywriter

  Agent:

    - Diretor de Arte

  Skill:

    - Coordenação Copy + Visual

  Input:

    - Copy atualizada + conceito visual associado

  Ação:

    - Revisar integração copy + visual

    - Ajustar direção visual se necessário

    - Validar mensagem clara em 3 segundos

  Output:

    - Direção criativa unificada atualizada




\- Nome: Análise de Performance Visual

  Frequência:

    - Diariamente às 16:00 (0 16 \* \* \*)

  Trigger:

    - Dados de KPIs disponíveis

  Agent:

    - Diretor de Arte

  Skill:

    - Evolução Visual Baseada em Dados

  Input:

    - CTR, engajamento por tipo de visual

  Ação:

    - Analisar patterns de alta performance

    - Identificar oportunidades de evolução

    - Propor ajustes baseados em dados

  Output:

    - Report diário: performance visual + recomendações




\- Nome: Pesquisa de Tendências Visuais

  Frequência:

    - Toda segunda às 09:00 (0 9 \* \* 1)

  Trigger:

    - Novo semana

  Agent:

    - Diretor de Arte

  Skill:

    - Curadoria Visual

    - Evolução Visual Baseada em Dados

  Input:

    - Setor e contexto de mercado

  Ação:

    - Pesquisar tendências visuais da semana

    - Filtrar por relevância à Neural Trax

    - Registrar tendências aplicáveis

  Output:

    - Trend board semanal atualizado




\- Nome: Report Semanal de Direção de Arte

  Frequência:

    - Toda sexta às 16:00 (0 16 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Diretor de Arte

  Skill:

    - Todos

  Input:

    - Todas as atividades da semana

  Ação:

    - Compilar métricas:

      - Conceitos visuais criados: X

      - Peças validadas: X (aprovadas, ajustes, reprovadas)

      - Mood boards gerados: X

      - Direções de vídeo: X

      - Evoluções propostas: X

      - Performance visual vs semana anterior

    - Gerar report semanal

  Output:

    - Report enviado ao Head de Marketing




\- Nome: Composição de Peças Novas

  Frequência:

    - Diariamente às 13:00 (0 13 \* \* \*)

  Trigger:

    - Novas peças necessitando direção de composição

  Agent:

    - Diretor de Arte

  Skill:

    - Composição Visual de Peças

  Input:

    - Tipo de peça, copy, conceito visual

  Ação:

    - Definir hierarquia visual

    - Especificar layout e posicionamento

    - Validar composição

    - Gerar guia para designer

  Output:

    - Direção de composição documentada