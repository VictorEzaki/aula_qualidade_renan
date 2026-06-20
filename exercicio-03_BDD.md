# BDD de um CRUD + Login

## Login no Sistema

### Cenário: Login com credenciais válidas
* **Given** o usuário está na tela de login e possui credenciais válidas
* **When** o usuário informa e-mail e senha e clica no botão Entrar
* **Then** o sistema autentica o usuário e redireciona para a página inicial

---

### Cenário: Login com credenciais inválidas
* **Given** o usuário está na tela de login
* **When** o usuário informa e-mail ou senha incorretos e clica no botão Entrar
* **Then** o sistema exibe a mensagem “Credenciais inválidas” e o acesso não é permitido

---

## CRUD de Usuário

### Create (Criar usuário)
**Cenário: Cadastrar novo usuário**
* **Given** o usuário está na tela de cadastro de usuário
* **When** o usuário preenche nome, e-mail e senha e clica no botão Cadastrar
* **Then** o sistema registra o novo usuário e exibe uma mensagem de sucesso

---

### Read (Consultar usuários)
**Cenário: Visualizar lista de usuários**
* **Given** existem usuários cadastrados no sistema
* **When** o usuário acessa a tela de listagem de usuários
* **Then** o sistema exibe a lista de usuários cadastrados com nome e e-mail

---

### Update (Atualizar usuário)
**Cenário: Atualizar dados do usuário**
* **Given** existe um usuário cadastrado no sistema e o usuário está na tela de edição
* **When** o usuário altera as informações do usuário e clica no botão Salvar
* **Then** o sistema atualiza os dados do usuário e exibe uma mensagem de confirmação

---

### Delete (Excluir usuário)
**Cenário: Excluir usuário**
* **Given** existe um usuário cadastrado no sistema
* **When** o usuário seleciona a opção Excluir usuário e confirma a exclusão
* **Then** o sistema remove o usuário do cadastro e atualiza a lista exibida

## Princípios de Teste

Os princípios de teste são fundamentais para entender que o objetivo do teste não é apenas "encontrar bugs", mas sim garantir a qualidade e reduzir riscos.

Segundo o **ISTQB**, existem 7 princípios de testes:

### 1. O teste mostra a presença de defeitos, não a ausência
Testar um software pode mostrar que existem defeitos, mas **não prova que ele está 100% livre de erros**. Mesmo após uma bateria intensa de testes, não podemos afirmar que não há nenhum bug escondido.

### 2. Teste exaustivo é impossível
Testar todas as combinações de dados e caminhos lógicos é inviável (levaria tempo e recursos infinitos). Por isso, usamos **análise de risco e priorização** para focar nos cenários que realmente importam.

### 3. Teste antecipado
Quanto mais cedo você começar a testar, melhor. Iniciar os testes logo no início do ciclo de vida (até na revisão de requisitos) ajuda a encontrar problemas antes que eles se tornem caros e difíceis de corrigir.

### 4. Agrupamento de defeitos 
Geralmente, a maioria dos problemas se concentra em um pequeno número de módulos ou funcionalidades. Se você encontrar muitos bugs em uma área específica, é bem provável que existam outros ali. É a aplicação do **Princípio de Pareto (80/20)**.

### 5. Paradoxo do Pesticida
Se você repetir os mesmos testes várias vezes, eles deixarão de encontrar novos bugs. Assim como as pragas criam resistência a pesticidas, o software "se acostuma" aos testes. É preciso **revisar e atualizar** os casos de teste constantemente.

### 6. Teste depende do contexto
Um aplicativo de banco (crítico e seguro) é testado de forma totalmente diferente de um jogo de celular ou de um blog. O **contexto dita a estratégia**, o rigor e as ferramentas utilizadas.

### 7. A ilusão da ausência de erros
Não adianta nada ter um sistema que funciona perfeitamente (sem bugs aparentes) se ele **não atende às necessidades do usuário** ou se é difícil de usar. Encontrar e consertar defeitos não ajuda se o sistema for inútil.
