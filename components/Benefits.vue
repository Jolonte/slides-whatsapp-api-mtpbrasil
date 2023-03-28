<script setup lang="ts">

interface Props {
    info: String,
}

const props = defineProps<Props>()

</script>

<template>
    <div v-if="props.info === 'rh'">
        <h1>RH e DP</h1>
        <p>Automatizar comunicação com candidatos e funcionários:</p>
        <ul>
            <li>Notificar sobre oportunidades de emprego;</li>
            <li>Marcar entrevistas;</li>
            <li>Envio de formliários de admissão;</li>
        </ul>
        <br>
        <ul>
            <li>Folha de pagamento;</li>
            <li>Benefícios;</li>
            <li>Férias;</li>
            <li>Lembretes;</li>
            <li>Notificações sobre novas políticas e atualizações;</li>
        </ul>
    </div>
    <div v-if="props.info === 'vendas'">
        <h1>Marketing e Vendas</h1>
        <p>Campanhas de marketing e comunicação com clientes:</p>
        <ul>
            <li>Menssagens informativas;</li>
            <li>Segmentação do público alvo;</li>
            <li>Envio de campanhas em massa;</li>
        </ul>
        <br>
        <ul>
            <li>Coletar feedback de clientes;</li>
            <li>Informações sobre serviços;</li>
            <li>Enviar catálogos;</li>
        </ul>
    </div>
    <div v-if="props.info === 'infra'">
        <h1>Infraestrutura</h1>
        <ul>
            <li>Notificar problemas técnicos;</li>
            <li>Atualizações do sistemas e/ou manutenções;</li>
            <li>Suporte técnico: Fornecer respostas rápidas a perguntas frequentes;</li>
            <li>Interrupções programadas;</li>
        </ul>
    </div>
    <div v-if="props.info === 'financas'">
        <h1>Finanças</h1>
        <ul>
            <li>Se comunicar com clientes sobre itens pendentes;</li>
            <li>Enviar notificações sobre faturas atrasadas;</li>
            <li>Cobranças automáticas;</li>
            <li>Permitir que os clientes paguem diretamete pelo Whatsapp;</li>
        </ul>
    </div>
</template>
