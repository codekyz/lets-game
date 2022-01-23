<template>
  <section class="insert">
      <article class="inputs">
        <input type="text" v-model="userName" class="shadow" placeholder="이름을 입력하세요">
      </article>
      
      <ul>
          <li v-for="yoilItem in yoilList" 
            v-bind:key="yoilItem.yoil"
            v-bind:class="{checked: yoilItem.checked}" 
            v-on:click="toggleYoil(yoilItem)">
            {{ yoilItem.yoil }}
          </li>
      </ul>

      <button v-on:click="addSchedule(userName, yoilList)">add</button>
  </section>
</template>

<script>
export default {
    data() {
        return {
            yoilList : [ {yoil:'월', checked:false},
                {yoil:'화', checked:false},
                {yoil:'수', checked:false},
                {yoil:'목', checked:false},
                {yoil:'금', checked:false},
                {yoil:'토', checked:false},
                {yoil:'일', checked:false}, ],
                
            userName: ''
        }
    },
    methods: {
        addSchedule(userName, yoilList) {
            if(this.userName !== '') {
                this.$emit('addSchedule', userName, yoilList);
                this.clearInput();
            }
        },

        clearInput() {
            this.userName = '';
        },
        toggleYoil(yoilItem) {
            yoilItem.checked = !yoilItem.checked;
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

.inputs input {
    padding: 10px 15px;
    margin-top: 30px;
    font-size: 16px;
}

ul {
    display: flex;
    list-style-type: none;
    margin: 0 0 30px 0;
    padding: 0;
}

ul li {
    padding: 10px 15px;
    background-color: #D9D8D7;
    cursor: pointer;
}

/* ul li:nth-child(even) {
    background-color: #ebebeb;
} */

.checked {
    background-color: #F29991;
    color: #FFF;
}

button {
    padding: 15px 30px ;
    margin-bottom: 30px;
}

</style>