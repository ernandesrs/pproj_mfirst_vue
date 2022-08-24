<template>
    <footer class="footer">
        Todos os direitos reservados &copy; {{ cYear }}
    </footer>
</template>

<script>

export default {
    name: 'MainFooter',
    data() {
        return {
            cYear: (new Date()).getFullYear()
        };
    }
};

</script>

<style>
.footer {
    background-color: #333;
    color: #d6d6d6;
    padding: 26px 0;
    margin-top: auto;
}
</style>