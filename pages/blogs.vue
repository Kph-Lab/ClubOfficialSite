<template>
    <main class="relative w-screen flex flex-col text-slate-900">
        <Header/>
        <div class="py-20 px-8">
            <BlogList :blogs="blogs"/>
        </div>
        <Footer/>
    </main>
</template>
<script setup lang="ts">
const { data } = await useAsyncData('navigation', () => fetchContentNavigation())
const blogs = data.value?.find(topArticle => topArticle._path == "/blog")?.children ?? []
</script>