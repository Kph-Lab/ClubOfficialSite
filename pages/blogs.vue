<template>
    <main class="relative w-screen flex flex-col text-slate-900">
        <Header/>
        <div class="py-20 px-8">
            <BlogList :blogs="showBlogs">
                <div class="flex flex-wrap items-center gap-2">
                    <button
                        v-for="tag in blogTags"
                        class="py-2 px-3 rounded-md border-[1px] border-gray-200"
                        :class="{ 'border-blue-400 bg-blue-200': selectedTags.includes(tag)}"
                        @click="updateTags(tag)">
                        #{{ tag }}
                    </button>
                </div>
            </BlogList>
        </div>
        <Footer/>
    </main>
</template>
<script setup lang="ts">
const { data } = await useAsyncData('navigation', () => fetchContentNavigation())
const blogs = data.value?.find(topArticle => topArticle._path == "/blog")?.children ?? []

const route = useRoute()

const joinLetter = ","

const selectedTags = computed(() => ((route.query.tags as string) ?? "").split(joinLetter).filter((tag) => tag != ""))
const blogTags = (() => {
    let tags: string[] = []
    blogs.forEach(blog => {
        blog.tags.forEach((tag: string) => {
            if( !tags.includes(tag) ){ tags.push(tag) }
        })
    })
    return tags
})()

const showBlogs = computed(() => {
    if( selectedTags.value.length == 0 ){
        return blogs
    }

    return blogs.filter((blog) => {
        for( const selectedTag of selectedTags.value){
            if( !blog.tags.includes(selectedTag) ){
                return false
            }
        }
        return true
    })
})

const router = useRouter()

const updateTags = (tag: string) => {
    const newTags = (() => {
        if( selectedTags.value.includes(tag) ){
            return selectedTags.value.filter((selectedTag) => selectedTag != tag)
        }else{
            return [ ...selectedTags.value, tag ]
        }
    })()
    router.push({
        path: route.path,
        query: {
            tags: newTags.join(joinLetter)
        }
    })
}
</script>