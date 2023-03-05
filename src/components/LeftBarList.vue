<template>
    <div class="left-bar-parent col-3">
        <div v-for="(data, index) in sidebarData" :key="index">
            <div>
                {{ data.name }}
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import sidebarData from '@/assets/json/sidebar.json'
console.log(sidebarData);
</script>

<style lang="scss" scoped>
.left-bar-parent{
	display: flex;
	justify-content: center;
    flex-direction: column;
}
</style>