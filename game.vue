<template>
  <div>
  <p>HP player{{randomNo(1,3)}}</p>
  {{player [randomNo(1,3-1)].name}}
  <p v-bind: style="font-size:fsize+'px'">{{game}}HELLO</p>
  +image
  <p>HP Monster 150</p>
   +image
  <button @click="start()">start</button>
  <button @click="attack()">Attack</button>
</div>
</template>

<script>
export default {
data: function() {
    return{
        // ชื่อ
   player: [
       {name: 'Anakin', hp: 90, image:''},
       {name: 'Iron Man', hp: 90, image:''},
       {name: 'Doremon', hp: 90, image:''},
   ],
   monster: [
       {name: 'thanos', hp: 90, image:''},
       {name: 'logi', hp: 90, image:''},
       {name: 'joker', hp: 90, image:''}
   ]

  }
},







props:{
    lable: String,
},
methods: {
    randomNo: function(min,max){
        return Math.max(Math.floor(Math.random() * max) + 1, min)
    },
start: function() {
    //random player 1-3 --> ชื่อ hp image
    this.aPlayer = this.player[this.randomNo(1,3)-1]
     //(...)
      //2. random Monster 1-3

  },
attack: function(){
     //1.player --> monster
     //2.player --> monster
     //3.player,HP <=0 ===> ?
     //4.monster,HP <=0 ==>
     //5.END GAME
}
}
</script>

}
<style>

</style>