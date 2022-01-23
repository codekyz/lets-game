<template>
  <header>

      <h1>
          게임 언제할래?
      </h1>

      <button class="clear_btn" v-on:click="clear">clearAll</button>

  </header>
</template>

<script>
export default {
    methods: {
        clear() {
            this.$emit('clear');
        }
    }
}
</script>

<style scoped>
header {
    display: flex;
    align-items: baseline;
}

h1 {
    margin: 30px 30px;
}

.clear_btn {
    padding: 5px 10px;
    margin: 0 30px 30px auto;
    box-sizing: border-box;
}



</style>