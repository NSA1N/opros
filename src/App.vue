<template>
  <div id="app">
    <section> 
      <h2>Как зовут твоих друзей?</h2>
      <input type="checkbox" id="sasha" value="Саша" v-model="checkedNames">
      <label for="sasha">Саша</label>
      <input type="checkbox" id="olya" value="Оля" v-model="checkedNames">
      <label for="olya">Оля</label>
      <input type="checkbox" id="sanchepezdol" value="Санчепездол" v-model="checkedNames">
      <label for="sanchepezdol">Санчепездол</label>
      <p>Выбрано: {{checkedNames}}</p>
      <br>
    </section>

    <section>
      <h2>Сколько у тебя IQ?</h2>
      <input type="radio" id="one" value="Меньше среднего" v-model="picked">
      <label for="low">Ниже среднего</label>
      <br>
      <input type="radio" id="two" value="Средний уровень" v-model="picked">
      <label for="medium">Средний уровень</label>
      <br>
      <input type="radio" id="three" value="Выше среднего" v-model="picked">
      <label for="high">Выше среднего</label>
      <br>
      <input type="radio" id="four" value="Я уникум" v-model="picked">
      <label for="cosmo">Я уникум</label>
      <br>
      <span>Выбрано: {{ picked }}</span>
      <br>
      <br>
    </section>
    <section>
      <h2>Что ты любишь?</h2>
      <select v-model="selected">
        <option disabled value="">Выберите один из вариантов</option>
        <option>Frontend</option>
        <option>Backend</option>
        <option>Okoloend</option>
      </select>
      <br>
      <br>
      <span>Выбрано: {{ selected }}</span>
      <br>
    <br>
</section>

<h2>Как зовут твоего лучшего друга?</h2>
<select name="" id="" v-model="selecteded">
  <option v-bind:key="name.value" 
  v-for="name in names">
    {{ name.text }}
  </option>
</select>
<br>
<span>Выбрано: {{selecteded}}</span>
<br>
<br>

  </div>
</template>

<script>
export default {
  name: 'App',
  
  data() {
    return {
      checkedNames: [],
      picked: "",
      selected: '',
      selecteded: '',
      names: [
        {text: 'Саша', value: '0'},
        
      ]
    }
  },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: rgb(238,174,202);
  background: radial-gradient(circle, rgba(238,174,202,1) 0%, rgba(148,187,233,1) 100%);
  text-align: center;
  
}
</style>