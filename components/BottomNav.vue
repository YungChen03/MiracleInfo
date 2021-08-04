<template>
  <div class="bottomnav">
    <div class="container">
      <button>
        <span class="material-icons">home</span>
        <div>Home</div>
      </button>

      <button>
        <span class="material-icons">whatshot</span>
        <div>Trending</div>
      </button>

      <button>
        <span class="material-icons">email</span>
        <div>Subscriptions</div>
      </button>

      <button>
        <span class="material-icons">archive</span>
        <div>Library</div>
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  position: fixed;
  background-color: white;
  display: flex;
  justify-content: space-around;
  width: 100%;
  height: 10vh;
  border-top: 1px solid #ddd;

  button {
    border: 0;
    background-color: white;
    cursor: pointer;
  }
}
</style>
