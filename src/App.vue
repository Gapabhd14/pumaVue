

<template>
  <div id="app">
	<open-screen v-if="showcomponent === 0" @showComp="()=>{this.showcomponent++}"></open-screen>
	  <!-- <three-d/> -->
  </div>
</template>

<script >
import OpenScreen from '@/components/OpenScreen.vue';
// import threeD from './components/threeD.vue';
export default {
	name: 'app',
	data() {
		return {
		showcomponent: 0,
		};
	},
	components: {
		OpenScreen,
	},
  
};
</script>


<style scoped>
#app {
	width: 100%;
	height: 100%;
	direction: rtl;
	overflow: hidden;
	margin: 0%;
}
@font-face {
	font-family: varela;
	src: url(./assets/fonts/Varela_Round/VarelaRound-Regular.ttf);
}
@font-face {
	font-family: horev;
	src: url(./assets/fonts/horev/horevclm-heavy-webfont.ttf);
}
* {
	font-family: varela;
	overflow: hidden;
	background-color: rgb(217, 217, 217);
	background-size: 100% 100%;
}
</style>
