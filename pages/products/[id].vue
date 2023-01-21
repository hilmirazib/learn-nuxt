<template>
    <div>
        <ProductDetail :product="product" />
    </div>
</template>

<script setup>
definePageMeta({
    layout: 'products'
})
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id;
const { data: product } = useFetch(uri, { key: id });
</script>

<style scoped>

</style>