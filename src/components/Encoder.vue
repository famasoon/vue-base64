<template>
  <div class="encoder">
    <h1>Vue base64 encoder</h1>
    <textarea name="encode" id="encoderbox" cols="30" rows="10" v-model="text"></textarea>
    <p>{{ b64Encode }}</p>
  </div>
</template>

<script>
export default {
  name: 'Encoder',
  data() {
    return {
      text: ''
    }
  },
  computed: {
    b64Encode: function() {
      return btoa(encodeURIComponent(this.text).replace(/%([0-9A-F]{2})/g,
        function toSolidBytes(match, p1) {
          return String.fromCharCode('0x' + p1);
      }));
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
    font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
    top: 0;
    right: 0;
    color: #34495e;
    font-size: 0.9em;
    padding: 5px 10px 0;
    line-height: 15px;
    height: 15px;
    font-weight: 600;
    word-wrap: break-word;
}
</style>
