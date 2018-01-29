<template>
  <div class="test">
      <h1>
          {{title}}
      </h1>
      <p>{{user.first_name}}</p>
      <p v-text="user.last_name"/>
      <span v-html="html"/>
  </div>
</template>

<script>
    export default {
        name: "test",
        data(){
            return{
                title: 'Hello World',
                user: {
                    first_name: "john",
                    last_name: "doe"
                },
                html: 'V-test'
            }            
        }
    }
</script>

<style scoped>

</style>
