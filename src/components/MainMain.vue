<template>
    <main class="main">
        <div class="main-container">
            <h1 class="main-title" v-show="pageTitle">{{ pageTitle }}</h1>
            <hr v-show="pageTitle">
            <div class="main-content">
                <ul>
                    <li v-for="item in items" v-bind:key="item">
                        <b>#{{ item.id }}</b> - {{ item.name }}
                    </li>
                </ul>
                <button @click="itemsListUpload">
                    Adicionar mais items na lista
                </button>
                <hr>
                <form>
                    <h3 style="text-align: left;">Título desta página</h3>
                    <div style="display:flex;">
                        <input type="text" v-model="pageTitle">
                    </div>
                    <h3 style="text-align: left;">Usuário</h3>
                    <div style="display:flex;">
                        <input type="text" v-model="user.first_name">
                        <div style="margin:0 1px;"></div>
                        <input type="text" v-model="user.last_name">
                    </div>
                    <p>{{ fullName }}</p>
                </form>
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
                    name: '1 muito top',
                },
                {
                    id: 2,
                    name: '2 item top',
                },
            ],

            user: {
                first_name: "",
                last_name: ""
            }
        };
    },

    methods: {
        itemsListUpload() {
            let id = this.items.length + 1;

            this.items.push({
                id: id,
                name: id + ' item top'
            });
        },
    },

    computed: {
        fullName() {
            return `${this.user.first_name} ${this.user.last_name}`;
        }
    },

    watch: {
        pageTitle() {
            console.log("Título da página foi alterado!\n");
            console.log("---- implementar uma lógica ----");
        },

        user: {
            handler() {
                console.log("Alterou User!!!\n");
                console.log("---- implementar uma lógica ----");
            },

            deep: true
        }
    },
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
    opacity: 0.8;
}

ul {
    list-style: none;
    padding-left: 0;
}

ul>li {
    display: flex;
    align-items: center;
    text-align: left;
    background-color: #f2f2f2;
    padding: 8px 16px;
    margin-bottom: 1px;
}

ul>li:hover {
    background-color: #ebeced;
    color: #35495E;
    cursor: pointer;
}

ul>li>button {
    margin-left: auto;
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