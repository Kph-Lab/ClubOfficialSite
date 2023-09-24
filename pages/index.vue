<template>
    <main class="relative w-screen flex flex-col text-slate-900">
        <Header/>
        <div class="h-screen grid place-content-center">
            <div class="text-center">
                <h1 class="md:text-7xl text-5xl">海城中高物理部</h1>
                <p class="mt-2 text-slate-400">海城中学高等学校新理科館1階</p>
            </div>
        </div>
        <div class="py-20 px-8 text-white bg-gradient-to-tr from-sky-800 to-blue-950">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-5xl text-center">作品</h2>
                <div class="w-full flex flex-row gap-4 mt-8 overflow-x-auto">
                    <div
                        v-for="work in works"
                        class="flex flex-col gap-2 min-w-[240px] basis-1/3">
                        <div
                            class="rounded-lg w-full bg-cover bg-center"
                            :style="{
                                aspectRatio: '1/1',
                                backgroundImage: `url(${work.image})
                            `}"/>
                        <h1 class="text-2xl font-bold">{{ work.title }}</h1>
                        <p>{{ work.description }}</p>
                        <NuxtLink
                            class="p-2 text-white/60"
                            :to="work._path">部誌を見る</NuxtLink>
                    </div>
                </div>
            </div>
        </div>
        <div class="py-20 px-8">
            <BlogList :blogs="blogs"/>
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