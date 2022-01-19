<template>
  <section class="insert">
      <article class="inputs">
        <input type="text" v-model="userName" class="shadow" placeholder="이름을 입력하세요">
        <input type="color" v-model="userColor" class="shadow">
      </article>
      
      <ul>
          <li class="checked">월</li>
          <li>화</li>
          <li>수</li>
          <li>목</li>
          <li>금</li>
          <li>토</li>
          <li>일</li>
      </ul>

      <button>add</button>
  </section>
</template>

<script>
export default {
    data: function() {
        return {
            userName: '',
            userColor: ''
        }
    }
}
</script>

<style scoped>

.insert {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.inputs {
    display: flex;
    align-items: center;
    margin: 20px 0;
}

.inputs input[type=text] {
    padding: 10px 15px;
    margin-right: 10px;
    font-size: 16px;
}

ul {
    display: flex;
    list-style: none;
    margin: 0 0 30px 0;
    padding: 0;
}

ul li {
    padding: 10px 15px;
    background-color: #D9D8D7;
    cursor: pointer;
}

ul li:nth-child(even) {
    background-color: #ebebeb;
}

.checked {
    background-color: #F29991;
    color: #FFF;
}

button {
    padding: 15px 30px ;
    margin-bottom: 30px;
}

</style>