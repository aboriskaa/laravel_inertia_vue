<template>
    <div class="container mx-auto w-96 pt-8">
        <h1 class="text-lg mb-2">Post</h1>
        <div class="mb-8">
            <Link :href="route('post.index')" class="text-sm mb-8 text-sky-500"
                >BACK</Link
            >
        </div>
        <div v-if="post">
            <div class="mt-8 pt-8 border-t border-sky-500">
                <div>id: {{ post.id }}</div>
                <div>title: {{ post.title }}</div>
                <div>content: {{ post.content }}</div>
                <div class="text-sm text-right">
                    created_at: {{ post.date }}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
    name: "Show",

    props: ["post"],

    components: {
        Link,
    },
};
</script>
<style scoped></style>
