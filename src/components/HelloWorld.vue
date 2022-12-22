<template>
  <div>
    <input type="text" placeholder="enter ip address" @change="apiCall()" />
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {};
  },
  methods: {
    apiCall() {
      fetch("http://ip-api.com/json/24.48.0.1")
        .then((response) => response.json())
        .then((data) => console.log(data));
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
