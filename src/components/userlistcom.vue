<template>
    <div class="userlist">

       <p>头像</p>
     
       <ul>
           <li v-for="(item,index) in userlist" @click="chooseuser(index)" :key="index">
               <img :src="item.img" alt="">
                 <p>{{item.name}}</p>
           </li>
     
       </ul>
    </div>
</template>

<script>
export default {
    data () {
        
      return {}
    },
    props:['userlist'],

    methods: {
        chooseuser(index){
           this.$emit('chooseuser',index)
        }
    },

    components: {},
}
</script>

<style scoped>


.userlist{
    width: 300px;
    height: 700px;
    background: skyblue;
      border: 1px solid black;
}
.userlist ul li{
    display: flex;
    flex-direction: row;
}
.userlist ul li img{
    width: 80px;
    height: 80px;
}
</style>