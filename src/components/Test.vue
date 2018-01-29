<template>
  <div class="test">
        <h1>
            {{title}}
        </h1>
        <input type="text" v-model="title"><br/>

        <button v-on:click="greet('Hello World')">Say Greeting</button>

        <p v-if="showName">{{user.first_name}}</p>
        <p v-else="showName">Gud</p>

        <p v-text="user.last_name"/>

        <span v-html="html"/>

        <ul>
            <li v-for="item in items">{{item.title}}</li>
        </ul>

        <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit">

        <hr/>

        <button v-on:click="switchName()">Switch Name</button>

        <input type="text" v-model="user.first_name"/>
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
                    {title: "Item Three"}
                ]                
            }           
        },
        methods: {
            greet: function(greeting){
                alert(greeting);
            },
            pressKey: function (e) {
                console.log(e.target.value);   
            },
            enterHit: function () {
                console.log("You hit enter");
            },
            switchName: function () {
                this.showName = !this.showName;
            }
        } 
    }
</script>

<style scoped>

</style>
