# Caso de Uso UC01 – Cadastrar Filho de Santo

## 1. Identificação

**ID:** UC01  
**Nome:** Cadastrar Filho de Santo  
**Ator Principal:** Administrador  
**Resumo:** Permite o cadastro de um novo filho de santo no sistema, com dados pessoais, dados espirituais, datas importantes e vínculo com guias.

---

## 2. Descrição

O administrador do sistema pode cadastrar um novo filho de santo informando seus dados básicos (nome, telefone, idade), além de informações específicas como cargo, data de entrada, data de coroação e guia espiritual. O campo de orixás de cabeça só pode ser preenchido após a coroação, conforme regra RN09.

---

## 3. Pré-condições

- O administrador deve estar autenticado no sistema.
- O terreiro já deve estar cadastrado.
- Não pode haver outro cadastro com o mesmo nome e data de entrada.

---

## 4. Pós-condições

- Um novo filho de santo é registrado no sistema e passa a constar na lista de membros da casa.
- A ficha pode ser atualizada posteriormente com informações adicionais, como os orixás de cabeça (após a coroação).

---

## 5. Fluxo Principal

1. O ator acessa o menu **“Filhos de Santo”**.
2. Clica em **“Novo Cadastro”**.
3. O sistema exibe um formulário com os seguintes campos:
   - Nome completo
   - Telefone (opcional)
   - Data de nascimento
   - Cargo
   - Data de entrada no terreiro
   - Data da coroação (opcional inicialmente)
   - Data da obrigação de Oxalá (opcional)
   - Lista de guias associados (opcional)
   - Pai/Mãe de cabeça (guia principal) (opcional)
4. O ator preenche os campos obrigatórios e opcionalmente informa a data da coroação.
5. Após preencher **data de nascimento**, o sistema exibe a idade atual ao lado do campo. 
6. Se a **data da coroação for informada**, o sistema habilita o campo:
   - Orixás de cabeça (múltipla escolha)
7. O ator clica em **“Salvar”**.
8. O sistema valida os dados e salva o novo filho de santo.

---

## 6. Fluxos Alternativos

### A1 – Dados incompletos ou inválidos
- O sistema exibe mensagem de erro e destaca os campos obrigatórios não preenchidos.


---

## 7. Regras de Negócio

- **RN01** – Todo filho de santo deve ter nome, data de entrada e cargo.
- **RN02** – Pode ter múltiplos guias associados.
- **RN09** – Os orixás de cabeça só podem ser cadastrados após a data de coroação estar definida.

---

## 8. Exceções

- **E01 – Erro de conexão com banco de dados:**  
  O sistema exibe mensagem de falha e permite tentar novamente ou salvar rascunho.

---

## 9. Requisitos Funcionais Relacionados

- RF01 – O sistema deve permitir o cadastro completo de filhos de santo.
- RF02 – O sistema deve associar guias aos filhos de santo.
- RF03 – O sistema deve bloquear o preenchimento dos orixás de cabeça sem data de coroação.

---

## 10. Mockup/Tela (opcional)

> Adicionar um esboço da tela de cadastro do filho de santo, com o campo de orixás desabilitado até a data de coroação ser preenchida.

---

## 11. Histórico de Revisões

| Data       | Autor                      | Alteração                                 |
|------------|----------------------------|--------------------------------------------|
| 20/06/2025 | Wanderson Almeida de Mello | Criação do caso de uso com regra RN09      |
