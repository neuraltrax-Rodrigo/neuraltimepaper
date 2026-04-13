# Skills

## Arquitetura de Sistemas Multi-Agente

* **Descrição:** Projeta a hierarquia completa de agentes da Neural Trax, definindo papéis, contratos de comunicação e fluxos de orquestração entre os 6 níveis.
* **Input:**
  * Descrição do domínio ou setor do cliente
  * Requisitos funcionais e não-funcionais do sistema
* **Output:** Diagrama de hierarquia de agentes + contratos de input/output por nível
* **Tools:** Claude API, Open Claw, GitHub
* **Processo:**
  1. Mapear domínio e casos de uso do cliente
  2. Definir agentes por nível (Orchestrator → Mind Clones)
  3. Especificar skills necessárias por agente
  4. Validar fluxos de comunicação e dependências
  5. Documentar em arquivos .md no padrão Neural Trax
* **Regras:**
  * Todo agente deve ter Identity.md, Soul.md e pelo menos uma skill definida
  * Nenhum agente opera sem contrato de input/output documentado

## Geração e Homologação de SKILL.md

* **Descrição:** Cria novas skills no padrão SKILL.md da plataforma Open Claw, validando estrutura, triggers e comportamento esperado.
* **Input:**
  * Nome e propósito da skill
  * Ferramentas disponíveis
  * Exemplos de input/output desejados
* **Output:** Arquivo SKILL.md completo e pronto para uso na plataforma
* **Tools:** Open Claw, GitHub
* **Processo:**
  1. Coletar contexto da skill (nome, trigger, domínio)
  2. Redigir frontmatter YAML e seções obrigatórias
  3. Definir exemplos de uso e regras de comportamento
  4. Salvar em `/mnt/skills/` e validar na plataforma
  5. Versionar no GitHub com tag de release
* **Regras:**
  * Seguir exatamente a estrutura do template padrão
  * Todo SKILL.md deve ter pelo menos 2 exemplos de trigger e 1 exemplo negativo

## Auditoria Técnica de Projetos de Clientes

* **Descrição:** Revisa a arquitetura técnica de implementações para clientes B2B antes do go-live, identificando riscos, gargalos e gaps de segurança.
* **Input:**
  * Documentação do projeto (arquivos .md, diagramas, configs)
  * Stack tecnológico do cliente
* **Output:** Relatório de auditoria com riscos priorizados e recomendações
* **Tools:** GitHub, Sentry, Claude API
* **Processo:**
  1. Revisar arquitetura e contratos de agentes
  2. Verificar configurações de segurança e permissões
  3. Testar fluxos críticos em ambiente de staging
  4. Documentar findings com severidade (crítico / alto / médio / baixo)
  5. Apresentar relatório ao CEO e lead de entrega
* **Regras:**
  * Nenhum projeto vai a produção com findings críticos abertos
  * Auditoria é obrigatória para todo projeto acima de 3 agentes

## Roadmap Tecnológico

* **Descrição:** Define e prioriza o roadmap da plataforma Neural Trax, alinhando evolução técnica com objetivos de negócio e feedback de clientes.
* **Input:**
  * OKRs do período
  * Feedback de clientes e time de entrega
  * Novidades do mercado de IA (modelos, ferramentas, frameworks)
* **Output:** Roadmap priorizado em formato de épicos e sprints
* **Tools:** Asana, Slack, Claude API
* **Processo:**
  1. Consolidar inputs de negócio e técnicos
  2. Mapear capacidades atuais vs. desejadas
  3. Priorizar por impacto × esforço
  4. Distribuir em sprints e atribuir a sub-agentes/squads
  5. Revisar quinzenalmente e ajustar conforme contexto
* **Regras:**
  * Roadmap deve ter horizonte mínimo de 90 dias
  * Toda feature deve ter critério de aceitação técnico definido antes do desenvolvimento