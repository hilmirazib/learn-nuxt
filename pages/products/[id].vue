<template>
    <div>

        <Head>
            <Title>Nuxt Dojo | {{ product?.title }}</Title>
            <Meta name="description" :content="product?.description" />
        </Head>
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

// if (!product.value) {
//     throw createError({ statusCode: 404, statusMessage: 'Page Not Found' })
// }
</script>

<style scoped>

</style>