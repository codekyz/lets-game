<template>
  <section class="list">
    <ul class="listHeader">
      <li>월</li>
      <li>화</li>
      <li>수</li>
      <li>목</li>
      <li>금</li>
      <li>토</li>
      <li>일</li>
    </ul>

    <div class="listUser">
      <ul>
        <li v-for="user in monUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in tueUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in wedUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in thuUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in friUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in satUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
      <ul>
        <li v-for="user in sunUserList"
          v-bind:key="user">
          {{ user ? user : no }}
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  props: ['monUserList', 'tueUserList', 'wedUserList', 'thuUserList', 
  'friUserList', 'satUserList', 'sunUserList'],

  data: function() {
    return {
      no : '0'
    }
  }
}
</script>

<style scoped>
.list {
  width: 100%;
  display: flex;
  flex-direction: column;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.listHeader {
  display: flex;
  justify-content: space-between;
  margin-left: 30px;
  margin-right: 30px;
}

.listHeader li {
  padding: 10px 20px;
  background-color: #D9D8D7;
}

.listUser {
  display: flex;
  justify-content: space-between;
  margin-left: 30px;
  margin-right: 30px;
}

.listUser ul li {
  padding: 10px 20px;
  background-color: #F29991;
}

</style>