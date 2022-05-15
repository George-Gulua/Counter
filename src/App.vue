<template>
    <div class="app">
        <header-menu @add-counter_card="addCounterCard"/>
        <main-section :counterList="counterList"/>
    </div>
</template>

<script>
import HeaderMenu from '@/components/HeaderMenu.vue';
import MainSection from '@/components/MainSection.vue';

export default {
    name: 'App',
    data () {
        return {
            counterList: []
        }
    },
    components: {
        HeaderMenu,
        MainSection,
    },
    methods: {
        addCounterCard (counterCard) {
            this.counterList.push(counterCard)
        }
    }
};
</script>

<style>
@import url('@/assets/global.css');
</style>
