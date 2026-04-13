# CronJobs

## Relatório Semanal de Saúde Técnica

* **Frequência:** Toda segunda-feira às 08h00 BRT (`0 8 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** CTO + Sentinel
* **Skill:** Auditoria Técnica de Projetos de Clientes
* **Input:** Logs da semana anterior, status de todos os projetos ativos
* **Ação:** Compilar relatório consolidado de saúde técnica (uptime, erros, pendências)
* **Output:** Relatório enviado ao CEO via Slack com resumo de status e alertas priorizados

## Revisão de Roadmap

* **Frequência:** A cada 15 dias, sexta-feira às 17h00 BRT (`0 17 */15 * 5`)
* **Trigger:** Agendamento automático
* **Agent:** CTO
* **Skill:** Roadmap Tecnológico
* **Input:** OKRs vigentes, feedback de projetos, novas capacidades de IA disponíveis
* **Ação:** Revisar e ajustar roadmap, repriorizar épicos se necessário
* **Output:** Roadmap atualizado no Asana + resumo de mudanças enviado ao CEO

## Auditoria de Segurança Mensal

* **Frequência:** Todo dia 1 do mês às 06h00 BRT (`0 6 1 * *`)
* **Trigger:** Agendamento automático
* **Agent:** Sentinel + CTO
* **Skill:** Auditoria Técnica de Projetos de Clientes (escopo segurança)
* **Input:** Logs de acesso, permissões de agentes, configurações de API keys
* **Ação:** Varrer todos os projetos em produção em busca de vulnerabilidades e não-conformidades LGPD
* **Output:** Relatório de segurança com findings e plano de remediação

## Sincronização de Skills

* **Frequência:** Diariamente às 03h00 BRT (`0 3 * * *`)
* **Trigger:** Agendamento automático
* **Agent:** Sigma (Arquiteto de IA)
* **Skill:** Geração e Homologação de SKILL.md
* **Input:** Diretório `/mnt/skills/` — arquivos novos ou modificados
* **Ação:** Detectar skills sem versionamento, validar estrutura YAML e registrar no índice interno
* **Output:** Log de sincronização + alerta no Slack se skill inválida for encontrada

## Digest Diário para o CEO

* **Frequência:** Todo dia útil às 07h30 BRT (`30 7 * * 1-5`)
* **Trigger:** Agendamento automático
* **Agent:** CTO
* **Skill:** \<preencher: skill de geração de digest executivo>
* **Input:** Status de agentes, pendências abertas, milestones do roadmap
* **Ação:** Gerar resumo técnico executivo do dia
* **Output:** Mensagem no Slack para o CEO com os 3 pontos técnicos mais relevantes do dia