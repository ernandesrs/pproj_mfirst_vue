<template>
    <div :class="['alert', 'alert-' + message.type]">
        <div class="text">{{ message.text }}</div>
        <button class="close" @click="closeAlert">X</button>
    </div>
</template>

<script>

export default {
    name: "UiAlert",

    props: ['message'],

    methods: {
        closeAlert() {
            this.$emit("closeAlert");
        }
    }
};

</script>

<style>
.alert {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 20px 0;
    padding: 15px;
    border: 1px solid rgb(229, 228, 228);
    font-weight: 600;
    font-size: 0.875rem;
    background-color: rgb(114, 114, 114);
    color: #e5e5e5;
    border-radius: 2px;
}

.alert>.close {
    background-color: transparent;
    border: 0;
    cursor: pointer;
    color: #e5e5e5;
}

.alert>.close:focus {
    outline: 0;
}

.alert-success {
    background-color: #54997a;
}

.alert-danger {
    background-color: #df6262;
}

.alert-warning {
    background-color: #ba9961;
}
</style>