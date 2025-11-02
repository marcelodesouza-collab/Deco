# 🏙️ Sistema de Denúncias Urbanas

> Plataforma inteligente para gestão de denúncias e problemas urbanos com inteligência artificial

## 📋 Visão Geral

O Sistema de Denúncias Urbanas é uma plataforma completa para gerenciamento de problemas urbanos reportados por cidadãos. Utilizando inteligência artificial e automação, o sistema facilita a comunicação entre cidadãos e gestores públicos, garantindo que problemas como buracos, iluminação defeituosa, lixo acumulado e outros sejam reportados, classificados e resolvidos de forma eficiente.

## ✨ Funcionalidades Principais

### 🤖 Agentes Inteligentes

O sistema conta com três agentes especializados baseados em IA:

1\. **Citizen Support Agent** (Assistente do Cidadão)

- Interface amigável para criação de denúncias
- Coleta informações essenciais: tipo, localização, descrição e fotos
- Guia o cidadão passo a passo no processo de denúncia
- Fornece número de protocolo para acompanhamento
- Responde perguntas sobre o status de denúncias

2\. **Classification Agent** (Agente de Classificação)

- Classificação automática do tipo de denúncia
- Análise de imagens anexadas usando visão computacional
- Determinação automática do nível de urgência
- Categorização inteligente baseada em descrição e evidências
- Processamento rápido para priorização eficiente

3\. **City Manager Agent** (Assistente do Gestor)

- Dashboard com análises e estatísticas
- Relatórios detalhados de denúncias por região
- Indicadores de desempenho (SLA, tempo médio de resolução)
- Insights para tomada de decisão
- Priorização de recursos baseada em dados

### 📱 Canais de Atendimento

O sistema oferece múltiplos canais para reportar problemas:

- **Web**: Interface responsiva e intuitiva
- **WhatsApp**: Integração para denúncias via mensagem
- **Telegram**: Bot automatizado para reportes
- **API**: Integração com outros sistemas municipais

### 🗂️ Tipos de Denúncias Suportados

- 🕳️ **Buracos e Pavimentação**: Problemas na via pública
- 💡 **Iluminação Pública**: Lâmpadas queimadas, postes danificados
- 🗑️ **Lixo e Limpeza**: Acúmulo irregular, descarte inadequado
- 🌳 **Áreas Verdes**: Manutenção de praças e parques
- 🚰 **Saneamento**: Vazamentos, esgoto a céu aberto
- 🚦 **Sinalização**: Placas danificadas, semáforos com defeito
- 🏗️ **Obras Irregulares**: Construções sem autorização
- 🐕 **Animais**: Maus tratos, animais abandonados
- 📢 **Outros**: Demais problemas urbanos

### 🎯 Níveis de Urgência

- **🔴 CRÍTICA**: Risco imediato à vida ou segurança pública
- **🟡 ALTA**: Problema significativo que requer atenção prioritária
- **🟢 MÉDIA**: Situação que deve ser resolvida em prazo normal
- **⚪ BAIXA**: Problema menor sem impacto imediato

## 🔄 Fluxo de Trabalho

### Para o Cidadão:

1. **Reportar**: Acessa o sistema e descreve o problema
2. **Anexar**: Adiciona fotos e localização
3. **Enviar**: Recebe número de protocolo
4. **Acompanhar**: Monitora o status da denúncia
5. **Avaliar**: Confirma a resolução e avalia o atendimento

### Para o Gestor:

1. **Receber**: Denúncia chega classificada automaticamente
2. **Analisar**: Visualiza detalhes, imagens e urgência
3. **Encaminhar**: Designa equipe responsável
4. **Monitorar**: Acompanha progresso em tempo real
5. **Concluir**: Registra resolução e fecha chamado

## 🛠️ Componentes Técnicos

### Tools (Ferramentas)

- **Criação de Denúncias**: Registro estruturado de novos casos
- **Consulta de Denúncias**: Busca e listagem com filtros
- **Atualização de Status**: Gerenciamento do ciclo de vida
- **Análise de Imagens**: Processamento com IA para classificação
- **Geolocalização**: Mapeamento preciso dos problemas
- **Notificações**: Alertas automáticos por email/SMS

### Workflows (Automações)

- **Triagem Automática**: Classificação e priorização inteligente
- **Roteamento**: Encaminhamento para departamento correto
- **SLA Monitoring**: Alertas para denúncias próximas do prazo
- **Relatórios Agendados**: Geração automática de dashboards
- **Integração Externa**: Sincronização com sistemas legados

### Views (Interfaces)

- **Dashboard Cidadão**: Visualização de denúncias pessoais
- **Dashboard Gestor**: Painel executivo com métricas
- **Mapa de Calor**: Visualização geográfica de problemas
- **Timeline**: Histórico completo de cada denúncia
- **Relatórios**: Exportação de dados e análises

## 📊 Banco de Dados

### Estrutura Principal:

```typescript
Denúncia {
  id: string
  protocolo: string
  tipo: TipoDenuncia
  urgencia: NivelUrgencia
  status: StatusDenuncia
  descricao: string
  localizacao: {
    endereco: string
    bairro: string
    coordenadas: { lat, lng }
  }
  cidadao: {
    nome: string
    contato: string
  }
  imagens: string[]
  criado_em: timestamp
  atualizado_em: timestamp
  resolvido_em?: timestamp
  responsavel?: string
  departamento?: string
  observacoes: string[]
}
```

## 🔐 Segurança e Privacidade

- ✅ Autenticação segura para gestores
- ✅ Dados do cidadão protegidos (LGPD compliant)
- ✅ Logs de auditoria de todas as ações
- ✅ Acesso baseado em roles e permissões
- ✅ Criptografia de dados sensíveis
- ✅ Backup automático diário

## 📈 Métricas e KPIs

### Para Gestão:

- **Volume**: Total de denúncias por período
- **Tempo Médio de Resolução**: Por tipo e urgência
- **Taxa de Resolução**: % de denúncias concluídas
- **Satisfação**: Avaliação dos cidadãos
- **Áreas Críticas**: Regiões com mais problemas
- **Performance da Equipe**: Produtividade por departamento

### Relatórios Disponíveis:

- Consolidado mensal/anual
- Por tipo de denúncia
- Por região/bairro
- Por status e urgência
- Análise temporal (tendências)
- Comparativos entre períodos

## 🚀 Benefícios

### Para os Cidadãos:

- ✨ Canal direto com a prefeitura
- 📱 Acesso fácil e multiplataforma
- 🔍 Transparência no acompanhamento
- ⚡ Respostas mais rápidas
- 🎯 Garantia de que o problema será tratado

### Para a Gestão Pública:

- 📊 Dados estruturados para decisões
- 🤖 Redução de trabalho manual
- 🎯 Priorização inteligente
- 💰 Otimização de recursos
- 📈 Melhoria contínua dos serviços
- 🏆 Maior satisfação da população

## 🔧 Integrações

- **Google Drive**: Armazenamento de imagens e documentos
- **WhatsApp/Telegram**: Recebimento de denúncias
- **Email/SMS**: Notificações automáticas
- **Google Maps**: Geolocalização e mapas
- **OpenAI**: Classificação inteligente com IA
- **Sistemas Legados**: APIs para integração municipal

## 📱 Tecnologias

- **Frontend**: React 19 + Tailwind CSS v4
- **Backend**: Cloudflare Workers + TypeScript
- **Database**: DECONFIG (Cloudflare Durable Objects)
- **IA**: OpenAI GPT-4 + Vision API
- **Infraestrutura**: Edge Computing (global)
- **Plataforma**: deco.cx

## 🎓 Como Usar

### Para Cidadãos:

1. Acesse o sistema via web ou app
2. Clique em "Nova Denúncia"
3. Preencha as informações solicitadas
4. Tire fotos do problema
5. Envie e guarde seu protocolo
6. Acompanhe o status online

### Para Gestores:

1. Faça login no painel administrativo
2. Visualize denúncias pendentes
3. Filtre por urgência, tipo ou região
4. Analise detalhes e imagens
5. Encaminhe para equipe responsável
6. Atualize status conforme resolução
7. Consulte relatórios e métricas

## 📞 Suporte

Para dúvidas ou suporte técnico:

- 📧 Email: suporte@denunciasurbanas.com.br
- 📱 WhatsApp: (11) 9999-9999
- 🌐 Portal: https://ajuda.denunciasurbanas.com.br

## 📄 Licença

Este sistema foi desenvolvido durante o Hackathon OS e está disponível sob licença open-source para uso por municípios e governos.

---

**Desenvolvido com ❤️ para melhorar nossas cidades**

*Última atualização: 2024*
