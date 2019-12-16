<template>
  <div id="app">
    {{msg}}
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {

  },
  data(){
    return {
      tdos: [
        {
          id: 1,
          title: 'Todo one',
          completed: false
        },
        {
          id: 2,
          title: 'todo two',
          completed: false
        },
        {
          id: 3,
          title: 'todo three',
          completed: false
        }
      ]
    }
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box
  }

  body{
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>
