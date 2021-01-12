<template>
	<div id="app">
		
		
		<h1 >Diretivas (Desafio)</h1>
		<hr>

	  
  
		<button v-quando:click="acao">Ativar</button>
		<p v-quando:mouseenter="mouseEnter">Vamos CODAR</p>
	</div>
</template>

<script>
export default {
	directives: { 
		quando: { 
			bind(el, binding) {
				//el.onclick = function(e) {
				//	binding.value()
				//}
				const tipo = binding.arg
				const fn = binding.value
				el.addEventListener(tipo, fn)
			}
		} 
	},
	methods: {
		acao() {
			alert('Vamos programar!')
		},
		mouseEnter() {
			console.log('Vamos programar!')
		}
	}
	
}
</script>

<style>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
	font-size: 2.5rem;
}

button {
	margin: 10px 0px;
	padding: 10px 20px;
	font-size: 1.4rem;
	border-radius: 5px;
	color: #FFF;
	background-color: #2196F3;
}

div.tres {
 width:30px;
 height:30px;
 border: 25px solid; /* As 4 bordas sólidas com 25px de espessura */
 border-color: #f00 #0f0 #00f #fc0; /* cores: topo, direita, inferior, esquerda */

 align-items: center;

 align-content: center;
 }

</style>
