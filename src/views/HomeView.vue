<template>
	<div class="container">
		<div class="row">
			<LeftBarList @SetCategory="SetCategory"></LeftBarList>
			<ItemList :ItemData="ItemData"></ItemList>
		</div>
	</div>
</template>

<script lang="ts" setup>
import LeftBarList from '@/components/LeftBarList.vue';
import ItemList from '@/components/Item/ItemList.vue';
import ItemTest from '@/assets/json/ItemTest.json';
import { ref, watch } from 'vue';

const category = ref('');

const ItemData = ref([{
	name: '',
	color: ''
}]);

function SetCategory(str: string){
	category.value = str;
}

watch(category, () => {
	//api
	if(category.value == 'cat')
		ItemData.value = ItemTest.cat;
	else
		ItemData.value = [];
	console.log(ItemData.value);
});

</script>

<style lang="scss" scoped>

</style>