# Tools

## Claude API (Anthropic)

* **Tipo:** API
* **Função:** Motor principal de raciocínio e geração dos agentes Neural Trax
* **Permissões:**
  * Enviar prompts com system, user e assistant turns
  * Usar ferramentas via function calling / MCP
  * Acessar modelos claude-opus, claude-sonnet e claude-haiku conforme custo/performance

## Open Claw (Plataforma Self-Hosted)

* **Tipo:** Plataforma interna
* **Função:** Ambiente de orquestração e execução dos agentes Neural Trax
* **Permissões:**
  * Criar, editar e acionar skills via SKILL.md
  * Gerenciar contexto de agentes e sessões
  * Executar fluxos multi-agente e visualizar logs

## GitHub

* **Tipo:** Integração
* **Função:** Versionamento de código, skills, configs de agentes e pipelines
* **Permissões:**
  * Ler e escrever repositórios de agentes
  * Criar branches, PRs e releases
  * Acionar workflows de CI/CD via Actions

## Docker / Docker Compose

* **Tipo:** Script / Infraestrutura
* **Função:** Containerização e orquestração local/cloud dos serviços da plataforma
* **Permissões:**
  * Build e push de imagens
  * Gerenciar volumes, redes e variáveis de ambiente
  * Restart automático de containers com política always

## Slack MCP

* **Tipo:** Integração / MCP Server
* **Função:** Comunicação interna e notificações dos agentes para o time
* **Permissões:**
  * Enviar mensagens em canais definidos
  * Criar drafts e alertas automáticos
  * Ler mensagens para contexto de tarefas colaborativas

## Zapier MCP

* **Tipo:** Integração / MCP Server
* **Função:** Automações e conexões com ferramentas externas dos clientes
* **Permissões:**
  * Disparar zaps via webhooks
  * Ler e escrever em Google Sheets, CRMs e plataformas conectadas
  * Enviar dados entre sistemas externos e agentes Neural Trax

## Sentry / Logging Stack

* **Tipo:** API / Monitoramento
* **Função:** Observabilidade, rastreamento de erros e performance dos agentes
* **Permissões:**
  * Capturar exceções e logs de agentes
  * Criar alertas e dashboards de health
  * Enviar relatórios automáticos via webhook