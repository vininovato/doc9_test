# 📊 Tabela: `solicitacoes_audiencias_logistica`

## 🧾 Descrição Geral

Esta tabela contém registros estruturados de **solicitações de audiências logísticas** realizadas por clientes da Doc9. Cada linha representa uma solicitação feita para que um profissional (advogado ou preposto) compareça a uma audiência jurídica em nome do cliente.

A Doc9 é responsável por organizar e executar a logística de presença em audiências em **todo o território nacional**, atuando com uma rede de parceiros que são acionados conforme local, data, tipo de audiência e especialidade necessária.

Os dados utilizados neste teste correspondem a um período fictício de **junho a dezembro de 2024**, com nomes de clientes e parceiros **anonimizados**. As demais informações representam um cenário realista adaptado para fins analíticos.

---

## 📁 Colunas e Descrições

| Coluna                          | Tipo        | Descrição                                                                                          |
| ------------------------------- | ----------- | -------------------------------------------------------------------------------------------------- |
| `id_solicitacao`                | `bigint`    | Identificador único da solicitação                                                                 |
| `nome_parceiro`                 | `text`      | Nome ou código do parceiro responsável por comparecer à audiência                                  |
| `nome_cliente`                  | `text`      | Nome ou código do cliente solicitante                                                              |
| `datahora_abertura_solicitacao` | `timestamp` | Data e hora em que a solicitação foi criada                                                        |
| `datahora_audiencia`            | `timestamp` | Data e hora agendada para a realização da audiência                                                |
| `prazo_para_inserir_dados`      | `timestamp` | Prazo máximo para que o parceiro forneça os dados necessários                                      |
| `data_envio`                    | `timestamp` | Data em que a solciitação foi enviada (realizada e concluída)                                      |
| `tipo`                          | `text`      | Tipo de solicitação (Audiência = sessão presencial, Teleaudiência = sessão Remota)                 |                        |
| `tipo_demanda`                  | `text`      | Perfil do profissional necessário: advogado, preposto ou ambos (combo)                             |
| `area_processo`                 | `text`      | Área jurídica do processo (ex: cível, trabalhista, tributária)                                     |
| `tipo_audiencia`                | `text`      | Tipo da audiência (ex: inicial, UNA, instrução)                                                    |
| `situacao`                      | `text`      | Situação atual da solicitação (ex: pendente, concluída, cancelada)                                 |
| `orgao`                         | `text`      | Nome do órgão judicial responsável por conduzir a audiência                                        |
| `comarca`                       | `text`      | Cidade ou jurisdição da audiência                                                                  |
| `uf_comarca`                    | `text`      | Unidade federativa da comarca (ex: SP, RJ, RS)                                                     |
| `situacao_dados`                | `text`      | Indica se os dados foram enviados dentro do prazo estabelecido (ex: "dentro do prazo", "atrasado") |
| `orientacoes_inseridas_cliente` | `text`      | Informa se as orientações foram inseridas com antecedência inferior a 24h                          |
| `qtd_troca`                     | `integer`   | Número de vezes que houve substituição do parceiro inicialmente alocado                            |
| `qtd_declinio`                  | `integer`   | Quantidade de vezes que parceiros recusaram o aceite da audiência                                  |
| `houve_revelia`                 | `integer`   | Indica se houve revelia (parceiro **não compareceu** e não houve tempo hábil para substituição)    |
| `houve_ausencia`                | `integer`   | Indica ausência do parceiro originalmente alocado (mas houve substituição a tempo)                 |
| `houve_ma_atuacao`              | `integer`   | Indica se houve avaliação negativa sobre a atuação do parceiro                                     |

---

## 📚 Glossário de Termos

| Termo                     | Significado                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------------------- |
| **Solicitação**           | Pedido feito por um cliente para que a Doc9 organize a presença de um profissional em uma audiência |
| **Parceiro**              | Profissional terceirizado (advogado ou preposto) acionado pela Doc9 para ir à audiência             |
| **Cliente**               | Empresa contratante da Doc9 que precisa de representação jurídica                                   |
| **Audiência**             | Reunião formal no processo jurídico, realizada em um fórum, tribunal ou órgão judicial              |
| **Comarca**               | Cidade ou região jurisdicional onde ocorre a audiência                                              |
| **Preposto**              | Representante da empresa que não é advogado (ex: gerente, supervisor), com autorização legal        |
| **Revelia**               | Quando a parte convocada não comparece à audiência **sem justificativa ou substituição**            |
| **Troca de audiencista**  | Substituição do parceiro que inicialmente aceitou a solicitação                                     |
| **Declínio**              | Recusa formal do parceiro ao ser convidado para a audiência                                         |
| **Orientações inseridas** | Informações que o cliente adiciona para orientar o parceiro, como contexto ou documentos            |
| **Área do processo**      | Categoria jurídica do caso, como trabalhista ou cível                                               |
| **Tipo de audiência**     | Fase ou natureza da audiência (ex: inicial, de conciliação, de instrução)                           |
