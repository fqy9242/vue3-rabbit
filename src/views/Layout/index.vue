<script setup>
import LayoutNav from './components/LayoutNav.vue'
import LayoutHeader from './components/LayoutHeader.vue'
import LayoutFooter from './components/LayoutFooter.vue'
import LayoutFlexd from './components/LayoutFlexd.vue';
import { useCategoryStore } from '@/stores/category';
import { onMounted } from 'vue';
const categoryStore = useCategoryStore()
onMounted(() => {
    categoryStore.getCategory()
})
</script>
<template>
    <LayoutFlexd />
    <LayoutNav />
    <LayoutHeader />
    <RouterView />
    <LayoutFooter />
</template> 