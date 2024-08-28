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