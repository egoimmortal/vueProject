<template>
    <div class="col">
        <div class="row">
            <div class="col-3 commodity" v-for="(item, index) in props.itemData" :key="index" :item="item">
                <ItemCom :item="item"></ItemCom>
            </div>
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
.commodity{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: solid;
    border-width: 1px;
    margin: 1%;
    margin-left: 3%;
    margin-right: 3%;
    padding: 2%;
    cursor: pointer;

    &:hover{
        border-color: #FF0000;
    }
}
</style>