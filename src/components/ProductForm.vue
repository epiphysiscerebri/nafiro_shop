<template>
    <form @submit.prevent>
        <h4>Создание карточки товара</h4>
        <input class="productItemInput" v-model="productItem.title" type="text" placeholder="Название">
        <input class="productItemInput" v-model="productItem.body" type="text" placeholder="Описание">
        <button class="btn" @click="createNewItem">Добавить</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            productItem: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createNewItem(e) {
            this.productItem.id = Date.now()
            this.$emit('create', this.productItem)
            this.productItem = {
                title: "",
                body: ""
            }
        }
    }
}
</script>

<style scoped>
form {
    display: flex;
    flex-direction: column;
}
.productItemInput {
    width: 100%;
    border: 1px solid #028894;
    padding: 10px 15px;
    margin-top: 15px;
}
.btn {
    margin-top: 15px;
    align-self: flex-end;
    padding: 10px 15px;
    background: none;
    color: #028894;
    border: 1px solid #028894;
}
</style>