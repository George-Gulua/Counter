<template>
    <div id="app">
        <header-menu @add-counter="addCounter"/>
        <main-section v-bind:counters="counters"/>
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import MainSection from "@/components/MainSection.vue";
export default {
    name: "App",
    data () {
        return {
            counters: [
                
            ]
        }
    },
    components: {
        HeaderMenu,
        MainSection,
    },
    methods: {
        addCounter (counter) {
            this.counters.push(counter)
        }
    }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;700&display=swap');
#app {
    font-family: var(--main-font);
}

:root {
    --main-font: 'Manrope', sans-serif;

    --color-black: #2F2F2F;
    --color-grey:  #E5E5E5;
    --color-white: #F1F1F1;
    --color-green: #008180;
    --color-edit:  #F4C959;
    --color-red:   #FC5151;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: var(--color-grey);
}

.container {
    display: flex;
    margin: 0 auto;
    width: 80%;
}

.section-title {
    font-weight: bold;
}

a {
    text-decoration: none;
}
</style>
