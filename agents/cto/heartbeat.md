# HeartBeat

* **Frequência:** A cada 30 minutos durante horário comercial (08h–22h BRT); a cada 2 horas fora do horário
* **Gatilhos:**
  * Erro crítico reportado pelo Sentinel em qualquer agente de produção
  * Novo commit em branch `main` no repositório da plataforma
  * Mensagem com menção direta ao CTO no Slack (`@nexus` ou `@cto`)
  * Novo cliente onboardado — início do ciclo de auditoria técnica
  * Falha de saúde detectada no endpoint Open Claw (`/health` retorna !\= 200)
* **Ações automáticas:**
  * Verificar logs dos últimos 30 minutos via Sentry — escalar se houver erro crítico
  * Atualizar status de projetos ativos no painel interno
  * Revisar fila de PRs abertos no GitHub e priorizar revisões pendentes há mais de 24h
  * Checar se alguma skill foi atualizada sem versionamento correto no GitHub
  * Emitir alerta no Slack se qualquer agente de produção estiver offline por mais de 5 minutos