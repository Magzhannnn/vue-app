<template>
	<div class="app">
		<post-form @create="createPost" />
		<post-list :posts="posts" @remove="removePost" />
	</div>
</template>

<script>
import PostForm from '@/components/PostForm';
import PostList from '@/components/PostList';

export default {
	components: {
		PostList,
		PostForm,
	},
	data() {
		return {
			posts: [
				{ id: 1, title: 'JavaScript 1', body: 'Описание поста 1' },
				{ id: 2, title: 'JavaScript 2', body: 'Описание поста 2' },
				{ id: 3, title: 'JavaScript 3', body: 'Описание поста 3' },
			],
		};
	},
	methods: {
		createPost(post) {
			this.posts.push(post);
		},
		removePost(postV) {
			this.posts = this.posts.filter(post => postV.id !== post.id)
		}
	},
};
</script>

<style>
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

.app {
	margin: 20px;
}
</style>
