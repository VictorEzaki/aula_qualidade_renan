# Quais as características de um tester ágil?
As características de um tester ágil estão relacionadas principalmente às habilidades essenciais de teste, ao whole team approach e à adaptação do teste em ambientes ágeis. O tester ágil não atua isoladamente; ele participa ativamente do time de desenvolvimento e colabora continuamente com os demais membros da equipe.

- **Colaboração com a equipe:** trabalha integrado ao time de desenvolvimento, participando da definição de requisitos, critérios de aceitação e estratégias de teste.

- **Boa comunicação:** relata defeitos e resultados de testes de forma clara e construtiva para os stakeholders.

- **Pensamento analítico e crítico:** analisa o sistema, identifica riscos e cria cenários de teste eficazes.

- **Atenção aos detalhes e curiosidade:** ajuda a identificar defeitos que não são facilmente percebidos.

- **Conhecimento técnico e do domínio do negócio:** permite criar testes mais eficientes e alinhados às necessidades do sistema.

Em resumo, o tester ágil é um profissional colaborativo, analítico e comunicativo, que contribui ativamente para garantir a qualidade do produto dentro da equipe.

# Em qual momento os testes ágeis aparecem no desenvolvimento de um software?
Nos métodos ágeis, os testes não acontecem apenas no final do desenvolvimento. Eles aparecem durante todo o ciclo de desenvolvimento, acompanhando cada etapa do trabalho da equipe.

Os principais momentos são:

1. Durante a definição de requisitos (histórias de usuário)
Os testers participam da criação das histórias de usuário e ajudam a definir critérios de aceitação, que servirão como base para os testes.

2. Antes do desenvolvimento (test-first)
Em abordagens como TDD, ATDD e BDD, os testes são escritos antes do código, servindo como guia para o desenvolvimento da funcionalidade.

3. Durante o desenvolvimento
Enquanto o código está sendo implementado, são executados testes como:

testes unitários (geralmente feitos pelos desenvolvedores);

revisões e testes exploratórios iniciais.

4. Após a implementação da funcionalidade
São realizados testes para validar o comportamento do sistema, como:

-  testes de integração;

- testes de sistema;

- testes de aceitação para verificar se a funcionalidade atende aos critérios definidos.

5. A cada nova entrega ou alteração
São executados testes de regressão, muitas vezes automatizados, para garantir que novas mudanças não quebraram funcionalidades existentes.

# Quando um code review faz sentido e quando ele deixa de fazer sentido?
Um code review faz sentido quando ele realmente contribui para melhorar a qualidade do código, compartilhar conhecimento e evitar erros antes que o código seja integrado ao projeto. Porém, em alguns contextos ele pode deixar de trazer benefícios.

Quando faz sentido:

- Antes de integrar código ao repositório principal (por exemplo, em um pull request).

- Quando o código é complexo ou crítico, pois outra pessoa pode identificar problemas de lógica, segurança ou desempenho.

- Para padronização do código, garantindo que boas práticas e padrões do projeto sejam seguidos.

- Para compartilhamento de conhecimento, permitindo que outros desenvolvedores entendam melhor partes do sistema.

Quando deixa de fazer sentido:

- Quando vira apenas burocracia, com revisões rápidas que não analisam o código de fato.

- Quando atrasa muito o desenvolvimento, bloqueando entregas sem trazer melhorias reais.

- Quando o código é muito simples ou trivial, onde o custo da revisão pode ser maior que o benefício.

- Quando o processo se torna excessivamente crítico ou pessoal, prejudicando a colaboração da equipe.
