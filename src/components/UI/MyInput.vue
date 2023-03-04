<template>
    <input :value="modelValue" @input="updateInput" class="productItemInput" type="text">
</template>

<script>
export default {
    name: 'MyInput',
    props: {
        modelValue: [String, Number]
    },
    methods: {
        updateInput(event) {
            this.$emit('update:modelValue', event.target.value)
        }
    }
}

</script>

<style scoped>
.productItemInput {
    width: 100%;
    border: 1px solid #028894;
    padding: 10px 15px;
    margin-top: 15px;
}
</style>