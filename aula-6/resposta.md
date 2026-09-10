# 📋 Automatização da Cobrança de Assinaturas de GMUDs

> **Problema:** Tempo gasto na organização, acompanhamento e envio de lembretes para os assinantes de GMUDs que possuem documentos pendentes de assinatura.

---

## 1. 🤝 Empatia

### Entendimento do processo atual

Para compreender melhor o problema, é necessário entender como funciona atualmente o processo de cobrança das assinaturas.

**Perguntas levantadas:**

* Como é realizada atualmente a cobrança dos responsáveis pelas GMUDs?
* Com que frequência os lembretes são enviados?
* Quanto tempo é gasto semanalmente nesse acompanhamento?
* Quais são as principais dificuldades encontradas durante o processo?

---

## 2. 🎯 Definição

### Problema identificado

O principal problema está no **tempo gasto para organizar, acompanhar e enviar lembretes aos usuários que possuem GMUDs pendentes de assinatura**.

Esse processo, quando realizado manualmente, exige acompanhamento constante e pode resultar em:

* ⏱️ Perda de tempo com atividades repetitivas;
* 📩 Envio manual de diversos lembretes;
* ⚠️ Risco de esquecer algum usuário;
* 📋 Dificuldade no acompanhamento das pendências;
* 🚧 Atrasos no processo de subida das GMUDs.

### 💡 Oportunidade

Automatizar o processo de cobrança, reduzindo o trabalho manual e garantindo que os responsáveis sejam notificados até que a pendência seja resolvida.

---

## 3. 💡 Ideação

Foram levantadas algumas possíveis soluções para o problema:

### 1️⃣ Lembrete semanal por e-mail

Enviar automaticamente um e-mail uma vez por semana para os usuários que possuem GMUDs pendentes de validação.

**Vantagens:**

* Fácil implementação;
* Comunicação formal;
* Baixa frequência de notificações.

**Desvantagem:**

* Pode não gerar urgência suficiente para resolver a pendência.

---

### 2️⃣ Lembrete diário via Microsoft Teams ⭐

Enviar automaticamente uma mensagem pelo **Microsoft Teams todos os dias** para os usuários que possuem GMUDs pendentes, mantendo as cobranças até que a assinatura seja realizada.

**Vantagens:**

* Comunicação mais direta;
* Maior visibilidade da pendência;
* Redução do acompanhamento manual;
* Cobrança contínua até a resolução.

**Desvantagem:**

* Pode gerar excesso de notificações se não houver regras de controle.

---

### 3️⃣ Bloqueio da subida de GMUDs com pendências

Impedir que chamados com GMUDs que possuam assinaturas pendentes sejam encaminhados/subidos.

**Vantagens:**

* Evita o avanço de GMUDs incompletas;
* Garante que as assinaturas sejam realizadas.

**Desvantagens:**

* Pode impactar o fluxo operacional;
* Pode gerar bloqueios desnecessários em situações excepcionais.

---

## 4. ✅ Escolha

### Solução escolhida

> **Enviar um lembrete via Microsoft Teams todos os dias até que a GMUD seja assinada.**

A solução foi escolhida por apresentar o melhor equilíbrio entre **automação, facilidade de acompanhamento e redução do trabalho manual**.

O responsável pela GMUD não precisará verificar constantemente quais usuários ainda possuem pendências, pois o sistema realizará automaticamente as cobranças.

---

## 5. 👤 História de Usuário

> **COMO** responsável e gerenciador das GMUDs,
> **QUERO** realizar cobranças de forma automática aos usuários com assinaturas pendentes,
> **PARA** focar meu tempo em outras demandas que necessitam de maior atenção.

---

## 6. ✔️ Critérios de Aceitação

### 🔴 1. GMUD com prazo vencido

**DADO** uma GMUD com o prazo de assinatura vencido,
**QUANDO** o usuário ainda não tiver realizado a assinatura,
**ENTÃO** deverá ser enviado um **lembrete URGENTE** para o usuário.

---

### 🏖️ 2. Usuário em férias

**DADO** um usuário que esteja de férias,
**QUANDO** ele possuir uma GMUD pendente de assinatura,
**ENTÃO** ele não deverá receber cobranças durante o período de férias.

**E** quando retornar das férias, deverá receber **IMEDIATAMENTE** a cobrança referente à GMUD pendente.

---

### 🚫 3. Usuário desligado da empresa

**DADO** um usuário que tenha sido desligado da empresa,
**QUANDO** ele possuir uma GMUD pendente de assinatura,
**ENTÃO** a GMUD deverá ser **encerrada sem a necessidade da assinatura desse usuário**.