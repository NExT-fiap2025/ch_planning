# Documento de Requisitos – Assessor Virtual Inteligente para Plataformas de Investimento

## 1. Introdução

### 1.1 Contexto

O projeto visa desenvolver um Assessor Virtual Inteligente que apoia assessores humanos na recomendação de carteiras personalizadas e educa clientes finais com conteúdos acessíveis e gamificação.

### 1.2 Objetivos

- Otimizar o trabalho dos assessores humanos aumentando sua produtividade.
- Educar e engajar os clientes finais por meio de recomendações claras e personalizadas.
- Promover inclusão financeira alinhada a práticas ESG.

---

## 2. Regras de Negócio

### 2.1 Decisão e Recomendações

- **RN1:** O Assessor Virtual **não toma a decisão final** sobre a carteira de investimentos.
- **RN2:** Ele pode sugerir a carteira que mais recomenda, mas as decisões finais são do assessor humano ou do cliente.
- **RN3:** As sugestões devem ser submetidas ao assessor humano antes de serem apresentadas ao cliente final para validação e ajustes.

### 2.2 Apresentação das Opções

- **RN4:** O cliente deve receber todas as opções de carteiras recomendadas, com explicações claras e acessíveis para facilitar a escolha informada.
- **RN5:** Recomendações devem ser atualizadas automaticamente com base no perfil de risco do cliente e mudanças macroeconômicas, incluindo justificativas e explicações das alterações.

### 2.3 Personalização e Controle de Perfil

- **RN6:** As recomendações devem considerar o perfil de risco (conservador, moderado, agressivo) e os objetivos financeiros do cliente em curto, médio e longo prazo.
- **RN7:** O cliente pode solicitar alteração do perfil de risco, porém essa mudança depende de progresso na gamificação e autorização segura, com validação via código eletrônico enviado por e-mail.

### 2.4 Educação e Interação

- **RN8:** O sistema deve oferecer educação financeira contínua, com explicações simples sobre ativos e conceitos.
- **RN9:** O cliente pode interagir com o assistente para tirar dúvidas e receber orientações.
- **RN10:** Deve existir uma jornada gamificada que engaje e recompense o progresso do cliente.

### 2.5 Monitoramento e Alertas

- **RN11:** O sistema deve alertar clientes e assessores sobre riscos, oportunidades e mudanças relevantes no mercado.
- **RN12:** Sempre que possível, recomendações devem considerar critérios ESG, promovendo investimentos socialmente responsáveis.

### 2.6 Histórico e Auditoria

- **RN13:** Todas as interações, recomendações, decisões e ajustes devem ser registrados para auditoria, segurança e transparência.

### 2.7 Flexibilidade e Limitações

- **RN14:** O sistema pode sugerir investimentos fora do portfólio padrão, mas deve indicar que tais opções não são recomendadas e requerem atenção do assessor humano.
- **RN15:** A plataforma gerencia o banco de ativos disponíveis; o assessor humano pode ajustar, mas não criar novos ativos fora do banco.

### 2.8 Comunicação e Relatórios

- **RN16:** O cliente receberá notificações personalizadas sobre mudanças em carteiras, recompensas e outras interações.
- **RN17:** Assessores terão acesso a relatórios periódicos com análises do comportamento e progresso dos clientes.

### 2.9 Planejamento e Simulação

- **RN18:** O sistema sugerirá estratégias de diversificação alinhadas ao risco e planejamento financeiro do cliente.
- **RN19:** Clientes poderão simular diferentes cenários de investimento para entender impactos e riscos.

### 2.10 Integração e Atualização

- **RN20:** O sistema deve integrar-se com plataformas externas (bancos, corretoras) para atualização automática de dados financeiros e de mercado.

## 3. Requisitos Funcionais (RF)

### RF1 – Cadastro e Autenticação

- RF1.1 O sistema deve permitir cadastro de usuários (clientes e assessores).
- RF1.2 O sistema deve autenticar usuários via login com senha e token JWT.
- RF1.3 O sistema deve permitir recuperação e redefinição de senha.

### RF2 – Gestão de Perfil

- RF2.1 O cliente pode criar e editar seu perfil financeiro e suitability.
- RF2.2 O assessor pode consultar os perfis dos clientes vinculados.

### RF3 – Recebimento e Atualização de Dados Macroeconômicos

- RF3.1 O sistema deve importar periodicamente dados macroeconômicos (taxa Selic, inflação, câmbio).
- RF3.2 O sistema deve disponibilizar esses dados para serviços internos via API.

### RF4 – Geração de Recomendações

- RF4.1 O sistema deve analisar perfil do cliente e contexto macroeconômico para sugerir até quatro carteiras recomendadas.
- RF4.2 Cada recomendação deve incluir explicação clara e educativa para o cliente.
- RF4.3 O assessor pode consultar e ajustar as recomendações manualmente.

### RF5 – Gamificação e Engajamento

- RF5.1 O sistema deve oferecer uma jornada gamificada para o cliente, com conquistas e recompensas.
- RF5.2 O progresso do cliente deve ser registrado e exibido em sua interface.

### RF6 – Monitoramento e Histórico

- RF6.1 O sistema deve armazenar o histórico de interações, recomendações e respostas do cliente.
- RF6.2 O assessor deve acessar histórico para melhorar o atendimento.

---

## 4. Requisitos Não Funcionais (RNF)

### RNF1 – Segurança

- RNF1.1 Dados sensíveis devem ser criptografados em trânsito e em repouso.
- RNF1.2 A autenticação deve utilizar mecanismos seguros (JWT, MFA).
- RNF1.3 O sistema deve seguir LGPD, permitindo controle do usuário sobre seus dados.

### RNF2 – Usabilidade

- RNF2.1 A interface deve ser acessível e intuitiva, para usuários com diferentes níveis de conhecimento.
- RNF2.2 As explicações devem usar linguagem simples e direta.

### RNF3 – Desempenho

- RNF3.1 As APIs devem responder a requisições em até 2 segundos na maioria dos casos.
- RNF3.2 O sistema deve suportar simultaneamente pelo menos 500 usuários ativos.

### RNF4 – Disponibilidade

- RNF4.1 O sistema deve ter disponibilidade mínima de 99,5% mensal.
- RNF4.2 O banco Oracle e serviços relacionados devem ter alta disponibilidade configurada.

### RNF5 – Escalabilidade

- RNF5.1 O sistema deve ser escalável horizontalmente para suportar crescimento da base de usuários.

### RNF6 – Manutenibilidade

- RNF6.1 O código deve seguir padrões de projeto e estar bem documentado.
- RNF6.2 As APIs devem ser documentadas via Swagger/OpenAPI.

---

---

## 5. Requisitos Tecnológicos

### RT1 – Infraestrutura e Plataforma

- O sistema deverá ser hospedado na **Microsoft Azure**, utilizando serviços como:

  - **Azure Virtual Machines (VM)** para hospedar o Oracle Database.
  - **Azure Kubernetes Service (AKS)** para orquestração dos microserviços Java.
  - **Azure API Management** para gestão e exposição das APIs REST.
  - **Azure DevOps** para pipelines de CI/CD, gerenciamento de código e automação.
  - **Azure Monitor e Application Insights** para monitoramento, logs e métricas.
  - **Azure VPN Gateway** ou **ExpressRoute** para conexão segura entre componentes.

### RT2 – Banco de Dados

- O banco de dados utilizado será o **Oracle Database**, hospedado em VM no Azure.
- Deverá ser configurado para alta disponibilidade, segurança (TDE) e backup automático.
- Integração com microserviços via drivers oficiais compatíveis com Java/Spring Boot.

### RT3 – Desenvolvimento Backend

- Utilizar **Java 17+** com **Spring Boot 3+** para construção dos microserviços.
- Documentação de APIs via **Swagger/OpenAPI**.
- Uso de padrões de projeto para garantir modularidade, escalabilidade e manutenção.

### RT4 – Desenvolvimento Frontend Mobile

- Utilizar **React Native** com **TypeScript** para desenvolvimento do aplicativo móvel.
- Utilização de **Azure App Center** para build, testes e distribuição.
- Integração com backend via chamadas REST seguras.

### RT5 – Segurança

- Implementar autenticação e autorização via **Azure Active Directory (AAD)**.
- Gerenciar segredos, chaves e certificados via **Azure Key Vault**.
- Aplicar criptografia TLS para comunicação entre sistemas.

### RT6 – Ferramentas de Teste e Qualidade

- Utilizar **Azure Test Plans** para gerenciamento dos testes.
- Integração com pipelines para testes automatizados.
- Análise de código com ferramentas compatíveis para garantir qualidade.

---

## 6. Critérios de Aceitação

- Usuários conseguem criar e editar perfil com sucesso.
- As recomendações são geradas automaticamente e incluem explicações claras.
- A gamificação funciona e registra progresso corretamente.
- Os dados macroeconômicos são atualizados e disponibilizados corretamente.
- O sistema protege os dados conforme a LGPD e implementa autenticação segura.
- O sistema atende às metas de desempenho e disponibilidade.
