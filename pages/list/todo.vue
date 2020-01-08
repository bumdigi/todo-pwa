<template>
	<section class="section">
		<div class="container">
			<div class="columns is-multiline">
				<div @click="onClickTest">/list/todo 입니다.</div>
			</div>
			<input type="text" v-model="user.email"/>
			<input type="text" v-model="user.password"/>
			<input type="text" v-model="user.name"/>
		</div>
	</section>
</template>

<script>
import axios from 'axios'

export default {
	data() {
		return {
			user: {}
		}
	},
	methods: {
		onClickTest() {
			console.log(this.user)
			let uri = 'http://localhost:4000/users/user'
				axios.post(uri, this.user).then(() => {
					
			})
		}
	}
}
</script>