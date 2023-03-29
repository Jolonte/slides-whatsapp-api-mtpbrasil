<script setup lang="ts">
const EMIT = defineEmits(['info'])

function buttonClick(tool: string) {
    EMIT('info', tool)
}
</script>

<template>
    <div class="flex h-full">
        <div class="grid gap-y-0 gap-x-10 grid-cols-2 grid-rows-3">
            <div @click="buttonClick('microsoft')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-green-400 hover:cursor-pointer bg-green-500">
                <mdi-microsoft class="w-20 h-20 text-white" />
            </div>
            <div @click="buttonClick('atlassian')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-blue-500 hover:cursor-pointer bg-blue-600">
                <mdi-atlassian class="w-20 h-20 text-white" />
            </div>
            <div @click="buttonClick('crm')" class="flex justify-center items-center w-40 h-40 rounded-2xl hover:bg-yellow-400 hover:cursor-pointer bg-yellow-500">
                <mdi-arrow-up-bold-circle class="w-20 h-20 text-white" />
            </div>
        </div>
    </div>
</template>