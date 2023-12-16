<template>
  <div class="hello">
    <h1><span style="color: blueviolet;">Topic:{{ msg }}</span></h1>

    <h4>Name:{{ name }}</h4>
    
    
    <p><button v-on:click="counter++">Count ++</button></p>
    <p><button v-on:click="counter--" v-if="counter>0">Count --</button></p>
    <p>Counting: {{ counter }}</p>   
    
    
    <input type="text" v-model="myName" placeholder="Enter text">
    <p>{{ myName }}</p> 

    <p>V-for </p>
    <ul>
      <li v-for="(country, index) in countries" :key="index">{{ country }}</li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
        name : 'Afzal',
        counter:0,
        myName: '',
        countries: ['Pakistan','Iran','Turkey']
    }
  }
}
</script>