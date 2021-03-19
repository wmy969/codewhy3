<template>
    <div class="chat">
        <p>聊天室</p>
        <p>用户:{{currentUser.name}}</p>
        
        <chatlist></chatlist> 
        <chatitem></chatitem>
    </div>
</template>

<script>
import chatlist from './chatlist'
import chatitem from './chatitem'
export default {
    props:['currentUser'],
    data () {
      return {}
    },

    methods: {},

    components: {
        chatlist,chatitem}
}
</script>

<style scoped>

.chat{
    width: 500px;
    height: 700px;
    border: 1px solid red;
}
</style>