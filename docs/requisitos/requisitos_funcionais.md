# 📝 Requisitos Funcionais (RF)

Este documento detalha as funcionalidades que o sistema "Gerenciamento Casa de Axé" deve oferecer aos seus usuários, com base nos casos de uso e regras de negócio definidos.

---

## 🔹 Módulo de Gerenciamento de Pessoas

### RF001: Gerenciar Membros (Filhos de Santo)
* **Descrição:** O sistema deve permitir o cadastro, visualização, edição e remoção (CRUD) de informações de membros da casa (filhos de santo).
* **Detalhes:**
    * Permitir cadastro de membros com nome, telefone, data de nascimento, data de entrada na casa, e data de coroação.
    * Os campos para 'pai de cabeça' e 'mãe de cabeça' (Orixás) devem ser desabilitados e só podem ser preenchidos ou editados após a `data de coroacao` do membro estar informada.
    * Exibir lista de membros com opções de filtro e pesquisa.
    * Permitir edição e remoção de membros existentes.
    * Validar o preenchimento de campos obrigatórios.

### RF002: Gerenciar Visitantes
* **Descrição:** O sistema deve permitir o CRUD de informações de visitantes da casa.
* **Detalhes:**
    * Permitir cadastro de visitantes com nome, telefone e observações.
    * Exibir lista de visitantes com opções de filtro e pesquisa.
    * Permitir edição e remoção de visitantes existentes.
    * Validar o preenchimento de campos obrigatórios.

---

## 🔹 Módulo de Gerenciamento de Entidades Espirituais

### RF003: Gerenciar Guias Espirituais
* **Descrição:** O sistema deve permitir o CRUD de guias espirituais, associando-os a membros e linhas espirituais.
* **Detalhes:**
    * Cadastro de guias com nome, associação a um membro que o incorpora, a qual linha espiritual pertence, preferências, pedidos e elementos que utiliza.
    * Validar que o membro e a linha espiritual associados sejam válidos e previamente cadastrados.
    * Exibir lista de guias espirituais com filtros e pesquisa.
    * Permitir edição e remoção de guias.

### RF004: Gerenciar Linhas Espirituais
* **Descrição:** O sistema deve permitir o CRUD de linhas espirituais (ex: Caboclos, Pretos Velhos).
* **Detalhes:**
    * Cadastro de linhas espirituais com nome e descrição.
    * Exibir lista de linhas espirituais com filtros e pesquisa.
    * Permitir edição e remoção de linhas.

### RF005: Gerenciar Orixás
* **Descrição:** O sistema deve permitir o CRUD dos orixás que podem ser associados como pai/mãe de cabeça aos membros.
* **Detalhes:**
    * Cadastro de orixás apenas com o nome.
    * Exibir lista de orixás com filtros e pesquisa.
    * Permitir edição e remoção de orixás.

---

## 🔹 Módulo de Gerenciamento de Giras e Eventos

### RF006: Gerenciar Giras
* **Descrição:** O sistema deve permitir o CRUD de giras, incluindo detalhes de agendamento e planejamento.
* **Detalhes:**
    * Cadastro de giras com título, data/hora de início e término, indicações e lista de compras.
    * Uma gira só pode ser cadastrada se tiver indicações ou lista de compras.
    * Exibir lista de giras com filtros e pesquisa.
    * Permitir edição e remoção de giras.
    * Validar o preenchimento de campos obrigatórios.

### RF007: Registrar Presença em Giras
* **Descrição:** O sistema deve permitir o registro da presença de membros e visitantes em uma gira específica.
* **Detalhes:**
    * Permitir selecionar membros e/ou visitantes presentes para uma gira.
    * Para uma gira ser considerada "realizada" no sistema, ao menos um membro ou visitante precisa ser marcado como participante.

### RF008: Consultar Agenda e Histórico
* **Descrição:** O sistema deve exibir um calendário de giras e eventos (agendados e passados), e permitir a consulta do histórico de atividades da casa.
* **Detalhes:**
    * Visualização de calendário com giras agendadas e eventos passados.
    * Filtros por data, tipo de evento, e por membro (Filhos de Santo devem poder visualizar apenas suas próprias participações).

---

## 🔹 Módulo Financeiro e de Estoque

### RF009: Gerenciar Mensalidades
* **Descrição:** O sistema deve permitir o CRUD de mensalidades pagas pelos membros.
* **Detalhes:**
    * Registro de mensalidades contendo valor, data de pagamento e período de referência (ex: Junho/2025), associada a um membro.
    * Exibir lista de mensalidades com filtros por membro ou período e pesquisa.
    * Permitir edição e remoção de mensalidades.
    * Validar o preenchimento de campos obrigatórios.

### RF010: Gerenciar Estoque de Artefatos
* **Descrição:** O sistema deve permitir o CRUD de itens do estoque e o registro de suas movimentações (entradas e saídas).
* **Detalhes:**
    * Cadastro de novos itens com nome, quantidade inicial e unidade de medida (ex: velas, ervas, bebidas).
    * Registro de entradas de itens (quantidade, data).
    * Registro de saídas de itens (quantidade, data, e associação opcional a uma gira).
    * Não permitir que a quantidade de saída seja maior que a quantidade atual em estoque.
    * Visualização do estoque atual e consulta do histórico detalhado de movimentações.
    * Permitir edição (exceto quantidade atual) e remoção de itens.

---

## 🔹 Módulo de Administração do Terreiro

### RF011: Gerenciar Dados do Terreiro
* **Descrição:** O sistema deve permitir ao Administrador cadastrar ou atualizar as informações fundamentais do terreiro.
* **Detalhes:**
    * Cadastro/atualização de nome, endereço e data de abertura do terreiro.
    * Validar o preenchimento de campos obrigatórios.

---

## 🔹 Requisito de Acesso e Segurança

### RF012: Autenticação e Autorização por Perfil
* **Descrição:** O sistema deve gerenciar o acesso dos usuários com base em seus perfis (Administrador, Filho de Santo, Secretário(a)).
* **Detalhes:**
    * Sistema de login com credenciais válidas.
    * **Administrador:** Acesso total a todas as funcionalidades.
    * **Secretário(a):** Acesso completo às funcionalidades de gerenciamento de membros, visitantes, guias, linhas, giras, presenças, mensalidades, estoque e orixás. Não deve ter acesso ao gerenciamento dos dados do Terreiro.
    * **Filho de Santo:** Acesso apenas para visualizar suas próprias informações de membro, seus guias espirituais, seus orixás associados, seu histórico de presenças em giras e suas mensalidades.