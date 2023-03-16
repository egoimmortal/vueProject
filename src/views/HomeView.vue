<template>
	<div class="container">
		<div class="row">
			<LeftBarList @SetCategory="SetCategory"></LeftBarList>
			<ItemList :itemData="itemData"></ItemList>
		</div>
	</div>
</template>

<script lang="ts" setup>
import LeftBarList from '@/components/LeftBarList.vue';
import ItemList from '@/components/Item/ItemList.vue';
import ItemTest from '@/assets/json/ItemTest.json';
import { ref, watch } from 'vue';

const category = ref('');

const itemData = ref([{
	name: '',
	color: '',
	imgPath: ''
}]);

itemData.value = [];

function SetCategory(str: string){
	category.value = str;
}

watch(category, () => {
	//api
	if(category.value == 'cat')
		itemData.value = ItemTest.cat;
	else
		itemData.value = [];
});

</script>

<style lang="scss" scoped>

</style>