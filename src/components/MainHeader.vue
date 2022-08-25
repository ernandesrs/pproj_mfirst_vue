<template>

    <header class="header">
        <div class="logo">
            <img src="@/assets/logo.png" alt="Logo">
            <h2>ue</h2>
        </div>

        <slot name="header-nav" />
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
    justify-content: space-between;
    align-items: center;
    cursor: default;
    margin-bottom: 20px;
}

.header>.logo {
    display: flex;
    align-items: center;
}

.header>.logo>img {
    height: 35px;
}

.header>.logo>h2 {
    font-size: 32px;
    margin: 0 0 0 0;
    color: #35495E;
}
</style>