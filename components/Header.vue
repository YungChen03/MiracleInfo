<template>
  <div class="container">
    <div class="logo">
      <img src="../assets/img/pngwing.com.png" />
    </div>
    <div class="search">
      <input v-if="isActive" class="searchbar" type="text" />
      <div class="search-icon" @click="toggleSearchBar">
        <span class="material-icons">search</span>
      </div>
      <div class="avatar">
        <img src="../assets/img/m.svg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleSearchBar() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
}
.container {
  height: 10vh;
  width: 95%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  border-bottom: 5px solid #ddd;
}

.logo {
  img {
    height: 5vh;
  }
}
.search {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 0 5px;

  input {
    height: 20px;
    width: 80%;
    border-radius: 50px;
    outline: none;
    margin: 0 5px;
  }

  .material-icons {
    cursor: pointer;
    font-size: 24px;
    margin: 0 10px;
  }
}
.avatar {
  img {
    height: 5vh;
  }
}
</style>
