# 📘 Modelo Conceitual do Banco de Dados
**Projeto:** Gerenciamento Casa de Axé

---

## 🔹 Entidades e Atributos

### 🔸 Terreiro
- **id** – Identificador único
- **nome**
- **endereço**
- **data de abertura**

---

### 🔸 Pessoa (abstrata)
- **id**
- **nome**
- *telefone* (opcional)

#### Especializações de Pessoa:

##### 🔸 Membro (especialização de Pessoa)
- **data de nascimento**
- **data de entrada no terreiro**
- *data de coroacao* (opcional)
- **[FK] terreiro_id** → Terreiro
- *pai_de_cabeca* → Orixá (após a coroação)
- *mae_de_cabeca* → Orixá (após a coroação)

##### 🔸 Visitante (especialização de Pessoa)
- *observações* (opcional)

---

### 🔸 Orixá
- **id**
- **nome**

---

### 🔸 Guia Espiritual
- **id**
- **nome**
- **[FK] membro_id** → Membro
- **[FK] linha_id** → Linha Espiritual
- *preferências* (opcional)
- *pedidos* (opcional)
- *elementos que utiliza* (opcional)

---

### 🔸 Linha Espiritual
- **id**
- **nome**  
  Ex: Preto-Velho, Caboclo, Erê, Baiano, Boiadeiro, Cigano, Marinheiro, Exu-Mirim, Exu, Pombagira, Malandro
- *descrição* (opcional)

---

### 🔸 Gira
- **id**
- **título**
- **data/hora de início**
- *data/hora de fim* (opcional)
- *indicações* (opcional)
- *lista de compras* (opcional)
- **[FK] terreiro_id** → Terreiro

---

## 🔹 Entidades Relacionais e Relacionamentos

### 🔸 Presença de Membro na Gira

**PresencaGiraMembro**
- **membro_id** → Membro
- **gira_id** → Gira

> Registra quais membros participaram de cada gira.

---

### 🔸 Presença de Visitante na Gira

**PresencaGiraVisitante**
- **visitante_id** → Visitante
- **gira_id** → Gira

> Registra a presença de visitantes em giras.

---

### 🔸 Membro ⇄ Guia Espiritual

**MembroGuia**
- **membro_id** → Membro
- **guia_id** → Guia Espiritual

> Relaciona membros aos guias espirituais que trabalham com eles.

---

## 👉 Regras de Negócio Importantes

- Um membro só pode ter orixás (pai/mãe de cabeça) após a **data de coroação**.
- Um guia pertence a apenas um membro e a uma linha espiritual.
- Um visitante pode existir sem estar vinculado a um terreiro.
- A entidade Pessoa não é instanciada diretamente; serve apenas para generalização.

---