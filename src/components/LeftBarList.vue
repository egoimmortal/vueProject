<template>
    <div class="left-bar-parent col-3">
        <div v-for="(data, index) in sidebarData" :key="index" class="sidebar" @click="handleClick(data.name)">
            <div>
                {{ data.name }}
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import sidebarData from '@/assets/json/sidebar.json';
import { defineEmits } from 'vue';

const emit = defineEmits(['SetCategory']);

const handleClick = (str: string) => {
    emit('SetCategory', str);
}

// console.log(sidebarData);
</script>

<style lang="scss" scoped>
.left-bar-parent{
	display: flex;
	justify-content: center;
    flex-direction: column;
}

.sidebar{
    background-color: #EAC100;
}
</style>