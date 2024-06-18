<template>
        <Header/>
    <div class="site-wrap">
        <TrafficCheckForm />
        <BenefitsAnalysisCards/>
        <DocumentsSlider/>
    </div>
</template>
<script setup>
import Header from './components/Header.vue';
import TrafficCheckForm from './components/TrafficCheckForm.vue'
import BenefitsAnalysisCards from './components/BenefitsAnalysisCards.vue'
</script>



<style lang="scss" scoped>
    .site-wrap{
        max-width: var(--site-width);
        width: 100%;
        margin-left: 374px;
    }
</style>
