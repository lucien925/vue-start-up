<template>
	<main class="main" role="main">
		<div class="main-container">
			<comment-area v-on:add-comment="addComment"></comment-area>
			<hr>
			<comment-wrap v-bind:comments="comments"></comment-wrap>
		</div>
	</main>
</template>
<script>
	import CommentArea from './CommentArea';
	import CommentWrap from './CommentWrap';
	export default {
		data() {
			return {
				comments: []
			}
		},
		components: {
			CommentArea, CommentWrap
		},
		methods: {
			addComment(comment) {
				this.comments.unshift(comment)				
			}
		}
	}
</script>

<style>
	.main-container {
		width: 1100px;
		margin: 10px auto;
		background: #ccc;
		padding: 20px 10px;
	}
	.main-container .comment-area-container {
	}
	.main-container .comment-area-container > textarea {
		box-sizing: border-box;
		border-radius: 5px;
		border: 1px solid #999;
		outline: none;
		resize: none;
		width: 100%;
		padding: 10px;
	}
	.main-container .comment-action-container {
		margin-top: 20px;
		height: 50px;
	}
	.main-container .comment-action-container > button {
		width: 100px;
		height: 30px;
		border-radius: 5px;
		background: #35495E;
		border: none;
		color: #FFFFFF;
		cursor: pointer;
	}
	.main-container .comment-action-container > button:hover {
		
	}
</style>