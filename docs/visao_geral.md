# 📖 Visão Geral do Sistema

## ✨ Nome do Projeto

**Gerenciamento Casa de Axé**
Sistema web voltado para apoiar a gestão administrativa, espiritual e ritualística de uma casa de umbanda.

## 🎯 Objetivo

Facilitar o controle de informações e atividades de um terreiro, oferecendo uma ferramenta digital intuitiva e segura para gestão de:

- Filhos de santo (Membros)
- Guias espirituais, incluindo suas linhas espirituais, preferências e pedidos
- Giras e funções, com registro de presença de membros e visitantes
- Mensalidades e doações
- Artefatos e elementos rituais, com controle de estoque
- Agenda e calendário espiritual, com histórico de eventos
- Dados do próprio Terreiro

## 👥 Atores do Sistema

| Ator           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Administrador  | Pai/Mãe de Santo ou gestor espiritual da casa. Responsável por gerenciar informações do `Terreiro`, agendamento de `Gira`s, cadastro de `Membro`s e `Visitante`s, `GuiaEspiritual`s, `Orixa`s, e `LinhaEspiritual`s, visualização de todas as presenças, e gerenciamento de mensalidades e estoque de artefatos.                                                                                                               |
| Filho de Santo | Membro iniciado que participa das giras. Pode visualizar suas próprias informações de `Membro`, seus `GuiaEspiritual`s e `Orixa`s associados, o histórico de suas `PresencaGiraMembro`, e suas mensalidades.                                                                                                                                                                                                            |
| Secretário(a)  | Auxilia o administrador no gerenciamento dos dados. Responsável pelo cadastro e atualização de `Membro`s, `Visitante`s, registro de `Gira`s e `PresencaGiraMembro`/`PresencaGiraVisitante`, gerenciamento de `GuiaEspiritual`s e `LinhaEspiritual`s, `Orixa`s, e auxílio no controle de mensalidades e estoque.                                                                                                 |
| Visitante      | Pessoa que pode participar de giras, mas sem as responsabilidades de um `Membro`. O sistema registra sua `PresencaGiraVisitante` e observações.                                                                                                                                                                                                                                                                     |

## 📚 Funcionalidades Principais

- Cadastro e gerenciamento de membros (filhos de santo), incluindo data de nascimento, entrada, coroação, pai/mãe de cabeça (Orixás), e associação ao terreiro
- Cadastro e gerenciamento de visitantes, com observações
- Registro de giras com título, datas de início e fim, indicações e listas de compras
- Gestão de entidades espirituais (`GuiaEspiritual`), incluindo nome, membro incorporador, linha espiritual, preferências, pedidos e elementos utilizados
- Gestão de linhas espirituais (`LinhaEspiritual`) com nome e descrição
- Controle de estoque de itens ritualísticos, registrando entradas e saídas de velas, ervas e bebidas
- Registro de mensalidades, incluindo valor, data de pagamento e período de referência
- Agenda com histórico de eventos e participantes (registro de presenças de membros e visitantes em giras)
- Associação entre membros e guias (`MembroGuia`)

## 🔐 Permissões

Cada ator terá acesso restrito às funcionalidades com base em seu papel no sistema.