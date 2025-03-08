<script setup>
const emit = defineEmits(['click']);

function handleButtonClick(value) {
    emit('click', value);
}
</script>

<template>
    <div class="teclado mt-3">
        <!-- Seção de Operações -->
        <div class="operacoes row mb-3">
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('+')"
                    class="btn rounded-circle botao btn-operacoes">+</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('-')"
                    class="btn rounded-circle botao btn-operacoes">-</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('*')"
                    class="btn rounded-circle botao btn-operacoes">×</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('/')"
                    class="btn rounded-circle botao btn-operacoes">&#247;</button>
            </div>
        </div>

        <!-- Seção de Números -->
        <div class="numeros row mb-3">
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('9')"
                    class="btn rounded-circle botao btn-numeros">9</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('8')"
                    class="btn rounded-circle botao btn-numeros">8</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('7')"
                    class="btn rounded-circle botao btn-numeros">7</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('6')"
                    class="btn rounded-circle botao btn-numeros">6</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('5')"
                    class="btn rounded-circle botao btn-numeros">5</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('4')"
                    class="btn rounded-circle botao btn-numeros">4</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('3')"
                    class="btn rounded-circle botao btn-numeros">3</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('2')"
                    class="btn rounded-circle botao btn-numeros">2</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('1')"
                    class="btn rounded-circle botao btn-numeros">1</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('0')"
                    class="btn rounded-circle botao btn-numeros">0</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('=')"
                    class="btn rounded-circle botao btn-acao">=</button>
            </div>
            <div class="col-3 mt-2">
                <button type="button" @click="handleButtonClick('AC')"
                    class="btn rounded-circle botao btn-acao">AC</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.botao {
    margin-left: 15px;
    width: 50px;
    height: 50px;
    border-color: rgba(0, 0, 0, 0.466);
    font-weight: bold;
}

.btn-operacoes {
    background-color: #fdfe9a;
    font-size: 20px;
}

.btn-operacoes:hover {
    background-color: #f1de72;
}

.btn-numeros {
    background-color: #ffc8e2;
}

.btn-numeros:hover {
    background-color: #e0a6cb;
}

.btn-acao {
    font-size: 20px;
    background-color: #c1e57b;
}

.btn-acao:hover {
    background-color: #a7d362;
}
</style>