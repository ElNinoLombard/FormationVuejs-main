<template>
  <div>
      <button @click="greet">Greet</button>
      <span>{{ total }}</span>
  </div>
  
</template>
<script>
export default {
  name : 'MethodsExample',
  data() {
    return  {
      name: 'Mark',
      count1: 0,
      count2: 0,
      lastUpdate: null
    }
  },
  methods: {
    greet() {
      this.count1=12
      this.say('Hi '+ this.name)
    },
    say(message){
      alert(message + '!')
    }
    
  },
  computed: {
    total () {
      return this.count1 + this.count2
    }
  },
  watch: {
    total() {
      this.lastUpdate = new Date()
    }
  }
}
</script>