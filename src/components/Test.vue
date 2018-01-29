<template>
  <div class="test">
      <h1>
          {{title}}
      </h1>
      <p v-if="showName">{{user.first_name}}</p>
      <p v-else="showName">Gud</p>
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
                html: 'V-test',
                showName: false
            }            
        }
    }
</script>

<style scoped>

</style>
