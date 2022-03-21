
<template>
  <div>
    <h1>{{ title }}</h1>
    <h2>{{ 3 + 3 }}</h2>
    <p v-if="isEnabled">{{ subtitle }}</p>
    <button @dblclick="toggle">トグルする</button>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default{
  data(){
    return {
      title: '初めてのVue.jsアプリです！',
      subtitle: 'ようこそ',
      isEnabled: true
    }
  },

  computed: {
    text(){
      if(this.isEnabled){
        return 'こんにちは！'
      }else{
        return 'さようなら、、'
      }
    }
  },

  methods: {
    toggle(){
      this.isEnabled =! this.isEnabled
    }
  }
}
</script>