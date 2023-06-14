<template>
  <div id="open-screen" v-touch:swipe="swipeHandler">
       <p class="titlePuma">פומה</p>
	   <div id="startBut"  @click="() => { this.$emit('showComp', 1); }">
			<p id="textStart">שנתחיל?</p>
	   </div>

  </div>
</template>

<script>
import Vue from 'vue'
import Vue2TouchEvents from 'vue2-touch-events'
import { ModelObj } from 'vue-3d-model';

Vue.use(Vue2TouchEvents)
export default {
	name: 'open-screen',
	data() {
		return {
			page: 0,
		};
	},
    // mounted() {
        
	// },
	methods: {
		swipeHandler (direction) {
            if(direction == "top"){
				console.log("yay"); // נעבור לקומפוננטה של הסבר על הלומדה
			}
        }
	}
};
</script>

<style scoped>
#open-screen {
	width: 100vw;
	height: 100vh;
}
#startBut{
	width: 25vw;
	height: 7vh;
	top: 45vh;
	right: 33vw;
	background-color: rgb(237, 125, 49);
	border-radius: 1vh;
	box-shadow: 0 20px 20px rgb(0 0 0 / 0.2);
}
#textStart{
	font-size:2vh;
	text-align: center;
	padding:2vh ;
}
.titlePuma {
	color: rgb(237, 125, 49);
	font-size: 40vw;
	font-family: horev;
	position: absolute;
	right: 25vw;
	animation: titleAnimation 1s 1 forwards;
}
@keyframes titleAnimation {
	from {top: 0vh; opacity: 0.1;}
	to {top: 20vh; opacity: 1;}
}
.model {
	background-color: aqua;
}
</style>
