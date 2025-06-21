## Documentação de Casos de Uso - Gerenciamento Casa de Axé

### 1. CU001: Gerenciar Membros (Filhos de Santo)

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova informações de membros da casa (filhos de santo). Inclui dados pessoais (nome, telefone, data de nascimento), data de entrada na casa, data de coroação e orixás de cabeça (pai de cabeça e mãe de cabeça).
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões de gerenciamento de membros adequadas.
* **Pós-condições:** As informações do membro são persistidas, atualizadas ou removidas no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Membros".
   2.  O sistema exibe a interface de gerenciamento de membros.
   3.  O Ator pode escolher uma das seguintes ações:
          * **Cadastrar Novo Membro:**
             1.  O Ator preenche os campos com os dados pessoais do membro (nome, telefone, data de nascimento), data de entrada na casa e data de coroação.
             2.  O sistema valida os dados inseridos.
             3.  O sistema salva as informações do novo membro.
          * **Visualizar Membros Existentes:**
             1.  O sistema exibe uma lista de todos os membros cadastrados.
             2.  O Ator pode utilizar filtros ou a barra de pesquisa para localizar membros específicos.
          * **Editar Membro Existente:**
             1.  O Ator seleciona um membro da lista para edição.
             2.  O sistema carrega os dados do membro na interface de edição.
             3.  O Ator modifica os campos desejados.
             4.  O sistema valida as alterações.
             5.  O sistema atualiza as informações do membro.
          * **Remover Membro Existente:**
             1.  O Ator seleciona um membro da lista para remoção.
             2.  O sistema solicita uma confirmação da remoção.
             3.  O sistema remove o membro do registro.
* **Fluxos Alternativos:**
   * **FA1.1: Campos Obrigatórios Não Preenchidos/Inválidos:**
      1.  No passo 3.1.2 ou 3.3.4 (Cadastrar/Editar Membro), se o Ator não preencher campos obrigatórios ou fornecer dados inválidos, o sistema exibe uma mensagem de erro indicando os campos problemáticos.
      2.  O Ator corrige os dados e tenta novamente.
   * **FA1.2: Orixás de Cabeça Antes da Coroação:**
      1.  No passo 3.1.1 ou 3.3.3 (Cadastrar/Editar Membro), os campos para os orixás de cabeça (pai de cabeça e mãe de cabeça) são desabilitados se a data de coroação não estiver preenchida.
      2.  O Ator deve preencher a data de coroação antes de poder inserir os orixás de cabeça.
* **Regras de Negócio Aplicáveis:** RN01, RN09

### 2. CU002: Gerenciar Visitantes

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova informações de visitantes da casa.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões de gerenciamento adequadas.
* **Pós-condições:** As informações do visitante são persistidas, atualizadas ou removidas no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Visitantes".
   2.  O sistema exibe a interface de gerenciamento de visitantes.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Novo Visitante:**
         1.  O Ator preenche os dados pessoais do visitante (nome, telefone) e quaisquer observações relevantes.
         2.  O sistema valida os dados inseridos.
         3.  O sistema salva as informações do novo visitante.
      * **Visualizar Visitantes Existentes:**
         1.  O sistema exibe uma lista de todos os visitantes cadastrados.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa para localizar visitantes específicos.
      * **Editar Visitante Existente:**
         1.  O Ator seleciona um visitante da lista para edição.
         2.  O sistema carrega os dados do visitante na interface de edição.
         3.  O Ator modifica os campos desejados.
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações do visitante.
      * **Remover Visitante Existente:**
         1.  O Ator seleciona um visitante da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove o visitante do registro.
* **Fluxos Alternativos:**
   * **FA2.1: Campos Obrigatórios Não Preenchidos/Inválidos:**
      1.  No passo 3.1.2 ou 3.3.4 (Cadastrar/Editar Visitante), se o Ator não preencher campos obrigatórios ou fornecer dados inválidos, o sistema exibe uma mensagem de erro indicando os campos problemáticos.
      2.  O Ator corrige os dados e tenta novamente.

### 3. CU003: Gerenciar Guias Espirituais

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova informações sobre os guias espirituais, incluindo seu nome, o membro ao qual ele incorpora, a linha espiritual a que pertence, preferências, pedidos e elementos que utiliza.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas. Os membros e as linhas espirituais relevantes devem estar previamente cadastrados.
* **Pós-condições:** O guia espiritual é cadastrado, atualizado ou removido no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Guias Espirituais".
   2.  O sistema exibe a interface de gerenciamento de guias espirituais.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Novo Guia Espiritual:**
         1.  O Ator preenche o nome do guia, seleciona o membro que o incorpora, a linha espiritual, e adiciona informações sobre preferências, pedidos e elementos utilizados.
         2.  O sistema valida os dados inseridos.
         3.  O sistema salva as informações do novo guia espiritual.
      * **Visualizar Guias Espirituais Existentes:**
         1.  O sistema exibe uma lista de todos os guias espirituais cadastrados.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa.
      * **Editar Guia Espiritual Existente:**
         1.  O Ator seleciona um guia espiritual da lista para edição.
         2.  O sistema carrega os dados do guia na interface de edição.
         3.  O Ator modifica os campos desejados.
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações do guia espiritual.
      * **Remover Guia Espiritual Existente:**
         1.  O Ator seleciona um guia espiritual da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove o guia espiritual do registro.
* **Fluxos Alternativos:**
   * **FA3.1: Membro/Linha Espiritual Não Encontrado:**
      1.  No passo 3.1.1 (Cadastrar Guia), se o membro ou a linha espiritual selecionada não for encontrada ou for inválida, o sistema exibe uma mensagem de erro.
      2.  O Ator verifica e corrige a seleção.
* **Regras de Negócio Aplicáveis:** RN02

### 4. CU004: Gerenciar Linhas Espirituais

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova as linhas espirituais (ex: Caboclos, Pretos Velhos) com nome e descrição.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas.
* **Pós-condições:** A linha espiritual é cadastrada, atualizada ou removida no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Linhas Espirituais".
   2.  O sistema exibe a interface de gerenciamento de linhas espirituais.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Nova Linha Espiritual:**
         1.  O Ator preenche o nome e a descrição da linha espiritual.
         2.  O sistema valida os dados inseridos.
         3.  O sistema salva as informações da nova linha espiritual.
      * **Visualizar Linhas Espirituais Existentes:**
         1.  O sistema exibe uma lista de todas as linhas espirituais cadastradas.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa.
      * **Editar Linha Espiritual Existente:**
         1.  O Ator seleciona uma linha espiritual da lista para edição.
         2.  O sistema carrega os dados da linha na interface de edição.
         3.  O Ator modifica os campos desejados.
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações da linha espiritual.
      * **Remover Linha Espiritual Existente:**
         1.  O Ator seleciona uma linha espiritual da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove a linha espiritual do registro.

### 5. CU005: Gerenciar Giras

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova giras. Cada gira deve conter um título, data de início e término, indicações e lista de compras.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas. O Terreiro deve estar cadastrado.
* **Pós-condições:** A gira é cadastrada, atualizada ou removida no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Giras".
   2.  O sistema exibe a interface de gerenciamento de giras.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Nova Gira:**
         1.  O Ator preenche título, data de início, data de término, indicações e lista de compras.
         2.  O sistema valida os dados inseridos.
         3.  O sistema salva as informações da nova gira.
      * **Visualizar Giras Existentes:**
         1.  O sistema exibe uma lista de todas as giras cadastradas.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa para localizar giras específicas.
      * **Editar Gira Existente:**
         1.  O Ator seleciona uma gira da lista para edição.
         2.  O sistema carrega os dados da gira na interface de edição.
         3.  O Ator modifica os campos desejados.
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações da gira.
      * **Remover Gira Existente:**
         1.  O Ator seleciona uma gira da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove a gira do registro.
* **Fluxos Alternativos:**
   * **FA5.1: Campos Obrigatórios Não Preenchidos/Inválidos:**
      1.  No passo 3.1.2 ou 3.3.4 (Cadastrar/Editar Gira), se o Ator não preencher campos obrigatórios ou fornecer dados inválidos, o sistema exibe uma mensagem de erro.
      2.  O Ator corrige os dados e tenta novamente.
* **Regras de Negócio Aplicáveis:** RN03, RN07

### 6. CU006: Registrar Presença em Giras

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite registrar a presença de membros e visitantes em uma gira específica.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas. A gira, os membros e/ou visitantes devem estar previamente cadastrados.
* **Pós-condições:** A presença de membros e/ou visitantes é registrada para a gira. Ao menos um membro ou visitante deve ser marcado como participante para que a gira seja "realizada" no sistema.
* **Fluxo Principal:**
   1.  O Ator seleciona a gira para a qual deseja registrar presenças.
   2.  O sistema exibe a lista de membros e visitantes disponíveis para seleção.
   3.  O Ator seleciona os membros e/ou visitantes presentes.
   4.  O sistema valida que ao menos um participante foi selecionado.
   5.  O sistema registra a presença dos selecionados na gira.
* **Fluxos Alternativos:**
   * **FA6.1: Nenhum Participante Selecionado:**
      1.  No passo 4, se o Ator tentar registrar a presença sem selecionar nenhum membro ou visitante, o sistema exibe uma mensagem de erro.
      2.  O Ator deve selecionar ao menos um participante.
* **Regras de Negócio Aplicáveis:** RN04

### 7. CU007: Gerenciar Mensalidades

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema registre, visualize, edite e remova as mensalidades pagas pelos membros. Cada mensalidade deve conter o valor, data de pagamento e período de referência.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas. O membro associado à mensalidade deve estar cadastrado.
* **Pós-condições:** A mensalidade é registrada, atualizada ou removida no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Mensalidades".
   2.  O sistema exibe a interface de gerenciamento de mensalidades.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Registrar Nova Mensalidade:**
         1.  O Ator seleciona o membro, informa o valor, a data de pagamento e o período de referência (ex: Junho/2025).
         2.  O sistema valida os dados inseridos.
         3.  O sistema salva a nova mensalidade.
      * **Visualizar Mensalidades Existentes:**
         1.  O sistema exibe uma lista de todas as mensalidades registradas.
         2.  O Ator pode utilizar filtros (por membro ou período) ou a barra de pesquisa.
      * **Editar Mensalidade Existente:**
         1.  O Ator seleciona uma mensalidade da lista para edição.
         2.  O sistema carrega os dados da mensalidade na interface de edição.
         3.  O Ator modifica os campos desejados.
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações da mensalidade.
      * **Remover Mensalidade Existente:**
         1.  O Ator seleciona uma mensalidade da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove a mensalidade do registro.
* **Fluxos Alternativos:**
   * **FA7.1: Campos Obrigatórios Não Preenchidos/Inválidos:**
      1.  No passo 3.1.2 ou 3.3.4 (Registrar/Editar Mensalidade), se o Ator não preencher campos obrigatórios ou fornecer dados inválidos, o sistema exibe uma mensagem de erro.
      2.  O Ator corrige os dados e tenta novamente.
* **Regras de Negócio Aplicáveis:** RN05

### 8. CU008: Gerenciar Estoque de Artefatos

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova itens do estoque, e registre movimentos de entrada e saída de artefatos rituais (como velas, ervas e bebidas).
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas.
* **Pós-condições:** O estoque é atualizado. Os movimentos de estoque são registrados.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Estoque".
   2.  O sistema exibe a interface de gerenciamento de estoque.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Novo Item de Estoque:**
         1.  O Ator informa o nome do item, a quantidade inicial e a unidade de medida.
         2.  O sistema valida os dados e salva o novo item no estoque.
      * **Registrar Entrada de Item:**
         1.  O Ator seleciona o item do estoque.
         2.  Informa a quantidade de entrada e a data da entrada.
         3.  O sistema atualiza a quantidade do item no estoque e registra o movimento.
      * **Registrar Saída de Item:**
         1.  O Ator seleciona o item do estoque.
         2.  Informa a quantidade de saída, a data da saída e, opcionalmente, associa a uma gira.
         3.  O sistema verifica a disponibilidade no estoque.
         4.  O sistema atualiza a quantidade do item no estoque e registra o movimento.
      * **Visualizar Estoque Atual:**
         1.  O sistema exibe uma lista de todos os itens em estoque com suas quantidades atuais.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa.
      * **Consultar Histórico de Movimentação:**
         1.  O sistema exibe o histórico detalhado de entradas e saídas por item ou por período.
      * **Editar Item de Estoque:**
         1.  O Ator seleciona um item da lista para edição.
         2.  O sistema carrega os dados do item na interface de edição.
         3.  O Ator modifica os campos desejados (exceto a quantidade atual, que é alterada por movimentos).
         4.  O sistema valida as alterações.
         5.  O sistema atualiza as informações do item.
      * **Remover Item de Estoque:**
         1.  O Ator seleciona um item da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove o item do registro.
* **Fluxos Alternativos:**
   * **FA8.1: Quantidade Insuficiente para Saída:**
      1.  No passo 3.3.3 (Registrar Saída), se a quantidade solicitada for maior que a `quantidade_atual` do item em estoque, o sistema exibe uma mensagem de erro.
      2.  O Ator ajusta a quantidade ou cancela a operação.
* **Regras de Negócio Aplicáveis:** RN06

### 9. CU009: Consultar Agenda e Histórico

* **Ator(es) Principal(is):** Administrador, Secretário(a), Filho de Santo
* **Descrição:** Permite que os atores visualizem o calendário de giras e eventos passados e futuros, e consultem o histórico de atividades da casa. Filhos de Santo podem visualizar suas próprias funções e participações.
* **Pré-condições:** O ator deve estar autenticado no sistema.
* **Pós-condições:** As informações da agenda e do histórico são exibidas ao ator.
* **Fluxo Principal:**
   1.  O Ator seleciona a opção "Agenda" ou "Histórico" no menu principal.
   2.  O sistema exibe o calendário com as giras agendadas e eventos passados.
   3.  O Ator pode utilizar filtros por data, tipo de evento, ou membro (para filhos de santo, filtrar suas próprias participações).
* **Regras de Negócio Aplicáveis:** N/A

### 10. CU010: Gerenciar Orixás

* **Ator(es) Principal(is):** Administrador, Secretário(a)
* **Descrição:** Permite que o sistema cadastre, visualize, edite e remova os orixás que podem ser associados como pai/mãe de cabeça aos membros.
* **Pré-condições:** O ator deve estar autenticado no sistema e possuir as permissões adequadas.
* **Pós-condições:** Orixá cadastrado, atualizado ou removido no sistema.
* **Fluxo Principal:**
   1.  O Ator acessa a funcionalidade de "Gerenciar Orixás".
   2.  O sistema exibe a interface de gerenciamento de orixás.
   3.  O Ator pode escolher uma das seguintes ações:
      * **Cadastrar Novo Orixá:**
         1.  O Ator preenche o nome do orixá.
         2.  O sistema valida os dados e salva o novo orixá.
      * **Visualizar Orixás Existentes:**
         1.  O sistema exibe uma lista de todos os orixás cadastrados.
         2.  O Ator pode utilizar filtros ou a barra de pesquisa.
      * **Editar Orixá Existente:**
         1.  O Ator seleciona um orixá da lista para edição.
         2.  O sistema carrega o nome do orixá na interface de edição.
         3.  O Ator modifica o nome.
         4.  O sistema valida as alterações e atualiza as informações do orixá.
      * **Remover Orixá Existente:**
         1.  O Ator seleciona um orixá da lista para remoção.
         2.  O sistema solicita uma confirmação da remoção.
         3.  O sistema remove o orixá do registro.

### 11. CU011: Gerenciar Dados do Terreiro

* **Ator(es) Principal(is):** Administrador
* **Descrição:** Permite que o Administrador cadastre ou atualize as informações fundamentais do terreiro, como nome, endereço e data de abertura.
* **Pré-condições:** O Administrador deve estar autenticado no sistema e possuir as permissões específicas para esta funcionalidade.
* **Pós-condições:** As informações do Terreiro são atualizadas e persistidas no sistema.
* **Fluxo Principal:**
   1.  O Administrador acessa a opção "Configurações do Terreiro".
   2.  O sistema exibe a interface com os campos editáveis para nome, endereço e data de abertura do terreiro.
   3.  O Administrador preenche ou edita as informações desejadas.
   4.  O sistema valida os dados inseridos.
   5.  O sistema salva as informações atualizadas do terreiro.
* **Fluxos Alternativos:**
   * **FA11.1: Campos Obrigatórios Não Preenchidos/Inválidos:**
      1.  No passo 4, se o Administrador não preencher campos obrigatórios ou fornecer dados inválidos, o sistema exibe uma mensagem de erro.
      2.  O Administrador corrige os dados e tenta novamente.