<template>
  <div>
    <img alt="Need a GUID?" src="../assets/need-a-guid.png">
    <h1>{{ message }}</h1>
  <div>
    <span>{{ guid }}</span>
  </div>
    <button v-on:click="generateGuid()">Generate a GUID</button>
  </div>
</template>

<script>
import { uuid } from 'vue-uuid';

export default {
  name: 'GuidMan',
  data() {
    return {
      guid: null,
    }
  },
  methods: { 
    generateGuid() {
      this.guid = uuid.v4()
    }
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
