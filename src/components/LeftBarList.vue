<template>
    <div class="left-bar-parent col-3">
        <div v-for="(data, index) in sidebarData" :key="index"
            @click="handleClick(data.name, index)"
            class="sidebar"
            :class="{'selected': currentNum == index}">
            <div>
                {{ data.name }}
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import sidebarData from '@/assets/json/sidebar.json';
import { defineEmits, ref } from 'vue';

const emit = defineEmits(['SetCategory']);

const currentNum = ref(-1);

const handleClick = (str: string, num: number) => {
    currentNum.value = num;
    emit('SetCategory', str);
}
</script>

<style lang="scss" scoped>
.left-bar-parent{
	display: flex;
	justify-content: center;
    flex-direction: column;
}

.sidebar{
    background-color: #EAC100;

    & div{
        cursor: pointer;
    }

    & div:hover{
        background-color: #00CACA;
    }

    &.selected{
        background-color: #ca5955;
    }
}
</style>