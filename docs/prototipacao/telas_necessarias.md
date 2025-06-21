# Detalhamento das Telas para Prototipação (MVP Otimizado)

Este documento apresenta a especificação funcional e de design para cada uma das 12 telas essenciais do MVP, aplicando as melhores práticas de UX/UI para uma aplicação mobile de gestão.

### 1. Tela: Login
* **Ator(es) Principal(is):** Administrador, Secretário(a), Filho de Santo.
* **Objetivo da Tela:** Autenticar o usuário de forma segura e direcioná-lo para o ambiente correto de acordo com seu perfil de acesso.
* **Estrutura e Componentes Chave:**
    * **Layout:** Vertical, centralizado, com amplo espaço em branco para foco total.
    * **Componentes:** Logo ou Símbolo da Casa (opcional), campo de texto "Usuário", campo de texto "Senha" (com ícone para alternar visibilidade), e um botão primário "Entrar" (sólido, vermelho, de fácil alcance).
* **Fluxo de Interação Principal:**
    1.  Usuário preenche os campos.
    2.  Toca em "Entrar".
    3.  O sistema valida as credenciais e direciona o usuário para a tela principal correspondente ao seu perfil (Dashboard para Admin/Secretário, Meu Perfil para Filho de Santo).
* **Justificativa de Design (UX):** A interface minimalista reduz a carga cognitiva. O direcionamento pós-login personaliza a experiência, atendendo ao princípio de design focado no ator.

### 2. Tela: Principal (Dashboard)
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Fornecer um ponto de partida rápido e visual para todas as tarefas de gestão do sistema.
* **Estrutura e Componentes Chave:**
    * **Layout:** Lista vertical de botões de navegação para melhor escaneabilidade e escalabilidade.
    * **Componentes:** Título claro ("Painel de Controle"), e botões de navegação para cada módulo principal (`Calendário 🗓️`, `Giras 🥁`, `Comunidade 🔱`, `Gestão 🌿`, `Configurações ⚙️`).
* **Fluxo de Interação Principal:** Usuário toca em um dos botões e navega para a tela do módulo correspondente.
* **Justificativa de Design (UX):** A lista vertical é ideal para mobile, e o uso de ícones e rótulos grandes atende ao princípio de *Reconhecimento em vez de Memorização*. O atalho para "Giras" otimiza um fluxo de trabalho comum.

### 3. Tela: Agenda 🥁
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Centralizar a visualização e o cadastro de todas as giras e eventos.
* **Estrutura e Componentes Chave:**
    * **Layout:** Visão principal com um seletor no topo para alternar entre "Calendário" e "Lista".
    * **Componentes:** Seletor de Visão, Área de Conteúdo (exibindo o calendário ou a lista cronológica), Botão de Ação Flutuante (FAB) `+` para adicionar novas giras.
* **Fluxo de Interação Principal:** Usuário visualiza eventos, alterna as visões, toca em uma gira para ver detalhes, ou toca no FAB para cadastrar uma nova.
* **Justificativa de Design (UX):** Consolida duas funcionalidades (`CU005` e `CU009`) em uma única tela, dando flexibilidade ao usuário e simplificando a arquitetura da informação.

### 4. Tela: Detalhes da Gira
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Apresentar todas as informações de uma gira de forma clara e servir como ponto de partida para ações contextuais.
* **Estrutura e Componentes Chave:** Título da Gira, seções com subtítulos ("Data e Hora", "Indicações", "Lista de Compras"), e um botão de ação principal "Registrar Presença".
* **Fluxo de Interação Principal:** Usuário analisa as informações e pode tocar em "Registrar Presença" para navegar até a tela de registro.
* **Justificativa de Design (UX):** A hierarquia visual clara torna a informação fácil de consumir, e o botão de ação contextual otimiza o fluxo da tarefa.

### 5. Tela: Registro de Presença
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Permitir a marcação rápida dos participantes de uma gira.
* **Estrutura e Componentes Chave:** Título da Gira, lista de nomes (membros e visitantes) com um checkbox ao lado de cada um, e um botão "Salvar Presenças" fixo na parte inferior.
* **Fluxo de Interação Principal:** Usuário marca os checkboxes dos presentes e toca em "Salvar".
* **Justificativa de Design (UX):** Um design de checklist é a forma mais eficiente e universalmente compreendida para tarefas de seleção múltipla.

### 6. Tela: Comunidade 🔱
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Gerenciar de forma centralizada todos os perfis de pessoas e entidades espirituais.
* **Estrutura e Componentes Chave:** Navegação por abas ("Membros", "Visitantes", "Guias Espirituais"), uma lista de cards correspondente à aba ativa, e um FAB `+` para adicionar novos registros.
* **Fluxo de Interação Principal:** Usuário seleciona uma aba, a lista é atualizada, e ele pode tocar em um item para ver detalhes ou no FAB para cadastrar.
* **Justificativa de Design (UX):** A consolidação em abas reduz o número de telas principais e cria um modelo mental consistente para a gestão de diferentes entidades.

### 7. Tela: Detalhes do Membro
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Apresentar um "dossiê" completo com todas as informações de um membro.
* **Estrutura e Componentes Chave:** Card de destaque com nome e foto, e seções de informações em cards separados ("Dados Pessoais", "Histórico na Casa", "Guias Associados"). Um botão "Editar" fica no topo.
* **Fluxo de Interação Principal:** Usuário consulta as informações e pode tocar em "Editar" para navegar para a tela de cadastro.
* **Justificativa de Design (UX):** Apresenta uma grande quantidade de informação de forma organizada e escaneável.

### 8. Tela: Cadastro/Edição de Membro/Guia
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Guiar o usuário na entrada de dados complexos de forma estruturada, prevenindo erros.
* **Estrutura e Componentes Chave:** Formulário de coluna única com seções lógicas. Implementa a lógica visual da regra `RN09` (campos desabilitados). Botões de ação "Salvar" e "Cancelar" fixos na parte inferior.
* **Fluxo de Interação Principal:** Usuário preenche os campos, o sistema valida os dados ao salvar, e retorna à tela anterior com uma mensagem de sucesso ou erro.
* **Justificativa de Design (UX):** Uma tela dedicada para formulários complexos evita a desordem. A lógica condicional é uma aplicação direta do princípio de *Prevenção de Erros*.

### 9. Tela: Gestão do Terreiro 🌿
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Unificar o controle de recursos financeiros (mensalidades) e materiais (estoque).
* **Estrutura e Componentes Chave:** Navegação por abas ("Mensalidades", "Estoque") e uma lista de registros correspondente à aba ativa. Um botão `+` permite adicionar novos registros.
* **Fluxo de Interação Principal:** Usuário seleciona uma aba, visualiza a lista, e pode tocar em um item para ver detalhes ou no `+` para adicionar um novo.
* **Justificativa de Design (UX):** Agrupa tarefas de gestão de recursos, criando um fluxo lógico para o administrador.

### 10. Tela: Detalhes do Item de Estoque
* **Ator(es) Principal(is):** Administrador, Secretário(a).
* **Objetivo da Tela:** Otimizar o fluxo de atualização de quantidade de um item de estoque.
* **Estrutura e Componentes Chave:** Card de status com nome e quantidade, botões de ação proeminentes ("+ Registrar Entrada", "- Registrar Saída"), e uma lista com o histórico de movimentações.
* **Fluxo de Interação Principal:** Usuário visualiza o status, toca em um dos botões de ação (que abre um modal para inserir a quantidade), e a lista de histórico é atualizada.
* **Justificativa de Design (UX):** Design orientado à tarefa que torna a ação mais comum extremamente rápida e contextual.

### 11. Tela: Configurações
* **Ator(es) Principal(is):** Administrador, Secretário(a) (parcial).
* **Objetivo da Tela:** Agrupar cadastros de suporte que são raramente modificados.
* **Estrutura e Componentes Chave:** Lista de navegação vertical simples ("Orixás", "Linhas Espirituais", "Dados do Terreiro").
* **Fluxo de Interação Principal:** Tocar em um item da lista abre um **modal** sobre a tela atual para edição rápida, sem sair do contexto.
* **Justificativa de Design (UX):** O uso de modais para CRUDs simples é uma prática mobile-first que acelera o fluxo de trabalho.

### 12. Tela: "Meu Perfil"
* **Ator(es) Principal(is):** Filho de Santo.
* **Objetivo da Tela:** Apresentar um resumo claro e pessoal de todas as informações relevantes para o membro.
* **Estrutura e Componentes Chave:** Dashboard pessoal com abas ("Meus Dados", "Meus Guias", "Minhas Giras", "Minhas Contribuições"). Todo o conteúdo é **apenas de leitura**.
* **Fluxo de Interação Principal:** Usuário faz login e aterrissa diretamente nesta tela, podendo navegar entre as abas para consultar suas informações.
* **Justificativa de Design (UX):** Design focado no ator que remove toda a complexidade desnecessária e oferece uma experiência de consulta limpa, como definido pelo `RF012`.