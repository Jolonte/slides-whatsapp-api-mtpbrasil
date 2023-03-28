<script setup lang="ts">

interface Props {
    info: String,
}

const props = defineProps<Props>()

</script>

<template>
    <div v-if="props.info === 'microsoft'">
        <h1>Microsoft</h1>
        <ul>
            <li>Dynamics 365: Agilizar processo de vendas;</li>
            <li>Teams: Comunicação com clientes;</li>
        </ul>
    </div>
    <div v-if="props.info === 'atlassian'">
        <h1>Atlassian</h1>
        <ul>
            <li>Jira: Equipes e funcionários podem receber notificações de incidentes e problemas em tempo real;</li>
            <li>Trello: Notificações de atividades no Trello;</li>
            <li>Confluence: Compartilhar arquivos, ideias e feedbacks. Monitorar progresso de projetos, definir tarefas e delegar responsabilidades, tudo em um só lugar;</li>
        </ul>
    </div>
    <div v-if="props.info === 'crm'">
        <h1>CRM</h1>
        <ul>
            <li>Acesso direto aos clientes: A empresa pode se comunicar diretamente com seus clientes por meio do aplicativo mais popular do mundo;</li>
            <li>Automatização de comunicações: Notificações, confirmações de agendamento, atualizações de status, entre outras;</li>
            <li>Aumento da conversão de vendas: Canal de vendas mais rápido e conveniente;</li>
        </ul>
    </div>
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
