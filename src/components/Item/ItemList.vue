<template>
    <div class="col">
        <div class="row">
            <ItemCom v-for="(item, index) in props.itemData" :key="index" :item="item"></ItemCom>
        </div>
    </div>
</template>

<script lang="ts" setup>
import ItemCom from './ItemCom.vue';
import { defineProps } from 'vue';

const props = defineProps<{
    itemData: {
        name: string,
        color: string,
        imgPath: string
    }[]
}>();
</script>

<style lang="scss" scoped>

</style>