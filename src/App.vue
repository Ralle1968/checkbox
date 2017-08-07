<template>
  <div id="app">
    <label>Text anzeigen</label>
    <input type="checkbox" value="ralf" v-model="displayText" @click="testClick"/>
    <div id="display">
      <p v-if='displayText'>Thats Ralf!!!</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      displayText: false,
      count: 1
      }
  },
  methods: {
    testClick: function(){
      console.log("Ich bin zum "+ this.count + " mal getriggert worden aus der Checkbox ");
      this.count++;
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

a {
  color: #42b983;
}
</style>
