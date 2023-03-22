<template>
    <img :src="require(`@/assets/${props.item.imgPath}`)">
    {{ props.item.name }}
</template>

<script lang="ts" setup>
import { defineProps, ref } from 'vue';

const props = defineProps<{
    item: {
        name: string,
        color: string,
        imgPath: string
    }
}>();
</script>

<style lang="scss" scoped>
img{
    width: 80%;
    height: auto;
}
</style>