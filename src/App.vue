<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Vue.js 프레임워크 수업입니다."/> -->
		<h1 id="h1">{{ msg }}</h1>
		<h2>
			이름은 {{ object.name }}이고 나이는 {{ object.age }}살입니다.
		</h2>
		<h3 id="h3" :align="align">
			내가 좋아하는 것은
		</h3>
		<ul>
			<li :align="align" v-for="item in items"> {{ item.favorite }}</li>
		</ul>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
	
var myid = {name: '유징', age: 51}

export default {
  name: 'App',
	data: function() {
		return {
			msg: 'Vue.js입니다.',
			object: myid,
			items: [
				{ favorite: '아메리카노' },
				{ favorite: '엔비사과' },
				{ favorite: '떡볶이' },
			],
			align: 'left',
		}
	},
  // components: {
  //   HelloWorld
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
	#h1 {
		background: #00F260;  /* fallback for old browsers */
		background: -webkit-linear-gradient(to right, #0575E6, #00F260);  /* Chrome 10-25, Safari 5.1-6 */
		background: linear-gradient(to right, #0575E6, #00F260); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
		color: #f5af19;
	}
	#h3 {
		background-color: #9CECFB;
		color: #8E2DE2;
	}
</style>
