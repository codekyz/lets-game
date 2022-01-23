<template>
<div id="app">
  <LetsHeader v-on:clear="clearAll"></LetsHeader>

  <LetsList 
    v-bind:monUserList="monUser" :tueUserList="tueUser"
    :wedUserList="wedUser" :thuUserList="thuUser"
    :friUserList="friUser" :satUserList="satUser"
    :sunUserList="sunUser"></LetsList>

  <LetsInput 
    v-on:addSchedule="addUserSchedule"></LetsInput>

  <LetsFooter></LetsFooter>
</div>
  

</template>

<script>
import LetsHeader from './components/LetsHeader'
import LetsList from './components/LetsList'
import LetsInput from './components/LetsInput'
import LetsFooter from './components/LetsFooter'

export default {
  data: () => {
    return {
      monUser: [],
      tueUser: [],
      wedUser: [],
      thuUser: [],
      friUser: [],
      satUser: [],
      sunUser: []
    }
  },

  methods: {
    addUserSchedule(userName, yoilList) {
      for (let i = 0; i < yoilList.length; i++) {     
        if (yoilList[i].checked && yoilList[i].yoil == '월') {
          this.monUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '화') {
          this.tueUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '수') {
          this.wedUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '목') {
          this.thuUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '금') {
          this.friUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '토') {
          this.satUser.push(userName);
        }
        if (yoilList[i].checked && yoilList[i].yoil == '일') {
          this.sunUser.push(userName);
        }
      }
    },

    clearAll() {
      this.monUser = [];
      this.tueUser = [];
      this.wedUser = [];
      this.thuUser = [];
      this.friUser = [];
      this.satUser = [];
      this.sunUser = [];
    }
  },

  components: {
    LetsHeader,
    LetsList,
    LetsInput,
    LetsFooter,
  }

}
</script>

<style>

body {
  margin: 0;
  background-color: #e7e7e7;
  font-family: 'GmarketSansMedium';
}

button {
  border: 1px solid #bbb;
  border-radius: 3px;
  background-color: #F29991;
  color: #FFF;
  font-family: 'GmarketSansMedium';
  cursor: pointer;
}

input {
  border: 1px solid #bbb;
  border-radius: 5px;
  font-family: 'GmarketSansMedium';
}

.shadow {
  box-shadow: 3px 5px 5px rgba(0, 0, 0, 15%);
}

</style>