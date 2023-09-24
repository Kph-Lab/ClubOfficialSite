<template>
    <div class="max-w-2xl mx-auto">
        <h2 class="text-5xl text-center">部誌</h2>
        <div class="flex flex-col gap-4 mt-8">
            <div
                class="flex flex-col md:flex-row md:items-center gap-4 basis-32"
                v-for="blog in blogs">
                <div
                    class="h-full bg-slate-200 rounded-md text-6xl grid place-content-center p-8 md:p-0 md:aspect-square">
                    {{ blog.icon }}
                </div>
                <div class="flex flex-col md:grow md:p-4">
                    <h3
                        class="text-3xl font-semibold whitespace-nowrap"
                        style="text-overflow: ellipsis; overflow: hidden;">{{ blog.title }}</h3>
                    <p>by: {{ blog.author }}</p>
                    <div class="flex flex-row">
                        <p
                            v-for="tag in blog.tags">
                            #{{ tag }}
                        </p>
                    </div>
                    <NuxtLink
                        class="p-2 text-slate-500"
                        :to="blog._path">
                        部誌を見る
                    </NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
import { NavItem } from '@nuxt/content/dist/runtime/types';

const props = defineProps<{
    blogs: NavItem[]
}>()
</script>