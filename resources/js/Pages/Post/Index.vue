<template>
    <div class="container mx-auto w-96 pt-8">
        <h1 class="text-lg mb-8">Posts</h1>
        <div class="mb-8">
            <Link
                :href="route('post.create')"
                route
                class="hover:bg-white hover:text-sky-500 block p-2 w-32 border border-sky-500 bg-sky-500 rounded-full text-center text-white"
                >Add Post</Link
            >
        </div>
        <div v-if="posts">
            <div
                class="mt-8 pt-8 border-t border-sky-500"
                v-for="post in posts"
            >
                <div>id: {{ post.id }}</div>
                <div>title: {{ post.title }}</div>
                <div>content: {{ post.content }}</div>
                <div class="text-sm text-right">
                    created_at: {{ post.date }}
                </div>
                <div class="text-sm text-right">
                    <Link
                        :href="route('post.show', post.id)"
                        class="text-sm mb-8 text-sky-500"
                        >Show</Link
                    >
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
    name: "Index",

    props: ["posts"],

    components: {
        Link,
    },
};
</script>
<style scoped></style>
