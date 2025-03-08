<script setup>
defineProps({
    numeroVisor: {
        type: String,
        required: true,
    },
});
</script>

<template>
    <div class="visor border border-dark rounded mx-auto w-100 px-2">
        <p>{{ numeroVisor || '0' }}</p>
    </div>
</template>

<style scoped>
.visor {
    height: 80px;
    background-color: #d5d5d58e;
}

.visor p {
    width: 100%;
    text-align: right;
    font-size: 3rem;
    font-family: 'Digital', sans-serif;
}
</style>