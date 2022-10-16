<template>
    <div class="container mx-auto w-96 pt-8">
        <h1 class="text-lg">Posts</h1>
        <div>
            <Link
                class="hover:bg-white hover:text-sky-500 block p-2 w-32 border border-sky-500 bg-sky-500 rounded-full text-center text-white"
                >Add Post</Link
            >
        </div>
    </div>
</template>
<script>
import { Link } from "@inertiajs/inertia-vue3";
export default {
    name: "Index",
    components: {
        Link,
    },
};
</script>
<style scoped></style>
