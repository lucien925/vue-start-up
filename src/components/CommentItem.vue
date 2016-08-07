<template>
	<li class="comment-item">
		<div class="avater">
			<img src="../assets/logo.png" alt="">
			<span>{{ item.user }}</span>	
		</div>
		<div class="content">
			<p>{{ item.content }}</p>
		</div>
	</li>
</template>
<script>
	export default {
		data() {
			return {}
		},
		props: ['item']
	}
</script>
<style>
	.comment-item {
		padding: 10px;
		height: 100px;
		background: #FFFFFF;
		margin: 10px;
		list-style: none;
	}
	.avater {
		float: left;

	}
	.avater > img{
		width: 80px;
		height: 80px;
		border: 1px solid #ccc;
	}
	.avater > span {
		display: block;
		height: 18px;
		line-height: 18px;
	}
	.content {
		margin-left: 100px;
	}
</style>