<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Mega Essential Stuff</h2>
    <ul>
      <div>
        <ul>
        <li>These guys were totally in the Beatles:</li>
          <li v-for="user in users">
        {{user.firstName}} {{user.lastName}}
        </li>
        </ul>
        </div>

        <div>
          <input type="text" v-model="input_val">
        </div>

        <div>
          Input Value: <span v-text="input_val"></span>


        </div>
      
      <br>
    </ul>
    <h2>Stuff</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
      <li><a href="http://github.com/jasonvandewarker" target="_blank">Git Hub</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'This is from within the data object. I added the members of the Beatles for no reason.',
      users: [
        {firstName: 'Paul', lastName: 'McCartney'},
        {firstName: 'John', lastName: 'Lennon'},
        {firstName: 'George', lastName: 'Harrison'},
        {firstName: 'Ringo', lastName: 'Starr'},
      ],
      input_val: '',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
