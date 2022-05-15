<template>
    <div id="main-section">
        <main>
            <div class="container">
                 <h2 class="section-title">Список счетчиков</h2>
                 <div class="counters">
                     <counter-item
                        v-for="counter in counters" :key="counter.id"
                        v-bind:counter="counter"
                        @increment-value="counter.number++"
                      />
                 </div>
            </div>
        </main>
    </div>
</template>

<script>
import CounterItem from "@/components/CounterItem.vue";
export default {
    name: "MainSection",
    props: ['counters'],
    components: {
        CounterItem
    }
};
</script>

<style scoped>
.container {
    gap: 52px;
    padding: 52px 0px;
    flex-direction: column;
}

.counters {
    display: flex;
    flex-wrap: wrap;
    row-gap: 50px;
    column-gap: 75px;
}

</style>