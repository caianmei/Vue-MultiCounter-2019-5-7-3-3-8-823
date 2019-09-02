<template>
  <div>
		<p>counterSum  is {{counterSum}}</p>
	</div>
</template>

<script>
	export default {
        name:"CounterGruop",
		data() {
			return {
				counterSum: 0
			}
		},
		methods: {
			
		},
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
