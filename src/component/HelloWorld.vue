<template>
	<div class="hello">
		<p>Vuex-基礎應用-自store中取得state / getter 資料, 透過 action mustation 修改 state</p>
		<br>
		<p>
			name:
			<span>{{ $store.state.name }}</span>
		</p>
		<p>
			Name.lnegth =
			<span>{{ $store.getters.nameLength }}</span>
		</p>
		<span> keyin your name and keydown "Enter": </span>
		<p></p>
		<input type="text" v-model="userName" placeholder="what's your name?"
			@keydown.enter="$store.dispatch('updateName', userName)" />
		<br><br><br><br><br>
		<form action="" id="login-form">
			<label for="email">
				Email
				<input type="email" name="email" id="email" required />
			</label>
			<br>
			<label for="password">
				Password
				<input type="password" name="password" id="password" required />
			</label>
			<br>
			<button id="btn" type="submit">Login</button>
		</form>
	</div>
</template>

<script>
export default {
	name: "HelloWorld",
	data() {
		return {
			userName: "",
		};
	}
}
</script>

<style scoped>
.hello {
	margin: 15rem auto;
	text-align: center;
	font-size: 1.2rem;
}

input {
	font-size: 1.5rem;
	text-align: center;
	padding: 5px 2px;
}

span {
	color: gray;
}

p>span {
	color: blue;
	font-weight: bold;
}
</style>