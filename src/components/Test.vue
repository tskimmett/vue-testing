<template>
  <div>
    <h2>Child Component</h2>
    <div v-for="(val, key) in field" :key="key">
      <label>
        {{ key }}
        <input v-model="$props['field'][key]" @input="$emit('updated')" />
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
  },
  methods: {
    update: function(e) {
      console.log("updated");
      this.field.unknown = new Date().toString();
      this.$emit("updated");
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
</style>
