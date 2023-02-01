<template>
  <div class="loginBox">
    <div><input type="text" /></div>
    <div><input type="password" /></div>
    <div><button></button></div>
    <div>
      <ul>
        <li>
          <ToggleButton />
        </li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>
    <div></div>
  </div>
</template>
<script>
import ToggleButton from '../element/ToggleButton.vue'
export default {
  components: { ToggleButton },
  data() {
    return {
      sampleData: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
<style scoped>
.loginBox {
  width: 400px;
  margin: 150px auto;
  height: 300px;
  box-shadow: 3px 3px 3px 3px #8f49cb;
}
.box {
  text-align: center;
  margin-bottom: 30px;
}
</style>
