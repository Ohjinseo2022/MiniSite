<template>
  <div class="loginBox">
    <div class="innerBox">
      <div class="inputBox">
        <label for="idinput">
          <font-awesome-icon class="icon" icon="fa-solid fa-user" /></label
        ><input
          id="idinput"
          type="text"
          @keyup.enter="onSubmit()"
          @input="oninputId()"
          v-model="id"
        />
        <span :class="{ clear: clearid, warning: true }">*</span>
      </div>
      <div class="inputBox">
        <label for="pwdinput">
          <font-awesome-icon class="icon" icon="fa-solid fa-lock" /></label
        ><input
          id="pwdinput"
          type="password"
          @keyup.enter="onSubmit()"
          @input="oninputPwd()"
          v-model="pwd"
        /><span :class="{ clear: clearpwd, warning: true }">*</span>
      </div>
      <div>
        <button class="loginbtn">
          로&nbsp;&nbsp;&nbsp;&nbsp;그&nbsp;&nbsp;&nbsp;&nbsp;인
        </button>
      </div>
      <div>
        <ul class="moreLogin">
          <li>
            <button class="kakao"></button>
          </li>
          <li>2</li>
          <li>3</li>
          <li>4</li>
        </ul>
      </div>
      <div></div>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      id: '',
      pwd: '',
      clearid: 0,
      clearpwd: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},

  computed: {},
  methods: {
    oninputId() {
      this.clearid = this.id === '' ? 0 : 1
    },
    oninputPwd() {
      this.clearpwd = this.pwd === '' ? 0 : 1
    },
    onSubmit() {
      console.log(this.id + this.pwd)
    }
  }
}
</script>
<style scoped>
.loginBox {
  width: 400px;
  margin: 150px auto;
  height: 300px;
  box-shadow: 3px 3px 3px 3px #8f49cb;
}
.innerBox {
  position: absolute;
}
.box {
  text-align: center;
  margin-bottom: 30px;
}

.moreLogin {
  width: 183px;
  list-style: none;
  margin: 0 auto;
}

.loginbtn {
  width: 183px;
  height: 45px;
  border: 0px;
  background-color: #b52aff;
  border-radius: 5px;
}
.loginbtn:active {
  background-color: #7f00cb;
}
.kakao {
  background-image: url('@/img/kakao_login_medium_narrow.png');
  background-size: cover;
  width: 183px;
  height: 45px;
  border: 0;
}

.kakao:hover {
  cursor: pointer;
}
input {
  border: 0;
  outline: none;
  width: 220px;
  font-size: 20px;
  margin-left: 10px;
}
.inputBox {
  border: 1px solid #7f00cb;
  height: 40px;
  width: 250px;
  position: relative;
  display: flex;

  justify-content: center;
  align-items: center;
  padding-left: 16px;
  margin: 15px;
}

.icon {
  color: #f7a9ff;
}

.warning {
  position: absolute;
  left: 25px;
  top: 5px;
  color: red;
}

.clear {
  display: none;
}
</style>
