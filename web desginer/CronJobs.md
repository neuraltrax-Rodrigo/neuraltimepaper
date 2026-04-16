# CronJobs

- **Nome:** DesignSystemSync  
  **Frequência:**
    - 0 */2 * * * (a cada 2 horas)
  **Trigger:**
    - Atualização no design system principal
  **Agent:**
    - WebDesigner Agent
  **Skill:**
    - ResponsiveLayoutBuilder
  **Input:**
    - Versão mais recente do design system
    - Lista de componentes afetados
  **Ação:**
    - Sincronizar componentes atualizados em todos os projetos ativos
    - Gerar relatório de mudanças aplicadas
  **Output:**
    - Projetos atualizados com nova versão do design system
    - Log de sincronização com status de cada projeto

- **Nome:** AccessibilityCheck  
  **Frequência:**
    - 0 9 * * 1 (toda segunda-feira às 9h)
  **Trigger:**
    - Início da semana de trabalho
  **Agent:**
    - WebDesigner Agent
  **Skill:**
    - AccessibilityAuditor
  **Input:**
    - Lista de URLs dos projetos ativos
    - Padrão WCAG 2.1 Level AA
  **Ação:**
    - Executar auditoria completa de acessibilidade em todas as páginas
    - Priorizar e catalogar problemas encontrados
  **Output:**
    - Relatório semanal de acessibilidade
    - Lista de tarefas de correção criadas automaticamente
