<template>
  <section class="list">
    <ul class="listHeader">
      <li>월요일</li>
      <li>화요일</li>
      <li>수요일</li>
      <li>목요일</li>
      <li>금요일</li>
      <li>토요일</li>
      <li>일요일</li>
    </ul>

    <div class="listUser">
      <ul>
        <li v-for="user in monUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in tueUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in wedUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in thuUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in friUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in satUserList"
          v-bind:key="user">
          {{ user }}
        </li>
      </ul>
      <ul>
        <li v-for="user in sunUserList"
          v-bind:key="user">
          {{ user }}
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
}

.listHeader li {
  flex: 1 1 0;
  padding: 10px 20px;
  background-color: #D9D8D7;
  box-sizing: border-box;
}

.listUser {
  display: flex;
}


.listUser ul {
  flex: 1 1 0;
  padding: 10px 20px;
  background-color: #F29991;
  box-sizing: border-box;
}

</style>