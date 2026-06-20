# Anotações de Aula: Qualidade e Teste de Software

## 1. Princípios de Teste (ISTQB)
Os 7 princípios fundamentais que guiam a atividade de teste:

1.  **O teste mostra a presença de defeitos, não a ausência:** O teste reduz a probabilidade de defeitos ocultos, mas não prova que o software está 100% correto.
2.  **Teste exaustivo é impossível:** Testar tudo é inviável. Deve-se focar em riscos e prioridades.
3.  **Teste antecipado:** Atividades de teste devem começar o mais cedo possível no ciclo de vida (*Shift Left*).
4.  **Agrupamento de defeitos:** Um pequeno número de módulos geralmente contém a maioria dos defeitos (Regra de 80/20).
5.  **Paradoxo do Pesticida:** Se os mesmos testes forem repetidos, eles deixarão de encontrar novos defeitos. Os testes precisam ser revisados.
6.  **Teste depende do contexto:** Testar um site de e-commerce é diferente de testar um software de controle industrial.
7.  **Ausência de erros é uma ilusão:** Encontrar e fixar defeitos não ajuda se o sistema for inutilizável ou não atender às expectativas do usuário.

---

## 2. Níveis de Teste
Definem o alvo ou o escopo do que está sendo testado.

* **Teste de Unidade (Componente):** Foca em partes isoladas do código (funções, métodos, classes).
    * *Exemplo:* Testar se a função de cálculo de desconto retorna o valor correto para uma compra.
* **Teste de Integração:** Foca nas interfaces e interações entre componentes ou sistemas.
    * *Exemplo:* Verificar se o módulo de "Pedido" consegue ler corretamente os dados do "Cadastro de Usuário".
* **Teste de Sistema:** Testa o comportamento do produto completo e integrado em relação aos requisitos.
    * *Exemplo:* Testar o fluxo completo de compra, do login ao fechamento do pedido.
* **Teste de Aceite:** Validação final feita para verificar se o sistema está pronto para o usuário final.
    * *Exemplo:* O cliente final realiza testes para validar se as telas atendem ao que foi solicitado no contrato.

---

## 3. Tipos de Teste
Referem-se ao objetivo do teste (funcionalidade, desempenho, estrutura).

* **Testes Funcionais:** Avaliam "o que" o sistema faz.
    * *Exemplo:* Verificar se o sistema permite cadastrar um usuário com e-mail válido.
* **Testes Não Funcionais:** Avaliam características como desempenho, usabilidade e segurança.
    * *Exemplo:* Testar se o sistema aguenta 500 usuários simultâneos (Teste de Carga).
* **Teste de Caixa-Branca:** Baseado na estrutura interna/código do software.
    * *Exemplo:* Verificar se todos os caminhos de uma estrutura `switch/case` foram executados.
* **Teste de Caixa-Preta:** Baseado nos requisitos, sem olhar o código interno.
    * *Exemplo:* Inserir dados em um formulário e verificar se a saída está correta.

---

## 4. Técnicas de Teste
Métodos para selecionar os melhores casos de teste.

### Técnicas de Caixa-Preta
* **Particionamento de Equivalência:** Divide os dados em grupos que devem ser processados da mesma forma.
    * *Exemplo:* Se um campo aceita idades de 18 a 60, testa-se um valor no meio (ex: 30) para representar todo o grupo.
* **Análise de Valor Limite:** Testa os extremos dos intervalos.
    * *Exemplo:* No campo de 18 a 60 anos, testar exatamente 17, 18, 60 e 61.
* **Tabela de Decisão:** Ideal para regras de negócio complexas com múltiplas condições.
    * *Exemplo:* Testar combinações de "Usuário Ativo" + "Possui Crédito" + "Primeira Compra".
* **Transição de Estado:** Testa as mudanças de comportamento do sistema conforme as ações.
    * *Exemplo:* Um pedido que passa de "Pendente" para "Pago" e depois "Enviado".
* **Teste de Caso de Uso:** Baseado em cenários reais de interação do usuário.
    * *Exemplo:* Realizar um fluxo de "Recuperação de Senha" do início ao fim.

### Técnicas Baseadas na Experiência
* **Suposição de Erro:** O testador antecipa erros com base no conhecimento de falhas anteriores.
    * *Exemplo:* Testar o que acontece se o usuário deixar um campo obrigatório em branco.
* **Teste Exploratório:** O testador aprende sobre o sistema enquanto desenha e executa os testes simultaneamente.
    * *Exemplo:* Navegar livremente por uma funcionalidade nova para entender seus limites.
