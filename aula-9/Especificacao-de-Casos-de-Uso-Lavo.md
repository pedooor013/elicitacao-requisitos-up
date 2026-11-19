# Especificação de Casos de Uso: Lavo

**Autor:** **Versão:** 1.0 **Data:**

## 1. Visão geral

**Descrição do sistema:**

Sistema para controle de uma lavanderia, onde o cliente realiza o pedido via APP

**Diagrama de casos de uso:**

![Diagrama de casos de uso da Lavo](diagrama-lavo.png)

## 2. Atores

| Ator | Descrição | Casos de uso em que participa |
|---|---|---|
| Cliente | Quem realiza o pedido | Realizar o pedido e o pagamento |
| Atendente | Quem atende o cliente e faz a gestão da coleta | Confirmar área de coleta, cobrar pagamento e sinalizar finalização da higienização |
| Entregador | Quem realiza a coleta e a entrega | Realizar a coleta, e conferir se as roupas são realmente do cliente |

## 3. Lista de casos de uso

| ID | Nome | Ator principal | Prioridade |
|---|---|---|---|
| UC01 | Realizar pedido | Cliente | Alta |
| UC02 | Confirmar área de coleta | Atendente | Alta |
| UC03 | Realizar coleta | Entregador | Alta |
| UC04 | Realizar cobrança de pagamento | Atendente | Alta |
| UC05 | Realizar pagamento | Cliente | Alta |
| UC06 | Confirmar roupas do cliente | Entregador | Alta |
| UC07 | Sinalizar finalização da higienização | Atendente | Alta |

## 4. Especificação de cada caso de uso

### UC01: Realizar pedido

| Campo | Descrição |
|---|---|
| **ID** | UC01 |
| **Nome** | Realizar pedido |
| **Objetivo** | Deseja realizar o pedido para lavagem das roupas |
| **Ator principal** | Cliente |
| **Gatilho** | Cliente acessa o app e inicia um novo pedido |
| **Pré-condições** | Cliente cadastrado no app |
| **Pós-condições** | Pedido realizado |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Acessa o app e inicia um novo pedido | Exibe o formulário de pedido |
| 2 | Informa o endereço de coleta e os dados do pedido | Valida os dados informados |
| 3 | Confirma o pedido | Registra o pedido como realizado e o encaminha ao Atendente |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Observações:**

---

### UC02: Confirmar área de coleta

| Campo | Descrição |
|---|---|
| **ID** | UC02 |
| **Nome** | Confirmar área de coleta |
| **Objetivo** | Confirmar se o pedido pode ser atendido |
| **Ator principal** | Atendente |
| **Atores secundários** | |
| **Gatilho** | Cliente realizar o pedido |
| **Pré-condições** | O cliente ter realizado o pedido |
| **Pós-condições** | Coleta confirmada |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Seleciona o pedido recém-realizado | Exibe os dados do pedido e o endereço de coleta |
| 2 | Verifica se o endereço está na área de atendimento e confirma a coleta | Valida a confirmação |
| 3 | — | Registra a coleta como confirmada e a libera para o Entregador |

**Fluxos alternativos**

| ID | Passo de origem | Condição | O que acontece |
|---|---|---|---|
| FA1 | | | |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Regras de negócio relacionadas**

| ID | Regra |
|---|---|
| RN01 | |

**Observações:**

---

### UC03: Realizar coleta

| Campo | Descrição |
|---|---|
| **ID** | UC03 |
| **Nome** | Realizar coleta |
| **Objetivo** | Realizar a coleta das roupas que devem ser lavadas |
| **Ator principal** | Entregador |
| **Atores secundários** | |
| **Gatilho** | Entregador inicia a coleta no endereço do cliente |
| **Pré-condições** | Coleta confirmada pelo Atendente (UC02) |
| **Pós-condições** | Coleta realizada |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Visualiza o pedido com coleta confirmada | Exibe o endereço e os dados do pedido |
| 2 | Recolhe as roupas no endereço do cliente e registra a coleta | Valida o registro |
| 3 | — | Registra a coleta como realizada |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Observações:**

---

### UC04: Realizar cobrança de pagamento

| Campo | Descrição |
|---|---|
| **ID** | UC04 |
| **Nome** | Realizar cobrança de pagamento |
| **Objetivo** | Cobrar do cliente o pagamento do serviço |
| **Ator principal** | Atendente |
| **Atores secundários** | |
| **Gatilho** | Atendente inicia a cobrança do pedido |
| **Pré-condições** | Higienização finalizada e sinalizada pelo Atendente (UC07) |
| **Pós-condições** | Pagamento realizado |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Seleciona o pedido com a higienização finalizada | Exibe o valor do serviço |
| 2 | Cobra o pagamento do cliente e registra o recebimento | Valida o registro |
| 3 | — | Registra o pagamento como realizado |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Observações:**

---

### UC05: Realizar pagamento

| Campo | Descrição |
|---|---|
| **ID** | UC05 |
| **Nome** | Realizar pagamento |
| **Objetivo** | Pagar o serviço de higienização das roupas |
| **Ator principal** | Cliente |
| **Atores secundários** | |
| **Gatilho** | Cliente escolhe pagar o pedido pelo app |
| **Pré-condições** | Higienização finalizada e sinalizada pelo Atendente (UC07) |
| **Pós-condições** | Pagamento realizado |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Seleciona pagar o pedido pelo app | Exibe o valor do serviço e as formas de pagamento |
| 2 | Escolhe a forma de pagamento e confirma | Processa o pagamento |
| 3 | — | Registra o pagamento como realizado e informa o cliente |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Observações:**

---

### UC06: Confirmar roupas do cliente

| Campo | Descrição |
|---|---|
| **ID** | UC06 |
| **Nome** | Confirmar roupas do cliente |
| **Objetivo** | Não entregar as roupas erradas para o cliente |
| **Ator principal** | Entregador |
| **Atores secundários** | |
| **Gatilho** | Entregador chega ao endereço do cliente para entregar as roupas |
| **Pré-condições** | O pagamento ter sido realizado |
| **Pós-condições** | Entrega realizada |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Chega ao endereço e seleciona o pedido | Exibe os dados do pedido e do cliente |
| 2 | Confere se as roupas são do cliente correto e confirma | Valida a confirmação |
| 3 | — | Registra a entrega como realizada |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | | | |

**Observações:**

---

### UC07: Sinalizar finalização da higienização

| Campo | Descrição |
|---|---|
| **ID** | UC07 |
| **Nome** | Sinalizar finalização da higienização |
| **Objetivo** | Informar ao sistema que a higienização das roupas do pedido foi finalizada (lavadas, secas e dobradas) |
| **Ator principal** | Atendente |
| **Atores secundários** | Nenhum |
| **Gatilho** | Atendente é avisado de que as roupas do pedido estão prontas e abre o pedido no sistema |
| **Pré-condições** | Coleta realizada (UC03); roupas lavadas, secas e dobradas fisicamente |
| **Pós-condições** | Higienização do pedido registrada como finalizada, liberando a cobrança e o pagamento (UC04 e UC05) |
| **Prioridade** | Alta |

**Fluxo principal**

| Passo | Ator | Sistema |
|---|---|---|
| 1 | Atendente seleciona o pedido cujas roupas ficaram prontas | Exibe os dados e a situação atual do pedido |
| 2 | Atendente sinaliza que a higienização foi finalizada | Verifica que a coleta do pedido foi realizada |
| 3 | — | Registra a higienização como finalizada e libera o pedido para cobrança e pagamento |

**Fluxos de exceção**

| ID | Passo de origem | Erro / situação | Tratamento |
|---|---|---|---|
| FE1 | 2 | Pedido sem coleta registrada | Bloqueia a sinalização e informa que a coleta ainda não foi realizada |

**Regras de negócio relacionadas**

| ID | Regra |
|---|---|
| RN01 | As roupas só são liberadas para dobra quando estiverem 100% limpas; a higienização só é sinalizada como finalizada depois da dobra |

**Observações:**
