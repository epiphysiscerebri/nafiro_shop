<template>
    <div class="productItem">
        <div><strong>Название: </strong>{{item.title}}</div>
        <div><strong>Описание: </strong>{{item.body}}</div>
    </div>
</template>

<script>
export default {
 props: {
    item: {
        type: Object,
        required: true
    }
 }
}
</script>

<style scoped>
.productItem {
    padding: 15px;
    margin-top: 15px;
    border: 3px solid #028894;
}
</style>