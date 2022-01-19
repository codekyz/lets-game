<template>
<div id="app">
  <LetsHeader></LetsHeader>
  <LetsList></LetsList>
  <LetsInput></LetsInput>
  <LetsFooter></LetsFooter>
</div>
  

</template>

<script>
import LetsHeader from './components/LetsHeader'
import LetsList from './components/LetsList'
import LetsInput from './components/LetsInput'
import LetsFooter from './components/LetsFooter'

export default {
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