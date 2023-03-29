<script setup lang="ts">
import { ref } from 'vue';

interface Props {
    value: Number,
    message: String
}

const props = defineProps<Props>()

const CHAT = ref(0)
const CHAT_PRICE = ref(0)

function addChat(propsPrice: number): void {
    CHAT.value++
    CHAT_PRICE.value+=propsPrice
}

function removeChat(propsPrice: number): void {
    CHAT.value--
    CHAT_PRICE.value-=propsPrice
}
</script>

<template>
    <div class="flex flex-col text-center my-4">
        <div class="flex justify-center gap-4">
            <p>{{ props.message }}: {{ Math.max(0, CHAT) }}</p>
            <p>Preço p/ conversa: R$ {{ Math.max(0, CHAT_PRICE.toFixed(2)) }}</p>
        </div>
        <div class="flex justify-center gap-2">
            <button @click="removeChat(props.value)">-</button>
            <button @click="addChat(props.value)">+</button>
        </div>
    </div>
</template>

<style scoped>
    button {
        background-color: white;
        color: black;
        padding: 0.5rem 1rem 0.5rem 1rem;
        border-radius: 1rem;
    }
    button:hover {
        background-color: aliceblue;
    }
</style>