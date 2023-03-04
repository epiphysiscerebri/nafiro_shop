<template>
    <form @submit.prevent>
        <h4>Создание карточки товара</h4>
        <MyInput v-model="productItem.title" type="text" placeholder="Название"/>
        <MyInput v-model="productItem.body" type="text" placeholder="Описание"/>
        <MyButton style="align-self: flex-end; margin-top: 15px;" @click="createNewItem">Добавить</MyButton>
    </form>
</template>

<script>

export default {
    data() {
        return {
            productItem: {
                title: "",
                body: "",
            }
        };
    },
    methods: {
        createNewItem(e) {
            this.productItem.id = Date.now();
            this.$emit("create", this.productItem);
            this.productItem = {
                title: "",
                body: ""
            };
        }
    },
}
</script>

<style scoped>
form {
    display: flex;
    flex-direction: column;
}
</style>