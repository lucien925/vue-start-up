<template>
	<div class="comment-area-container">
		<div class="comment-content">
			<textarea name="comment" id="comment" rows="10" placeholder="有什么新鲜事想告诉大家?"></textarea>
		</div>
		<div class="comment-action">
			<button v-on:click="handleClick">发布</button>
		</div>
	</div>
</template>
<script>
	export default {
		data() {
			return {}
		},
		methods: {
			handleClick() {
				var content = this.$el.querySelector('#comment').value;
				// 	comment = {
				// 		user: 'lucienyu',
				// 		avater: '',
				// 		content: content
				// 	}
				// this.comments.push(comment);
				// var $parent = this.$parent,
				// 	$el = this.$el,
				// 	content = $el.querySelector('#comment'),
				// 	comment = {
				// 		user: 'lucienyu',
				// 		avater: '',
				// 		content: content
				// 	}
				// $parent.comments.push(comment);
				this.$dispatch('add-comment', {
			 		user: 'lucienyu',
			 		avater: '',
			 		content: content
			 	})


			}
		}
	}
</script>
<style scoped>
	.comment-area-container {
		padding: 10px;
	}
	.comment-content {
		padding: 10px;
		border: 1px solid #ccc;
		background: #ffffff;
	}
	.comment-content > textarea {
		width: 100%;
		font-size: 14px;
		border: none;
		resize: none;
		outline: none;

	}

	.comment-action {
		padding-top: 20px;
	}
	.comment-action > button {
		width: 100px;
		height: 30px;
		cursor: pointer;
	}
</style>