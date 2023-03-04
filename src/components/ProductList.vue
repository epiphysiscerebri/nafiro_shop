<template>
    <div>
        <h3>Список товаров</h3>
        <ProductItem v-for="(item, i) in productItems" :item="item" :key="item.id" @remove="$emit('remove', item)"/>
    </div>
</template>

<script>
import ProductItem from '@/components/ProductItem.vue';
export default {
    components: {
        ProductItem
    },
    props: {
        productItems: {
            type: Array,
            required: true
        }
    },
    data() {
        return {}
    }
}
</script>

<style scoped>

</style>