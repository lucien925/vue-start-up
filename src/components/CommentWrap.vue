<template>
	<ul class="comment-lists">
		<comment-item  
			v-for="comment in comments"
			:item="comment"
			transition="out-in"
		>
			
		</comment-item>
	</ul>
</template>

<script>
	import CommentItem from './CommentItem';
	export default {
		data() {
			return {
				
			}
		},
		props: ['comments'],
		components: {
			CommentItem,
		}
	}
</script>