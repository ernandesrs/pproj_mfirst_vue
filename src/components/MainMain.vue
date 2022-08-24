<template>
    <main class="main">
        <div class="main-container">
            <h1 class="main-title" v-show="pageTitle">{{ pageTitle }}</h1>
            <hr v-show="pageTitle">
            <div class="main-content">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas
                    aspernatur perferendis provident illum dolores, recusandae quis
                    suscipit omnis magnam. Facilis quasi optio sed velit amet quia officia
                    molestiae possimus voluptatum, quidem deleniti inventore illum. Maxime
                    libero aperiam pariatur provident omnis?
                </p>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis qui
                    perspiciatis aperiam, non rem eaque incidunt adipisci odit iste quo
                    assumenda laudantium, neque porro esse distinctio nihil blanditiis
                    vitae repudiandae fuga eveniet sapiente ut sit! Distinctio doloribus
                    quibusdam sunt ex provident perspiciatis quas atque, facilis, ducimus
                    exercitationem incidunt sint reiciendis doloremque veritatis, nam enim
                    explicabo. Similique optio itaque nisi delectus iste eaque autem
                    ducimus reiciendis nesciunt aliquam, quo, nulla at quas velit, tenetur
                    ea commodi?
                </p>
                <p>
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quasi totam
                    ut voluptatum sapiente vitae eaque ipsum ipsam eum distinctio cumque?
                </p>
            </div>
        </div>
    </main>
</template>

<script>

export default {
    name: 'MainMain',
    data() {
        return {
            pageTitle: 'Conteúdo da página inicial'
        };
    }
};

</script>

<style>
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