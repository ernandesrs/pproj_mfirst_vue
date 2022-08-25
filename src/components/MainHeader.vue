<template>

    <header class="header">
        <img src="@/assets/logo.png" alt="Logo">
        <h2>ue</h2>
    </header>

</template>

<script>

export default {
    name: 'MainHeader',
}

</script>

<style>
.header {
    display: flex;
    justify-content: start;
    align-items: center;
    cursor: default;
    margin-bottom: 20px;
}

.header>img {
    height: 45px;
}

.header>h2 {
    font-size: 52px;
    margin: 0 0 0 -2px;
    color: #35495E;
}
</style>