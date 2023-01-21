<template>
    <div>
        <p>Route {{ id }}</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore distinctio optio quisquam.</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params
</script>

<style scoped>

</style>