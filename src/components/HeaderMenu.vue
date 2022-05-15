<template>
    <header class="header-menu">
        <div class="container">
            <a class="label" href="/">Count<span>er</span></a>
            <button class="btn-create" @click="addElement()">Создать счетчик</button>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderMenu',
    methods: {
        addElement () {
            this.$emit('add-counter-card', {
                id: Date.now(),
                number: 0
            })
        }
    }
}
</script>

<style scoped>
header {
    background: var(--color-black);
}

.container{
    align-items: center;
    justify-content: space-between;
    padding: 16px 0px;
}

.label {
    cursor: pointer;
    color: white;
    font-size: 18px;
    font-weight: 700;
}

span {
    color: var(--color-red);
}

.btn-create {
    font-size: 14px;
    font-weight: 400;
    border: 1px solid white;
    border-radius: 4px;
    padding: 8px 24px;
    transition: .3s;
    background: var(--color-black);
    text-transform: uppercase;
    color: white;
    cursor: pointer;
}

.btn-create:hover {
    background: white;
    color: var(--color-black);
    border-color: var(--color-black);
}

@media screen and (max-width: 375px){
    .btn-create {
        padding: 8px 12px;
    }
}
</style>