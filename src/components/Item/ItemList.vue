<template>
    <div class="col">
        <ItemCom></ItemCom>
        props
    </div>
</template>

<script lang="ts" setup>
import ItemCom from './ItemCom.vue';
import { defineProps } from 'vue';

const props = defineProps({
    name: String,
    color: String
})

console.log(props);

</script>

<style lang="scss" scoped>

</style>