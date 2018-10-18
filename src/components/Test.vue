<template>
  <div>
    <h2>Child Component</h2>
    <aside>edit the fields</aside>
    <div class="field" v-for="(val, key) in field" :key="key">
      <label>
        {{ key }}
        <input v-model="$props['field'][key]" />
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: "Test",
  props: {
    field: {
      type: Object
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
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
label {font-weight: bold;}

.field:not(:first-child) {margin-top: 10px;}

input {border-radius: 3px; border: solid 1px #aaa; padding: 4px; }

aside {font-size: 12px;}
</style>
