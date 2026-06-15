# Análise de Risco

Atividade referente à apresentação **08 - Qualidade e Teste - Análise de Risco**, considerando os cenários reportados nas páginas **24 a 30**.

---

## 1. Risco: Interrupção temporária do serviço devido à manutenção programada

**Probabilidade:** C

**Impacto:** 3

**Matriz do Risco:** C3 - Médio

**Testes utilizados:** Teste de disponibilidade, Teste de regressão, Teste funcional, Teste de sistema

**Estratégia de mitigação:** Planejar a manutenção para horários de menor uso, comunicar os usuários com antecedência, criar uma página de aviso de indisponibilidade, realizar backup antes da manutenção e executar testes de regressão após o retorno do sistema para garantir que as funcionalidades principais continuam funcionando corretamente.

**Tipos de Risco:**

**Técnico:** O sistema pode não retornar corretamente após a manutenção, apresentar falhas em serviços, APIs, banco de dados ou integrações.

**Operacional:** A equipe pode não seguir corretamente o plano de manutenção, esquecer etapas importantes ou não validar o ambiente após a atualização.

**Negócio:** A indisponibilidade pode impedir usuários de acessarem o sistema, prejudicar vendas, atendimentos ou processos internos durante o período de manutenção.

**Usuário:** Usuários podem tentar acessar o sistema durante a manutenção e não entender o motivo da indisponibilidade caso não exista uma comunicação clara.

---

## 2. Risco: Vulnerabilidade de segurança em dependência de terceiros

**Probabilidade:** D

**Impacto:** 5

**Matriz do Risco:** D5 - Crítico

**Testes utilizados:** Teste de segurança, Análise de vulnerabilidades, Teste de regressão, Teste automatizado de dependências

**Estratégia de mitigação:** Manter bibliotecas, frameworks e pacotes sempre atualizados, utilizar ferramentas como `npm audit`, Dependabot ou Snyk, remover dependências desnecessárias, acompanhar alertas de segurança e validar o sistema após atualizações para garantir que nenhuma funcionalidade foi quebrada.

**Tipos de Risco:**

**Técnico:** Uma dependência vulnerável pode permitir falhas no sistema, execução de código indevido, quebra de funcionalidades ou incompatibilidade após atualizações.

**Segurança:** A vulnerabilidade pode permitir acesso não autorizado, vazamento de dados, exploração de falhas conhecidas ou comprometimento da aplicação.

**Negócio:** Uma falha de segurança pode gerar perda de confiança dos usuários, prejuízo financeiro, danos à imagem da empresa e possíveis problemas legais.

**Operacional:** A equipe pode não perceber rapidamente a existência da vulnerabilidade ou demorar para aplicar correções, aumentando a exposição do sistema.

---

## 3. Risco: Erro de interface do usuário causando confusão

**Probabilidade:** C

**Impacto:** 3

**Matriz do Risco:** C3 - Médio

**Testes utilizados:** Teste funcional, Teste de usabilidade, Teste de regressão, Teste automatizado E2E

**Estratégia de mitigação:** Realizar testes de usabilidade com usuários, revisar textos, botões, mensagens e fluxos da interface, padronizar componentes visuais, validar os principais caminhos do sistema com testes funcionais e criar testes automatizados E2E para fluxos críticos.

**Tipos de Risco:**

**Técnico:** Componentes da interface podem estar mal implementados, botões podem executar ações erradas, mensagens podem não aparecer corretamente ou telas podem apresentar problemas de renderização.

**Humano:** O usuário pode interpretar incorretamente botões, mensagens, campos ou etapas do sistema, realizando ações erradas ou abandonando o fluxo.

**Negócio:** Uma interface confusa pode reduzir a satisfação dos usuários, aumentar chamados de suporte, diminuir conversões ou prejudicar o uso do sistema.

**Usabilidade:** O sistema pode até funcionar corretamente do ponto de vista técnico, mas não atender bem às necessidades do usuário por ser difícil de entender ou utilizar.

---

## 4. Risco: Falha no processo de backup de dados

**Probabilidade:** C

**Impacto:** 5

**Matriz do Risco:** C5 - Alto

**Testes utilizados:** Teste de recuperação, Teste de integridade de backup, Teste de banco de dados, Teste de regressão

**Estratégia de mitigação:** Configurar backups automáticos, armazenar cópias em locais seguros, definir política de retenção, monitorar falhas no processo de backup e realizar testes periódicos de restauração para garantir que os dados podem ser recuperados corretamente em caso de incidente.

**Tipos de Risco:**

**Técnico:** O backup pode não ser gerado corretamente, ficar corrompido, estar incompleto ou não ser compatível com o processo de restauração.

**Operacional:** A equipe pode não monitorar os backups, não testar a restauração ou não perceber falhas no processo até ocorrer um problema real.

**Negócio:** A perda de dados pode comprometer operações, gerar prejuízos, afetar clientes e prejudicar a continuidade do serviço.

**Segurança:** Backups mal protegidos podem expor informações sensíveis caso sejam acessados por pessoas não autorizadas.

---

## 5. Risco: Ataque de phishing aos usuários do aplicativo

**Probabilidade:** D

**Impacto:** 5

**Matriz do Risco:** D5 - Crítico

**Testes utilizados:** Teste de segurança, Teste de engenharia social simulado, Teste de autenticação, Teste de aceite

**Estratégia de mitigação:** Orientar os usuários sobre mensagens falsas, utilizar autenticação em dois fatores, configurar mecanismos de segurança em e-mails como SPF, DKIM e DMARC, monitorar acessos suspeitos, criar alertas de login e manter canais oficiais de comunicação bem definidos.

**Tipos de Risco:**

**Técnico:** O sistema pode não possuir mecanismos suficientes para detectar acessos suspeitos, proteger contas ou alertar usuários sobre tentativas de fraude.

**Humano:** Usuários podem clicar em links falsos, informar senhas em páginas fraudulentas ou confiar em mensagens que aparentam ser oficiais.

**Segurança:** Contas podem ser invadidas, dados pessoais podem ser expostos e acessos indevidos podem ocorrer dentro do sistema.

**Negócio:** Um ataque de phishing pode afetar a reputação da empresa, gerar perda de confiança, aumentar chamados de suporte e causar prejuízos financeiros.

---

# Resumo Geral da Matriz de Risco

| Cenário | Probabilidade | Impacto | Matriz do Risco | Classificação |
|---|---:|---:|---|---|
| Interrupção temporária do serviço devido à manutenção programada | C | 3 | C3 | Médio |
| Vulnerabilidade de segurança em dependência de terceiros | D | 5 | D5 | Crítico |
| Erro de interface do usuário causando confusão | C | 3 | C3 | Médio |
| Falha no processo de backup de dados | C | 5 | C5 | Alto |
| Ataque de phishing aos usuários do aplicativo | D | 5 | D5 | Crítico |

---

# Conclusão

A análise dos cenários mostra que os riscos mais críticos estão relacionados à segurança, principalmente a vulnerabilidade em dependências de terceiros e o ataque de phishing aos usuários. Esses riscos possuem alta probabilidade e alto impacto, pois podem comprometer dados, acessos, confiança dos usuários e a continuidade do negócio.

Também foram identificados riscos importantes relacionados à disponibilidade, usabilidade e backup. Mesmo quando o risco não é classificado como crítico, ele precisa ser tratado com planejamento, testes adequados e ações preventivas.

Dessa forma, a aplicação de testes funcionais, testes de regressão, testes de usabilidade, testes de segurança, testes de recuperação e testes automatizados contribui para reduzir falhas, melhorar a qualidade do software e proteger os usuários.