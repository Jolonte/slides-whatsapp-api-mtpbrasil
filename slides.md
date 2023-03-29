---
theme: seriph
background: 'conver_one.jpg'
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Apresentação Whatsapp Business API
drawings:
  persist: false
transition: slide-left
css: unocss
title: Whatsapp Business API
---

# Whatsapp Business API

## Eficiência, sucesso, e produtividade ágil.

<!-- Slide introdutório -->

---
transition: fade-out
---

# Diferenças entre

[Referências](https://www.suri.ai/blog/diferenca-whatsapp-business-e-api).

<div class="flex pt-2">

  <div class="flex flex-col items-center w-100 text-center">
    <h2>Whatsapp Business</h2>
    <div class="flex flex-col pt-2 gap-0 max-w-60">
      <p>Indicado a pequenas empresas;</p>
      <p>Gratuito;</p>
      <p>Perfil comercial: Endereço, site e email;</p>
      <p>Pode ser usado em celulares;</p>
      <p>Respostas rápidas e métricas.</p>
    </div>
  </div>

  <div class="flex flex-col items-center w-100 text-center">
    <h2>Whatsapp Business API</h2>
    <div class="flex flex-col pt-2 gap-0 max-w-60">
      <p>Indicado a empresas de médio/grande porte;</p>
      <p>Pago;</p>
      <p>Automatiza e gerencia atendimentos;</p>
      <p>Usado em plataformas SaaS;</p>
      <p>Notificações, chatbots e múltiplos números.</p>
    </div>
  </div>
</div>

---
layout: center
---

# Preço
[Referências](https://sleekflow.io/pt-br/whatsapp-pricing-calculator).

#### Uma conversa é uma sessão de 24 horas em que a empresa e o usuário podem trocar quantas mensagens quiserem. Existem dois tipos de conversa:

<Counter :value="0.0293" message="Conversas iniciadas pelo usuário" />
<Counter :value="0.2615" message="Conversas iniciadas pela empresa" />

---

# Como a API é integrada
[Referências](https://www.twilio.com/pt-br/docs/whatsapp/quickstart/node).
### Exemplo em um código Node.js usando o Twilio

```js {all|1|2|3|5-12|all}
const ACCOUNT_SID = 'SUA_ACCOUNT_SID';
const AUTH_TOKEN = 'SEU_AUTH_TOKEN';
const CLIENT = require('twilio')(ACCOUNT_SID, AUTH_TOKEN);

CLIENT.messages
  .create({
     from: 'whatsapp:+14155238886', // substituir pelo número do Twilio WhatsApp Sandbox
     body: 'Olá, esta é uma mensagem enviada via WhatsApp Business API!',
     to: 'whatsapp:+55SEU_NUMERO_DE_TELEFONE'
   })
  .then(message => console.log(message.sid))
  .catch(err => console.log(err));
```

---
layout: two-cols
transition: slide-up
---

# Integração com plataformas SaaS
[Referências](https://www.twilio.com/pt-br/docs/whatsapp/quickstart/node).

<script setup lang="ts">
  import { ref } from 'vue';
  
  const TOOL = ref('')

  function changeTool(value) {
    TOOL.value = value
  }
</script>

<Plataforms @info="changeTool" />

::right::

<Benefits :info="TOOL" />

<!-- animações -->

---
layout: two-cols
---

# Benefícios para o Staff

<script setup lang="ts">
  import { ref } from 'vue';
  
  const TEAM = ref('')

  function changeTeam(value) {
    TEAM.value = value
  }
</script>

<Teams @info="changeTeam" />

::right::

<Benefits :info="TEAM" />

---
layout: center
transition: fade-out
---

# Empresas que usam o Whatsapp Business API
[Referências](https://www.take.net/blog/whatsapp/whatsapp-business-api/).

<Image />

---
transition: fade-out
---

# Conclusão

- Melhorar a experiência do cliente;
- Aumentar a produtividade da equipe;
- Reduzir os custos operacionais;
- Ampliar o alcance e a visibilidade da marca;
- Fácil implementação;
- Uso interno no STAFF;
