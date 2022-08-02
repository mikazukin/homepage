<template>
  <div class="card_wrap">
    <div class="left_part">
      <slot name="date"></slot>
      <slot name="title"></slot>
    </div>
    <div class="right_part">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.card_wrap {
  width: 80%;
  margin: 0 auto 50px;
  height: 100px;
  border-radius: 10px;
  display: flex;
  box-shadow: 5px 5px 5px 5px gray;
}

.left_part {
  background: green;
  width: 30%;
  height: 100%;
  color: white;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.right_part {
  width: 70%;
  height: 100%;
}
</style>