<template>
  <div id="app">
    <label v-bind:class="{ red: checked }">Text anzeigen</label>
    <input type="checkbox" value="true" v-model="checked" @click="testClick"/>
    <div id="display">
      <p>{{ checked }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      checked: false,
      count: 1
      }
  },
  methods: {
    testClick: function(){
      console.log(this.checked);
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
  font-size: 20px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

.red {
  color: red;
}
</style>
