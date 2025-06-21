# 📋 Requisitos Não Funcionais (RNF)

Este documento descreve os critérios de qualidade para o sistema "Gerenciamento Casa de Axé", focando em como o sistema deve operar, e não no que ele faz.

---

## 🔹 Qualidades de Desempenho

### RNF001: Desempenho
* **Descrição:** O sistema deve apresentar um tempo de resposta rápido para as interações do usuário e carregamento de dados.
* **Critério de Aceitação:**
  * 90% das operações (CRUD e consultas simples) devem ser concluídas em até 3 segundos.
  * Consultas e carregamento de listas com até 1000 registros devem ser finalizadas em menos de 2 segundos.

---

## 🔹 Qualidades de Usabilidade

### RNF002: Usabilidade
* **Descrição:** A interface do usuário deve ser intuitiva e de fácil navegação para todos os perfis de usuários.
* **Critério de Aceitação:**
  * A interface deve ser clara e consistente.
  * O sistema deve fornecer mensagens de erro claras e informativas ao usuário.
  * Feedback visual para ações (ex: indicadores de carregamento, mensagens de sucesso/erro) deve ser fornecido.

---

## 🔹 Qualidades de Segurança

### RNF003: Segurança
* **Descrição:** O sistema deve proteger os dados e garantir que apenas usuários autorizados tenham acesso às funcionalidades e informações.
* **Critério de Aceitação:**
  * Os dados sensíveis (pessoais, espirituais, financeiros) devem ser protegidos contra acesso não autorizado.
  * As senhas dos usuários devem ser armazenadas de forma criptografada e não recuperável.
  * O controle de acesso baseado em papéis (RBAC) deve ser rigorosamente implementado.
  * Todas as comunicações entre o cliente e o servidor (frontend e backend) devem ser criptografadas via HTTPS.

---

## 🔹 Qualidades de Confiabilidade

### RNF004: Confiabilidade
* **Descrição:** O sistema deve ser estável, robusto e garantir a integridade dos dados.
* **Critério de Aceitação:**
  * Minimizar o tempo de inatividade inesperado (alta disponibilidade).
  * Tratamento adequado de exceções para evitar falhas ou travamentos do sistema.
  * Garantia da integridade dos dados durante todas as operações de persistência (criação, leitura, atualização e exclusão).

---

## 🔹 Qualidades de Escalabilidade e Manutenibilidade

### RNF005: Escalabilidade
* **Descrição:** O sistema deve ser capaz de lidar com um aumento de usuários e volume de dados no futuro sem degradação significativa de desempenho.
* **Critério de Aceitação:**
  * A arquitetura deve permitir a adição de mais recursos de hardware (vertical) ou instâncias (horizontal) para suportar crescimento.
  * A base de dados (MySQL) deve ser capaz de gerenciar um grande volume de registros de forma eficiente.

### RNF006: Manutenibilidade
* **Descrição:** O código-fonte e a documentação do sistema devem ser fáceis de entender, modificar e estender.
* **Critério de Aceitação:**
  * O código deve seguir boas práticas de programação, ser modular e bem comentado.
  * A documentação técnica (incluindo diagramas PlantUML/Draw.io e estes requisitos) deve ser clara e mantida atualizada.

---

## 🔹 Qualidades de Portabilidade e Compatibilidade

### RNF007: Portabilidade
* **Descrição:** O backend do sistema deve ser capaz de ser implantado em diferentes ambientes de servidor que suportem as tecnologias definidas.
* **Critério de Aceitação:**
  * A aplicação Spring Boot deve ser executável em sistemas operacionais comuns (Linux, Windows, macOS) e em ambientes de nuvem.

### RNF008: Compatibilidade
* **Descrição:** A interface web do sistema deve ser compatível com os principais navegadores modernos.
* **Critério de Aceitação:**
  * Funcionalidade e apresentação consistentes em Chrome (últimas 2 versões), Firefox (últimas 2 versões), Edge (últimas 2 versões) e Safari (últimas 2 versões).