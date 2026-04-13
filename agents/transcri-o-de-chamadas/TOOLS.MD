**# Tools**




\- Nome: Google Drive Connector

  Tipo: Integração

  Função: Acessar gravações de reuniões salvas no Google Drive

  Permissões:

  - Listar novos arquivos de áudio/vídeo

  - Download de gravações

  - Identificar cliente por nome de arquivo ou pasta

  - Marcar arquivos como processados




\- Nome: Transcription Engine

  Tipo: API

  Função: Transcrever áudio para texto com alta precisão

  Permissões:

  - Converter áudio em texto

  - Identificar falantes (se possível)

  - Suporte a português brasileiro

  - Gerar texto formatado com timestamps




\- Nome: Asana CRM

  Tipo: Integração

  Função: Salvar transcrição na pasta do cliente no projeto CRM

  Permissões:

  - Identificar cliente pelo nome

  - Criar/task anexar documento .md na pasta do cliente

  - Atualizar status do projeto com nova transcrição

  - Vincular transcrição ao lead/oportunidade




\- Nome: Insight Extractor

  Tipo: Script

  Função: Analisar transcrição e extrair insights de vendas e reunião

  Permissões:

  - Identificar sinais de compra (interesse, urgência, budget)

  - Capturar objeções levantadas

  - Extrair decisões tomadas

  - Listar próximos passos e responsáveis

  - Calcular sentimento geral (positivo/neutro/negativo)

  - Gerar score de probabilidade de fechamento




\- Nome: Email Sender

  Tipo: Integração

  Função: Enviar instruções ao Head de Vendas e Head de Processo

  Permissões:

  - Enviar email com resumo da transcrição

  - Incluir instruções de relatório

  - Incluir sugestões de processo

  - CC para stakeholders relevantes




\- Nome: MD File Generator

  Tipo: Script

  Função: Gerar arquivo .md estruturado com transcrição e insights

  Permissões:

  - Criar arquivo markdown formatado

  - Incluir transcrição completa

  - Incluir seção de insights

  - Incluir metadata (data, duração, participantes, cliente)

  - Salvar com nome padrão: "Transcrição\_\[Cliente]\_\[Data].md"