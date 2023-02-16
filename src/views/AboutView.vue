<template>
	<div class="about">
		<h1>This is an about me page</h1>
		<h1>關於我的頁面</h1>
		<div class="content">
			<div class="left">
				timeline
			</div>
			<div class="right row">
				<div class="col-12">
					1. 工作:
				</div>
				<div class="col-12">
					2. 語言:
				</div>
				<div class="col-12">
					<div class="row">
						<span class="col-12">3. 筆記分享:</span>
						<a class="col-6" href="https://hackmd.io/@pemomi/r1GSbeq3s">hackmd-css</a>
						<a class="col-6" href="https://hackmd.io/@pemomi/rk-FRk53o">hackmd-git</a>
					</div>
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