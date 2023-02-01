<template>
  <div class="headerBody">
    <nav>
      <ul>
        <li>즐겨찾기&nbsp;|&nbsp;</li>
        <li>이용가이드&nbsp;|&nbsp;</li>
        <li>오늘날짜</li>
      </ul>
      <ul>
        <li>로그인&nbsp;|&nbsp;</li>

        <li>회원가입&nbsp;|&nbsp;</li>

        <li>1:1 문의</li>
      </ul>
    </nav>
    <br />
    <br />
    <div class="searchBox">
      <div>로고!</div>
      <div :class="{ search: true, searchBorder: focus, searchfocus: !focus }">
        <input
          class="searchbar"
          v-model="search"
          @focus="choutline()"
          @blur="choutline()"
          type="text"
        />
        <button>
          <font-awesome-icon
            style="font-size: 20px; color: #7f00cb"
            icon="fa-solid fa-magnifying-glass"
          />
        </button>
      </div>
    </div>

    <div class="categoryBar">
      <div>
        <router-link to="/"
          ><font-awesome-icon style="color: #f6f3f3" icon="fa-solid fa-house"
        /></router-link>
      </div>
      <ul class="menu">
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      sampleData: '',
      focus: true,
      search: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    choutline() {
      this.focus = !this.focus
    }
  }
}
</script>
<style scoped>
.headerBody {
  width: 100%;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 7px;
}

nav > ul {
  display: flex;
  list-style: none;
}

.searchBox {
  display: flex;
  margin: 7px;
  justify-content: center;
  align-items: center;
}
.searchBox > div {
  margin: 5px;
}
.search {
  height: 35px;
  border-radius: 5px;
}
.searchBorder {
  border: 3px solid #ec65ff;
}
.searchfocus {
  border: 3px solid #7f00cb;
}
.searchbar {
  outline-style: none;
  font-size: 22px;
  width: 200px;
  border: 0;
}
button {
  width: 27px;
  height: 27px;
  border: 0;
}

.categoryBar {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 50px;
  background: #8f49cb;
}
.menu {
  display: flex;
  list-style: none;
  justify-content: space-around;
  width: 90%;
}
</style>
