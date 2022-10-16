<template>
    <div class="container mx-auto w-96 pt-8">
        <h1 class="text-lg mb-2">Create</h1>
        <div class="mb-8">
            <Link :href="route('post.index')" class="text-sm mb-8 text-sky-500"
                >BACK</Link
            >
        </div>
        <form @submit.prevent="store">
            <div class="mb-4">
                <input
                    v-model="title"
                    class="w-full rounded-lg border-gray-300"
                    type="text"
                    placeholder="title"
                />
            </div>
            <div class="mb-4">
                <textarea
                    v-model="content"
                    class="w-full rounded-lg border-gray-300"
                    type="text"
                    placeholder="content"
                ></textarea>
            </div>
            <div>
                <button
                    class="ml-auto hover:bg-white hover:text-sky-500 block p-2 w-32 border border-sky-500 bg-sky-500 rounded-full text-center text-white"
                    type="submit"
                >
                    Store
                </button>
            </div>
        </form>
    </div>
</template>
<script>
import { Link } from "@inertiajs/inertia-vue3";
export default {
    name: "Index",
    components: {
        Link,
    },
    data() {
        return {
            title: "",
            content: "",
        };
    },
    methods: {
        store() {
            this.$inertia.post("/posts", {
                title: this.title,
                content: this.content,
            });
        },
    },
};
</script>
<style scoped></style>
