# Priorização de Histórias de Usuário

---

## 01) Prioridade Máxima

**História de usuário original:**
> "O restaurante precisa avisar quando um item do cardápio fica indisponível."

**História ajustada para o padrão INVEST:**
> "Como restaurante, quero poder alterar o status de algum item do cardápio para indisponível."

**Critérios de Aceitação:**

1. Dado que os ingredientes de um certo prato acabaram, quando o cliente estiver escolhendo o seu pedido, então o status do prato deve ser atualizado para indisponível.
2. Dado que o cliente já tinha adicionado o pedido ao carrinho, quando o restaurante mudar o status do prato para inativo, então, ao clicar em finalizar pedido, deve ser exibido um modal informando que o prato escolhido está indisponível.
3. Dado que o restaurante já tinha aceitado o pedido, quando os ingredientes acabarem, então o cliente deve ser notificado para escolher outro produto do restaurante de mesmo valor ou solicitar reembolso.

**Ordenação MoSCoW:**

Essa funcionalidade deve ser um **MUST**, pois assim o entregador terá um apoio maior e conseguirá finalizar a entrega do pedido; esse ponto facilitará muito a vida de clientes e entregadores.

---

## 02) Prioridade Alta

**História de usuário original:**
> "O entregador precisa reportar um problema durante a entrega."

**História ajustada para o padrão INVEST:**
> "Como entregador, quero que, quando eu tiver algum problema no trajeto ou na hora de realizar a entrega, eu possa reportar isso ao cliente e/ou ao suporte."

**Critérios de Aceitação:**

1. Dado que o entregador não localizou o cliente, quando chegar ao ponto de encontro definido, então o entregador deve poder entrar em contato com o suporte para decidir o que deve ser feito.
2. Dado que o entregador sofreu um acidente, quando estiver realizando a entrega, então ele deve poder avisar o cliente sobre o atraso ou, a depender do acidente, solicitar a troca de entregadores para o pedido que está sendo transportado.
3. Dado que o entregador não está encontrando o endereço definido, quando estiver realizando a entrega, então ele deve conseguir entrar em contato com o cliente.

**Ordenação MoSCoW:**

Essa funcionalidade será um **MUST**, para evitar desavenças com clientes e restaurantes.

---

## 03) Prioridade Média

**História de usuário original:**
> "O usuário precisa acompanhar o pedido depois de fazer a compra."

**História ajustada para o padrão INVEST:**
> "Como cliente, quero poder acompanhar todas as etapas do meu pedido, desde o preparo até a entrega, e, se possível, acompanhar em tempo real o trajeto quando o entregador estiver trazendo o pedido."

**Critérios de Aceitação:**

1. Dado que o cliente realizou um pedido, quando o pedido começar a ser preparado, então o cliente deve ser notificado.
2. Dado que o entregador buscou o pedido, quando o restaurante finalizar o preparo, então o cliente deve poder acompanhar em tempo real o trajeto do seu pedido.
3. Dado que o restaurante negou o preparo do pedido, quando o cliente tiver realizado o pedido, então o cliente deve receber um estorno e ser notificado.

**Ordenação MoSCoW:**

A princípio, seria uma tarefa **Could**; porém, a funcionalidade de acompanhar em tempo real a rota do pedido é um **Won't**.
