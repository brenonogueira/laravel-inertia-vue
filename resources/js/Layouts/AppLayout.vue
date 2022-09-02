<template>
    <div>
        <LayoutMenuVue />
        <slot />
    </div>
</template>

<script>
import LayoutMenuVue from './LayoutMenu.vue';

export default {
    components: {
        LayoutMenuVue
    },
    name: 'AppLayout'
}
</script>

<style lang="scss" scoped>
</style>