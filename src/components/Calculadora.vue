<script setup>
import { ref } from 'vue';
import Visor from './Visor.vue';
import Teclado from './Teclado.vue';

const numeroVisor = ref('');

function handleClick(value) {
    if (value === 'AC') {
        numeroVisor.value = '';
    } else if (value === '=') {
        try {
            numeroVisor.value = eval(numeroVisor.value).toString();
        } catch (error) {
            numeroVisor.value = '⚠️ERRO⚠️';
            setTimeout(() => {
                numeroVisor.value = ''
            }, 800);
        }
    } else {
        numeroVisor.value += value;
    }
}

function handleKeyDown(event) {
    const key = event.key;
    const keyMap = {
        '0': '0',
        '1': '1',
        '2': '2',
        '3': '3',
        '4': '4',
        '5': '5',
        '6': '6',
        '7': '7',
        '8': '8',
        '9': '9',
        '+': '+',
        '-': '-',
        '*': '*',
        '/': '/',
        '.': '.',
        'Enter': '=',
        'Backspace': 'AC',
        'Escape': 'AC',
    };

    if (keyMap[key]) {
        handleClick(keyMap[key]);
    }
}
</script>

<template>
    <main @keydown="handleKeyDown" tabindex="0" class="bg-dark d-flex justify-content-center align-items-center"
        style="height: 100vh;">
        <div class="corpo border border-dark rounded p-4">
            <Visor :numeroVisor="numeroVisor" />
            <Teclado @click="handleClick" />
        </div>
    </main>
</template>

<style scoped>
.corpo {
    width: 30vw;
    background-color: #c2ffe1;
}
</style>