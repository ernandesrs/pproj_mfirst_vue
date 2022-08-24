<template>
    <main class="main">
        <div class="main-container">
            <h1 class="main-title" v-show="pageTitle">{{ pageTitle }}</h1>
            <hr v-show="pageTitle">
            <div class="main-content">
                <ul>
                    <li v-for="item in items" v-bind:key="item">
                        <b>#{{ item.id }}</b> {{ item.name }}
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<script>

export default {
    name: 'MainMain',
    data() {
        return {
            pageTitle: 'Uma lista qualquer',
            items: [
                {
                    id: 1,
                    name: 'Item muito top',
                },
                {
                    id: 2,
                    name: 'Outro item top',
                },
                {
                    id: 3,
                    name: 'Legal este item',
                },
                {
                    id: 4,
                    name: 'Penúltimo item, mas não menos legal',
                },
                {
                    id: 5,
                    name: 'Último item, mas não menos legal',
                },
            ],
        };
    }
};

</script>

<style>
ul {
    list-style: none;
    padding-left: 0;
}

ul>li {
    display: block;
    text-align: left;
    background-color: #f2f2f2;
    padding: 8px 16px;
    margin-bottom: 1px;
}

ul>li:hover {
    background-color: #35495E;
    color: #f2f2f2;
    cursor: pointer;
}

.main {
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 18px 26px;
}

.main>.main-container {
    width: 100%;
    max-width: 562px;
    border: 1px solid #CCC;
    padding: 18px 26px;
    background-color: #f1f1f1;
}

.main>.main-container>.main-title {
    padding-bottom: 8px;
}
</style>