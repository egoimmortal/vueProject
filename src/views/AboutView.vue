<template>
	<div class="about">
		<h1>This is an about me page</h1>
		<h1>關於我的頁面</h1>
		<div class="content">
			<div class="left">
				timeline
			</div>
			<div class="right">
				<div>
					1. 工作:
				</div>
				<div>
					2. 語言:
				</div>
				<div>
					3. 筆記: <a href="https://hackmd.io/@pemomi/r1GSbeq3s">hackmd-css</a>
				</div>
			</div>
		</div>
	</div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.content{
	display: flex;
    justify-content: space-around;
    align-items: center;
}
</style>