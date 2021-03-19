<template>
  <div id="app">
    <div class="content">

          <chatroom :currentUser="currentUser"></chatroom>
    <userlistcom @chooseuser="toggleuser" :userlist="userlist"></userlistcom>
    </div>

  </div>
</template>

<script>
import chatroom from './components/chatroom.vue'
import userlistcom from './components/userlistcom'


export default {
  name: 'App',
  components: {
    chatroom,userlistcom
     
  },
  data(){
    return {
        userlist:[
          {
            name:'小明',
            img:require('./assets/img/01.jpeg')
          },
          {
            name:'小华',
            img:require('./assets/img/02.jpeg')
          },
          {
            name:'小红',
            img:require('./assets/img/03.jpeg')
          },
          {
            name:'小光',
            img:require('./assets/img/04.jpeg')
          }
         
        ],
        currentUser:{
            name:'小明',
            img:require('./assets/img/01.jpeg')
          }
        
    }
  },
  methods:{
    toggleuser(index){
     this.currentUser=   this.userlist[index]
    } 
  }
}
</script>

<style scoped>
.content{
  display: flex;
  margin: 0 auto;
  width: 800px;
  height: 700px;
}
</style>
