<template>
  <div class="list">
    <h1>{{ header }}</h1>
	<div class="drop">
	<ul>
	<li v-for="item in grocery"><a :href="item.href">{{item.text}}</a>
	<ul v-if="item.sub">
		<li v-for="x in item.sub">{{x.text}}</li>
		
	</ul>
	</li>
	
	</ul>
	</div>  
</div>



</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      header: 'Drop Down Menu',
	grocery: [
		{id: 0, text: 'Vegetables', href: '#1', sub: 
							[{id: 0, text: 'Corn'},
							{id:1, text: 'Potatoe'}]},
		{id: 1, text: 'Grains', href: '#2', sub:[{id: 0, text: 'Rice'},
							{id:1, text: 'Bread'}]},
		{id: 2, text: 'Dessert', href: '#3'},
		{id: 3, text: 'Diary', href: '#4'}
	],
	seen: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list {
	margin:0 auto;
	max-width:600px;
	background:#eee;
	padding:10px;
	color:#2d2d2d;
	text-shadow:1px -1px 2px #eee;
}

.drop {
	width:200px;
	background:#ddd;
	padding:5px;
}
ul {
	padding-left:20px;
}
a {
	text-decoration:none;
	color:#2d2d2d;
	transition:color .2s ease-in-out;
}
a:hover {
	color:#999;
}
</style>
