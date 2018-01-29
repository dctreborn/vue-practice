<template>
  <div class="test">
      <h1>
          {{title}}
      </h1>
      <p v-if="showName">{{user.first_name}}</p>
      <p v-else="showName">Gud</p>
      <p v-text="user.last_name"/>
      <span v-html="html"/>
      <ul>
          <li v-for="item in items">{{item.title}}</li>
      </ul>
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
                showName: false,
                items: [
                    {title: "Item One"},
                    {title: "Item Two"},
                    {title: "Item Three"},
                ]
            }            
        }
    }
</script>

<style scoped>

</style>
