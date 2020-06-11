Game Monter use vuejs
<div id="app">
  {{ message }}
</div>
<!-- --------------------------------------------------- -->
<div id="app-3">
  <span v-if="seen">Now you see me</span>
</div>
<!-- --------------------------------------------------- -->
<div id="app-5">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>
<!-- --------------------------------------------------- -->
<div id="app-6">
  <p>{{ message }}</p>
  <input v-model="message">
</div>

<script type="text/javascript">
	var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
});
//---------------------------------------------------
var app3 = new Vue({
  el: '#app-3',
  data: {
    seen: true
  }
})
//---------------------------------------------------
var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
//---------------------------------------------------
var app6 = new Vue({
  el: '#app-6',
  data: {
    message: 'Hello Vue!'
  }
})
</script>
