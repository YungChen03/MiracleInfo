<template>
  <div class="container">
    <div class="navbar">
      <div class="logo">
        <img src="../assets/img/pngwing.com.png" />
      </div>
      <div class="search-wrap">
        <input v-if="isActive" class="searchbar" type="text" />
        <div class="search-icon" @click="toggleSearchBar">
          <span class="material-icons">search</span>
        </div>
        <div class="avatar">
          <img src="../assets/img/m.svg" />
        </div>
      </div>
    </div>

    <div class="badge-wrap">
      <div class="badge" v-for="badge in badges" :key="badge.topic">
        <div class="text">{{ badge.topic }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
      badges: [
        {
          topic: "全部"
        },
        {
          topic: "音樂"
        },
        {
          topic: "直播中"
        },
        {
          topic: "棒球"
        },
        {
          topic: "自然"
        },
        {
          topic: "烹飪節目"
        },
        {
          topic: "健身"
        },
        {
          topic: "視覺藝術"
        },
        {
          topic: "最新上傳"
        },
        {
          topic: "已觀看"
        }
      ]
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
.container {
  position: fixed;
  z-index: 100;
  width: 100%;
}
.navbar {
  height: 9vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 5px;
  border-bottom: 3px solid #ddd;
  background-color: #fff;
  transform: translateY(-8px) translateX(-8px);
}

.logo {
  img {
    height: 5vh;
    margin-left: 10px;
  }
}
.search-wrap {
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
    margin-right: 15px;
  }
}
.badge-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 4vh;
  width: 100%;
  padding: 10px;
  background-color: #fff;
  transform: translateY(-8px);
  text-align: center;
  .badge {
    min-width: 65px;
    margin: 1rem;
    padding: 0.25rem 0.5rem;
    background-color: #eee;
    border-radius: 50px;
    cursor: pointer;
    max-height: 21px;

    &:nth-child(1) {
      color: white;
      background-color: black;
    }
  }
}

@media screen and (max-width: 900px) {
  .badge-wrap {
    width: 200%;
    justify-content: flex-start;
  }
}
@media screen and (max-width: 1200px) {
  .badge-wrap {
    width: 120%;
  }
}
</style>
