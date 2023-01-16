<template>
    <div>
        <h2 class="font-bold text-3xl subpixel-antialiased">Currency API</h2>
        <div class="card mt-4">
            <h4 class="font-bold text-lg">
                {{ data.IDR.code }}
            </h4>
            <p>
                {{ data.IDR.value }}
            </p>
        </div>
        <p>{{ ninja }}</p>
    </div>
</template>

<script setup>
definePageMeta({
    layout: 'custom'
});

const { ninja } = await useFetch('/api/ninja');
const { data } = await useFetch('/api/currency/IDR');
</script>