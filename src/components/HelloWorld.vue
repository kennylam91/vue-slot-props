<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <current-user>
      <template v-slot="slotProps">
        {{slotProps.user.firstName}}
      </template>
    </current-user>

    <current-user>
      <template v-slot="slotProps">
        {{slotProps.user.lastName}}
      </template>
    </current-user>
    
  </div>
</template>

<script>
import CurrentUser from './CurrentUser'
export default {
  name: 'HelloWorld',
  components:{CurrentUser},
  props: {
    msg: String
  }
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
