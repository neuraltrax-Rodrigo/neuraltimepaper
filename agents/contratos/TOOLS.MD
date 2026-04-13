**# Tools**




\- Nome: Asana Integration

  Tipo: Integração

  Função: Ler dados de projetos fechados (cliente, produtos, automações, valores, implementação)

  Permissões:

  - Leitura de projetos com status "Fechado"

  - Extração de dados de escopo e valores

  - Atualização de status do projeto




\- Nome: Modelo de Contrato

  Tipo: Script

  Função: Template base do contrato comercial da Neural Trax com cláusulas variáveis

  Permissões:

  - Leitura do modelo vigente

  - Preenchimento de variáveis (partes, escopo, valores, prazos)

  - Versionamento de modelos




\- Nome: Catálogo de Produtos e Automações

  Tipo: Integração

  Função: Acessar descrição técnica de produtos e automações vendidas

  Permissões:

  - Leitura de especificações de produtos

  - Leitura de escopo de automações

  - Leitura de planos de implementação




\- Nome: Gerador de PDF

  Tipo: Script

  Função: Converter contrato preenchido em PDF profissional

  Permissões:

  - Geração de PDF a partir de dados estruturados

  - Formatação profissional

  - Inclusão de logo e dados da empresa




\- Nome: Email Sender

  Tipo: Integração

  Função: Enviar contratos ao usuário para aprovação e ao cliente após aprovação

  Permissões:

  - Envio de email com anexo PDF

  - Envio para usuário e cliente

  - Rastreamento de entregas e aberturas




\- Nome: Aprovador de Contrato

  Tipo: Script

  Função: Submeter contrato ao usuário e aguardar aprovação antes de envio

  Permissões:

  - Notificar usuário com contrato para revisão

  - Receber aprovação ou solicitar alterações

  - Bloquear envio sem aprovação explícita