<template>
    <main class="flex flex-col gap-8">
        <Header/>
        <div class="max-w-2xl mx-auto pt-8">
            <div>
                <h1 class="text-6xl font-semibold">{{ title ?? "記事が見つかりません" }}</h1>
                <p v-if="!!author">by: {{ author }}</p>
            </div>
            <ContentDoc
                id="document"
                class="mt-4">
                <template #not-found>
                    <p>すみません、記事が見つかりませんでした、、、</p>
                    <NuxtLink to="/">ホームへ戻る</NuxtLink>
                </template>
            </ContentDoc>
        </div>
        <Footer/>
    </main>
</template>
<script setup lang="ts">
const route = useRoute()

const { data } = await useAsyncData('page-data', () => queryContent(`/blog/${route.params.blog}`).findOne())
const { title, author } = data.value ?? {} as { [key: string]: string }
</script>
<style>
#document > h1 {
    font-size: 40px;
    font-weight: bold;
}
#document > h2 {
    font-size: 24px;
}
#document > blockquote {
    padding: 8px 12px;
    margin: 8px 0;
    background-color: #f1f5f9;
    border-left: solid 2px #cbd5e1;
    border-radius: 4px;
}
#document > ul {
    list-style: disc;
    margin: 8px 0;
}
#document > ol {
    list-style: decimal;
    margin: 8px 0;
}
#document > * > img {
    border-radius: 8px;
}
</style>