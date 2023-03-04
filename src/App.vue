<template>
    <div class="app">
        <ProductForm @create="createNewItem"/>
        <ProductList :productItems="productItems" @remove="removeItem"/>
    </div>
</template>

<script>
import ProductList from '@/components/ProductList.vue'
import ProductForm from '@/components/ProductForm.vue'
export default {
    components: {
        ProductList,
        ProductForm
    },
    data() {
        return {
            productItems: [
                {   
                    id: 1,
                    title: 'Белый диван',
                    body: 'Отличный диван'
                },
                {
                    id: 2,
                    title: 'Синий диван',
                    body: 'Отличный диван'
                },
                {
                    id: 3,
                    title: 'Красный диван',
                    body: 'Отличный диван'
                },
            ] 
        }
    },
    methods: {
        createNewItem(item) {
            this.productItems.push(item)
        },
        removeItem(item) {
            this.productItems = this.productItems.filter(it => it.id !== item.id)
        }
    },
 }
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.app {
    padding: 20px;
}

</style>