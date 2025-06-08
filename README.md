# 📅 Plano Detalhado com Sub-steps (5 por tarefa)

---

## 1. Arquitetura Orientada a Serviços (Java + Oracle + Azure)

### Modelagem banco Oracle

1. Analisar requisitos de dados do projeto.
2. Definir tabelas principais (perfil, recomendação, histórico, gamificação).
3. Criar índices para otimização de consultas.
4. Configurar usuários, roles e permissões de acesso.
5. Estabelecer rotina de backup e recovery.

### Configuração Oracle no Azure

1. Provisionar VM no Azure para Oracle.
2. Instalar e configurar Oracle Database na VM.
3. Configurar rede segura com VPN Gateway ou ExpressRoute.
4. Testar conectividade segura entre backend e banco.
5. Configurar alta disponibilidade (failover).

### Desenvolver microserviço Autenticação

1. Definir endpoints para login e logout.
2. Implementar geração de tokens JWT.
3. Validar tokens em requests autenticados.
4. Controlar expiração e renovação de tokens.
5. Testar fluxo de autenticação completo.

### Desenvolver microserviço Perfil Cliente

1. Modelar entidade perfil e suitability.
2. Criar endpoints CRUD para perfil.
3. Validar regras de negócio para dados de perfil.
4. Implementar integração com banco Oracle.
5. Realizar testes unitários e integração.

### Desenvolver microserviço Macroeconômico

1. Identificar fontes confiáveis de dados macroeconômicos.
2. Criar job para atualização periódica dos dados.
3. Construir API para consulta dos dados atualizados.
4. Implementar cache para otimização.
5. Testar respostas e performance da API.

### Desenvolver microserviço Recomendações

1. Definir algoritmo de recomendação baseado em regras.
2. Implementar lógica de análise do perfil + contexto.
3. Criar endpoints para consulta das carteiras recomendadas.
4. Integrar persistência no Oracle.
5. Validar e testar recomendações geradas.

### Documentar APIs com Swagger/OpenAPI

1. Descrever cada endpoint com métodos, parâmetros e respostas.
2. Inserir exemplos de payload para requisição e resposta.
3. Validar documentação automatizada com Swagger UI.
4. Compartilhar documentação com equipe e ajustar conforme feedback.
5. Atualizar documentação a cada alteração da API.

### Configurar Azure API Management

1. Criar instância do API Management no Azure.
2. Importar APIs REST do backend para o serviço.
3. Definir políticas de segurança e throttling.
4. Configurar monitoramento e relatórios.
5. Testar publicação e acesso controlado das APIs.

---

## 2. Mobile Development (React Native + Azure)

### Protótipo no Figma

1. Levantar requisitos e fluxos principais do app.
2. Criar wireframes para as telas essenciais.
3. Aplicar identidade visual e design detalhado.
4. Construir protótipo navegável para validação.
5. Coletar feedback e ajustar design.

### Desenvolvimento Tela Perfil/Suitability

1. Criar layout da tela com campos de dados.
2. Implementar componentes editáveis.
3. Implementar chamada API para carregamento de dados.
4. Implementar envio de alterações para backend.
5. Testar tela em dispositivos reais.

### Desenvolvimento Navegação

1. Configurar React Navigation no projeto.
2. Definir rotas e stacks das telas.
3. Implementar navegação condicional (ex: autenticação).
4. Testar fluxo completo do usuário.
5. Corrigir bugs e otimizar transições.

### Persistência local AsyncStorage

1. Definir dados que serão armazenados localmente.
2. Implementar gravação e leitura no AsyncStorage.
3. Garantir sincronização com backend.
4. Tratar erros e inconsistências de dados.
5. Testar uso offline e recuperação de dados.

### Desenvolvimento Autenticação

1. Criar tela/login form para entrada do usuário.
2. Implementar chamada API para autenticação.
3. Armazenar token JWT recebido.
4. Gerenciar estado de autenticação no app.
5. Implementar logout e limpeza de dados.

### Testes e ajustes UI responsiva

1. Testar telas em múltiplos tamanhos de tela e dispositivos.
2. Ajustar layouts com Flexbox e estilos responsivos.
3. Corrigir problemas de overflow e posicionamento.
4. Validar acessibilidade básica.
5. Realizar testes de usabilidade com usuários.

### Configurar Azure Notification Hubs

1. Criar recurso Notification Hub no Azure.
2. Integrar SDK no app React Native.
3. Implementar recepção e exibição de notificações.
4. Criar serviço backend para envio de notificações.
5. Testar envio e recebimento em vários dispositivos.

---

## 3. Operating Systems e Infraestrutura (Azure)

### Provisionar Azure VM para Oracle DB

1. Criar grupo de recursos no Azure.
2. Provisionar máquina virtual com especificações necessárias.
3. Instalar Oracle Database e dependências.
4. Configurar regras de firewall e NSG.
5. Validar instalação e acesso remoto seguro.

### Configurar VPN Gateway/ExpressRoute

1. Criar recurso VPN Gateway no Azure.
2. Configurar conexões VPN para redes locais/Oracle Cloud.
3. Configurar ExpressRoute para alta performance (opcional).
4. Testar conectividade e performance.
5. Documentar configuração para manutenção.

### Criar Container Registry e AKS

1. Criar Azure Container Registry (ACR).
2. Configurar pipelines de build para imagens Docker.
3. Provisionar Azure Kubernetes Service (AKS).
4. Configurar clusters e deploy inicial.
5. Testar escalabilidade e atualizações.

### Configurar Azure Security Center

1. Ativar Security Center para recursos Azure.
2. Aplicar políticas de segurança recomendadas.
3. Configurar alertas e monitoramento.
4. Auditar configurações e compliance.
5. Revisar e ajustar conforme novas ameaças.

### Configurar monitoramento

1. Ativar Azure Monitor para VMs e AKS.
2. Configurar Application Insights para apps backend.
3. Integrar logs do Oracle com Azure Monitor.
4. Criar dashboards personalizados.
5. Definir alertas críticos.

### Automatizar CI/CD com Azure DevOps

1. Criar projetos e repositórios no Azure DevOps.
2. Configurar pipeline para build automático.
3. Implementar testes automatizados no pipeline.
4. Criar pipeline de deploy para Azure AKS/VM.
5. Validar e ajustar pipeline continuamente.

---

## 4. Testing, Compliance and Quality Assurance (QA)

### Definir objetivos e problemas

1. Reunir equipe para alinhamento do escopo.
2. Documentar o problema a ser resolvido.
3. Estabelecer objetivos mensuráveis.
4. Validar entendimento com stakeholders.
5. Formalizar em documento.

### Pesquisar produtos similares

1. Identificar concorrentes diretos e indiretos.
2. Analisar funcionalidades e limitações.
3. Comparar arquiteturas e tecnologias.
4. Documentar pontos fortes e fracos.
5. Apresentar relatório para equipe.

### Criar diagramas TOGAF no Archi

1. Definir Motivation View: missão, visão, valores.
2. Modelar Business Layer: processos, atores, serviços.
3. Modelar Application Layer: sistemas e integrações.
4. Modelar Technology Layer: infraestrutura e segurança.
5. Exportar diagramas com documentação associada.

### Planejar e executar testes

1. Definir critérios e métricas para testes.
2. Escrever casos de teste unitários e de integração.
3. Criar ambiente e dados para testes.
4. Executar testes e registrar resultados.
5. Corrigir defeitos encontrados.

### Definir métricas e KPIs

1. Escolher indicadores de qualidade, performance e segurança.
2. Configurar ferramentas para coleta e monitoramento.
3. Estabelecer metas e limites aceitáveis.
4. Documentar processos para análise contínua.
5. Revisar e ajustar indicadores periodicamente.

---

## 5. Cybersecurity

### Configurar autenticação Azure AD

1. Criar e configurar Azure Active Directory tenant.
2. Registrar aplicações e configurar permissões.
3. Implementar login com OAuth2/Microsoft Identity no backend.
4. Ativar MFA para usuários sensíveis.
5. Testar autenticação em diferentes cenários.

### Implementar Azure Key Vault

1. Criar cofre no Azure Key Vault.
2. Armazenar segredos, certificados e chaves.
3. Configurar acesso controlado por identidade gerenciada.
4. Integrar Key Vault com aplicações e bancos.
5. Monitorar uso e acesso.

### Configurar criptografia Oracle TDE

1. Ativar Transparent Data Encryption no Oracle DB.
2. Gerenciar chaves de criptografia com segurança.
3. Validar proteção em dados armazenados.
4. Testar performance após ativação.
5. Documentar configuração para auditoria.

### Implementar testes de segurança

1. Planejar cenários para testes de entrada maliciosa.
2. Automatizar testes com ferramentas de segurança.
3. Executar pentests básicos e análise de vulnerabilidades.
4. Corrigir e revalidar falhas encontradas.
5. Documentar resultados e ações.

### Monitorar com Azure Sentinel

1. Configurar conectores de log para Azure Sentinel.
2. Criar regras de detecção de ameaças.
3. Definir playbooks de resposta automática.
4. Monitorar alertas e incidentes em tempo real.
5. Ajustar regras e playbooks conforme necessário.

### Implementar controle LGPD

1. Desenvolver funcionalidades para acesso do usuário aos dados.
2. Permitir edição e exclusão conforme requisições.
3. Criar logs de auditoria para essas operações.
4. Garantir comunicação clara da política de privacidade.
5. Validar conformidade legal regularmente.

---

