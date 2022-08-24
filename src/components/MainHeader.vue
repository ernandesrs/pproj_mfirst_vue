<template>
    <header class="header">
        <img class="logo" src="./../assets/logo.png" alt="MfirstVue">

        <slot name="subtitle" />
        
        <p class="desc">
            Este é meu primeiro componente em Vue: 24/08/2022.
        </p>
        <p class="date">
            Hoje é dia: <strong v-text="fullDate"></strong>
        </p>
    </header>
</template>

<script>
export default {
    name: 'MainHeader',
    data() {
        return {
            today: {
                day: (new Date()).getDay(),
                month: (new Date()).getMonth(),
                year: (new Date()).getFullYear(),
            }
        };
    },

    computed: {
        fullDate() {
            return `${this.today.day}/${this.today.month}/${this.today.year}`;
        },
    },
}
</script>

<style>
.header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    min-height: 75px;
    border-bottom: 1px solid #CCC;
    text-align: center;
}

.logo {
    width: 100%;
    max-width: 100px;
}

.desc {
    width: 100%;
    max-width: 375px;
    font-weight: 600;
    color: rgb(75, 75, 75);
    cursor: default;
}
</style>