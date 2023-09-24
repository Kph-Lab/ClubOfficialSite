<template>
    <main class="relative w-screen flex flex-col text-slate-900">
        <Header/>
        <div class="py-20 my-8 px-8">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-5xl text-center">作品</h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 mt-8">
                    <div
                        v-for="work in works"
                        class="flex flex-col gap-2 basis-1/3">
                        <div
                            class="rounded-lg w-full bg-cover bg-center"
                            :style="{
                                aspectRatio: '1/1',
                                backgroundImage: `url(${work.image})
                            `}"/>
                        <h1 class="text-2xl font-bold">{{ work.title }}</h1>
                        <p>{{ work.description }}</p>
                        <NuxtLink
                            class="p-2 text-black/60"
                            :to="work._path">部誌を見る</NuxtLink>
                    </div>
                </div>
            </div>
        </div>
        <Footer/>
    </main>
</template>
<script setup lang="ts">
const { data } = await useAsyncData('navigation', () => fetchContentNavigation())
const blogs = data.value?.find(topArticle => topArticle._path == "/blog")?.children ?? []

const works = computed(() => {
    return blogs?.filter(blog => (blog.tags as string[]).includes("作品"))
})
</script>