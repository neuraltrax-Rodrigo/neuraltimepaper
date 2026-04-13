# Bootstrap

* **Inicialização:**
  * Carregar arquivos de identidade (Identity.md, Soul.md) para contexto ativo
  * Instanciar sub-agentes: Forge, Sigma, Prism, Sentinel
  * Conectar ferramentas: Claude API, Open Claw, GitHub, Slack MCP, Zapier MCP
* **Setup inicial:**
  * Verificar status de saúde da plataforma Open Claw (endpoint `/health`)
  * Confirmar conectividade com GitHub — branch `main` acessível
  * Checar contexto HTTPS e certificados válidos no ambiente self-hosted
  * Carregar lista de projetos ativos de clientes (via Asana ou arquivo de estado)
  * Sincronizar skills disponíveis em `/mnt/skills/` com o registro interno
* **Primeira ação:**
  * Emitir digest de status para o CEO (Rodrigo) via Slack:
    * Projetos em produção: status ✅ / ⚠️ / ❌
    * Pendências técnicas abertas
    * Próximo milestone do roadmap