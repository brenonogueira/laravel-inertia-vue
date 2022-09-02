<template>
    <div>
        <h1>Estou na about</h1>
        <h2>Olá, {{ name }}</h2>
    </div>
</template>

<script>
    export default {
    name: 'PageAbout',
    props: {
        name: String
    }
    }
</script>

<style lang="scss" scoped>

</style>