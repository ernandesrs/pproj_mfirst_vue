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
                <button @click="itemsListUpload">
                    Adicionar mais items na lista
                </button>
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
            ],
        };
    },

    methods: {
        itemsListUpload() {
            let id = this.items.length + 1;

            this.items.push({
                id: id,
                name: 'Outro item de número ' + id
            });
        },
    }
};

</script>

<style>
button {
    border: 0;
    background-color: #35495E;
    padding: 8px 16px;
    color: #f2f2f2;
    cursor: pointer;
    border-radius: 2px;
}

button:hover {
    background-color: #35495ef0;
}

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