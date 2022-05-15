<template>
    <div class="counter-item">
        <div class="counter-number">{{ counterItem.number }}</div>
        <button class="btn-increment" @click="$emit('increment-value')">Увеличить</button>
    </div>
</template>

<script>
export default {
    name: 'CounterItem',
    props: {
        counterItem: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
.counter-item {
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    background: white;
    border-radius: 16px;
    padding: 32px;
    flex-basis: calc(100%/4 - 50px);
    box-shadow: 0px 0px 4px rgba(0, 0, 0, .1);
}

.btn-increment {
    display: flex;
    align-items: center;
    border: 1px solid var(--color-edit);
    border-radius: 16px 16px 16px 16px;
    padding: 16px 24px;
    margin-top: 16px;
    cursor: pointer;
    transition: .3s;
}

.btn-increment:hover {
    background: var(--color-edit);
}


@media screen and (max-width: 1264px){
    .counter-item {
        flex-basis: calc(100%/3 - 50px);
    }
}

@media screen and (max-width: 600px){
    .counter-item {
        flex-basis: 100%
    }
}


</style>