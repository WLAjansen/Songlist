<template>
  <header class="header">
    <div class="desc">
      <h1>Playlist</h1>
      <p>Your daily update of the most played tracks right now.</p>
     <p>1 New entry - Last updated: 4 hours ago</p>
      </div>
      <img src="../assets/global.png">
      </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
.header {
    background: #333;
    color: #fff;
    text-align: left;
    padding: 30px 0px 40px 20px;
}

.desc {
  position: absolute;
  left: 25%;
  top: 8%;
}

</style>
