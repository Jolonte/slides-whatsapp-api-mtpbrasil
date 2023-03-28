<script setup lang="ts">
const EMIT = defineEmits(['info'])

function buttonClick(equipe: string) {
    EMIT('info', equipe)
}
</script>

<template>
    <div class="flex h-full items-center">
        <div class="grid gap-4 grid-cols-2 grid-rows-3">
            <div @click="buttonClick('rh')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-blue-500 hover:cursor-pointer bg-blue-600">
                <mdi-account-group class="w-20 h-20 text-white" />
            </div>
            <div @click="buttonClick('vendas')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-red-400 hover:cursor-pointer bg-red-500">
                <mdi-percent-box class="w-20 h-20 text-white" />
            </div>
            <div @click="buttonClick('infra')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-purple-500 hover:cursor-pointer bg-purple-600">
                <mdi-desktop-classic class="w-20 h-20 text-white" />
            </div>
            <div @click="buttonClick('financas')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-green-400 hover:cursor-pointer bg-green-500">
                <mdi-finance class="w-20 h-20 text-white" />
            </div>
        </div>
    </div>
</template>