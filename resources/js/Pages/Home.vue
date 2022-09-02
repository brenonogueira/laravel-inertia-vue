<template>
    <div>
        <div>
            <Link :href="route('home')">Posts</Link>
            <Link :href="route('about')">About</Link>
        </div>
    </div>

    <div class="overflow-x-auto">
        <table class="min-w-full text-sm border border-gray-100 divide-y-2 divide-gray-200">
            <thead>
                <tr class="divide-x divide-gray-100">
                    <th class="px-4 py-2 font-medium text-left text-gray-900 whitespace-nowrap">ID</th>
                    <th class="px-4 py-2 font-medium text-left text-gray-900 whitespace-nowrap">Título</th>
                    <th class="px-4 py-2 font-medium text-left text-gray-900 whitespace-nowrap">Descrição</th>
                </tr>
            </thead>

            <tbody class="divide-y divide-gray-200">
                <tr class="divide-x divide-gray-100" v-for="post in posts" :key="post.id">
                    <td class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap">{{ post.id }}</td>
                    <td class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap">{{ post.title }}</td>
                    <td class="px-4 py-2 text-gray-700 whitespace-nowrap">{{ post.content }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
import { Link } from '@inertiajs/inertia-vue3'
import AppLayoutVue from '../Layouts/AppLayout.vue';

export default {
    layout: AppLayoutVue,

    name: 'Page Home',

    components: {
        Link
    },

    props: {
        posts: Object
    },
}
</script>
<style lang="scss" scoped>
</style>