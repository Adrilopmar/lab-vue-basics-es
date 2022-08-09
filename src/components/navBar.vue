<template>
     <div class="container">
        <h2>hey! this should be a nav bar</h2>
        <h2>{{title}}</h2>
    </div>
    <h3>operación matemática sencilla : 2 + 2 = {{2+2}}</h3>
    <div class="it">
    <h4>the string below is from a function</h4>
        <p>{{giveMeString()}}</p>
    </div>
    <div class="it4">
        <h3 v-show="clicked">Now you see me, now you don't!</h3>
        <button @click="helloWorld">click and see what happens </button>
    </div>
    <div class="it5">
        <h2 id="policeNino" :class="swapColor ? 'changingColor':'warningColor'">{{police}}</h2>
        <button  @click="changeColor()">click fast and see what happens</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            title:'This title comes from the data',
            clicked:false,
            stringFromFunction:`I talked to god on the telephone... But I really can't tell you what he told me...but...It was a LIE!`,
            swapColor:false,
            police:'The Police'
        }
    },
    methods:{
        helloWorld(){
            this.clicked =!this.clicked
            // console.log('Hello from the console')
        },
        giveMeString(){
            return this.stringFromFunction
        },
        changeColor(){
            document.getElementById('policeNino').innerHTML +=' nino'
            this.swapColor = !this.swapColor
        }
    }
}
</script>
<style scoped>
.changingColor{
    color: rgb(67, 86, 252);
}
.warningColor{
    color: rgb(228, 3, 3);
}
button{
    font-size: 18px;
    padding: 7px 7px;
}
</style>
