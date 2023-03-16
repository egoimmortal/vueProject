<template>
    <div class="col-4 commodity">
        <img :src="require(`@/assets/${props.item.imgPath}`)">
        {{ props.item.name }}
    </div>
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
.commodity{
    height: 300px;
}
</style>