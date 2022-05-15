<template>
    <main class="main-section">
            <div class="container">
                 <h2 class="section-title">Список счетчиков</h2>
                 <div class="counter-list">
                     <counter-item
                        v-for="counterItem in counterList" :key="counterItem.id"
                        :counterItem="counterItem"
                        @increment-value="counterItem.number++"
                      />
                 </div>
            </div>
    </main>
</template>

<script>
import CounterItem from '@/components/CounterItem.vue'

export default {
    name: 'MainSection',
    props: {
        counterList: {
            type: Array,
            required: true
        }
    },
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

.counter-list {
    display: flex;
    flex-wrap: wrap;
    gap: 50px;
}
</style>