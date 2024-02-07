<script setup>
    import ApiCovid from './components/apiCovid.vue'
</script>

<template>
    <div class="container mx-auto">
        <div class="shadow-xl">
            <h1 class="text-2xl font-bold mb-4 text-center titulo">Casos confirmados de COVID-19 por País</h1>
        </div>
       

        <div class="shadow-xl">
            <ApiCovid></ApiCovid>
        </div>
        
    </div>


 
        
</template>

<style scoped>
    .titulo{
        padding-top: 52px;
    }
</style>
