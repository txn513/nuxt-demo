<template>
    <div>
        <p>about</p>
        <div v-for="item in list" :key="item">{{ item }}</div>
    </div>
</template>
<script>
export default {
    async asyncData({ $axios }) {
        const res = await $axios.$get('/api/test')
            return { list: res.data.list }
    }
}
</script>
