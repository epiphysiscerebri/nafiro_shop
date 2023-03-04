<template>
    <div class="productItem">
        <div>
            <div><strong>Название: </strong>{{item.title}}</div>
            <div><strong>Описание: </strong>{{item.body}}</div>
        </div>
        <div class="product_btns">
            <MyButton>Удалить</MyButton>
        </div>
    </div>
</template>

<script>

export default {
    props: {
        item: {
            type: Object,
            required: true
        }
    },
}
</script>

<style scoped>
.productItem {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px;
    margin-top: 15px;
    border: 3px solid #028894;
}
</style>