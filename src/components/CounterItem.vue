<template>
    <div class="counter-item">
        <div class="counter-number">{{ counter.number }}</div>
        <button class="btn-increment" @click="increment">Увеличить</button>
    </div>
</template>

<script>

export default {
    name: "CounterItem",
    props: {
        counter: {
            type: Object,
            required: true
        }
    },
    methods: {
        increment () {
            this.$emit('increment-value')
        }
    }
}
</script>
<style>
.counter-item {
    display: inline-flex;
    justify-content: space-between;
    align-items: center;
    background: white;
    flex-basis: calc(100%/3 - 50px);
    border-radius: 16px;
    box-shadow: 0px 0px 4px rgba(0, 0, 0, .1);
}

.counter-number {
    padding: 0px 24px;
}

.btn-increment {
    display: flex;
    align-items: center;
    border: 1px solid var(--color-edit);
    border-radius: 0px 16px 16px 0px;
    padding: 16px 24px;
    cursor: pointer;
    transition: .3s;
}

.btn-increment:hover {
    background: var(--color-edit);
}

@media screen and (max-width: 1024px){
    .counter-item {
        flex-basis: calc(100%/2 - 50px);
    }
}

@media screen and (max-width:768px){
    .counter-item {
        flex-basis: 100%;
    }
}
</style>